---
title: 'Dettagli di progettazione: Gestione dei metodi di riordino | Microsoft Docs'
description: Panoramica dei task per la definizione di un metodo di riordino nella pianificazione dell'approvvigionamento.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 69f9f1f2f63e1d16ec1ef4980c00d21bada06166
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245782"
---
# <a name="design-details-handling-reordering-policies"></a>Dettagli di progettazione: Gestione dei metodi di riordino
Affinché un articolo partecipi alla pianificazione dell'approvvigionamento, i metodi di riordino devono essere definiti. Sono disponibili i seguenti quattro metodi di riordino:  

* Qtà Riordino Fissa  
* Qtà Massima  
* Ordine  
* Lotto-per-Lotto  

I motivi Qtà Riordino Fissa e Qtà massima sono relativi alla pianificazione del magazzino. Sebbene la pianificazione del magazzino sia tecnicamente più semplice della procedura di contropartita, questi criteri devono coesistere con la contropartita dettagliata della tracciabilità di approvvigionamento e ordine. Per controllare l'integrazione tra i due e fornire visibilità nella logica di pianificazione, rigidi principi controllano la gestione dei metodi di riordino.  

## <a name="the-role-of-the-reorder-point"></a>Il ruolo del punto di riordino
Oltre alla contropartita generale di approvvigionamento e domanda, il sistema di pianificazione deve inoltre monitorare i livelli di magazzino per gli articoli interessati in modo che siano rispettati i metodi di riordino definiti:  

Un punto di riordino rappresenta la domanda durante il lead time. Quando la giacenza disponibile scende sotto il livello di magazzino definito dal punto di riordino, è tempo di ordinare una maggiore quantità. Nel frattempo, si prevede una diminuzione graduale della giacenza, che possibilmente raggiunge lo zero (o il livello di scorta di sicurezza), finché non arriva il rifornimento.  

Di conseguenza, il sistema di pianificazione suggerirà un ordine di approvvigionamento programmato in avanti alla fase in cui la giacenza prevista passa al di sotto del punto di riordino.  

Il punto di riordino riflette un determinato livello di magazzino. Tuttavia, i livelli di magazzino possono spostarsi in modo significativo nell'intervallo di tempo e, pertanto, il sistema di pianificazione deve costantemente monitorare le scorte disponibili previste.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Monitoraggio del livello di giacenza disponibile e del punto di riordino
Il magazzino è un tipo di approvvigionamento, ma per la pianificazione del magazzino, il sistema di pianificazione distingue tra due livelli di magazzino:  

* Quantità scorte previste  
* Scorte disponibili previste  

### <a name="projected-inventory"></a>Quantità scorte previste  
Inizialmente, la giacenza disponibile corrisponde alla quantità di giacenza lorda, inclusi approvvigionamento e domanda passati anche se non registrati, all'avvio del processo di pianificazione. In futuro, diventa un livello di giacenza disponibile mobile che viene mantenuto dalle quantità lorde di approvvigionamenti e domande futuri perché sono introdotte seguendo la linea del tempo (se impegnate o allocate in altri modi).  

La giacenza disponibile viene utilizzata dal sistema di pianificazione per monitorare il punto di riordino e per determinare la quantità di riordino quando viene utilizzato il metodo di riordino Qtà Massima.  

### <a name="projected-available-inventory"></a>Scorte disponibili previste  
Le scorte disponibili previste sono la parte della giacenza disponibile che in un dato momento è disponibile per soddisfare la domanda. Le scorte disponibili previste vengono utilizzate dal motore di pianificazione durante il monitoraggio del livello della scorta di sicurezza.  

Le scorte disponibili previste vengono utilizzate dal sistema di pianificazione per monitorare il livello di scorta di sicurezza, dal momento che la scorta di sicurezza deve essere sempre disponibile per servire la domanda imprevista.  

### <a name="time-buckets"></a>Intervalli di tempo  
È importante disporre di un controllo stretto delle scorte previste per rilevare quando viene raggiunto il punto di riordino e per calcolare le giuste quantità dell'ordine quando si utilizza il metodo di riordino Qtà massima.  

