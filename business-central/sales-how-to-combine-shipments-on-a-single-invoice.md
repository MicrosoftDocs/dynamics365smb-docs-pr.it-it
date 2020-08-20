---
title: 'Procedura: Combinare le spedizioni in una singola fattura | Documenti Microsoft'
description: Se si desidera fatturare più di una spedizione per volta, utilizzare la funzionalità per le spedizioni cumulate.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f6ce4c0c304fc8255789ec91fb3a00ba78170d6d
ms.sourcegitcommit: 6078bc9b2b571248d779722ce4125f250e7a3922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/07/2020
ms.locfileid: "3666924"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="81443-103">Combinare le spedizioni in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="81443-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="81443-104">Se si desidera fatturare più di una spedizione per volta, utilizzare la funzionalità per le spedizioni cumulate.</span><span class="sxs-lookup"><span data-stu-id="81443-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="81443-105">Prima di creare una spedizione cumulata, è necessario che venga registrata più di una spedizione di vendita per lo stesso cliente nella stessa valuta.</span><span class="sxs-lookup"><span data-stu-id="81443-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="81443-106">In altri termini, è necessario creare due o più ordini di vendita e registrarli come spediti, ma non fatturati.</span><span class="sxs-lookup"><span data-stu-id="81443-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="81443-107">Per combinare manualmente le spedizioni in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="81443-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="81443-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture vendite** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="81443-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="81443-109">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="81443-109">Choose the **New** action.</span></span> <span data-ttu-id="81443-110">Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="81443-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="81443-111">Nel campo **Vendere a - Nr. cliente**</span><span class="sxs-lookup"><span data-stu-id="81443-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="81443-112">immettere il cliente che riceverà la fattura per gli articoli spediti.</span><span class="sxs-lookup"><span data-stu-id="81443-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="81443-113">Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di spedizione**.</span><span class="sxs-lookup"><span data-stu-id="81443-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="81443-114">Selezionare le righe di spedizione che si desidera includere nella fattura:</span><span class="sxs-lookup"><span data-stu-id="81443-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="81443-115">Per inserire tutte le righe, selezionare tutte le righe, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="81443-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="81443-116">Per inserire righe specifiche, selezionare le righe, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="81443-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="81443-117">È possibile utilizzare il tasto CTRL per selezionare più righe non consecutive.</span><span class="sxs-lookup"><span data-stu-id="81443-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="81443-118">Se viene selezionata una riga di spedizione errata o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura ed eseguire nuovamente la funzione **Prendi righe di spedizione**.</span><span class="sxs-lookup"><span data-stu-id="81443-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="81443-119">Per registrare la fattura scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="81443-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="81443-120">Per combinare automaticamente le spedizioni in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="81443-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="81443-121">selezionerà solo gli ordini di vendita in cui **Fatture cumulative** è scelto.</span><span class="sxs-lookup"><span data-stu-id="81443-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="81443-122">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture cumulative** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="81443-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="81443-123">Viene visualizzata la pagina di richiesta del processo batch.</span><span class="sxs-lookup"><span data-stu-id="81443-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="81443-124">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="81443-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="81443-125">Scegliere la casella di controllo **Registra fatture**.</span><span class="sxs-lookup"><span data-stu-id="81443-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="81443-126">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="81443-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="81443-127">Se la casella di controllo **Registra fatture** non è selezionata per il processo batch, sarà necessario registrare manualmente le fatture.</span><span class="sxs-lookup"><span data-stu-id="81443-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="81443-128">Per rimuovere ordini di vendita aperti dopo la registrazione della spedizione combinata</span><span class="sxs-lookup"><span data-stu-id="81443-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="81443-129">Quando le spedizioni vengono cumulate in una fattura e registrate, per le righe fatturate viene creata una fattura di vendita registrata.</span><span class="sxs-lookup"><span data-stu-id="81443-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="81443-130">Il campo **Quantità fatturata** dell'ordine di vendita o dell'ordine di vendita programmato di origine viene aggiornato in base alla quantità fatturata.</span><span class="sxs-lookup"><span data-stu-id="81443-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="81443-131">Quando si fatturano spedizioni in questo modo, gli ordini da cui sono state registrate le spedizioni vengono mantenuti, anche se sono già stati completamente spediti e fatturati.</span><span class="sxs-lookup"><span data-stu-id="81443-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="81443-132">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina ord. vendita fatturati** e quindi selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="81443-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="81443-133">Specificare nel campo del filtro **Nr.**</span><span class="sxs-lookup"><span data-stu-id="81443-133">Specify in the **No.**</span></span> <span data-ttu-id="81443-134">quali ordini di vendite eliminare.</span><span class="sxs-lookup"><span data-stu-id="81443-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="81443-135">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="81443-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="81443-136">In alternativa, eliminare i singoli ordini di vendita manualmente.</span><span class="sxs-lookup"><span data-stu-id="81443-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="81443-137">Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di vendita programmati.</span><span class="sxs-lookup"><span data-stu-id="81443-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="81443-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="81443-138">See Also</span></span>  
[<span data-ttu-id="81443-139">Vendite</span><span class="sxs-lookup"><span data-stu-id="81443-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="81443-140">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81443-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
