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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 50198afaa8caae9a11a06a25357fa94ad26b0b8f
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943187"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="5b526-103">Effettuare spedizioni dirette</span><span class="sxs-lookup"><span data-stu-id="5b526-103">Make Drop Shipments</span></span>
<span data-ttu-id="5b526-104">Una spedizione diretta è costituita dalla spedizione di articoli direttamente da un fornitore a un cliente.</span><span class="sxs-lookup"><span data-stu-id="5b526-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="5b526-105">Quando un ordine cliente è contrassegnato per la spedizione di consegna e si crea un ordine d'acquisto specificando il cliente nel campo **Spedire a** **Indirizzo cliente**, è possibile collegare i due documenti e quindi istruire il fornitore spedire direttamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="5b526-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="5b526-106">Per creare un ordine di vendita per una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="5b526-106">To create a sales order for drop shipment</span></span>
<span data-ttu-id="5b526-107">Per preparare una spedizione diretta, si crea un ordine di vendita per un articolo come al solito, ad eccezione del fatto che è necessario indicare sulla riga di vendita che la vendita richiede la spedizione diretta.</span><span class="sxs-lookup"><span data-stu-id="5b526-107">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="5b526-108">Creare un ordine cliente per un articolo.</span><span class="sxs-lookup"><span data-stu-id="5b526-108">Create a sales order for an item.</span></span> <span data-ttu-id="5b526-109">Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="5b526-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="5b526-110">Nella riga ordine di vendita per la spedizione diretta selezionare la casella di controllo **Spedizione diretta**.</span><span class="sxs-lookup"><span data-stu-id="5b526-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="5b526-111">Utilizzare la funzione **Scegli colonne** se il campo non è visualizzato.</span><span class="sxs-lookup"><span data-stu-id="5b526-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="5b526-112">Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="5b526-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="5b526-113">Per creare l'ordine di acquisto per la spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="5b526-113">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="5b526-114">Per preparare una spedizione diretta per l'articolo da vendere, si crea un ordine di acquisto come al solito, ad eccezione del fatto che è necessario indicare nell'ordine di acquisto che deve essere spedito al cliente e non a se stessi.</span><span class="sxs-lookup"><span data-stu-id="5b526-114">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="5b526-115">Creare un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="5b526-115">Create a purchase order.</span></span> <span data-ttu-id="5b526-116">Non compilare i campi nelle righe.</span><span class="sxs-lookup"><span data-stu-id="5b526-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="5b526-117">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="5b526-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="5b526-118">Nel campo **Spedire a**, selezionare **Indirizzo cliente**.</span><span class="sxs-lookup"><span data-stu-id="5b526-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="5b526-119">Nel campo **Cliente**, selezionare il cliente a cui si sta vendendo.</span><span class="sxs-lookup"><span data-stu-id="5b526-119">In the **Customer** field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="5b526-120">Scegliere l'azione **Spedizioni dirette** e scegliere l'azione **Ottieni ordini vendite**.</span><span class="sxs-lookup"><span data-stu-id="5b526-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="5b526-121">Nella pagina **Lista vendite**, selezionare l'ordine di vendita che è stato preparato nella sezione [Per creare un ordine di vendita per una spedizione diretta](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="5b526-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="5b526-122">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b526-122">Choose the **OK** button.</span></span>

<span data-ttu-id="5b526-123">Le informazioni di riga dall'ordine di vendita vengono inserite nelle righe dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="5b526-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="5b526-124">È possibile istruire il fornitore di spedire gli articoli al cliente, ad esempio spedendo l'ordine di acquisto come PDF.</span><span class="sxs-lookup"><span data-stu-id="5b526-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="5b526-125">Per visualizzare l'ordine di acquisto collegato dall'ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="5b526-125">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="5b526-126">Selezionare la riga dell'ordine di vendita con spedizione diretta, scegliere l'azione **Ordine**, scegliere l'azione **Spedizione diretta** e quindi scegliere l'azione **Ordine acquisto**.</span><span class="sxs-lookup"><span data-stu-id="5b526-126">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="5b526-127">Per registrare una spedizione diretta</span><span class="sxs-lookup"><span data-stu-id="5b526-127">To post a drop shipment</span></span>
<span data-ttu-id="5b526-128">Dopo che il fornitore ha spedito gli articoli, è possibile registrare l'ordine di vendita come spedito.</span><span class="sxs-lookup"><span data-stu-id="5b526-128">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="5b526-129">È possibile registrare anche l'ordine di acquisto, ma solo con l'opzione **Ricevi** finché l'ordine di vendita non viene fatturato.</span><span class="sxs-lookup"><span data-stu-id="5b526-129">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="5b526-130">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="5b526-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5b526-131">Aprire l'ordine di vendita creato nella sezione [Per creare un ordine di vendita per una spedizione diretta]().</span><span class="sxs-lookup"><span data-stu-id="5b526-131">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="5b526-132">Nel campo **Qtà da spedire**, specificare la quantità dell'ordine da spedire, la quantità dell'ordine completa o parziale.</span><span class="sxs-lookup"><span data-stu-id="5b526-132">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="5b526-133">Scegliere l'azione **Registra** o **Registra e invia**.</span><span class="sxs-lookup"><span data-stu-id="5b526-133">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="5b526-134">Selezionare l'opzione **Spedizione** per fatturare in seguito oppure l'opzione **Spedisci e fattura** per fatturare immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5b526-134">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b526-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b526-135">See Also</span></span>
[<span data-ttu-id="5b526-136">Creare ordini speciali</span><span class="sxs-lookup"><span data-stu-id="5b526-136">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="5b526-137">Acquistare articoli per una vendita</span><span class="sxs-lookup"><span data-stu-id="5b526-137">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="5b526-138">Vendere prodotti</span><span class="sxs-lookup"><span data-stu-id="5b526-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="5b526-139">Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="5b526-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="5b526-140">Vendite</span><span class="sxs-lookup"><span data-stu-id="5b526-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5b526-141">Magazzino</span><span class="sxs-lookup"><span data-stu-id="5b526-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5b526-142">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5b526-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