Come dichiarato in precedenza, il livello di magazzino previsto viene calcolato all'inizio del periodo di pianificazione. È un livello lordo che non considera gli impegni e le allocazioni simili. Per monitorare il livello di magazzino durante la sequenza di pianificazione, le modifiche aggregate vengono monitorate dal sistema nell'arco di un intervallo di tempo. Il sistema garantisce che l'intervallo di tempo sia almeno di un giorno perché è l'unità di tempo più precisa in caso di un evento di approvvigionamento o di domanda.  

### <a name="determining-the-projected-inventory-level"></a>Determinazione del livello di magazzino previsto  
Nella seguente sequenza viene descritto in che modo viene determinato il livello di giacenza disponibile:  

* Quando un evento di approvvigionamento, ad esempio un ordine di acquisto, è stato completamente pianificato, la giacenza disponibile verrà aumentata alla data di scadenza.  
* Una volta che un evento di domanda è stato completamente soddisfatto, la giacenza disponibile non diminuirà immediatamente. In alternativa, registra un sollecito di diminuzione, ovvero un record interno che contiene la data e la quantità di contributo alla giacenza disponibile.  
* Quando un evento di approvvigionamento successivo viene pianificato e collocato nella sequenza temporale, i solleciti di riduzione registrati vengono analizzati singolarmente fino alla data di approvvigionamento pianificata durante l'aggiornamento della giacenza disponibile. Durante il processo, potrebbe essere raggiunto o superato il livello del punto di riordino del sollecito di incremento interno.  
* Se viene immesso un nuovo ordine di approvvigionamento, nel sistema viene controllato se tale ordine viene immesso prima dell'approvvigionamento corrente. In questo caso, il nuovo approvvigionamento diventa l'approvvigionamento corrente e la procedura di contropartita rincomincia.  

Di seguito viene illustrato questo principio:  

![Determinazione del livello di magazzino previsto](media/nav_app_supply_planning_2_projected_inventory.png "Determinazione del livello di magazzino previsto")  

1. L'approvvigionamento **Sa** di 4 (fisso) chiude la domanda **Da** di -3.  
2. CloseDemand: Creare un sollecito di riduzione di -3 (non visualizzato).  
3. L'approvvigionamento **Sa** viene chiuso con un surplus di 1 (non esiste più domanda).  

     Ciò aumenta il livello di scorte previste a +4, mentre la giacenza **disponibile** diventa -1.  

4. Il successivo approvvigionamento **Sb** di 2 (un altro ordine) è già stato immesso nella sequenza temporale.  
5. Il sistema controlla se esiste un sollecito di riduzione precedente a **Sb**; in caso negativo, non viene intrapresa alcuna azione.  
6. Il sistema chiude l'approvvigionamento **Sb** (non esiste più domanda) riducendolo a 0 (annullamento) o lasciandolo invariato.  

     Ciò aumenta il livello del magazzino previsto (A: +0 => +4 o B: +2 = +6).  

7. Il sistema esegue un controllo finale: è presente un sollecito di riduzione? Sì, ne esiste uno alla data di **Da**.  
8. Viene aggiunto un sollecito di diminuzione dal sistema di -3 al livello di giacenza disponibile, A: +4 -3 = 1 o B: +6 -3 = +3.  
9. Nel caso di A, il sistema crea un ordine programmato in avanti che inizia alla data indicata di **Da**.  

     Nel caso di B, viene raggiunto il punto di riordino e viene creato un nuovo ordine.

## <a name="the-role-of-the-time-bucket"></a>Il ruolo dell'intervallo di tempo
Lo scopo dell'intervallo di tempo è di raccogliere gli eventi di domanda nell'intervallo di tempo in modo da creare un ordine di approvvigionamento congiunto.  

Per i metodi di riordino che utilizzano un punto di riordino, è possibile definire un intervallo di tempo. In questo modo si garantisce che la domanda nello stesso periodo di tempo venga accumulata prima di controllare l'impatto sulla giacenza disponibile e se il punto di riordino sia stato superato. Se il punto di riordino è passato, viene programmato un nuovo ordine di approvvigionamento in una data successiva dalla fine del periodo definito dall'intervallo di tempo. Gli intervalli di tempo iniziano con la data di inizio pianificazione.  

