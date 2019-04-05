---
title: 'Dettagli di progettazione: Tabella Assegnazione pianificazione | Microsoft Docs'
description: Questo argomento fornisce informazioni dettagliate sulle conseguenze relative alla modifica del metodo di pianificazione per un articolo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 9a1661d71bd28009a0c0b83a50e27cae3c833ea7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802142"
---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="8e69d-103">Dettagli di progettazione: Tabella Assegnazione pianificazione</span><span class="sxs-lookup"><span data-stu-id="8e69d-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="8e69d-104">Tutti gli articoli devono essere pianificati, tuttavia, non esiste motivo per calcolare un piano per un articolo a meno che non ci sia stato una modifica nella domanda o nel modello di approvvigionamento dall'ultima volta in cui è stato calcolato un piano.</span><span class="sxs-lookup"><span data-stu-id="8e69d-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  

<span data-ttu-id="8e69d-105">Se l'utente ha immesso un nuovo ordine di vendita o ne ha cambiato uno esistente, esiste motivo per ricalcolare il piano.</span><span class="sxs-lookup"><span data-stu-id="8e69d-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="8e69d-106">Altri motivi includono una modifica nella previsione o la scorta di sicurezza desiderata.</span><span class="sxs-lookup"><span data-stu-id="8e69d-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="8e69d-107">Modificare una distinta base aggiungendo o rimuovendo un componente che molto probabilmente indicherebbe una modifica, ma solo per l'articolo del componente.</span><span class="sxs-lookup"><span data-stu-id="8e69d-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  

<span data-ttu-id="8e69d-108">Per più ubicazioni, l'assegnazione avviene a livello di articolo per ogni combinazione di ubicazione.</span><span class="sxs-lookup"><span data-stu-id="8e69d-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="8e69d-109">Se, ad esempio, un ordine di vendita è stato creato solo in un'ubicazione, il programma assegnerà l'articolo a tale specifica ubicazione per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8e69d-109">If, for example, a sales order has been created at only one location, the program will assign the item at that specific location for planning.</span></span>  

<span data-ttu-id="8e69d-110">Il motivo per selezionare gli articoli per la pianificazione è una questione di prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e69d-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="8e69d-111">Se non viene apportata alcuna modifica nel modello domanda-approvvigionamento di un articolo, il sistema di pianificazione non suggerirà alcuna azione da intraprendere.</span><span class="sxs-lookup"><span data-stu-id="8e69d-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="8e69d-112">Senza l'assegnazione di pianificazione, il sistema deve eseguire i calcoli per tutti gli articoli per determinare cosa pianificare e cosa sfrutta maggiormente le risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="8e69d-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  

<span data-ttu-id="8e69d-113">Nella tabella **Pianificazione assegnazione** vengono monitorati gli eventi di domanda e approvvigionamento e assegnati gli articoli appropriati per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8e69d-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="8e69d-114">I seguenti eventi vengono monitorati:</span><span class="sxs-lookup"><span data-stu-id="8e69d-114">The following events are monitored:</span></span>  

* <span data-ttu-id="8e69d-115">Un nuovo ordine di vendita, previsione, componente, ordine acquisto, ordine di produzione, ordine di assemblaggio o ordine di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="8e69d-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="8e69d-116">Modifica di un elemento, quantità, ubicazione, variante o data in un nuovo ordine di vendita, previsione, componente, ordine acquisto, ordine di produzione, ordine di assemblaggio o ordine di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="8e69d-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="8e69d-117">Annullamento di un nuovo ordine di vendita, previsione, componente, ordine acquisto, ordine di produzione, ordine di assemblaggio o ordine di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="8e69d-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="8e69d-118">Consumo di articoli diversi da quelli pianificati.</span><span class="sxs-lookup"><span data-stu-id="8e69d-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="8e69d-119">Output di articoli diversi da quelli pianificati.</span><span class="sxs-lookup"><span data-stu-id="8e69d-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="8e69d-120">Modifiche non pianificate in magazzino.</span><span class="sxs-lookup"><span data-stu-id="8e69d-120">Unplanned changes in inventory.</span></span>  

