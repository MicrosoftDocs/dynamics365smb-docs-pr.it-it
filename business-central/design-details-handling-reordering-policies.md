---
title: Dettagli di progettazione - Gestione dei metodi di riordino
description: Questo articolo fornisce una panoramica dei criteri di riordino che è possibile utilizzare nella pianificazione dell'approvvigionamento.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# Dettagli di progettazione: Gestione dei metodi di riordino

Per includere un articolo nella pianificazione dell'approvvigionamento, è necessario specificare un criterio di riordino nella pagina **Scheda articolo** . Sono disponibili i seguenti criteri di riordino:  

* Qtà Riordino Fissa  
* Qtà Massima  
* Ordinamento  
* Lotto-per-Lotto  

I criteri **Qtà riordino fissa** e **Qtà massima** sono relativi alla pianificazione del magazzino. Questi criteri coesistono con il bilanciamento graduale dell'approvvigionamento e la tracciabilità degli ordini.  

## Il ruolo del punto di riordino

Un punto di riordino rappresenta la domanda durante il lead time. Quando la giacenza disponibile scende sotto il livello di magazzino definito dal punto di riordino, è tempo di ordinare altra quantità. Il magazzino diminuisce gradualmente fino all'arrivo dell'approvvigionamento. Può raggiungere lo zero o il livello delle scorte di sicurezza. Il sistema di pianificazione suggerisce un ordine di approvvigionamento programmato in avanti alla fase in cui la giacenza prevista passa al di sotto del punto di riordino.  

I livelli di magazzino possono variare in modo significativo durante l'intervallo di tempo. Pertanto, il sistema di pianificazione monitora costantemente le scorte disponibili.

## Monitoraggio del livello di giacenza disponibile e del punto di riordino

Il magazzino è un tipo di approvvigionamento, ma per la pianificazione del magazzino, il sistema di pianificazione distingue tra due livelli di magazzino:  

* Quantità scorte previste  
* Scorte disponibili previste  

### Quantità scorte previste  

All'inizio del processo di pianificazione, le scorte previste sono la quantità lorda del magazzino. La quantità lorda include la domanda e l'offerta registrate e non registrate in passato. Questa quantità diventa un livello di magazzino previsto mantenuto dalle quantità lorde derivanti dalla domanda e dall'offerta future. La domanda e l'offerta future vengono introdotte nella linea del tempo, riservate o assegnate in altri modi.  

La giacenza disponibile viene utilizzata dal sistema di pianificazione per monitorare il punto di riordino e per determinare la quantità di riordino quando viene utilizzato il metodo di riordino **Qtà massima**.  

### Scorte disponibili previste  

Le scorte disponibili previste sono la parte della giacenza disponibile che in un dato momento è disponibile per soddisfare la domanda. Le scorte disponibili previste vengono utilizzate dal sistema di pianificazione durante il monitoraggio del livello della scorta di sicurezza. Le scorte di sicurezza devono essere sempre disponibili per una domanda imprevista.  

### Intervalli di tempo  

È importante disporre di un controllo delle scorte previste per rilevare quando viene raggiunto il punto di riordino e per calcolare le giuste quantità dell'ordine quando si utilizza il metodo di riordino **Qtà massima**.  

