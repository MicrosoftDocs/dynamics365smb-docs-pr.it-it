---
title: 'Dettagli di progettazione: Il concetto di contropartita in breve | Microsoft Docs'
description: "La domanda è fornita dai clienti di una società. L'approvvigionamento è ciò che la società può creare e rimuovere per stabilire il saldo. Il sistema di pianificazione inizia con la domanda indipendente e successivamente risale a ritroso fino all'approvvigionamento."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ffaa6b174d495b4a22423cabd13b74025db021ed
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-concept-of-balancing-in-brief"></a><span data-ttu-id="afa4f-105">Dettagli di progettazione: Il concetto di contropartita in breve</span><span class="sxs-lookup"><span data-stu-id="afa4f-105">Design Details: The Concept of Balancing in Brief</span></span>
<span data-ttu-id="afa4f-106">La domanda è fornita dai clienti di una società.</span><span class="sxs-lookup"><span data-stu-id="afa4f-106">Demand is given by a company’s customers.</span></span> <span data-ttu-id="afa4f-107">L'approvvigionamento è ciò che la società può creare e rimuovere per stabilire il saldo.</span><span class="sxs-lookup"><span data-stu-id="afa4f-107">Supply is what the company can create and remove to establish balance.</span></span> <span data-ttu-id="afa4f-108">Il sistema di pianificazione inizia con la domanda indipendente e successivamente risale a ritroso fino all'approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="afa4f-108">The planning system starts with the independent demand and then tracks backwards to the supply.</span></span>  
  
 <span data-ttu-id="afa4f-109">I profili di magazzino vengono utilizzati per contenere le informazioni sulle domande, gli approvvigionamenti, le quantità e l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="afa4f-109">The inventory profiles are used to contain information about the demands and supplies, quantities, and timing.</span></span> <span data-ttu-id="afa4f-110">I profili essenzialmente compongono i due lati della bilancia.</span><span class="sxs-lookup"><span data-stu-id="afa4f-110">These profiles essentially make up the two sides of the balancing scale.</span></span>  
  
 <span data-ttu-id="afa4f-111">L'obiettivo del meccanismo di pianificazione consiste nel controbilanciare la domanda e l'approvvigionamento di un articolo per garantire che l'approvvigionamento corrisponda alla domanda in modo fattibile così come definito dalle regole e dai parametri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="afa4f-111">The objective of the planning mechanism is to counterbalance the demand and supply of an item to ensure that supply will match demand in a feasible way as defined by the planning parameters and rules.</span></span>  
  
 <span data-ttu-id="afa4f-112">![](media/nav_app_supply_planning_2_balancing.png "NAV_APP_supply_planning_2_balancing")</span><span class="sxs-lookup"><span data-stu-id="afa4f-112">![](media/nav_app_supply_planning_2_balancing.png "NAV_APP_supply_planning_2_balancing")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afa4f-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afa4f-113">See Also</span></span>  
 <span data-ttu-id="afa4f-114">[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="afa4f-114">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="afa4f-115">[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="afa4f-115">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="afa4f-116">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="afa4f-116">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
