---
title: Definizione e allocazione dei costi | Microsoft Docs
description: "Con le allocazioni costi è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo. È possibile definire tutte le allocazioni necessarie."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="57780-104">Definizione e allocazione dei costi</span><span class="sxs-lookup"><span data-stu-id="57780-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="57780-105">Con le allocazioni costi è possibile spostare i costi e i ricavi tra i tipi di costo, i centri di costo e gli oggetti di costo.</span><span class="sxs-lookup"><span data-stu-id="57780-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="57780-106">È possibile definire tutte le allocazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="57780-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="57780-107">Ogni allocazione è costituita da:</span><span class="sxs-lookup"><span data-stu-id="57780-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="57780-108">Un'origine allocazione.</span><span class="sxs-lookup"><span data-stu-id="57780-108">An allocation source.</span></span>  
-   <span data-ttu-id="57780-109">Uno o più destinazioni di allocazione.</span><span class="sxs-lookup"><span data-stu-id="57780-109">One or more allocation targets.</span></span>  

<span data-ttu-id="57780-110">L'origine dell'allocazione stabilisce quali costi devono essere assegnati, mentre le destinazioni di allocazione determinano dove i costi devono essere allocati.</span><span class="sxs-lookup"><span data-stu-id="57780-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="57780-111">Ad esempio, i costi per il tipo di costo Elettricità e riscaldamento sono un'origine di allocazione.</span><span class="sxs-lookup"><span data-stu-id="57780-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="57780-112">Allocare tutti i costi del riscaldamento e dell'elettricità a tre centri di costo: Workshop, Produzione e Vendite.</span><span class="sxs-lookup"><span data-stu-id="57780-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="57780-113">Questi centri di costi sono le destinazioni di allocazione.</span><span class="sxs-lookup"><span data-stu-id="57780-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="57780-114">Per ogni origine di allocazione, è possibile definire un livello di allocazione, un periodo di validità e una variante come identificatore di gruppo.</span><span class="sxs-lookup"><span data-stu-id="57780-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="57780-115">È possibile utilizzare un processo batch per impostare i filtri per selezionare le definizioni di allocazione e quindi eseguire le allocazioni costi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="57780-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="57780-116">Per ogni destinazione di allocazione, è possibile definire una base di allocazione.</span><span class="sxs-lookup"><span data-stu-id="57780-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="57780-117">La base di allocazione può essere statica o dinamica.</span><span class="sxs-lookup"><span data-stu-id="57780-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="57780-118">Le basi di allocazioni statiche sono basate su un valore definito, come la superficie o un rapporto di allocazione stabilito, ad esempio 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="57780-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="57780-119">Le basi di allocazioni dinamiche dipendono da valori variabili, quali il numero di impiegati in un centro di costo o i ricavi di vendite di un oggetto di costo in un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="57780-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="57780-120">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="57780-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="57780-121">A</span><span class="sxs-lookup"><span data-stu-id="57780-121">To</span></span>|<span data-ttu-id="57780-122">Vedere</span><span class="sxs-lookup"><span data-stu-id="57780-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="57780-123">Impostare origini e destinazioni dell'allocazione.</span><span class="sxs-lookup"><span data-stu-id="57780-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="57780-124">Impostare origini e destinazioni dell'allocazione</span><span class="sxs-lookup"><span data-stu-id="57780-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="57780-125">Impostare vari filtri per le basi di allocazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="57780-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="57780-126">Impostazione di filtri per le basi di allocazione dinamica</span><span class="sxs-lookup"><span data-stu-id="57780-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="57780-127">Visualizzare un esempio su come definire un'allocazione statica.</span><span class="sxs-lookup"><span data-stu-id="57780-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="57780-128">Esempio di scenario: Definizione delle allocazioni statiche in base al rapporto di allocazione</span><span class="sxs-lookup"><span data-stu-id="57780-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="57780-129">Visualizzare un esempio su come definire un'allocazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="57780-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="57780-130">Esempio dello scenario: definizione delle allocazioni dinamiche in base agli articoli venduti</span><span class="sxs-lookup"><span data-stu-id="57780-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="57780-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57780-131">See Also</span></span>  
 <span data-ttu-id="57780-132">[Impostazione della contabilità industriale](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="57780-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="57780-133">[Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="57780-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="57780-134">[Contabilizzazione dei costi](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="57780-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="57780-135">[Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="57780-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="57780-136">Informazioni sulla contabilità industriale</span><span class="sxs-lookup"><span data-stu-id="57780-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