Il livello di magazzino previsto viene calcolato all'inizio del periodo di pianificazione. È un livello lordo che non considera gli impegni e altre allocazioni. Per monitorare il livello di magazzino durante la sequenza di pianificazione, le modifiche aggregate vengono monitorate dal sistema si pianificazione nell'arco di un periodo di tempo. Questo periodo è chiamato *intervallo di tempo*. Per saperne di più sugli intervalli di tempo, vai a [Il ruolo dell'intervallo di tempo](#the-role-of-the-time-bucket). Il sistema di pianificazione garantisce che l'intervallo di tempo sia di almeno un giorno. Un giorno è l'unità di tempo minima per gli eventi di domanda od offerta.  

### Determinazione del livello di magazzino previsto  

Nella seguente sequenza viene descritto in che modo il sistema di pianificazione determina il livello di giacenza disponibile:  

* Quando un evento di approvvigionamento, ad esempio un ordine di acquisto, è stato completamente pianificato, aumenta la giacenza disponibile alla data di scadenza dell'evento.  
* Quando un evento di domanda è completamente soddisfatto, la giacenza disponibile non diminuisce immediatamente. In alternativa, registra un sollecito di diminuzione, ovvero un record interno che contiene la data e la quantità dell'aggiunta alla giacenza disponibile.  
* Quando un successivo evento di approvvigionamento viene pianificato e aggiunto alla sequenza temporale, il sistema esamina i solleciti di diminuzione registrati uno per uno alla data pianificata dell'approvvigionamento. Durante il processo, può essere raggiunto o superato il livello del punto di riordino del sollecito di incremento interno.  
* Se viene immesso un nuovo ordine di approvvigionamento, viene controllato se l'ordine viene immesso prima dell'approvvigionamento corrente. In questo caso, il nuovo approvvigionamento diventa l'approvvigionamento corrente e la procedura di bilanciamento rincomincia.  

L'immagine seguente illustra questo principio.  

![Determinazione del livello di magazzino previsto.](media/nav_app_supply_planning_2_projected_inventory.png "Determinazione del livello di magazzino previsto")  

1. L'approvvigionamento **Sa** di 4 (fisso) chiude la domanda **Da** di -3.  
2. CloseDemand: Creare un sollecito di riduzione di -3 (non visualizzato).  
3. L'approvvigionamento **Sa** viene chiuso con un surplus di 1 (non esiste più domanda).  

     Il livello di scorte previste viene aumentato a +4, mentre la giacenza **disponibile** diventa -1.  

4. Il successivo approvvigionamento **Sb** di 2 (un altro ordine) è già stato immesso nella sequenza temporale.  
5. Il sistema di pianificazione controlla se esiste un sollecito di riduzione precedente a **Sb** (in questo esempio non c'è e non viene intrapresa alcuna azione).  
6. Il sistema di pianificazione chiude l'approvvigionamento **Sb** (non esiste più domanda) riducendolo a 0 (annullamento) o lasciandolo invariato.  

     Il livello del magazzino previsto viene aumentato (A: +0 => +4 o B: +2 = +6).  

7. Il sistema di pianificazione effettua un controllo finale. C'è qualche sollecito di riduzione? Sì, ne esiste uno alla data di **Da**.  
8. Il sistema di pianificazione aggiunge un sollecito di diminuzione di -3 al livello di giacenza disponibile, A: +4 -3 = 1 o B: +6 -3 = +3.  
9. Per A, il sistema di pianificazione crea un ordine programmato in avanti che inizia alla data indicata di **Da**. Per B, viene raggiunto il punto di riordino e viene creato un nuovo ordine.

## Il ruolo dell'intervallo di tempo

Lo scopo dell'intervallo di tempo è di raccogliere gli eventi di domanda nell'intervallo di tempo in modo da creare un ordine di approvvigionamento congiunto.  

Per i metodi di riordino che utilizzano un punto di riordino, è possibile definire un intervallo di tempo. Gli intervalli di tempo aiutano a garantire che le richieste all'interno dello stesso periodo di tempo vengano accumulate. Il sistema controlla quindi l'effetto sul magazzino previsto e se il punto di riordino è stato superato.

Se il punto di riordino è passato, il sistema programma in avanti un nuovo ordine di approvvigionamento dalla fine dell'intervallo di tempo. Gli intervalli di tempo iniziano con la data di inizio pianificazione.  

Il concetto di intervallo di tempo riflette il processo manuale di controllo del livello di magazzino su base frequente anziché ad ogni transazione. Devi definire la frequenza (intervallo di tempo). Ad esempio, puoi raccogliere tutte le esigenze dell'articolo da un fornitore per inserire un ordine settimanale.  

![Esempio di pianificazione basata su intervallo di tempo.](media/nav_app_supply_planning_2_reorder_cycle.png "Esempio di pianificazione basata su intervallo di tempo")  

L'intervallo di tempo viene spesso utilizzato per evitare un effetto di sovrapposizione. Ad esempio, una riga equilibrata di approvvigionamento e domanda dove una domanda iniziale viene annullata o ne viene creata una nuova. Il risultato sarebbe che ogni ordine di approvvigionamento (eccetto l'ultimo) viene riprogrammato.

## Restare al di sotto del livello di overflow

Quando si utilizzano i criteri di riordino **Qtà massima** e **Qtà riordino fissa**, il sistema di pianificazione si concentra solo sulle giacenze previste nell'intervallo di tempo specificato. Potrebbe suggerire un'offerta extra quando la domanda negativa o le modifiche positive dell'offerta si verificano al di fuori dell'intervallo di tempo. Per l'approvvigionamento extra, il sistema di pianificazione calcola la quantità di cui ridurre l'approvvigionamento. Questa quantità è denominata “livello di overflow”. L'overflow è disponibile come riga di pianificazione con un'azione **Cambia Qtà (riduzione)** o **Annulla** e il seguente messaggio di avviso:  

* Attenzione: La giacenza disponibile [xx] è superiore al livello di overflow [xx] alla data di scadenza [xx].*  

![Livello di overflow del magazzino.](media/supplyplanning_2_overflow1_new.png "Livello di overflow del magazzino")  

### Calcolo del livello di overflow  

Il livello di overflow viene calcolato in modi diversi a seconda del criterio di riordino.  

#### Qtà Massima

Livello di overflow = giacenza massima  

> [!NOTE]  
> Se utilizzi una quantità minima dell'ordine, viene aggiunta come segue:
>
> Livello di overflow = giacenza massima + quantità minima dell'ordine.  

#### Qtà Riordino Fissa  

Livello di overflow = quantità di riordino + punto di riordino  

> [!NOTE]  
> Se la quantità minima dell'ordine è superiore al punto di riordino, viene sostituita come segue:
>
> Livello di overflow = quantità di riordino + quantità minima dell'ordine  

#### Molteplicità dell'ordine  

In presenza di una molteplicità di ordini, viene rettificato il livello di overflow per i metodi di riordino sia Quantità massima che Quantità riordino fissa.  

### Creazione della riga di pianificazione con avviso di overflow  

Una riga di pianificazione viene creata quando un approvvigionamento esistente determina un aumento della giacenza disponibile oltre il livello di overflow alla fine di un intervallo di tempo. Per avvisare dell'approvvigionamento extra, la riga di pianificazione contiene un messaggio di avviso, il campo **Accetta messaggio azione** non è selezionato e il messaggio di azione è **Annulla** o **Cambia qtà**.  

#### Calcolo della quantità della riga di pianificazione  

La quantità in una riga di pianificazione viene calcolata come segue:

quantità della riga di pianificazione = quantità dell'approvvigionamento corrente - (scorte previste - livello di overflow)  

> [!NOTE]  
> Analogamente a tutte le righe di avviso, le quantità ordine minime e massime e di ordine multiplo vengono ignorate.  

#### Definizione del tipo di messaggio di azione  

* Se la quantità della riga di pianificazione è uguale o superiore a 0, il messaggio di azione sarà **Cambia qtà**.  
* Se la quantità della riga di pianificazione è uguale o inferiore a 0, il messaggio di azione sarà **Annulla**  

#### Composizione del messaggio di avviso  

In caso di overflow, nella pagina **Elementi di pianificazione non tracciati** viene visualizzato un messaggio di avviso con le informazioni seguenti:  

* Livello di giacenza disponibile che ha attivato l'avviso  
* Livello di overflow calcolato  
* Data di scadenza dell'evento di approvvigionamento  

Esempio: "La giacenza disponibile 120 è superiore al livello di overflow 60 in 01-28-23”  

### Scenario di esempio  

In questo scenario, un cliente modifica un ordine di vendita da 70 a 40 pezzi tra due esecuzioni di pianificazione. La funzionalità di overflow riduce l'acquisto che è stato suggerito per la quantità di vendita iniziale.  

#### Impostazione articolo  

|Metodo di riordino|Qtà Massima|  
|-----------------------|------------------|  
|Quantità massima ordine|100|  
|Punto riordino|50|  
|Magazzino|80|  

#### Situazione prima della riduzione della vendita  

|Evento|Cambia Qtà|Quantità scorte previste|  
|-----------|-----------------|-------------------------|  
|Giorno uno|Nessuno|80|  
|Vendite|-70|10|  
|Fine dell'intervallo di tempo|Nessuno|10|  
|Suggerire nuovo ordine di acquisto|+90|100|  

#### Situazione dopo la riduzione della vendita  

|Cambia|Cambia Qtà|Quantità scorte previste|  
|------------|-----------------|-------------------------|  
|Giorno uno|Nessuno|80|  
|Vendite|-40|40|  
|Acquisti|+90|130|  
|Fine dell'intervallo di tempo|Nessuno|130|  
|Suggerire di ridurre l'acquisto<br><br> ordine di acquisto da 90 a 60|-30|100|  

#### Righe pianificazione risultanti  

Il sistema crea una riga di pianificazione avviso per ridurre l'acquisto di 30 da 90 a 60 per mantenere la giacenza disponibile su 100 in base al livello di overflow.  

![Pianificazione in base al livello di overflow.](media/nav_app_supply_planning_2_overflow2.png "Pianificazione in base al livello di overflow")  

> [!NOTE]  
> Senza la funzionalità di overflow, nessun avviso viene creato se il livello di giacenza disponibile è superiore alla giacenza massima, che può causare un approvvigionamento extra di 30.

## Gestione delle giacenze negative previste

Il punto di riordino esprime la domanda prevista durante il lead time dell'articolo. Le scorte previste devono essere abbastanza grandi da coprire la domanda fino a che non viene ricevuto il nuovo ordine. Nel frattempo, la scorta di sicurezza deve coprire le fluttuazioni della domanda fino a un livello di servizio di destinazione.  

Il sistema di pianificazione considera un'emergenza se una domanda futura non può essere soddisfatta dal magazzino previsto. O, espresso in altro modo, che il magazzino previsto diventa negativo. Il sistema suggerisce di creare un nuovo ordine di approvvigionamento per coprire la parte non soddisfatta della domanda. La dimensione del nuovo ordine di approvvigionamento non terrà conto della giacenza massima o della quantità di riordino né dei seguenti modificatori dell'ordine:

* Quantità massima dell'ordine
* Quantità minima dell'ordine
* Molteplicità dell'ordine 

In alternativa, riflette la carenza esatta.  

Nella riga di pianificazione per questo tipo di ordine di approvvigionamento verrà visualizzata un'icona di avviso di **emergenza** con informazioni aggiuntive sulla situazione.  

Nella seguente immagine l'approvvigionamento D rappresenta un ordine di emergenza per la rettifica della giacenza negativa.  

![Suggerimenti di pianificazione di emergenza per evitare giacenze negative.](media/nav_app_supply_planning_2_negative_inventory.png "Suggerimenti di pianificazione di emergenza per evitare giacenze negative")  

1. L'approvvigionamento **A**, la giacenza disponibile iniziale, è inferiore al punto di riordino.  
2. Viene creato un nuovo approvvigionamento programmato in avanti (**C**).  

     (quantità = giacenza massima – livello giacenza disponibile)  
3. L'approvvigionamento **A** viene chiuso dalla domanda **B**, che non viene coperta completamente.  

     La domanda **B** potrebbe provare a pianificare l'Approvvigionamento C ma l'intervallo di tempo lo impedisce.  
4. Un nuovo approvvigionamento (**D**) viene creato per coprire la quantità residua sulla domanda **B**.  
5. La domanda **B** viene chiusa creando un sollecito alle scorte previste.  
6. Il nuovo approvvigionamento **D** viene chiuso.  
7. Le scorte previste sono controllate. Il punto di riordino non è stato superato.  
8. L'approvvigionamento **C** viene chiuso (non c'è più la domanda).  
9. Controllo finale. Non esistono solleciti a livello di magazzino in sospeso.  

