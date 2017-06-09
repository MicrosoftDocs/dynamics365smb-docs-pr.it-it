---
title: 'Procedura: Correggere o annullare le fatture di acquisto non pagate | Documenti Microsoft'
description: 'Procedura: Correggere o annullare le fatture di acquisto non pagate'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fba080da79d3a9d3f816c8ddc0a02c877211bcb4
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Procedura: Correggere o annullare le fatture di acquisto non pagate
È possibile correggere o annullare una fattura di acquisto registrata. Ciò risulta utile se si desidera correggere un errore di digitazione o se si desidera modificare l'acquisto in una fase iniziale dell'elaborazione dell'ordine.

Se è già stato eseguito il pagamento dei prodotti nella fattura di acquisto registrata, non è possibile correggerli o annullarli dalla fattura di acquisto registrata. In alternativa, è necessario creare manualmente una nota di credito di acquisto per stornare l'acquisto. Per ulteriori informazioni vedere [Procedura: Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md).

Nella finestra **Fattura acquisto registrata** è possibile scegliere il pulsante **Rettifica** o il pulsante **Annulla**. Quando si rettifica o si annulla una fattura di acquisto registrata, la nota di credito di acquisto viene applicata a tutti i movimenti contabili generali e di inventario creati quando la fattura di acquisto iniziale è stata registrata. Ciò consente di stornare la fattura di acquisto nei record finanziari e lascia la nota di credito di acquisto registrata correttiva per l'audit trail. Di seguito viene descritto l'utilizzo di **Rettifica** e di **Annulla**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Per correggere una fattura di acquisto registrata
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Fatture acquisto reg.**, quindi scegliere il collegamento correlato.  
2. Selezionare la fattura di acquisto che si desidera rettificare.  

    **Nota**: se viene selezionata la casella di controllo **Annullato**, non è possibile rettificare la fattura di acquisto registrata poiché è già stata rettificata o annullata.
3. Nella finestra **Fattura acquisto registrata** scegliere **Rettifica**.

    Viene creata una nuova fattura di acquisto con le stesse informazioni in cui è possibile apportare la rettifica. Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md). Il campo **Annullato** nella fattura di acquisto registrata iniziale viene modificato in **Sì**.

    Una nota di credito di acquisto viene automaticamente creata e registrata per annullare la fattura di acquisto registrata iniziale.
4. Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di acquisto registrata che annulla la fattura di acquisto registrata iniziale.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Per annullare una fattura di acquisto registrata
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Fatture acquisto reg.**, quindi scegliere il collegamento correlato.  
2. Selezionare la fattura di acquisto che si desidera annullare.

    **Nota**: se viene selezionata la casella di controllo **Annullato**, non è possibile annullare la fattura di acquisto registrata poiché è già stata annullata o rettificata.
3. Nella finestra **Fattura acquisto registrata** scegliere **Annulla**.

    Una nota di credito di acquisto viene automaticamente creata e registrata per annullare la fattura di acquisto registrata iniziale. Il campo **Annullato** nella fattura di acquisto registrata iniziale viene modificato in **Sì**.
4. Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di acquisto registrata che annulla la fattura di acquisto registrata iniziale.

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

