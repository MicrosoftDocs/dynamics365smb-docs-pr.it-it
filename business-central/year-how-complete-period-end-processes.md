---
title: Attività facoltative per periodi di chiusura | Documenti Microsoft
description: In questo argomento vengono descritti i processi e le attività facoltativi per la chiusura dei periodi contabili in Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 104f63e07e4bfd8945f73581a4fb7810f946304f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755569"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="e780c-103">Panoramica delle attività per la chiusura dei periodi contabili</span><span class="sxs-lookup"><span data-stu-id="e780c-103">Overview of Tasks to Close Accounting Periods</span></span>
<span data-ttu-id="e780c-104">In [!INCLUDE[prod_short](includes/prod_short.md)] non è obbligatorio chiudere i periodi, tuttavia, vi sono numerose attività di chiusura del periodo (chiusura del mese) che è possibile svolgere.</span><span class="sxs-lookup"><span data-stu-id="e780c-104">[!INCLUDE[prod_short](includes/prod_short.md)] does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="e780c-105">In questo argomento viene fornita una sintesi dei processi e delle attività facoltativi per periodi di chiusura.</span><span class="sxs-lookup"><span data-stu-id="e780c-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="e780c-106">Contabilità generale</span><span class="sxs-lookup"><span data-stu-id="e780c-106">General Ledger</span></span>
* <span data-ttu-id="e780c-107">Specificare periodi di registrazione a livello di sistema e specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e780c-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="e780c-108">Ciò specifica le date tra le quali è ammessa la registrazione.</span><span class="sxs-lookup"><span data-stu-id="e780c-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="e780c-109">In base alle esigenze aziendali, è possibile consentire la registrazione all'inizio del periodo o verso la chiusura.</span><span class="sxs-lookup"><span data-stu-id="e780c-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="e780c-110">Per ulteriori informazioni, vedere [Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="e780c-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="e780c-111">Apportare tutte le rettifiche C/G necessarie.</span><span class="sxs-lookup"><span data-stu-id="e780c-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="e780c-112">Aggiornare e contabilizzare le registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="e780c-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="e780c-113">Eseguire le situazioni contabili come segue:</span><span class="sxs-lookup"><span data-stu-id="e780c-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="e780c-114">Aprire la pagina **Situazione contabile** e quindi scegliere l'azione **Stampa**.</span><span class="sxs-lookup"><span data-stu-id="e780c-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="e780c-115">Contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="e780c-115">Sales and Receivables</span></span>
* <span data-ttu-id="e780c-116">Registrare tutti gli ordini di vendita, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="e780c-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="e780c-117">Contabilizzare tutte le registrazioni incassi.</span><span class="sxs-lookup"><span data-stu-id="e780c-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="e780c-118">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità clienti.</span><span class="sxs-lookup"><span data-stu-id="e780c-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="e780c-119">Riconciliare i crediti v/clienti nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e780c-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="e780c-120">Eseguire il processo batch **Elimina ord. vendita fatturati**.</span><span class="sxs-lookup"><span data-stu-id="e780c-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="e780c-121">Contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="e780c-121">Purchases and Payables</span></span>
* <span data-ttu-id="e780c-122">Contabilizzare tutti gli ordini di acquisto, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="e780c-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="e780c-123">Contabilizzare tutte le registrazioni pagamenti.</span><span class="sxs-lookup"><span data-stu-id="e780c-123">Post all payment journals.</span></span>  
* <span data-ttu-id="e780c-124">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità fornitori.</span><span class="sxs-lookup"><span data-stu-id="e780c-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="e780c-125">Eseguire il report **Scadenziario fornitori** e riconciliare i debiti v/fornitori nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="e780c-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="e780c-126">Eseguire il processo batch **Elimina ordini acquisto fatturati**.</span><span class="sxs-lookup"><span data-stu-id="e780c-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="e780c-127">Cespiti</span><span class="sxs-lookup"><span data-stu-id="e780c-127">Fixed Assets</span></span>
* <span data-ttu-id="e780c-128">Registrare tutti i costi di manutenzione che sono stati registrati tramite le registrazioni cespiti o le fatture.</span><span class="sxs-lookup"><span data-stu-id="e780c-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="e780c-129">Registrare le rettifiche.</span><span class="sxs-lookup"><span data-stu-id="e780c-129">Post adjustments.</span></span>
* <span data-ttu-id="e780c-130">Registrare la rivalutazione.</span><span class="sxs-lookup"><span data-stu-id="e780c-130">Post appreciation.</span></span>
* <span data-ttu-id="e780c-131">Registrare l'ammortamento.</span><span class="sxs-lookup"><span data-stu-id="e780c-131">Post depreciation.</span></span>
* <span data-ttu-id="e780c-132">Aggiornare e registrare le registrazioni periodiche cespiti.</span><span class="sxs-lookup"><span data-stu-id="e780c-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="e780c-133">Intercompany</span><span class="sxs-lookup"><span data-stu-id="e780c-133">Intercompany</span></span>
* <span data-ttu-id="e780c-134">Elaborare transazioni Intercompany</span><span class="sxs-lookup"><span data-stu-id="e780c-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="e780c-135">Calcolare ed elaborare l'imposta di vendita.</span><span class="sxs-lookup"><span data-stu-id="e780c-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="e780c-136">Completare le dichiarazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="e780c-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e780c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e780c-137">See Also</span></span>
[<span data-ttu-id="e780c-138">Chiusura di anni e periodi</span><span class="sxs-lookup"><span data-stu-id="e780c-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="e780c-139">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="e780c-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="e780c-140">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e780c-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
