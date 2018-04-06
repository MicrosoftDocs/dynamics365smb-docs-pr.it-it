---
title: 'Procedura: Cumulare i carichi | Documenti Microsoft'
description: "Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione Cumula carichi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2176baf2947a08785fdf6327b2ebebf35686d04a
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="8e734-103">Combinare i carichi in una singola fattura</span><span class="sxs-lookup"><span data-stu-id="8e734-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="8e734-104">Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione **Cumula carichi**.</span><span class="sxs-lookup"><span data-stu-id="8e734-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="8e734-105">Prima di creare un carico di acquisto cumulato, è necessario che venga registrato più di un carico per lo stesso fornitore nella stessa valuta.</span><span class="sxs-lookup"><span data-stu-id="8e734-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="8e734-106">In altri termini, è necessario compilare due o più ordini di acquisto e registrarli come ricevuti, ma non fatturati.</span><span class="sxs-lookup"><span data-stu-id="8e734-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="8e734-107">Quando i carichi di acquisto vengono cumulati in una fattura e registrati, viene creata una fattura di acquisto registrata per le righe fatturate.</span><span class="sxs-lookup"><span data-stu-id="8e734-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="8e734-108">Il campo **Quantità fatturata** dell'ordine di acquisto o dell'ordine di acquisto programmato di origine viene aggiornato in base alla quantità fatturata.</span><span class="sxs-lookup"><span data-stu-id="8e734-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="8e734-109">Tuttavia, il documento di acquisto originale non viene eliminato, anche se è stato completamente ricevuto e fatturato; è necessario quindi eliminare il documento di acquisto manualmente.</span><span class="sxs-lookup"><span data-stu-id="8e734-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="8e734-110">Per cumulare i carichi</span><span class="sxs-lookup"><span data-stu-id="8e734-110">To combine receipts</span></span>  
1. <span data-ttu-id="8e734-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture di acquisto**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8e734-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8e734-112">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="8e734-112">Choose the **New** action.</span></span> <span data-ttu-id="8e734-113">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="8e734-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="8e734-114">Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di carico**.</span><span class="sxs-lookup"><span data-stu-id="8e734-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="8e734-115">Selezionare più righe di carico che si desidera includere nella fattura.</span><span class="sxs-lookup"><span data-stu-id="8e734-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="8e734-116">Se è stata selezionata una riga di carico non corretta o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura di acquisto ed eseguire nuovamente la funzione **Prendi righe di carico**.</span><span class="sxs-lookup"><span data-stu-id="8e734-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="8e734-117">Per registrare la fattura scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="8e734-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="8e734-118">Per rimuovere ordini di acquisto aperti dopo la registrazione del carico cumulativa</span><span class="sxs-lookup"><span data-stu-id="8e734-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="8e734-119">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Elimina ordini acquisto fatturati**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8e734-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="8e734-120">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="8e734-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="8e734-121">.</span><span class="sxs-lookup"><span data-stu-id="8e734-121">.</span></span>
3. <span data-ttu-id="8e734-122">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e734-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="8e734-123">In alternativa, eliminare i singoli ordini manualmente.</span><span class="sxs-lookup"><span data-stu-id="8e734-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="8e734-124">Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di acquisto programmati.</span><span class="sxs-lookup"><span data-stu-id="8e734-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e734-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e734-125">See Also</span></span>  
[<span data-ttu-id="8e734-126">Acquisti</span><span class="sxs-lookup"><span data-stu-id="8e734-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8e734-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8e734-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