Nella seguente sezione vengono illustrate le caratteristiche dei quattro metodi di riordino supportati.

## Criteri di riordino

I metodi di riordino consentono di definire la quantità da ordinare quando l'articolo deve essere rifornito. Esistono quattro metodi diversi di riordine.  

### Quantità di riordino fissa

Il criterio quantità di riordino fissa viene in genere utilizzato per la pianificazione del magazzino per gli articoli con le seguenti caratteristiche:

* Costo di magazzino basso
* Basso rischio di obsolescenza
* Basso numero di articoli

Di norma, usa questo criterio in connessione con un punto di riordino che riflette la domanda anticipata durante il lead time dell'articolo.  

#### Calcolato per intervallo di tempo  

Se raggiungi o superi il punto di riordino in un intervallo di tempo (ciclo di riordino), il sistema suggerisce due azioni:

* Creare un nuovo ordine di approvvigionamento per la quantità di riordino
* Pianificare in avanti l'ordine dalla prima data dopo la fine dell'intervallo di tempo  

Il punto di riordino programmato riduce il numero di suggerimenti di approvvigionamento. Riflette un processo di controllo manuale del contenuto effettivo delle collocazioni nella tua warehouse.  

#### Crea solo l'approvvigionamento necessario  

Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione controlla il seguente approvvigionamento:

