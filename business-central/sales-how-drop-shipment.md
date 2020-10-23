---
title: Collegare un ordine di vendita a un ordine di acquisto per una spedizione diretta | Documenti Microsoft
description: Viene descritto come creare un ordine di vendita collegato a un ordine di acquisto per consentire la spedizione diretta dal fornitore al cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: add7cf9f2f274f50d0e187362b2e0c1bcc2fe8e0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926274"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="eabe9-103">Effettuare spedizioni dirette</span><span class="sxs-lookup"><span data-stu-id="eabe9-103">Make Drop Shipments</span></span>

<span data-ttu-id="eabe9-104">Una spedizione diretta è costituita dalla spedizione di articoli direttamente da un fornitore a un cliente.</span><span class="sxs-lookup"><span data-stu-id="eabe9-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="eabe9-105">Quando un ordine cliente è contrassegnato per la spedizione di consegna e si crea un ordine d'acquisto specificando il cliente nel campo **Spedire a** **Indirizzo cliente**, è possibile collegare i due documenti e istruire il fornitore spedire direttamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="eabe9-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="eabe9-106">Per creare un ordine di vendita per una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="eabe9-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="eabe9-107">Per preparare una spedizione diretta, si crea un ordine di vendita per un articolo e indicare sulla riga di vendita che la vendita richiede la spedizione diretta.</span><span class="sxs-lookup"><span data-stu-id="eabe9-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="eabe9-108">Creare un ordine cliente per un articolo.</span><span class="sxs-lookup"><span data-stu-id="eabe9-108">Create a sales order for an item.</span></span> <span data-ttu-id="eabe9-109">Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="eabe9-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="eabe9-110">Nella riga ordine di vendita per la spedizione diretta selezionare la casella di controllo **Spedizione diretta**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="eabe9-111">Utilizzare la funzione **Scegli colonne** se il campo non è visualizzato.</span><span class="sxs-lookup"><span data-stu-id="eabe9-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="eabe9-112">Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="eabe9-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="eabe9-113">Per creare l'ordine di acquisto per la spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="eabe9-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="eabe9-114">Per preparare una spedizione diretta, indicare nell'ordine di acquisto che l'articolo deve essere spedito al cliente, non a se stessi.</span><span class="sxs-lookup"><span data-stu-id="eabe9-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="eabe9-115">Creare un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="eabe9-115">Create a purchase order.</span></span> <span data-ttu-id="eabe9-116">Non compilare i campi nelle righe.</span><span class="sxs-lookup"><span data-stu-id="eabe9-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="eabe9-117">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="eabe9-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="eabe9-118">Nel campo **Spedire a**, selezionare **Indirizzo cliente**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="eabe9-119">Nel campo **Cliente**, selezionare il cliente a cui si sta vendendo.</span><span class="sxs-lookup"><span data-stu-id="eabe9-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="eabe9-120">Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="eabe9-121">Nella pagina **Lista vendite**, selezionare l'ordine di vendita che è stato preparato nella sezione [Per creare un ordine di vendita per una spedizione diretta](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="eabe9-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="eabe9-122">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-122">Choose the **OK** button.</span></span>

<span data-ttu-id="eabe9-123">Le informazioni di riga dall'ordine di vendita vengono inserite nelle righe dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="eabe9-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="eabe9-124">È possibile istruire il fornitore di spedire gli articoli al cliente, ad esempio spedendo l'ordine di acquisto come PDF.</span><span class="sxs-lookup"><span data-stu-id="eabe9-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="eabe9-125">Per creare più ordini di acquisto per spedizioni dirette</span><span class="sxs-lookup"><span data-stu-id="eabe9-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="eabe9-126">È inoltre possibile utilizzare la richiesta di approvvigionamento per creare l'ordine di acquisto per il fornitore.</span><span class="sxs-lookup"><span data-stu-id="eabe9-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="eabe9-127">Il vantaggio di utilizzare la richiesta di approvvigionamento è che è possibile creare ordini di acquisto per tutte le spedizioni dirette in sospeso, quindi non è necessario crearle singolarmente.</span><span class="sxs-lookup"><span data-stu-id="eabe9-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="eabe9-128">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Richieste di approvvigionamento** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="eabe9-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="eabe9-129">Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="eabe9-130">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="eabe9-131">Rivedere le righe dell'ordine di acquisto e nel campo **Nr. fornitore**, selezionare il fornitore che fornisce le merci richieste.</span><span class="sxs-lookup"><span data-stu-id="eabe9-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="eabe9-132">Scegliere l'azione **Esegui messaggi di azione** per convertire le righe riviste in un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="eabe9-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="eabe9-133">Per visualizzare l'ordine di acquisto collegato dall'ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="eabe9-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="eabe9-134">Selezionare la riga dell'ordine di vendita con spedizione diretta, scegliere l'azione **Ordine**, scegliere l'azione **Spedizione diretta** e quindi scegliere l'azione **Ordine acquisto**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="eabe9-135">Per registrare una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="eabe9-135">To post a drop shipment</span></span>

<span data-ttu-id="eabe9-136">Dopo che il fornitore ha spedito gli articoli, è possibile registrare l'ordine di vendita come spedito.</span><span class="sxs-lookup"><span data-stu-id="eabe9-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="eabe9-137">È possibile registrare anche l'ordine di acquisto, ma solo con l'opzione **Ricevi** finché l'ordine di vendita non viene fatturato.</span><span class="sxs-lookup"><span data-stu-id="eabe9-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="eabe9-138">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="eabe9-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="eabe9-139">Aprire l'ordine di vendita creato nella sezione [Per creare un ordine di vendita per una spedizione diretta](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="eabe9-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="eabe9-140">Nel campo **Qtà da spedire**, specificare la quantità dell'ordine da spedire, la quantità dell'ordine completa o parziale.</span><span class="sxs-lookup"><span data-stu-id="eabe9-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="eabe9-141">Scegliere l'azione **Registra** o **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="eabe9-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="eabe9-142">Selezionare l'opzione **Spedizione** per fatturare in seguito oppure l'opzione **Spedisci e fattura** per fatturare immediatamente.</span><span class="sxs-lookup"><span data-stu-id="eabe9-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="eabe9-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eabe9-143">See Also</span></span>

[<span data-ttu-id="eabe9-144">Creare ordini speciali</span><span class="sxs-lookup"><span data-stu-id="eabe9-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="eabe9-145">Acquistare articoli per una vendita</span><span class="sxs-lookup"><span data-stu-id="eabe9-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="eabe9-146">Vendere prodotti</span><span class="sxs-lookup"><span data-stu-id="eabe9-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="eabe9-147">Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="eabe9-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="eabe9-148">Vendite</span><span class="sxs-lookup"><span data-stu-id="eabe9-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="eabe9-149">Magazzino</span><span class="sxs-lookup"><span data-stu-id="eabe9-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="eabe9-150">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eabe9-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
