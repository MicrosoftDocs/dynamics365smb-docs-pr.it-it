---
title: 'Dettagli di progettazione: Domanda e approvvigionamento | Microsoft Docs'
description: Questo argomento introduce il concetto di domanda, ovvero il termine comune utilizzato per tutti i tipi di domanda lorda, ad esempio un ordine di vendita e un componente necessario da un ordine di produzione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cbafba8d012244b10c142912b357188a1f7eece4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386951"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="d0e06-103">Dettagli di progettazione: Domanda nell'ubicazione Vuota</span><span class="sxs-lookup"><span data-stu-id="d0e06-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="d0e06-104">Quando un utente crea un evento di domanda, ad esempio una riga dell'ordine di vendita, il programma consente a volte all'utente di specificare un codice ubicazione e in altre non lo consente, ovvero viene utilizzata un'ubicazione vuota.</span><span class="sxs-lookup"><span data-stu-id="d0e06-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="d0e06-105">Per la domanda con o senza codici ubicazione, il sistema di pianificazione agisce in modo diretto nei casi indicati di seguito.</span><span class="sxs-lookup"><span data-stu-id="d0e06-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="d0e06-106">Le righe della domanda includono sempre codici ubicazione e il sistema utilizza completamente le USK, incluso il setup dell'ubicazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="d0e06-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="d0e06-107">Le righe della domanda non includono mai i codici ubicazione e il sistema non utilizza le USK o il setup dell'ubicazione (come nel caso dell'ultimo scenario riportato di seguito).</span><span class="sxs-lookup"><span data-stu-id="d0e06-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="d0e06-108">Se tuttavia i codici ubicazione sono a volte inclusi e a volte non inclusi negli eventi della domanda, il sistema di pianificazione segue regole specifiche in base al setup.</span><span class="sxs-lookup"><span data-stu-id="d0e06-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="d0e06-109">Domanda nell'ubicazione</span><span class="sxs-lookup"><span data-stu-id="d0e06-109">Demand at Location</span></span>
<span data-ttu-id="d0e06-110">In caso di rilevamento di una domanda in corrispondenza di un'ubicazione, il funzionamento del sistema di pianificazione varia in base a tre importanti valori di setup.</span><span class="sxs-lookup"><span data-stu-id="d0e06-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="d0e06-111">Durante l'esecuzione della pianificazione, viene eseguito il controllo dei tre valori di setup in sequenza, quindi la pianificazione viene eseguita in base a tali valori.</span><span class="sxs-lookup"><span data-stu-id="d0e06-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="d0e06-112">Viene verificata la presenza di un segno di spunta nel campo **Ubicazione Obbligatoria**.</span><span class="sxs-lookup"><span data-stu-id="d0e06-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="d0e06-113">In caso affermativo</span><span class="sxs-lookup"><span data-stu-id="d0e06-113">If yes, then:</span></span>

2. <span data-ttu-id="d0e06-114">Viene verificata la presenza dell'unità di stockkeeping (USK) per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="d0e06-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="d0e06-115">In caso affermativo</span><span class="sxs-lookup"><span data-stu-id="d0e06-115">If yes, then:</span></span>

    <span data-ttu-id="d0e06-116">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK.</span><span class="sxs-lookup"><span data-stu-id="d0e06-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="d0e06-117">In caso negativo</span><span class="sxs-lookup"><span data-stu-id="d0e06-117">If no, then:</span></span>