Il concetto di attività in un intervallo di tempo riflette il processo manuale di controllo del livello di magazzino su base frequente anziché ad ogni transazione. L'utente deve definire la frequenza (intervallo di tempo). Ad esempio, l'utente raccoglie tutte le esigenze dell'articolo da un fornitore per inserire un ordine settimanale.  

![Esempio di pianificazione basata su intervallo di tempo](media/nav_app_supply_planning_2_reorder_cycle.png "Esempio di pianificazione basata su intervallo di tempo")  

L'intervallo di tempo viene in genere utilizzato per evitare un effetto di sovrapposizione. Ad esempio, una riga equilibrata di approvvigionamento e domanda dove una domanda iniziale viene annullata o ne viene creata una nuova. Il risultato sarebbe che ogni ordine di approvvigionamento (eccetto l'ultimo) viene riprogrammato.

## <a name="staying-under-the-overflow-level"></a>Al di sotto del livello di overflow
Quando si utilizzano i metodi Qtà Massima e Qtà Riordino Fissa, il sistema di pianificazione si concentra solo sulle giacenze previste nell'intervallo di tempo specificato. Ciò significa che il sistema di pianificazione può suggerire un approvvigionamento superfluo quando si verificano dei cambiamenti nella domanda negativa o nell'approvvigionamento positivo al di fuori dell'intervallo di tempo specificato. Se, per questo motivo, viene suggerito un approvvigionamento inutile, il sistema di pianificazione calcola la quantità alla quale l'approvvigionamento dovrebbe essere ridotto (o eliminato) per evitare l'approvvigionamento superfluo. Questa quantità è denominata “livello di overflow”. L'overflow viene comunicato come una riga di pianificazione con un'azione **Cambia Qtà (riduzione)** o **Annulla** e il seguente messaggio di avviso:  

*Attenzione: La giacenza disponibile [xx] è superiore al livello di overflow [xx] alla data di scadenza [xx].*  

![Livello di overflow del magazzino](media/supplyplanning_2_overflow1_new.png "Livello di overflow del magazzino")  

###  <a name="calculating-the-overflow-level"></a>Calcolo del livello di overflow  
Il livello di overflow viene calcolato in modi diversi a seconda dell'impostazione della pianificazione.  

#### <a name="maximum-qty-reordering-policy"></a>Metodo di riordino di Qtà Massima  
Livello di overflow = giacenza massima  

> [!NOTE]  
>  Se è presente una quantità ordine minima, verrà aggiunta come segue: Livello di overflow = giacenza massima + quantità ordine minima.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Metodo di riordino Qtà Riordino Fissa  
Livello di overflow = quantità di riordino + punto di riordino  

> [!NOTE]  
>  Se la quantità di ordine minima è superiore al punto di riordino, sarà sostituita come segue: Livello di overflow = quantità di riordino + quantità ordine minima  

#### <a name="order-multiple"></a>Molteplicità ordine  
In presenza di una molteplicità di ordini, verrà rettificato il livello di overflow per i metodi di riordino sia Quantità massima che Quantità riordino fissa.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Creazione della riga di pianificazione con avviso di overflow  
Quando un approvvigionamento esistente determina un aumento della giacenza disponibile oltre il livello di overflow alla fine di un intervallo di tempo, viene creata una riga di pianificazione. Per avvisare del potenziale approvvigionamento superfluo, la riga di pianificazione contiene un messaggio di avviso, il campo **Accetta messaggio azione** non è selezionato e il messaggio di azione è Annulla o Cambia Qtà.  

#### <a name="calculating-the-planning-line-quantity"></a>Calcolo della quantità della riga di pianificazione  
Quantità della riga di pianificazione = quantità dell'approvvigionamento corrente - (scorte previste - livello di overflow)  

> [!NOTE]  
>  Analogamente a tutte le righe di avviso, tutte le quantità ordine minime e massime o di ordine multiplo verranno ignorate.  

#### <a name="defining-the-action-message-type"></a>Definizione del tipo di messaggio di azione  

