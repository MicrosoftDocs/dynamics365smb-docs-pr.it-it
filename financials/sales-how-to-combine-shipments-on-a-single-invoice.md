---
title: 'Procedura: Combinare le spedizioni in una singola fattura | Documenti Microsoft'
description: "Se si desidera fatturare più di una spedizione per volta, utilizzare la funzionalità per le spedizioni cumulate."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="aa04c-103">Combinare le spedizioni in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="aa04c-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="aa04c-104">Se si desidera fatturare più di una spedizione per volta, utilizzare la funzionalità per le spedizioni cumulate.</span><span class="sxs-lookup"><span data-stu-id="aa04c-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="aa04c-105">Prima di creare una spedizione cumulata, è necessario che venga registrata più di una spedizione di vendita per lo stesso cliente nella stessa valuta.</span><span class="sxs-lookup"><span data-stu-id="aa04c-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="aa04c-106">In altri termini, è necessario compilare due o più ordini di vendita e registrarli come spediti, ma non fatturati.</span><span class="sxs-lookup"><span data-stu-id="aa04c-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="aa04c-107">Per cumulare le spedizioni, è necessario selezionare la casella di controllo **Fatt. cumulative** nella Scheda dettaglio **Spedizione** della scheda **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="aa04c-108">Per combinare manualmente le spedizioni in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="aa04c-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="aa04c-109">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Fatture vendite**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="aa04c-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aa04c-110">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-110">Choose the **New** action.</span></span> <span data-ttu-id="aa04c-111">Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="aa04c-111">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="aa04c-112">Nel campo **Vendere a - Nr. cliente**</span><span class="sxs-lookup"><span data-stu-id="aa04c-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="aa04c-113">immettere il cliente che riceverà la fattura per gli articoli spediti.</span><span class="sxs-lookup"><span data-stu-id="aa04c-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="aa04c-114">Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di spedizione**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="aa04c-115">Selezionare le righe di spedizione che si desidera includere nella fattura:</span><span class="sxs-lookup"><span data-stu-id="aa04c-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="aa04c-116">Per inserire tutte le righe, selezionare tutte le righe, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="aa04c-117">Per inserire righe specifiche, selezionare le righe, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="aa04c-118">È possibile utilizzare il tasto CTRL per selezionare più righe non consecutive.</span><span class="sxs-lookup"><span data-stu-id="aa04c-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="aa04c-119">Se viene selezionata una riga di spedizione errata o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura ed eseguire nuovamente la funzione **Prendi righe di spedizione**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="aa04c-120">Per registrare la fattura scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="aa04c-121">Per combinare automaticamente le spedizioni in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="aa04c-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="aa04c-122">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture cumulative**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="aa04c-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="aa04c-123">Viene visualizzata la finestra di richiesta del processo batch.</span><span class="sxs-lookup"><span data-stu-id="aa04c-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="aa04c-124">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="aa04c-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="aa04c-125">Selezionare la casella di controllo **Registra fatture**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="aa04c-126">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="aa04c-127">Se la casella di controllo **Registra fatture** non è selezionata per il processo batch, sarà necessario registrare manualmente le fatture.</span><span class="sxs-lookup"><span data-stu-id="aa04c-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="aa04c-128">Per rimuovere ordini di vendita aperti dopo la registrazione della spedizione combinata</span><span class="sxs-lookup"><span data-stu-id="aa04c-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="aa04c-129">Quando le spedizioni vengono cumulate in una fattura e registrate, per le righe fatturate viene creata una fattura di vendita registrata.</span><span class="sxs-lookup"><span data-stu-id="aa04c-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="aa04c-130">Il campo **Quantità fatturata** dell'ordine di vendita o dell'ordine di vendita programmato di origine viene aggiornato in base alla quantità fatturata.</span><span class="sxs-lookup"><span data-stu-id="aa04c-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="aa04c-131">Quando si fatturano spedizioni in questo modo, gli ordini da cui sono state registrate le spedizioni vengono mantenuti, anche se sono già stati completamente spediti e fatturati.</span><span class="sxs-lookup"><span data-stu-id="aa04c-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="aa04c-132">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Elimina ordini vendita fatturati**, quindi scegliere il collegamento.</span><span class="sxs-lookup"><span data-stu-id="aa04c-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="aa04c-133">Specificare nel campo del filtro **Nr.**</span><span class="sxs-lookup"><span data-stu-id="aa04c-133">Specify in the **No.**</span></span> <span data-ttu-id="aa04c-134">quali ordini di vendite eliminare.</span><span class="sxs-lookup"><span data-stu-id="aa04c-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="aa04c-135">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa04c-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="aa04c-136">In alternativa, eliminare i singoli ordini di vendita manualmente.</span><span class="sxs-lookup"><span data-stu-id="aa04c-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="aa04c-137">Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di vendita programmati.</span><span class="sxs-lookup"><span data-stu-id="aa04c-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa04c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa04c-138">See Also</span></span>  
[<span data-ttu-id="aa04c-139">Vendite</span><span class="sxs-lookup"><span data-stu-id="aa04c-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="aa04c-140">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa04c-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

