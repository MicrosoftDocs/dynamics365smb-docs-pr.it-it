---
title: Correggere o annullare le fatture di acquisto non pagate | Documenti Microsoft
description: Descrive come correggere o annullare una fattura di acquisto registrata e creare automaticamente una nota di credito di acquisto.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 75a56e6089567c456280b2cc287dda62fb4f3f8b
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="0aa24-103">Procedura: Correggere o annullare le fatture di acquisto non pagate</span><span class="sxs-lookup"><span data-stu-id="0aa24-103">How to: Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="0aa24-104">È possibile correggere o annullare una fattura di acquisto registrata.</span><span class="sxs-lookup"><span data-stu-id="0aa24-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="0aa24-105">Ciò risulta utile se si desidera correggere un errore di digitazione o se si desidera modificare l'acquisto in una fase iniziale dell'elaborazione dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="0aa24-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="0aa24-106">Se è già stato eseguito il pagamento dei prodotti nella fattura di acquisto registrata, non è possibile correggerli o annullarli dalla fattura di acquisto registrata.</span><span class="sxs-lookup"><span data-stu-id="0aa24-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="0aa24-107">In alternativa, è necessario creare manualmente una nota di credito di acquisto per stornare l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="0aa24-107">Instead, you must manually create a purchase credit memo to reverse the purchase.</span></span> <span data-ttu-id="0aa24-108">Per ulteriori informazioni vedere [Procedura: Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="0aa24-108">For more information, see [How to: Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="0aa24-109">Nella finestra **Fattura acquisto registrata** è possibile scegliere il pulsante **Rettifica** o il pulsante **Annulla**.</span><span class="sxs-lookup"><span data-stu-id="0aa24-109">In the **Posted Purchase Invoice** window, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="0aa24-110">Quando si rettifica o si annulla una fattura di acquisto registrata, la nota di credito di acquisto viene applicata a tutti i movimenti contabili generali e di inventario creati quando la fattura di acquisto iniziale è stata registrata.</span><span class="sxs-lookup"><span data-stu-id="0aa24-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="0aa24-111">Ciò consente di stornare la fattura di acquisto nei record finanziari e lascia la nota di credito di acquisto registrata correttiva per l'audit trail.</span><span class="sxs-lookup"><span data-stu-id="0aa24-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="0aa24-112">Di seguito viene descritto l'utilizzo di **Rettifica** e di **Annulla**.</span><span class="sxs-lookup"><span data-stu-id="0aa24-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="0aa24-113">Per correggere una fattura di acquisto registrata</span><span class="sxs-lookup"><span data-stu-id="0aa24-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="0aa24-114">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di acquisto registrate**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0aa24-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aa24-115">Selezionare la fattura di acquisto che si desidera rettificare.</span><span class="sxs-lookup"><span data-stu-id="0aa24-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="0aa24-116">Se viene selezionata la casella di controllo **Annullata**, non è possibile rettificare la fattura di acquisto registrata poiché è già stata rettificata o annullata.</span><span class="sxs-lookup"><span data-stu-id="0aa24-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="0aa24-117">Nella finestra **Fattura acquisto registrata** scegliere **Rettifica**.</span><span class="sxs-lookup"><span data-stu-id="0aa24-117">In the **Posted Purchase Invoice** window, choose **Correct**.</span></span>

    <span data-ttu-id="0aa24-118">Viene creata una nuova fattura di acquisto con le stesse informazioni in cui è possibile apportare la rettifica.</span><span class="sxs-lookup"><span data-stu-id="0aa24-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="0aa24-119">Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="0aa24-119">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="0aa24-120">Il campo **Annullato** nella fattura di acquisto registrata iniziale viene modificato in **Sì**.</span><span class="sxs-lookup"><span data-stu-id="0aa24-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="0aa24-121">Una nota di credito di acquisto viene automaticamente creata e registrata per annullare la fattura di acquisto registrata iniziale.</span><span class="sxs-lookup"><span data-stu-id="0aa24-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="0aa24-122">Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di acquisto registrata che annulla la fattura di acquisto registrata iniziale.</span><span class="sxs-lookup"><span data-stu-id="0aa24-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="0aa24-123">Per annullare una fattura di acquisto registrata</span><span class="sxs-lookup"><span data-stu-id="0aa24-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="0aa24-124">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di acquisto registrate**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0aa24-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aa24-125">Selezionare la fattura di acquisto che si desidera annullare.</span><span class="sxs-lookup"><span data-stu-id="0aa24-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="0aa24-126">Se viene selezionata la casella di controllo **Annullata**, non è possibile annullare la fattura di acquisto registrata poiché è già stata rettificata o annullata.</span><span class="sxs-lookup"><span data-stu-id="0aa24-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="0aa24-127">Nella finestra **Fattura acquisto registrata** scegliere **Annulla**.</span><span class="sxs-lookup"><span data-stu-id="0aa24-127">In the **Posted Purchase Invoice** window, choose **Cancel**.</span></span>

    <span data-ttu-id="0aa24-128">Una nota di credito di acquisto viene automaticamente creata e registrata per annullare la fattura di acquisto registrata iniziale.</span><span class="sxs-lookup"><span data-stu-id="0aa24-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="0aa24-129">Il campo **Annullato** nella fattura di acquisto registrata iniziale viene modificato in **Sì**.</span><span class="sxs-lookup"><span data-stu-id="0aa24-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="0aa24-130">Scegliere **Mostra nota credito di rettifica** per visualizzare la nota di credito di acquisto registrata che annulla la fattura di acquisto registrata iniziale.</span><span class="sxs-lookup"><span data-stu-id="0aa24-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="0aa24-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aa24-131">See Also</span></span>
[<span data-ttu-id="0aa24-132">Acquisti</span><span class="sxs-lookup"><span data-stu-id="0aa24-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="0aa24-133">Procedura: Registrare gli acquisti</span><span class="sxs-lookup"><span data-stu-id="0aa24-133">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="0aa24-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0aa24-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

