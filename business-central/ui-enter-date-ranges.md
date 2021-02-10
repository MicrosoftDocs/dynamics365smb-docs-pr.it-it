---
title: Immissione di date e ore in Business Central | Documenti Microsoft
description: Ottenere informazioni su come immettere le date e le ore inclusi suggerimenti relativi alla produttività quali abbreviazioni, espressioni e intervalli. Filtrare elenchi o report per una data o periodo specifici.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 853a45dc32907c2d9b69f7b2e592dc164c20a094
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757369"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="45928-104">Utilizzo di date e orari del calendario</span><span class="sxs-lookup"><span data-stu-id="45928-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="45928-105">offre diversi modi per immettere date e orari, incluse potenti funzionalità per accelerare l'immissione dei dati o scrivere espressioni di calendario complesse.</span><span class="sxs-lookup"><span data-stu-id="45928-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="45928-106">È possibile immettere date e orari nei campi in diversi punti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="45928-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="45928-107">Ad esempio, in un ordine di vendita, è possibile impostare la data di spedizione.</span><span class="sxs-lookup"><span data-stu-id="45928-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="45928-108">Quando si filtrano gli elenchi o i dati dei report, è possibile immettere date e orari per contrassegnare solo i dati a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="45928-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="45928-109">Verificare le impostazioni di lingua e paese</span><span class="sxs-lookup"><span data-stu-id="45928-109">Check your region and language settings</span></span>
<span data-ttu-id="45928-110">La pagina **Impostazioni personali** specifica la **Regione** e il **Linguaggio** che si sta utilizzando nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="45928-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="45928-111">Queste impostazioni influenzano le modalità di immissione delle date e ore.</span><span class="sxs-lookup"><span data-stu-id="45928-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="45928-112">L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati.</span><span class="sxs-lookup"><span data-stu-id="45928-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="45928-113">Per gli schemi di date che coinvolgono le parole, la lingua delle parole utilizzate deve corrispondere all'impostazione della **Lingua**.</span><span class="sxs-lookup"><span data-stu-id="45928-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="45928-114">utilizza il sistema di calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="45928-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="45928-115">Immissione di date</span><span class="sxs-lookup"><span data-stu-id="45928-115">Entering Dates</span></span>

<span data-ttu-id="45928-116">In un campo Data, è possibile immettere una data utilizzando il formato standard per le impostazioni di un paese.</span><span class="sxs-lookup"><span data-stu-id="45928-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="45928-117">Diverse regioni possono utilizzare separatori diversi tra i giorni, i mesi e gli anni.</span><span class="sxs-lookup"><span data-stu-id="45928-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="45928-118">Ad esempio, alcune regioni utilizzano i trattini (gg-mm-aaaa) e altri usano le barre (gg/mm/aaaa).</span><span class="sxs-lookup"><span data-stu-id="45928-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="45928-119">Tuttavia, è possibile utilizzare qualsiasi separatore, anche uno spazio, e la data verrà automaticamente modificata per utilizzare separatori che corrispondono alla regione.</span><span class="sxs-lookup"><span data-stu-id="45928-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="45928-120">Si noti che il formato in cui le date vengono visualizzate sui report stampati o sui documenti inviati via e-mail non è influenzato dalla scelta personale di impostazione della regione.</span><span class="sxs-lookup"><span data-stu-id="45928-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="45928-121">Per lavorare in modo più produttivo con date e orari, è possibile utilizzare uno dei metodi o formati descritti nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="45928-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="45928-122">Selezionare le date dal calendario</span><span class="sxs-lookup"><span data-stu-id="45928-122">Picking dates from the calendar</span></span>

