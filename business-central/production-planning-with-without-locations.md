---
title: Pianificazione con o senza ubicazioni | Microsoft Docs
description: È importante comprendere la pianificazione con o senza codici ubicazione nelle righe della domanda.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 49448cc56d76846c70471a53a257986b543f11b3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758819"
---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="58593-103">Pianificazione con o senza ubicazioni</span><span class="sxs-lookup"><span data-stu-id="58593-103">Planning With or Without Locations</span></span>
<span data-ttu-id="58593-104">Nel caso della pianificazione con o senza codici ubicazione nelle righe della domanda, il sistema di pianificazione agisce in modo diretto nei casi indicati di seguito.</span><span class="sxs-lookup"><span data-stu-id="58593-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="58593-105">Le righe della domanda includono sempre codici ubicazione e il sistema utilizza completamente le unità di stockkeeping, incluso il setup dell'ubicazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="58593-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="58593-106">Le righe della domanda non includono mai i codici ubicazione e il sistema non utilizza le USK o il setup dell'ubicazione, come nel caso dell'ultimo scenario riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="58593-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="58593-107">Se tuttavia i codici ubicazione sono a volte inclusi e a volte non inclusi nelle righe della domanda, il sistema di pianificazione segue regole specifiche in base al setup.</span><span class="sxs-lookup"><span data-stu-id="58593-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="58593-108">Domanda nell'ubicazione</span><span class="sxs-lookup"><span data-stu-id="58593-108">Demand at Location</span></span>  
<span data-ttu-id="58593-109">In caso di rilevamento di una domanda in corrispondenza di un'ubicazione, ovvero una riga con un codice ubicazione, il funzionamento del sistema di pianificazione varia in base a 3 importanti valori di setup.</span><span class="sxs-lookup"><span data-stu-id="58593-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="58593-110">Durante l'esecuzione della pianificazione, viene eseguito il controllo dei 3 valori di setup in sequenza, quindi la pianificazione viene eseguita in base a tali valori, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="58593-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="58593-111">Viene verificata la presenza di un segno di spunta nel campo **Ubicazione Obbligatoria**.</span><span class="sxs-lookup"><span data-stu-id="58593-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="58593-112">In caso affermativo</span><span class="sxs-lookup"><span data-stu-id="58593-112">If yes, then:</span></span>  

2.  <span data-ttu-id="58593-113">Viene verificata la presenza dell'unità di stockkeeping (USK) per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="58593-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="58593-114">In caso affermativo</span><span class="sxs-lookup"><span data-stu-id="58593-114">If yes, then:</span></span>  

    <span data-ttu-id="58593-115">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK.</span><span class="sxs-lookup"><span data-stu-id="58593-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="58593-116">In caso negativo</span><span class="sxs-lookup"><span data-stu-id="58593-116">If no, then:</span></span>  

