---
title: Immissione di date e ore in Business Central | Documenti Microsoft
description: Ottenere informazioni su come immettere le date e le ore inclusi suggerimenti relativi alla produttività quali abbreviazioni, espressioni e intervalli. Filtrare elenchi o report per una data o periodo specifici.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: c7e80edfd796056176d37ad12a56c76e64bb44e6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "932980"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="c9e31-104">Utilizzo di date e orari del calendario</span><span class="sxs-lookup"><span data-stu-id="c9e31-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="c9e31-105">offre diversi modi per immettere date e orari, incluse potenti funzionalità per accelerare l'immissione dei dati o scrivere espressioni di calendario complesse.</span><span class="sxs-lookup"><span data-stu-id="c9e31-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="c9e31-106">È possibile immettere date e orari nei campi in diversi punti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9e31-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="c9e31-107">Ad esempio, in un ordine di vendita, è possibile impostare la data di spedizione.</span><span class="sxs-lookup"><span data-stu-id="c9e31-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="c9e31-108">Quando si filtrano gli elenchi o i dati dei report, è possibile immettere date e orari per contrassegnare solo i dati a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="c9e31-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="c9e31-109">Verificare le impostazioni di lingua e paese</span><span class="sxs-lookup"><span data-stu-id="c9e31-109">Check your region and language settings</span></span>

