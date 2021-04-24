---
title: Utilizzo delle Dimensioni per tenere traccia e analizzare facilmente i dati
description: Utilizza le dimensioni per classificare i movimenti, ad esempio, per reparto o progetto, in modo da tenere traccia e analizzare facilmente i dati per consentirti di prendere buone decisioni aziendali.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: aa97686299648b81e68aef1a3701e0c32d73138a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774082"
---
# <a name="working-with-dimensions"></a>Utilizzo delle dimensioni
Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare nei documenti, ad esempio ordini vendita. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

Ad esempio, anziché impostare conti di contabilità generale distinti per ogni reparto e progetto, è possibile utilizzare le dimensioni come base per l'analisi ed evitare di dover creare un piano dei conti complesso. Per ulteriori informazioni, vedere [Business Intelligence](bi.md).

Un altro esempio consiste nell'impostare una dimensione denominata *Reparto* e nell'utilizzare tale dimensione al momento della registrazione dei documenti di vendita. In questo modo sarà possibile utilizzare strumenti di business intelligence per vedere quale reparto ha venduto quali articoli. Più dimensioni si utilizzano, più dettagliati sono i report su cui è possibile basare le decisioni aziendali. Ad esempio, un singolo movimento di vendita può includere informazioni di più dimensioni, quali:  

* Il conto in cui è stata registrata la vendita dell'articolo  
* Dove l'articolo è stato venduto
* Chi lo ha venduto
* Il tipo di cliente che lo ha acquistato  

