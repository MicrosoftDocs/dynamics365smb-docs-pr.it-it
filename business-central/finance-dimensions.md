---
title: Utilizzo delle Dimensioni per tenere traccia e analizzare i dati
description: 'Utilizza le dimensioni per classificare i movimenti, ad esempio, per reparto o progetto, in modo da tenere traccia e analizzare facilmente i dati per consentirti di prendere buone decisioni aziendali.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# <a name="work-with-dimensions" />Utilizzare le dimensioni

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio ordini vendita. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

Quindi, anziché impostare conti di contabilità generale distinti per ogni reparto e progetto, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare un piano dei conti complesso. Per ulteriori informazioni vedi [Business Intelligence](bi.md).

Un altro esempio consiste nell'impostare una dimensione denominata *Reparto* e nell'utilizzare tale dimensione al momento della registrazione dei documenti di vendita. In questo modo puoi utilizzare strumenti di business intelligence per vedere quale reparto ha venduto quali articoli. Più dimensioni si utilizzano, più dettagliati sono i report su cui è possibile basare le decisioni aziendali. Infatti, un singolo movimento di vendita può includere informazioni di più dimensioni, quali:  

* Il conto in cui è stata registrata la vendita dell'articolo.  
* Dove l'articolo è stato venduto.
* Chi lo ha venduto.
* Quale cliente l'ha acquistato.

## <a name="analyzing-by-dimensions" />Analisi per dimensioni

