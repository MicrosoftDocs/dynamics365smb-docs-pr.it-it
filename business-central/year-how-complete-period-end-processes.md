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
ms.openlocfilehash: 6526760c78cb11d8454b7f5390c6fefe713647d2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918240"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="7c637-103">Panoramica delle attività per la chiusura dei periodi contabili</span><span class="sxs-lookup"><span data-stu-id="7c637-103">Overview of Tasks to Close Accounting Periods</span></span>
<span data-ttu-id="7c637-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] non è obbligatorio chiudere i periodi, tuttavia, vi sono numerose attività di chiusura del periodo (chiusura del mese) che è possibile svolgere.</span><span class="sxs-lookup"><span data-stu-id="7c637-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="7c637-105">In questo argomento viene fornita una sintesi dei processi e delle attività facoltativi per periodi di chiusura.</span><span class="sxs-lookup"><span data-stu-id="7c637-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="7c637-106">Contabilità generale</span><span class="sxs-lookup"><span data-stu-id="7c637-106">General Ledger</span></span>
* <span data-ttu-id="7c637-107">Specificare periodi di registrazione a livello di sistema e specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7c637-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="7c637-108">Ciò specifica le date tra le quali è ammessa la registrazione.</span><span class="sxs-lookup"><span data-stu-id="7c637-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="7c637-109">In base alle esigenze aziendali, è possibile consentire la registrazione all'inizio del periodo o verso la chiusura.</span><span class="sxs-lookup"><span data-stu-id="7c637-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="7c637-110">Per ulteriori informazioni, vedere [Specificare i periodi di registrazione](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="7c637-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="7c637-111">Apportare tutte le rettifiche C/G necessarie.</span><span class="sxs-lookup"><span data-stu-id="7c637-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="7c637-112">Aggiornare e contabilizzare le registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="7c637-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="7c637-113">Eseguire le situazioni contabili come segue:</span><span class="sxs-lookup"><span data-stu-id="7c637-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="7c637-114">Aprire la pagina **Situazione contabile** e quindi scegliere l'azione **Stampa**.</span><span class="sxs-lookup"><span data-stu-id="7c637-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="7c637-115">Contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="7c637-115">Sales and Receivables</span></span>
* <span data-ttu-id="7c637-116">Registrare tutti gli ordini di vendita, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="7c637-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="7c637-117">Contabilizzare tutte le registrazioni incassi.</span><span class="sxs-lookup"><span data-stu-id="7c637-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="7c637-118">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità clienti.</span><span class="sxs-lookup"><span data-stu-id="7c637-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="7c637-119">Riconciliare i crediti v/clienti nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="7c637-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="7c637-120">Eseguire il processo batch **Elimina ord. vendita fatturati**.</span><span class="sxs-lookup"><span data-stu-id="7c637-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="7c637-121">Contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="7c637-121">Purchases and Payables</span></span>
* <span data-ttu-id="7c637-122">Contabilizzare tutti gli ordini di acquisto, le fatture, le note di credito e gli ordini di reso.</span><span class="sxs-lookup"><span data-stu-id="7c637-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="7c637-123">Contabilizzare tutte le registrazioni pagamenti.</span><span class="sxs-lookup"><span data-stu-id="7c637-123">Post all payment journals.</span></span>  
* <span data-ttu-id="7c637-124">Aggiornare e contabilizzare le registrazioni periodiche correlate alla contabilità fornitori.</span><span class="sxs-lookup"><span data-stu-id="7c637-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="7c637-125">Eseguire il report **Scadenziario fornitori** e riconciliare i debiti v/fornitori nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="7c637-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="7c637-126">Eseguire il processo batch **Elimina ordini acquisto fatturati**.</span><span class="sxs-lookup"><span data-stu-id="7c637-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="7c637-127">Cespiti</span><span class="sxs-lookup"><span data-stu-id="7c637-127">Fixed Assets</span></span>
* <span data-ttu-id="7c637-128">Registrare tutti i costi di manutenzione che sono stati registrati tramite le registrazioni cespiti o le fatture.</span><span class="sxs-lookup"><span data-stu-id="7c637-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="7c637-129">Registrare le rettifiche.</span><span class="sxs-lookup"><span data-stu-id="7c637-129">Post adjustments.</span></span>
* <span data-ttu-id="7c637-130">Registrare la rivalutazione.</span><span class="sxs-lookup"><span data-stu-id="7c637-130">Post appreciation.</span></span>
* <span data-ttu-id="7c637-131">Registrare l'ammortamento.</span><span class="sxs-lookup"><span data-stu-id="7c637-131">Post depreciation.</span></span>
* <span data-ttu-id="7c637-132">Aggiornare e registrare le registrazioni periodiche cespiti.</span><span class="sxs-lookup"><span data-stu-id="7c637-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="7c637-133">Intercompany</span><span class="sxs-lookup"><span data-stu-id="7c637-133">Intercompany</span></span>
* <span data-ttu-id="7c637-134">Elaborare transazioni Intercompany</span><span class="sxs-lookup"><span data-stu-id="7c637-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="7c637-135">Calcolare ed elaborare l'imposta di vendita.</span><span class="sxs-lookup"><span data-stu-id="7c637-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="7c637-136">Completare le dichiarazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="7c637-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c637-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c637-137">See Also</span></span>
[<span data-ttu-id="7c637-138">Chiusura di anni e periodi</span><span class="sxs-lookup"><span data-stu-id="7c637-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="7c637-139">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="7c637-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="7c637-140">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7c637-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