-   Se la quantità della riga di pianificazione è uguale o superiore a 0, il messaggio di azione sarà Cambia qtà.  
-   Se la quantità della riga di pianificazione è uguale o inferiore a 0, il messaggio di azione sarà pari ad Annulla  

#### <a name="composing-the-warning-message"></a>Composizione del messaggio di avviso  
In caso di overflow, nella pagina **Elementi di pianificazione non tracciati** viene visualizzato un messaggio di avviso con le informazioni seguenti:  

-   Livello di giacenza disponibile che ha attivato l'avviso  
-   Livello di overflow calcolato  
-   Data di scadenza dell'evento di approvvigionamento.  

Esempio: "La giacenza disponibile 120 è superiore al livello di overflow 60 in 28-01-11”  

### <a name="scenario"></a>Scenario  
In questo scenario, un cliente modifica un ordine di vendita da 70 a 40 pezzi tra due esecuzioni di pianificazione. La funzionalità di overflow consente di ridurre l'acquisto che è stato suggerito per la quantità di vendita iniziale.  

#### <a name="item-setup"></a>Setup articolo  

|Metodo di riordino|Qtà Massima|  
|-----------------------|------------------|  
|Quantità massima ordine|100|  
|Punto riordino|50|  
|Magazzino|80|  

#### <a name="situation-before-sales-decrease"></a>Situazione prima della riduzione della vendita  

|Evento|Cambia Qtà|Quantità scorte previste|  
|-----------|-----------------|-------------------------|  
|Giorno uno|Nessuno|80|  
|Vendite|-70|10|  
|Fine dell'intervallo di tempo|Nessuno|10|  
|Suggerire nuovo ordine di acquisto|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Situazione dopo la riduzione della vendita  

|Cambia|Cambia Qtà|Quantità scorte previste|  
|------------|-----------------|-------------------------|  
|Giorno uno|Nessuno|80|  
|Vendite|-40|40|  
|Acquisti|+90|130|  
|Fine dell'intervallo di tempo|Nessuno|130|  
|Suggerire di ridurre l'acquisto<br /><br /> ordine di acquisto da 90 a 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Righe pianificazione risultanti  
 Una riga di pianificazione (avviso) viene creata per ridurre l'acquisto di 30 da 90 a 60 per mantenere la giacenza disponibile su 100 in base al livello di overflow.  

![Pianificazione in base al livello di overflow](media/nav_app_supply_planning_2_overflow2.png "Pianificazione in base al livello di overflow")  

> [!NOTE]  
>  Senza la funzionalità di overflow, nessun avviso viene creato se il livello di giacenza disponibile è superiore alla giacenza massima. Potrebbe verificarsi un approvvigionamento superfluo di 30.

## <a name="handling-projected-negative-inventory"></a>Gestione giacenze negative previste
Il punto di riordino esprime la domanda prevista durante il lead time dell'articolo. Quando il punto di riordino viene superato, è tempo di ordinare quantità maggiori. Ma le scorte previste devono essere abbastanza grandi da coprire la domanda fino a che non viene ricevuto il nuovo ordine. Nel frattempo, la scorta di sicurezza deve coprire le fluttuazioni della domanda fino a un livello di servizio di destinazione.  

 Di conseguenza, se una domanda futura non può essere servita dalle scorte previste, oppure espressa in un altro modo, il sistema di pianificazione considera un'emergenza se la giacenza disponibile diventa negativa. Il sistema tratta questo tipo di eccezione suggerendo un nuovo ordine di approvvigionamento in modo da soddisfare la parte della domanda che non può essere soddisfatta dal magazzino o da un altro approvvigionamento. Le dimensioni dell'ordine del nuovo ordine di approvvigionamento non prenderanno in considerazione la giacenza massima o la quantità di riordino, né prenderanno in considerazione i modificatori di ordine Quantità massima ordine, Quantità minima ordine e Molteplicità ordine. In alternativa, rifletterà la carenza esatta.  

 Nella riga di pianificazione per questo tipo ordine di approvvigionamento verrà visualizzata un'icona di avviso di emergenza. Verranno inoltre fornite informazioni aggiuntive su ricerca per informare l'utente della situazione.  

 Nella seguente illustrazione l'approvvigionamento D rappresenta un ordine di emergenza per la rettifica della giacenza negativa.  

 ![Suggerimenti di pianificazione di emergenza per evitare giacenze negative](media/nav_app_supply_planning_2_negative_inventory.png "Suggerimenti di pianificazione di emergenza per evitare giacenze negative")  

