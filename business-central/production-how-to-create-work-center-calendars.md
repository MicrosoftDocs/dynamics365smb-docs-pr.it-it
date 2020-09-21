---
title: Come impostare i calendari del reparto produzione | Microsoft Docs
description: In un calendario delle aree di produzione sono specificati i giorni e gli orari lavorativi, i turni, le ferie e le assenze che determinano la capacità lorda disponibile dell'area di produzione, misurata in tempo, sulla base dei valori definiti per l'efficienza e la capacità di tale area. Per la creazione e l'attivazione di un calendario delle aree di produzione sono necessarie diverse attività preliminari.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8fe746bcde1bf02c366664c02ea48029777e22ef
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777938"
---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="971a3-104">Impostare i calendari del reparto produzione</span><span class="sxs-lookup"><span data-stu-id="971a3-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="971a3-105">In un calendario delle aree di produzione o dei centri di lavoro sono specificati i giorni e gli orari lavorativi, i turni, le ferie e le assenze che determinano la capacità lorda disponibile dell'area o del centro, misurata in tempo, sulla base dei valori definiti per l'efficienza e la capacità di tale area o centro.</span><span class="sxs-lookup"><span data-stu-id="971a3-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="971a3-106">Come base per il calcolo di un calendario specifico delle aree di produzione o dei centri di lavoro è prima di tutto necessario configurare uno o più calendari del reparto produzione generali.</span><span class="sxs-lookup"><span data-stu-id="971a3-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="971a3-107">In un calendario del reparto produzione viene definita una settimana lavorativa standard in termini di ora di inizio e di fine di ogni giorno lavorativo e di relazione di turni lavorativi.</span><span class="sxs-lookup"><span data-stu-id="971a3-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="971a3-108">In tale calendario sono inoltre disponibili le ferie fisse nel corso di un anno.</span><span class="sxs-lookup"><span data-stu-id="971a3-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="971a3-109">Di seguito viene descritto come impostare i calendari delle aree di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="971a3-110">I passaggi sono gli stessi della procedura per l'impostazione dei calendari dei centri di lavoro.</span><span class="sxs-lookup"><span data-stu-id="971a3-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="971a3-111">Per creare turni lavorativi</span><span class="sxs-lookup"><span data-stu-id="971a3-111">To create work shifts</span></span>  
1.  <span data-ttu-id="971a3-112">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Turni lavorativi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="971a3-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="971a3-113">In una riga vuota immettere un numero nel campo **Codice** per identificare il turno lavorativo, ad esempio **1**.</span><span class="sxs-lookup"><span data-stu-id="971a3-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="971a3-114">Descrivere il turno lavorativo nel campo **Descrizione**, ad esempio **1mo Turno**.</span><span class="sxs-lookup"><span data-stu-id="971a3-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="971a3-115">Facoltativamente, compilare le righe relative a un secondo o terzo turno lavorativo.</span><span class="sxs-lookup"><span data-stu-id="971a3-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="971a3-116">Anche se nelle aree di produzione specificate non vengono effettuati turni diversi, immettere almeno un codice di turno lavorativo.</span><span class="sxs-lookup"><span data-stu-id="971a3-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="971a3-117">Per impostare un calendario reparto prod.</span><span class="sxs-lookup"><span data-stu-id="971a3-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="971a3-118">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Calendari reparto prod.** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="971a3-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="971a3-119">In una riga vuota immettere un numero nel campo **Codice** per identificare il calendario reparto prod.</span><span class="sxs-lookup"><span data-stu-id="971a3-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="971a3-120">Nel campo **Descrizione** immettere una descrizione del calendario.</span><span class="sxs-lookup"><span data-stu-id="971a3-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="971a3-121">Scegliere l'azione **Giorni lavorativi**.</span><span class="sxs-lookup"><span data-stu-id="971a3-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="971a3-122">Nella pagina **Giorni lavorativi rep. prod.**, specificare una settimana lavorativa completa, con l'ora di inizio e di fine per ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="971a3-122">On the **Shop Calendar Working Days** page, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="971a3-123">Nel campo **Cod. turno lavorativo** , selezionare uno dei turni precedentemente definiti.</span><span class="sxs-lookup"><span data-stu-id="971a3-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="971a3-124">Aggiungere una riga per ogni giorno lavorativo e ogni turno.</span><span class="sxs-lookup"><span data-stu-id="971a3-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="971a3-125">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="971a3-125">For example:</span></span>  

    <span data-ttu-id="971a3-126">Lunedì 07.00 15.00 1</span><span class="sxs-lookup"><span data-stu-id="971a3-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="971a3-127">Martedì 07.00 15.00 1</span><span class="sxs-lookup"><span data-stu-id="971a3-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="971a3-128">Se è necessario un calendario reparto prod. con due turni lavorativi, occorre compilarlo come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="971a3-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="971a3-129">Lunedì 07.00 15.00 1</span><span class="sxs-lookup"><span data-stu-id="971a3-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="971a3-130">Lunedì 15.00 23.00 2</span><span class="sxs-lookup"><span data-stu-id="971a3-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="971a3-131">Martedì 07.00 15.00 1</span><span class="sxs-lookup"><span data-stu-id="971a3-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="971a3-132">Martedì 15.00 23.00 2</span><span class="sxs-lookup"><span data-stu-id="971a3-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="971a3-133">Eventuali giorni della settimana non definiti nel calendario reparto produz., ad esempio sabato e domenica, verranno semplicemente considerati giorni non lavorativi e la relativa capacità disponibile sarà pari a zero in un calendario aree di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="971a3-134">Dopo avere definito tutti i giorni lavorativi di una settimana, è possibile chiudere la pagina **Giorni Lavorativi Rep. Prod.** e procedere all'immissione delle ferie:</span><span class="sxs-lookup"><span data-stu-id="971a3-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** page and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="971a3-135">Nella pagina **Calendari reparto prod.**, selezionare il calendario del reparto produzione, quindi scegliere l'azione **Ferie**.</span><span class="sxs-lookup"><span data-stu-id="971a3-135">On the **Shop Calendars** page, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="971a3-136">Nella pagina **Cal. festività rep. prod.**, definire le ferie dell'anno specificando l'ora e la data di inizio e fine e la descrizione di ogni festività in righe distinte.</span><span class="sxs-lookup"><span data-stu-id="971a3-136">On the **Shop Calendar Holidays** page, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="971a3-137">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="971a3-137">For example:</span></span>  

    <span data-ttu-id="971a3-138">04/07/14 0.00.00 23.59.00 Vacanze estive</span><span class="sxs-lookup"><span data-stu-id="971a3-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="971a3-139">05/07/14 0.00.00 23.59.00 Vacanze estive</span><span class="sxs-lookup"><span data-stu-id="971a3-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="971a3-140">06/07/14 0.00.00 23.59.00 Vacanze estive</span><span class="sxs-lookup"><span data-stu-id="971a3-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="971a3-141">La capacità disponibile per le ferie definite sarà pari a zero in un calendario delle aree di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="971a3-142">È ora possibile assegnare il calendario reparto prod. a un'area di produzione per calcolare il calendario reparto prod. su cui sarà basata la pianificazione di tutte le operazioni in tale area di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="971a3-143">Per calcolare un calendario aree di produzione</span><span class="sxs-lookup"><span data-stu-id="971a3-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="971a3-144">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Aree di produzione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="971a3-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="971a3-145">Aprire l'area di produzione che si desidera aggiornare.</span><span class="sxs-lookup"><span data-stu-id="971a3-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="971a3-146">Nel campo **Cod. calendario reparto prod.**, selezionare il calendario del reparto produzione da utilizzare come base per un calendario delle aree di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="971a3-147">Scegliere l'azione **Calendario**.</span><span class="sxs-lookup"><span data-stu-id="971a3-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="971a3-148">Nella pagina **Calendario aree di prod.**, scegliere l'azione **Mostra matrice**.</span><span class="sxs-lookup"><span data-stu-id="971a3-148">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="971a3-149">Nel lato sinistro della pagina della matrice sono elencate le aree di produzione configurate.</span><span class="sxs-lookup"><span data-stu-id="971a3-149">The left side of the matrix page lists the work centers that are set up.</span></span> <span data-ttu-id="971a3-150">Nella parte destra è disponibile un calendario, in cui vengono visualizzati i valori relativi alla capacità disponibile per giorno lavorativo nell'unità di misura specificata, ad esempio **480** minuti.</span><span class="sxs-lookup"><span data-stu-id="971a3-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="971a3-151">Ogni riga rappresenta il calendario relativo a un'area di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="971a3-152">È anche possibile selezionare i valori di capacità per ogni settimana o mese cambiando l'opzione del campo **Visualizza per** nella pagina **Calendario aree di prod.**.</span><span class="sxs-lookup"><span data-stu-id="971a3-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field on the **Work Center Calendar** page.</span></span>  

    <span data-ttu-id="971a3-153">Per riflettere il nuovo calendario di reparto come riga dell'area di produzione selezionata, è necessario prima calcolarlo.</span><span class="sxs-lookup"><span data-stu-id="971a3-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="971a3-154">Scegliere l'azione **Calcola**.</span><span class="sxs-lookup"><span data-stu-id="971a3-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="971a3-155">Nella Scheda dettaglio **Area di produzione** è possibile impostare un filtro per eseguire il calcolo solo per un'area di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="971a3-156">Se non si imposta alcun filtro, verranno calcolati tutti i calendari delle aree di produzione esistenti.</span><span class="sxs-lookup"><span data-stu-id="971a3-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="971a3-157">Definire la data di inizio e di fine del periodo di calendario da calcolare, ad esempio un anno, dal giorno 01/01/14 al 31/12/14.</span><span class="sxs-lookup"><span data-stu-id="971a3-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="971a3-158">Scegliere **OK** per calcolare la capacità.</span><span class="sxs-lookup"><span data-stu-id="971a3-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="971a3-159">Vengono ora creati o aggiornati i movimenti di calendario, in cui viene visualizzata la capacità disponibile per ogni periodo sulla base dei tre gruppi seguenti di dati master:</span><span class="sxs-lookup"><span data-stu-id="971a3-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="971a3-160">Giorni e turni lavorativi definiti nel calendario reparto prod. assegnato.</span><span class="sxs-lookup"><span data-stu-id="971a3-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="971a3-161">Valore specificato nel campo **Capacità** della scheda area di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="971a3-162">Valore specificato nel campo **Efficienza** della scheda dell'area di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="971a3-163">Il calendario calcolato dell'area di produzione definirà ora quando e quanta capacità è disponibile in quest'area di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="971a3-164">Ciò controlla la pianificazione dettagliata delle operazioni eseguite nell'area di produzione.</span><span class="sxs-lookup"><span data-stu-id="971a3-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="971a3-165">Per registrare un'assenza dell'area di produzione</span><span class="sxs-lookup"><span data-stu-id="971a3-165">To record work center absence</span></span>  