3.  <span data-ttu-id="58593-117">Viene verificata la presenza del codice ubicazione richiesto nel campo **Componenti nell'Ubicazione**.</span><span class="sxs-lookup"><span data-stu-id="58593-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="58593-118">In caso affermativo</span><span class="sxs-lookup"><span data-stu-id="58593-118">If yes, then:</span></span>  

    <span data-ttu-id="58593-119">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="58593-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="58593-120">In caso negativo</span><span class="sxs-lookup"><span data-stu-id="58593-120">If no, then:</span></span>  

    <span data-ttu-id="58593-121">L'articolo viene pianificato in base a quanto segue: Metodi di Riordino =  *Lotto-per-Lotto*, Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.</span><span class="sxs-lookup"><span data-stu-id="58593-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="58593-122">Nel caso degli articoli per i quali è utilizzato il metodo di riordino  *Ordine*, il sistema continuerà a utilizzare  *Ordine* e tutte le altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="58593-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="58593-123">Questa "alternativa minima" riguarda esclusivamente la domanda.</span><span class="sxs-lookup"><span data-stu-id="58593-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="58593-124">Gli eventuali parametri di pianificazione definiti vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="58593-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="58593-125">Vedere le differenze di scenario riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="58593-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="58593-126">Domanda nell'"ubicazione vuota"</span><span class="sxs-lookup"><span data-stu-id="58593-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="58593-127">Anche se la casella di controllo **Ubicazione obbligatoria** è selezionata, il sistema consente la creazione delle righe della domanda senza un codice ubicazione, definita anche come ubicazione *VUOTA*.</span><span class="sxs-lookup"><span data-stu-id="58593-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="58593-128">Si tratta di una deviazione per il sistema perché dispone di diversi valori setup ottimizzati per gestire le ubicazioni (vedere sopra) e di conseguenza il motore di pianificazione non creerà una riga di pianificazione per tale riga della domanda.</span><span class="sxs-lookup"><span data-stu-id="58593-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="58593-129">Se il campo **Ubicazione obbligatoria** non è selezionato ma non esiste nessuno dei valori setup dell'ubicazione, anche questa è considerata una deviazione e il sistema di pianificazione reagirà restituendo l'"alternativa minima":</span><span class="sxs-lookup"><span data-stu-id="58593-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="58593-130">L'articolo viene pertanto pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane *Ordine)*, Includi Giacenze =  *Sì*, tutti gli altri parametri vuoti.</span><span class="sxs-lookup"><span data-stu-id="58593-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="58593-131">Vedere le differenze negli scenari di setup riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="58593-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="58593-132">Setup 1:</span><span class="sxs-lookup"><span data-stu-id="58593-132">Setup 1:</span></span>  

-   <span data-ttu-id="58593-133">Ubicazione Obbligatoria = *Sì*</span><span class="sxs-lookup"><span data-stu-id="58593-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="58593-134">Unità di stockkeeping =  *ROSSO*</span><span class="sxs-lookup"><span data-stu-id="58593-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="58593-135">Componenti nell'Ubicazione =  *BLU*</span><span class="sxs-lookup"><span data-stu-id="58593-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="58593-136">Caso 1.1: domanda nell'ubicazione *ROSSO*</span><span class="sxs-lookup"><span data-stu-id="58593-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="58593-137">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK, incluso il possibile trasferimento.</span><span class="sxs-lookup"><span data-stu-id="58593-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="58593-138">Caso 1.2: domanda nell'ubicazione *BLU*</span><span class="sxs-lookup"><span data-stu-id="58593-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="58593-139">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="58593-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="58593-140">Caso 1.3: domanda nell'ubicazione  *VERDE*</span><span class="sxs-lookup"><span data-stu-id="58593-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="58593-141">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.</span><span class="sxs-lookup"><span data-stu-id="58593-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="58593-142">Caso 1.4: domanda nell'ubicazione  *VUOTA*</span><span class="sxs-lookup"><span data-stu-id="58593-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="58593-143">L'articolo non viene pianificato perché non è definita alcuna ubicazione nella riga della domanda.</span><span class="sxs-lookup"><span data-stu-id="58593-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="58593-144">Setup 2:</span><span class="sxs-lookup"><span data-stu-id="58593-144">Setup 2:</span></span>  

-   <span data-ttu-id="58593-145">Ubicazione Obbligatoria = *Sì*</span><span class="sxs-lookup"><span data-stu-id="58593-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="58593-146">Nessuna USK esistente</span><span class="sxs-lookup"><span data-stu-id="58593-146">No SKU exists</span></span>  
-   <span data-ttu-id="58593-147">Componenti nell'Ubicazione =  *BLU*</span><span class="sxs-lookup"><span data-stu-id="58593-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="58593-148">Caso 2.1: domanda nell'ubicazione  *ROSSO*</span><span class="sxs-lookup"><span data-stu-id="58593-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="58593-149">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.</span><span class="sxs-lookup"><span data-stu-id="58593-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="58593-150">Caso 2.2: domanda nell'ubicazione *BLU*</span><span class="sxs-lookup"><span data-stu-id="58593-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="58593-151">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="58593-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="58593-152">Setup 3:</span><span class="sxs-lookup"><span data-stu-id="58593-152">Setup 3:</span></span>  

