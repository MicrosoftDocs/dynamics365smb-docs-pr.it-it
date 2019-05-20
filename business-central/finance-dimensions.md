---
title: Utilizzare le dimensioni| Documenti Microsoft
description: Utilizzare le dimensioni per classificare i movimenti, ad esempio, per reparto o progetto, in modo da tenere traccia e analizzare facilmente i dati.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9072bd45d5189ec42e8f1adaa3554fa182c36f1f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244724"
---
# <a name="working-with-dimensions"></a>Utilizzo delle dimensioni
Per rendere più semplice eseguire analisi sui documenti, quali ordini di vendita, è possibile utilizzare le dimensioni. Le dimensioni sono attributi e valori che categorizzano i movimenti in modo da poterli seguire e analizzare. Ad esempio, le dimensioni possono indicare il progetto o il reparto da cui un movimento proviene.  

For example, anziché impostare conti di contabilità generale distinti per ogni reparto e progetto, è possibile utilizzare le dimensioni. Ciò dà un'opportunità ricca per l'analisi, senza creare un piano dei conti complesso. Per ulteriori informazioni, vedere [Business Intelligence](bi.md).

Un altro esempio consiste nell'impostare una dimensione denominata *Reparto* e nell'utilizzare tale dimensione al momento della registrazione dei documenti di vendita. In questo modo sarà possibile utilizzare strumenti di business intelligence per vedere quale reparto ha venduto quali articoli.
Più dimensioni si utilizzano, più dettagliati sono i report su cui è possibile basare le decisioni aziendali. Ad esempio, un singolo movimento di vendita può includere le informazioni di più dimensioni, quali:  

* Il conto in cui è stata registrata la vendita dell'articolo  
* Dove l'articolo è stato venduto
* Chi lo ha venduto
* Il tipo di cliente che lo ha acquistato  

## <a name="analyzing-by-dimensions"></a>Analisi per dimensioni
La funzionalità Dimensioni svolge un ruolo importante in business intelligence, ad esempio quando si definiscono le visualizzazioni analisi. Per ulteriori informazioni, vedere [Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md).

> [!TIP]
> Un modo rapido per analizzare i dati transazionali in base alle dimensioni consiste nel filtrare i totali nel piano dei conti e le voci in tutte le pagine **Voci** in base alle dimensioni. Cercare l'azione **Imposta filtro dimensione**.

## <a name="dimension-sets"></a>Set di dimensioni
Un set di dimensioni è una combinazione univoca di valori dimensioni. Viene archiviato come movimenti set di dimensioni nel database. Ogni movimento set di dimensioni rappresenta un valore dimensioni singolo. Il set di dimensioni è identificato da un ID set di dimensioni comune assegnato a ogni movimento set di dimensioni che appartiene al set di dimensioni.  

Quando si crea una riga di registrazione, una testata del documento o una riga documento, è possibile specificare una combinazione di valori dimensioni. Anziché archiviare esplicitamente ogni valore dimensioni nel database, viene assegnato un ID set di dimensioni alla riga di registrazione, alla testata del documento o alla riga del documento per specificare il set di dimensioni.  

## <a name="setting-up-dimensions"></a>Setup delle dimensioni
È possibile definire le dimensioni e i valori di dimensione da utilizzare per classificare le registrazioni e i documenti, ad esempio ordini di vendita e di acquisto. Impostare le dimensioni nella pagina **Dimensioni** in cui si crea una riga per ogni dimensione, ad esempio *Progetto*, *Reparto*, *Area* e *Agente*.

Vengono inoltre impostati i valori delle dimensioni. Ad esempio, i valori potrebbero essere i reparti della società. I valori di dimensione possono essere impostati in una struttura gerarchica simile al piano dei conti, in modo che i dati possano essere suddivisi in vari livelli di granularità e i sottoinsiemi dei valori di dimensione sommati. In base alle necessità, è possibile impostare un numero illimitato di dimensioni e di valori dimensioni che possono essere utilizzati da tutti gli utenti nella società.

