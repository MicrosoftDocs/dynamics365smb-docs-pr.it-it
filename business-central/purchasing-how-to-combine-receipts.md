---
title: 'Procedura: Cumulare i carichi | Documenti Microsoft'
description: Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione Cumula carichi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/02/2020
ms.author: sgroespe
ms.openlocfilehash: f5b3c47ab430b89c2f747f73bc427e045a902992
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534673"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="02d03-103">Combinare i carichi in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="02d03-103">Combine Receipts on a Single Invoice</span></span>

<span data-ttu-id="02d03-104">Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione **Cumula carichi**.</span><span class="sxs-lookup"><span data-stu-id="02d03-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="02d03-105">Prima di creare un carico di acquisto cumulato, è necessario che venga registrato più di un carico per lo stesso fornitore nella stessa valuta.</span><span class="sxs-lookup"><span data-stu-id="02d03-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="02d03-106">In altri termini, è necessario compilare due o più ordini di acquisto e registrarli come ricevuti, ma non fatturati.</span><span class="sxs-lookup"><span data-stu-id="02d03-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="02d03-107">Quando i carichi di acquisto vengono cumulati in una fattura e registrati, viene creata una fattura di acquisto registrata per le righe fatturate.</span><span class="sxs-lookup"><span data-stu-id="02d03-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="02d03-108">Il campo **Quantità fatturata** dell'ordine di acquisto o dell'ordine di acquisto programmato di origine viene aggiornato in base alla quantità fatturata.</span><span class="sxs-lookup"><span data-stu-id="02d03-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="02d03-109">Tuttavia, il documento di acquisto originale non viene eliminato, anche se è stato completamente ricevuto e fatturato; è necessario quindi eliminare il documento di acquisto manualmente.</span><span class="sxs-lookup"><span data-stu-id="02d03-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

> [!NOTE]
> <span data-ttu-id="02d03-110">La fattura di acquisto risultante non può essere successivamente corretta o annullata.</span><span class="sxs-lookup"><span data-stu-id="02d03-110">The resulting purchase invoice cannot later be corrected or canceled.</span></span> <span data-ttu-id="02d03-111">Se si desidera modificare una fattura di acquisto creata in questo modo, è necessario utilizzare le note di credito di acquisto.</span><span class="sxs-lookup"><span data-stu-id="02d03-111">If you want to modify a purchase invoice that is created in this way, you must use purchase credit memos.</span></span> <span data-ttu-id="02d03-112">Per ulteriori informazioni, vedere [Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="02d03-112">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span>

## <a name="to-combine-receipts"></a><span data-ttu-id="02d03-113">Per cumulare i carichi</span><span class="sxs-lookup"><span data-stu-id="02d03-113">To combine receipts</span></span>

1. <span data-ttu-id="02d03-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="02d03-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="02d03-115">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="02d03-115">Choose the **New** action.</span></span> <span data-ttu-id="02d03-116">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="02d03-116">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="02d03-117">Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di carico**.</span><span class="sxs-lookup"><span data-stu-id="02d03-117">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="02d03-118">Selezionare più righe di carico che si desidera includere nella fattura.</span><span class="sxs-lookup"><span data-stu-id="02d03-118">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="02d03-119">Se è stata selezionata una riga di carico non corretta o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura di acquisto ed eseguire nuovamente la funzione **Prendi righe di carico**.</span><span class="sxs-lookup"><span data-stu-id="02d03-119">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="02d03-120">Per registrare la fattura scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="02d03-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="02d03-121">Per rimuovere ordini di acquisto aperti dopo la registrazione del carico cumulativa</span><span class="sxs-lookup"><span data-stu-id="02d03-121">To remove open purchase orders after combined receipt posting</span></span>

1. <span data-ttu-id="02d03-122">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina ordini acquisto fatturati** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="02d03-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="02d03-123">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="02d03-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="02d03-124">.</span><span class="sxs-lookup"><span data-stu-id="02d03-124">.</span></span>
3. <span data-ttu-id="02d03-125">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="02d03-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="02d03-126">In alternativa, eliminare i singoli ordini manualmente.</span><span class="sxs-lookup"><span data-stu-id="02d03-126">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="02d03-127">Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di acquisto programmati.</span><span class="sxs-lookup"><span data-stu-id="02d03-127">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="02d03-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="02d03-128">See Also</span></span>

[<span data-ttu-id="02d03-129">Acquisti</span><span class="sxs-lookup"><span data-stu-id="02d03-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="02d03-130">Correggere o annullare le fatture di acquisto non pagate</span><span class="sxs-lookup"><span data-stu-id="02d03-130">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
<span data-ttu-id="02d03-131">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02d03-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
