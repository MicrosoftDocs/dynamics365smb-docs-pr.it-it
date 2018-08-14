---
title: Impostare gli intervalli di date in Business Central | Documenti Microsoft
description: Informazioni su come ottenere un report per visualizzare i dati relativi a periodi di tempo specifici utilizzando gli intervalli di date in Business Central.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: it-it
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="c09c1-103">Immettere intervalli di date</span><span class="sxs-lookup"><span data-stu-id="c09c1-103">Entering Date Ranges</span></span>
<span data-ttu-id="c09c1-104">È possibile impostare filtri contenenti una data di inizio e una data di fine per visualizzare solo la data inclusa in un intervallo di date o di ore specifico.</span><span class="sxs-lookup"><span data-stu-id="c09c1-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="c09c1-105">All'impostazione di intervalli di date si applicano regole speciali.</span><span class="sxs-lookup"><span data-stu-id="c09c1-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="c09c1-106">Si consideri come esempio la **Lista primi 10 clienti**:</span><span class="sxs-lookup"><span data-stu-id="c09c1-106">Let's take the **Customer Top 10** as an example:</span></span>

![Impostare un intervallo di date nella pagina di richiesta per la Lista primi 10 clienti](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="c09c1-108">In questo campo è possibile limitare il report a un intervallo di date, ad esempio, alle ultime 2 settimane o a un totale di 6 settimane o a qualsiasi intervallo che si desidera.</span><span class="sxs-lookup"><span data-stu-id="c09c1-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="c09c1-109">Per impostare gli intervalli di date, immettere le date quindi utilizzare **..**</span><span class="sxs-lookup"><span data-stu-id="c09c1-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="c09c1-110">o **|** per impostare l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="c09c1-110">or **|** to set the range.</span></span> <span data-ttu-id="c09c1-111">Nell'esempio, per visualizzare i 10 clienti principali per le prime 2 settimane di maggio, impostare il filtro data come *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="c09c1-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="c09c1-112">Di seguito vengono proposti altri esempi:</span><span class="sxs-lookup"><span data-stu-id="c09c1-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="c09c1-113">Significato</span><span class="sxs-lookup"><span data-stu-id="c09c1-113">Meaning</span></span> | <span data-ttu-id="c09c1-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="c09c1-114">Example</span></span> | <span data-ttu-id="c09c1-115">movimenti inclusi</span><span class="sxs-lookup"><span data-stu-id="c09c1-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="c09c1-116">uguale a</span><span class="sxs-lookup"><span data-stu-id="c09c1-116">Equal to</span></span>| <span data-ttu-id="c09c1-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="c09c1-117">12 15 16</span></span> |<span data-ttu-id="c09c1-118">Solo i movimenti registrati il 15 dicembre 2016.</span><span class="sxs-lookup"><span data-stu-id="c09c1-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="c09c1-119">intervallo</span><span class="sxs-lookup"><span data-stu-id="c09c1-119">Interval</span></span>| <span data-ttu-id="c09c1-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="c09c1-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="c09c1-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="c09c1-121">..12 15 16</span></span>|<span data-ttu-id="c09c1-122">Movimenti registrati in date comprese tra il 15 dicembre 2016 e il 15 gennaio 2017, inclusi.</span><span class="sxs-lookup"><span data-stu-id="c09c1-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="c09c1-123">Movimenti registrati prima del 15 dicembre 2016, incluso.</span><span class="sxs-lookup"><span data-stu-id="c09c1-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="c09c1-124">oppure</span><span class="sxs-lookup"><span data-stu-id="c09c1-124">Either/or</span></span>|<span data-ttu-id="c09c1-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="c09c1-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="c09c1-126">Movimenti registrati il 15 dicembre o il 16 dicembre 2016.</span><span class="sxs-lookup"><span data-stu-id="c09c1-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="c09c1-127">Se sono presenti movimenti registrati in entrambi i giorni, verranno visualizzati tutti.</span><span class="sxs-lookup"><span data-stu-id="c09c1-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="c09c1-128">È inoltre possibile combinare i vari tipi di formato.</span><span class="sxs-lookup"><span data-stu-id="c09c1-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="c09c1-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="c09c1-129">Example</span></span> | <span data-ttu-id="c09c1-130">movimenti inclusi</span><span class="sxs-lookup"><span data-stu-id="c09c1-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="c09c1-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="c09c1-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="c09c1-132">Movimenti registrati il 15 dicembre 2016 o in date comprese tra il 01° dicembre 2016 e il 31 maggio 2017 inclusi.</span><span class="sxs-lookup"><span data-stu-id="c09c1-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="c09c1-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="c09c1-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="c09c1-134">Movimenti registrati il 14 dicembre, o in giorni precedenti, o movimenti registrati il 30 dicembre, o successivamente, ossia tutti i movimenti esclusi quelli registrati in date comprese tra il 15 e il 29 dicembre, incluse.</span><span class="sxs-lookup"><span data-stu-id="c09c1-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="c09c1-135">Si noti che negli esempi è stato utilizzato il formato data MMGGAA degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="c09c1-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="c09c1-136">Quando [!INCLUDE[d365fin](includes/d365fin_md.md)] sarà disponibile in altri mercati, sarà possibile utilizzare i formati abituali per il proprio paese.</span><span class="sxs-lookup"><span data-stu-id="c09c1-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="c09c1-137">Utilizzo di formule per le date</span><span class="sxs-lookup"><span data-stu-id="c09c1-137">Using Date Formulas</span></span>
<span data-ttu-id="c09c1-138">Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date.</span><span class="sxs-lookup"><span data-stu-id="c09c1-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="c09c1-139">È possibile immettere formule per le date in diversi campi di calcolo e in campi relativi alla frequenza della ricorrenza in registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="c09c1-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="c09c1-140">In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo.</span><span class="sxs-lookup"><span data-stu-id="c09c1-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="c09c1-141">Di conseguenza, se si immette, ad esempio, **1W**, il periodo è effettivamente di otto giorni perché la data odierna è inclusa.</span><span class="sxs-lookup"><span data-stu-id="c09c1-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="c09c1-142">Per specificare un periodo di sette giorni (una settimana vera) includendo la data di inizio del periodo, è necessario immettere **6D** o **1W\-1D**.</span><span class="sxs-lookup"><span data-stu-id="c09c1-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="c09c1-143">Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:</span><span class="sxs-lookup"><span data-stu-id="c09c1-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="c09c1-144">La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.</span><span class="sxs-lookup"><span data-stu-id="c09c1-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="c09c1-145">La formula nel campo **Periodo di dilazione** per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza (o dalla data di scadenza del sollecito precedente) alla creazione del sollecito.</span><span class="sxs-lookup"><span data-stu-id="c09c1-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="c09c1-146">La formula nel campo **Calcolo data di scadenza** determina la modalità di calcolo della data di scadenza nel sollecito.</span><span class="sxs-lookup"><span data-stu-id="c09c1-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="c09c1-147">La formula per il calcolo della data può contenere un massimo di 20 caratteri, sia numeri che lettere.</span><span class="sxs-lookup"><span data-stu-id="c09c1-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="c09c1-148">È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di tempo diverse.</span><span class="sxs-lookup"><span data-stu-id="c09c1-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="c09c1-149">Lettera</span><span class="sxs-lookup"><span data-stu-id="c09c1-149">Letter</span></span>  |  <span data-ttu-id="c09c1-150">Specifica temporale</span><span class="sxs-lookup"><span data-stu-id="c09c1-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="c09c1-151">C</span><span class="sxs-lookup"><span data-stu-id="c09c1-151">C</span></span>|<span data-ttu-id="c09c1-152">Corrente</span><span class="sxs-lookup"><span data-stu-id="c09c1-152">Current</span></span>|
|<span data-ttu-id="c09c1-153">D</span><span class="sxs-lookup"><span data-stu-id="c09c1-153">D</span></span>|<span data-ttu-id="c09c1-154">Giorno\(i\)</span><span class="sxs-lookup"><span data-stu-id="c09c1-154">Day\(s\)</span></span>|
|<span data-ttu-id="c09c1-155">OVEST</span><span class="sxs-lookup"><span data-stu-id="c09c1-155">W</span></span>|<span data-ttu-id="c09c1-156">Settimana\(e\)</span><span class="sxs-lookup"><span data-stu-id="c09c1-156">Week\(s\)</span></span>|
|<span data-ttu-id="c09c1-157">M</span><span class="sxs-lookup"><span data-stu-id="c09c1-157">M</span></span>|<span data-ttu-id="c09c1-158">Mese\(i\)</span><span class="sxs-lookup"><span data-stu-id="c09c1-158">Month\(s\)</span></span>|
|<span data-ttu-id="c09c1-159">T</span><span class="sxs-lookup"><span data-stu-id="c09c1-159">Q</span></span>|<span data-ttu-id="c09c1-160">Trimestre\(i\)</span><span class="sxs-lookup"><span data-stu-id="c09c1-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="c09c1-161">A</span><span class="sxs-lookup"><span data-stu-id="c09c1-161">Y</span></span>|<span data-ttu-id="c09c1-162">Anno\(i\)</span><span class="sxs-lookup"><span data-stu-id="c09c1-162">Year\(s\)</span></span>|

<span data-ttu-id="c09c1-163">È possibile creare una formula per la data in tre modi diversi.</span><span class="sxs-lookup"><span data-stu-id="c09c1-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="c09c1-164">L'esempio seguente mostra come usare **C**, vale a dire corrente, e un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="c09c1-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="c09c1-165">Espressione</span><span class="sxs-lookup"><span data-stu-id="c09c1-165">Expression</span></span>  |  <span data-ttu-id="c09c1-166">Significato</span><span class="sxs-lookup"><span data-stu-id="c09c1-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="c09c1-167">CW</span><span class="sxs-lookup"><span data-stu-id="c09c1-167">CW</span></span>|<span data-ttu-id="c09c1-168">Settimana corrente</span><span class="sxs-lookup"><span data-stu-id="c09c1-168">Current week</span></span>|
|<span data-ttu-id="c09c1-169">CM</span><span class="sxs-lookup"><span data-stu-id="c09c1-169">CM</span></span>|<span data-ttu-id="c09c1-170">Mese corrente</span><span class="sxs-lookup"><span data-stu-id="c09c1-170">Current month</span></span>|

<span data-ttu-id="c09c1-171">L'esempio seguente mostra come usare un numero e un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="c09c1-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="c09c1-172">Il numero non può essere maggiore di 9999.</span><span class="sxs-lookup"><span data-stu-id="c09c1-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="c09c1-173">Espressione</span><span class="sxs-lookup"><span data-stu-id="c09c1-173">Expression</span></span>  |  <span data-ttu-id="c09c1-174">Significato</span><span class="sxs-lookup"><span data-stu-id="c09c1-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="c09c1-175">10D</span><span class="sxs-lookup"><span data-stu-id="c09c1-175">10D</span></span>|<span data-ttu-id="c09c1-176">10 giorni a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="c09c1-176">10 days from today</span></span>|
|<span data-ttu-id="c09c1-177">2W</span><span class="sxs-lookup"><span data-stu-id="c09c1-177">2W</span></span>|<span data-ttu-id="c09c1-178">2 settimane a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="c09c1-178">2 weeks from today</span></span>|

<span data-ttu-id="c09c1-179">L'esempio seguente mostra come usare un'unità di tempo e un numero.</span><span class="sxs-lookup"><span data-stu-id="c09c1-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="c09c1-180">Espressione</span><span class="sxs-lookup"><span data-stu-id="c09c1-180">Expression</span></span>  |  <span data-ttu-id="c09c1-181">Significato</span><span class="sxs-lookup"><span data-stu-id="c09c1-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="c09c1-182">D10</span><span class="sxs-lookup"><span data-stu-id="c09c1-182">D10</span></span>|<span data-ttu-id="c09c1-183">Il successivo giorno 10 del mese</span><span class="sxs-lookup"><span data-stu-id="c09c1-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="c09c1-184">WD4</span><span class="sxs-lookup"><span data-stu-id="c09c1-184">WD4</span></span>|<span data-ttu-id="c09c1-185">Il successivo quarto giorno della settimana \(Giovedì\)</span><span class="sxs-lookup"><span data-stu-id="c09c1-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="c09c1-186">Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c09c1-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="c09c1-187">Espressione</span><span class="sxs-lookup"><span data-stu-id="c09c1-187">Expression</span></span>  |  <span data-ttu-id="c09c1-188">Significato</span><span class="sxs-lookup"><span data-stu-id="c09c1-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="c09c1-189">CM\+10D</span><span class="sxs-lookup"><span data-stu-id="c09c1-189">CM\+10D</span></span>|<span data-ttu-id="c09c1-190">Corrente mese \+ 10 giorni</span><span class="sxs-lookup"><span data-stu-id="c09c1-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="c09c1-191">Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.</span><span class="sxs-lookup"><span data-stu-id="c09c1-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="c09c1-192">Espressione</span><span class="sxs-lookup"><span data-stu-id="c09c1-192">Expression</span></span>  |  <span data-ttu-id="c09c1-193">Significato</span><span class="sxs-lookup"><span data-stu-id="c09c1-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="c09c1-194">-1A</span><span class="sxs-lookup"><span data-stu-id="c09c1-194">-1Y</span></span>|<span data-ttu-id="c09c1-195">1 anno fa da oggi</span><span class="sxs-lookup"><span data-stu-id="c09c1-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="c09c1-196">Se l'ubicazione utilizza un calendario di base, la formula per la data immessa, ad esempio, nel campo **Durata spedizione** verrà interpretata in base ai giorni lavorativi del calendario.</span><span class="sxs-lookup"><span data-stu-id="c09c1-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="c09c1-197">Ad esempio la formula **1W** significa sette giorni lavorativi.</span><span class="sxs-lookup"><span data-stu-id="c09c1-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="c09c1-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c09c1-198">See Also</span></span>
<span data-ttu-id="c09c1-199">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c09c1-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c09c1-200">Calcolo della data per gli acquisti</span><span class="sxs-lookup"><span data-stu-id="c09c1-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="c09c1-201">Immissione di criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="c09c1-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