<span data-ttu-id="45928-123">Qualsiasi campo che visualizza un'icona di calendario può essere impostato utilizzando il selettore di date del calendario.</span><span class="sxs-lookup"><span data-stu-id="45928-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="45928-124">Per visualizzare il selettore di date del calendario, attivare l'icona del calendario o premere CTRL+tasto HOME nel campo.</span><span class="sxs-lookup"><span data-stu-id="45928-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="45928-125">![Campi data](media/ui-date-field.png "Esempio di un campo data")</span><span class="sxs-lookup"><span data-stu-id="45928-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="45928-126">Vedere anche [Tasti di scelta rapida nel calendario (selezione data)](keyboard-shortcuts.md#calendarshortcuts).</span><span class="sxs-lookup"><span data-stu-id="45928-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="45928-127">Schema giorno\-settimana\-anno</span><span class="sxs-lookup"><span data-stu-id="45928-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="45928-128">È possibile immettere una data come giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno.</span><span class="sxs-lookup"><span data-stu-id="45928-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="45928-129">Ad esempio, Lun25 o lun25 indica il lunedì della settimana 25.</span><span class="sxs-lookup"><span data-stu-id="45928-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="45928-130">Se non si immette un anno, viene utilizzato l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="45928-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="45928-131">Anziché immettere l'intera parola per il giorno della settimana, è possibile immettere una parte della parola, a partire dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="45928-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="45928-132">Nel caso dei conflitti (come in italiano m che potrebbe essere Martedì o Mercoledì), i giorni vengono valutati in base all'impostazione dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="45928-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="45928-133">L'input viene prima valutato rispetto alla data di lavoro e alla data odierna, quindi è necessario ricordare questa informazione quando si utilizzano abbreviazioni.</span><span class="sxs-lookup"><span data-stu-id="45928-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="45928-134">Ad esempio, in italiano, s indica settimana pertanto non può significare Sabato.</span><span class="sxs-lookup"><span data-stu-id="45928-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="45928-135">Lo schema del numero della settimana è sempre ISO 8601, dove la settimana 1 è la settimana che include il 4 gennaio o la settimana con il primo giovedì dell'anno.</span><span class="sxs-lookup"><span data-stu-id="45928-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="45928-136">Schemi con cifre</span><span class="sxs-lookup"><span data-stu-id="45928-136">Digit patterns</span></span>

<span data-ttu-id="45928-137">In un campo di data è possibile immettere due, quattro, sei o otto cifre:</span><span class="sxs-lookup"><span data-stu-id="45928-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="45928-138">Se si immettono solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="45928-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="45928-139">Se si immettono quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="45928-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="45928-140">L'ordine giorno e il mese è determinato dalle impostazioni di un paese.</span><span class="sxs-lookup"><span data-stu-id="45928-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="45928-141">Anche se le impostazioni del paese hanno l'anno prima del giorno e del mese, le quattro cifre vengono interpretate come giorno e mese.</span><span class="sxs-lookup"><span data-stu-id="45928-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="45928-142">Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1930 e 31/12/2029, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="45928-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="45928-143">Oggi</span><span class="sxs-lookup"><span data-stu-id="45928-143">Today</span></span>

<span data-ttu-id="45928-144">Immettere la parola corrispondente a oggi nella lingua impostata in **Lingua**. La data verrà impostata così sulla data corrente.</span><span class="sxs-lookup"><span data-stu-id="45928-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="45928-145">Invece di immettere la parola intera, è possibile immettere una parte della parola, a partire dall'inizio, ad esempio o oppure og, purché non sia anche l'inizio di un'altra parola.</span><span class="sxs-lookup"><span data-stu-id="45928-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="45928-146">Periodo</span><span class="sxs-lookup"><span data-stu-id="45928-146">Period</span></span>

<span data-ttu-id="45928-147">Per filtrare uno specifico periodo contabile, in un campo Data immettere la lettera p o la parola periodo, seguita da un numero che identifica il periodo contabile, ad esempio p2 o periodo4.</span><span class="sxs-lookup"><span data-stu-id="45928-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="45928-148">Il periodo contabile è relativo all'anno fiscale della data di lavoro corrente impostata nella Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="45928-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="45928-149">Ad esempio, se la data di lavoro è **21/03/20**, p1 oppure soltanto p filtra il primo periodo contabile dell'anno fiscale 2020 (come 01/01/20..31/01/20).</span><span class="sxs-lookup"><span data-stu-id="45928-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="45928-150">p15 filtra il quindicesimo periodo contabile dall'inizio dell'anno fiscale 2020 (come 01/03/21..31/03/21).</span><span class="sxs-lookup"><span data-stu-id="45928-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="45928-151">I periodi contabili sono definiti nella pagina **Periodi contabili**.</span><span class="sxs-lookup"><span data-stu-id="45928-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="45928-152">Per visualizzare o modificare i periodi contabili, aprire la pagina [qui](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="45928-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="45928-153">Data di lavoro corrente</span><span class="sxs-lookup"><span data-stu-id="45928-153">Current work date</span></span>

<span data-ttu-id="45928-154">La funzionalità della data di lavoro consente di registrare le transizioni utilizzando una data diversa dalla data corrente.</span><span class="sxs-lookup"><span data-stu-id="45928-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="45928-155">La parola "data di lavoro", nella lingua impostata in **Lingua** imposterà la data sulla data di lavoro attualmente impostata e specificata nella pagina **Impostazioni personali**.</span><span class="sxs-lookup"><span data-stu-id="45928-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="45928-156">Anziché immettere l'intera parola, è possibile immettere una parte della parola, ad esempio "l" o "lavoro".</span><span class="sxs-lookup"><span data-stu-id="45928-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="45928-157">Se non è stata definita una data di lavoro, per tale valore verrà automaticamente utilizzata la data corrente.</span><span class="sxs-lookup"><span data-stu-id="45928-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="45928-158">Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.</span><span class="sxs-lookup"><span data-stu-id="45928-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="45928-159">Vedere anche [Modificare le impostazioni di base, quali l'ora di lavoro](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="45928-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="45928-160">Data chiusura</span><span class="sxs-lookup"><span data-stu-id="45928-160">Closing Date</span></span>

<span data-ttu-id="45928-161">Per chiudere un anno fiscale, è possibile utilizzare date di chiusura per indicare un movimento di chiusura.</span><span class="sxs-lookup"><span data-stu-id="45928-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="45928-162">Una data di chiusura è tecnicamente compresa tra due date, ad esempio 31 dicembre e 1 gennaio.</span><span class="sxs-lookup"><span data-stu-id="45928-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="45928-163">Per specificare che si tratta di una data di chiusura, immettere C prima della data, ad esempio C123101.</span><span class="sxs-lookup"><span data-stu-id="45928-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="45928-164">Questo metodo può essere utilizzato insieme a tutti i modelli per data.</span><span class="sxs-lookup"><span data-stu-id="45928-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="45928-165">Esempi</span><span class="sxs-lookup"><span data-stu-id="45928-165">Examples</span></span>

<span data-ttu-id="45928-166">Nella tabella seguente sono contenuti esempi di date utilizzando tutti i formati.</span><span class="sxs-lookup"><span data-stu-id="45928-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="45928-167">Presuppone le impostazioni di paese con formato di data **anno.mese.giorno.**, una settimana che inizia il lunedì e la lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="45928-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="45928-168">**Immissione**</span><span class="sxs-lookup"><span data-stu-id="45928-168">**Entry**</span></span>      |<span data-ttu-id="45928-169">**Interpretazione**</span><span class="sxs-lookup"><span data-stu-id="45928-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="45928-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="45928-170">2018.12.31.</span></span>|<span data-ttu-id="45928-171">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="45928-171">2018.12.31.</span></span>|
|<span data-ttu-id="45928-172">181231</span><span class="sxs-lookup"><span data-stu-id="45928-172">181231</span></span>|<span data-ttu-id="45928-173">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="45928-173">2018.12.31.</span></span>|
|<span data-ttu-id="45928-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="45928-174">18.12.31.</span></span>|<span data-ttu-id="45928-175">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="45928-175">2018.12.31.</span></span>|
|<span data-ttu-id="45928-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="45928-176">18.12.31.</span></span>|<span data-ttu-id="45928-177">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="45928-177">2018.12.31.</span></span>|
|<span data-ttu-id="45928-178">20181231</span><span class="sxs-lookup"><span data-stu-id="45928-178">20181231</span></span>|<span data-ttu-id="45928-179">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="45928-179">2018.12.31.</span></span>|
|<span data-ttu-id="45928-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="45928-180">18/12,31</span></span>|<span data-ttu-id="45928-181">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="45928-181">2018.12.31.</span></span>|
|<span data-ttu-id="45928-182">11</span><span class="sxs-lookup"><span data-stu-id="45928-182">11</span></span>|<span data-ttu-id="45928-183">anno data di lavoro.mese data di lavoro.11.</span><span class="sxs-lookup"><span data-stu-id="45928-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="45928-184">1112</span><span class="sxs-lookup"><span data-stu-id="45928-184">1112</span></span>|<span data-ttu-id="45928-185">anno data di lavoro.11.12.</span><span class="sxs-lookup"><span data-stu-id="45928-185">work date year.11.12.</span></span>|
|<span data-ttu-id="45928-186">o oppure oggi</span><span class="sxs-lookup"><span data-stu-id="45928-186">t or today</span></span>|<span data-ttu-id="45928-187">data odierna</span><span class="sxs-lookup"><span data-stu-id="45928-187">today's date</span></span>|
|<span data-ttu-id="45928-188">p4</span><span class="sxs-lookup"><span data-stu-id="45928-188">p4</span></span>|<span data-ttu-id="45928-189">intervallo di date che include il quarto periodo contabile, ad esempio 01/04/20..30/04/20</span><span class="sxs-lookup"><span data-stu-id="45928-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="45928-190">l o data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-190">w or workdate</span></span>|<span data-ttu-id="45928-191">la data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-191">the working date</span></span>|
|<span data-ttu-id="45928-192">lu o lunedì</span><span class="sxs-lookup"><span data-stu-id="45928-192">m or Monday</span></span>|<span data-ttu-id="45928-193">Lunedì della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-193">Monday of the work date week</span></span>|
|<span data-ttu-id="45928-194">ma o martedì</span><span class="sxs-lookup"><span data-stu-id="45928-194">tu or Tuesday</span></span>|<span data-ttu-id="45928-195">Martedì della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="45928-196">sa o Sabato</span><span class="sxs-lookup"><span data-stu-id="45928-196">sa or Saturday</span></span>|<span data-ttu-id="45928-197">Sabato della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="45928-198">d o Domenica</span><span class="sxs-lookup"><span data-stu-id="45928-198">s or Sunday</span></span>|<span data-ttu-id="45928-199">Domenica della settimana della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="45928-200">m23</span><span class="sxs-lookup"><span data-stu-id="45928-200">t23</span></span>|<span data-ttu-id="45928-201">Martedì della settimana 23 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="45928-202">m 23</span><span class="sxs-lookup"><span data-stu-id="45928-202">t 23</span></span>|<span data-ttu-id="45928-203">Martedì della settimana 23 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="45928-204">m-1</span><span class="sxs-lookup"><span data-stu-id="45928-204">t-1</span></span>|<span data-ttu-id="45928-205">Martedì della settimana 1 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="45928-206">Impostazione di intervalli di date</span><span class="sxs-lookup"><span data-stu-id="45928-206">Setting Ranges</span></span>

<span data-ttu-id="45928-207">In elenchi, totali e report, è possibile impostare filtri su date, orari e periodi di tempo contenenti un valore iniziale e facoltativamente un valore finale per visualizzare solo i dati contenuti in tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="45928-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="45928-208">All'impostazione di intervalli di date si applicano regole standard.</span><span class="sxs-lookup"><span data-stu-id="45928-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="45928-209">**significato**</span><span class="sxs-lookup"><span data-stu-id="45928-209">**Meaning**</span></span>|<span data-ttu-id="45928-210">**Espressione di esempio (data)**</span><span class="sxs-lookup"><span data-stu-id="45928-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="45928-211">**Dati inclusi nel filtro**</span><span class="sxs-lookup"><span data-stu-id="45928-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="45928-212">intervallo</span><span class="sxs-lookup"><span data-stu-id="45928-212">Interval</span></span>|<span data-ttu-id="45928-213">15 12 00..01 15 01</span><span class="sxs-lookup"><span data-stu-id="45928-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="45928-214">..15 12 00</span><span class="sxs-lookup"><span data-stu-id="45928-214">..12 15 00</span></span><br /><br /><span data-ttu-id="45928-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="45928-215">p1..p4</span></span>|<span data-ttu-id="45928-216">Record la cui data di risposta è compresa tra il 15 12 00 e il 15 01 01 inclusi.</span><span class="sxs-lookup"><span data-stu-id="45928-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="45928-217">Record con data 15 12 00 o precedente.</span><span class="sxs-lookup"><span data-stu-id="45928-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="45928-218">Intervallo di date che include il secondo, il terzo e il quarto periodo contabile, ad esempio 01/01/20..30/04/20..</span><span class="sxs-lookup"><span data-stu-id="45928-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="45928-219">oppure</span><span class="sxs-lookup"><span data-stu-id="45928-219">Either/or</span></span>|<span data-ttu-id="45928-220">15 12 00\|16 12 00</span><span class="sxs-lookup"><span data-stu-id="45928-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="45928-221">Record con data 15 12 00 o 16 12 00.</span><span class="sxs-lookup"><span data-stu-id="45928-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="45928-222">Se ci sono record con date in entrambi i giorni, saranno tutti visualizzati.</span><span class="sxs-lookup"><span data-stu-id="45928-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="45928-223">Combinazione</span><span class="sxs-lookup"><span data-stu-id="45928-223">Combination</span></span>|<span data-ttu-id="45928-224">15 12 00\|01 12 00..10 12 00</span><span class="sxs-lookup"><span data-stu-id="45928-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="45928-225">..14 12 00\|30 12 00..</span><span class="sxs-lookup"><span data-stu-id="45928-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="45928-226">Record con data 15 12 00 o in date tra l'01 12 00 e il 10 12 00 compresi.</span><span class="sxs-lookup"><span data-stu-id="45928-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="45928-227">Record la cui data è il 12 14 00 o una data precedente oppure il 12 30 00 o una data successiva, ossia tutti i record esclusi quelli la cui data di risposta è compresa tra il 12 15 00 e il 12 29 00 inclusi.</span><span class="sxs-lookup"><span data-stu-id="45928-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="45928-228">È possibile utilizzare uno qualsiasi dei formati validi nei filtri dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="45928-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="45928-229">Ad esempio, lun14 3..o 4p applicato a un campo data/ora risulta un filtro dalle 3 AM di lunedì nella settimana 14 dell'anno della data di lavoro corrente, incluso, fino alle 4 PM, comprese.</span><span class="sxs-lookup"><span data-stu-id="45928-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="45928-230">Utilizzo di formule per le date</span><span class="sxs-lookup"><span data-stu-id="45928-230">Using Date Formulas</span></span>
<span data-ttu-id="45928-231">Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date.</span><span class="sxs-lookup"><span data-stu-id="45928-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="45928-232">È possibile immettere formule per le date in diversi campi o filtri per il calcolo della data.</span><span class="sxs-lookup"><span data-stu-id="45928-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="45928-233">In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo.</span><span class="sxs-lookup"><span data-stu-id="45928-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="45928-234">Di conseguenza, se si immette, ad esempio, 1S, il periodo è effettivamente di otto giorni perché la data odierna è inclusa.</span><span class="sxs-lookup"><span data-stu-id="45928-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="45928-235">Per specificare un periodo di sette giorni \(una settimana\) includendo la data di inizio del periodo, è necessario immettere 6G o 1S-1G.</span><span class="sxs-lookup"><span data-stu-id="45928-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="45928-236">Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:</span><span class="sxs-lookup"><span data-stu-id="45928-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="45928-237">La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.</span><span class="sxs-lookup"><span data-stu-id="45928-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="45928-238">La formula nel campo **Periodo di dilazione** per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza \(o dalla data del sollecito precedente\) alla creazione del sollecito.</span><span class="sxs-lookup"><span data-stu-id="45928-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="45928-239">La formula nel campo **Calcolo data di scadenza** determina la modalità di calcolo della data di scadenza nel sollecito.</span><span class="sxs-lookup"><span data-stu-id="45928-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="45928-240">La formula per la data può contenere un massimo di 20 caratteri, sia numeri che lettere.</span><span class="sxs-lookup"><span data-stu-id="45928-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="45928-241">È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di calendario.</span><span class="sxs-lookup"><span data-stu-id="45928-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="45928-242">Lettera</span><span class="sxs-lookup"><span data-stu-id="45928-242">Letter</span></span>  |  <span data-ttu-id="45928-243">Significato</span><span class="sxs-lookup"><span data-stu-id="45928-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="45928-244">C</span><span class="sxs-lookup"><span data-stu-id="45928-244">C</span></span>|<span data-ttu-id="45928-245">Corrente</span><span class="sxs-lookup"><span data-stu-id="45928-245">Current</span></span>|
|<span data-ttu-id="45928-246">G</span><span class="sxs-lookup"><span data-stu-id="45928-246">D</span></span>|<span data-ttu-id="45928-247">Giorno\(i\)</span><span class="sxs-lookup"><span data-stu-id="45928-247">Day\(s\)</span></span>|
|<span data-ttu-id="45928-248">S</span><span class="sxs-lookup"><span data-stu-id="45928-248">W</span></span>|<span data-ttu-id="45928-249">Settimana\(e\)</span><span class="sxs-lookup"><span data-stu-id="45928-249">Week\(s\)</span></span>|
|<span data-ttu-id="45928-250">M</span><span class="sxs-lookup"><span data-stu-id="45928-250">M</span></span>|<span data-ttu-id="45928-251">Mese\(i\)</span><span class="sxs-lookup"><span data-stu-id="45928-251">Month\(s\)</span></span>|
|<span data-ttu-id="45928-252">T</span><span class="sxs-lookup"><span data-stu-id="45928-252">Q</span></span>|<span data-ttu-id="45928-253">Trimestre\(i\)</span><span class="sxs-lookup"><span data-stu-id="45928-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="45928-254">A</span><span class="sxs-lookup"><span data-stu-id="45928-254">Y</span></span>|<span data-ttu-id="45928-255">Anno\(i\)</span><span class="sxs-lookup"><span data-stu-id="45928-255">Year\(s\)</span></span>|

<span data-ttu-id="45928-256">È possibile creare una formula per la data in tre modi diversi.</span><span class="sxs-lookup"><span data-stu-id="45928-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="45928-257">L'esempio seguente mostra come usare C, vale a dire corrente, e un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="45928-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="45928-258">Espressione</span><span class="sxs-lookup"><span data-stu-id="45928-258">Expression</span></span>  |  <span data-ttu-id="45928-259">Significato</span><span class="sxs-lookup"><span data-stu-id="45928-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="45928-260">SC</span><span class="sxs-lookup"><span data-stu-id="45928-260">CW</span></span>|<span data-ttu-id="45928-261">Settimana corrente</span><span class="sxs-lookup"><span data-stu-id="45928-261">Current week</span></span>|
|<span data-ttu-id="45928-262">MC</span><span class="sxs-lookup"><span data-stu-id="45928-262">CM</span></span>|<span data-ttu-id="45928-263">Mese corrente</span><span class="sxs-lookup"><span data-stu-id="45928-263">Current month</span></span>|

<span data-ttu-id="45928-264">L'esempio seguente mostra come usare un numero e un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="45928-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="45928-265">Il numero non può essere maggiore di 9999.</span><span class="sxs-lookup"><span data-stu-id="45928-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="45928-266">Espressione</span><span class="sxs-lookup"><span data-stu-id="45928-266">Expression</span></span>  |  <span data-ttu-id="45928-267">Significato</span><span class="sxs-lookup"><span data-stu-id="45928-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="45928-268">10G</span><span class="sxs-lookup"><span data-stu-id="45928-268">10D</span></span>|<span data-ttu-id="45928-269">10 giorni a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="45928-269">10 days from today</span></span>|
|<span data-ttu-id="45928-270">2S</span><span class="sxs-lookup"><span data-stu-id="45928-270">2W</span></span>|<span data-ttu-id="45928-271">2 settimane a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="45928-271">2 weeks from today</span></span>|

<span data-ttu-id="45928-272">L'esempio seguente mostra come usare un'unità di tempo e un numero.</span><span class="sxs-lookup"><span data-stu-id="45928-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="45928-273">Espressione</span><span class="sxs-lookup"><span data-stu-id="45928-273">Expression</span></span>  |  <span data-ttu-id="45928-274">Significato</span><span class="sxs-lookup"><span data-stu-id="45928-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="45928-275">G10</span><span class="sxs-lookup"><span data-stu-id="45928-275">D10</span></span>|<span data-ttu-id="45928-276">Il successivo giorno 10 del mese</span><span class="sxs-lookup"><span data-stu-id="45928-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="45928-277">GS4</span><span class="sxs-lookup"><span data-stu-id="45928-277">WD4</span></span>|<span data-ttu-id="45928-278">Il successivo quarto giorno della settimana \(Giovedì\)</span><span class="sxs-lookup"><span data-stu-id="45928-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="45928-279">Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="45928-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="45928-280">Espressione</span><span class="sxs-lookup"><span data-stu-id="45928-280">Expression</span></span>  |  <span data-ttu-id="45928-281">Significato</span><span class="sxs-lookup"><span data-stu-id="45928-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="45928-282">MC+10G</span><span class="sxs-lookup"><span data-stu-id="45928-282">CM+10D</span></span>|<span data-ttu-id="45928-283">Mese corrente \+ 10 giorni</span><span class="sxs-lookup"><span data-stu-id="45928-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="45928-284">Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.</span><span class="sxs-lookup"><span data-stu-id="45928-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="45928-285">Espressione</span><span class="sxs-lookup"><span data-stu-id="45928-285">Expression</span></span>  |  <span data-ttu-id="45928-286">Significato</span><span class="sxs-lookup"><span data-stu-id="45928-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="45928-287">-1A</span><span class="sxs-lookup"><span data-stu-id="45928-287">-1Y</span></span>|<span data-ttu-id="45928-288">1 anno fa da oggi</span><span class="sxs-lookup"><span data-stu-id="45928-288">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="45928-289">Se l'ubicazione utilizza un calendario di base, la formula per la data immessa, ad esempio, nel campo **Durata spedizione** verrà interpretata in base ai giorni lavorativi del calendario.</span><span class="sxs-lookup"><span data-stu-id="45928-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="45928-290">Ad esempio la formula 1S significa sette giorni lavorativi.</span><span class="sxs-lookup"><span data-stu-id="45928-290">For example, 1W  means seven working days.</span></span>
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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

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

## <a name="entering-times"></a><span data-ttu-id="45928-291">Immissione di ore</span><span class="sxs-lookup"><span data-stu-id="45928-291">Entering Times</span></span>
<span data-ttu-id="45928-292">Quando si immettono le ore, è possibile inserire qualsiasi separatore non spaziale desiderato tra le unità, ma se si utilizzano cifre doppie per ciascuna unità fino a millisecondi, non è necessario.</span><span class="sxs-lookup"><span data-stu-id="45928-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="45928-293">È necessario immettere solo le unità di grandi dimensioni di richiedere; il resto sarà uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="45928-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="45928-294">È inoltre possibile omettere qualsiasi di contrassegno con l'indicazione AM/PM.</span><span class="sxs-lookup"><span data-stu-id="45928-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="45928-295">Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="45928-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="45928-296">Presuppone le impostazioni del paese che formattano le ore in base a **Ore:Minuti:Secondi.Millisecondi.**</span><span class="sxs-lookup"><span data-stu-id="45928-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="45928-297">e utilizzano gli indicatori AM e PM per "AM" e"PM" rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="45928-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="45928-298">**Immissione**</span><span class="sxs-lookup"><span data-stu-id="45928-298">**Entry**</span></span>      |<span data-ttu-id="45928-299">**Interpretazione**</span><span class="sxs-lookup"><span data-stu-id="45928-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="45928-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="45928-300">05:23:17</span></span>|<span data-ttu-id="45928-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="45928-301">05:23:17</span></span>|
|<span data-ttu-id="45928-302">5</span><span class="sxs-lookup"><span data-stu-id="45928-302">5</span></span>|<span data-ttu-id="45928-303">05.00.00</span><span class="sxs-lookup"><span data-stu-id="45928-303">05:00:00</span></span>|
|<span data-ttu-id="45928-304">5AM</span><span class="sxs-lookup"><span data-stu-id="45928-304">5AM</span></span>|<span data-ttu-id="45928-305">05.00.00</span><span class="sxs-lookup"><span data-stu-id="45928-305">05:00:00</span></span>|
|<span data-ttu-id="45928-306">5P</span><span class="sxs-lookup"><span data-stu-id="45928-306">5P</span></span>|<span data-ttu-id="45928-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-307">17:00:00</span></span>|
|<span data-ttu-id="45928-308">12</span><span class="sxs-lookup"><span data-stu-id="45928-308">12</span></span>|<span data-ttu-id="45928-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-309">12:00:00</span></span>|
|<span data-ttu-id="45928-310">12A</span><span class="sxs-lookup"><span data-stu-id="45928-310">12A</span></span>|<span data-ttu-id="45928-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-311">00:00:00</span></span>|
|<span data-ttu-id="45928-312">12P</span><span class="sxs-lookup"><span data-stu-id="45928-312">12P</span></span>|<span data-ttu-id="45928-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-313">12:00:00</span></span>|
|<span data-ttu-id="45928-314">17</span><span class="sxs-lookup"><span data-stu-id="45928-314">17</span></span>|<span data-ttu-id="45928-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-315">17:00:00</span></span>|
|<span data-ttu-id="45928-316">5:30</span><span class="sxs-lookup"><span data-stu-id="45928-316">5:30</span></span>|<span data-ttu-id="45928-317">05.30.00</span><span class="sxs-lookup"><span data-stu-id="45928-317">05:30:00</span></span>|
|<span data-ttu-id="45928-318">0530</span><span class="sxs-lookup"><span data-stu-id="45928-318">0530</span></span>|<span data-ttu-id="45928-319">05.30.00</span><span class="sxs-lookup"><span data-stu-id="45928-319">05:30:00</span></span>|
|<span data-ttu-id="45928-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="45928-320">5:30:5</span></span>|<span data-ttu-id="45928-321">05.30.05</span><span class="sxs-lookup"><span data-stu-id="45928-321">05:30:05</span></span>|
|<span data-ttu-id="45928-322">053005</span><span class="sxs-lookup"><span data-stu-id="45928-322">053005</span></span>|<span data-ttu-id="45928-323">05.30.05</span><span class="sxs-lookup"><span data-stu-id="45928-323">05:30:05</span></span>|
|<span data-ttu-id="45928-324">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="45928-324">5:30:5,50</span></span>|<span data-ttu-id="45928-325">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="45928-325">05:30:05.5</span></span>|
|<span data-ttu-id="45928-326">053005050</span><span class="sxs-lookup"><span data-stu-id="45928-326">053005050</span></span>|<span data-ttu-id="45928-327">05.30.05,05</span><span class="sxs-lookup"><span data-stu-id="45928-327">05:30:05.05</span></span>|

<span data-ttu-id="45928-328">È necessario tenere presente che i millisecondi vengono interpretati come notazione decimale.</span><span class="sxs-lookup"><span data-stu-id="45928-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="45928-329">Così, ad esempio, 3, 30 e 300 significano tutti 300 millisecondi, mentre 03 significa 30 e 003 significa 3 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="45928-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="45928-330">Non è possibile utilizzare 24:00 per indicare la mezzanotte oppure utilizzare qualsiasi valore superiore a 24:00.</span><span class="sxs-lookup"><span data-stu-id="45928-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="45928-331">La parola per "ora" nella lingua usata da [!INCLUDE[prod_short](includes/prod_long.md)] verrà valutata per l'ora corrente del computer o dispositivo mobile in uso.</span><span class="sxs-lookup"><span data-stu-id="45928-331">The word for 'time' in the language used by [!INCLUDE[prod_short](includes/prod_long.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="45928-332">È possibile immettere qualsiasi parte della parola, a partire dall'inizio, come o oppure ORA.</span><span class="sxs-lookup"><span data-stu-id="45928-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="45928-333">Immissione di date e ore combinate</span><span class="sxs-lookup"><span data-stu-id="45928-333">Entering combined Dates and Times</span></span>
<span data-ttu-id="45928-334">Quando si immettono dati di tipo datetime che corrispondono a una data e un'ora combinate in un campo, è necessario inserire uno spazio tra la data e l'ora.</span><span class="sxs-lookup"><span data-stu-id="45928-334">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="45928-335">La parte della data può contenere solo spazi nella forma del separatore della data ufficiale delle impostazioni del paese.</span><span class="sxs-lookup"><span data-stu-id="45928-335">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="45928-336">L'ora può contenere spazi attorno all'indicatore AM / PM.</span><span class="sxs-lookup"><span data-stu-id="45928-336">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="45928-337">È anche possibile inserire solo una data in un campo datetime, ma non è possibile inserire solo un'ora.</span><span class="sxs-lookup"><span data-stu-id="45928-337">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="45928-338">La seguente tabella elenca alcuni esempi di combinazioni di data/ora.</span><span class="sxs-lookup"><span data-stu-id="45928-338">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="45928-339">Le impostazioni del paese negli esempi mostrano le date nel formato giorno\-mese\-anno, utilizzando i designatori AM / PM, la lingua inglese e la domenica come inizio della settimana.</span><span class="sxs-lookup"><span data-stu-id="45928-339">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="45928-340">**Immissione**</span><span class="sxs-lookup"><span data-stu-id="45928-340">**Entry**</span></span>      |<span data-ttu-id="45928-341">**Interpretazione**</span><span class="sxs-lookup"><span data-stu-id="45928-341">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="45928-342">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="45928-342">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="45928-343">08/01/2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="45928-343">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="45928-344">131202 132455</span><span class="sxs-lookup"><span data-stu-id="45928-344">131202 132455</span></span>|<span data-ttu-id="45928-345">13/12/2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="45928-345">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="45928-346">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="45928-346">1-12-02 10</span></span>|<span data-ttu-id="45928-347">01/12/2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-347">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="45928-348">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="45928-348">1.12.02 5</span></span>|<span data-ttu-id="45928-349">01/12/2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-349">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="45928-350">1.12.02</span><span class="sxs-lookup"><span data-stu-id="45928-350">1.12.02</span></span>|<span data-ttu-id="45928-351">01/12/2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-351">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="45928-352">11 12</span><span class="sxs-lookup"><span data-stu-id="45928-352">11 12</span></span>|<span data-ttu-id="45928-353">11/mese data di lavoro/anno data di lavoro 12:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-353">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="45928-354">1112 12</span><span class="sxs-lookup"><span data-stu-id="45928-354">1112 12</span></span>|<span data-ttu-id="45928-355">11/12/anno data di lavoro 12:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-355">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="45928-356">o oppure oggi</span><span class="sxs-lookup"><span data-stu-id="45928-356">t or today</span></span>|<span data-ttu-id="45928-357">Data odierna 00.00.00</span><span class="sxs-lookup"><span data-stu-id="45928-357">today's date 00:00:00</span></span>|
|<span data-ttu-id="45928-358">o 10:30</span><span class="sxs-lookup"><span data-stu-id="45928-358">t 10:30</span></span>|<span data-ttu-id="45928-359">Data odierna 10.30.00</span><span class="sxs-lookup"><span data-stu-id="45928-359">today's date 10:30:00</span></span>|
|<span data-ttu-id="45928-360">o 3:3:3</span><span class="sxs-lookup"><span data-stu-id="45928-360">t 3:3:3</span></span>|<span data-ttu-id="45928-361">Data odierna 03.03.03</span><span class="sxs-lookup"><span data-stu-id="45928-361">today's date 03:03:03</span></span>|
|<span data-ttu-id="45928-362">l o data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-362">w or workdate</span></span>|<span data-ttu-id="45928-363">Data del lavoro 00.00.00</span><span class="sxs-lookup"><span data-stu-id="45928-363">the working date 00:00:00</span></span>|
|<span data-ttu-id="45928-364">lu o lunedì</span><span class="sxs-lookup"><span data-stu-id="45928-364">m or Monday</span></span>|<span data-ttu-id="45928-365">Lunedì della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-365">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="45928-366">ma o martedì</span><span class="sxs-lookup"><span data-stu-id="45928-366">tu or Tuesday</span></span>|<span data-ttu-id="45928-367">Martedì della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-367">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="45928-368">sa o Sabato</span><span class="sxs-lookup"><span data-stu-id="45928-368">sa or Saturday</span></span>|<span data-ttu-id="45928-369">Sabato della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-369">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="45928-370">d o Domenica</span><span class="sxs-lookup"><span data-stu-id="45928-370">s or Sunday</span></span>|<span data-ttu-id="45928-371">Domenica della settimana della data di lavoro 00:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-371">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="45928-372">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="45928-372">tu 10:30</span></span>|<span data-ttu-id="45928-373">Martedì della settimana della data di lavoro 10:30:00</span><span class="sxs-lookup"><span data-stu-id="45928-373">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="45928-374">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="45928-374">tu 3:3:3</span></span>|<span data-ttu-id="45928-375">Martedì della settimana della data di lavoro 03:03:03</span><span class="sxs-lookup"><span data-stu-id="45928-375">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="45928-376">m23 o</span><span class="sxs-lookup"><span data-stu-id="45928-376">t23 t</span></span>|<span data-ttu-id="45928-377">Martedì della settimana 23 dell'anno della data di lavoro, ora corrente del giorno</span><span class="sxs-lookup"><span data-stu-id="45928-377">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="45928-378">m23</span><span class="sxs-lookup"><span data-stu-id="45928-378">t23</span></span>|<span data-ttu-id="45928-379">Martedì della settimana 23 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-379">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="45928-380">m 23</span><span class="sxs-lookup"><span data-stu-id="45928-380">t 23</span></span>|<span data-ttu-id="45928-381">Oggi 23:00:00</span><span class="sxs-lookup"><span data-stu-id="45928-381">Today 23:00:00</span></span>|
|<span data-ttu-id="45928-382">m-1</span><span class="sxs-lookup"><span data-stu-id="45928-382">t-1</span></span>|<span data-ttu-id="45928-383">Martedì della settimana 1 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="45928-383">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="45928-384">Immissione della durata</span><span class="sxs-lookup"><span data-stu-id="45928-384">Entering Duration</span></span>
<span data-ttu-id="45928-385">Alcuni campi dell'applicazione rappresentano una durata, o una quantità di tempo trascorso, anziché una data o un'ora specifica.</span><span class="sxs-lookup"><span data-stu-id="45928-385">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="45928-386">È possibile immettere una durata in caratteri numerici seguiti dalla relativa unità di misura.</span><span class="sxs-lookup"><span data-stu-id="45928-386">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="45928-387">Di seguito vengono forniti alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="45928-387">Here are some examples.</span></span>

|<span data-ttu-id="45928-388">**Durata**</span><span class="sxs-lookup"><span data-stu-id="45928-388">**Duration**</span></span>|<span data-ttu-id="45928-389">**Unità di misura**</span><span class="sxs-lookup"><span data-stu-id="45928-389">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="45928-390">2h</span><span class="sxs-lookup"><span data-stu-id="45928-390">2h</span></span>|<span data-ttu-id="45928-391">2 ore</span><span class="sxs-lookup"><span data-stu-id="45928-391">2 hrs</span></span>|
|<span data-ttu-id="45928-392">6h 30 m</span><span class="sxs-lookup"><span data-stu-id="45928-392">6h 30 m</span></span>|<span data-ttu-id="45928-393">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="45928-393">6 hrs 30 mins</span></span>|
|<span data-ttu-id="45928-394">6.5h</span><span class="sxs-lookup"><span data-stu-id="45928-394">6.5h</span></span>|<span data-ttu-id="45928-395">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="45928-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="45928-396">90m</span><span class="sxs-lookup"><span data-stu-id="45928-396">90m</span></span>|<span data-ttu-id="45928-397">1 ora 30 minuti</span><span class="sxs-lookup"><span data-stu-id="45928-397">1 hr 30 mins</span></span>|
|<span data-ttu-id="45928-398">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="45928-398">2d 6h 30m</span></span>|<span data-ttu-id="45928-399">2 giorni 6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="45928-399">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="45928-400">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="45928-400">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="45928-401">2 giorni 6 ore 30 minuti 56 secondi 600 millisecondi</span><span class="sxs-lookup"><span data-stu-id="45928-401">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="45928-402">È inoltre possibile immettere un numero che verrà automaticamente convertito in una durata.</span><span class="sxs-lookup"><span data-stu-id="45928-402">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="45928-403">Il numero immesso viene convertito in base all'unità di misura predefinita specificata nel campo relativo alla durata.</span><span class="sxs-lookup"><span data-stu-id="45928-403">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="45928-404">Per visualizzare l'unità di misura utilizzata in un campo di durata, immettere un numero e controllare l'unità di misura in cui viene convertito.</span><span class="sxs-lookup"><span data-stu-id="45928-404">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="45928-405">Ad esempio, il numero 5 viene convertito in 5 h se l'unità di misura è l'ora.</span><span class="sxs-lookup"><span data-stu-id="45928-405">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="45928-406">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="45928-406">See Also</span></span>
<span data-ttu-id="45928-407">[Utilizzo di [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="45928-407">[Working with [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="45928-408">Calcolo della data per gli acquisti</span><span class="sxs-lookup"><span data-stu-id="45928-408">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="45928-409">Immissione di criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="45928-409">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
