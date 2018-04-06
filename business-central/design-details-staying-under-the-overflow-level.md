---
title: 'Dettagli di progettazione: Al di sotto del livello di overflow | Microsoft Docs'
description: "Quando si utilizzano i campo Qtà Massima e Qtà Riordino Fissa, il sistema di pianificazione si concentra solo sulle giacenze previste nell'intervallo di tempo specificato. Ciò significa che il sistema di pianificazione può suggerire un approvvigionamento superfluo quando si verificano dei cambiamenti nella domanda negativa o nell'approvvigionamento positivo al di fuori dell'intervallo di tempo specificato."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2fc2ef2528a1edc85c0a7694c1afc5bec7a0065a
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="444e1-104">Dettagli di progettazione: Al di sotto del livello di overflow</span><span class="sxs-lookup"><span data-stu-id="444e1-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="444e1-105">Quando si utilizzano i metodi Qtà Massima e Qtà Riordino Fissa, il sistema di pianificazione si concentra solo sulle giacenze previste nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="444e1-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="444e1-106">Ciò significa che il sistema di pianificazione può suggerire un approvvigionamento superfluo quando si verificano dei cambiamenti nella domanda negativa o nell'approvvigionamento positivo al di fuori dell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="444e1-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="444e1-107">Se, per questo motivo, viene suggerito un approvvigionamento inutile, il sistema di pianificazione calcola la quantità alla quale l'approvvigionamento dovrebbe essere ridotto (o eliminato) per evitare l'approvvigionamento superfluo.</span><span class="sxs-lookup"><span data-stu-id="444e1-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="444e1-108">Questa quantità è denominata “livello di overflow”.</span><span class="sxs-lookup"><span data-stu-id="444e1-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="444e1-109">L'overflow viene comunicato come una riga di pianificazione con un'azione **Cambia Qtà (riduzione)** o **Annulla** e il seguente messaggio di avviso:</span><span class="sxs-lookup"><span data-stu-id="444e1-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="444e1-110">*Attenzione: La giacenza disponibile [xx] è superiore al livello di overflow [xx] alla data di scadenza [xx].*</span><span class="sxs-lookup"><span data-stu-id="444e1-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="444e1-111">![Livello di overflow della giacenza](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span><span class="sxs-lookup"><span data-stu-id="444e1-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="444e1-112">Calcolo del livello di overflow</span><span class="sxs-lookup"><span data-stu-id="444e1-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="444e1-113">Il livello di overflow viene calcolato in modi diversi a seconda dell'impostazione della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="444e1-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="444e1-114">Metodo di riordino di Qtà Massima</span><span class="sxs-lookup"><span data-stu-id="444e1-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="444e1-115">Livello di overflow = giacenza massima</span><span class="sxs-lookup"><span data-stu-id="444e1-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="444e1-116">Se è presente una quantità ordine minima, verrà aggiunta come segue: Livello di overflow = giacenza massima + quantità ordine minima.</span><span class="sxs-lookup"><span data-stu-id="444e1-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="444e1-117">Metodo di riordino Qtà Riordino Fissa</span><span class="sxs-lookup"><span data-stu-id="444e1-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="444e1-118">Livello di overflow = quantità di riordino + punto di riordino</span><span class="sxs-lookup"><span data-stu-id="444e1-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="444e1-119">Se la quantità di ordine minima è superiore al punto di riordino, sarà sostituita come segue: Livello di overflow = quantità di riordino + quantità ordine minima</span><span class="sxs-lookup"><span data-stu-id="444e1-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="444e1-120">Molteplicità ordine</span><span class="sxs-lookup"><span data-stu-id="444e1-120">Order Multiple</span></span>  
<span data-ttu-id="444e1-121">In presenza di una molteplicità di ordini, verrà rettificato il livello di overflow per i metodi di riordino sia Quantità massima che Quantità riordino fissa.</span><span class="sxs-lookup"><span data-stu-id="444e1-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="444e1-122">Creazione della riga di pianificazione con avviso di overflow</span><span class="sxs-lookup"><span data-stu-id="444e1-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="444e1-123">Quando un approvvigionamento esistente determina un aumento della giacenza disponibile oltre il livello di overflow alla fine di un intervallo di tempo, viene creata una riga di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="444e1-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="444e1-124">Per avvisare del potenziale approvvigionamento superfluo, la riga di pianificazione contiene un messaggio di avviso, il campo **Accetta messaggio azione** non è selezionato e il messaggio di azione è Annulla o Cambia Qtà.</span><span class="sxs-lookup"><span data-stu-id="444e1-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="444e1-125">Calcolo della quantità della riga di pianificazione</span><span class="sxs-lookup"><span data-stu-id="444e1-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="444e1-126">Quantità della riga di pianificazione = quantità dell'approvvigionamento corrente - (scorte previste - livello di overflow)</span><span class="sxs-lookup"><span data-stu-id="444e1-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="444e1-127">Analogamente a tutte le righe di avviso, tutte le quantità ordine minime e massime o di ordine multiplo verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="444e1-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="444e1-128">Definizione del tipo di messaggio di azione</span><span class="sxs-lookup"><span data-stu-id="444e1-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="444e1-129">Se la quantità della riga di pianificazione è uguale o superiore a 0, il messaggio di azione sarà Cambia qtà.</span><span class="sxs-lookup"><span data-stu-id="444e1-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="444e1-130">Se la quantità della riga di pianificazione è uguale o inferiore a 0, il messaggio di azione sarà pari ad Annulla</span><span class="sxs-lookup"><span data-stu-id="444e1-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="444e1-131">Composizione del messaggio di avviso</span><span class="sxs-lookup"><span data-stu-id="444e1-131">Composing the Warning Message</span></span>  
<span data-ttu-id="444e1-132">In caso di overflow, nella finestra **Elementi di pianificazione non tracciati** viene visualizzato un messaggio di avviso con le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="444e1-132">In case of overflow, the **Untracked Planning Elements** window displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="444e1-133">Livello di giacenza disponibile che ha attivato l'avviso</span><span class="sxs-lookup"><span data-stu-id="444e1-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="444e1-134">Livello di overflow calcolato</span><span class="sxs-lookup"><span data-stu-id="444e1-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="444e1-135">Data di scadenza dell'evento di approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="444e1-135">The due date of the supply event.</span></span>  

