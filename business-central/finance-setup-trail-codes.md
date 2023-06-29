---
title: Impostazione codici per audit trail
description: Informazioni sulle attività per impostare i codici sorgente e le causali da utilizzare per tenere traccia degli audit trail.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Impostazione di codici sorgente e causali per audit trail

A tutti i movimenti registrati viene automaticamente assegnato un codice origine, in modo da poter risalire all'origine delle transazioni. Se si desidera assegnare ai movimenti un codice origine aggiuntivo, è possibile utilizzare le causali. Le causali indicano perché è stato creato un movimento. Quando si impostano le causali, è possibile assegnarle alle definizioni delle registrazioni e ai batch di registrazione, nonché a singoli documenti e righe di registrazione.  

Sia per i codici sorgente sia per le causali, utilizzare codici facili da ricordare e descrittivi. Il codice deve essere unico ed è possibile impostare un numero indefinito di codici.

## <a name="define-source-codes"></a><a name="define-source-codes"></a>Definire i codici origine

A volte può essere necessario conoscere la provenienza di un determinato movimento, ovvero sapere, ad esempio, se è riconducibile alla contabilizzazione di una registrazione COGE o di una fattura di acquisto. Il codice origine indica dove è stato creato un movimento. I movimenti vengono creati alla contabilizzazione di registrazioni e fatture e all'esecuzione di determinati processi batch. Ogni tipo di registrazione dispone di un codice origine specifico, che viene assegnato alla creazione dei movimenti.  

Quando si contabilizzano registrazioni, ordini, fatture, note credito o registrazioni e quando si eseguono alcuni processi batch, vengono generati dei movimenti nei rendiconti finanziari. La pagina **Setup codice origine** contiene varie Schede dettaglio, una per ogni area di applicazione. Ogni Scheda dettaglio contiene i codici origine applicabili a quell'area di applicazione.

Sia in fase di registrazione che di esecuzione di un processo batch, il codice origine corretto viene automaticamente allegato al movimento. Nel caso si contabilizzino delle registrazioni COGE, ad esempio, al movimento viene allegato il codice *GENJNL*. È quindi possibile filtrare la pagina **Movimenti C/G** pagina per mostrare quali movimenti sono stati pubblicati dalla registrazioni COGE o dai documenti di vendita.

### <a name="to-define-source-codes"></a><a name="to-define-source-codes"></a>Per definire i codici origine

1. Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Setup codice origine**, quindi scegli il collegamento correlato.  

2. Nella finestra **Setup codice origine**, per ogni tipo di registrazione e processo batch, specificare il codice sorgente pertinente.  

È possibile modificare il contenuto di un campo in un secondo momento e tale modifica avrà un impatto sulle registrazioni future.

## <a name="change-source-codes"></a><a name="change-source-codes"></a>Modificare i codici origine

Potrebbe essere necessario modificare un codice origine. Ad esempio, può essere necessario modificare il codice origine *GENJNL* in *GNJ*.

### <a name="to-change-source-codes"></a><a name="to-change-source-codes"></a>Per modificare i codici origine

1. Scegli l'icona ![Cerca pagina o report.](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Codici origine**, quindi scegli il collegamento correlato.

2. Nella riga che contiene il codice da modificare selezionare il codice nel campo **Codice**.

3. Immettere il nuovo codice, quindi fare clic sul pulsante **Sì**. È possibile modificare anche il contenuto del campo **Descrizione**.

Tutti i nuovi movimenti contabilizzati dalle registrazioni COGE disporranno di nuovo codice origine.

## <a name="define-reason-codes"></a><a name="define-reason-codes"></a>Definire le causali

Le causali integrano i codici sorgente e vengono utilizzati per indicare il motivo per cui è stata creato un movimento. È possibile assegnare causali a movimenti singoli e assegnare codici permanenti a definizioni e batch di registrazioni specifici. Una volta collegate le causali a una riga di registrazioni oppure a una testata delle vendite o degli acquisti, tutti i movimenti verranno contrassegnati automaticamente da una causale al momento della registrazione.  

### <a name="to-set-up-reason-codes"></a><a name="to-set-up-reason-codes"></a>Per impostare le causali

1. Scegli l'icona ![Cerca pagina o report.](media/ui-search/search_small.png "Icona Cerca pagina o report")  immetti **Causali**, quindi scegli il collegamento correlato.

2. Nella finestra **Causali** immettere il primo codice nel campo **Codice**. Nel campo **Descrizione** immettere un testo esplicativo.

Ripetere la procedura per ogni codice che si intende utilizzare. È possibile impostare quanti codici si ritengono necessari.

La seguente procedura descrive come aggiungere una causale a una definizione di registrazioni, ma passaggi simili si applicano all'aggiunta di una causale a una riga di registrazione o a un batch di registrazioni.  

### <a name="to-assign-reason-codes-to-journal-templates"></a><a name="to-assign-reason-codes-to-journal-templates"></a>Per assegnare causali alle definizioni di registrazioni

1. Scegli l'icona ![Cerca pagina o report.](media/ui-search/search_small.png "Icona Cerca pagina o report")  immetti **Definizioni registrazioni COGE**, quindi scegli il collegamento correlato.

2. Sulla riga della definizione di registrazioni selezionata immettere il codice pertinente nel campo **Causale**.

3. Chiudere la definizione di registrazioni.

La causale selezionata verrà copiata nei nuovi batch di registrazioni creati in questa definizione di registrazioni. È possibile assegnare causali a definizioni di registrazioni in altre aree di applicazione utilizzando la stessa procedura.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Per utilizzare le causali sui documenti di acquisto e vendita

1. Aprire il documento di acquisto o vendita appropriato.

2. Nella testata degli acquisti o delle vendite immettere la causale nel campo **Causale**.

Quando la fattura viene registrata, la causale viene copiata in ogni movimento C/G, cliente e fornitore. Non è possibile assegnare causali diverse a singole righe di acquisto e vendita, perché tutte le righe vengono registrate come un unico movimento.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Vedi anche

[Finanze](finance.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzare le dimensioni](finance-dimensions.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Analizzare il flusso di cassa dell'azienda](finance-analyze-cash-flow.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