1.  L'approvvigionamento **A**, la giacenza disponibile iniziale, è inferiore al punto di riordino.  
2.  Viene creato un nuovo approvvigionamento programmato in avanti (**C**).  

     (Quantità = Giacenza massima – Livello giacenza disponibile)  
3.  L'approvvigionamento **A** viene chiuso dalla domanda **B**, che non viene coperta completamente.  

     La domanda **B** potrebbe provare a pianificare l'Approvvigionamento C ma ciò non accade in base al concetto dell'intervallo di tempo.  
4.  Un nuovo approvvigionamento (**D**) viene creato per coprire la quantità residua sulla domanda **B**.  
5.  La domanda **B** viene chiusa creando un sollecito alle scorte previste.  
6.  Il nuovo approvvigionamento **D** viene chiuso.  
7.  La giacenza disponibile è controllata; il punto di riordino non è stato superato.  
8.  L'approvvigionamento **C** viene chiuso (non esiste più la domanda).  
9. Controllo finale: non esistono solleciti di livello di magazzino in sospeso.  

> [!NOTE]  
>  Il passaggio 4 indica in che modo il sistema opera nelle versioni precedenti a Microsoft Dynamics NAV 2009 SP1.  

Ciò conclude la descrizione dei principi centrali relativi alla pianificazione del magazzino basata sui metodi di riordino. Nella seguente sezione vengono illustrate le caratteristiche dei quattro metodi di riordino supportati.

## <a name="reordering-policies"></a>Metodi di riordino
I metodi di riordino consentono di definire la quantità da ordinare quando l'articolo deve essere rifornito. Esistono quattro metodi diversi di riordine.  

### <a name="fixed-reorder-qty"></a>Qtà Riordino Fissa
Il criterio Qtà Riordino Fissa è correlato alla pianificazione di magazzino dei tipici articoli C (costo di magazzino basso, basso rischio di obsolescenza e/o molti articoli). Questo metodo viene in genere utilizzato in connessione con un punto di riordino che riflette la domanda anticipata durante il lead time dell'articolo.  

#### <a name="calculated-per-time-bucket"></a>Calcolato per intervallo di tempo  
Se il sistema di pianificazione rileva che il punto di riordino è stato raggiunto o superato in un intervallo di tempo specificato (ciclo di riordino) - sopra o in corrispondenza del punto di riordino all'inizio del periodo e sotto o in corrispondenza del punto di riordino alla fine del periodo - verrà suggerito di creare un nuovo ordine di approvvigionamento della quantità di riordino specificata e di programmarlo dalla prima data successiva alla fine dell'intervallo di tempo.  

Il concetto di punto di riordino programmato riduce il numero di suggerimenti di approvvigionamento. Ciò riflette un processo manuale di entrare nella warehouse spesso per controllare i contenuti effettivi nelle varie collocazioni.  

#### <a name="creates-only-necessary-supply"></a>Crea solo l'approvvigionamento necessario  
Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione controlla se l'approvvigionamento è già stato ordinato per essere ricevuto entro il lead time di un articolo. Se un ordine di approvvigionamento esistente risolverà il problema portando la giacenza disponibile al punto di riordino o oltre nel lead time, il sistema non suggerirà un nuovo ordine di approvvigionamento.  

Gli ordini di approvvigionamento che vengono creati specificamente per soddisfare un punto di riordino sono esclusi dal bilanciamento dell'approvvigionamento ordinario e non verranno in alcun modo modificati in seguito. Di conseguenza, se un articolo che utilizza il punto di riordino deve essere eliminato (non compilato), è consigliabile verificare gli ordini di approvvigionamento inevasi manualmente o modificare il metodo di riordino lotto-per-Lotto con cui il sistema ridurrà o annullerà l'approvvigionamento superfluo.  

