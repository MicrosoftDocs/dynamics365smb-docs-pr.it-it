---
title: 'Dettagli di progettazione: Il ruolo del punto di riordino | Microsoft Docs'
description: "In questo argomento viene evidenziata l'importanza di impostare un punto di riordino, in modo da sapere quando è necessario approvvigionare il magazzino."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: e39a7efdc796e8745bd9d8f7d74cdcfb171d851f
ms.contentlocale: it-it
ms.lasthandoff: 11/20/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="be4b2-103">Dettagli di progettazione: Il ruolo del punto di riordino</span><span class="sxs-lookup"><span data-stu-id="be4b2-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="be4b2-104">Oltre alla contropartita generale di approvvigionamento e domanda, il sistema di pianificazione deve inoltre monitorare i livelli di magazzino per gli articoli interessati in modo che siano rispettati i metodi di riordino definiti:</span><span class="sxs-lookup"><span data-stu-id="be4b2-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  

<span data-ttu-id="be4b2-105">Un punto di riordino rappresenta la domanda durante il lead time.</span><span class="sxs-lookup"><span data-stu-id="be4b2-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="be4b2-106">Quando la giacenza disponibile scende sotto il livello di magazzino definito dal punto di riordino, è tempo di ordinare una maggiore quantità.</span><span class="sxs-lookup"><span data-stu-id="be4b2-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="be4b2-107">Nel frattempo, si prevede una diminuzione graduale della giacenza, che possibilmente raggiunge lo zero (o il livello di scorta di sicurezza), finché non arriva il rifornimento.</span><span class="sxs-lookup"><span data-stu-id="be4b2-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  

<span data-ttu-id="be4b2-108">Di conseguenza, il sistema di pianificazione suggerirà un ordine di approvvigionamento programmato in avanti alla fase in cui la giacenza prevista passa al di sotto del punto di riordino.</span><span class="sxs-lookup"><span data-stu-id="be4b2-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  

<span data-ttu-id="be4b2-109">Il punto di riordino riflette un determinato livello di magazzino.</span><span class="sxs-lookup"><span data-stu-id="be4b2-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="be4b2-110">Tuttavia, i livelli di magazzino possono spostarsi in modo significativo nell'intervallo di tempo e, pertanto, il sistema di pianificazione deve costantemente monitorare le scorte disponibili previste.</span><span class="sxs-lookup"><span data-stu-id="be4b2-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be4b2-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be4b2-111">See Also</span></span>  
<span data-ttu-id="be4b2-112">[Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="be4b2-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="be4b2-113">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="be4b2-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="be4b2-114">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="be4b2-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="be4b2-115">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="be4b2-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

