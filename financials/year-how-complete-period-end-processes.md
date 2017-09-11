---
title: "Attività facoltative per periodi di chiusura | Documenti Microsoft"
description: "In questo argomento vengono descritti i processi e le attività facoltativi per la chiusura dei periodi contabili in Financials."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="86e2b-103">Panoramica delle attività per la chiusura dei periodi contabili</span><span class="sxs-lookup"><span data-stu-id="86e2b-103">Overview of Tasks to Close Accounting Periods</span></span>
<span data-ttu-id="86e2b-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] non è obbligatorio chiudere i periodi, tuttavia, vi sono numerose attività di chiusura del periodo (chiusura del mese) che è possibile svolgere.</span><span class="sxs-lookup"><span data-stu-id="86e2b-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="86e2b-105">In questo argomento viene fornita una sintesi dei processi e delle attività facoltativi per periodi di chiusura.</span><span class="sxs-lookup"><span data-stu-id="86e2b-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="86e2b-106">Contabilità generale</span><span class="sxs-lookup"><span data-stu-id="86e2b-106">General Ledger</span></span>
* <span data-ttu-id="86e2b-107">Specificare periodi di registrazione a livello di sistema e specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="86e2b-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="86e2b-108">Ciò specifica le date tra le quali è ammessa la registrazione.</span><span class="sxs-lookup"><span data-stu-id="86e2b-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="86e2b-109">In base alle esigenze aziendali, è possibile consentire la registrazione all'inizio del periodo o verso la chiusura.</span><span class="sxs-lookup"><span data-stu-id="86e2b-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="86e2b-110">Per ulteriori informazioni, vedere [Procedura: Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="86e2b-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="86e2b-111">Apportare tutte le rettifiche C/G necessarie.</span><span class="sxs-lookup"><span data-stu-id="86e2b-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="86e2b-112">Aggiornare e contabilizzare le registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="86e2b-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="86e2b-113">Eseguire le situazioni contabili come segue:</span><span class="sxs-lookup"><span data-stu-id="86e2b-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="86e2b-114">Aprire la finestra **Situazione contabile** e quindi scegliere l'azione **Stampa**.</span><span class="sxs-lookup"><span data-stu-id="86e2b-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="86e2b-115">Contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="86e2b-115">Sales and Receivables</span></span>
* <span data-ttu-id="86e2b-116">Registrare tutti gli ordini di vendita, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="86e2b-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="86e2b-117">Contabilizzare tutte le registrazioni incassi.</span><span class="sxs-lookup"><span data-stu-id="86e2b-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="86e2b-118">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità clienti.</span><span class="sxs-lookup"><span data-stu-id="86e2b-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="86e2b-119">Riconciliare i crediti v/clienti nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="86e2b-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="86e2b-120">Eseguire il processo batch **Elimina ord. vendita fatturati**.</span><span class="sxs-lookup"><span data-stu-id="86e2b-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="86e2b-121">Contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="86e2b-121">Purchases and Payables</span></span>
* <span data-ttu-id="86e2b-122">Contabilizzare tutti gli ordini di acquisto, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="86e2b-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="86e2b-123">Contabilizzare tutte le registrazioni pagamenti.</span><span class="sxs-lookup"><span data-stu-id="86e2b-123">Post all payment journals.</span></span>  
* <span data-ttu-id="86e2b-124">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità fornitori.</span><span class="sxs-lookup"><span data-stu-id="86e2b-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="86e2b-125">Eseguire il report **Scadenziario fornitori** e riconciliare i debiti v/fornitori nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="86e2b-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="86e2b-126">Eseguire il processo batch **Elimina ordini acquisto fatturati**.</span><span class="sxs-lookup"><span data-stu-id="86e2b-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="86e2b-127">Calcolare ed elaborare l'imposta di vendita.</span><span class="sxs-lookup"><span data-stu-id="86e2b-127">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="86e2b-128">Completare le dichiarazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="86e2b-128">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="86e2b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86e2b-129">See Also</span></span>
[<span data-ttu-id="86e2b-130">Chiusura di anni e periodi</span><span class="sxs-lookup"><span data-stu-id="86e2b-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="86e2b-131">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="86e2b-131">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="86e2b-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="86e2b-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