#### <a name="combines-with-order-modifiers"></a>Combina con i modificatori di ordine  
I modificatori di ordini, Quantità minima ordine, Quantità massima ordine e Molteplicità ordine, non devono svolgere un grande ruolo quando vengono utilizzati i criteri di quantità riordino fissa. Tuttavia, il sistema di pianificazione prende ancora in considerazione questi modificatori e diminuirà la quantità alle quantità di ordine massime specificate (e creerà due o più approvvigionamenti per raggiungere la quantità di ordine totale), aumenterà la quantità di ordine minima o arrotonderà la quantità di ordine fino a soddisfare la molteplicità ordine specificata.  

#### <a name="combines-with-calendars"></a>Associazioni con i calendari  
Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione verifica che l'ordine sia programmato per un giorno non lavorativo, in base ai calendari definiti nel campo **Codice calendario base** delle pagine **Informazioni società** e **Scheda Ubicazione**.  

Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. In questo modo, potrebbe verificarsi che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.  

#### <a name="should-not-be-used-with-forecast"></a>Non deve essere utilizzato con la previsione  
Poiché la domanda prevista è già espressa nel livello del punto di riordino non è necessario includere una previsione nella pianificazione di un articolo utilizzando un punto di riordino. Se è necessario basare il piano su una previsione, utilizzare il metodo lotto per lotto.  

#### <a name="must-not-be-used-with-reservations"></a>Non deve essere utilizzato con gli impegni  
Se l'utente ha impegnato una quantità, ad esempio una quantità in magazzino, per una domanda remota, la struttura della pianificazione rimarrà alterata. Anche se il livello della quantità scorte previste è ammesso relativamente al punto di riordino, le quantità potrebbero non essere disponibili. Il sistema può provare a compensare creando ordini di eccezione; tuttavia, è consigliabile che il campo Impegno sia impostato su Mai negli articoli che sono pianificati utilizzando un punto di riordino.

### <a name="maximum-qty"></a>Qtà Massima
Il criterio Quantità massima è un modo per mantenere il magazzino utilizzando un punto di riordino.  

Tutto ciò che riguarda il metodo Qtà Riordino Fissa si applica anche a questi criteri. L'unica differenza è la quantità dell'approvvigionamento suggerito. Se si utilizza il metodo della quantità massima, la quantità di riordino verrà definita in modo dinamico in base al livello delle giacenze disponibili e quindi in genere differirà da ordine a ordine.  

#### <a name="calculated-per-time-bucket"></a>Calcolato per intervallo di tempo  
La quantità di riordino viene determinata in un punto del tempo (alla fine di un intervallo di tempo) quando il sistema di pianificazione rileva che il punto di riordino è stato superato. A questo punto, il sistema misura l'interruzione dal livello di magazzino previsto corrente fino al magazzino massimo specificato. Ciò costituisce la quantità che deve essere riordinata. Il sistema controlla quindi se l'approvvigionamento è già stato ordinato altrove in modo che possa essere caricato entro il lead time e, in caso affermativo, riduce la quantità del nuovo ordine di approvvigionamento della quantità già ordinata.  

Il sistema assicurerà che la giacenza disponibile raggiunga almeno il livello del punto di riordino, nel caso l'utente abbia dimenticato di specificare una quantità di magazzino massima.  

#### <a name="combines-with-order-modifiers"></a>Combina con i modificatori di ordine  
In base all'impostazione, è consigliabile combinare i criteri Quantità massima con i modificatori di ordini per garantire una quantità minima dell'ordine o per arrotondarla a un numero intero di unità di misura di acquisto, o suddividerla in più lotti come definito dalla quantità massima ordine.  

### <a name="combines-with-calendars"></a>Associazioni con i calendari  
Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione verifica che l'ordine sia programmato per un giorno non lavorativo, in base ai calendari definiti nel campo **Codice calendario base** delle pagine **Informazioni società** e **Scheda Ubicazione**.  

Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. In questo modo, potrebbe verificarsi che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.