* Se l'approvvigionamento è già ordinato
* Se prevedi di ricevere l'approvvigionamento entro il lead time dell'articolo

Il sistema non suggerirà un nuovo ordine di approvvigionamento se un approvvigionamento porterà il magazzino previsto al punto di riordino entro il lead time.  

Gli ordini di approvvigionamento che vengono creati specificamente per soddisfare un punto di riordino sono esclusi dal bilanciamento dell'approvvigionamento ordinario e non verranno modificati. Se desideri eliminare gradualmente un articolo che ha un punto di riordino, controlla manualmente i tuoi ordini di approvvigionamento in sospeso o modifica il criterio di riordino in **Lotto per lotto**. Il sistema ridurrà o annullerà l'approvvigionamento extra.  

#### Combina con i modificatori di ordine  

I modificatori di ordini, Quantità minima ordine, Quantità massima ordine e Molteplicità ordine non devono svolgere un ruolo significativo quando vengono utilizzati i criteri di quantità riordino fissa. Tuttavia, il sistema di pianificazione ne tiene conto:

* Diminuisci la quantità fino alla quantità massima dell'ordine specificata (e crea due o più approvvigionamenti per raggiungere la quantità totale dell'ordine)
* Aumenta l'ordine fino alla quantità minima specificata
* Arrotonda la quantità dell'ordine per soddisfare un multiplo dell'ordine specificato  

