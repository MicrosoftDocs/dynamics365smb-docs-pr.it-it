---
title: Contabilizzare documenti e registrazioni IC | Documenti Microsoft
description: Utilizzare documenti Intercompany per registrare le transazioni con i partner Intercompany.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2f56dd9746ab065628f5785715153b82fa02a155
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-intercompany-documents-and-journals"></a>Utilizzo di documenti e registrazioni intercompany
Utilizzare documenti o registrazioni intercompany per registrare le transazioni con i partner Intercompany. Quando si registra un documento o una riga di registrazione intercompany nella società, viene creato un documento o una riga di registrazione corrispondente nella casella in uscita IC che è possibile trasferire al partner. Il partner può quindi registrare le transazione corrispondente nella società, senza dover immettere di nuovo i dati.

Per i documenti di acquisto e di vendita, il codice partner IC per il cliente o il fornitore interessato garantisce che tutte le fatture e gli ordini generati per le transazioni con tali società producano i documenti corrispondenti nella società partner, consentendo un corretto bilancio dei conti.

Per le righe di registrazione COGE intercompany non è necessario specificare i conti per un singolo gruppo di registri, ma è sufficiente indicare l'identificativo della società partner. Le righe di registrazione COGE intercompany corrispondenti vengono nella società partner e comportano il bilancio dei registri di entrambe le società coinvolte in una transazione.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Per compilare e inviare un ordine di vendita intercompany
Gli ordini di vendita e acquisto, così come gli ordini di reso, possono essere inviati prima della registrazione. Le fatture e le note di credito non possono essere inviate finché non vengono registrate.

La procedura seguente illustra come compilare e inviare un ordine di vendita intercompany. Gli stessi passaggi si applicano agli ordini di acquisto e agli ordini di reso intercompany e alle fatture e alle note di credito intercompany registrate.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di vendita**, quindi scegliere il collegamento correlato.  
2. Per creare un nuovo ordine di vendita, selezionare **Nuovo**. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).  
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Assicurarsi che il cliente sia partner intercompany.
5. Per inviare l'ordine di vendita prima di registrarlo, scegliere l'azione **Invia ordine vendita IC**.

> [!NOTE]
> Se si esegue il passaggio 4, l'ordine di vendita verrà trasferito nella casella in uscita intercompany da cui è possibile inviarlo in un secondo tempo. Per ulteriori informazioni, vedere [Gestire la casella in entrata e in uscita intercompany](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Per compilare e annotare registrazioni intercompany
Quando si registra una riga di registrazione COGE intercompany nella società, viene creata una riga di registrazione corrispondente nella casella in uscita IC che è possibile trasferire al partner. Il partner può quindi registrare le transazione corrispondente nella società, senza dover immettere di nuovo i dati.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE IC**, quindi scegliere il collegamento correlato.  
2. Aprire il batch registrazioni appropriato. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).
3. Compilare i campi, se necessario.
4. Nel campo **Nr. conto C/G partner IC.** immettere il conto di contabilità generale IC in cui verrà registrato l'importo della società partner.

    > [!NOTE]
    > È necessario che il campo venga compilato in una riga con un conto corrente bancario o un conto C/G specificato nel campo **Nr. Conto** o nel campo **Nr. contropartita**.  
5. Scegliere l'azione **Registra**.

I movimenti interessati vengono registrati nella società e una registrazione con i movimenti corrispondenti viene creata nella casella in uscita IC che è possibile inviare alla società partner. Per ulteriori informazioni, vedere [Gestire la casella in entrata e in uscita intercompany](intercompany-how-manage-intercompany-inbox.md). 

## <a name="see-also"></a>Vedi anche
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

