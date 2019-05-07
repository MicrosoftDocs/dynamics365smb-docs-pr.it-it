---
title: 'Dettagli di progettazione: Assegnazione priorità ordini | Microsoft Docs'
description: Informazioni su come assegnare le priorità per soddisfare domanda e approvvigionamento.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 06eb5221369d8777330ae844adfb5d87658d591d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "924212"
---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="476da-103">Dettagli di progettazione: Assegnazione priorità ordini</span><span class="sxs-lookup"><span data-stu-id="476da-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="476da-104">All'interno di una determinata USK, la data richiesta o disponibile rappresenta la priorità più alta; la domanda della data corrente deve essere gestita prima della domanda della settimana successiva.</span><span class="sxs-lookup"><span data-stu-id="476da-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="476da-105">Ma oltre a questa priorità globale, il sistema di pianificazione suggerirà inoltre il tipo di domanda da soddisfare prima di soddisfarne un'altra.</span><span class="sxs-lookup"><span data-stu-id="476da-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="476da-106">Analogamente, verrà suggerito quale origine di approvvigionamento deve essere collegata prima di collegare altre origini di approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="476da-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="476da-107">Questa operazione viene eseguita in base alle priorità degli ordini.</span><span class="sxs-lookup"><span data-stu-id="476da-107">This is done according to order priorities.</span></span>  

<span data-ttu-id="476da-108">La domanda e l'approvvigionamento caricati contribuiscono a un profilo per la giacenza disponibile in base alle seguenti priorità:</span><span class="sxs-lookup"><span data-stu-id="476da-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  

## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="476da-109">Priorità sul lato della domanda</span><span class="sxs-lookup"><span data-stu-id="476da-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="476da-110">Già spediti: Mov. contabili articolo</span><span class="sxs-lookup"><span data-stu-id="476da-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="476da-111">Ordine di reso acquisto</span><span class="sxs-lookup"><span data-stu-id="476da-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="476da-112">Ordini Vendita</span><span class="sxs-lookup"><span data-stu-id="476da-112">Sales Order</span></span>  
4. <span data-ttu-id="476da-113">Ordine Assistenza</span><span class="sxs-lookup"><span data-stu-id="476da-113">Service Order</span></span>  
5. <span data-ttu-id="476da-114">Necessità componente di produzione</span><span class="sxs-lookup"><span data-stu-id="476da-114">Production Component Need</span></span>  
6. <span data-ttu-id="476da-115">Riga ordine di assemblaggio</span><span class="sxs-lookup"><span data-stu-id="476da-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="476da-116">Ordine di trasferimento in uscita</span><span class="sxs-lookup"><span data-stu-id="476da-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="476da-117">L'ordine programmato (non ancora utilizzato dagli ordini di vendita correlati)</span><span class="sxs-lookup"><span data-stu-id="476da-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="476da-118">Previsione (non ancora utilizzata da altri ordini di vendita)</span><span class="sxs-lookup"><span data-stu-id="476da-118">Forecast (that has not already been consumed by other sales orders)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="476da-119">I resi di acquisto non vengono in genere inclusi nella pianificazione dell'approvvigionamento; devono essere sempre impegnati dal lotto che sta per essere reso.</span><span class="sxs-lookup"><span data-stu-id="476da-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="476da-120">Se non impegnati, i resi di acquisto svolgono un ruolo nella disponibilità e hanno un'elevata priorità per evitare che il sistema suggerisca un ordine di approvvigionamento solo per un ordine di reso.</span><span class="sxs-lookup"><span data-stu-id="476da-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  

## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="476da-121">Priorità sul lato dell'approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="476da-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="476da-122">Già in magazzino: Mov. contabili articoli (Flessibilità pianificazione = Nessuna)</span><span class="sxs-lookup"><span data-stu-id="476da-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="476da-123">Ordine di reso vendita (flessibilità pianificazione = nessuna)</span><span class="sxs-lookup"><span data-stu-id="476da-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="476da-124">Ordine di trasferimento in ingresso</span><span class="sxs-lookup"><span data-stu-id="476da-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="476da-125">Ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="476da-125">Production Order</span></span>  
5. <span data-ttu-id="476da-126">Ordine di assemblaggio</span><span class="sxs-lookup"><span data-stu-id="476da-126">Assembly Order</span></span>  
6. <span data-ttu-id="476da-127">Ordine acquisto</span><span class="sxs-lookup"><span data-stu-id="476da-127">Purchase Order</span></span>  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="476da-128">Priorità correlata allo stato di domanda e approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="476da-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="476da-129">Oltre alle priorità specificate dal tipo di domanda e approvvigionamento, lo stato attuale degli ordini nel processo di esecuzione definisce anche una priorità.</span><span class="sxs-lookup"><span data-stu-id="476da-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="476da-130">Ad esempio, le attività di magazzino hanno un l'impatto e lo stato degli ordini di vendita, di acquisto, di trasferimento, di assemblaggio e di produzione vengono presi in considerazione:</span><span class="sxs-lookup"><span data-stu-id="476da-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  

1. <span data-ttu-id="476da-131">Gestito parzialmente (flessibilità pianificazione = nessuna)</span><span class="sxs-lookup"><span data-stu-id="476da-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="476da-132">Già nel processo nel warehouse (flessibilità pianificazione = Nessuna)</span><span class="sxs-lookup"><span data-stu-id="476da-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="476da-133">Rilasciato - tutti i tipi di ordine (flessibilità pianificazione = illimitata)</span><span class="sxs-lookup"><span data-stu-id="476da-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="476da-134">Ordine di produzione confermato (flessibilità pianificazione = illimitata)</span><span class="sxs-lookup"><span data-stu-id="476da-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="476da-135">Pianificato/Aperto - tutti i tipi di ordine (flessibilità pianificazione = illimitata)</span><span class="sxs-lookup"><span data-stu-id="476da-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  

## <a name="see-also"></a><span data-ttu-id="476da-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="476da-136">See Also</span></span>  
<span data-ttu-id="476da-137">[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="476da-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="476da-138">[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="476da-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="476da-139">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="476da-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
