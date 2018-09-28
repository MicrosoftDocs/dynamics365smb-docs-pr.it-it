---
title: 'Dettagli di progettazione: Gestione dei metodi di riordino | Microsoft Docs'
description: Panoramica dei task per la definizione di un metodo di riordino nella pianificazione dell'approvvigionamento.
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
ms.openlocfilehash: e06d91bc1c293e7015af0fe21d918361f322c10d
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="8e3ee-103">Dettagli di progettazione: Gestione dei metodi di riordino</span><span class="sxs-lookup"><span data-stu-id="8e3ee-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="8e3ee-104">Affinché un articolo partecipi alla pianificazione dell'approvvigionamento, i metodi di riordino devono essere definiti.</span><span class="sxs-lookup"><span data-stu-id="8e3ee-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="8e3ee-105">Sono disponibili i seguenti quattro metodi di riordino:</span><span class="sxs-lookup"><span data-stu-id="8e3ee-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="8e3ee-106">Qtà Riordino Fissa</span><span class="sxs-lookup"><span data-stu-id="8e3ee-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="8e3ee-107">Qtà Massima</span><span class="sxs-lookup"><span data-stu-id="8e3ee-107">Maximum Qty.</span></span>  
* <span data-ttu-id="8e3ee-108">Ordine</span><span class="sxs-lookup"><span data-stu-id="8e3ee-108">Order</span></span>  
* <span data-ttu-id="8e3ee-109">Lotto-per-Lotto</span><span class="sxs-lookup"><span data-stu-id="8e3ee-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="8e3ee-110">I motivi Qtà Riordino Fissa e Qtà massima sono relativi alla pianificazione del magazzino.</span><span class="sxs-lookup"><span data-stu-id="8e3ee-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="8e3ee-111">Sebbene la pianificazione del magazzino sia tecnicamente più semplice della procedura di contropartita, questi criteri devono coesistere con la contropartita dettagliata della tracciabilità di approvvigionamento e ordine.</span><span class="sxs-lookup"><span data-stu-id="8e3ee-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="8e3ee-112">Per controllare l'integrazione tra i due e fornire visibilità nella logica di pianificazione, rigidi principi controllano la gestione dei metodi di riordino.</span><span class="sxs-lookup"><span data-stu-id="8e3ee-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="8e3ee-113">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="8e3ee-113">In This Section</span></span>  
[<span data-ttu-id="8e3ee-114">Dettagli di progettazione: Il ruolo del punto di riordino</span><span class="sxs-lookup"><span data-stu-id="8e3ee-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="8e3ee-115">Dettagli di progettazione: Monitoraggio del livello di giacenza disponibile e del punto di riordino</span><span class="sxs-lookup"><span data-stu-id="8e3ee-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="8e3ee-116">Dettagli di progettazione: Il ruolo dell'intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="8e3ee-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="8e3ee-117">Dettagli di progettazione: Al di sotto del livello di overflow</span><span class="sxs-lookup"><span data-stu-id="8e3ee-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="8e3ee-118">Dettagli di progettazione: Gestione giacenze negative previste</span><span class="sxs-lookup"><span data-stu-id="8e3ee-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="8e3ee-119">Dettagli di progettazione: Metodi di riordino</span><span class="sxs-lookup"><span data-stu-id="8e3ee-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="8e3ee-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e3ee-120">See Also</span></span>  
<span data-ttu-id="8e3ee-121">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="8e3ee-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="8e3ee-122">[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="8e3ee-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="8e3ee-123">[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="8e3ee-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="8e3ee-124">[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="8e3ee-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="8e3ee-125">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="8e3ee-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