<span data-ttu-id="444e1-136">Esempio: "La giacenza disponibile 120 è superiore al livello di overflow 60 in 28-01-11”</span><span class="sxs-lookup"><span data-stu-id="444e1-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="444e1-137">Scenario</span><span class="sxs-lookup"><span data-stu-id="444e1-137">Scenario</span></span>  
<span data-ttu-id="444e1-138">In questo scenario, un cliente modifica un ordine di vendita da 70 a 40 pezzi tra due esecuzioni di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="444e1-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="444e1-139">La funzionalità di overflow consente di ridurre l'acquisto che è stato suggerito per la quantità di vendita iniziale.</span><span class="sxs-lookup"><span data-stu-id="444e1-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="444e1-140">Impostazione articolo</span><span class="sxs-lookup"><span data-stu-id="444e1-140">Item setup</span></span>  

|<span data-ttu-id="444e1-141">Metodo di riordino</span><span class="sxs-lookup"><span data-stu-id="444e1-141">Reordering Policy</span></span>|<span data-ttu-id="444e1-142">Qtà Massima</span><span class="sxs-lookup"><span data-stu-id="444e1-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="444e1-143">Quantità massima ordine</span><span class="sxs-lookup"><span data-stu-id="444e1-143">Maximum Order Quantity</span></span>|<span data-ttu-id="444e1-144">100</span><span class="sxs-lookup"><span data-stu-id="444e1-144">100</span></span>|  
|<span data-ttu-id="444e1-145">Punto riordino</span><span class="sxs-lookup"><span data-stu-id="444e1-145">Reorder Point</span></span>|<span data-ttu-id="444e1-146">50</span><span class="sxs-lookup"><span data-stu-id="444e1-146">50</span></span>|  
|<span data-ttu-id="444e1-147">Magazzino</span><span class="sxs-lookup"><span data-stu-id="444e1-147">Inventory</span></span>|<span data-ttu-id="444e1-148">80</span><span class="sxs-lookup"><span data-stu-id="444e1-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="444e1-149">Situazione prima della riduzione della vendita</span><span class="sxs-lookup"><span data-stu-id="444e1-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="444e1-150">Evento</span><span class="sxs-lookup"><span data-stu-id="444e1-150">Event</span></span>|<span data-ttu-id="444e1-151">Cambia Qtà</span><span class="sxs-lookup"><span data-stu-id="444e1-151">Change Qty.</span></span>|<span data-ttu-id="444e1-152">Quantità scorte previste</span><span class="sxs-lookup"><span data-stu-id="444e1-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="444e1-153">Giorno uno</span><span class="sxs-lookup"><span data-stu-id="444e1-153">Day one</span></span>|<span data-ttu-id="444e1-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="444e1-154">None</span></span>|<span data-ttu-id="444e1-155">80</span><span class="sxs-lookup"><span data-stu-id="444e1-155">80</span></span>|  
|<span data-ttu-id="444e1-156">Vendite</span><span class="sxs-lookup"><span data-stu-id="444e1-156">Sale</span></span>|<span data-ttu-id="444e1-157">-70</span><span class="sxs-lookup"><span data-stu-id="444e1-157">-70</span></span>|<span data-ttu-id="444e1-158">10</span><span class="sxs-lookup"><span data-stu-id="444e1-158">10</span></span>|  
|<span data-ttu-id="444e1-159">Fine dell'intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="444e1-159">End of time bucket</span></span>|<span data-ttu-id="444e1-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="444e1-160">None</span></span>|<span data-ttu-id="444e1-161">10</span><span class="sxs-lookup"><span data-stu-id="444e1-161">10</span></span>|  
|<span data-ttu-id="444e1-162">Suggerire nuovo ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="444e1-162">Suggest new purchase order</span></span>|<span data-ttu-id="444e1-163">+90</span><span class="sxs-lookup"><span data-stu-id="444e1-163">+90</span></span>|<span data-ttu-id="444e1-164">100</span><span class="sxs-lookup"><span data-stu-id="444e1-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="444e1-165">Situazione dopo la riduzione della vendita</span><span class="sxs-lookup"><span data-stu-id="444e1-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="444e1-166">Cambia</span><span class="sxs-lookup"><span data-stu-id="444e1-166">Change</span></span>|<span data-ttu-id="444e1-167">Cambia Qtà</span><span class="sxs-lookup"><span data-stu-id="444e1-167">Change Qty.</span></span>|<span data-ttu-id="444e1-168">Quantità scorte previste</span><span class="sxs-lookup"><span data-stu-id="444e1-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="444e1-169">Giorno uno</span><span class="sxs-lookup"><span data-stu-id="444e1-169">Day one</span></span>|<span data-ttu-id="444e1-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="444e1-170">None</span></span>|<span data-ttu-id="444e1-171">80</span><span class="sxs-lookup"><span data-stu-id="444e1-171">80</span></span>|  
|<span data-ttu-id="444e1-172">Vendite</span><span class="sxs-lookup"><span data-stu-id="444e1-172">Sale</span></span>|<span data-ttu-id="444e1-173">-40</span><span class="sxs-lookup"><span data-stu-id="444e1-173">-40</span></span>|<span data-ttu-id="444e1-174">40</span><span class="sxs-lookup"><span data-stu-id="444e1-174">40</span></span>|  
|<span data-ttu-id="444e1-175">Acquisti</span><span class="sxs-lookup"><span data-stu-id="444e1-175">Purchase</span></span>|<span data-ttu-id="444e1-176">+90</span><span class="sxs-lookup"><span data-stu-id="444e1-176">+90</span></span>|<span data-ttu-id="444e1-177">130</span><span class="sxs-lookup"><span data-stu-id="444e1-177">130</span></span>|  
|<span data-ttu-id="444e1-178">Fine dell'intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="444e1-178">End of time bucket</span></span>|<span data-ttu-id="444e1-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="444e1-179">None</span></span>|<span data-ttu-id="444e1-180">130</span><span class="sxs-lookup"><span data-stu-id="444e1-180">130</span></span>|  
|<span data-ttu-id="444e1-181">Suggerire di ridurre l'acquisto</span><span class="sxs-lookup"><span data-stu-id="444e1-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="444e1-182">ordine di acquisto da 90 a 60</span><span class="sxs-lookup"><span data-stu-id="444e1-182">order from 90 to 60</span></span>|<span data-ttu-id="444e1-183">-30</span><span class="sxs-lookup"><span data-stu-id="444e1-183">-30</span></span>|<span data-ttu-id="444e1-184">100</span><span class="sxs-lookup"><span data-stu-id="444e1-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="444e1-185">Righe pianificazione risultanti</span><span class="sxs-lookup"><span data-stu-id="444e1-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="444e1-186">Una riga di pianificazione (avviso) viene creata per ridurre l'acquisto di 30 da 90 a 60 per mantenere la giacenza disponibile su 100 in base al livello di overflow.</span><span class="sxs-lookup"><span data-stu-id="444e1-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="444e1-187">![Pianificazione in base al livello di overflow](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span><span class="sxs-lookup"><span data-stu-id="444e1-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="444e1-188">Senza la funzionalità di overflow, nessun avviso viene creato se il livello di giacenza disponibile è superiore alla giacenza massima.</span><span class="sxs-lookup"><span data-stu-id="444e1-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="444e1-189">Potrebbe verificarsi un approvvigionamento superfluo di 30.</span><span class="sxs-lookup"><span data-stu-id="444e1-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="444e1-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="444e1-190">See Also</span></span>  
<span data-ttu-id="444e1-191">[Dettagli di progettazione: Metodi di riordino](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="444e1-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="444e1-192">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="444e1-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="444e1-193">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="444e1-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="444e1-194">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="444e1-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

