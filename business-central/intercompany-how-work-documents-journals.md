---
title: Contabilizzare documenti e registrazioni IC
description: Questo argomento spiega come utilizzare documenti o registrazioni intercompany per registrare le transazioni con i partner Intercompany.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals"></a>Utilizzo di documenti e registrazioni intercompany

Utilizzare documenti o registrazioni intercompany per registrare le transazioni con i partner Intercompany. È possibile registrare transazioni in conti C/G e, se sono stati impostati conti bancari interaziendali, è anche possibile registrare transazioni da banca a banca. Per ulteriori informazioni sulla configurazione di conti bancari interaziendali, vai a [Specificare i conti bancari da utilizzare per i partner intercompany](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Quando si registra un documento o una riga di registrazione intercompany nella società, viene creato un documento o una riga di registrazione corrispondente nella casella in uscita IC. Trasferisci la riga dalla casella in uscita al tuo partner. Il partner può quindi registrare le transazione corrispondente nella società, senza dover immettere di nuovo i dati.

Per i documenti di acquisto e di vendita, il codice partner IC per il cliente o il fornitore garantisce che tutte le fatture e gli ordini per le transazioni tra i partner producano i documenti corrispondenti nella società partner. I conti della società si bilanciano correttamente.

Lo stesso vale per le righe registrazioni COGE intercompany. Non è necessario specificare i conti, basta scegliere l'azienda partner. Le righe registrazioni COGE intercompany corrispondenti vengono quindi create nella società partner.

## <a name="fill-in-and-send-an-intercompany-sales-order"></a>Compilare e inviare un ordine di vendita intercompany

Gli ordini di vendita e acquisto, così come gli ordini di reso, possono essere inviati prima della registrazione. Le fatture e le note di credito non possono essere inviate finché non vengono registrate.

La procedura seguente illustra come compilare e inviare un ordine di vendita intercompany. Gli stessi passaggi si applicano agli ordini di acquisto e agli ordini di reso intercompany e alle fatture e alle note di credito intercompany registrate.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Per creare un nuovo ordine di vendita, selezionare **Nuovo**. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).  
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Assicurarsi che il cliente sia partner intercompany.
5. Per inviare l'ordine di vendita prima di registrarlo, scegliere l'azione **Invia ordine vendita IC**.

> [!NOTE]
> Se esegui il passaggio 5, l'ordine di vendita viene trasferito nella casella in uscita intercompany da cui puoi inviarlo in un secondo tempo. Per ulteriori informazioni sulla casella in entrata e in uscita intercompany, vai a [Gestire la casella in entrata e in uscita intercompany](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal"></a>Compilare e contabilizzare le registrazioni intercompany

Quando si registra una riga di registrazione COGE intercompany nella società, viene creata una riga di registrazione corrispondente nella casella in uscita IC che è possibile trasferire al partner. Con il primo ciclo di rilascio del 2022, è anche possibile impostare la società per creare automaticamente le transazioni intercompany ricevute dai partner, contabilizzate nelle registrazioni COGE intercompany. Il partner può quindi registrare le transazione corrispondente nella società, senza dover immettere di nuovo i dati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni COGE intercompany**, quindi scegli il collegamento correlato.  
2. Apri il batch registrazioni. Per ulteriori informazioni, vedi [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).
3. Compilare i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. Nel campo **Nr. conto C/G partner IC.** immettere il conto di contabilità generale IC in cui verrà registrato l'importo della società partner.

    > [!NOTE]
    > È necessario che il campo venga compilato in una riga con un conto corrente bancario o un conto C/G specificato nel campo **Nr. Conto** o nel campo **Nr. contropartita**.  
5. Scegli l'azione **Registra**.

I movimenti vengono registrati nella società e una registrazione con i movimenti corrispondenti viene creata nella casella in uscita IC in modo da poterli inviare alla società partner.

## <a name="see-also"></a>Vedere anche

[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