#### Combina con i calendari  

Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione controlla se l'ordine è programmato per un giorno non lavorativo. Utilizza i calendari specificati nel campo **Codice calendario di base** nelle pagine **Informazioni sulla società** e **Scheda ubicazione**.  

Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. Lo spostamento di data potrebbe causare che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.  

#### Non deve essere utilizzato con le previsioni  

Poiché la domanda prevista è già espressa nel livello del punto di riordino non è necessario includere una previsione nella pianificazione. Se è necessario basare il piano su una previsione, utilizza il criterio **lotto per lotto**.  

#### Non deve essere utilizzato con le prenotazioni  

Se hai prenotato una quantità, ad esempio una quantità in magazzino, per una domanda remota, potresti alterare la struttura della pianificazione. Anche se il livello della quantità scorte previste è ammesso relativamente al punto di riordino, le quantità potrebbero non essere disponibili. Il sistema potrebbe tentare di compensare creando ordini di eccezione. Tuttavia, ti consigliamo di impostare il campo **Prenota** su **Mai** per gli articoli pianificati utilizzando un punto di riordino.

### Quantità massima

Il criterio Quantità massima è un modo per mantenere il magazzino utilizzando un punto di riordino.  

Tutto ciò che riguarda il metodo Qtà Riordino Fissa si applica anche a questi criteri. L'unica differenza è la quantità dell'approvvigionamento suggerito. Se si utilizza il metodo della quantità massima, la quantità di riordino verrà definita in modo dinamico in base al livello delle giacenze disponibili. Pertanto, di solito differisce da ordine a ordine.  

#### Calcolare per intervallo di tempo

Quando raggiungi o superi il punto di riordino, il sistema determina la quantità di riordino alla fine di un intervallo di tempo. Misura la differenza tra il livello di magazzino previsto corrente e il magazzino massimo specificato per determinare la quantità da ordinare. Il sistema controlla quindi:

* Se l'approvvigionamento è già ordinato
* Se prevedi di ricevere l'approvvigionamento entro il lead time dell'articolo

In tal caso, il sistema riduce la quantità del nuovo ordine di approvvigionamento delle quantità già ordinate.  

Se non specifichi una quantità massima di scorte, il sistema di pianificazione assicura che le scorte previste raggiungano la quantità di riordino.

#### Combinare con i modificatori di ordine

A seconda della configurazione, potrebbe essere meglio combinare il criterio Quantità massima con i modificatori d'ordine: 

* Per assicurare una quantità minima dell'ordine
* Arrotonda la quantità a un numero intero di unità di misura di acquisto
* Dividi la quantità in lotti come definito dalla quantità massima dell'ordine  

### Combinare con i calendari

Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione controlla se l'ordine è programmato per un giorno non lavorativo. Utilizza i calendari specificati nel campo **Codice calendario di base** nelle pagine **Informazioni sulla società** e **Scheda ubicazione**.  

Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. Lo spostamento di data potrebbe causare che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.

