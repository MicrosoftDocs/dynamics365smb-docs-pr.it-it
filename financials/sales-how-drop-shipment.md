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
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="fab99-103">Procedura: Effettuare spedizioni dirette</span><span class="sxs-lookup"><span data-stu-id="fab99-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="fab99-104">Una spedizione diretta è costituita dalla spedizione di articoli direttamente da un fornitore a un cliente.</span><span class="sxs-lookup"><span data-stu-id="fab99-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="fab99-105">Quando un ordine di vendita è contrassegnato per la spedizione diretta e si crea un ordine di acquisto specificando il cliente nel campo **Vendere a - Nr. cliente**,</span><span class="sxs-lookup"><span data-stu-id="fab99-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="fab99-106">è possibile collegare due documenti e istruire il fornitore di spedire direttamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="fab99-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="fab99-107">Per creare un ordine di vendita per una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="fab99-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="fab99-108">Per preparare una spedizione diretta, si crea un ordine di vendita per un articolo come al solito, ad eccezione del fatto che è necessario indicare sulla riga di vendita che la vendita richiede la spedizione diretta.</span><span class="sxs-lookup"><span data-stu-id="fab99-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="fab99-109">Creare un ordine cliente per un articolo.</span><span class="sxs-lookup"><span data-stu-id="fab99-109">Create a sales order for an item.</span></span> <span data-ttu-id="fab99-110">Per ulteriori informazioni, vedere [Procedura: Vendere prodotti](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="fab99-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="fab99-111">Nella riga ordine di vendita per la spedizione diretta selezionare la casella di controllo **Spedizione diretta**.</span><span class="sxs-lookup"><span data-stu-id="fab99-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="fab99-112">Utilizzare la funzione **Scegli colonne** se il campo non è visualizzato.</span><span class="sxs-lookup"><span data-stu-id="fab99-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="fab99-113">Per ulteriori informazioni, vedere [Personalizzazione utente](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="fab99-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="fab99-114">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="fab99-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="fab99-115">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="fab99-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="fab99-116">Per creare l'ordine di acquisto per la spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="fab99-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="fab99-117">Per preparare una spedizione diretta per l'articolo da vendere, si crea un ordine di acquisto come al solito, ad eccezione del fatto che è necessario indicare nell'ordine di acquisto che deve essere spedito al cliente e non a se stessi.</span><span class="sxs-lookup"><span data-stu-id="fab99-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="fab99-118">Creare un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="fab99-118">Create a purchase order.</span></span> <span data-ttu-id="fab99-119">Non compilare i campi nelle righe.</span><span class="sxs-lookup"><span data-stu-id="fab99-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="fab99-120">Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="fab99-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="fab99-121">Nel campo **Vendere a - Nr. cliente**</span><span class="sxs-lookup"><span data-stu-id="fab99-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="fab99-122">selezionare il cliente a cui si sta vendendo.</span><span class="sxs-lookup"><span data-stu-id="fab99-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="fab99-123">Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.</span><span class="sxs-lookup"><span data-stu-id="fab99-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="fab99-124">Nella finestra **Lista vendite**, selezionare l'ordine di vendita che è stato preparato nella sezione "Per creare un ordine di vendita per una spedizione diretta".</span><span class="sxs-lookup"><span data-stu-id="fab99-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="fab99-125">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="fab99-125">Choose the **OK** button.</span></span>

<span data-ttu-id="fab99-126">Le informazioni di riga dall'ordine di vendita vengono inserite nelle righe dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="fab99-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="fab99-127">È possibile istruire il fornitore di spedire gli articoli al cliente, ad esempio spedendo l'ordine di acquisto come PDF.</span><span class="sxs-lookup"><span data-stu-id="fab99-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="fab99-128">Per visualizzare l'ordine di acquisto collegato dall'ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="fab99-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="fab99-129">Selezionare la riga dell'ordine di vendita con spedizione diretta, scegliere l'azione **Ordine**, scegliere l'azione **Spedizione diretta** e quindi scegliere l'azione **Ordine acquisto**.</span><span class="sxs-lookup"><span data-stu-id="fab99-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="fab99-130">Per registrare una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="fab99-130">To post a drop shipment</span></span>
<span data-ttu-id="fab99-131">Dopo che il fornitore ha spedito gli articoli, è possibile registrare l'ordine di vendita come spedito.</span><span class="sxs-lookup"><span data-stu-id="fab99-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="fab99-132">È possibile registrare anche l'ordine di acquisto, ma solo con l'opzione **Ricevi** finché l'ordine di vendita non viene fatturato.</span><span class="sxs-lookup"><span data-stu-id="fab99-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="fab99-133">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di vendita**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fab99-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="fab99-134">Aprire l'ordine di vendita creato nella sezione "Per creare un ordine di vendita per una spedizione diretta".</span><span class="sxs-lookup"><span data-stu-id="fab99-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="fab99-135">Nel campo **Qtà da spedire**, specificare la quantità dell'ordine da spedire, la quantità dell'ordine completa o parziale.</span><span class="sxs-lookup"><span data-stu-id="fab99-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="fab99-136">Scegliere l'azione **Registra** o **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="fab99-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="fab99-137">Selezionare l'opzione **Spedizione** per fatturare in seguito oppure l'opzione **Spedisci e fattura** per fatturare immediatamente.</span><span class="sxs-lookup"><span data-stu-id="fab99-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="fab99-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fab99-138">See Also</span></span>
<span data-ttu-id="fab99-139">[Procedura: Creare ordini speciali](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="fab99-139">[How to: Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="fab99-140">Procedura: Vendere prodotti</span><span class="sxs-lookup"><span data-stu-id="fab99-140">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="fab99-141">Procedura: Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="fab99-141">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="fab99-142">Vendite</span><span class="sxs-lookup"><span data-stu-id="fab99-142">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="fab99-143">Magazzino</span><span class="sxs-lookup"><span data-stu-id="fab99-143">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="fab99-144">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fab99-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