<span data-ttu-id="8e69d-121">Per questi spostamenti di domanda-approvvigionamento, il sistema di tracciabilità ordine e di messaggistica di azioni gestisce la tabella Compiti di pianificazione e stabilisce un motivo di pianificazione come messaggio di azione.</span><span class="sxs-lookup"><span data-stu-id="8e69d-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  

<span data-ttu-id="8e69d-122">Le seguenti modifiche nell'anagrafica possono causare uno sbilanciamento nella pianificazione:</span><span class="sxs-lookup"><span data-stu-id="8e69d-122">The following changes in master data can also cause a planning imbalance:</span></span>  

* <span data-ttu-id="8e69d-123">Modifica dello stato in Certificato nella testata della DB di produzione (per tutti gli articoli che utilizzano tale testata).</span><span class="sxs-lookup"><span data-stu-id="8e69d-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="8e69d-124">Riga eliminata (articolo figlio).</span><span class="sxs-lookup"><span data-stu-id="8e69d-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="8e69d-125">Modifica dello stato in Certificato nella testata ciclo (per tutti gli articoli che utilizzano tale ciclo).</span><span class="sxs-lookup"><span data-stu-id="8e69d-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="8e69d-126">Le modifiche ai seguenti campi della scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="8e69d-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="8e69d-127">Scorta di sicurezza o Lead time di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8e69d-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="8e69d-128">Calcolo lead time.</span><span class="sxs-lookup"><span data-stu-id="8e69d-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="8e69d-129">Punto riordino.</span><span class="sxs-lookup"><span data-stu-id="8e69d-129">Reorder Point.</span></span>  
* <span data-ttu-id="8e69d-130">Nr. DB produzione (e tutti i figli del riferimento alla DB obsoleta).</span><span class="sxs-lookup"><span data-stu-id="8e69d-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="8e69d-131">Nr. ciclo</span><span class="sxs-lookup"><span data-stu-id="8e69d-131">Routing No.</span></span>  
* <span data-ttu-id="8e69d-132">Metodo di riordino.</span><span class="sxs-lookup"><span data-stu-id="8e69d-132">Reordering Policy.</span></span>  

<span data-ttu-id="8e69d-133">In questi casi, una nuova funzione, gestione delle assegnazioni della pianificazione, gestisce la tabella e determina il motivo della pianificazione come Saldo periodo.</span><span class="sxs-lookup"><span data-stu-id="8e69d-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  

<span data-ttu-id="8e69d-134">Le seguenti modifiche non causano un'assegnazione di pianificazione:</span><span class="sxs-lookup"><span data-stu-id="8e69d-134">The following changes do not cause a planning assignment:</span></span>  

* <span data-ttu-id="8e69d-135">Calendari</span><span class="sxs-lookup"><span data-stu-id="8e69d-135">Calendars</span></span>  
* <span data-ttu-id="8e69d-136">Altri parametri di pianificazione nella scheda articolo</span><span class="sxs-lookup"><span data-stu-id="8e69d-136">Other planning parameters on the item card</span></span>  

<span data-ttu-id="8e69d-137">Nel calcolo di un MPS o un MRP si applicano le seguenti restrizioni:</span><span class="sxs-lookup"><span data-stu-id="8e69d-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  

* <span data-ttu-id="8e69d-138">MPS: il sistema di pianificazione controlla che l'articolo includa una previsione di domanda o un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="8e69d-138">MPS: The planning system checks that the item carries a demand forecast or a sales order.</span></span> <span data-ttu-id="8e69d-139">In caso contrario, l'articolo non viene incluso nel piano.</span><span class="sxs-lookup"><span data-stu-id="8e69d-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="8e69d-140">MRP: se il sistema di pianificazione rileva che l'articolo sta per essere rifornito da una riga di pianificazione MPS o da un ordine di approvvigionamento MPS, l'articolo verrà escluso dalla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8e69d-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="8e69d-141">Tuttavia, è inclusa qualsiasi domanda dai componenti pertinenti.</span><span class="sxs-lookup"><span data-stu-id="8e69d-141">However, any demand from relevant components is included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8e69d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e69d-142">See Also</span></span>  
<span data-ttu-id="8e69d-143">[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="8e69d-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="8e69d-144">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="8e69d-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="8e69d-145">[Dettagli di progettazione: Trasferimenti nella pianificazione](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="8e69d-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="8e69d-146">Dettagli di progettazione: Parametri di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8e69d-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