### Ordinamento

In un ambiente di produzione su ordine, un articolo viene acquistato o prodotto per coprire una domanda specifica. In genere, il criterio di riordino degli ordini viene utilizzato per gli articoli con le seguenti caratteristiche

* La domanda è poco frequente
* Il lead time è insignificante
* Gli attributi richiesti variano  

[!INCLUDE [prod_short](includes/prod_short.md)] crea un collegamento ordine su ordine, che funge da connessione preliminare tra l'approvvigionamento, un ordine di approvvigionamento o il magazzino e la domanda. È possibile applicare il collegamento ordine su ordine durante la pianificazione nei seguenti modi:  

* Se usi il criterio Produzione su ordine per creare ordini di produzione di tipo progetto o multilivello (producendo i componenti necessari nello stesso ordine di produzione)  
* Se usi la funzionalità Pianifica ordine vendita per creare un ordine di produzione da un ordine di vendita  

> [!TIP]
> Se gli attributi dell'articolo non variano, potrebbe essere meglio utilizzare un criterio di riordino lotto per lotto. Di conseguenza, viene utilizzato il magazzino non pianificato e si accumuleranno solo ordini di vendita con la stessa data di spedizione o all'interno di un intervallo di tempo definito.  

#### Collegamenti ordine su ordine e date di scadenza passate

A differenza della maggior parte dei set di approvvigionamento-domanda, gli ordini collegati con date di scadenza precedenti alla data di inizio della pianificazione sono completamente pianificati dal sistema. Il motivo di questa eccezione è che la domanda e l'approvvigionamento specifici devono essere sincronizzati. Per ulteriori informazioni sulla zona bloccata che si applica alla maggior parte dei tipi di domanda-approvvigionamento, vedi [Elaborare gli ordini prima della data di inizio pianificazione](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### Lotto-per-Lotto

Il criterio lotto per lotto è il più flessibile perché il sistema reagisce solo alla domanda effettiva. Agisce sulla domanda anticipata dagli ordini previsti e programmati e quindi regola la quantità dell'ordine in base alla domanda. I criteri sono destinati agli articoli dove il magazzino può essere accettato ma dovrebbe essere evitato.  

In un certo senso, il criterio lotto per lotto è simile al criterio dell'ordine. Può accettare quantità in magazzino e raggruppa la domanda e l'offerta negli intervalli di tempo definiti.

Puoi specificare l'intervallo di tempo nel campo **Intervallo di tempo** della pagina **Scheda articolo**. La dimensione minima dell'intervallo di tempo è un giorno, perché è l'unità di misura temporale più piccola per gli eventi di domanda e offerta in [!INCLUDE [prod_short](includes/prod_short.md)].  

L'intervallo di tempo fissa anche dei limiti sui tempi di riprogrammazione di un ordine di approvvigionamento per soddisfare una domanda specificata. L'approvvigionamento nell'intervallo di tempo viene riprogrammato all'interno o all'esterno in modo da soddisfare la domanda. L'approvvigionamento anticipato causerà un magazzino extra e dovresti annullarla. Per l'approvvigionamento successivo, crea un nuovo ordine di approvvigionamento.  

Con questo criterio puoi specificare una scorta di sicurezza per compensare i cambiamenti nell'offerta o per soddisfare una domanda improvvisa. Il criterio lotto per lotto può includere anche un periodo di stabilizzazione e una quantità di stabilizzazione per ridurre la programmazione degli ordini.  

Insieme al campo **Periodo di riprogrammazione** contribuisce a definire il ciclo di riordino insieme al campo **Periodo di accumulo lotti**. A partire dalla data della prima domanda, tutte le domande sono accumulate nel successivo periodo di accumulo lotto in un ordine di approvvigionamento nella data della prima domanda. Le domanda esterna al periodo di accumulo lotto non è coperta dall'ordine di approvvigionamento.

Poiché la quantità dell'ordine di approvvigionamento si basa sulla domanda effettiva, può avere senso utilizzare i modificatori dell'ordine:

* Arrotonda la quantità dell'ordine per soddisfare un ordine multiplo (o unità di misura di acquisto)
* Aumenta l'ordine fino a una quantità minima specificata
* Diminuisci la quantità fino alla quantità massima specificata (e crea due o più approvvigionamenti per raggiungere la quantità totale necessaria)

## Vedere anche  

[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)  
[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md)  
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]