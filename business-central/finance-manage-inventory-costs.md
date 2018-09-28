---
title: Gestione dei costi del magazzino | Microsoft Docs
description: La gestione dei costi, detta anche "costing", riguarda la registrazione e il reporting dei costi operativi business. Comprende inoltre il reporting dei costi di produzione e di magazzino, ovvero il valore degli articoli.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 088b8fdb11c32594499af752d5c6be652e2f69a6
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="33ca2-104">Gestione dei costi di magazzino</span><span class="sxs-lookup"><span data-stu-id="33ca2-104">Managing Inventory Costs</span></span>
<span data-ttu-id="33ca2-105">La gestione dei costi, detta anche "costing", riguarda la registrazione e il reporting dei costi operativi business.</span><span class="sxs-lookup"><span data-stu-id="33ca2-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="33ca2-106">Comprende inoltre il reporting dei costi di produzione e di magazzino, ovvero il valore degli articoli.</span><span class="sxs-lookup"><span data-stu-id="33ca2-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="33ca2-107">Di seguito sono elencati i principi fondamentali di questa materia: i metodi di costing definiscono il modo in cui gli articoli vengono valutati quando escono dal magazzino, la rettifica dei costi aggiorna il costo della merce venduta con costi di acquisto correlati registrati dopo la vendita e infine il valore di magazzino deve essere registrato in appositi conti C/G con periodicità regolare.</span><span class="sxs-lookup"><span data-stu-id="33ca2-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="33ca2-108">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="33ca2-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="33ca2-109">**Per**</span><span class="sxs-lookup"><span data-stu-id="33ca2-109">**To**</span></span>|<span data-ttu-id="33ca2-110">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="33ca2-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="33ca2-111">Leggere diverse informazioni concettuali per comprendere i principi alla base della funzionalità di costing di magazzino in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="33ca2-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>|[<span data-ttu-id="33ca2-112">Informazioni sul costing di magazzino</span><span class="sxs-lookup"><span data-stu-id="33ca2-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="33ca2-113">Impostare periodi magazzino, metodi di costing e metodi di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="33ca2-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="33ca2-114">Impostazione della valutazione magazzino e i costi</span><span class="sxs-lookup"><span data-stu-id="33ca2-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="33ca2-115">Rivalutare o ammortizzare il valore di uno o più articoli in magazzino registrandone il corrente valore calcolato.</span><span class="sxs-lookup"><span data-stu-id="33ca2-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="33ca2-116">Rivalutare il magazzino</span><span class="sxs-lookup"><span data-stu-id="33ca2-116">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="33ca2-117">Rettificare i costi articolo, automaticamente o manualmente, per inoltrare le modifiche dei costi dai movimenti in entrata ai movimenti in uscita correlati.</span><span class="sxs-lookup"><span data-stu-id="33ca2-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="33ca2-118">Rettifica costi articolo</span><span class="sxs-lookup"><span data-stu-id="33ca2-118">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="33ca2-119">Utilizzare le funzioni di costing speciali per le transazioni di articoli quotidiane nelle operazioni articoli.</span><span class="sxs-lookup"><span data-stu-id="33ca2-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="33ca2-120">Gestione dei costi del magazzino e di produzione</span><span class="sxs-lookup"><span data-stu-id="33ca2-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="33ca2-121">È necessario aggiornare periodicamente i costi standard dei componenti, nelle distinte base di assemblaggio e di produzione, ed eseguire il rollup dei nuovi costi nell'articolo padre.</span><span class="sxs-lookup"><span data-stu-id="33ca2-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="33ca2-122">Aggiornare i costi standard</span><span class="sxs-lookup"><span data-stu-id="33ca2-122">Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="33ca2-123">Eseguire attività di controllo e reporting di chiusura del periodo, ad esempio calcolare il valore di magazzino e registrare i costi nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="33ca2-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="33ca2-124">Creazione di report dei costi e riconciliazione con la contabilità generale</span><span class="sxs-lookup"><span data-stu-id="33ca2-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="33ca2-125">Informazioni su tutti i meccanismi nel sistema di costing.</span><span class="sxs-lookup"><span data-stu-id="33ca2-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="33ca2-126">Dettagli di progettazione: Costing di magazzino</span><span class="sxs-lookup"><span data-stu-id="33ca2-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="33ca2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ca2-127">See Also</span></span>  
 [<span data-ttu-id="33ca2-128">Finanze</span><span class="sxs-lookup"><span data-stu-id="33ca2-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="33ca2-129">[Magazzino](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="33ca2-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="33ca2-130">[Vendite](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="33ca2-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="33ca2-131">Acquisti</span><span class="sxs-lookup"><span data-stu-id="33ca2-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="33ca2-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="33ca2-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