-   <span data-ttu-id="58593-153">Ubicazione Obbligatoria = *No*</span><span class="sxs-lookup"><span data-stu-id="58593-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="58593-154">Nessuna USK esistente</span><span class="sxs-lookup"><span data-stu-id="58593-154">No SKU exists</span></span>  
-   <span data-ttu-id="58593-155">Componenti nell'Ubicazione =  *BLU*</span><span class="sxs-lookup"><span data-stu-id="58593-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="58593-156">Caso 3.1: domanda nell'ubicazione  *ROSSO*</span><span class="sxs-lookup"><span data-stu-id="58593-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="58593-157">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.</span><span class="sxs-lookup"><span data-stu-id="58593-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="58593-158">Caso 3.2: domanda nell'ubicazione *BLU*</span><span class="sxs-lookup"><span data-stu-id="58593-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="58593-159">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="58593-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="58593-160">Caso 3.3: domanda nell'ubicazione  *VUOTA*</span><span class="sxs-lookup"><span data-stu-id="58593-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="58593-161">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.</span><span class="sxs-lookup"><span data-stu-id="58593-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="58593-162">Setup 4:</span><span class="sxs-lookup"><span data-stu-id="58593-162">Setup 4:</span></span>  

-   <span data-ttu-id="58593-163">Ubicazione Obbligatoria = *No*</span><span class="sxs-lookup"><span data-stu-id="58593-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="58593-164">Nessuna USK esistente</span><span class="sxs-lookup"><span data-stu-id="58593-164">No SKU exists</span></span>  
-   <span data-ttu-id="58593-165">Componenti nell'Ubicazione =  *VUOTO*</span><span class="sxs-lookup"><span data-stu-id="58593-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="58593-166">Caso 4.1: domanda nell'ubicazione  *BLU*</span><span class="sxs-lookup"><span data-stu-id="58593-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="58593-167">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino =  *Lotto-per-Lotto* ( *Ordine* rimane  *Ordine*), Includi Giacenze =  *Sì*, tutti gli altri parametri di pianificazione vuoti.</span><span class="sxs-lookup"><span data-stu-id="58593-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="58593-168">Caso 4.2: domanda nell'ubicazione  *VUOTA*</span><span class="sxs-lookup"><span data-stu-id="58593-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="58593-169">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="58593-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="58593-170">Come risulta evidente dall'ultimo scenario, l'unico modo per ottenere un risultato corretto per una riga della domanda senza un codice ubicazione consiste nel disabilitare i valori di setup relativi alle ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="58593-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="58593-171">In modo analogo, l'unico modo per ottenere risultati di pianificazione stabili per la domanda nelle ubicazioni consiste nell'utilizzare le unità di stockkeeping.</span><span class="sxs-lookup"><span data-stu-id="58593-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="58593-172">Se si esegue spesso la pianificazione per la domanda nelle ubicazioni, si consiglia pertanto di utilizzare la funzionalità Unità di Stockkeeping.</span><span class="sxs-lookup"><span data-stu-id="58593-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="58593-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58593-173">See Also</span></span>
<span data-ttu-id="58593-174">[Pianif.](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="58593-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="58593-175">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="58593-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="58593-176">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="58593-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="58593-177">Magazzino</span><span class="sxs-lookup"><span data-stu-id="58593-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="58593-178">Acquisti</span><span class="sxs-lookup"><span data-stu-id="58593-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="58593-179">[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="58593-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="58593-180">Impostare le procedure ottimali: Pianificazione forniture</span><span class="sxs-lookup"><span data-stu-id="58593-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="58593-181">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58593-181">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