3. <span data-ttu-id="d0e06-118">Viene verificata la presenza del codice ubicazione richiesto nel campo Componenti nell'Ubicazione.</span><span class="sxs-lookup"><span data-stu-id="d0e06-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="d0e06-119">In caso affermativo</span><span class="sxs-lookup"><span data-stu-id="d0e06-119">If yes, then:</span></span>

  <span data-ttu-id="d0e06-120">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="d0e06-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="d0e06-121">In caso negativo</span><span class="sxs-lookup"><span data-stu-id="d0e06-121">If no, then:</span></span>

  <span data-ttu-id="d0e06-122">L'articolo viene pianificato in base a quanto segue: Metodi di Riordino = Lotto-per-Lotto, Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti, articoli che utilizzano il Metodo di riordino = Il sistema continuerà a utilizzare l'Ordine e tutte le altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="d0e06-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d0e06-123">L'impostazione della pianificazione eccezionale che viene resa come l'ultima reazione nel passaggio 3 precedente viene indicata di seguito come "l'alternativa minima".</span><span class="sxs-lookup"><span data-stu-id="d0e06-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="d0e06-124">Questa impostazione di pianificazione copre solo la domanda esatta e tutti gli altri parametri di pianificazione vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="d0e06-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="d0e06-125">Per informazioni sulle variazioni della logica di pianificazione, vedere la sezione relativa agli scenari di seguito riportata.</span><span class="sxs-lookup"><span data-stu-id="d0e06-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="d0e06-126">Domanda nell'ubicazione vuota</span><span class="sxs-lookup"><span data-stu-id="d0e06-126">Demand at Blank Location</span></span>
<span data-ttu-id="d0e06-127">Anche se il campo **Ubicazione obbligatoria** è selezionato, il programma consentirà la creazione delle righe della domanda senza un codice ubicazione, definita anche come ubicazione vuota.</span><span class="sxs-lookup"><span data-stu-id="d0e06-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="d0e06-128">Si tratta di una deviazione per il sistema perché dispone di diversi valori setup ottimizzati per gestire le ubicazioni (vedere sopra) e di conseguenza il motore di pianificazione non creerà una riga di pianificazione per tale riga della domanda.</span><span class="sxs-lookup"><span data-stu-id="d0e06-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="d0e06-129">Se il campo **Ubicazione obbligatoria** non è selezionato ma è presente uno dei valori di impostazione ubicazione disponibili, verrà considerato una deviazione e il sistema di pianificazione reagirà utilizzando un'"alternativa minima". L'articolo viene pianificato in base a: metodo di riordino = lotto per lotto (ordine rimane ordine), Includi giacenze = Sì, tutti gli altri parametri di pianificazione = vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0e06-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="d0e06-130">Scenari</span><span class="sxs-lookup"><span data-stu-id="d0e06-130">Scenarios</span></span>
<span data-ttu-id="d0e06-131">Gli scenari seguenti descrivono le variazioni di domanda nell'ubicazione vuota e come il sistema di pianificazione risolve con "un'alternativa minima".</span><span class="sxs-lookup"><span data-stu-id="d0e06-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="d0e06-132">Setup 1:</span><span class="sxs-lookup"><span data-stu-id="d0e06-132">Setup 1:</span></span>
<span data-ttu-id="d0e06-133">Ubicazione Obbligatoria = Sì</span><span class="sxs-lookup"><span data-stu-id="d0e06-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="d0e06-134">Unità di stockkeeping impostate su ROSSO</span><span class="sxs-lookup"><span data-stu-id="d0e06-134">SKU is set up for RED</span></span>

<span data-ttu-id="d0e06-135">Componenti nell'ubicazione = BLU</span><span class="sxs-lookup"><span data-stu-id="d0e06-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="d0e06-136">Caso 1.1: domanda nell'ubicazione ROSSA</span><span class="sxs-lookup"><span data-stu-id="d0e06-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="d0e06-137">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda USK.</span><span class="sxs-lookup"><span data-stu-id="d0e06-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="d0e06-138">Caso 1.2: domanda nell'ubicazione BLU</span><span class="sxs-lookup"><span data-stu-id="d0e06-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="d0e06-139">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0e06-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="d0e06-140">Caso 1.3: domanda nell'ubicazione VERDE</span><span class="sxs-lookup"><span data-stu-id="d0e06-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="d0e06-141">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0e06-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="d0e06-142">Caso 1.4: domanda nell'ubicazione VUOTA</span><span class="sxs-lookup"><span data-stu-id="d0e06-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="d0e06-143">L'articolo non viene pianificato perché non è definita alcuna ubicazione nella riga della domanda.</span><span class="sxs-lookup"><span data-stu-id="d0e06-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="d0e06-144">Setup 2:</span><span class="sxs-lookup"><span data-stu-id="d0e06-144">Setup 2:</span></span>
<span data-ttu-id="d0e06-145">Ubicazione Obbligatoria = Sì</span><span class="sxs-lookup"><span data-stu-id="d0e06-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="d0e06-146">Nessuna USK esistente</span><span class="sxs-lookup"><span data-stu-id="d0e06-146">No SKU exists</span></span>

