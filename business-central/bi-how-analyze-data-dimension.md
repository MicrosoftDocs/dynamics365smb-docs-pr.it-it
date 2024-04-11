---
title: Analizzare i dati per dimensioni
description: Questo articolo descrive come analizzare i dati aziendali in base alle dimensioni per ottenere maggiori informazioni dettagliate sulla tua attività.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analizzare i dati per dimensioni

Nelle analisi finanziarie, una dimensione corrisponde ai dati che aggiungi a un movimento come una specie di contrassegno per raggruppare movimenti con caratteristiche simili. Ad esempio, le dimensioni spesso raggruppano movimenti per clienti, aree geografiche, prodotti e venditori. I gruppi ti consentono di recuperare facilmente i dati su di essi per l'analisi. Puoi usare le dimensioni per i movimenti in registrazioni, documenti e budget.

Ogni dimensione descrive lo stato attivo dell'analisi. Quindi, un'analisi bidimensionale, ad esempio, corrisponde a vendite per area. Utilizzando più di due dimensioni quando crei un movimento, puoi eseguire un'analisi più complessa. Un esempio di analisi complessa è l'esplorazione delle vendite per campagna di vendita, per gruppo di clienti e per area. Ciò ti offre una visione più approfondita della tua attività, ad esempio quanto bene sta operando, dove sta prosperando e dove non lo sta facendo e dove dovresti allocare più risorse. Queste informazioni ti consentono di prendere decisioni più informate. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

> [!TIP]
> Un modo rapido per analizzare i dati transazionali in base alle dimensioni consiste nel filtrare i totali nel piano dei conti e le voci in tutte le pagine **Voci** in base alle dimensioni. Cerca l'azione **Imposta filtro dimensione**.

> [!NOTE]
> Se scopri che è stata utilizzata una dimensione errata nei movimenti di contabilità generale registrati, puoi correggerla e aggiornare le visualizzazioni analisi. Per ulteriori informazioni, vedi [Risoluzione dei problemi e correzione delle dimensioni](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Impostare una visualizzazione analisi

Un'analisi basata sulle dimensioni utilizza una combinazione selezionata di dimensioni. È possibile archiviare, recuperare e aggiornare il set di dimensioni creando una scheda **Visualizzazione analisi**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Visualizzazioni analisi**, quindi scegli il collegamento correlato.  
2. Nella pagina **Lista visualizzazione analisi** scegliere l'azione **Nuovo**.
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Per aggiungere altri codici di dimensione ai quattro disponibili nella Scheda dettaglio **Dimensioni**, scegli l'azione **Filtro**, compila i campi e scegli il pulsante **OK**.  
5. Per aggiornare la visualizzazione, scegliere l'azione **Aggiorna**.

## Analizzare per dimensioni

Utilizza le visualizzazioni analisi precedentemente impostate con la matrice **Analisi per dimensioni** per visualizzare gli importi della contabilità generale.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Visualizzazioni analisi**, quindi scegli il collegamento correlato.  
2. Seleziona la visualizzazione di analisi desiderata e scegli l'azione **Analisi per dimensioni**.
3. All'inizio della pagina **Analisi vendite per dimensioni**, compila i campi per definire quali dati visualizzare e come.
4. Scegli l'azione **Mostra matrice** per aprire la pagina della matrice per la visualizzazione analisi.
5. Per accedere ai dettagli di un importo nella pagina matrice, scegli l'importo.  

- Nelle colonne a sinistra sono contenute informazioni sulla base di ciò che hai selezionato nel campo **Mostra come righe** della testata.  
- Le colonne a destra contengono informazioni sulla base di ciò che hai selezionato nel campo **Mostra come colonne** della testata.

> [!IMPORTANT]  
> Non puoi selezionare una durata periodo più breve rispetto al periodo specificato per la compressione della data nella scheda **Visualizzazione analisi**. Le azioni **Set successivo** e **Set precedente** non sono disponibili se nel campo **Mostra come righe** oppure **Mostra come colonne** hai selezionato il valore **Periodo**.  

> [!NOTE]  
> È possibile utilizzare il report **Dimensioni - Dettagli** per visualizzare una dettagliata classificazione di come le dimensioni siano state utilizzate nei movimenti contabili durante un periodo selezionato. È possibile utilizzare il report **Dimensioni - Totali** per visualizzare solo gli importi totali.  

> [!TIP]  
> È inoltre possibile modificare la visualizzazione cambiando il contenuto dei campi **Mostra come righe** e **Mostra come colonne**. Per ripristinare un'impostazione di visualizzazione, scegliere l'azione **Inverti righe e colonne**.

## Aggiornare una visualizzazione analisi

Gli importi nella pagina **Analisi per dimensioni** forniscono un'immagine dello stato della società al momento dell'ultimo aggiornamento. Per ottenere lo stato corrente, esegui l'azione di aggiornamento per aggiornare la visualizzazione analisi.

Usa la seguente procedura per aggiornare una visualizzazione analisi dalla pagina **Analisi per Dimensioni**. I passaggi sono simili a quelli per l'aggiornamento delle pagine **Scheda visualizzazione analisi** e **Lista visualizzazione analisi**.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Visualizzazioni analisi**, quindi scegli il collegamento correlato.
2. Seleziona la visualizzazione di analisi desiderata e scegli l'azione **Analisi per dimensioni**.
3. Nella finestra **Analisi per dimensioni**, selezionare il campo **Codice visual. analisi**.  
4. Selezionare la riga con la visualizzazione analisi desiderata.  
5. Nella pagina **Visualizzazioni analisi**, seleziona la visualizzazione analisi e scegli l'azione **Aggiorna**.  

> [!TIP]  
> Se selezioni la casella di controllo **Aggiorna in registrazione** in una scheda di visualizzazione analisi, la visualizzazione viene aggiornata automaticamente alla registrazione di una transazione associata.

> [!NOTE]  
> Per aggiornare contemporaneamente alcune o tutte le visualizzazioni analisi, utilizza il processo batch **Aggiorna visualizzazione analisi**.  

## Vedere anche

[Business Intelligence finanziario](bi.md)  
[Dati finanziari](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare le dimensioni](finance-dimensions.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
