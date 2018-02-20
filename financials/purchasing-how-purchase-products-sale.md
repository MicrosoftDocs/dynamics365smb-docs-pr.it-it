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
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 67e76ea76267c001277be3203c28103c3acb3214
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="purchase-items-for-a-sale"></a><span data-ttu-id="2c2aa-103">Acquistare articoli per una vendita</span><span class="sxs-lookup"><span data-stu-id="2c2aa-103">Purchase Items for a Sale</span></span>
<span data-ttu-id="2c2aa-104">Dagli ordini di vendita e dalle fatture di vendita, è possibile utilizzare funzioni per creare rapidamente i documenti di acquisto relativi alle quantità mancanti di articoli che sono necessari per la vendita.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="2c2aa-105">È possibile utilizzare due funzioni diverse che variano a seconda del tipo documento.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="2c2aa-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="2c2aa-106">Function</span></span>|<span data-ttu-id="2c2aa-107">Description</span><span class="sxs-lookup"><span data-stu-id="2c2aa-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="2c2aa-108">**Crea ordini di acquisto**</span><span class="sxs-lookup"><span data-stu-id="2c2aa-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="2c2aa-109">Da un ordine di vendita, questa funzione crea un ordine di acquisto per ciascun fornitore di articoli nell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="2c2aa-110">È possibile modificare la quantità di acquisto prima di creare gli ordini di acquisto.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="2c2aa-111">Vengono suggerite solo le quantità di vendita non disponibili.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="2c2aa-112">**Crea fattura di acquisto**</span><span class="sxs-lookup"><span data-stu-id="2c2aa-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="2c2aa-113">Da un ordine di vendita e da una fattura di vendita, questa funzione crea una fattura di acquisto per un fornitore selezionato per tutte le righe o per le righe selezionate nel documento di vendita.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="2c2aa-114">Viene suggerita la quantità di vendita completa.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="2c2aa-115">Per creare uno o più ordini di acquisto da un ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="2c2aa-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="2c2aa-116">Per creare un ordine di acquisto per ogni quantità articolo non disponibile nell'ordine di vendita, è possibile utilizzare la funzione **Crea ordini di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span>

1. <span data-ttu-id="2c2aa-117">Nella home page, selezionare la sezione **Ordini di vendita in corso**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-117">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="2c2aa-118">Aprire un ordine di vendita per cui si desidera acquistare degli articoli.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-118">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="2c2aa-119">Scegliere l'azione **Crea ordini di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-119">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="2c2aa-120">Viene visualizzata la finestra **Crea ordini di acquisto** in cui viene mostrata una riga per ogni articolo differente nell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-120">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="2c2aa-121">Vengono visualizzate per impostazione predefinita le righe per entrambe le quantità di vendita disponibili e non disponibili (in grigio).</span><span class="sxs-lookup"><span data-stu-id="2c2aa-121">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="2c2aa-122">È possibile scegliere l'azione **Mostra non disponibili** per visualizzare solo le righe relative alle quantità di vendita non disponibili.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-122">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="2c2aa-123">Il campo **Quantità da acquistare** contiene la quantità di vendita non disponibile per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-123">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="2c2aa-124">Per effettuare un acquisto di una quantità diversa dalla quantità di vendita non disponibile, modificare il valore nel campo **Quantità da acquistare**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-124">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="2c2aa-125">È possibile modificare anche il campo **Quantità da acquistare** nelle righe inattive anche se rappresentano le quantità di vendita completamente disponibili.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-125">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="2c2aa-126">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-126">Choose the **OK** button.</span></span>

    <span data-ttu-id="2c2aa-127">Un ordine di acquisto viene creato per ciascun fornitore di articoli nell'ordine di vendita, inclusa qualsiasi modifica delle quantità effettuata nella finestra **Crea ordini di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-127">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="2c2aa-128">Continuare a elaborare l'ordine o gli ordini di acquisto, ad esempio, modificando o aggiungendo altre righe all'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-128">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="2c2aa-129">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="2c2aa-129">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="2c2aa-130">Per creare una fattura di acquisto da un ordine o una fattura di vendita</span><span class="sxs-lookup"><span data-stu-id="2c2aa-130">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="2c2aa-131">Per creare un'unica fattura di acquisto per una o più righe di un documento di vendita selezionando prima il fornitore da cui effettuare l'acquisto, utilizzare la funzione **Crea fattura di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-131">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2c2aa-132">Questa funzione crea una fattura di acquisto per la quantità articolo esatta nel documento di vendita selezionato.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-132">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="2c2aa-133">Per modificare la quantità di acquisto, è necessario modificare la fattura di acquisto dopo che è stata creata.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-133">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="2c2aa-134">Nella home page, selezionare la sezione **Fatture vendita in corso**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-134">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="2c2aa-135">Aprire una fattura di vendita per cui si desidera acquistare degli articoli.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-135">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="2c2aa-136">Selezionare una o più righe della fattura di vendita da utilizzare nella fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-136">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="2c2aa-137">Per utilizzare tutte le righe della fattura di vendita, selezionarle tutte o non selezionarne alcuna.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-137">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="2c2aa-138">Scegliere l'azione **Crea fattura di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-138">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="2c2aa-139">Selezionare **Tutte le righe** o **Righe selezionate**, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-139">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="2c2aa-140">Nell'elenco di fornitori che viene visualizzato, selezionare il fornitore da cui si desidera acquistare tutti gli articoli e scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-140">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2c2aa-141">Viene creata una fattura d'acquisto che contiene una, più o tutte le righe nella fattura di vendita.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-141">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="2c2aa-142">Continuare a elaborare la fattura di acquisto, ad esempio, modificando o aggiungendo altre righe alla fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="2c2aa-142">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="2c2aa-143">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="2c2aa-143">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c2aa-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c2aa-144">See Also</span></span>
[<span data-ttu-id="2c2aa-145">Acquisti</span><span class="sxs-lookup"><span data-stu-id="2c2aa-145">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="2c2aa-146">Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="2c2aa-146">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="2c2aa-147">Fatturare le vendite</span><span class="sxs-lookup"><span data-stu-id="2c2aa-147">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="2c2aa-148">Registrare nuovi fornitori</span><span class="sxs-lookup"><span data-stu-id="2c2aa-148">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="2c2aa-149">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c2aa-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