## <a name="analyzing-by-dimensions"></a>Analisi per dimensioni
Dimensioni svolge un ruolo importante in business intelligence, ad esempio quando si definiscono le visualizzazioni analisi. Per ulteriori informazioni, vedere [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

> [!TIP]
> Un modo rapido di analizzare i dati transazionali in base alle dimensioni consiste nell'utilizzare l'azione **Imposta filtro dimensione** per filtrare i totali per dimensione nel piano dei conti e nelle pagine dei movimenti.

## <a name="dimension-sets"></a>Set di dimensioni
<!--we describe what they are, but not their value.-->
Un set di dimensioni è una combinazione univoca di valori dimensioni. Viene archiviato come movimenti set di dimensioni nel database. Ogni movimento set di dimensioni rappresenta un valore dimensioni singolo. Il set di dimensioni è identificato da un ID set di dimensioni comune assegnato a ogni movimento set di dimensioni che appartiene al set di dimensioni.  

Quando si crea una riga di registrazione, una testata del documento o una riga documento, è possibile specificare una combinazione di valori dimensioni. Anziché archiviare esplicitamente ogni valore dimensioni nel database, viene assegnato un ID set di dimensioni alla riga di registrazione, alla testata del documento o alla riga del documento per specificare il set di dimensioni.  

## <a name="setting-up-dimensions"></a>Setup delle dimensioni
È possibile definire le dimensioni e i valori di dimensione da utilizzare per classificare le registrazioni e i documenti, ad esempio ordini di vendita e di acquisto. Impostare le dimensioni nella pagina **Dimensioni** in cui si crea una riga per ogni dimensione, ad esempio *Progetto*, *Reparto*, *Area* e *Agente*.

Vengono inoltre impostati i valori delle dimensioni. Ad esempio, i valori potrebbero essere i reparti della società. I valori di dimensione possono essere impostati in una struttura gerarchica simile al piano dei conti, in modo che i dati possano essere suddivisi in vari livelli di granularità e i sottoinsiemi dei valori di dimensione sommati. In base alle necessità, è possibile impostare un numero illimitato di dimensioni e di valori dimensioni che possono essere utilizzati da tutti gli utenti nella società.

Quando dimensioni e valori sono impostati, è possibile definire dimensioni globali e a collegamento rapido nella pagina **Setup contabilità generale** che saranno sempre disponibili per essere selezionati come campi nelle righe di documenti e registrazioni, e movimenti contabili, senza dover aprire prima la pagina **Dimensioni**. Per ulteriori informazioni, vedere [Per impostare dimensioni globali e a collegamento rapido](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Dimensioni globali** utilizzate come filtro, ad esempio, per report, processi batch e report XML. È possibile utilizzare solo due dimensioni globali, scegliere pertanto le dimensioni che verranno utilizzate più spesso.
* Le **dimensioni a collegamento rapido** sono disponibili come campi nelle registrazioni, nelle righe dei documenti e nei movimenti contabili. È possibile creare fino a otto dimensioni.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Per impostare le dimensioni di default per clienti, fornitori e altri conti
È possibile assegnare una dimensione di default per un conto specifico. La dimensione verrà copiata nelle registrazioni o nel documento quando si immette il numero di conto in una riga, ma è possibile eliminare o modificare il codice nella riga se il dato non è appropriato. È inoltre possibile impostare una dimensione richiesta per la registrazione del movimento con un tipo di conto specifico.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Dimensioni** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Dimensioni**, selezionare la dimensione appropriata e quindi scegliere l'azione **Dim. di default tipo di conto**.  
4.  Compilare i campi per ogni nuova dimensione di default che si desidera impostare. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Se si desidera rendere obbligatoria una dimensione senza assegnare ad essa un valore di default, non compilare il campo **Codice valore dimensioni** e selezionare **Codice obbligatorio** nel campo **Registrazione valore**.  

> [!WARNING]  
>  Se un conto viene utilizzato nel processo batch **Rettifica tassi di cambio** o nel processo batch **Registra costo magazzino in C/G**, non selezionare **Codice obbligatorio** o **Stesso Cod.**. Questi processi batch non supportano l'uso di codici di dimensione.  

> [!NOTE]  
>  Se a un conto deve essere assegnata una dimensione diversa da quella predefinita per il tipo di conto, è necessario impostare una dimensione predefinita per il conto in questione. La dimensione predefinita per il conto sostituirà la dimensione predefinita per quel tipo di conto.  

### <a name="to-set-up-default-dimension-priorities"></a>Per impostare priorità nelle dimensioni di default  
Per tipi di conto diversi, come un conto cliente e un conto articoli, possono essere impostate dimensioni di default diverse. Un movimento potrà quindi avere più di una proposta di dimensione di default per un'unica dimensione. Per evitare conflitti è possibile applicare delle regole di priorità alle diverse fonti.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Priorità dimensioni di default** e quindi scegliere il collegamento correlato.  
2.  Nel campo **Codice origine** della pagina **Priorità dimensioni di default** immettere il codice origine per la tabella movimenti a cui si desidera applicare le priorità dimensioni di default.  
3.  Compilare i campi per ogni priorità della dimensione di default desiderata per il codice di origine selezionato.
4.  Ripetere la procedura per ogni codice di origine per il quale si desidera impostare le priorità della dimensione di default.  

> [!IMPORTANT]  
>  Se vengono impostate due tabelle con la stessa priorità per lo stesso codice origine, in [!INCLUDE[prod_short](includes/prod_short.md)] verrà sempre selezionata la tabella con l'ID minore.  

### <a name="to-set-up-dimension-combinations"></a>Per impostare combinazioni dimensioni  
Per evitare di registrare movimenti con dimensioni contraddittorie o non pertinenti è possibile bloccare o limitare specifiche combinazioni di due dimensioni. Se una combinazione di dimensioni è bloccata non è possibile registrare entrambe le dimensioni nello stesso movimento, qualsiasi siano i valori dimensioni. Una combinazione dimensioni limitata permette invece di registrare entrambe le dimensioni nello stesso movimento, ma soltanto per determinate combinazioni di valori dimensioni.

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Combinazioni di dimensioni** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Combinazioni di dimensioni** selezionare il campo della combinazione dimensioni e selezionare una delle seguenti opzioni.  

    |Campo|Description|
    |----------------------------------|---------------------------------------|  
    |**Nessuna limitazione**|La combinazione di dimensioni non avrà alcuna restrizione. Tutti i valori di dimensione sono ammessi.|  
    |**Limitato**|La combinazione di dimensioni avrà delle restrizioni che dipenderanno dai valori dimensioni che vengono immessi. È necessario definire le limitazioni nella pagina **Combinazione Valori Dimensioni**.|  
    |**Bloccato**|Questa combinazione di dimensioni non è ammessa.|  

3.  Se è stata selezionata l'opzione **Limitato** è necessario definire quali combinazioni di valori dimensioni sono bloccati. Per effettuare questa operazione, selezionare il campo per definire la combinazione delle dimensioni.  
4.  Selezionare una combinazione bloccata di valori di dimensione e selezionare l'opzione **Bloccato** nel campo. Un campo vuoto indica che la combinazione di valori di dimensione corrispondente è ammessa. Ripetere la procedura se sono presenti altre combinazioni bloccate  

> [!NOTE]  
>  Su righe e colonne vengono visualizzate le stesse dimensioni e pertanto tutte le combinazioni sono presenti due volte. In [!INCLUDE[prod_short](includes/prod_short.md)] l'impostazione scelta viene automaticamente visualizzata in entrambi i campi. Non è possibile immettere alcuna selezione nei campi lungo la diagonale che ha origine nell'angolo in alto a sinistra perché questi campi hanno la stessa dimensione sia sulla riga che sulla colonna.  
>   
>  L'opzione selezionata viene visualizzata dopo l'uscita dal campo.  
>   
>  Per visualizzare il nome delle dimensioni anziché il codice, selezionare il campo **Mostra nome colonna**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Per impostare dimensioni globali e a collegamento rapido
Le dimensioni globali e a collegamento rapido possono essere utilizzate come filtri in [!INCLUDE[prod_short](includes/prod_short.md)], tra cui report, processi batch, pagine di movimento contabili e visualizzazioni analisi. Le dimensioni globali e a collegamento rapido sono sempre disponibili per essere inserite direttamente senza prima aprire la pagina **Dimensioni**. Nelle righe di registrazioni e documenti, è possibile selezionare dimensioni globali e a collegamento rapido in un campo della riga. È possibile impostare due dimensioni globali e otto dimensioni a collegamento rapido. Scegliere le dimensioni che si utilizzano maggiormente.

> [!Important]  
> La modifica di una dimensione globale o a collegamento rapido richiede l'aggiornamento di tutti i movimenti registrati con la dimensione. Per modificare una dimensione globale è possibile utilizzare la funzione **Cambia dimensioni globali**, ma questa soluzione può richiedere molto tempo, influire sulle prestazioni e comportare il blocco delle tabelle durante l'aggiornamento. Di conseguenza, scegliere con attenzione le dimensioni globali e a collegamento rapido in modo da non dover modificarle in seguito. Per modificare una dimensione a collegamento rapido, utilizzare l'azione **Cambia dimensioni**. <br /><br />
> Per ulteriori informazioni, vedere [Per cambiare le dimensioni globali](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Quando si aggiunge o si modifica una dimensione globale o a collegamento rapido, viene eseguita automaticamente la disconnessione e una nuova connessione di modo che il nuovo valore possa essere utilizzato.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.
2. Nella Scheda dettaglio **Dimensioni**, riempire i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Per cambiare le dimensioni globali
Quando si modifica una dimensione globale o a collegamento rapido, tutti movimenti registrati con la dimensione in questione vengono aggiornati. Poiché questo processo può richiedere molto tempo e influire sulle prestazioni, vengono fornite due diverse modalità per adattare il processo alle dimensioni del database.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Cambia dimensioni globali**.
3. Nella parte superiore della pagina, selezionare una delle seguenti opzioni per definire in quale modalità viene eseguito il processo batch.

    |Opzione|Descrizione|
    |-|-|
    |**Sequenziale**|(Predefinita) La modifica viene eseguita in una transazione che reimposta tutti i movimenti sulle dimensioni precedenti alla modifica.<br /><br />Questa opzione è consigliata se la società contiene relativamente pochi movimenti pubblicati in cui il completamento richiederà il tempo più breve. Il processo blocca più tabelle e blocca altri utenti fino al suo completamento. Da notare che su database di grandi dimensioni, il completamento del processo potrebbe non riuscire in questa modalità. In tal caso, utilizzare l'opzione **Parallela**.|
    |**Parallela**|La modifica della dimensione avviene in più sessioni in background e l'operazione viene suddivisa in più transazioni. Per utilizzare questa opzione, attiva l'interruttore **Elaborazione parallela**. <br /><br />Questa opzione è consigliata per società o database di grandi dimensioni con molti movimenti registrati poiché il completamento sarà il più breve. Da notare che con questa modalità, il processo di aggiornamento non verrà avviato se sono presenti più sessioni di database attive.|  

4. Nei campi **Cod. dimens. globale 1** e/o **Cod. dimens. globale 2** immettere la/e nuova/e dimensione/i. Le dimensioni correnti sono visualizzate in grigio dietro i campi.
5. A seconda della modalità, eseguire una delle seguenti operazioni:
    * In modalità **Sequenziale**, scegliere l'azione **Avvia**.
    * In modalità **Parallelo**, scegliere l'azione **Prepara**.

    La scheda **Movimenti log** viene compilato con le informazioni sulle dimensioni che verranno modificate.
7. Uscire da [!INCLUDE[prod_short](includes/prod_short.md)], quindi accedere nuovamente.
8. Scegliere l'azione **Avvia** per avviare l'elaborazione parallela delle modifiche delle dimensioni. <!--is this also dependent on the mode?-->

### <a name="example-of-dimension-setup"></a>Esempio di setup dimensioni
Supponiamo che la società desideri tenere traccia delle transazioni in base alla struttura organizzativa e alle posizioni geografiche. A tale scopo, è possibile impostare due dimensioni nella pagina **Dimensioni** :

* **AREA**  
* **REPARTO**  

| Codice | Name | Didascalia codice | Didascalia filtro |
| --- | --- | --- | --- |
| AREA |Area |Codice area |Filtro area |
| REPARTO |Reparto |Codice reparto |Filtro per reparto |

Per **AREA**, è possibile aggiungere i seguenti valori dimensioni:

| Codice | Name | Tipo valori dimensioni |
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

Per le zone due are geografiche principali, Europa e America,, si aggiungono sottocategorie per regioni tramite l'indentazione dei valori di dimensione. In questo modo sarà possibile ottenere report per vendite o spese nelle varie regioni e i totali per le aree geografiche più grandi. È anche possibile scegliere di utilizzare paesi o regioni come valori di dimensione, province o città, a seconda della propria attività.

> [!NOTE]  
>   Per impostare una gerarchia, i codici devono essere in ordine alfabetico. Inclusi quelli dei valori dimensioni che forniti in [!INCLUDE[prod_short](includes/prod_short.md)].  

Per **REPARTO**, è possibile aggiungere i seguenti valori dimensioni:

| Codice | Name | Tipo valori dimensioni |
| --- | --- | --- |
| AMMIN |Setup |Standard |
| PROD |Produzione |Standard |
| VENDITE |Vendite |Standard |

Con questa impostazione, è possibile aggiungere due dimensioni come dimensioni globali nella pagina **Setup contabilità generale**. Ciò significa che è possibile utilizzare AREA e REPARTO come filtri per i movimenti di contabilità generale, nonché per tutti i report e le situazioni contabili. Le dimensioni globali sono inoltre disponibili automaticamente come dimensioni a collegamento rapido nelle righe di registrazione e nelle testate dei documenti.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Sintesi delle dimensioni utilizzate più volte
La pagina **Dimensioni di Default-Multipli** consente di determinare come un gruppo di conti utilizza le dimensioni e i valori delle dimensioni. Per effettuare questa operazione, evidenziare i vari conti nella lista dei conti, quindi specificare per essi le dimensioni e i valori dimensioni di default. Se per i conti evidenziati sono state specificate le dimensioni di default, tali dimensioni e i valori dimensioni verranno suggeriti automaticamente ogni volta che si utilizza uno dei conti, ad esempio, in una riga di registrazioni. I campi dimensione vengono compilati automaticamente, facilitando la registrazione dei movimenti. I valori dimensioni suggeriti possono tuttavia essere modificati, ad esempio, in una riga di registrazioni.

La pagina **Dimensioni di Default-Multipli** contiene i seguenti campi:

|Campo|Description|
|-----|-----------|  
|**Codice dimensione**|Mostra tutte le dimensioni di default impostate in uno o più conti evidenziati. Selezionando il campo è possibile visualizzare una lista di tutte le dimensioni disponibili. Selezionando una dimensione, tale dimensione verrà impostata come default per tutti i conti evidenziati.|
|**Codice valore dimensioni**|Mostra un valore dimensioni singolo oppure la dicitura Conflitto. Se nel campo è presente un valore dimensioni, a tutti i campi selezionati corrisponderà lo stesso valore dimensioni di default. Se nel campo è presente la dicitura Conflitto, non è stato impostato lo stesso valore dimensioni di default per tutti i conti evidenziati. Selezionando il campo è possibile visualizzare una lista di tutti i valori dimensioni disponibili. Selezionando un valore dimensioni, tale valore dimensioni verrà impostato come default per tutti i conti evidenziati.|
|**Registrazione valore**|Mostra una singola regola per la registrazione del valore oppure la dicitura Conflitto. Se nel campo è presente una regola di registrazione, allora a tutti i conti selezionati corrisponderà la stessa regole di registrazione del valore per un valore dimensioni. Se nel campo è presente la dicitura Conflitto, non è stata impostata la stessa regola di registrazione del valore per un valore dimensione per tutti i conti evidenziati. Selezionando il campo Registrazione valore è possibile visualizzare una lista delle regole per la registrazione del valore. Selezionando una regola per la registrazione del valore, tale regola verrà applicata per tutti i conti evidenziati.|

## <a name="using-dimensions"></a>Utilizzo delle dimensioni
In un documento come un ordine di vendita, è possibile aggiungere le informazioni sulle dimensioni sia per una singola riga del documento che l'intero documento. Ad esempio, nella pagina **Ordine di vendita** è possibile immettere i valori dimensioni per le prime due dimensioni a collegamento rapido nelle singole righe vendita e aggiungere altre informazioni sulle dimensioni selezionando il pulsante **Dimensioni**.  

Se si lavora nelle registrazioni invece, è possibile aggiungere informazioni sulle dimensioni a un movimento nello stesso modo, se le dimensioni a collegamento rapido sono state impostate come campi direttamente sulle righe di registrazione.  

È possibile impostare le dimensioni di default per i conti o i tipi di conto, in modo che le dimensioni e i valori dimensioni vengano compilati automaticamente.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Per visualizzare le dimensioni globali nelle pagine dei movimenti contabili:  
I valori delle dimensioni globali vengono sempre\-definiti e denominati dalla società. Per visualizzare le dimensioni globali della società, aprire la pagina **Setup contabilità generale**.  

In una pagina di movimenti contabili è possibile vedere se sono state impostate le dimensioni globali per i movimenti. Le due dimensioni globali si differenziano da tutte le altre dimensioni in quanto è possibile utilizzarle come filtro in qualsiasi punto di [!INCLUDE[prod_short](includes/prod_short.md)].  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Piano dei conti**, selezionare l'azione **Movimenti contabili**.  
3.  Per visualizzare solo i movimenti pertinenti, impostare uno o più filtri nella pagina.  
4.  Per visualizzare tutte le dimensioni di un movimento, selezionare il movimento e scegliere l'azione **Dimensioni**.  

> [!NOTE]  
>  La pagina **Dimensioni Voci Partitario** visualizza le dimensioni di un movimento contabile alla volta. Il contenuto della pagina **Dimensioni Voci Partitario** cambierà al variare del movimento contabile selezionato.

## <a name="troubleshooting-dimensions-errors"></a>Risoluzione dei problemi relativi alle dimensioni
Quando si registrano documenti o righe di registrazione che contengono dimensioni, possono verificarsi vari errori che in genere sono relativi a un'errata impostazione o assegnazione di dimensioni.

> [!NOTE]
> Nell'elenco di potenziali messaggi di errore seguente, i codici *%X* sono segnaposti per le variabili di dati che il messaggio effettivo conterrà nell'interfaccia utente a seconda del contesto. Ad esempio, *%1 %2 bloccata.* potrebbe essere visualizzato nell'interfaccia utente come “Codice dimensione AREA bloccato".  

|Problema|Messaggio di errore|Soluzione possibile|
|-----|-------------|-----------------|
|Dimensione bloccata|%1 %2 bloccata.|- Trovare documenti non registrati che contengono il set di dimensioni con la dimensione bloccata e sbloccarla.<br />- Rimuovere la riga del set di dimensioni per la dimensione bloccata.|
|Dimensione eliminata|Impossibile trovare %1 %2.|- Ripristinare la dimensione mancante.<br />- Trovare documenti non registrati che contengono il set di dimensioni con la dimensione mancante e aggiungerla.<br />- Rimuovere la riga del set di dimensioni per la dimensione mancante.|
|Valore di dimensione bloccato|%1 %2 - %3 bloccato.|- Trovare documenti non registrati che contengono il set di dimensioni con il valore di dimensione bloccato e sbloccarlo.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione bloccato.|
|Valore di dimensione eliminato|    %1 per %2 mancante.|- Ripristinare il valore di dimensione mancante.<br />- Trovare documenti non registrati che contengono il set di dimensioni con il valore di dimensione mancante e aggiungerlo.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione mancante.|
|Valore di dimensione non consentito|Il tipo di valore di dimensione per %1 %2 - %3 non deve essere %4.|- Impostare il campo **Tipo valori dimensioni** nella pagina **Valori dimensioni** su **Standard** o **Inizio-Totale**.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione bloccato.|
|Combinazione di dimensioni bloccata|Le dimensioni %1 e %2 non possono essere utilizzate contemporaneamente.|- Trovare documenti non registrati che contengono il set di dimensioni con la combinazione di dimensioni bloccata e sbloccarla.<br />- Modificare una delle righe del set di autorizzazioni in conflitto per la combinazione di dimensioni.|
|Combinazione di valori di dimensioni bloccata|Le combinazioni di dimensioni %1 - %2 e %3 - %4 non possono essere usare contemporaneamente.|- Trovare documenti non registrati che contengono il set di dimensioni con la combinazione di valori di dimensioni bloccata e sbloccarla.<br />- Modificare una delle righe del set di autorizzazioni in conflitto per la combinazione di valori di dimensioni.|
|Codice del valore di dimensione vuoto per la dimensione di default in cui il campo **Registrazione valore** contiene **Codice obbligatorio**|- Selezionare un %1 per %2 %3.<br />- Selezionare un %1 per i %2 %3 per %4 %5.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere un valore di dimensione non vuoto per la dimensione in conflitto nel set di dimensioni.|
|Codice del valore di dimensione errato per la dimensione di default in cui il campo **Registrazione valore** contiene **Stesso Cod.**|- Selezionare %1 %2 per i %3 %4.<br />- Selezionare %1 %2 per i %3 %4 per %5 %6.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere il valore di dimensione richiesto per la dimensione in conflitto nel set di dimensioni.|
|Codice del valore di dimensione non vuoto per la dimensione di default vuota in cui il campo **Registrazione valore** contiene **Stesso Cod.**|-%1 %2 deve essere vuoto.<br />-%1 %2 deve essere vuoto per %3 %4.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere un codice del valore di dimensione vuoto per la dimensione in conflitto nel set di dimensioni.|
|Valore di dimensione non previsto per la dimensione di default in cui il campo **Registrazione valore** contiene **Nessun Cod.**|-%1 %2 non deve essere nominato.<br />-%1 %2 non deve essere nominato per %3 %4.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Rimuovere la riga in conflitto dal set di dimensioni.|
|Una correzione dimensionale non viene completata correttamente.||-Scegli **Ripristina** per riportare la correzione allo stato di bozza. Ciò ripristina le modifiche e puoi eseguire nuovamente la correzione.|

## <a name="changing-dimension-assignments-after-posting"></a>Modifica delle assegnazioni delle dimensioni dopo la registrazione
Se scopri che è stata utilizzata una dimensione errata nei movimenti di contabilità generale registrati, puoi correggere i valori delle dimensioni e aggiornare le visualizzazioni di analisi. Ciò contribuirà a mantenere accurati i rapporti e le analisi finanziarie.

### <a name="setting-up-dimension-corrections"></a>Configurazione delle dimensioni delle correzioni
Ci sono due cose da considerare quando si impostano le correzioni delle dimensioni:

* Ci sono dimensioni che non vuoi che le persone cambino? Nella pagina **Impostazioni correzione quota**, specifica le dimensioni che desideri bloccare per le modifiche.
* A chi vuoi consentire di modificare le dimensioni? Per consentire alle persone di apportare modifiche, assegna l'autorizzazione **CORREZIONE DIM D365** agli utenti. Le autorizzazioni consentono loro di creare correzioni delle dimensioni, eseguirle e annullarle se necessario. Potranno anche specificare le dimensioni bloccate. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a>Correzione di una dimensione
È possibile selezionare manualmente uno o più movimenti di contabilità generale oppure utilizzare i filtri per selezionare gruppi di movimenti. Se necessario, puoi anche aggiungere o eliminare dimensioni. 

1. Per avviare una correzione dimensionale, utilizzare una delle seguenti pagine:

* Nella pagina **Registro/CG**, selezionando un registro, quindi scegliendo l'azione **Dimensioni corrette**. Ciò avvia una correzione per le voci nel registro selezionato.
* Nella pagina **Movimenti C/G**, scegliendo l'azione **Correzione dimensionale**. 

2. Nel campo **Descrizione** immettere le informazioni relative alla modifica. Altre persone potrebbero utilizzare queste informazioni in seguito per capire cosa è stato fatto.
3. Nella Scheda dettaglio **Movimenti contabili selezionati**, seleziona le voci pertinenti.

> [!IMPORTANT]
> Quando modifichi una selezione, i valori nella Scheda dettaglio **Modifiche alla correzione delle dimensioni** vengono ripristinati. Pertanto, selezionare sempre le voci prima di specificare le modifiche al valore della dimensione.

   Nella seguente tabella vengono illustrate le opzioni.

   |Opzione  |Descrizione  |
   |---------|---------|
   |Aggiungi movimenti correlati     |Aggiungi voci C/G che si trovano nello stesso registro C/G.|   
   |Aggiungi per filtro     |Utilizza i criteri dei filtri quando aggiungi voci C/G.|
   |Selezione manuale     |Seleziona voci C/G specifiche.         |
   |Aggiungi per dimensioni     |Filtra le voci C/G in base alle dimensioni.         |
   |Rimuovi movimenti     |Deseleziona voci C/G.         |
   |Gestisci criteri di selezione     |Tieni traccia del processo di selezione e, se necessario, annulla le selezioni.         |

4. Nella Scheda dettaglio **Modifiche alla correzione delle dimensioni**, scegli la dimensione che desideri modificare nel campo **Codice dimensione** e il nuovo valore nel campo **Nuovo codice valore dimensione**.
5. Per convalidare la correzione, scegli **Convalida le modifiche alle dimensioni**. Per ulteriori informazioni, vedi [Convalida delle correzioni delle dimensioni](finance-dimensions.md#validating-dimension-corrections).
6. Scegli **Esegui**.

### <a name="validating-dimension-corrections"></a>Convalida delle correzioni delle dimensioni
Prima di eseguire una correzione, è una buona idea convalidarla. La convalida controlla le restrizioni sulla registrazione del valore per i conti C/G, le restrizioni per le dimensioni e se i valori delle dimensioni sono bloccati. Durante la convalida, lo stato della correzione è impostato su **Convalida in corso**. Dopo aver convalidato una correzione, il risultato viene visualizzato nel campo **Stato di convalida**. Se sono stati rilevati errori, è possibile utilizzare l'azione **Visualizza errori** per indagare su di loro. Dopo aver corretto un errore, è necessario utilizzare l'azione **Riapri** per eseguire la correzione o una nuova convalida.

Puoi eseguire una correzione immediatamente o programmarne l'esecuzione in un secondo momento. Se stai eseguendo correzioni su un set di dati di grandi dimensioni, ti consigliamo di pianificarne l'esecuzione al di fuori dell'orario di lavoro. Per ulteriori informazioni, vedi [Correzioni delle dimensioni su set di dati di grandi dimensioni](finance-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a>Annullamento di una correzione
Dopo aver corretto una dimensione, se non ti piace quello che vedi puoi usare l'azione **Annulla** per ripristinare il valore precedente. Tuttavia, puoi annullare solo la correzione più recente. Prima di annullare una correzione, puoi convalidare le modifiche che verranno apportate dall'annullamento. Ad esempio, ciò è utile se le restrizioni sulle dimensioni sono cambiate dopo la correzione.

Se l'azione Annulla non è disponibile, ad esempio perché sono state apportate molte correzioni, è possibile utilizzare l'azione **Copia in bozza** per avviare una nuova correzione per le stesse voci.

### <a name="dimension-corrections-on-large-data-sets"></a>Correzioni dimensionali su set di dati di grandi dimensioni
Prestare attenzione quando si correggono set di voci di grandi dimensioni, ad esempio set che includono più di 10.000 voci. Se puoi, ti consigliamo di utilizzare i filtri per eseguire le correzioni su set di dati di dimensioni più piccole. È anche una buona idea eseguire le correzioni al di fuori del normale orario lavorativo. 

### <a name="using-analysis-views-with-dimension-corrections"></a>Utilizzo delle visualizzazioni delle analisi con correzioni delle dimensioni
Se **Aggiorna in registrazione** è abilitata per una visualizzazione analisi, [!INCLUDE[prod_short](includes/prod_short.md)] può visualizzare quando vengono registrati documenti e giornali. Puoi inoltre aggiornare le viste con questa impostazione abilitata con i risultati delle correzioni delle dimensioni. A tale scopo, attivare il toggle **Aggiorna visualizzazione analisi**. L'aggiornamento delle visualizzazioni delle analisi può influire sulle prestazioni, soprattutto per set di dati di grandi dimensioni, quindi si consiglia di aggiornare le visualizzazioni di analisi solo per set di dati di piccole dimensioni.  

### <a name="viewing-historical-dimension-corrections"></a>Visualizzazione delle correzioni delle dimensioni storiche
Se un movimento di contabilità generale è stato corretto, è possibile esaminare la modifica utilizzando l'azione **Storia delle correzioni dimensionali**.

### <a name="handling-incomplete-corrections"></a>Gestione delle correzioni incomplete
Se una correzione non viene completata, verrà visualizzato un avviso sulla scheda di correzione. In tal caso, puoi utilizzare l'azione **Ripristina** per riportare la correzione allo stato di bozza e annullare le modifiche. È quindi possibile eseguire nuovamente la correzione.

> [!NOTE]
> La reimpostazione di una correzione incompleta non influirà sugli aggiornamenti alle visualizzazioni dell'analisi perché questi si verificano alla fine del processo di correzione.

### <a name="using-cost-accounting-with-corrected-gl-entries"></a>Utilizzo della contabilità industriale con movimenti C/G corretti
Dopo aver corretto le dimensioni, i dati per la contabilità dei costi non saranno sincronizzati. La contabilità industriale utilizza le dimensioni per aggregare gli importi per i centri di costo e gli oggetti di costo e per eseguire le allocazioni dei costi. La modifica delle dimensioni per i movimenti C/G comporterà probabilmente la riesecuzione dei modelli di contabilità industriale. Se è necessario eliminare solo alcuni registri dei costi e rieseguire le allocazioni o è necessario eliminare tutto e rieseguire tutti i modelli dipende dai dati che sono stati aggiornati e da come sono impostate le capacità di contabilità dei costi. Identificare dove le correzioni dimensionali influiranno sulla contabilità dei costi e dove sono necessari aggiornamenti è un processo manuale. [!INCLUDE[prod_short](includes/prod_short.md)] attualmente non fornisce un modo automatizzato per farlo.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]