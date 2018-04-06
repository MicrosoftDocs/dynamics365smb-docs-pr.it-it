---
title: 'Dettagli di progettazione: Il ruolo dell''intervallo di tempo | Microsoft Docs'
description: "Lo scopo dell'intervallo di tempo è di raccogliere gli eventi di domanda nell'intervallo di tempo in modo da creare un ordine di approvvigionamento congiunto."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="51359-103">Dettagli di progettazione: Il ruolo dell'intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="51359-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="51359-104">Lo scopo dell'intervallo di tempo è di raccogliere gli eventi di domanda nell'intervallo di tempo in modo da creare un ordine di approvvigionamento congiunto.</span><span class="sxs-lookup"><span data-stu-id="51359-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  
  
 <span data-ttu-id="51359-105">Per i metodi di riordino che utilizzano un punto di riordino, è possibile definire un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="51359-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="51359-106">In questo modo si garantisce che la domanda nello stesso periodo di tempo venga accumulata prima di controllare l'impatto sulla giacenza disponibile e se il punto di riordino sia stato superato.</span><span class="sxs-lookup"><span data-stu-id="51359-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="51359-107">Se il punto di riordino è passato, viene programmato un nuovo ordine di approvvigionamento in una data successiva dalla fine del periodo definito dall'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="51359-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="51359-108">Gli intervalli di tempo iniziano con la data di inizio pianificazione.</span><span class="sxs-lookup"><span data-stu-id="51359-108">The time buckets begin on the planning starting date.</span></span>  
  
 <span data-ttu-id="51359-109">Il concetto di attività in un intervallo di tempo riflette il processo manuale di controllo del livello di magazzino su base frequente anziché ad ogni transazione.</span><span class="sxs-lookup"><span data-stu-id="51359-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="51359-110">L'utente deve definire la frequenza (intervallo di tempo).</span><span class="sxs-lookup"><span data-stu-id="51359-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="51359-111">Ad esempio, l'utente raccoglie tutte le esigenze dell'articolo da un fornitore per inserire un ordine settimanale.</span><span class="sxs-lookup"><span data-stu-id="51359-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  
  
 <span data-ttu-id="51359-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span><span class="sxs-lookup"><span data-stu-id="51359-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span></span>  
  
 <span data-ttu-id="51359-113">L'intervallo di tempo viene in genere utilizzato per evitare un effetto di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="51359-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="51359-114">Ad esempio, una riga equilibrata di approvvigionamento e domanda dove una domanda iniziale viene annullata o ne viene creata una nuova.</span><span class="sxs-lookup"><span data-stu-id="51359-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="51359-115">Il risultato sarebbe che ogni ordine di approvvigionamento (eccetto l'ultimo) viene riprogrammato.</span><span class="sxs-lookup"><span data-stu-id="51359-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51359-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51359-116">See Also</span></span>  
 <span data-ttu-id="51359-117">[Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="51359-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="51359-118">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="51359-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="51359-119">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="51359-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="51359-120">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="51359-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
