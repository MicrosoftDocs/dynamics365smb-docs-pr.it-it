---
title: Creare una fattura di acquisto da una fattura di vendita per acquistare gli articoli per una vendita | Documenti Microsoft
description: "Da una fattura di vendita, per acquistare prodotti, è possibile creare una fattura di acquisto per un fornitore."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a><span data-ttu-id="a0c5c-103">Procedura: Acquistare articoli per una vendita</span><span class="sxs-lookup"><span data-stu-id="a0c5c-103">How to: Purchase Items for a Sale</span></span>
<span data-ttu-id="a0c5c-104">Dagli ordini di vendita e dalle fatture di vendita, è possibile utilizzare funzioni per creare rapidamente i documenti di acquisto relativi alle quantità mancanti di articoli che sono necessari per la vendita.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="a0c5c-105">È possibile utilizzare due funzioni diverse che variano a seconda del tipo documento.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="a0c5c-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="a0c5c-106">Function</span></span>|<span data-ttu-id="a0c5c-107">Description</span><span class="sxs-lookup"><span data-stu-id="a0c5c-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="a0c5c-108">**Crea ordini di acquisto**</span><span class="sxs-lookup"><span data-stu-id="a0c5c-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="a0c5c-109">Da un ordine di vendita, questa funzione crea un ordine di acquisto per ciascun fornitore di articoli nell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="a0c5c-110">È possibile modificare la quantità di acquisto prima di creare gli ordini di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="a0c5c-111">Vengono suggerite solo le quantità di vendita non disponibili.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="a0c5c-112">**Crea fattura di acquisto**</span><span class="sxs-lookup"><span data-stu-id="a0c5c-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="a0c5c-113">Da un ordine di vendita e da una fattura di vendita, questa funzione crea una fattura di acquisto per un fornitore selezionato per tutte le righe o per le righe selezionate nel documento di vendita.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="a0c5c-114">Viene suggerita la quantità di vendita completa.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="a0c5c-115">Per creare uno o più ordini di acquisto da un ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="a0c5c-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="a0c5c-116">Per creare un ordine di acquisto per ogni quantità articolo non disponibile nell'ordine di vendita, è possibile utilizzare la funzione **Crea ordini di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="a0c5c-117">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-117">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="a0c5c-118">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="a0c5c-118">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

1. <span data-ttu-id="a0c5c-119">Nella home page, selezionare la sezione **Ordini di vendita in corso**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-119">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="a0c5c-120">Aprire un ordine di vendita per cui si desidera acquistare degli articoli.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-120">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="a0c5c-121">Scegliere l'azione **Crea ordini di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-121">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="a0c5c-122">Viene visualizzata la finestra **Crea ordini di acquisto** in cui viene mostrata una riga per ogni articolo differente nell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-122">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="a0c5c-123">Vengono visualizzate per impostazione predefinita le righe per entrambe le quantità di vendita disponibili e non disponibili (in grigio).</span><span class="sxs-lookup"><span data-stu-id="a0c5c-123">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="a0c5c-124">È possibile scegliere l'azione **Mostra non disponibili** per visualizzare solo le righe relative alle quantità di vendita non disponibili.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-124">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="a0c5c-125">Il campo **Quantità da acquistare** contiene la quantità di vendita non disponibile per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-125">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="a0c5c-126">Per effettuare un acquisto di una quantità diversa dalla quantità di vendita non disponibile, modificare il valore nel campo **Quantità da acquistare**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-126">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="a0c5c-127">È possibile modificare anche il campo **Quantità da acquistare** nelle righe inattive anche se rappresentano le quantità di vendita completamente disponibili.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-127">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="a0c5c-128">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-128">Choose the **OK** button.</span></span> 
    
    <span data-ttu-id="a0c5c-129">Un ordine di acquisto viene creato per ciascun fornitore di articoli nell'ordine di vendita, inclusa qualsiasi modifica delle quantità effettuata nella finestra **Crea ordini di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-129">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="a0c5c-130">Continuare a elaborare l'ordine o gli ordini di acquisto, ad esempio, modificando o aggiungendo altre righe all'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-130">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="a0c5c-131">Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="a0c5c-131">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="a0c5c-132">Per creare una fattura di acquisto da un ordine o una fattura di vendita</span><span class="sxs-lookup"><span data-stu-id="a0c5c-132">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="a0c5c-133">Per creare un'unica fattura di acquisto per una o più righe di un documento di vendita selezionando prima il fornitore da cui effettuare l'acquisto, utilizzare la funzione **Crea fattura di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-133">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="a0c5c-134">Questa funzione crea una fattura di acquisto per la quantità articolo esatta nel documento di vendita selezionato.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-134">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="a0c5c-135">Per modificare la quantità di acquisto, è necessario modificare la fattura di acquisto dopo che è stata creata.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-135">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="a0c5c-136">Nella home page, selezionare la sezione **Fatture vendita in corso**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-136">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="a0c5c-137">Aprire una fattura di vendita per cui si desidera acquistare degli articoli.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-137">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="a0c5c-138">Selezionare una o più righe della fattura di vendita da utilizzare nella fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-138">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="a0c5c-139">Per utilizzare tutte le righe della fattura di vendita, selezionarle tutte o non selezionarne alcuna.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-139">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="a0c5c-140">Scegliere l'azione **Crea fattura di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-140">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="a0c5c-141">Selezionare **Tutte le righe** o **Righe selezionate**, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-141">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="a0c5c-142">Nell'elenco di fornitori che viene visualizzato, selezionare il fornitore da cui si desidera acquistare tutti gli articoli e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-142">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="a0c5c-143">Viene creata una fattura d'acquisto che contiene una, più o tutte le righe nella fattura di vendita.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-143">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="a0c5c-144">Continuare a elaborare la fattura di acquisto, ad esempio, modificando o aggiungendo altre righe alla fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a0c5c-144">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="a0c5c-145">Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="a0c5c-145">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a0c5c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0c5c-146">See Also</span></span>
[<span data-ttu-id="a0c5c-147">Acquisti</span><span class="sxs-lookup"><span data-stu-id="a0c5c-147">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a0c5c-148">Procedura: Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="a0c5c-148">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="a0c5c-149">Procedura: Fatturare le vendite</span><span class="sxs-lookup"><span data-stu-id="a0c5c-149">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="a0c5c-150">Procedura: Registrare nuovi fornitori</span><span class="sxs-lookup"><span data-stu-id="a0c5c-150">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="a0c5c-151">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0c5c-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