Quando dimensioni e valori sono impostati, è possibile definire dimensioni globali e a collegamento rapido nella pagina **Setup contabilità generale** che saranno sempre disponibili per essere selezionati come campi nelle righe di documenti e registrazioni, senza dover aprire prima la pagina **Dimensioni**. Per ulteriori informazioni, vedere [Per impostare dimensioni globali e a collegamento rapido](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Dimensioni globali** utilizzate come filtro, ad esempio, per report e processi batch. È possibile utilizzare solo due dimensioni globali, scegliere pertanto le dimensioni che verranno utilizzate più spesso.
* Le **dimensioni a collegamento rapido** sono disponibili come campi nelle righe di registrazioni e documenti. È possibile creare fino a sei dimensioni a collegamento rapido.  

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
>  Se a un conto deve essere assegnata una dimensione diversa da quella di default già impostata per quel determinato tipo di conto, è necessario impostare una dimensione di default per il conto in questione. La dimensione predefinita per il singolo conto sostituirà la dimensione predefinita per quel tipo di conto.  

### <a name="to-set-up-default-dimension-priorities"></a>Per impostare priorità nelle dimensioni di default  
Per tipi di conto diversi, come un conto cliente e un conto articoli, possono essere impostate dimensioni di default diverse. Un movimento potrà quindi avere più di una proposta di dimensione di default per un'unica dimensione. Per evitare conflitti è possibile applicare delle regole di priorità alle diverse fonti.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Priorità dimensioni di default** e quindi scegliere il collegamento correlato.  
2.  Nel campo **Codice origine** della pagina **Priorità dimensioni di default** immettere il codice origine per la tabella movimenti a cui si desidera applicare le priorità dimensioni di default.  
3.  Compilare i campi per ogni priorità della dimensione di default desiderata per il codice di origine selezionato.
4.  Ripetere la procedura per ogni codice di origine per il quale si desidera impostare le priorità della dimensione di default.  

> [!IMPORTANT]  
>  Se vengono impostate due tabelle con la stessa priorità per lo stesso codice origine, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verrà sempre selezionata la tabella con l'ID minore.  

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
>  Su righe e colonne vengono visualizzate le stesse dimensioni e pertanto tutte le combinazioni sono presenti due volte. In [!INCLUDE[d365fin](includes/d365fin_md.md)]l'impostazione scelta viene automaticamente visualizzata in entrambi i campi. Non è possibile immettere alcuna selezione nei campi lungo la diagonale che ha origine nell'angolo in alto a sinistra perché questi campi hanno la stessa dimensione sia sulla riga che sulla colonna.  
>   
>  L'opzione selezionata viene visualizzata dopo l'uscita dal campo.  
>   
>  Per visualizzare il nome delle dimensioni anziché il codice, selezionare il campo **Mostra nome colonna**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Per impostare dimensioni globali e a collegamento rapido
Le dimensioni globali e a collegamento rapido possono essere utilizzate come filtro ovunque in [!INCLUDE[d365fin](includes/d365fin_md.md)], tra cui report, processi batch e visualizzazioni analisi. Le dimensioni globali e a collegamento rapido sono sempre disponibili per essere inserite direttamente senza prima aprire la pagina **Dimensioni**. Nelle righe di registrazioni e documenti, è possibile selezionare dimensioni globali e a collegamento rapido in un campo della riga. È possibile impostare due dimensioni globali e otto dimensioni a collegamento rapido. Scegliere le dimensioni che si utilizzano maggiormente.

> [!Important]  
> La modifica di una dimensione globale o a collegamento rapido richiede l'aggiornamento di tutti i movimenti registrati con la dimensione. È possibile eseguire questa task con la funzione **Cambia dimensioni globali**, ma può richiedere molto tempo e influire sulle prestazioni. Di conseguenza, scegliere con attenzione le dimensioni globali e a collegamento rapido in modo da non dover modificarle in seguito.

> [!Note]
> Quando si aggiunge o si modifica una dimensione globale o a collegamento rapido, viene eseguita automaticamente la disconnessione e una nuova connessione di modo che il nuovo valore possa essere utilizzato in tutta l'applicazione.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.
2. Nella Scheda dettaglio **Dimensioni**, riempire i campi. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Per cambiare le dimensioni globali
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cambia dimensioni globali** e quindi scegliere il collegamento correlato.
2. Passare sulle azioni e sui campi nella pagina con il mouse per informazioni su come cambiare le dimensioni globali e a collegamento rapido.

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
>   Per impostare una gerarchia, i codici devono essere in ordine alfabetico. Inclusi quelli dei valori dimensioni che forniti in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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

In una pagina di movimenti contabili è possibile vedere se sono state impostate le dimensioni globali per i movimenti. Le due dimensioni globali si differenziano da tutte le altre dimensioni in quanto è possibile utilizzarle come filtro in qualsiasi punto di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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
|Valore di dimensione eliminato|   %1 per %2 mancante.|- Ripristinare il valore di dimensione mancante.<br />- Trovare documenti non registrati che contengono il set di dimensioni con il valore di dimensione mancante e aggiungerlo.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione mancante.|
|Valore di dimensione non consentito|Il tipo di valore di dimensione per %1 %2 - %3 non deve essere %4.|- Impostare il campo **Tipo valori dimensioni** nella pagina **Valori dimensioni** su **Standard** o **Inizio-Totale**.<br />- Rimuovere la riga del set di dimensioni per il valore di dimensione bloccato.|
|Combinazione di dimensioni bloccata|Le dimensioni %1 e %2 non possono essere utilizzate contemporaneamente.|- Trovare documenti non registrati che contengono il set di dimensioni con la combinazione di dimensioni bloccata e sbloccarla.<br />- Modificare una delle righe del set di autorizzazioni in conflitto per la combinazione di dimensioni.|
|Combinazione di valori di dimensioni bloccata|Le combinazioni di dimensioni %1 - %2 e %3 - %4 non possono essere usare contemporaneamente.|- Trovare documenti non registrati che contengono il set di dimensioni con la combinazione di valori di dimensioni bloccata e sbloccarla.<br />- Modificare una delle righe del set di autorizzazioni in conflitto per la combinazione di valori di dimensioni.|
|Codice del valore di dimensione vuoto per la dimensione di default in cui il campo **Registrazione valore** contiene **Codice obbligatorio**|- Selezionare un %1 per %2 %3.<br />- Selezionare un %1 per i %2 %3 per %4 %5.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere un valore di dimensione non vuoto per la dimensione in conflitto nel set di dimensioni.|
|Codice del valore di dimensione errato per la dimensione di default in cui il campo **Registrazione valore** contiene **Stesso Cod.**|- Selezionare %1 %2 per i %3 %4.<br />- Selezionare %1 %2 per i %3 %4 per %5 %6.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere il valore di dimensione richiesto per la dimensione in conflitto nel set di dimensioni.|
|Codice del valore di dimensione non vuoto per la dimensione di default vuota in cui il campo **Registrazione valore** contiene **Stesso Cod.**|- %1 %2 deve essere vuoto.<br />- %1 %2 deve essere vuoto per %3 %4.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Immettere un codice del valore di dimensione vuoto per la dimensione in conflitto nel set di dimensioni.|
|Valore di dimensione non previsto per la dimensione di default in cui il campo **Registrazione valore** contiene **Nessun Cod.**|- %1 %2 non deve essere nominato.<br />- %1 %2 non deve essere nominato per %3 %4.|- Modificare il campo **Registrazione valore** nella pagina **Dimensione di default**.<br />- Rimuovere la riga in conflitto dal set di dimensioni.|

## <a name="see-also"></a>Vedere anche
[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Analizzare i dati per dimensioni](bi-how-analyze-data-dimension.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
