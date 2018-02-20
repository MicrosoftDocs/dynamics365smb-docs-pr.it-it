---
title: 'Dettagli di progettazione: Gestione giacenze negative previste | Microsoft Docs'
description: "Il punto di riordino esprime la domanda prevista durante il lead time dell'articolo. Quando il punto di riordino viene superato, è tempo di ordinare quantità maggiori. Ma le scorte previste devono essere abbastanza grandi da coprire la domanda fino a che non viene ricevuto il nuovo ordine. Nel frattempo, la scorta di sicurezza deve coprire le fluttuazioni della domanda fino a un livello di servizio di destinazione."
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
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="80dae-106">Dettagli di progettazione: Gestione giacenze negative previste</span><span class="sxs-lookup"><span data-stu-id="80dae-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="80dae-107">Il punto di riordino esprime la domanda prevista durante il lead time dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="80dae-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="80dae-108">Quando il punto di riordino viene superato, è tempo di ordinare quantità maggiori.</span><span class="sxs-lookup"><span data-stu-id="80dae-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="80dae-109">Ma le scorte previste devono essere abbastanza grandi da coprire la domanda fino a che non viene ricevuto il nuovo ordine.</span><span class="sxs-lookup"><span data-stu-id="80dae-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="80dae-110">Nel frattempo, la scorta di sicurezza deve coprire le fluttuazioni della domanda fino a un livello di servizio di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80dae-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="80dae-111">Di conseguenza, se una domanda futura non può essere servita dalle scorte previste, oppure espressa in un altro modo, il sistema di pianificazione considera un'emergenza se la giacenza disponibile diventa negativa.</span><span class="sxs-lookup"><span data-stu-id="80dae-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="80dae-112">Il sistema tratta questo tipo di eccezione suggerendo un nuovo ordine di approvvigionamento in modo da soddisfare la parte della domanda che non può essere soddisfatta dal magazzino o da un altro approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="80dae-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="80dae-113">Le dimensioni dell'ordine del nuovo ordine di approvvigionamento non prenderanno in considerazione la giacenza massima o la quantità di riordino, né prenderanno in considerazione i modificatori di ordine Quantità massima ordine, Quantità minima ordine e Molteplicità ordine.</span><span class="sxs-lookup"><span data-stu-id="80dae-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="80dae-114">In alternativa, rifletterà la carenza esatta.</span><span class="sxs-lookup"><span data-stu-id="80dae-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="80dae-115">Nella riga di pianificazione per questo tipo ordine di approvvigionamento verrà visualizzata un'icona di avviso di emergenza. Verranno inoltre fornite informazioni aggiuntive su ricerca per informare l'utente della situazione.</span><span class="sxs-lookup"><span data-stu-id="80dae-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="80dae-116">Nella seguente illustrazione l'approvvigionamento D rappresenta un ordine di emergenza per la rettifica della giacenza negativa.</span><span class="sxs-lookup"><span data-stu-id="80dae-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 <span data-ttu-id="80dae-117">![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")</span><span class="sxs-lookup"><span data-stu-id="80dae-117">![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")</span></span>  

1.  <span data-ttu-id="80dae-118">L'approvvigionamento **A**, la giacenza disponibile iniziale, è inferiore al punto di riordino.</span><span class="sxs-lookup"><span data-stu-id="80dae-118">Supply **A**, initial projected inventory, is below reorder point.</span></span>  

2.  <span data-ttu-id="80dae-119">Viene creato un nuovo approvvigionamento programmato in avanti (**C**).</span><span class="sxs-lookup"><span data-stu-id="80dae-119">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="80dae-120">(Quantità = Giacenza massima – Livello giacenza disponibile)</span><span class="sxs-lookup"><span data-stu-id="80dae-120">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  

3.  <span data-ttu-id="80dae-121">L'approvvigionamento **A** viene chiuso dalla domanda **B**, che non viene coperta completamente.</span><span class="sxs-lookup"><span data-stu-id="80dae-121">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="80dae-122">La domanda **B** potrebbe provare a pianificare l'Approvvigionamento C ma ciò non accade in base al concetto dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="80dae-122">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  

4.  <span data-ttu-id="80dae-123">Un nuovo approvvigionamento (**D**) viene creato per coprire la quantità residua sulla domanda **B**.</span><span class="sxs-lookup"><span data-stu-id="80dae-123">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  

5.  <span data-ttu-id="80dae-124">La domanda **B** viene chiusa creando un sollecito alle scorte previste.</span><span class="sxs-lookup"><span data-stu-id="80dae-124">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  

6.  <span data-ttu-id="80dae-125">Il nuovo approvvigionamento **D** viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="80dae-125">The new supply **D** is closed.</span></span>  

7.  <span data-ttu-id="80dae-126">La giacenza disponibile è controllata; il punto di riordino non è stato superato.</span><span class="sxs-lookup"><span data-stu-id="80dae-126">Projected Inventory is checked; reorder point has not been crossed.</span></span>  

8.  <span data-ttu-id="80dae-127">L'approvvigionamento **C** viene chiuso (non esiste più la domanda).</span><span class="sxs-lookup"><span data-stu-id="80dae-127">Supply **C** is closed (no more demand exists).</span></span>  

9. <span data-ttu-id="80dae-128">Controllo finale: non esistono solleciti di livello di magazzino in sospeso.</span><span class="sxs-lookup"><span data-stu-id="80dae-128">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="80dae-129">Il passaggio 4 indica in che modo il sistema opera nelle versioni precedenti a Microsoft Dynamics NAV 2009 SP1.</span><span class="sxs-lookup"><span data-stu-id="80dae-129">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="80dae-130">Ciò conclude la descrizione dei principi centrali relativi alla pianificazione del magazzino basata sui metodi di riordino.</span><span class="sxs-lookup"><span data-stu-id="80dae-130">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="80dae-131">Nella seguente sezione vengono illustrate le caratteristiche dei quattro metodi di riordino supportati.</span><span class="sxs-lookup"><span data-stu-id="80dae-131">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="80dae-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80dae-132">See Also</span></span>  
 <span data-ttu-id="80dae-133">[Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="80dae-133">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="80dae-134">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="80dae-134">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="80dae-135">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="80dae-135">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="80dae-136">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="80dae-136">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

