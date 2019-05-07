---
title: 'Procedura: Cumulare i carichi | Documenti Microsoft'
description: Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione Cumula carichi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5e1b04cc998319cc835b5dcc1547723c48be6763
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "926869"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="8e99c-103">Combinare i carichi in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="8e99c-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="8e99c-104">Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione **Cumula carichi**.</span><span class="sxs-lookup"><span data-stu-id="8e99c-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="8e99c-105">Prima di creare un carico di acquisto cumulato, è necessario che venga registrato più di un carico per lo stesso fornitore nella stessa valuta.</span><span class="sxs-lookup"><span data-stu-id="8e99c-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="8e99c-106">In altri termini, è necessario compilare due o più ordini di acquisto e registrarli come ricevuti, ma non fatturati.</span><span class="sxs-lookup"><span data-stu-id="8e99c-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="8e99c-107">Quando i carichi di acquisto vengono cumulati in una fattura e registrati, viene creata una fattura di acquisto registrata per le righe fatturate.</span><span class="sxs-lookup"><span data-stu-id="8e99c-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="8e99c-108">Il campo **Quantità fatturata** dell'ordine di acquisto o dell'ordine di acquisto programmato di origine viene aggiornato in base alla quantità fatturata.</span><span class="sxs-lookup"><span data-stu-id="8e99c-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="8e99c-109">Tuttavia, il documento di acquisto originale non viene eliminato, anche se è stato completamente ricevuto e fatturato; è necessario quindi eliminare il documento di acquisto manualmente.</span><span class="sxs-lookup"><span data-stu-id="8e99c-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="8e99c-110">Per cumulare i carichi</span><span class="sxs-lookup"><span data-stu-id="8e99c-110">To combine receipts</span></span>  
1. <span data-ttu-id="8e99c-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture di acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8e99c-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8e99c-112">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="8e99c-112">Choose the **New** action.</span></span> <span data-ttu-id="8e99c-113">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="8e99c-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="8e99c-114">Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di carico**.</span><span class="sxs-lookup"><span data-stu-id="8e99c-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="8e99c-115">Selezionare più righe di carico che si desidera includere nella fattura.</span><span class="sxs-lookup"><span data-stu-id="8e99c-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="8e99c-116">Se è stata selezionata una riga di carico non corretta o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura di acquisto ed eseguire nuovamente la funzione **Prendi righe di carico**.</span><span class="sxs-lookup"><span data-stu-id="8e99c-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="8e99c-117">Per registrare la fattura scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="8e99c-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="8e99c-118">Per rimuovere ordini di acquisto aperti dopo la registrazione del carico cumulativa</span><span class="sxs-lookup"><span data-stu-id="8e99c-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="8e99c-119">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina ordini acquisto fatturati** e quindi selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8e99c-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="8e99c-120">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="8e99c-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="8e99c-121">.</span><span class="sxs-lookup"><span data-stu-id="8e99c-121">.</span></span>
3. <span data-ttu-id="8e99c-122">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e99c-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="8e99c-123">In alternativa, eliminare i singoli ordini manualmente.</span><span class="sxs-lookup"><span data-stu-id="8e99c-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="8e99c-124">Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di acquisto programmati.</span><span class="sxs-lookup"><span data-stu-id="8e99c-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e99c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e99c-125">See Also</span></span>  
[<span data-ttu-id="8e99c-126">Acquisti</span><span class="sxs-lookup"><span data-stu-id="8e99c-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8e99c-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8e99c-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
