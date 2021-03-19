---
title: 'Dettagli di progettazione: Bilanciamento domanda e approvvigionamento | Documenti Microsoft'
description: Per comprendere il funzionamento del sistema di pianificazione, è necessario comprendere gli obiettivi classificati in ordine di priorità del sistema di pianificazione, i più importanti dei quali servono a garantire che qualsiasi domanda sarà soddisfatta da un approvvigionamento sufficiente e ogni domanda avrà uno scopo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f8f09c843397c7b3fa0a24bc90f5799a157fa883
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388726"
---
# <a name="design-details-balancing-demand-and-supply"></a>Dettagli di progettazione: Bilanciamento domanda e approvvigionamento
Per comprendere il funzionamento del sistema di pianificazione, è necessario comprendere gli obiettivi classificati in ordine di priorità del sistema di pianificazione, i più importanti dei quali servono a garantire quanto segue:  

- Qualsiasi domanda verrà soddisfatta da approvvigionamento sufficiente.  
- Qualsiasi approvvigionamento serve a uno scopo.  

 In genere, questi obiettivi vengono raggiunti equilibrando l'approvvigionamento con la domanda.  

## <a name="demand-and-supply"></a>Domanda e approvvigionamento
 La domanda è il termine comune utilizzato per tutti i tipi di domanda lorda, ad esempio un ordine di vendita e un componente necessario da un ordine di produzione. Inoltre, l'applicazione consente i tipi di domanda più tecnici, ad esempio resi di acquisto e delle giacenze negative.  

  Approvvigionamento è il termine comune utilizzato per indicare qualsiasi genere di quantità in entrata o positiva, quale il magazzino, gli acquisti, l'assemblaggio, la produzione o i trasferimenti in entrata. Inoltre, anche un reso di vendita può rappresentare un approvvigionamento.  

  Per ordinare le numerose origini di approvvigionamento e di domanda, il sistema di pianificazione le organizza su due righe chiamate profili di magazzino. Un profilo conserva gli eventi di domanda e l'altro conserva i corrispondenti eventi di approvvigionamento. Ogni evento rappresenta un'entità di rete di ordini, ad esempio una riga ordine di vendita, un movimento contabile di magazzino o una riga di ordine di produzione.  

  Quando vengono caricati i profili di magazzino, i differenti set di domanda-approvvigionamento vengono bilanciati in modo da fornire un piano di approvvigionamento che soddisfi gli obiettivi elencati.  

  I parametri di pianificazione e i livelli di magazzino sono altri tipi rispettivamente di domanda e di approvvigionamento, che subiscono la contropartita integrata per rifornire gli articoli in stock. Per ulteriori informazioni, vedere [Dettagli di programmazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Il concetto di contropartita in breve
  La domanda è fornita dai clienti di una società. L'approvvigionamento è ciò che la società può creare e rimuovere per stabilire il saldo. Il sistema di pianificazione inizia con la domanda indipendente e successivamente risale a ritroso fino all'approvvigionamento.  

   I profili di magazzino vengono utilizzati per contenere le informazioni sulle domande, gli approvvigionamenti, le quantità e l'intervallo. I profili essenzialmente compongono i due lati della bilancia.  

   L'obiettivo del meccanismo di pianificazione consiste nel controbilanciare la domanda e l'approvvigionamento di un articolo per garantire che l'approvvigionamento corrisponda alla domanda in modo fattibile così come definito dalle regole e dai parametri di pianificazione.  

   ![Panoramica sull'equilibrio di approvvigionamento e domanda](media/nav_app_supply_planning_2_balancing.png "Panoramica sull'equilibrio di approvvigionamento e domanda")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Gestione ordini prima della data di inizio pianificazione
Per evitare che un piano di approvvigionamento mostri suggerimenti impossibili e pertanto inutili, il sistema di pianificazione considera il periodo fino alla data di inizio pianificazione come una zona bloccata nella quale nulla viene pianificato. La seguente regola si applica alla zona bloccata:  

Tutta le domande e l'approvvigionamento prima della data di inizio del periodo di pianificazione verranno considerati come parte del magazzino o saranno spediti.  

Di conseguenza, il sistema di pianificazione non suggerisce, con poche eccezioni, modifiche agli ordini di approvvigionamento nella zona bloccata e nessun collegamento di tracciabilità viene creato o gestito per quel periodo.  

Le eccezioni a questa regola sono:  

   * Se le scorte disponibili previste, inclusa la somma di domanda e approvvigionamento nella zona bloccata, è inferiore a zero.  
   * Se i numeri seriali o di lotto sono obbligatori negli ordini retrodatati.  
   * Se il set di approvvigionamento-domanda è collegato da un metodo ordine su ordine.  

Se la giacenza disponibile iniziale è minore di zero, il sistema di pianificazione suggerisce un ordine di approvvigionamento di emergenza datato il giorno precedente al periodo di pianificazione per coprire la quantità mancante. Di conseguenza, il magazzino previsto e disponibile sarà sempre almeno uguale a zero quando inizia la pianificazione per il periodo futuro. Nella riga di pianificazione per questo ordine di approvvigionamento verrà visualizzata un'icona di avviso di emergenza. Verranno inoltre fornite informazioni aggiuntive su ricerca.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>I numeri seriali o di lotto e i collegamenti ordine su ordine sono esenti dalla zona bloccata  
   Se i numeri seriali o di lotto sono obbligatori o è presente un collegamento ordine su ordine, il sistema di pianificazione ignorerà la zona bloccata e includerà tali quantità che sono retrodatate dalla data iniziale e potenzialmente suggerirà delle azioni correttive se la domanda e l'approvvigionamento non sono sincronizzati. Il motivo economico di questo principio è che questo specifico set di domanda e approvvigionamento deve corrispondere per garantire che la domanda specifica sia soddisfatta completamente.

## <a name="loading-the-inventory-profiles"></a>Carico dei profili di magazzino
Per ordinare le numerose origini di approvvigionamento e di domanda, il sistema di pianificazione le organizza su due sequenze temporali chiamate profili di magazzino.  

I normali tipi di domanda e approvvigionamento con date di scadenza corrispondenti o successive alla data iniziale di pianificazione vengono caricati in ciascun profilo di magazzino. Una volta caricati, i diversi tipi di domanda e approvvigionamento vengono ordinati in base alle priorità globali, ad esempio la data di scadenza, i codici di ultimo livello, l'ubicazione e la variante. Inoltre, vengono applicate delle priorità di ordine a diversi tipi per garantire che la domanda più importante sia completata per prima. Per ulteriori informazioni, vedere [Assegnazione priorità ordini](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Come precedentemente citato, la domanda potrebbe essere anche negativa. Ciò significa che deve essere considerata come approvvigionamento; tuttavia, a differenza dei tipi normali di approvvigionamento, la domanda negativa viene considerata un approvvigionamento fisso. Il sistema di pianificazione può prenderlo in considerazione, ma non suggerirà modifiche.  

In genere, il sistema di pianificazione considera tutti gli ordini di approvvigionamento dopo la data di inizio della pianificazione come oggetti da modificare per soddisfare la domanda. Tuttavia, non appena una quantità viene registrata da un ordine di approvvigionamento, non può più essere modificata dal sistema di pianificazione. Di conseguenza, i seguenti ordini diversi non possono essere ripianificati:  

- Ordini di produzione rilasciati in cui è stato registrato il consumo o l'output.  
- Ordini di assemblaggio in cui è stato registrato il consumo o l'output.  
- Ordini di trasferimento in cui è stata registrata la spedizione.  
- Ordini di acquisto in cui il carico è stato registrato.  

Oltre a caricare i tipi di approvvigionamento e di domanda, alcuni tipi vengono caricati con attenzione alle regole speciali e alle dipendenze descritte di seguito.  

### <a name="item-dimensions-are-separated"></a>Le dimensioni articolo sono separate  
Il piano di approvvigionamento deve essere calcolato in base alla combinazione delle dimensioni dell'articolo, ad esempio la variante e l'ubicazione. Tuttavia, non esiste motivo per calcolare una combinazione teorica. Solo le combinazioni che includono la necessità di approvvigionamento e/o di domanda devono essere calcolate.  

Ciò è controllato dal sistema di pianificazione attraverso l'esecuzione del profilo di magazzino. Quando viene trovata una nuova combinazione, viene creato un record di controllo interno che contiene le informazioni effettive sulla combinazione. L'applicazione inserisce la USK come record di controllo o ciclo esterno. Di conseguenza, vengono impostati i parametri di pianificazione appropriati in base a una combinazione di variante e ubicazione e l'applicazione può procedere al ciclo interno.  

> [!NOTE]  
>  L'applicazione non richiede all'utente di immettere un record di USK durante l'immissione della domanda e/o dell'approvvigionamento per una particolare combinazione di variante e ubicazione. Di conseguenza, se un USK non esiste per una combinazione specifica, l'applicazione crea un record USK temporaneo in base ai dati della scheda articolo. Se il campo Ubicazione obbligatoria è impostato su Sì nella pagina Setup magazzino, è necessario creare una USK oppure impostare Componenti nell'ubicazione su Sì. Per ulteriori informazioni, vedere [Dettagli di progettazione: Domanda nell'ubicazione vuota](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>I numeri seriali o di lotto vengono caricati dal livello di specifica  
Gli attributi in forma di numeri di serie o di lotto vengono caricati nei profili del magazzino insieme alla domanda e all'approvvigionamento a cui sono assegnati.  

Gli attributi di domanda e approvvigionamento sono ordinati per priorità ordini nonché per livello di specifica. Poiché le corrispondenze del numero seriale o di lotto riflettono il livello di specifica, la domanda più specifica, ad esempio un numero di lotti selezionato in modo specifico per una riga di vendita, cercherà una corrispondenza prima della domanda meno specifica, ad esempio una vendita da un numero qualsiasi di lotto selezionato.  

> [!NOTE]  
>  Non vi sono regole di priorità dedicate per l'approvvigionamento e la domanda dotati di numeri seriali o di lotto, eccetto il livello di specifica definito dalle relative combinazioni di numeri seriali e di lotto e l'impostazione di tracciabilità articolo degli articoli interessati.  

Durante la contropartita, il sistema di pianificazione considera l'approvvigionamento che offre i numeri di serie o di lotto come inflessibili e non prova ad aumentare o ripianificare tali ordini di approvvigionamento (a meno che non siano utilizzati in una relazione ordine-a-ordine). Vedere I collegamenti da ordine a ordine non sono mai interrotti). Ciò protegge l'approvvigionamento dal ricevere vari messaggi di azione potenzialmente in conflitto quando un approvvigionamento contiene attributi che variano, ad esempio una raccolta di numeri seriali differenti.  

Un altro motivo per cui l'approvvigionamento con numero seriale o di lotto non è flessibile è che ai numeri seriali o di lotto in genere vengono assegnati in ritardo nel processo potrebbe confondere se vengono suggerite le modifiche.  

Il saldo dei numeri seriali o di lotto non rispetta la *Zona bloccata*. Se la domanda e l'approvvigionamento non sono sincronizzati, il sistema di pianificazione suggerirà delle modifiche o dei nuovi ordini, indipendentemente dalla data di inizio della pianificazione.  

### <a name="order-to-order-links-are-never-broken"></a>I collegamenti ordine su ordine non sono mai interrotti  
Nella pianificazione di un articolo ordine su ordine, l'approvvigionamento collegato non deve essere utilizzato per domande diverse da quella originariamente di destinazione. La domanda collegata non dovrebbe essere coperta da un altro approvvigionamento casuale, anche se, in questa situazione, è disponibile per tempo e quantità. Ad esempio, un ordine di assemblaggio collegato a un ordine di vendita in uno scenario di assemblaggio su ordine non può essere utilizzato per coprire un'altra domanda.  

La domanda e l'approvvigionamento ordine su ordine devono essere in totale pareggio. Il sistema di pianificazione assicurerà l'approvvigionamento in tutte le condizioni senza considerare i parametri di dimensioni ordine, i modificatori e le quantità di magazzino (diverse dalle quantità correlate agli ordini collegati). Per lo stesso motivo, il sistema suggerirà approvvigionamenti eccedente in calo se la domanda collegata viene diminuita.  

Questo bilanciamento influisce anche sui tempi. L'orizzonte limitato che viene fornito dall'intervallo di tempo non viene considerato; l'approvvigionamento verrà riprogrammato se i tempi della domanda sono cambiati. Tuttavia, il tempo di smorzamento sarà rispettato e impedirà la riprogrammazione all'esterno degli approvvigionamenti ordine su ordine, ad eccezione degli approvvigionamenti interni di un ordine di produzione a più livelli (ordine di progetto).  

> [!NOTE]  
>  I numeri seriali e di lotto possono inoltre essere specificati nella domanda ordine su ordine. In questo caso, l'approvvigionamento non viene considerato inflessibile per impostazione predefinita, come nel caso dei numeri seriali o di lotto. In questo caso, il sistema aumenterà o diminuirà a seconda dei cambiamenti nella domanda. Inoltre, se una domanda contiene più numeri seriali o di lotto diversi, ad esempio più di un numero di lotto, un ordine di approvvigionamento verrà suggerito per lotto.  

> [!NOTE]  
>  Le previsioni non devono condurre alla creazione degli ordini di approvvigionamento associati a un collegamento ordine-a-ordine. Se viene utilizzata la previsione, deve essere utilizzata solo come generatore della domanda dipendente in un ambiente di produzione.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Il componente richiesto viene caricato in base alle modifiche dell'ordine di produzione  
Nella gestione degli ordini di produzione, il sistema di pianificazione deve monitorare i componenti necessari prima di caricarli nel profilo della domanda. Le righe componenti derivanti da un ordine di produzione corretto sostituiranno quelle dell'ordine originale. In questo modo il sistema di pianificazione stabilisce sicuramente che le righe di pianificazione per componenti necessari non vengano mai duplicate.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> La scorta di sicurezza può essere consumata  
La scorta di sicurezza è principalmente un tipo di domanda e pertanto viene caricata nel profilo di magazzino alla data di inizio della pianificazione.  

La scorta di sicurezza è una quantità di magazzino accantonata per compensare le incertezze della domanda durante il lead time di rifornimento. Tuttavia, può essere consumato se è necessario attingere per soddisfare una domanda. In tal caso, il sistema assicura che la scorta di sicurezza sia rapidamente reintegrata suggerendo un ordine di approvvigionamento per rifornire la quantità di scorta di sicurezza alla data in cui è stata consumata. La riga di pianificazione relativa a tale ordine conterrà un'icona di avviso di eccezione indicante che la scorta di sicurezza è stata parzialmente o completamente consumata per mezzo di un ordine di eccezione per la quantità mancante.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>La domanda di previsione viene ridotta dagli ordini di vendita  
La previsione della domanda esprime la domanda futuro prevista. Mentre la domanda effettiva viene immessa, in genere come ordini vendita per articoli prodotti, viene utilizzata la previsione.  

La previsione stessa non viene effettivamente ridotta dagli ordini di vendita; rimane la stessa. Tuttavia, le quantità previste utilizzate nel calcolo della pianificazione vengono ridotte (delle quantità dell'ordine di vendita) prima che l'eventuale quantità residua sia immessa nel profilo di magazzino della domanda. Quando il sistema di pianificazione esamina le vendite effettive del periodo, sono inclusi sia gli ordini di vendita aperti che i movimenti contabili articoli di vendita, a meno che non siano derivati da un ordine programmato.  

È richiesto un utente per definire un periodo di previsione valido. La data della quantità prevista definisce l'inizio del periodo e la data della previsione successiva definisce la fine del periodo.  

La previsione per periodi precedenti al periodo di pianificazione non viene utilizzata, indipendentemente dal fatto che sia stata consumata o meno. La prima cifra di previsione interessante è la data di inizio o la data più vicina precedente alla data di inizio pianificazione.  

La previsione può riguardare una domanda indipendente, ad esempio ordini di vendita, o una domanda dipendente, come i componenti dell'ordine di produzione (modulo-previsione). Un articolo può avere entrambi i tipi di previsione. Durante la pianificazione, il consumo avviene separatamente, prima per domanda indipendente quindi per la domanda dipendente.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>La domanda dell'ordine programmato viene ridotta dagli ordini di vendita  
Le previsioni vengono completate dall'ordine di vendita programmato al fine di specificare la domanda futura da un cliente specifico. Analogamente alle previsioni (non specificato), le vendite effettive dovrebbero consumare la domanda prevista e la quantità residua dovrebbe immettere il profilo di magazzino della domanda. Di nuovo, il consumo non riduce effettivamente l'ordine programmato.  

Il calcolo della pianificazione considera gli ordini vendita aperti collegati alla riga ordine di copertura specifica, ma non considera alcun periodo di tempo valido. Non vengono considerati neppure gli ordini registrati, poiché la procedura di registrazione ha già ridotto la quantità inevasa dell'ordine programmato.

## <a name="prioritizing-orders"></a>Assegnazione priorità ordini
All'interno di una determinata USK, la data richiesta o disponibile rappresenta la priorità più alta; la domanda della data corrente deve essere gestita prima della domanda della settimana successiva. Ma oltre a questa priorità globale, il sistema di pianificazione suggerirà inoltre il tipo di domanda da soddisfare prima di soddisfarne un'altra. Analogamente, verrà suggerito quale origine di approvvigionamento deve essere collegata prima di collegare altre origini di approvvigionamento. Questa operazione viene eseguita in base alle priorità degli ordini.  

La domanda e l'approvvigionamento caricati contribuiscono a un profilo per la giacenza disponibile in base alle seguenti priorità:  

### <a name="priorities-on-the-demand-side"></a>Priorità sul lato della domanda  
1. Già spediti: Mov. contabili articolo  
2. Ordine di reso acquisto  
3. Ordini Vendita  
4. Ordine Assistenza  
5. Necessità componente di produzione  
6. Riga ordine di assemblaggio  
7. Ordine di trasferimento in uscita  
8. L'ordine programmato (non ancora utilizzato dagli ordini di vendita correlati)  
9. Previsione (non ancora utilizzata da altri ordini di vendita)  

> [!NOTE]  
>  I resi di acquisto non vengono in genere inclusi nella pianificazione dell'approvvigionamento; devono essere sempre impegnati dal lotto che sta per essere reso. Se non impegnati, i resi di acquisto svolgono un ruolo nella disponibilità e hanno un'elevata priorità per evitare che il sistema suggerisca un ordine di approvvigionamento solo per un ordine di reso.  

### <a name="priorities-on-the-supply-side"></a>Priorità sul lato dell'approvvigionamento  
1. Già in magazzino: Mov. contabili articoli (Flessibilità pianificazione = Nessuna)  
2. Ordine di reso vendita (flessibilità pianificazione = nessuna)  
3. Ordine di trasferimento in ingresso  
4. Ordine di produzione  
5. Ordine di assemblaggio  
6. Ordine acquisto  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Priorità correlata allo stato di domanda e approvvigionamento  
Oltre alle priorità specificate dal tipo di domanda e approvvigionamento, lo stato attuale degli ordini nel processo di esecuzione definisce anche una priorità. Ad esempio, le attività di magazzino hanno un l'impatto e lo stato degli ordini di vendita, di acquisto, di trasferimento, di assemblaggio e di produzione vengono presi in considerazione:  

1. Gestito parzialmente (flessibilità pianificazione = nessuna)  
2. Già nel processo nel warehouse (flessibilità pianificazione = Nessuna)  
3. Rilasciato - tutti i tipi di ordine (flessibilità pianificazione = illimitata)  
4. Ordine di produzione confermato (flessibilità pianificazione = illimitata)  
5. Pianificato/Aperto - tutti i tipi di ordine (flessibilità pianificazione = illimitata)

## <a name="balancing-supply-with-demand"></a>Bilanciamento approvvigionamento con domanda
Il cuore del sistema di pianificazione implica il bilanciamento tra domanda e approvvigionamento per mezzo di azioni suggerite all'utente per riesaminare gli ordini di approvvigionamento nel caso di sbilanciamento. Questa operazione viene eseguita per combinazione di variante e ubicazione.  

Si immagini che ogni profilo di magazzino contenga una serie di eventi di domanda (ordinati per data e per priorità) e un numero corrispondente di eventi di approvvigionamento. Ogni evento si riferisce al suo tipo e identificativo di origine. Le regole per controbilanciare l'articolo sono chiare. Quattro istanze di domanda corrispondente e di approvvigionamento possono verificarsi in qualsiasi momento nel processo:  

1. Non esiste alcuna domanda o approvvigionamento per l'articolo => la pianificazione è terminata (o non deve iniziare).  
2. La domanda esiste ma non esiste un approvvigionamento => suggerire approvvigionamento.  
3. L'approvvigionamento esiste ma non esiste una domanda => approvvigionamento da annullare.  
4. Esistono sia la domanda che l'approvvigionamento => è necessario fare domande e fornire risposte affinché il sistema possa garantire che tale domanda venga soddisfatta e l'approvvigionamento sia sufficiente.  

    Se l'intervallo di approvvigionamento non è appropriato, è possibile riprogrammare l'approvvigionamento come segue:  

    1.  Se l'approvvigionamento viene inserito prima della domanda, è possibile riprogrammarlo in modo che il magazzino sia più basso possibile.  
    2.  Se l'approvvigionamento viene inserito successivamente alla domanda, è possibile riprogrammarlo. Altrimenti, il sistema suggerirà un nuovo approvvigionamento.  
    3.  Se l'approvvigionamento soddisfa la domanda alla data, il sistema di pianificazione può procedere a verificare se la quantità di approvvigionamento può coprire la domanda.  

    Una volta impostati i tempi, la quantità appropriata da fornire può essere calcolata come segue:  

    1.  Se la quantità di approvvigionamento è minore della domanda, è possibile che la quantità di approvvigionamento possa essere aumentata (o non aumentata se limitata da un metodo di quantità massima).  
    2.  Se la quantità di approvvigionamento è maggiore della domanda, è possibile che la quantità di approvvigionamento possa essere diminuita (o non diminuita se limitata da un metodo di quantità minima).  

    A questo punto, esiste una di queste due situazioni:  

    1.  La domanda corrente può essere coperta, nel qual caso può essere chiusa e si può procedere con la pianificazione della domanda successiva.  
    2.  L'approvvigionamento ha raggiunto il massimo, lasciando una certa quantità di domanda scoperta. In questo caso, il sistema di pianificazione può chiudere l'approvvigionamento corrente e procedere a quello successivo.  

 La procedura inizia dappertutto con la domanda successiva e l'approvvigionamento corrente o viceversa. L'approvvigionamento corrente potrebbe essere in grado di soddisfare anche la domanda successiva o la domanda corrente se non è stata ancora interamente coperta.  

### <a name="rules-concerning-actions-for-supply-events"></a>Regole concernenti azioni per gli eventi di approvvigionamento  
Quando il sistema di pianificazione esegue un calcolo dall'alto verso il basso in cui l'approvvigionamento deve soddisfare la domanda, la domanda viene considerata come un dato di fatto, vale a dire che rimane fuori dal controllo del sistema di pianificazione. Tuttavia, il lato dell'approvvigionamento può essere gestito. Di conseguenza, il sistema di pianificazione suggerirà la creazione di nuovi ordini di approvvigionamento, la ripianificazione di quelli esistenti e/o la modifica della quantità dell'ordine. Se un ordine di approvvigionamento esistente diventa superfluo, il sistema di pianificazione ne suggerirà l'annullamento all'utente.  

Se l'utente desidera escludere un ordine di approvvigionamento esistente dai suggerimenti di pianificazione, può dichiarare di non disporre di flessibilità di pianificazione (flessibilità pianificazione = nessuna). Quindi, l'approvvigionamento in eccesso da tale ordine verrà utilizzato per soddisfare la domanda, ma non verrà suggerita alcuna azione.  

In genere, tutti gli approvvigionamenti hanno una flessibilità di pianificazione che è limitata dalle condizioni di ciascuna delle azioni suggerite.  

-   **Riprogramma all'esterno**: la data di un ordine di approvvigionamento esistente può essere programmata per soddisfare la data di scadenza della domanda a meno che:  

    -   Rappresenta il magazzino (sempre nel giorno zero).  
    -   Contiene un metodo da ordine a ordine collegato a un'altra domanda.  
    -   Risiede al di fuori della pagina di ripianificazione definita dall'intervallo di tempo.  
    -   Esiste un approvvigionamento più recente che potrebbe essere utilizzato.  
    -   D'altro canto, l'utente potrebbe scegliere di non ripianificare per i seguenti motivi:  
    -   L'ordine di approvvigionamento è già stato associato a un'altra domanda in una data precedente.  
    -   La riprogrammazione necessaria è talmente minima che l'utente la trova trascurabile.  

-   **Riprogramma all'interno**: la data di un ordine di approvvigionamento esistente può essere programmata nel periodo, ad eccezione delle seguenti condizioni:  

    -   È collegata direttamente a un'altra domanda.  
    -   Risiede al di fuori della pagina di ripianificazione definita dall'intervallo di tempo.  

> [!NOTE]  
>  Nella pianificazione di un articolo tramite un punto di riordino, l'ordine di approvvigionamento può sempre essere riprogrammato all'interno, se necessario. Ciò è comune negli ordini di approvvigionamento programmati in avanti attivati da un punto di riordino.  

-   **Aumentare la quantità**: la quantità di un ordine di approvvigionamento esistente può essere aumentata per soddisfare la domanda a meno che l'ordine di approvvigionamento sia collegato direttamente a una domanda da un collegamento ordine a ordine.  

> [!NOTE]  
>  Anche se è possibile aumentare l'ordine di approvvigionamento, potrebbe essere limitato a causa di quantità massima ordine definita.  

-   **Riduci quantità**: un ordine di approvvigionamento esistente con un surplus rispetto a una domanda esistente può essere ridotto per soddisfare la domanda.  

> [!NOTE]  
>  Anche se la quantità può essere diminuita, può ancora esservi un certo surplus rispetto alla domanda a causa di una quantità minima di ordine definita o molteplicità ordine.  

-   **Annulla**: come incidente speciale dell'azione di riduzione quantità, l'ordine di approvvigionamento potrebbe essere annullato se è stato diminuito a zero.  
-   **Nuovo**: se non è presente alcun ordine di approvvigionamento già esistente o un ordine esistente non può essere modificato per soddisfare la quantità necessaria alla data di scadenza richiesta, verrà proposto un nuovo ordine di approvvigionamento.  

### <a name="determining-the-supply-quantity"></a>Determinazione della quantità di approvvigionamento  
I parametri di pianificazione definiti dall'utente controllano la quantità suggerita di ogni ordine di approvvigionamento.  

Quando il sistema di pianificazione calcola la quantità di nuovo ordine di approvvigionamento o la modifica della quantità in un ordine esistente, la quantità suggerita può essere diversa dalla quantità effettivamente richiesta.  

Se è selezionata una quantità massima di magazzino o una quantità di ordine fissa, la quantità suggerita può essere aumentata per soddisfare la quantità fissa o la giacenza massima. Se un metodo di riordino utilizza un punto di riordino, la quantità può essere aumentata almeno per soddisfare il punto di riordino.  

 La quantità suggerita può essere modificata nella sequenza:  

1. Eseguire il drill-down alla quantità di ordine massima (se esistente).  
2. Fino alla quantità minima ordine.  
3. Fino a soddisfare la molteplicità di ordini più vicina. (Nel caso di impostazioni errate, questo potrebbe violare le quantità di ordine massima).  

### <a name="order-tracking-links-during-planning"></a>Collegamenti della tracciabilità ordini durante la pianificazione  
Nel caso di tracciabilità dell'ordine durante la pianificazione, è importante ricordare che il sistema di pianificazione ridispone i collegamenti di tracciabilità ordine creati in modo dinamico per le combinazioni articolo/variante/ubicazione.  

Questo avviene per due motivi:  

-   Il sistema di pianificazione deve essere in grado di giustificare i suggerimenti che fornisce; che tutta la domanda sia stata coperta e che non esistano ordini di approvvigionamento superflui.  
-   I collegamenti di tracciabilità ordine creati in modo dinamico devono essere ribilanciati regolarmente.  

Nel tempo, i collegamenti di tracciabilità ordini dinamici finiscono per non quadrare poiché l'intera rete di tracciabilità ordini non viene ridisposta fino a quando un evento di approvvigionamento o di domanda non viene effettivamente chiuso.  

Prima di bilanciare l'approvvigionamento con la domanda, l'applicazione elimina tutti i collegamenti di tracciabilità ordine esistenti. Quindi durante la procedura di bilanciamento, quando viene chiuso un evento di approvvigionamento o di domanda, il programma stabilisce nuovi collegamenti di tracciabilità ordine tra la domanda e l'approvvigionamento.  

> [!NOTE]  
>  Anche se l'articolo non è impostato per la tracciabilità dinamica dell'ordine, il sistema pianificato creerà collegamenti di tracciabilità ordine come di seguito illustrato.
## <a name="closing-demand-and-supply"></a>Chiusura domanda e approvvigionamento
Una volta che sono state eseguite le procedure di contropartita di approvvigionamento, sono disponibili tre casi finali possibili:  

* La quantità e la data necessarie degli eventi di domanda sono state soddisfatte e la relativa pianificazione può essere chiusa. L'evento di approvvigionamento è ancora aperto e può essere in grado di soddisfare la domanda successiva, pertanto la procedura di contropartita può rincominciare con l'evento di approvvigionamento corrente e la domanda successiva.  
* L'ordine di approvvigionamento non può essere modificato per soddisfare tutta la domanda. Un evento di domanda è ancora aperto, con una quantità scoperta che può essere coperta dal successivo evento di approvvigionamento. L'evento di approvvigionamento corrente viene quindi chiuso, in modo che l'azione di bilanciamento posso riprendere dall'inizio con gli eventi domanda corrente e approvvigionamento successivo.  
* Tutta la domanda è stata coperta; non esiste alcuna domanda successiva (o non c'è stata alcuna domanda). Se esiste un surplus di approvvigionamento, può essere ridotto (o annullato) e quindi chiuso. È possibile che degli eventi di approvvigionamento aggiuntivi persistano nella catena, nel qual caso anch'essi devono essere annullati.  

Infine, il sistema di pianificazione creerà un collegamento di tracciabilità ordine tra approvvigionamento e domanda.  

### <a name="creating-the-planning-line-suggested-action"></a>Creazione della riga di pianificazione (azione suggerita)  
Se viene suggerita una qualsiasi azione, ad esempio nuovo, modifica della quantità, riprogrammazione e modifica della quantità o annullamento, per esaminare l'ordine di approvvigionamento, tramite il sistema di pianificazione viene creata una riga di pianificazione nel prospetto di pianificazione. A causa della tracciabilità dell'ordine, la riga di pianificazione viene creata non solo al momento della chiusura dell'evento di approvvigionamento, ma anche se l'evento della domanda è chiuso, anche se l'evento di approvvigionamento è ancora aperto e potrebbe essere soggetto a ulteriori modifiche quando viene elaborata la domanda successiva. Ciò significa che, una volta creata, la riga di pianificazione può essere modificata nuovamente.  

Per ridurre al minimo l'accesso al database durante la gestione degli ordini di produzione, la riga di pianificazione può essere gestita a tre livelli, mirando al contempo a eseguire il livello di manutenzione meno impegnativo:  

* Creare solo la riga di pianificazione con la data di scadenza e la quantità corrente ma senza il ciclo e i componenti.  
* Includere il ciclo: il ciclo di produzione pianificato viene steso includendo il calcolo delle date di inizio e di fine e dei periodi. Ciò risulta molto impegnativo in termini di accessi al database. Per determinare le date di scadenza e di fine, può essere necessario calcolare anche se l'evento di approvvigionamento non è stato chiuso (nel caso di programmazione in avanti).  
* Includere l'esplosione della distinta base: questa operazione può attendere fino a poco prima della chiusura dell'evento approvvigionamento.  

Ciò conclude le descrizioni delle modalità di caricamento, di assegnazione di priorità e di bilanciamento di domanda e approvvigionamento nel sistema di pianificazione. A integrazione di questa attività di pianificazione dell'approvvigionamento, il sistema deve garantire che il livello di magazzino richiesto di ciascun articolo pianificato sia mantenuto in base al relativo metodo di riordino.

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
 [Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]