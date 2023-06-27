---
title: Analizzare i dati per dimensioni
description: Questo articolo descrive come analizzare i dati aziendali in base alle dimensioni per ottenere maggiori informazioni dettagliate sulla tua attività.
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="analyze-data-by-dimensions" />Analizzare i dati per dimensioni

Nelle analisi finanziarie, una dimensione corrisponde ai dati che aggiungi a un movimento come una specie di contrassegno. Tali dati vengono utilizzati per raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Le dimensioni possono essere utilizzate per i movimenti nelle registrazioni, nei documenti e nei. 

Ogni "dimensione" descrive lo stato attivo dell'analisi. Quindi, un'analisi bidimensionale, ad esempio, corrisponde a vendite per area. Creando più di due dimensioni quando si crea un movimento, è possibile eseguire analisi molto più complesse, ad esempio vendite per campagna di vendita per gruppo di clienti per area. Ciò ti offre una visione più approfondita della tua attività, ad esempio quanto bene sta operando, dove sta prosperando e dove non lo sta facendo e dove dovrebbero essere allocate più risorse, in modo da poter prendere decisioni più informate mentre vai avanti. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

> [!TIP]
> Un modo rapido per analizzare i dati transazionali in base alle dimensioni consiste nel filtrare i totali nel piano dei conti e le voci in tutte le pagine **Voci** in base alle dimensioni. Cerca l'azione **Imposta filtro dimensione**.

> [!NOTE]
> Se scopri che è stata utilizzata una dimensione errata nei movimenti di contabilità generale registrati, puoi correggerli e aggiornare le visualizzazioni di analisi. Per ulteriori informazioni, vedi la sezione [Risoluzione dei problemi e correzione delle dimensioni](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view" />Impostare una visualizzazione analisi

Un'analisi basata sulle dimensioni utilizza una combinazione selezionata di dimensioni. È possibile archiviare, recuperare e aggiornare il set di dimensioni creando una scheda **Visualizzazione analisi**. 

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Visualizzazioni analisi**, quindi scegli il collegamento correlato.  
2. Nella pagina **Lista visualizzazione analisi** scegliere l'azione **Nuovo**.
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Per aggiungere altri codici di dimensione ai quattro disponibili nella Scheda dettaglio **Dimensioni**, scegli l'azione **Filtro**, compila i campi e scegli il pulsante **OK**.  
5. Per aggiornare la visualizzazione, scegliere l'azione **Aggiorna**.

## <a name="analyze-by-dimensions" />Analizzare per dimensioni

Utilizza le visualizzazioni analisi precedentemente impostate con la matrice **Analisi per dimensioni** per visualizzare gli importi della contabilità generale.   

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Visualizzazioni analisi**, quindi scegli il collegamento correlato.  
2. Seleziona la visualizzazione di analisi desiderata e scegli l'azione **Analisi per dimensioni**.
3. All'inizio della pagina **Analisi vendite per dimensioni**, compilare i campi per definire quali dati sono visualizzati e come.
4. Scegliere l'azione **Mostra matrice** per aprire la pagina della matrice rispettiva per la visualizzazione analisi definita.
5. Per visualizzare la specifica di un importo nella pagina della matrice, selezionare l'importo di cui eseguire il drill-down.  

- Nelle colonne a sinistra sono contenute informazioni sulla base di ciò che è stato selezionato nel campo **Mostra come righe** della testata.  
- Le colonne a destra contengono informazioni sulla base di ciò che è stato selezionato nel campo **Mostra come colonne** della testata.

> [!IMPORTANT]  
> Non è possibile selezionare una durata periodo più breve rispetto a quello specificato per la compressione data nella scheda **Visualizzazione analisi**. I comandi **Periodo successivo** e **Periodo precedente** non sono attivi se nel campo **Mostra come righe** oppure **Mostra come colonne** è stato selezionato il valore **Periodo**.  

> [!NOTE]  
> È possibile utilizzare il report **Dimensioni - Dettagli** per visualizzare una classificazione dettagliata di come sono state utilizzate le dimensioni per i movimenti di un determinato periodo selezionato. È possibile utilizzare il report **Dimensioni - Totali** per visualizzare solo gli importi totali.  

> [!TIP]  
> È inoltre possibile modificare la visualizzazione cambiando il contenuto dei campi **Mostra come righe** e **Mostra come colonne**. Per ripristinare un'impostazione di visualizzazione, scegliere l'azione **Inverti righe e colonne**.

## <a name="update-an-analysis-view" />Aggiornare una visualizzazione analisi

Gli importi visualizzati nella pagina **Analisi per dimensioni** forniscono un'immagine dello stato della società al momento dell'ultimo aggiornamento. Per avere un'immagine dello stato corrente, è necessario eseguire la funzione di aggiornamento per aggiornare la visualizzazione dell'analisi.

Usa la seguente procedura per aggiornare una visualizzazione analisi dalla pagina **Analisi per Dimensioni**. I passaggi sono simili a quelli per l'aggiornamento delle pagine **Scheda visualizzazione analisi** e **Lista visualizzazione analisi**.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Visualizzazioni analisi**, quindi scegli il collegamento correlato.
2. Seleziona la visualizzazione di analisi desiderata e scegli l'azione **Analisi per dimensioni**.
3. Nella finestra **Analisi per dimensioni**, selezionare il campo **Codice visual. analisi**.  
4. Selezionare la riga con la visualizzazione analisi desiderata.  
5. Nella pagina **Visualizzazioni analisi**, seleziona la visualizzazione analisi e scegli l'azione **Aggiorna**.  

> [!TIP]  
> Se selezioni la casella di controllo **Aggiorna in registrazione** in una scheda di visualizzazione analisi, la visualizzazione viene aggiornata automaticamente alla registrazione di una transazione associata.

> [!NOTE]  
> Per aggiornare contemporaneamente alcune o tutte le visualizzazioni analisi, è necessario utilizzare il processo batch **Aggiorna visualizzazione analisi**.  

## <a name="see-related-training-at-microsoft-learn" />Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index).

## <a name="see-also" />Vedere anche

[Business Intelligence finanziario](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare le dimensioni](finance-dimensions.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