Dimensioni svolge un ruolo importante in business intelligence, ad esempio quando si definiscono le visualizzazioni analisi. Per ulteriori informazioni, vedi [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

> [!TIP]
> Un modo rapido di analizzare i dati transazionali in base alle dimensioni consiste nell'utilizzare l'azione **Imposta filtro dimensione** per filtrare i totali per dimensione nel piano dei conti e nelle pagine dei movimenti.

> [!NOTE]
> Le visualizzazioni analisi utilizzano spesso i dati delle dimensioni. Se scopri che è stata utilizzata una dimensione errata nei movimenti di contabilità generale (C/G) registrati, puoi correggere i valori delle dimensioni e aggiornare le visualizzazioni di analisi. Ciò contribuirà a mantenere accurati i rapporti e le analisi finanziarie. Per ulteriori informazioni, vedi [Risoluzione dei problemi e correzione delle dimensioni](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets" />Set di dimensioni

Un set di dimensioni è una combinazione univoca di valori dimensioni. Viene archiviato come movimenti set di dimensioni nel database. Ogni movimento set di dimensioni rappresenta un valore dimensioni singolo. Inoltre, ogni set di dimensioni e il movimento set di dimensioni al suo interno sono identificati da un ID set di dimensioni comune.  

Quando si crea una riga di registrazione, una testata del documento o una riga documento, è possibile specificare una combinazione di valori dimensioni. Anziché archiviare esplicitamente ogni valore dimensioni nel database, viene assegnato un ID set di dimensioni alla riga di registrazione, alla testata del documento o alla riga del documento per specificare il set di dimensioni.  

## <a name="setting-up-dimensions" />Impostazione delle dimensioni

È possibile definire le dimensioni e i valori dimensioni da utilizzare per classificare le registrazioni e i documenti, ad esempio ordini di vendita e di acquisto. Impostare le dimensioni nella pagina **Dimensioni** in cui si crea una riga per ogni dimensione, ad esempio *Progetto*, *Reparto*, *Area* e *Agente*.

Vengono inoltre impostati i valori delle dimensioni. Diciamo che i valori rappresentano i reparti della tua azienda. I valori delle dimensioni possono essere impostati in una struttura gerarchica simile al piano dei conti. Ciò significa che i dati possono essere suddivisi in vari livelli di granularità e possono essere sommati i sottoinsiemi dei valori dimensioni. In base alle necessità, è possibile impostare un numero illimitato di dimensioni e di valori dimensioni che possono essere utilizzati da tutti gli utenti nella società.

Quando si impostano dimensioni e valori, è possibile definire dimensioni globali e di scelta rapida nella pagina **Setup contabilità generale**. Queste dimensioni sono quindi sempre disponibili per essere selezionate come campi nelle righe del documento e del giornale di registrazione e nei movimenti contabili, senza aprire prima la pagina **Dimensioni**. Per ulteriori informazioni, vedi la sezione [Per impostare dimensioni globali e a collegamento rapido](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Dimensioni globali** utilizzate come filtro, ad esempio, per report, processi batch e report XML. È possibile utilizzare solo due dimensioni globali, scegliere pertanto le dimensioni che verranno utilizzate più spesso.
* Le **dimensioni a collegamento rapido** sono disponibili come campi nelle registrazioni, nelle righe dei documenti e nei movimenti contabili. È possibile creare fino a otto dimensioni.  

> [!NOTE]
> Dopo aver utilizzato una nuova dimensione in qualsiasi voce, ad esempio una riga o un nuovo record, non è possibile eliminare la dimensione, anche se non si registra la voce. Questo perché [!INCLUDE[prod_short](includes/prod_short.md)] crea immediatamente un set di dimensioni per la riga o il record. Ulteriori informazioni nella sezione [Set di dimensioni](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts" />Per impostare le dimensioni di default per clienti, fornitori e altri conti

È possibile assegnare una dimensione di default per un conto specifico. La dimensione viene copiata nelle registrazioni o nel documento quando si immette il numero di conto in una riga, ma è possibile eliminare o modificare il codice nella riga se il dato non è appropriato. Puoi anche richiedere una dimensione per la registrazione di un movimento in un tipo specifico di conto. > 

> [!NOTE]
> Le priorità delle dimensioni predefinite si aprono per scenari di vendite e acquisti a cui potresti voler prestare particolare attenzione. Quando si utilizzano le priorità delle dimensioni predefinite nei documenti di vendita e di acquisto, [!INCLUDE [prod_short](includes/prod_short.md)] considera sempre le dimensioni nell'intestazione come provenienti dal cliente o dal fornitore. Ciò vale per le dimensioni impostate manualmente o per impostazione predefinita ed è particolarmente rilevante quando si utilizzano dimensioni predefinite su ubicazioni e articoli ma non per clienti o fornitori.
>
> **Esempio**
>
> Hai uno scenario con le seguenti impostazioni di dimensione:
>
> * Un cliente senza dimensioni predefinite
> * Un articolo con ADM come valore di dimensione per la dimensione REPARTO
> * Un'ubicazione con PROD come valore di dimensione per la dimensione REPARTO
> * Le priorità delle dimensioni predefinite sono impostate come Cliente > Articolo > Ubicazione
>
> Quando crei un nuovo documento in questo scenario, le dimensioni vengono utilizzate come segue:
>
> * Se crei un nuovo documento e aggiungi un'ubicazione, il valore predefinito per le nuove righe sarà PROD. Quando aggiungi righe con articoli, [!INCLUDE [prod_short](includes/prod_short.md)] manterrà PROD perché proviene dall'intestazione del documento.
>
> * Se crei un nuovo documento e aggiungi articoli che hanno il valore della dimensione ADM e specifichi un'ubicazione nell'intestazione del documento, [!INCLUDE [prod_short](includes/prod_short.md)] ti chiederà se vuoi sovrascrivere le righe esistenti perché c'è un conflitto.
>
> Ti consigliamo di testare l'impostazione predefinita delle dimensioni, le priorità delle dimensioni e l'ordine in cui inserisci i dati nei documenti.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Dimensioni**, quindi scegli il collegamento correlato.  
2. Nella pagina **Dimensioni**, seleziona la dimensione appropriata e quindi scegli l'azione **Dim. di default tipo di conto**.  
3. Compila i campi per ogni nuova dimensione che vuoi impostare. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Se vuoi rendere obbligatoria una dimensione senza assegnare ad essa un valore predefinito, non compilare il campo **Codice valore dimensioni** e seleziona **Codice obbligatorio** nel campo **Registrazione valore**.  

> [!WARNING]  
> Se un conto viene utilizzato nel processo batch **Rettifica tassi di cambio** o nel processo batch **Registra costo magazzino in C/G**, non selezionare **Codice obbligatorio** o **Stesso Cod.**. Questi processi batch non supportano l'uso di codici di dimensione.  

> [!NOTE]  
> Se a un conto deve essere assegnata una dimensione diversa da quella predefinita per il tipo di conto, è necessario impostare una nuova dimensione predefinita per il conto. La dimensione predefinita per il conto sostituirà la dimensione predefinita per quel tipo di conto.  

### <a name="to-set-up-default-dimension-priorities" />Per impostare priorità nelle dimensioni di default

Per tipi di conto diversi, come un conto cliente e un conto articoli, possono essere impostate dimensioni predefinite diverse. Un movimento può quindi avere più di una proposta di dimensione predefinita. Per evitare conflitti è possibile applicare delle regole di priorità alle diverse fonti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Priorità dimensioni di default**, quindi seleziona il collegamento correlato.  
2. Nel campo **Codice origine** della pagina **Priorità dimensioni di default** immetti il codice origine per la tabella movimenti a cui vuoi applicare le priorità dimensioni di default.  
3. Compila i campi per ogni priorità della dimensione predefinita desiderata per il codice di origine selezionato.
4. Ripeti la procedura per ogni codice di origine per il quale vuoi impostare le priorità della dimensione predefinita.  

> [!IMPORTANT]  
> Se vengono impostate due tabelle con la stessa priorità per lo stesso codice origine, in [!INCLUDE[prod_short](includes/prod_short.md)] verrà sempre selezionata la tabella con l'ID minore.  

### <a name="to-set-up-dimension-combinations" />Per impostare combinazioni dimensioni

Per evitare di registrare movimenti con dimensioni contraddittorie o non pertinenti è possibile bloccare o limitare specifiche combinazioni di due dimensioni. Se una combinazione di dimensioni è bloccata, non è possibile registrare entrambe le dimensioni nello stesso movimento, qualsiasi siano i valori dimensioni. Una combinazione dimensioni limitata permette invece di registrare entrambe le dimensioni nello stesso movimento, ma soltanto per determinate combinazioni di valori dimensioni.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Combinazioni di dimensioni**, quindi seleziona il collegamento correlato.  
2. Nella pagina **Combinazioni di dimensioni** seleziona il campo della combinazione dimensioni desiderato tra le seguenti opzioni.  

    |Campo|Descrizione|
    |----------------------------------|---------------------------------------|  
    |**Nessuna limitazione**|La combinazione di dimensioni non avrà alcuna restrizione. Tutti i valori di dimensione sono ammessi.|  
    |**Limitato**|La combinazione di dimensioni avrà delle restrizioni che dipenderanno dai valori dimensioni che vengono immessi. È necessario definire le limitazioni nella pagina **Combinazione Valori Dimensioni**.|  
    |**Bloccato**|Questa combinazione di dimensioni non è ammessa.|  

3. Se è stata selezionata l'opzione **Limitato** è necessario definire quali combinazioni di valori dimensioni sono bloccati. Per effettuare questa operazione, seleziona il campo per definire la combinazione dei valori delle dimensioni.  
4. Selezionare una combinazione bloccata di valori di dimensione e selezionare l'opzione **Bloccato** nel campo. Un campo vuoto indica che la combinazione di valori dimensioni corrispondente è ammessa. Ripetere la procedura se sono presenti altre combinazioni bloccate  

> [!NOTE]  
> Su righe e colonne vengono visualizzate le stesse dimensioni e pertanto tutte le combinazioni sono presenti due volte. In [!INCLUDE[prod_short](includes/prod_short.md)] l'impostazione scelta viene automaticamente visualizzata in entrambi i campi. Non è possibile immettere alcuna selezione nei campi lungo la diagonale che ha origine nell'angolo in alto a sinistra perché questi campi hanno la stessa dimensione sia sulla riga che sulla colonna.  
>
> L'opzione selezionata viene visualizzata dopo l'uscita dal campo.  
>
> Per visualizzare il nome delle dimensioni anziché il codice, selezionare il campo **Mostra nome colonna**.

### <a name="to-set-up-global-and-shortcut-dimensions" />Per impostare dimensioni globali e a collegamento rapido

Le dimensioni globali e a collegamento rapido possono essere utilizzate come filtri in [!INCLUDE[prod_short](includes/prod_short.md)], tra cui report, processi batch, pagine di movimento contabili e visualizzazioni analisi. Le dimensioni globali e a collegamento rapido possono inserite direttamente senza prima aprire la pagina **Dimensioni**. Nelle righe di registrazioni e documenti, è possibile selezionare dimensioni globali e a collegamento rapido in un campo della riga. È possibile impostare due dimensioni globali e otto dimensioni a collegamento rapido. Scegliere le dimensioni che si utilizzano maggiormente.

> [!IMPORTANT]
> La modifica di una dimensione globale o a collegamento rapido richiede l'aggiornamento di tutti i movimenti registrati con la dimensione. Per modificare una dimensione globale puoi utilizzare la funzione **Cambia dimensioni globali**, ma questa soluzione può richiedere molto tempo, influire sulle prestazioni e comportare il blocco delle tabelle durante l'aggiornamento. Assicurati di scegliere con attenzione le dimensioni globali e a collegamento rapido in modo da non dover modificarle in seguito. Per modificare una dimensione a collegamento rapido, utilizzare l'azione **Cambia dimensioni**.
>
> Per ulteriori informazioni, vedi la sezione [Per cambiare le dimensioni globali](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Quando si aggiunge o si modifica una dimensione globale o a collegamento rapido, viene eseguita automaticamente la disconnessione e una nuova connessione di modo che il nuovo valore possa essere utilizzato.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.
2. Nella Scheda dettaglio **Dimensioni**, riempire i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions" />Per cambiare le dimensioni globali

Quando modifichi una dimensione globale o a collegamento rapido, tutti movimenti registrati con la dimensione in questione vengono aggiornati. Poiché questo processo può richiedere molto tempo e influire sulle prestazioni, vengono fornite due diverse modalità per adattare il processo alle dimensioni del database.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Cambia dimensioni globali**.
3. Nella parte superiore della pagina, seleziona una delle due seguenti modalità per eseguire il processo batch.

    |Opzione|Descrizione|
    |-|-|
    |**Sequenziale**|(Predefinita) La modifica viene eseguita in una transazione che reimposta tutti i movimenti sulle dimensioni precedenti alla modifica.<br /><br />Questa opzione è consigliata se la società ha relativamente pochi movimenti registrati, nel qual caso il processo batch richiede il tempo più breve per essere completato. Il processo blocca più tabelle e blocca altri utenti fino al suo completamento. Tieni presente che con i database di grandi dimensioni, il completamento del processo potrebbe non riuscire in questa modalità. In tal caso, utilizzare l'opzione **Parallela**.|
    |**Parallela**|La modifica della dimensione avviene in più sessioni in background e l'operazione viene suddivisa in più transazioni. Per utilizzare questa opzione, attiva l'interruttore **Elaborazione parallela**. <br /><br />Questa opzione è consigliata per società o database di grandi dimensioni con molti movimenti registrati poiché il completamento sarà il più breve. Tieni presente che con questa modalità, il processo di aggiornamento non verrà avviato se sono presenti più sessioni di database attive.|  

4. Nei campi **Cod. dimens. globale 1** e/o **Cod. dimens. globale 2** immettere la/e nuova/e dimensione/i. Le dimensioni correnti sono visualizzate in grigio dietro i campi.
5. A seconda della modalità, eseguire una delle seguenti operazioni:
    * In modalità **Sequenziale**, scegliere l'azione **Avvia**.
    * In modalità **Parallelo**, scegliere l'azione **Prepara**.

    La scheda **Movimenti log** viene compilata con le informazioni sulle dimensioni da modificare.
6. Esci da [!INCLUDE[prod_short](includes/prod_short.md)], quindi accedi nuovamente.
7. Scegli l'azione **Avvia** per iniziare l'elaborazione parallela delle modifiche delle dimensioni.

### <a name="example-of-dimension-setup" />Esempio di setup dimensioni

Supponiamo che la società desideri tenere traccia delle transazioni in base alla struttura organizzativa e alle posizioni geografiche. A tale scopo, puoi impostare due dimensioni nella pagina **Dimensioni** :

* **AREA**  
* **REPARTO**  

| Codice | Name | Didascalia codice | Didascalia filtro |
| --- | --- | --- | --- |
| AREA |Area |Codice area |Filtro area |
| REPARTO |Reparto |Codice reparto |Filtro per reparto |

Per **AREA**, aggiungi i seguenti valori dimensioni:

| Codice | Nome | Tipo di valore dimensioni |
| --- | --- | --- |
| 10 |America |Inizio-Totale |
| 20 |Nord America |Standard |
| 30 |Pacifico |Standard |
| 40 |Sud America |Standard |
| 50 |America, totale |Fine-Totale |
| 60 |Europa |Inizio-Totale |
| 70 |UE |Standard |
| 80 |Extracomunitaria |Standard |
| 90 |Europa, totale |Fine-Totale |

Per le zone due are geografiche principali, Europa e America,, si aggiungono sottocategorie per regioni tramite l'indentazione dei valori di dimensione. In questo modo puoi ottenere report per vendite o spese nelle varie aree e i totali per le aree geografiche più grandi. È anche possibile scegliere di utilizzare paesi, aree, province o città come valori dimensioni, a seconda della propria attività.

> [!NOTE]  
> Per impostare una gerarchia, i codici devono essere in ordine alfabetico. Sono inclusi quelli dei valori dimensioni che forniti in [!INCLUDE[prod_short](includes/prod_short.md)].  

Per **REPARTO**, aggiungi i seguenti valori dimensioni:

| Codice | Nome | Tipo di valore dimensioni |
| --- | --- | --- |
| AMMIN |Setup |Standard |
| PROD |Produzione |Standard |
| VENDITE |Vendite |Standard |

Con questa impostazione, puoi aggiungere due dimensioni come dimensioni globali nella pagina **Setup contabilità generale**. Ciò significa che puoi utilizzare AREA e REPARTO come filtri per i movimenti di contabilità generale, nonché per tutti i report. Le dimensioni globali sono inoltre disponibili automaticamente come dimensioni a collegamento rapido nelle righe di registrazione e nelle testate dei documenti.

## <a name="getting-an-overview-of-dimensions-used-multiple-times" />Sintesi delle dimensioni utilizzate più volte

La pagina **Dimensioni di Default-Multipli** consente di determinare come un gruppo di conti utilizza le dimensioni e i valori delle dimensioni. Puoi impostarla evidenziando più conti, quindi specificando le dimensioni predefinite e i valori delle dimensioni per essi. Successivamente, l'applicazione suggerisce queste dimensioni e valori dimensioni ogni volta che viene utilizzato uno di questi conti, ad esempio in una riga di registrazione. I campi dimensione vengono compilati automaticamente, facilitando la registrazione dei movimenti. Inoltre tieni presente che i valori dimensioni suggeriti possono tuttavia essere modificati, ad esempio, in una riga di registrazione.

La pagina **Dimensioni di Default-Multipli** contiene i seguenti campi:

|Campo|Descrizione|
|-----|-----------|  
|**Codice dimensione**|Mostra tutte le dimensioni predefinite impostate in uno o più conti evidenziati. Selezionando questo campo puoi visualizzare una lista di tutte le dimensioni disponibili. Selezionando una dimensione, tale dimensione viene impostata come predefinita per tutti i conti evidenziati.|
|**Codice valore dimensioni**|Mostra un valore dimensioni singolo oppure la dicitura Conflitto. Se nel campo è presente un valore dimensioni, a tutti i campi selezionati corrisponderà lo stesso valore dimensioni di default. Se nel campo è presente la dicitura Conflitto, non è stato impostato lo stesso valore dimensioni predefinito per tutti i conti evidenziati. Selezionando il campo **Codice dimensione** visualizzi una lista di tutti i valori dimensioni disponibili. Selezionando un valore dimensioni, viene impostato come predefinito per tutti i conti evidenziati.|
|**Registrazione valore**|Mostra una singola regola per la registrazione del valore oppure la dicitura Conflitto. Se nel campo è presente una regola di registrazione, allora a tutti i conti selezionati corrisponderà la stessa regole di registrazione del valore per un valore dimensioni. Se nel campo è presente la dicitura Conflitto, non è stata impostata la stessa regola di registrazione del valore per un valore dimensione per tutti i conti evidenziati. Selezionando il campo **Registrazione valore** visualizzi una lista delle regole per la registrazione del valore di una dimensione. Selezionando una regola per la registrazione del valore, tale regola viene applicata per tutti i conti evidenziati.|

## <a name="use-dimensions" />Usare le dimensioni

In un documento come un ordine di vendita, è possibile aggiungere le informazioni sulle dimensioni sia per una singola riga del documento che l'intero documento. Pertanto, nella pagina **Ordine di vendita** puoi immettere i valori dimensioni per le prime due dimensioni a collegamento rapido nelle singole righe vendita e aggiungere altre informazioni sulle dimensioni selezionando il pulsante **Dimensioni**.  

Se si lavora nelle registrazioni invece, è possibile aggiungere informazioni sulle dimensioni a un movimento nello stesso modo, se le dimensioni a collegamento rapido sono state impostate come campi direttamente sulle righe di registrazione.  

Puoi anche impostare le dimensioni predefinite per i conti o i tipi di conto, in modo che le dimensioni e i valori dimensioni vengano compilati automaticamente.

### <a name="to-view-global-dimensions-in-ledger-entry-pages" />Per visualizzare le dimensioni globali nelle pagine dei movimenti contabili:

I valori delle dimensioni globali vengono sempredefiniti e denominati dalla società. Per visualizzare le dimensioni globali della società, aprire la pagina **Setup contabilità generale**.

In una pagina di movimenti contabili è possibile vedere se sono state impostate le dimensioni globali per i movimenti. Le due dimensioni globali si differenziano dalle altre dimensioni in quanto è possibile utilizzarle come filtro in qualsiasi punto di [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Nella pagina **Piano dei conti**, selezionare l'azione **Movimenti contabili**.  
3. Per visualizzare solo i movimenti pertinenti, imposta uno o più filtri nella pagina.  
4. Per visualizzare tutte le dimensioni di un movimento, seleziona il movimento e scegli l'azione **Dimensioni**.  

> [!NOTE]  
> La pagina **Dimensioni Voci Partitario** visualizza le dimensioni di un movimento contabile alla volta. Il contenuto della pagina **Dimensioni Voci Partitario** cambia al variare del movimento contabile selezionato.

## <a name="see-related-microsoft-trainingtrainingmodulesdimensions-dynamics-365-business-centralindex" />Vedi il relativo [training Microsoft](/training/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also" />Vedere anche

[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
