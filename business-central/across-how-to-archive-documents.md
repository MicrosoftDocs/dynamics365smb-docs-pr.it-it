---
title: Come archiviare documenti di acquisto e vendita | Documenti Microsoft
description: "È possibile archiviare ordini di acquisto e vendita, offerte, ordini di reso e ordini programmati e utilizzare il documento archiviato per ricreare il documento da cui è stato archiviato."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: 6b1b23c062fdb1c4558a292c7aa454ae24ff3c71
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="archive-documents"></a><span data-ttu-id="00bb4-103">Archiviare documenti</span><span class="sxs-lookup"><span data-stu-id="00bb4-103">Archive Documents</span></span>
<span data-ttu-id="00bb4-104">È possibile archiviare ordini di acquisto e vendita, offerte, ordini di reso e ordini programmati e utilizzare il documento archiviato per ricreare il documento da cui è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="00bb4-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="00bb4-105">Per impostare l'archiviazione automatica dei documenti</span><span class="sxs-lookup"><span data-stu-id="00bb4-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="00bb4-106">È possibile impostare l'archiviazione automatica di documenti di vendita e di acquisto, offerte, ordini programmati e ordini di reso, prima di eliminarli.</span><span class="sxs-lookup"><span data-stu-id="00bb4-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="00bb4-107">La procedura seguente illustra come configurare l'archiviazione automatica di documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="00bb4-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="00bb4-108">I passaggi sono simili per i documenti di acquisto.</span><span class="sxs-lookup"><span data-stu-id="00bb4-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="00bb4-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità clienti e vendite** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="00bb4-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="00bb4-110">Nella finestra **Setup contabilità clienti e vendite** compilare i campi come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="00bb4-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="00bb4-111">Campo</span><span class="sxs-lookup"><span data-stu-id="00bb4-111">Field</span></span>|<span data-ttu-id="00bb4-112">Description</span><span class="sxs-lookup"><span data-stu-id="00bb4-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="00bb4-113">**Archiviazione Offerte Vendita**</span><span class="sxs-lookup"><span data-stu-id="00bb4-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="00bb4-114">**Mai** per non archiviare mai offerte di vendita quando vengono eliminate.</span><span class="sxs-lookup"><span data-stu-id="00bb4-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="00bb4-115">**Domanda** per chiedere all'utente di scegliere se archiviare le offerte di vendita quando vengono eliminate.</span><span class="sxs-lookup"><span data-stu-id="00bb4-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="00bb4-116">**Sempre** per non archiviare automaticamente le offerte di vendita quando vengono eliminate.</span><span class="sxs-lookup"><span data-stu-id="00bb4-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="00bb4-117">**Archiviazione ordini di vendita programmati**</span><span class="sxs-lookup"><span data-stu-id="00bb4-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="00bb4-118">Selezionare questa opzione per archiviare automaticamente gli ordini di vendita programmati ogni volta che vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="00bb4-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="00bb4-119">**Ordini archiviati e ordini di reso**</span><span class="sxs-lookup"><span data-stu-id="00bb4-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="00bb4-120">Selezionare questa opzione per archiviare automaticamente gli ordini di vendita ogni volta che vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="00bb4-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="00bb4-121">Per archiviare un ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="00bb4-121">To archive a sales order</span></span>
<span data-ttu-id="00bb4-122">Di seguito viene descritto come archiviare un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="00bb4-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="00bb4-123">I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.</span><span class="sxs-lookup"><span data-stu-id="00bb4-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="00bb4-124">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="00bb4-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="00bb4-125">Aprire un ordine di vendita da archiviare.</span><span class="sxs-lookup"><span data-stu-id="00bb4-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="00bb4-126">Scegliere l'azione **Archivia documento**.</span><span class="sxs-lookup"><span data-stu-id="00bb4-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="00bb4-127">L'ordine di vendita è archiviato.</span><span class="sxs-lookup"><span data-stu-id="00bb4-127">The sales order is archived.</span></span> <span data-ttu-id="00bb4-128">È possibile visualizzarlo nella finestra **Ordine vendite archiviato**.</span><span class="sxs-lookup"><span data-stu-id="00bb4-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="00bb4-129">Da qui, è anche possibile utilizzarlo per ricreare l'ordine di vendita da cui è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="00bb4-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="00bb4-130">Per ricreare un ordine di vendita dall'archivio</span><span class="sxs-lookup"><span data-stu-id="00bb4-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="00bb4-131">Di seguito viene descritto come ricreare un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="00bb4-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="00bb4-132">I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.</span><span class="sxs-lookup"><span data-stu-id="00bb4-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="00bb4-133">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita archiviati** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="00bb4-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="00bb4-134">Selezionare l'ordine di vendita archiviato da ricreare, quindi scegliere l'azione **Ripristina**.</span><span class="sxs-lookup"><span data-stu-id="00bb4-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="00bb4-135">L'ordine di vendita viene creato e aggiunto alla finestra **Ordini vendita**.</span><span class="sxs-lookup"><span data-stu-id="00bb4-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="00bb4-136">Per eliminare ordini di vendita archiviati</span><span class="sxs-lookup"><span data-stu-id="00bb4-136">To delete archived sales orders</span></span>
<span data-ttu-id="00bb4-137">Di seguito viene descritto come eliminare ordini di vendita archiviati.</span><span class="sxs-lookup"><span data-stu-id="00bb4-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="00bb4-138">I passaggi sono simili per altri altri documenti di acquisto e vendita archiviati.</span><span class="sxs-lookup"><span data-stu-id="00bb4-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="00bb4-139">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina versioni ordine vendita archiviate** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="00bb4-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="00bb4-140">Nella finestra **Elimina versioni ordine vendita archiviate**, selezionare i filtri appropriati.</span><span class="sxs-lookup"><span data-stu-id="00bb4-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="00bb4-141">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="00bb4-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="00bb4-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00bb4-142">See Also</span></span>
[<span data-ttu-id="00bb4-143">Tenere traccia delle righe dei documenti</span><span class="sxs-lookup"><span data-stu-id="00bb4-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="00bb4-144">Vendite</span><span class="sxs-lookup"><span data-stu-id="00bb4-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="00bb4-145">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="00bb4-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="00bb4-146">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00bb4-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

