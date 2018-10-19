---
title: Prelievo e spedizione nelle configurazioni della warehouse di base | Documenti Microsoft
description: "In Business Central, i processi in uscita per il prelievo e la spedizione possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6739a7fc1400e9c1cfbc276c0a9ebeb3f95467b2
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Procedura dettagliata: prelievo e spedizione nelle configurazioni della warehouse di base
In [!INCLUDE[d365fin](includes/d365fin_md.md)], i processi in uscita per il prelievo e la spedizione possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Prelievi|Spedizioni|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registra prelievo e spedizione dalla riga ordine|X|||2|  
|B|Registra prelievo e spedizione da un documento di prelievo magazzino||X||3|  
|C|Registra prelievo e spedizione da un documento di spedizione warehouse|||X|5/4/6|  
|D|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse||X|X|5/4/6|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md).  

Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  
Nelle configurazioni della warehouse di base in cui un'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, utilizzare la finestra **Prelievi magazzino** per registrare le informazioni riguardanti il prelievo e la spedizione per i documenti di origine in uscita. Il documento di origine in uscita può essere un ordine di vendita, un ordine di reso da acquisto, un ordine di trasferimento in uscita o un ordine di produzione i cui componenti sono necessari.  

In questa procedura dettagliata sono illustrati i task seguenti:  

-   Impostazione ubicazione ARGENTO per i prelievi magazzino.  
-   Creazione di un ordine di vendita per il cliente 10000 per 30 altoparlanti.  
-   Rilascio dell'ordine di vendita per la gestione warehouse.  
-   Creazione di un prelievo di magazzino in base al documento origine rilasciato.  
-   Registrazione della movimentazione warehouse dalla warehouse e registrazione contemporanea della spedizione vendita per l'ordine di vendita di origine.  

## <a name="roles"></a>Ruoli  
Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

-   Manager warehouse  
-   Gestore ordini  
-   Lavoro warehouse  

## <a name="prerequisites"></a>Prerequisiti  
Per completare questa procedura dettagliata, sarà necessario:  

-   CRONUS International Ltd. installato.  
-   Per diventare un impiegato warehouse presso l'ubicazione ARGENTO, effettuare i seguenti passaggi:  

    1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.  
    2.  Selezionare il campo **ID utente** , quindi il proprio account utente nella finestra **Utenti**.  
    3.  Nel campo **Codice ubicazione** immettere ARGENTO.  
    4.  Selezionare il campo **Default**.  

-   Rendere l'articolo LS-81 disponibile nell'ubicazione ARGENTO seguendo i passaggi di seguito riportati:  

    1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni magazzino** e quindi scegliere il collegamento correlato.  
    2.  Aprire il giornale di default e quindi creare due righe registrazioni magazzino con le informazioni seguenti sulla data di lavoro (23 gennaio).  

        |Tipo movimento|Numero di articolo|Cod. ubicazione|Codice collocazione|Quantità|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Rettifica positiva|LS-81|ARGENTO|S-01-0001 **Nota:**  la collocazione di default dell'articolo in CRONUS|20|  
        |Rettifica positiva|LS-81|ARGENTO|S-01-0002|20|  

    3.  Scegliere l'azione **Registra**, quindi selezionare il pulsante **Sì**.  

## <a name="story"></a>Scenario  
Ellen, responsabile warehouse presso CRONUS, imposta la warehouse ARGENTO per la gestione dei prelievi di base in cui gli addetti alla warehouse elaborano ordini in uscita singoli. Elisabetta, il gestore ordini, crea un ordine di vendita per 30 unità dell'articolo LS-81 da spedire al cliente 10000 dalla warehouse ARGENTO. Gianni, il lavoratore warehouse deve assicurarsi che la spedizione sia preparata e consegnata al cliente. Gianni gestisce tutte le attività interessate nella finestra **Prelievo magazzino** che automaticamente punta alle collocazioni in cui viene archiviato LS-81.  

## <a name="setting-up-the-location"></a>Impostazione dell'ubicazione  
L'impostazione della finestra **Scheda Ubicazione** definisce i flussi della warehouse della società.  

### <a name="to-set-up-the-location"></a>Per impostare l'ubicazione  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.  
2.  Aprire la scheda ubicazione ARGENTO.  
3.  Selezionare la casella di controllo **Richiesto prelievo**.  

## <a name="creating-the-sales-order"></a>Creazione dell'ordine di vendita  
Gli ordini di vendita sono il tipo più comune di documenti origine in uscita.  

### <a name="to-create-the-sales-order"></a>Per creare l'ordine di vendita  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di vendita** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Creare un ordine di vendita per il fornitore 10000 alla data di lavoro (23 gennaio) con la riga di ordine di vendita seguente.  

    |Articolo|Cod. ubicazione|Quantità|  
    |----------|-------------------|--------------|  
    |LS_81|ARGENTO|30|  

     Comunicare alla warehouse che l'ordine di vendita è pronto per la gestione warehouse.  

4.  Scegliere l'azione **Rilascia**.  

    Gianni procede al prelievo e alla spedizione degli articoli venduti.  

## <a name="picking-and-shipping-items"></a>Prelievo e spedizione articoli  
Nella finestra **Prelievo magazzino** è possibile gestire tutte le attività di warehouse in uscita per un documento origine specifico, ad esempio un ordine di vendita.  

### <a name="to-pick-and-ship-items"></a>Per prelevare gli articoli e procedere alla spedizione  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prelievi magazzino** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Selezionare il campo **Documento origine**, quindi selezionare **Ordine vendita**.  
4.  Selezionare il campo **Nr. origine**, selezionare la riga per la vendita al cliente 10000 e fare clic sul pulsante **OK**.  

    In alternativa, scegliere l'azione **Prendi documento origine**, quindi selezionare l'ordine di vendita.  
5.  Scegliere l'azione **Autocompil. qtà da gestire**.  

    In alternativa, nel campo **Qtà da gestire** immettere 10 e 30 rispettivamente nelle due righe di prelievo magazzino.  
6.  Scegliere l'azione **Registra**, selezionare **Spedizione**, quindi scegliere il pulsante **OK**.  

    I 30 altoparlanti ora sono registrati come prelevati dalle collocazioni S-01-0001 e S-01-0002 e viene creato un movimento contabile articolo negativo che riflette la spedizione di vendita registrata.  

## <a name="see-also"></a>Vedi anche  
 [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md)   
 [Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md)   
 [Spostare articoli ad hoc nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Dettagli di progettazione: Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md)   
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

