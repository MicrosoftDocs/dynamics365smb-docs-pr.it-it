---
title: Attività facoltative per periodi di chiusura | Documenti Microsoft
description: In questo argomento vengono descritti i processi e le attività facoltativi per la chiusura dei periodi contabili in Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6066d0ddcfc32520f56d053c9624e8c1d8e7505d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391026"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="4aab3-103">Panoramica delle attività per la chiusura dei periodi contabili</span><span class="sxs-lookup"><span data-stu-id="4aab3-103">Overview of Tasks to Close Accounting Periods</span></span>
<span data-ttu-id="4aab3-104">In [!INCLUDE[prod_short](includes/prod_short.md)] non è obbligatorio chiudere i periodi, tuttavia, vi sono numerose attività di chiusura del periodo (chiusura del mese) che è possibile svolgere.</span><span class="sxs-lookup"><span data-stu-id="4aab3-104">[!INCLUDE[prod_short](includes/prod_short.md)] does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="4aab3-105">In questo argomento viene fornita una sintesi dei processi e delle attività facoltativi per periodi di chiusura.</span><span class="sxs-lookup"><span data-stu-id="4aab3-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="4aab3-106">Contabilità generale</span><span class="sxs-lookup"><span data-stu-id="4aab3-106">General Ledger</span></span>
* <span data-ttu-id="4aab3-107">Specificare periodi di registrazione a livello di sistema e specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4aab3-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="4aab3-108">Ciò specifica le date tra le quali è ammessa la registrazione.</span><span class="sxs-lookup"><span data-stu-id="4aab3-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="4aab3-109">In base alle esigenze aziendali, è possibile consentire la registrazione all'inizio del periodo o verso la chiusura.</span><span class="sxs-lookup"><span data-stu-id="4aab3-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="4aab3-110">Per ulteriori informazioni, vedere [Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="4aab3-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="4aab3-111">Apportare tutte le rettifiche C/G necessarie.</span><span class="sxs-lookup"><span data-stu-id="4aab3-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="4aab3-112">Aggiornare e contabilizzare le registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="4aab3-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="4aab3-113">Eseguire le situazioni contabili come segue:</span><span class="sxs-lookup"><span data-stu-id="4aab3-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="4aab3-114">Aprire la pagina **Situazione contabile** e quindi scegliere l'azione **Stampa**.</span><span class="sxs-lookup"><span data-stu-id="4aab3-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="4aab3-115">Contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="4aab3-115">Sales and Receivables</span></span>
* <span data-ttu-id="4aab3-116">Registrare tutti gli ordini di vendita, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="4aab3-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="4aab3-117">Contabilizzare tutte le registrazioni incassi.</span><span class="sxs-lookup"><span data-stu-id="4aab3-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="4aab3-118">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità clienti.</span><span class="sxs-lookup"><span data-stu-id="4aab3-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="4aab3-119">Riconciliare i crediti v/clienti nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4aab3-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="4aab3-120">Eseguire il processo batch **Elimina ord. vendita fatturati**.</span><span class="sxs-lookup"><span data-stu-id="4aab3-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="4aab3-121">Contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="4aab3-121">Purchases and Payables</span></span>
* <span data-ttu-id="4aab3-122">Contabilizzare tutti gli ordini di acquisto, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="4aab3-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="4aab3-123">Contabilizzare tutte le registrazioni pagamenti.</span><span class="sxs-lookup"><span data-stu-id="4aab3-123">Post all payment journals.</span></span>  
* <span data-ttu-id="4aab3-124">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità fornitori.</span><span class="sxs-lookup"><span data-stu-id="4aab3-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="4aab3-125">Eseguire il report **Scadenziario fornitori** e riconciliare i debiti v/fornitori nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4aab3-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="4aab3-126">Eseguire il processo batch **Elimina ordini acquisto fatturati**.</span><span class="sxs-lookup"><span data-stu-id="4aab3-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="4aab3-127">Cespiti</span><span class="sxs-lookup"><span data-stu-id="4aab3-127">Fixed Assets</span></span>
* <span data-ttu-id="4aab3-128">Registrare tutti i costi di manutenzione che sono stati registrati tramite le registrazioni cespiti o le fatture.</span><span class="sxs-lookup"><span data-stu-id="4aab3-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="4aab3-129">Registrare le rettifiche.</span><span class="sxs-lookup"><span data-stu-id="4aab3-129">Post adjustments.</span></span>
* <span data-ttu-id="4aab3-130">Registrare la rivalutazione.</span><span class="sxs-lookup"><span data-stu-id="4aab3-130">Post appreciation.</span></span>
* <span data-ttu-id="4aab3-131">Registrare l'ammortamento.</span><span class="sxs-lookup"><span data-stu-id="4aab3-131">Post depreciation.</span></span>
* <span data-ttu-id="4aab3-132">Aggiornare e registrare le registrazioni periodiche cespiti.</span><span class="sxs-lookup"><span data-stu-id="4aab3-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="4aab3-133">Intercompany</span><span class="sxs-lookup"><span data-stu-id="4aab3-133">Intercompany</span></span>
* <span data-ttu-id="4aab3-134">Elaborare transazioni Intercompany</span><span class="sxs-lookup"><span data-stu-id="4aab3-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="4aab3-135">Calcolare ed elaborare l'imposta di vendita.</span><span class="sxs-lookup"><span data-stu-id="4aab3-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="4aab3-136">Completare le dichiarazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="4aab3-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4aab3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4aab3-137">See Also</span></span>
[<span data-ttu-id="4aab3-138">Chiusura di anni e periodi</span><span class="sxs-lookup"><span data-stu-id="4aab3-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="4aab3-139">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="4aab3-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="4aab3-140">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4aab3-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]