1.  <span data-ttu-id="971a3-166">Nella pagina **Calendario aree di prod.**, scegliere l'azione **Mostra matrice**.</span><span class="sxs-lookup"><span data-stu-id="971a3-166">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="971a3-167">Nella pagina **Matrice calendario aree di prod.** selezionare l'area di produzione e il giornio di calendario in cui registrare l'orario di assenza, quindi scegliere l'azione **Assenze**.</span><span class="sxs-lookup"><span data-stu-id="971a3-167">On the **Work Center Calendar Matrix** page, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="971a3-168">Nella pagina **Assenze** definire l'ora di inizio, l'ora di fine e la descrizione dell'assenza relativa al giorno specificato.</span><span class="sxs-lookup"><span data-stu-id="971a3-168">On the **Absence** page, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="971a3-169">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="971a3-169">For example:</span></span>  

    <span data-ttu-id="971a3-170">25/01/01 08.00 10.00 Manutenzione</span><span class="sxs-lookup"><span data-stu-id="971a3-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="971a3-171">Scegliere l'azione **Aggiorna** e chiudere la pagina **Assenze**.</span><span class="sxs-lookup"><span data-stu-id="971a3-171">Choose the **Update** action, and then close the **Absence** page.</span></span>  

<span data-ttu-id="971a3-172">La capacità del giorno selezionato risulta ora diminuita in base al tempo di assenza registrato.</span><span class="sxs-lookup"><span data-stu-id="971a3-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="971a3-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="971a3-173">See Also</span></span>  
[<span data-ttu-id="971a3-174">Impostare i calendari di base</span><span class="sxs-lookup"><span data-stu-id="971a3-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="971a3-175">Impostare aree di produzione e centri di lavoro</span><span class="sxs-lookup"><span data-stu-id="971a3-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="971a3-176">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="971a3-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="971a3-177">Manufacturing</span><span class="sxs-lookup"><span data-stu-id="971a3-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="971a3-178">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="971a3-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