<span data-ttu-id="d0e06-147">Componenti nell'ubicazione = BLU</span><span class="sxs-lookup"><span data-stu-id="d0e06-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="d0e06-148">Caso 2.1: domanda nell'ubicazione ROSSA</span><span class="sxs-lookup"><span data-stu-id="d0e06-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="d0e06-149">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0e06-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="d0e06-150">Caso 2.2: domanda nell'ubicazione BLU</span><span class="sxs-lookup"><span data-stu-id="d0e06-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="d0e06-151">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="d0e06-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="d0e06-152">Setup 3:</span><span class="sxs-lookup"><span data-stu-id="d0e06-152">Setup 3:</span></span>
<span data-ttu-id="d0e06-153">Ubicazione Obbligatoria = No</span><span class="sxs-lookup"><span data-stu-id="d0e06-153">Location Mandatory = No</span></span>

<span data-ttu-id="d0e06-154">Nessuna USK esistente</span><span class="sxs-lookup"><span data-stu-id="d0e06-154">No SKU exists</span></span>

<span data-ttu-id="d0e06-155">Componenti nell'ubicazione = BLU</span><span class="sxs-lookup"><span data-stu-id="d0e06-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="d0e06-156">Caso 3.1: domanda nell'ubicazione ROSSA</span><span class="sxs-lookup"><span data-stu-id="d0e06-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="d0e06-157">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0e06-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="d0e06-158">Caso 3.2: domanda nell'ubicazione BLU</span><span class="sxs-lookup"><span data-stu-id="d0e06-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="d0e06-159">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="d0e06-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="d0e06-160">Caso 3.3: domanda nell'ubicazione VUOTA</span><span class="sxs-lookup"><span data-stu-id="d0e06-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="d0e06-161">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0e06-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="d0e06-162">Setup 4:</span><span class="sxs-lookup"><span data-stu-id="d0e06-162">Setup 4:</span></span>
<span data-ttu-id="d0e06-163">Ubicazione Obbligatoria = No</span><span class="sxs-lookup"><span data-stu-id="d0e06-163">Location Mandatory = No</span></span>

<span data-ttu-id="d0e06-164">Nessuna USK esistente</span><span class="sxs-lookup"><span data-stu-id="d0e06-164">No SKU exists</span></span>

<span data-ttu-id="d0e06-165">Componenti nell'ubicazione = VUOTO</span><span class="sxs-lookup"><span data-stu-id="d0e06-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="d0e06-166">Caso 4.1: domanda nell'ubicazione BLU</span><span class="sxs-lookup"><span data-stu-id="d0e06-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="d0e06-167">L'articolo viene pianificato in base a quanto segue: Metodo di Riordino = Lotto-per-Lotto (Ordine rimane Ordine), Includi Giacenze = Sì, tutti gli altri parametri di pianificazione = Vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0e06-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="d0e06-168">Caso 4.2: domanda nell'ubicazione VUOTA</span><span class="sxs-lookup"><span data-stu-id="d0e06-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="d0e06-169">L'articolo viene pianificato in base ai parametri di pianificazione nella scheda articolo.</span><span class="sxs-lookup"><span data-stu-id="d0e06-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="d0e06-170">Come illustrato nell'ultimo scenario, l'unico modo per ottenere un risultato corretto per una riga della domanda senza un codice ubicazione consiste nel disabilitare i valori di setup relativi alle ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="d0e06-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="d0e06-171">In modo analogo, l'unico modo per ottenere risultati di pianificazione stabili per la domanda nelle ubicazioni consiste nell'utilizzare le USK.</span><span class="sxs-lookup"><span data-stu-id="d0e06-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="d0e06-172">Se le società eseguono spesso la pianificazione per la domanda nelle ubicazioni, si consiglia pertanto di utilizzare l'area Unità di Stockkeeping.</span><span class="sxs-lookup"><span data-stu-id="d0e06-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0e06-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d0e06-173">See Also</span></span>  
<span data-ttu-id="d0e06-174">[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="d0e06-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="d0e06-175">[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="d0e06-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="d0e06-176">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="d0e06-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]