### <a name="order"></a>Ordinamento
In un ambiente di produzione su ordine, un articolo viene acquistato o prodotto esclusivamente per coprire una domanda specifica. In genere si riferisce ad articoli A e le motivazioni per scegliere il metodo di riordino Ordine può essere quello di una domanda poco frequente, un lead time insignificante o la variazione degli attributi necessari.  

Il programma crea un collegamento ordine su ordine, che funge da connessione preliminare tra l'approvvigionamento, un ordine di approvvigionamento o il magazzino e la domanda che deve soddisfare.  

Oltre all'utilizzo del metodo Ordine, il collegamento ordine-a-ordine può essere applicato durante la pianificazione nei seguenti modi:  

* Se si utilizza la politica di produzione Produzione su ordine per creare ordini di produzione di tipo progetto o multilivello (producendo i componenti necessari nello stesso ordine di produzione).  
* Se si utilizza la funzionalità Pianifica ordine vendita per creare un ordine di produzione da un ordine di vendita.  

Anche se un'azienda manifatturiera si considera come ambiente di produzione su ordine, potrebbe essere meglio utilizzare un metodo di riordino lotto-per-lotto se gli articoli sono standard puro senza variazione negli attributi. Di conseguenza, verrà utilizzato il magazzino non pianificato e si accumuleranno solo ordini di vendita con la stessa data di spedizione o all'interno di un intervallo di tempo definito.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Collegamenti ordine su ordine e date di scadenza arretrate  
A differenza della maggior parte dei set di approvvigionamento-domanda, gli ordini collegati con date di scadenza precedenti alla data di inizio della pianificazione sono completamente pianificati dal sistema. Il motivo economico di questa eccezione è che la domanda e l'approvvigionamento specifici devono essere sincronizzati attraverso l'esecuzione. Per ulteriori informazioni sulla zona bloccata che si applica alla maggior parte dei tipi di domanda-approvvigionamento, vedere [Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione](design-details-dealing-with-orders-before-the-planning-starting-date.md).

### <a name="lot-for-lot"></a>Lotto-per-Lotto
I criteri lotto per lotto sono i più flessibili perché il sistema reagisce solo alla domanda effettiva, agiscono inoltre sulla domanda prevista dalla previsione e dagli ordini programmati e stabiliscono la quantità dell'ordine in base alla domanda. I criteri lotto per lotto sono destinati agli elementi A e B dove il magazzino può essere accettato ma dovrebbe essere evitato.  

Per certi aspetti, il metodo lotto per lotto è simile al metodo Ordine, ma presenta un approccio generico agli articoli; può accettare quantità in magazzino e aggrega la domanda e il corrispondente approvvigionamento in intervalli di tempo definiti dall'utente.  

L'intervallo di tempo è definito nel campo **Intervallo di tempo**. Il sistema utilizza l'intervallo di tempo minimo pari a un giorno, che è l'unità di misura più piccola per gli eventi di domanda e approvvigionamento offerta dal sistema (sebbene, nella pratica, gli ordini di produzione e le richieste di componenti possano essere misurate in secondi).  

L'intervallo di tempo fissa anche dei limiti sui tempi di riprogrammazione di un ordine di approvvigionamento esistente per soddisfare una domanda specificata. Se l'approvvigionamento rientra nell'intervallo di tempo, viene riprogrammato all'interno o all'esterno in modo da soddisfare la domanda. In caso contrario, se risiede in un periodo precedente, causerà un accumulo di magazzino inutile e dovrà essere annullato. Se risiede dopo, verrà invece creato un nuovo ordine di approvvigionamento.  

Con questo metodo, è possibile definire una scorta di sicurezza per compensare possibili fluttuazioni nell'approvvigionamento o per soddisfare una domanda improvvisa.  

Poiché la quantità dell'ordine di approvvigionamento è basato sulla domanda effettiva e può essere sensato utilizzare i modificatori di ordini: arrotondare la quantità di ordine fino a soddisfare un multiplo dell'ordine specificato (o unità di misura dell'acquisto), aumentare l'ordine a una quantità ordine minima specificata oppure diminuire la quantità alla quantità massima specificata (e creare quindi due o più approvvigionamenti per raggiungere la quantità necessaria totale).

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