<span data-ttu-id="c9e31-110">La pagina [**Impostazioni personali**](https://businesscentral.dynamics.com?page=9176 "Vai direttamente alla pagina delle impostazioni personali in Business Central") consente di specificare la **Regione** e la **Lingua** che si utilizzano nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9e31-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="c9e31-111">Queste impostazioni influenzano le modalità di immissione delle date e ore.</span><span class="sxs-lookup"><span data-stu-id="c9e31-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="c9e31-112">L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati.</span><span class="sxs-lookup"><span data-stu-id="c9e31-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="c9e31-113">Per gli schemi di date che coinvolgono le parole, la lingua delle parole utilizzate deve corrispondere all'impostazione della **Lingua**.</span><span class="sxs-lookup"><span data-stu-id="c9e31-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="c9e31-114">utilizza il sistema di calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="c9e31-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="c9e31-115">Immissione di date</span><span class="sxs-lookup"><span data-stu-id="c9e31-115">Entering Dates</span></span>

<span data-ttu-id="c9e31-116">In un campo Data, è possibile immettere una data utilizzando il formato standard per le impostazioni di un paese.</span><span class="sxs-lookup"><span data-stu-id="c9e31-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="c9e31-117">Diverse regioni possono utilizzare separatori diversi tra i giorni, i mesi e gli anni.</span><span class="sxs-lookup"><span data-stu-id="c9e31-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="c9e31-118">Ad esempio, alcune regioni utilizzano i trattini (gg-mm-aaaa) e altri usano le barre (gg/mm/aaaa).</span><span class="sxs-lookup"><span data-stu-id="c9e31-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="c9e31-119">Tuttavia, è possibile utilizzare qualsiasi separatore, anche uno spazio, e la data verrà automaticamente modificata per utilizzare separatori che corrispondono alla regione.</span><span class="sxs-lookup"><span data-stu-id="c9e31-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="c9e31-120">Si noti che il formato in cui le date vengono visualizzate sui report stampati o sui documenti inviati via e-mail non è influenzato dalla scelta personale di impostazione della regione.</span><span class="sxs-lookup"><span data-stu-id="c9e31-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="c9e31-121">Per lavorare in modo più produttivo con date e orari, è possibile utilizzare uno dei metodi o formati descritti nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9e31-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="c9e31-122">Selezionare le date dal calendario</span><span class="sxs-lookup"><span data-stu-id="c9e31-122">Picking dates from the calendar</span></span>

<span data-ttu-id="c9e31-123">Qualsiasi campo che visualizza un'icona di calendario può essere impostato utilizzando il selettore di date del calendario.</span><span class="sxs-lookup"><span data-stu-id="c9e31-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="c9e31-124">Per visualizzare il selettore di date del calendario, attivare l'icona del calendario o premere CTRL+tasto HOME nel campo.</span><span class="sxs-lookup"><span data-stu-id="c9e31-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="c9e31-125">![Campi Data](media/ui-date-field.png "Esempio di un campo data")</span><span class="sxs-lookup"><span data-stu-id="c9e31-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="c9e31-126">Vedere anche [Tasti di scelta rapida nel calendario (selezione data)](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="c9e31-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="c9e31-127">Schema giorno\-settimana\-anno</span><span class="sxs-lookup"><span data-stu-id="c9e31-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="c9e31-128">È possibile immettere una data come giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno.</span><span class="sxs-lookup"><span data-stu-id="c9e31-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="c9e31-129">Ad esempio, `Mon25` o `mon25` indica il lunedì della settimana 25.</span><span class="sxs-lookup"><span data-stu-id="c9e31-129">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="c9e31-130">Se non si immette un anno, viene utilizzato l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9e31-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="c9e31-131">Anziché immettere l'intera parola per il giorno della settimana, è possibile immettere una parte della parola, a partire dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="c9e31-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="c9e31-132">Nel caso dei conflitti (come in inglese `s` che potrebbe essere Saturday o Sunday), i giorni vengono valutati in base all'impostazione di un paese.</span><span class="sxs-lookup"><span data-stu-id="c9e31-132">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="c9e31-133">L'input viene prima valutato rispetto a `workdate` e `today`, ricordare questa informazione quando si utilizzano abbreviazioni.</span><span class="sxs-lookup"><span data-stu-id="c9e31-133">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="c9e31-134">Ad esempio, in inglese, `t` indica già oggi (today) pertanto non può significare Tuesday o Thursday.</span><span class="sxs-lookup"><span data-stu-id="c9e31-134">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="c9e31-135">Lo schema del numero della settimana è sempre ISO 8601, dove la settimana 1 è la settimana che include il 4 gennaio o la settimana con il primo giovedì dell'anno.</span><span class="sxs-lookup"><span data-stu-id="c9e31-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="c9e31-136">Schemi con cifre</span><span class="sxs-lookup"><span data-stu-id="c9e31-136">Digit patterns</span></span>

<span data-ttu-id="c9e31-137">In un campo di data è possibile immettere due, quattro, sei o otto cifre:</span><span class="sxs-lookup"><span data-stu-id="c9e31-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="c9e31-138">Se si immettono solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9e31-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="c9e31-139">Se si immettono quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9e31-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="c9e31-140">L'ordine giorno e il mese è determinato dalle impostazioni di un paese.</span><span class="sxs-lookup"><span data-stu-id="c9e31-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="c9e31-141">Anche se le impostazioni del paese hanno l'anno prima del giorno e del mese, le quattro cifre vengono interpretate come giorno e mese.</span><span class="sxs-lookup"><span data-stu-id="c9e31-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="c9e31-142">Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1930 e 31/12/2029, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="c9e31-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="c9e31-143">Oggi</span><span class="sxs-lookup"><span data-stu-id="c9e31-143">Today</span></span>

<span data-ttu-id="c9e31-144">Immettere la parola corrispondente a `today`nella lingua impostata in **Lingua**, questo imposterà la data e sulla data corrente.</span><span class="sxs-lookup"><span data-stu-id="c9e31-144">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="c9e31-145">Anziché immettere la parola intera, è possibile immettere una parte della parola, a partire dall'inizio, ad esempio `t` o `tod`, purché non sia anche l'inizio di un'altra parola.</span><span class="sxs-lookup"><span data-stu-id="c9e31-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="c9e31-146">Periodo</span><span class="sxs-lookup"><span data-stu-id="c9e31-146">Period</span></span>

<span data-ttu-id="c9e31-147">Per filtrare uno specifico periodo contabile, in un campo Data immettere la lettera `p` o la parola `period` seguita da un numero che identifica il periodo contabile, ad esempio `p2` o `period4`.</span><span class="sxs-lookup"><span data-stu-id="c9e31-147">To filter on a specific accounting period, in a date field enter the letter `p`, or the word `period`, followed by a number that identifies the accounting period, like `p2` or `period4`.</span></span> <span data-ttu-id="c9e31-148">Il periodo contabile è relativo all'anno fiscale della data di lavoro corrente impostata nella Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="c9e31-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="c9e31-149">Ad esempio, se la data di lavoro è **03/21/20**, `p1`, oppure soltanto `p`, filtra il primo periodo contabile dell'anno fiscale 2020 (come `01/01/20..01/31/20`).</span><span class="sxs-lookup"><span data-stu-id="c9e31-149">For example, if the work date is **03/21/20**, then `p1`, or just `p`, filters on the first accounting period of the fiscal year 2020 (such as `01/01/20..01/31/20`).</span></span> <span data-ttu-id="c9e31-150">`p15` filtra il quindicesimo periodo contabile dall'inizio dell'anno fiscale 2020 (come `03/01/21..03/31/21`).</span><span class="sxs-lookup"><span data-stu-id="c9e31-150">`p15` filters on the fifteenth accounting period from the start of fiscal year 2020 (such as `03/01/21..03/31/21`).</span></span> 

<span data-ttu-id="c9e31-151">I periodi contabili sono definiti nella pagina **Periodi contabili**.</span><span class="sxs-lookup"><span data-stu-id="c9e31-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="c9e31-152">Per visualizzare o modificare i periodi contabili, aprire la pagina [qui](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="c9e31-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="c9e31-153">Data di lavoro corrente</span><span class="sxs-lookup"><span data-stu-id="c9e31-153">Current work date</span></span>

<span data-ttu-id="c9e31-154">La funzionalità della data di lavoro consente di registrare le transizioni utilizzando una data diversa dalla data corrente.</span><span class="sxs-lookup"><span data-stu-id="c9e31-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="c9e31-155">La parola "workdate", nella lingua impostata in **Lingua** imposterà la data sulla data di lavoro attualmente impostata e specificata nella pagina [**Impostazioni personali**](https://businesscentral.dynamics.com?page=9176 "\"Passare direttamente alla pagina impostazioni utente in Business Central").</span><span class="sxs-lookup"><span data-stu-id="c9e31-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="c9e31-156">Anziché immettere l'intera parola, è possibile immettere una parte della parola, ad esempio "l" o "lavoro".</span><span class="sxs-lookup"><span data-stu-id="c9e31-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="c9e31-157">Se non è stata definita una data di lavoro, per tale valore verrà automaticamente utilizzata la data corrente.</span><span class="sxs-lookup"><span data-stu-id="c9e31-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="c9e31-158">Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.</span><span class="sxs-lookup"><span data-stu-id="c9e31-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="c9e31-159">Vedere anche [Modificare le impostazioni di base, quali l'ora di lavoro](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="c9e31-159">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="c9e31-160">Data chiusura</span><span class="sxs-lookup"><span data-stu-id="c9e31-160">Closing Date</span></span>

<span data-ttu-id="c9e31-161">Per chiudere un anno fiscale, è possibile utilizzare date di chiusura per indicare un movimento di chiusura.</span><span class="sxs-lookup"><span data-stu-id="c9e31-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="c9e31-162">Una data di chiusura è tecnicamente compresa tra due date, ad esempio 31 dicembre e 1 gennaio.</span><span class="sxs-lookup"><span data-stu-id="c9e31-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="c9e31-163">Per specificare che si tratta di una data di chiusura, immettere `C` prima della data, ad esempio `C123101`.</span><span class="sxs-lookup"><span data-stu-id="c9e31-163">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="c9e31-164">Questo metodo può essere utilizzato insieme a tutti i modelli per data.</span><span class="sxs-lookup"><span data-stu-id="c9e31-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="c9e31-165">Esempi</span><span class="sxs-lookup"><span data-stu-id="c9e31-165">Examples</span></span>

<span data-ttu-id="c9e31-166">Nella tabella seguente sono contenuti esempi di date utilizzando tutti i formati.</span><span class="sxs-lookup"><span data-stu-id="c9e31-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="c9e31-167">Presuppone le impostazioni di paese con formato di data **anno.mese.giorno.**, una settimana che inizia il lunedì e la lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="c9e31-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="c9e31-168">**Immissione**</span><span class="sxs-lookup"><span data-stu-id="c9e31-168">**Entry**</span></span>      |<span data-ttu-id="c9e31-169">**Interpretazione**</span><span class="sxs-lookup"><span data-stu-id="c9e31-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="c9e31-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="c9e31-170">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="c9e31-171">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="c9e31-171">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="c9e31-172">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="c9e31-172">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="c9e31-173">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="c9e31-173">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="c9e31-174">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="c9e31-174">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="c9e31-175">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="c9e31-175">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="c9e31-176">anno data di lavoro.mese data di lavoro.11.</span><span class="sxs-lookup"><span data-stu-id="c9e31-176">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="c9e31-177">anno data di lavoro.11.12.</span><span class="sxs-lookup"><span data-stu-id="c9e31-177">work date year.11.12.</span></span>|
|<span data-ttu-id="c9e31-178">`t` o `today`</span><span class="sxs-lookup"><span data-stu-id="c9e31-178">`t` or `today`</span></span>|<span data-ttu-id="c9e31-179">data odierna</span><span class="sxs-lookup"><span data-stu-id="c9e31-179">today's date</span></span>|
|`p4`|<span data-ttu-id="c9e31-180">intervallo di date che include il quarto periodo contabile, ad esempio `04/01/20..04/30/20`</span><span class="sxs-lookup"><span data-stu-id="c9e31-180">date range that includes the fourth accounting period, such as `04/01/20..04/30/20`</span></span>|
|<span data-ttu-id="c9e31-181">`w` o `workdate`</span><span class="sxs-lookup"><span data-stu-id="c9e31-181">`w` or `workdate`</span></span>|<span data-ttu-id="c9e31-182">la data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-182">the working date</span></span>|
|<span data-ttu-id="c9e31-183">`m` o `Monday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-183">`m` or `Monday`</span></span>|<span data-ttu-id="c9e31-184">Lunedì della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-184">Monday of the work date week</span></span>|
|<span data-ttu-id="c9e31-185">`tu` o `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-185">`tu` or `Tuesday`</span></span>|<span data-ttu-id="c9e31-186">Martedì della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-186">Tuesday of the work date week</span></span>|
|<span data-ttu-id="c9e31-187">`sa` o `Saturday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-187">`sa` or `Saturday`</span></span>|<span data-ttu-id="c9e31-188">Sabato della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-188">Saturday of the work date week</span></span>|
|<span data-ttu-id="c9e31-189">`s` o `Sunday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-189">`s` or `Sunday`</span></span>|<span data-ttu-id="c9e31-190">Domenica della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-190">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="c9e31-191">Martedì della settimana 23 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-191">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="c9e31-192">Martedì della settimana 23 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-192">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="c9e31-193">Martedì della settimana 1 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-193">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="c9e31-194">Impostazione di intervalli di date</span><span class="sxs-lookup"><span data-stu-id="c9e31-194">Setting Ranges</span></span>

<span data-ttu-id="c9e31-195">In elenchi, totali e report, è possibile impostare filtri su date, orari e periodi di tempo contenenti un valore iniziale e facoltativamente un valore finale per visualizzare solo i dati contenuti in tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="c9e31-195">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="c9e31-196">All'impostazione di intervalli di date si applicano regole standard.</span><span class="sxs-lookup"><span data-stu-id="c9e31-196">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="c9e31-197">**significato**</span><span class="sxs-lookup"><span data-stu-id="c9e31-197">**Meaning**</span></span>|<span data-ttu-id="c9e31-198">**Espressione di esempio (data)**</span><span class="sxs-lookup"><span data-stu-id="c9e31-198">**Sample expression (Date)**</span></span>|<span data-ttu-id="c9e31-199">**Dati inclusi nel filtro**</span><span class="sxs-lookup"><span data-stu-id="c9e31-199">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="c9e31-200">intervallo</span><span class="sxs-lookup"><span data-stu-id="c9e31-200">Interval</span></span>|`12 15 00..01 15 01`<br /><br />`..12 15 00`<br /><br />`p1..p4`|<span data-ttu-id="c9e31-201">Record la cui data di risposta è compresa tra il 12 15 00 e il 01 15 01 inclusi.</span><span class="sxs-lookup"><span data-stu-id="c9e31-201">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="c9e31-202">Record con data 12 15 00 o precedente.</span><span class="sxs-lookup"><span data-stu-id="c9e31-202">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="c9e31-203">Intervallo di date che include il secondo, il terzo e il quarto periodo contabile, ad esempio `01/01/20..04/30/20`.</span><span class="sxs-lookup"><span data-stu-id="c9e31-203">Date range that includes the second, third, and fourth accounting periods, such as `01/01/20..04/30/20`.</span></span>|
|<span data-ttu-id="c9e31-204">oppure</span><span class="sxs-lookup"><span data-stu-id="c9e31-204">Either/or</span></span>|`12 15 00|12 16 00`|<span data-ttu-id="c9e31-205">Record con data 12 15 00 o 12 16 00.</span><span class="sxs-lookup"><span data-stu-id="c9e31-205">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="c9e31-206">Se ci sono record con date in entrambi i giorni, saranno tutti visualizzati.</span><span class="sxs-lookup"><span data-stu-id="c9e31-206">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="c9e31-207">Combinazione</span><span class="sxs-lookup"><span data-stu-id="c9e31-207">Combination</span></span>|<span data-ttu-id="c9e31-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span><span class="sxs-lookup"><span data-stu-id="c9e31-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span></span>|<span data-ttu-id="c9e31-209">Record con data 12 15 00 o in date tra il 12 01 00 e il 12 10 00 compresi.</span><span class="sxs-lookup"><span data-stu-id="c9e31-209">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="c9e31-210">\nRecord la cui data è il 12 14 00 o una data precedente oppure il 12 30 00 o una data successiva, ossia tutti i record esclusi quelli la cui data di risposta è compresa tra il 12 15 00 e il 12 29 00 inclusi.</span><span class="sxs-lookup"><span data-stu-id="c9e31-210">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="c9e31-211">È possibile utilizzare uno qualsiasi dei formati validi nei filtri dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="c9e31-211">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="c9e31-212">Ad esempio, `mon14 3..t 4p` applicato a un campo data/ora risulta un filtro dalle 3 AM di lunedì nella settimana 14 dell'anno della data di lavoro corrente, incluso, fino alle 4 PM, comprese.</span><span class="sxs-lookup"><span data-stu-id="c9e31-212">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="c9e31-213">Utilizzo di formule per le date</span><span class="sxs-lookup"><span data-stu-id="c9e31-213">Using Date Formulas</span></span>
<span data-ttu-id="c9e31-214">Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date.</span><span class="sxs-lookup"><span data-stu-id="c9e31-214">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="c9e31-215">È possibile immettere formule per le date in diversi campi o filtri per il calcolo della data.</span><span class="sxs-lookup"><span data-stu-id="c9e31-215">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="c9e31-216">In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo.</span><span class="sxs-lookup"><span data-stu-id="c9e31-216">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="c9e31-217">Di conseguenza, se si immette, ad esempio, `1W`, il periodo è effettivamente di otto giorni perché la data odierna è inclusa.</span><span class="sxs-lookup"><span data-stu-id="c9e31-217">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="c9e31-218">Per specificare un periodo di sette giorni \(una settimana\) includendo la data di inizio del periodo, è necessario immettere `6D` o `1W-1D`.</span><span class="sxs-lookup"><span data-stu-id="c9e31-218">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="c9e31-219">Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:</span><span class="sxs-lookup"><span data-stu-id="c9e31-219">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="c9e31-220">La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.</span><span class="sxs-lookup"><span data-stu-id="c9e31-220">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="c9e31-221">La formula nel campo **Periodo di dilazione** per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza \(o dalla data del sollecito precedente\) alla creazione del sollecito.</span><span class="sxs-lookup"><span data-stu-id="c9e31-221">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="c9e31-222">La formula nel campo **Calcolo data di scadenza** determina la modalità di calcolo della data di scadenza nel sollecito.</span><span class="sxs-lookup"><span data-stu-id="c9e31-222">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="c9e31-223">La formula per la data può contenere un massimo di 20 caratteri, sia numeri che lettere.</span><span class="sxs-lookup"><span data-stu-id="c9e31-223">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="c9e31-224">È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di calendario.</span><span class="sxs-lookup"><span data-stu-id="c9e31-224">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="c9e31-225">Lettera</span><span class="sxs-lookup"><span data-stu-id="c9e31-225">Letter</span></span>  |  <span data-ttu-id="c9e31-226">Significato</span><span class="sxs-lookup"><span data-stu-id="c9e31-226">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="c9e31-227">Corrente</span><span class="sxs-lookup"><span data-stu-id="c9e31-227">Current</span></span>|
|`D`|<span data-ttu-id="c9e31-228">Giorno\(i\)</span><span class="sxs-lookup"><span data-stu-id="c9e31-228">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="c9e31-229">Settimana\(e\)</span><span class="sxs-lookup"><span data-stu-id="c9e31-229">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="c9e31-230">Mese\(i\)</span><span class="sxs-lookup"><span data-stu-id="c9e31-230">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="c9e31-231">Trimestre\(i\)</span><span class="sxs-lookup"><span data-stu-id="c9e31-231">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="c9e31-232">Anno\(i\)</span><span class="sxs-lookup"><span data-stu-id="c9e31-232">Year\(s\)</span></span>|

<span data-ttu-id="c9e31-233">È possibile creare una formula per la data in tre modi diversi.</span><span class="sxs-lookup"><span data-stu-id="c9e31-233">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="c9e31-234">L'esempio seguente mostra come usare `C`, vale a dire corrente, e un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="c9e31-234">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="c9e31-235">Espressione</span><span class="sxs-lookup"><span data-stu-id="c9e31-235">Expression</span></span>  |  <span data-ttu-id="c9e31-236">Significato</span><span class="sxs-lookup"><span data-stu-id="c9e31-236">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="c9e31-237">Settimana corrente</span><span class="sxs-lookup"><span data-stu-id="c9e31-237">Current week</span></span>|
|`CM`|<span data-ttu-id="c9e31-238">Mese corrente</span><span class="sxs-lookup"><span data-stu-id="c9e31-238">Current month</span></span>|

<span data-ttu-id="c9e31-239">L'esempio seguente mostra come usare un numero e un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="c9e31-239">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="c9e31-240">Il numero non può essere maggiore di 9999.</span><span class="sxs-lookup"><span data-stu-id="c9e31-240">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="c9e31-241">Espressione</span><span class="sxs-lookup"><span data-stu-id="c9e31-241">Expression</span></span>  |  <span data-ttu-id="c9e31-242">Significato</span><span class="sxs-lookup"><span data-stu-id="c9e31-242">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="c9e31-243">10 giorni a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="c9e31-243">10 days from today</span></span>|
|`2W`|<span data-ttu-id="c9e31-244">2 settimane a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="c9e31-244">2 weeks from today</span></span>|

<span data-ttu-id="c9e31-245">L'esempio seguente mostra come usare un'unità di tempo e un numero.</span><span class="sxs-lookup"><span data-stu-id="c9e31-245">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="c9e31-246">Espressione</span><span class="sxs-lookup"><span data-stu-id="c9e31-246">Expression</span></span>  |  <span data-ttu-id="c9e31-247">Significato</span><span class="sxs-lookup"><span data-stu-id="c9e31-247">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="c9e31-248">Il successivo giorno 10 del mese</span><span class="sxs-lookup"><span data-stu-id="c9e31-248">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="c9e31-249">Il successivo quarto giorno della settimana \(Giovedì\)</span><span class="sxs-lookup"><span data-stu-id="c9e31-249">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="c9e31-250">Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c9e31-250">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="c9e31-251">Espressione</span><span class="sxs-lookup"><span data-stu-id="c9e31-251">Expression</span></span>  |  <span data-ttu-id="c9e31-252">Significato</span><span class="sxs-lookup"><span data-stu-id="c9e31-252">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="c9e31-253">Corrente mese \+ 10 giorni</span><span class="sxs-lookup"><span data-stu-id="c9e31-253">Current month \+ 10 days</span></span>|

<span data-ttu-id="c9e31-254">Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.</span><span class="sxs-lookup"><span data-stu-id="c9e31-254">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="c9e31-255">Espressione</span><span class="sxs-lookup"><span data-stu-id="c9e31-255">Expression</span></span>  |  <span data-ttu-id="c9e31-256">Significato</span><span class="sxs-lookup"><span data-stu-id="c9e31-256">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="c9e31-257">1 anno fa da oggi</span><span class="sxs-lookup"><span data-stu-id="c9e31-257">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="c9e31-258">Se l'ubicazione utilizza un calendario di base, la formula per la data immessa, ad esempio, nel campo **Durata spedizione** verrà interpretata in base ai giorni lavorativi del calendario.</span><span class="sxs-lookup"><span data-stu-id="c9e31-258">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="c9e31-259">Ad esempio la formula `1W` significa sette giorni lavorativi.</span><span class="sxs-lookup"><span data-stu-id="c9e31-259">For example, `1W`  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="c9e31-260">Immissione di ore</span><span class="sxs-lookup"><span data-stu-id="c9e31-260">Entering Times</span></span>
<span data-ttu-id="c9e31-261">Quando si immettono le ore, è possibile inserire qualsiasi separatore non spaziale desiderato tra le unità, ma se si utilizzano cifre doppie per ciascuna unità fino a millisecondi, non è necessario.</span><span class="sxs-lookup"><span data-stu-id="c9e31-261">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="c9e31-262">È necessario immettere solo le unità di grandi dimensioni di richiedere; il resto sarà uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="c9e31-262">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="c9e31-263">È inoltre possibile omettere qualsiasi di contrassegno con l'indicazione AM/PM.</span><span class="sxs-lookup"><span data-stu-id="c9e31-263">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="c9e31-264">Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="c9e31-264">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="c9e31-265">Presuppone le impostazioni del paese che formattano le ore in base a **Ore:Minuti:Secondi.Millisecondi.**</span><span class="sxs-lookup"><span data-stu-id="c9e31-265">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="c9e31-266">e utilizzano gli indicatori AM e PM per "AM" e"PM" rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="c9e31-266">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="c9e31-267">**Immissione**</span><span class="sxs-lookup"><span data-stu-id="c9e31-267">**Entry**</span></span>      |<span data-ttu-id="c9e31-268">**Interpretazione**</span><span class="sxs-lookup"><span data-stu-id="c9e31-268">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="c9e31-269">05:23:17</span><span class="sxs-lookup"><span data-stu-id="c9e31-269">05:23:17</span></span>|
|`5`|<span data-ttu-id="c9e31-270">05.00.00</span><span class="sxs-lookup"><span data-stu-id="c9e31-270">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="c9e31-271">05.00.00</span><span class="sxs-lookup"><span data-stu-id="c9e31-271">05:00:00</span></span>|
|`5P`|<span data-ttu-id="c9e31-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-272">17:00:00</span></span>|
|`12`|<span data-ttu-id="c9e31-273">12:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-273">12:00:00</span></span>|
|`12A`|<span data-ttu-id="c9e31-274">00:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-274">00:00:00</span></span>|
|`12P`|<span data-ttu-id="c9e31-275">12:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-275">12:00:00</span></span>|
|`17`|<span data-ttu-id="c9e31-276">17:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-276">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="c9e31-277">05.30.00</span><span class="sxs-lookup"><span data-stu-id="c9e31-277">05:30:00</span></span>|
|`0530`|<span data-ttu-id="c9e31-278">05.30.00</span><span class="sxs-lookup"><span data-stu-id="c9e31-278">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="c9e31-279">05.30.05</span><span class="sxs-lookup"><span data-stu-id="c9e31-279">05:30:05</span></span>|
|`053005`|<span data-ttu-id="c9e31-280">05.30.05</span><span class="sxs-lookup"><span data-stu-id="c9e31-280">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="c9e31-281">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="c9e31-281">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="c9e31-282">05.30.05,05</span><span class="sxs-lookup"><span data-stu-id="c9e31-282">05:30:05.05</span></span>|

<span data-ttu-id="c9e31-283">È necessario tenere presente che i millisecondi vengono interpretati come notazione decimale.</span><span class="sxs-lookup"><span data-stu-id="c9e31-283">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="c9e31-284">Così, ad esempio `3`, `30` e `300` tutti significano 300 millisecondi, mentre `03` significa `30` e `003` significa 3 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="c9e31-284">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="c9e31-285">Non è possibile utilizzare `24:00` per indicare la mezzanotte, oppure utilizzare qualsiasi valore superiore a 24:00.</span><span class="sxs-lookup"><span data-stu-id="c9e31-285">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="c9e31-286">La parola per "ora" nella lingua usata da [!INCLUDE[d365fin](includes/d365fin_long_md.md)] verrà valutata per l'ora corrente del computer o dispositivo mobile in uso.</span><span class="sxs-lookup"><span data-stu-id="c9e31-286">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="c9e31-287">È possibile immettere qualsiasi parte della parola, a partire dall'inizio, come `t` o `TIM`.</span><span class="sxs-lookup"><span data-stu-id="c9e31-287">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="c9e31-288">Immissione di date e ore combinate</span><span class="sxs-lookup"><span data-stu-id="c9e31-288">Entering combined Dates and Times</span></span>
<span data-ttu-id="c9e31-289">Quando si immettono dati di tipo datetime che corrispondono a una data e un'ora combinate in un campo, è necessario inserire uno spazio tra la data e l'ora.</span><span class="sxs-lookup"><span data-stu-id="c9e31-289">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="c9e31-290">La parte della data può contenere solo spazi nella forma del separatore della data ufficiale delle impostazioni del paese.</span><span class="sxs-lookup"><span data-stu-id="c9e31-290">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="c9e31-291">L'ora può contenere spazi attorno all'indicatore AM / PM.</span><span class="sxs-lookup"><span data-stu-id="c9e31-291">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="c9e31-292">È anche possibile inserire solo una data in un campo datetime, ma non è possibile inserire solo un'ora.</span><span class="sxs-lookup"><span data-stu-id="c9e31-292">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="c9e31-293">La seguente tabella elenca alcuni esempi di combinazioni di data/ora.</span><span class="sxs-lookup"><span data-stu-id="c9e31-293">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="c9e31-294">Le impostazioni del paese negli esempi mostrano le date nel formato giorno\-mese\-anno, utilizzando i designatori AM / PM, la lingua inglese e la domenica come inizio della settimana.</span><span class="sxs-lookup"><span data-stu-id="c9e31-294">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="c9e31-295">**Immissione**</span><span class="sxs-lookup"><span data-stu-id="c9e31-295">**Entry**</span></span>      |<span data-ttu-id="c9e31-296">**Interpretazione**</span><span class="sxs-lookup"><span data-stu-id="c9e31-296">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="c9e31-297">08\-01\-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="c9e31-297">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="c9e31-298">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="c9e31-298">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="c9e31-299">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-299">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="c9e31-300">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-300">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="c9e31-301">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-301">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="c9e31-302">11\-mese data di lavoro\-anno data di lavoro 12:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-302">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="c9e31-303">11\-12\-anno data di lavoro 12:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-303">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="c9e31-304">`t` o `today`</span><span class="sxs-lookup"><span data-stu-id="c9e31-304">`t` or `today`</span></span>|<span data-ttu-id="c9e31-305">Data odierna 00.00.00</span><span class="sxs-lookup"><span data-stu-id="c9e31-305">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="c9e31-306">Data odierna 10.30.00</span><span class="sxs-lookup"><span data-stu-id="c9e31-306">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="c9e31-307">Data odierna 03.03.03</span><span class="sxs-lookup"><span data-stu-id="c9e31-307">today's date 03:03:03</span></span>|
|<span data-ttu-id="c9e31-308">`w` o `workdate`</span><span class="sxs-lookup"><span data-stu-id="c9e31-308">`w` or `workdate`</span></span>|<span data-ttu-id="c9e31-309">Data del lavoro 00.00.00</span><span class="sxs-lookup"><span data-stu-id="c9e31-309">the working date 00:00:00</span></span>|
|<span data-ttu-id="c9e31-310">`m` o `Monday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-310">`m` or `Monday`</span></span>|<span data-ttu-id="c9e31-311">Lunedì della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-311">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="c9e31-312">`tu` o `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-312">`tu` or `Tuesday`</span></span>|<span data-ttu-id="c9e31-313">Martedì della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-313">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="c9e31-314">`sa` o `Saturday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-314">`sa` or `Saturday`</span></span>|<span data-ttu-id="c9e31-315">Sabato della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-315">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="c9e31-316">`s` o `Sunday`</span><span class="sxs-lookup"><span data-stu-id="c9e31-316">`s` or `Sunday`</span></span>|<span data-ttu-id="c9e31-317">Domenica della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-317">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="c9e31-318">Martedì della settimana della data di lavoro 10:30:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-318">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="c9e31-319">Martedì della settimana della data di lavoro 03:03:03</span><span class="sxs-lookup"><span data-stu-id="c9e31-319">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="c9e31-320">Martedì della settimana 23 dell'anno della data di lavoro, ora corrente del giorno</span><span class="sxs-lookup"><span data-stu-id="c9e31-320">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="c9e31-321">Martedì della settimana 23 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-321">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="c9e31-322">Oggi 23:00:00</span><span class="sxs-lookup"><span data-stu-id="c9e31-322">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="c9e31-323">Martedì della settimana 1 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="c9e31-323">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="c9e31-324">Immissione della durata</span><span class="sxs-lookup"><span data-stu-id="c9e31-324">Entering Duration</span></span>
<span data-ttu-id="c9e31-325">Alcuni campi dell'applicazione rappresentano una durata, o una quantità di tempo trascorso, anziché una data o un'ora specifica.</span><span class="sxs-lookup"><span data-stu-id="c9e31-325">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="c9e31-326">È possibile immettere una durata in caratteri numerici seguiti dalla relativa unità di misura.</span><span class="sxs-lookup"><span data-stu-id="c9e31-326">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="c9e31-327">Di seguito vengono forniti alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="c9e31-327">Here are some examples.</span></span>

|<span data-ttu-id="c9e31-328">**Durata**</span><span class="sxs-lookup"><span data-stu-id="c9e31-328">**Duration**</span></span>|<span data-ttu-id="c9e31-329">**Unità di misura**</span><span class="sxs-lookup"><span data-stu-id="c9e31-329">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="c9e31-330">2 ore</span><span class="sxs-lookup"><span data-stu-id="c9e31-330">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="c9e31-331">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="c9e31-331">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="c9e31-332">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="c9e31-332">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="c9e31-333">1 ora 30 minuti</span><span class="sxs-lookup"><span data-stu-id="c9e31-333">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="c9e31-334">2 giorni 6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="c9e31-334">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="c9e31-335">2 giorni 6 ore 30 minuti 56 secondi 600 millisecondi</span><span class="sxs-lookup"><span data-stu-id="c9e31-335">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="c9e31-336">È inoltre possibile immettere un numero che verrà automaticamente convertito in una durata.</span><span class="sxs-lookup"><span data-stu-id="c9e31-336">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="c9e31-337">Il numero immesso viene convertito in base all'unità di misura predefinita specificata nel campo relativo alla durata.</span><span class="sxs-lookup"><span data-stu-id="c9e31-337">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="c9e31-338">Per visualizzare l'unità di misura utilizzata in un campo di durata, immettere un numero e controllare l'unità di misura in cui viene convertito.</span><span class="sxs-lookup"><span data-stu-id="c9e31-338">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="c9e31-339">Ad esempio, il numero `5` viene convertito in 5 h se l'unità di misura è l'ora.</span><span class="sxs-lookup"><span data-stu-id="c9e31-339">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="c9e31-340">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9e31-340">See Also</span></span>
<span data-ttu-id="c9e31-341">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9e31-341">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c9e31-342">Calcolo della data per gli acquisti</span><span class="sxs-lookup"><span data-stu-id="c9e31-342">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="c9e31-343">Immissione di criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="c9e31-343">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
