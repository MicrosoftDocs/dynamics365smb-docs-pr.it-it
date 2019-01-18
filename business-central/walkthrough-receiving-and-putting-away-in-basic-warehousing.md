---
title: 'Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base | Documenti Microsoft'
description: "In Business Central, i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 0ba61572a237e177b763b7b8a2e13ca7ec93eea4
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base
In [!INCLUDE[d365fin](includes/d365fin_md.md)], i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Carichi|Stoccaggi|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|X|||2|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino|||X|3|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse||X||5/4/6|  
|D|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse||X|X|5/4/6|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).  

Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  
Nelle configurazioni di warehouse di base in cui un'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi ma non l'elaborazione dei carichi, utilizzare la pagina **Stoccaggio in magazzino** per registrare le informazioni riguardanti lo stoccaggio e il carico per i documenti di origine in entrata. Il documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata o un ordine di produzione il cui output è pronto per lo stoccaggio.

> [!NOTE]
> Anche se le impostazioni sono definite **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile registrare carichi e spedizioni direttamente dai documenti commerciali di origine nelle ubicazioni in cui si selezionano queste caselle di controllo.  

In questa procedura dettagliata sono illustrati i task seguenti.  

-   Impostazione ubicazione ARGENTO per gli stoccaggi magazzino.  
-   Impostazione ubicazione ARGENTO per la gestione della collocazione.  
-   Definizione di una collocazione di default per l'articolo LS-81. (LS-75 è già impostato in CRONUS).  
-   Creazione di un ordine di acquisto per il fornitore 10000 per 40 altoparlanti.  
-   Verificare che le collocazioni di stoccaggio siano preimpostate in base all'impostazione.  
-   Rilascio dell'ordine di acquisto per la gestione warehouse.  
-   Creazione di uno stoccaggio in magazzino in base al documento origine rilasciato.  
-   Verificare che le collocazioni di stoccaggio siano ereditate dell'ordine di acquisto.  
-   Registrazione della movimentazione warehouse nella warehouse e registrazione contemporanea della ricezione acquisti per l'ordine di acquisto di origine.  

## <a name="roles"></a>Ruoli  
Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

-   Manager warehouse  
-   Rivenditore  
-   Lavoro warehouse  

## <a name="prerequisites"></a>Prerequisiti  
Per completare questa procedura dettagliata, sarà necessario:  

-   CRONUS International Ltd. installato.  
-   Per diventare un impiegato warehouse presso l'ubicazione ARGENTO, effettuare i seguenti passaggi:  

    1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.  
    2.  Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.  
    3.  Nel campo **Codice ubicazione** immettere ARGENTO.  
    4.  Selezionare il campo **Default**.  

## <a name="story"></a>Scenario  
Ellen, responsabile warehouse presso CRONUS International Ltd., crea un ordine di acquisto per 10 unità dell'articolo LS-75 e 30 unità dell'articolo LS-81 per il fornitore 10000 che deve essere consegnato alla warehouse ARGENTO. Quando la consegna arriva alla warehouse, Gianni, il lavoratore warehouse, esegue lo stoccaggio degli articoli nelle collocazioni di default per gli articoli. Quando Gianni registra lo stoccaggio, gli articoli vengono registrati come ricevuti nel magazzino e disponibili alla vendita o a un'altra domanda.  

## <a name="setting-up-the-location"></a>Impostazione dell'ubicazione  
 L'impostazione della pagina **Scheda Ubicazione** definisce i flussi della warehouse della società.  

### <a name="to-set-up-the-location"></a>Per impostare l'ubicazione  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.  
2.  Aprire la scheda ubicazione ARGENTO.  
3.  Selezionare la casella di controllo **Richiesto stoccaggio**.  

    Impostare una collocazione di default per i due numeri articolo per controllare dove vengono stoccati.  

4.  Scegliere l'azione **Collocazioni**.  
5.  Selezionare la prima riga, per la collocazione S-01-0001, quindi scegliere l'azione **Contenuti**.  

    Notare che nella pagina **Contenuto collocazione** l'articolo LS-75 è già impostato come contenuto nella collocazione S-01-0001.  

6.  Scegliere l'azione **Nuovo**.  
7.  Selezionare i campi **Fisso** e **Default**.  
8.  Nel campo **Nr. articolo** immettere LS-81.  

## <a name="creating-the-purchase-order"></a>Creazione dell'ordine di acquisto  
Gli ordini di acquisto sono il tipo più comune di documenti origine in entrata.  

### <a name="to-create-the-purchase-order"></a>Per creare l'ordine di acquisto.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e selezionare il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Creare un ordine di acquisto per il fornitore 10000 alla data di lavoro (23 gennaio) con le righe di ordine di acquisto seguenti.  

    |Articolo|Cod. ubicazione|Codice collocazione|Quantità|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|ARGENTO|S-01-0001|10|  
    |LS-81|ARGENTO|S-01-0001|30|  

    > [!NOTE]  
    >  Il codice di collocazione viene immesso automaticamente in base al setup eseguito nella sezione "Impostazione dell'ubicazione".  

    Comunicare alla warehouse che l'ordine di acquisto è pronto per la gestione warehouse al momento della consegna.  

4.  Scegliere l'azione **Rilascia**.  

    La consegna degli altoparlanti dal fornitore 10000 è arrivata alla warehouse ARGENTO e Gianni continua lo stoccaggio.  

## <a name="receiving-and-putting-the-items-away"></a>Ricezione e stoccaggio di articoli  
Nella pagina **Stoccaggio in magazzino** è possibile gestire tutte le attività di warehouse in entrata per un documento origine specifico, ad esempio un ordine di acquisto.  

### <a name="to-receive-and-put-the-items-away"></a>Per ricevere e stoccare gli articoli  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stoccaggi magazzino** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Selezionare il campo **Documento origine**, quindi selezionare **Ordine acquisto**.  
4.  Selezionare il campo **Nr. origine**, selezionare la riga per gli acquisti dal fornitore 10000 e fare clic sul pulsante **OK**.  

    In alternativa, nel gruppo **Funzioni** del gruppo **Azioni** selezionare **Prendi documento origine**, quindi selezionare l'ordine di acquisto.  

5.  Scegliere l'azione **Autocompil. qtà da gestire**.  

    In alternativa, nel campo **Qtà da gestire** immettere 10 e 30 rispettivamente nelle due righe di stoccaggio magazzino.  

6.  Scegliere l'azione **Registra**, selezionare l'azione **Ricevi**, quindi il pulsante **OK**.  

    I 40 altoparlanti ora sono registrati come stoccati nella collocazione S-01-0001 e viene creato un movimento contabile articolo positivo che riflette la ricezione acquisti registrata.  

## <a name="see-also"></a>Vedi anche  
 [Eseguire lo stoccaggio con Stoccaggi Magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md)   
 [Spostare articoli ad hoc nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md)   
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

