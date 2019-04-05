---
title: Collegare un ordine di vendita a un ordine di acquisto per una spedizione diretta | Documenti Microsoft
description: Viene descritto come creare un ordine di vendita collegato a un ordine di acquisto per consentire la spedizione diretta dal fornitore al cliente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 77bed1563a5c0187e78f7e7013dfed4a723d7702
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801681"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="408bb-103">Effettuare spedizioni dirette</span><span class="sxs-lookup"><span data-stu-id="408bb-103">Make Drop Shipments</span></span>
<span data-ttu-id="408bb-104">Una spedizione diretta è costituita dalla spedizione di articoli direttamente da un fornitore a un cliente.</span><span class="sxs-lookup"><span data-stu-id="408bb-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="408bb-105">Quando un ordine di vendita è contrassegnato per la spedizione diretta e si crea un ordine di acquisto specificando il cliente nel campo **Vendere a - Nr. cliente**,</span><span class="sxs-lookup"><span data-stu-id="408bb-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="408bb-106">è possibile collegare due documenti e istruire il fornitore di spedire direttamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="408bb-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="408bb-107">Per creare un ordine di vendita per una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="408bb-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="408bb-108">Per preparare una spedizione diretta, si crea un ordine di vendita per un articolo come al solito, ad eccezione del fatto che è necessario indicare sulla riga di vendita che la vendita richiede la spedizione diretta.</span><span class="sxs-lookup"><span data-stu-id="408bb-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="408bb-109">Creare un ordine cliente per un articolo.</span><span class="sxs-lookup"><span data-stu-id="408bb-109">Create a sales order for an item.</span></span> <span data-ttu-id="408bb-110">Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="408bb-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="408bb-111">Nella riga ordine di vendita per la spedizione diretta selezionare la casella di controllo **Spedizione diretta**.</span><span class="sxs-lookup"><span data-stu-id="408bb-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="408bb-112">Utilizzare la funzione **Scegli colonne** se il campo non è visualizzato.</span><span class="sxs-lookup"><span data-stu-id="408bb-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="408bb-113">Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="408bb-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="408bb-114">Per creare l'ordine di acquisto per la spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="408bb-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="408bb-115">Per preparare una spedizione diretta per l'articolo da vendere, si crea un ordine di acquisto come al solito, ad eccezione del fatto che è necessario indicare nell'ordine di acquisto che deve essere spedito al cliente e non a se stessi.</span><span class="sxs-lookup"><span data-stu-id="408bb-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="408bb-116">Creare un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="408bb-116">Create a purchase order.</span></span> <span data-ttu-id="408bb-117">Non compilare i campi nelle righe.</span><span class="sxs-lookup"><span data-stu-id="408bb-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="408bb-118">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="408bb-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="408bb-119">Nel campo **Vendere a - Nr. cliente**</span><span class="sxs-lookup"><span data-stu-id="408bb-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="408bb-120">selezionare il cliente a cui si sta vendendo.</span><span class="sxs-lookup"><span data-stu-id="408bb-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="408bb-121">Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.</span><span class="sxs-lookup"><span data-stu-id="408bb-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="408bb-122">Nella pagina **Lista vendite**, selezionare l'ordine di vendita che è stato preparato nella sezione [Per creare un ordine di vendita per una spedizione diretta](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="408bb-122">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="408bb-123">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="408bb-123">Choose the **OK** button.</span></span>

<span data-ttu-id="408bb-124">Le informazioni di riga dall'ordine di vendita vengono inserite nelle righe dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="408bb-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="408bb-125">È possibile istruire il fornitore di spedire gli articoli al cliente, ad esempio spedendo l'ordine di acquisto come PDF.</span><span class="sxs-lookup"><span data-stu-id="408bb-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="408bb-126">Per visualizzare l'ordine di acquisto collegato dall'ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="408bb-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="408bb-127">Selezionare la riga dell'ordine di vendita con spedizione diretta, scegliere l'azione **Ordine**, scegliere l'azione **Spedizione diretta** e quindi scegliere l'azione **Ordine acquisto**.</span><span class="sxs-lookup"><span data-stu-id="408bb-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="408bb-128">Per registrare una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="408bb-128">To post a drop shipment</span></span>
<span data-ttu-id="408bb-129">Dopo che il fornitore ha spedito gli articoli, è possibile registrare l'ordine di vendita come spedito.</span><span class="sxs-lookup"><span data-stu-id="408bb-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="408bb-130">È possibile registrare anche l'ordine di acquisto, ma solo con l'opzione **Ricevi** finché l'ordine di vendita non viene fatturato.</span><span class="sxs-lookup"><span data-stu-id="408bb-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="408bb-131">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="408bb-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="408bb-132">Aprire l'ordine di vendita creato nella sezione [Per creare un ordine di vendita per una spedizione diretta]().</span><span class="sxs-lookup"><span data-stu-id="408bb-132">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="408bb-133">Nel campo **Qtà da spedire**, specificare la quantità dell'ordine da spedire, la quantità dell'ordine completa o parziale.</span><span class="sxs-lookup"><span data-stu-id="408bb-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="408bb-134">Scegliere l'azione **Registra** o **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="408bb-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="408bb-135">Selezionare l'opzione **Spedizione** per fatturare in seguito oppure l'opzione **Spedisci e fattura** per fatturare immediatamente.</span><span class="sxs-lookup"><span data-stu-id="408bb-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="408bb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="408bb-136">See Also</span></span>
[<span data-ttu-id="408bb-137">Creare ordini speciali</span><span class="sxs-lookup"><span data-stu-id="408bb-137">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="408bb-138">Acquistare articoli per una vendita</span><span class="sxs-lookup"><span data-stu-id="408bb-138">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="408bb-139">Vendere prodotti</span><span class="sxs-lookup"><span data-stu-id="408bb-139">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="408bb-140">Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="408bb-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="408bb-141">Vendite</span><span class="sxs-lookup"><span data-stu-id="408bb-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="408bb-142">Magazzino</span><span class="sxs-lookup"><span data-stu-id="408bb-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="408bb-143">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="408bb-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
