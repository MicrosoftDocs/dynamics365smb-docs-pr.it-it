---
title: Creare un ordine di vendita collegato a un ordine di acquisto per una spedizione diretta | Documenti Microsoft
description: Viene descritto come creare un ordine di vendita collegato a un ordine di acquisto per consentire la spedizione diretta dal fornitore al cliente.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 087ead3b0a28d09cd687c1fcb60f6fee2c914c4a
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="make-drop-shipments"></a><span data-ttu-id="82013-103">Effettuare spedizioni dirette</span><span class="sxs-lookup"><span data-stu-id="82013-103">Make Drop Shipments</span></span>
<span data-ttu-id="82013-104">Una spedizione diretta è costituita dalla spedizione di articoli direttamente da un fornitore a un cliente.</span><span class="sxs-lookup"><span data-stu-id="82013-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="82013-105">Quando un ordine di vendita è contrassegnato per la spedizione diretta e si crea un ordine di acquisto specificando il cliente nel campo **Vendere a - Nr. cliente**,</span><span class="sxs-lookup"><span data-stu-id="82013-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="82013-106">è possibile collegare due documenti e istruire il fornitore di spedire direttamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="82013-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="82013-107">Per creare un ordine di vendita per una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="82013-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="82013-108">Per preparare una spedizione diretta, si crea un ordine di vendita per un articolo come al solito, ad eccezione del fatto che è necessario indicare sulla riga di vendita che la vendita richiede la spedizione diretta.</span><span class="sxs-lookup"><span data-stu-id="82013-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="82013-109">Creare un ordine cliente per un articolo.</span><span class="sxs-lookup"><span data-stu-id="82013-109">Create a sales order for an item.</span></span> <span data-ttu-id="82013-110">Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="82013-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="82013-111">Nella riga ordine di vendita per la spedizione diretta selezionare la casella di controllo **Spedizione diretta**.</span><span class="sxs-lookup"><span data-stu-id="82013-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="82013-112">Utilizzare la funzione **Scegli colonne** se il campo non è visualizzato.</span><span class="sxs-lookup"><span data-stu-id="82013-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="82013-113">Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="82013-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="82013-114">Per creare l'ordine di acquisto per la spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="82013-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="82013-115">Per preparare una spedizione diretta per l'articolo da vendere, si crea un ordine di acquisto come al solito, ad eccezione del fatto che è necessario indicare nell'ordine di acquisto che deve essere spedito al cliente e non a se stessi.</span><span class="sxs-lookup"><span data-stu-id="82013-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="82013-116">Creare un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="82013-116">Create a purchase order.</span></span> <span data-ttu-id="82013-117">Non compilare i campi nelle righe.</span><span class="sxs-lookup"><span data-stu-id="82013-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="82013-118">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="82013-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="82013-119">Nel campo **Vendere a - Nr. cliente**</span><span class="sxs-lookup"><span data-stu-id="82013-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="82013-120">selezionare il cliente a cui si sta vendendo.</span><span class="sxs-lookup"><span data-stu-id="82013-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="82013-121">Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.</span><span class="sxs-lookup"><span data-stu-id="82013-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="82013-122">Nella finestra **Lista vendite**, selezionare l'ordine di vendita che è stato preparato nella sezione "Per creare un ordine di vendita per una spedizione diretta".</span><span class="sxs-lookup"><span data-stu-id="82013-122">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="82013-123">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="82013-123">Choose the **OK** button.</span></span>

<span data-ttu-id="82013-124">Le informazioni di riga dall'ordine di vendita vengono inserite nelle righe dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="82013-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="82013-125">È possibile istruire il fornitore di spedire gli articoli al cliente, ad esempio spedendo l'ordine di acquisto come PDF.</span><span class="sxs-lookup"><span data-stu-id="82013-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="82013-126">Per visualizzare l'ordine di acquisto collegato dall'ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="82013-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="82013-127">Selezionare la riga dell'ordine di vendita con spedizione diretta, scegliere l'azione **Ordine**, scegliere l'azione **Spedizione diretta** e quindi scegliere l'azione **Ordine acquisto**.</span><span class="sxs-lookup"><span data-stu-id="82013-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="82013-128">Per registrare una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="82013-128">To post a drop shipment</span></span>
<span data-ttu-id="82013-129">Dopo che il fornitore ha spedito gli articoli, è possibile registrare l'ordine di vendita come spedito.</span><span class="sxs-lookup"><span data-stu-id="82013-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="82013-130">È possibile registrare anche l'ordine di acquisto, ma solo con l'opzione **Ricevi** finché l'ordine di vendita non viene fatturato.</span><span class="sxs-lookup"><span data-stu-id="82013-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="82013-131">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di vendita**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="82013-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="82013-132">Aprire l'ordine di vendita creato nella sezione "Per creare un ordine di vendita per una spedizione diretta".</span><span class="sxs-lookup"><span data-stu-id="82013-132">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="82013-133">Nel campo **Qtà da spedire**, specificare la quantità dell'ordine da spedire, la quantità dell'ordine completa o parziale.</span><span class="sxs-lookup"><span data-stu-id="82013-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="82013-134">Scegliere l'azione **Registra** o **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="82013-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="82013-135">Selezionare l'opzione **Spedizione** per fatturare in seguito oppure l'opzione **Spedisci e fattura** per fatturare immediatamente.</span><span class="sxs-lookup"><span data-stu-id="82013-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="82013-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82013-136">See Also</span></span>
<span data-ttu-id="82013-137">[Creare ordini speciali](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="82013-137">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="82013-138">Vendere prodotti</span><span class="sxs-lookup"><span data-stu-id="82013-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="82013-139">Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="82013-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="82013-140">Vendite</span><span class="sxs-lookup"><span data-stu-id="82013-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="82013-141">Magazzino</span><span class="sxs-lookup"><span data-stu-id="82013-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="82013-142">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82013-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

