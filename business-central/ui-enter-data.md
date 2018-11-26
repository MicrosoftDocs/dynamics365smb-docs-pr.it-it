---
title: Come immettere dati nei campi| Microsoft Docs
description: Numerose funzioni generali consentono di immettere dati in modo semplice e veloce. In questo argomento sono descritte tutte le funzioni generali per l'immissione di dati.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5d74aa32c192378c3ffc03e56da2ebb4676f3d87
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---

# <a name="entering-data"></a><span data-ttu-id="f7d56-104">Immissione di dati</span><span class="sxs-lookup"><span data-stu-id="f7d56-104">Entering Data</span></span>
<span data-ttu-id="f7d56-105">Numerose funzioni generali consentono di immettere dati in modo semplice e veloce.</span><span class="sxs-lookup"><span data-stu-id="f7d56-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="f7d56-106">In questo articolo sono descritte tutte le funzioni generali per l'immissione di dati.</span><span class="sxs-lookup"><span data-stu-id="f7d56-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="f7d56-107">Gli esempi in questo articolo utilizzano dati di esempio.</span><span class="sxs-lookup"><span data-stu-id="f7d56-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="f7d56-108">Campi obbligatori</span><span class="sxs-lookup"><span data-stu-id="f7d56-108">Mandatory Fields</span></span>
<span data-ttu-id="f7d56-109">Quando si immettono dati nelle pagine, alcuni campi sono contrassegnati con un asterisco rosso.</span><span class="sxs-lookup"><span data-stu-id="f7d56-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="f7d56-110">L'asterisco rosso significa che il campo deve essere compilato per completare un determinato processo che utilizza il campo, ad esempio registrare una transazione che utilizza il valore nel campo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="f7d56-111">Anche se il campo contiene un asterisco rosso, non è obbligatorio compilarlo prima di continuare con altri campi o chiudere la pagina.</span><span class="sxs-lookup"><span data-stu-id="f7d56-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="f7d56-112">L'asterisco rosso è solo un promemoria che segnala che l'utente sarà bloccato e non potrà completare un determinato processo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="f7d56-113">Trovare dati durante la digitazione</span><span class="sxs-lookup"><span data-stu-id="f7d56-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="f7d56-114">Quando si inizia a digitare dei caratteri in un campo, un elenco a discesa visualizza i valori di campo possibili.</span><span class="sxs-lookup"><span data-stu-id="f7d56-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="f7d56-115">L'elenco cambia se si digitano ulteriori caratteri ed è possibile selezionare il valore corretto quando viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f7d56-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="f7d56-116">In molti campi è disponibile un pulsante Freccia GIÙ che è possibile selezionare.</span><span class="sxs-lookup"><span data-stu-id="f7d56-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="f7d56-117">Facendo clic sulla freccia, è possibile ottenere un elenco di tutti i dati disponibili in un quel campo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="f7d56-118">Il pulsante ha due funzioni, a seconda del tipo di campo:</span><span class="sxs-lookup"><span data-stu-id="f7d56-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="f7d56-119">Lookup - Vengono visualizzate informazioni di un'altra tabella che possono essere immesse nel campo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="f7d56-120">È possibile selezionare soltanto un dato alla volta.</span><span class="sxs-lookup"><span data-stu-id="f7d56-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="f7d56-121">DropDown - Vengono visualizzate le scelte possibili per il campo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="f7d56-122">È possibile selezionare soltanto una delle opzioni.</span><span class="sxs-lookup"><span data-stu-id="f7d56-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards on the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="f7d56-123">Immettere quantità mediante calcolo</span><span class="sxs-lookup"><span data-stu-id="f7d56-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="f7d56-124">Quando si immettono numeri nei campi numerici come il campo **Quantità** in una riga di registrazione magazzino, è possibile immettere la formula invece della quantità della somma.</span><span class="sxs-lookup"><span data-stu-id="f7d56-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="f7d56-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="f7d56-125">Examples</span></span>  

-   <span data-ttu-id="f7d56-126">Se si immette 19+19, il valore del campo viene calcolato in 38.</span><span class="sxs-lookup"><span data-stu-id="f7d56-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="f7d56-127">Se si immette 41-9, il valore del campo viene calcolato in 32.</span><span class="sxs-lookup"><span data-stu-id="f7d56-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="f7d56-128">Se si immette 12\*4, il valore del campo viene calcolato in 48.</span><span class="sxs-lookup"><span data-stu-id="f7d56-128">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="f7d56-129">Se si immette 12/4, il valore del campo viene calcolato in 3.</span><span class="sxs-lookup"><span data-stu-id="f7d56-129">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="f7d56-130">Immettere numeri negativi</span><span class="sxs-lookup"><span data-stu-id="f7d56-130">Entering Negative Numbers</span></span>
<span data-ttu-id="f7d56-131">È possibile immettere numeri negativi in due modi.</span><span class="sxs-lookup"><span data-stu-id="f7d56-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="f7d56-132">Il numero -20,5 può essere immesso come:</span><span class="sxs-lookup"><span data-stu-id="f7d56-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="f7d56-133">-20,5</span><span class="sxs-lookup"><span data-stu-id="f7d56-133">-20.5</span></span>  

    <span data-ttu-id="f7d56-134">oppure</span><span class="sxs-lookup"><span data-stu-id="f7d56-134">or</span></span>
-   <span data-ttu-id="f7d56-135">20,5-</span><span class="sxs-lookup"><span data-stu-id="f7d56-135">20.5-</span></span>  

 <span data-ttu-id="f7d56-136">In entrambi i casi, l'importo verrà registrato come -20,5.</span><span class="sxs-lookup"><span data-stu-id="f7d56-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="f7d56-137">Se l'ultimo carattere dell'espressione è un **+** o un **-**, l'intera espressione verrà registrata con tale segno.</span><span class="sxs-lookup"><span data-stu-id="f7d56-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="f7d56-138">Ad esempio **10-20+** restituirà 10 e non -10.</span><span class="sxs-lookup"><span data-stu-id="f7d56-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="f7d56-139">Immissione di date e ore</span><span class="sxs-lookup"><span data-stu-id="f7d56-139">Entering Dates and Times</span></span>
<span data-ttu-id="f7d56-140">È possibile immettere date e ore in tutti i campi riservati alle date (campi di data).</span><span class="sxs-lookup"><span data-stu-id="f7d56-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="f7d56-141">È possibile immettere date con o senza separatori.</span><span class="sxs-lookup"><span data-stu-id="f7d56-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="f7d56-142">La modalità di immissione di date e ore dipende dalle impostazioni di **Area geografica**.</span><span class="sxs-lookup"><span data-stu-id="f7d56-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="f7d56-143">Per ulteriori informazioni, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f7d56-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="f7d56-144">Immissione di date</span><span class="sxs-lookup"><span data-stu-id="f7d56-144">Entering Dates</span></span>  
 <span data-ttu-id="f7d56-145">In un campo di data è possibile immettere due, quattro, sei o otto cifre:</span><span class="sxs-lookup"><span data-stu-id="f7d56-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="f7d56-146">Se si immettono solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f7d56-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="f7d56-147">Se si immettono quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f7d56-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="f7d56-148">Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1930 e 31/12/2029, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="f7d56-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="f7d56-149">È inoltre possibile immettere una data composta da un giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno. Lu25 o lu25, ad esempio, indica lunedì nella settimana numero 25.</span><span class="sxs-lookup"><span data-stu-id="f7d56-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="f7d56-150">Anziché immettere una data specifica, è possibile immettere uno dei due codici seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7d56-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="f7d56-151">Codice</span><span class="sxs-lookup"><span data-stu-id="f7d56-151">Code</span></span>|<span data-ttu-id="f7d56-152">Risultato</span><span class="sxs-lookup"><span data-stu-id="f7d56-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="f7d56-153">t</span><span class="sxs-lookup"><span data-stu-id="f7d56-153">t</span></span>|<span data-ttu-id="f7d56-154">Si tratta della data odierna (la data di sistema del computer).</span><span class="sxs-lookup"><span data-stu-id="f7d56-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="f7d56-155">w</span><span class="sxs-lookup"><span data-stu-id="f7d56-155">w</span></span>|<span data-ttu-id="f7d56-156">La data di lavoro impostata nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7d56-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="f7d56-157">Per modificare la data di lavoro, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f7d56-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="f7d56-158">Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.</span><span class="sxs-lookup"><span data-stu-id="f7d56-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="f7d56-159">Immissione di ore</span><span class="sxs-lookup"><span data-stu-id="f7d56-159">Entering Times</span></span>  
 <span data-ttu-id="f7d56-160">Quando si immette l'ora, è possibile inserire qualsiasi separatore tra le unità. L'immissione di un separatore è tuttavia facoltativa.</span><span class="sxs-lookup"><span data-stu-id="f7d56-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="f7d56-161">Non è necessario immettere i minuti, i secondi o l'indicazione AM/PM.</span><span class="sxs-lookup"><span data-stu-id="f7d56-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="f7d56-162">Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="f7d56-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="f7d56-163">Movimento</span><span class="sxs-lookup"><span data-stu-id="f7d56-163">Entry</span></span>|<span data-ttu-id="f7d56-164">Interpretazione</span><span class="sxs-lookup"><span data-stu-id="f7d56-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="f7d56-165">5</span><span class="sxs-lookup"><span data-stu-id="f7d56-165">5</span></span>|<span data-ttu-id="f7d56-166">05.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-166">05:00:00</span></span>|  
|<span data-ttu-id="f7d56-167">5:30</span><span class="sxs-lookup"><span data-stu-id="f7d56-167">5:30</span></span>|<span data-ttu-id="f7d56-168">05.30.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-168">05:30:00</span></span>|  
|<span data-ttu-id="f7d56-169">0530</span><span class="sxs-lookup"><span data-stu-id="f7d56-169">0530</span></span>|<span data-ttu-id="f7d56-170">05.30.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-170">05:30:00</span></span>|  
|<span data-ttu-id="f7d56-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="f7d56-171">5:30:5</span></span>|<span data-ttu-id="f7d56-172">05.30.05</span><span class="sxs-lookup"><span data-stu-id="f7d56-172">05:30:05</span></span>|  
|<span data-ttu-id="f7d56-173">053005</span><span class="sxs-lookup"><span data-stu-id="f7d56-173">053005</span></span>|<span data-ttu-id="f7d56-174">05.30.05</span><span class="sxs-lookup"><span data-stu-id="f7d56-174">05:30:05</span></span>|  
|<span data-ttu-id="f7d56-175">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="f7d56-175">5:30:5,50</span></span>|<span data-ttu-id="f7d56-176">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="f7d56-176">05:30:05.5</span></span>|  
|<span data-ttu-id="f7d56-177">053005050</span><span class="sxs-lookup"><span data-stu-id="f7d56-177">053005050</span></span>|<span data-ttu-id="f7d56-178">05.30.05,05</span><span class="sxs-lookup"><span data-stu-id="f7d56-178">05:30:05.05</span></span>|  

 <span data-ttu-id="f7d56-179">Se non si utilizza un separatore, è necessario immettere due cifre per ciascuna unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="f7d56-180">Immissione di date e ore</span><span class="sxs-lookup"><span data-stu-id="f7d56-180">Entering Datetimes</span></span>  
 <span data-ttu-id="f7d56-181">Quando si immettono date e ore, è necessario inserire uno spazio tra la data e l'ora.</span><span class="sxs-lookup"><span data-stu-id="f7d56-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="f7d56-182">Nella tabella seguente sono elencati i vari formati in cui è possibile immettere la data e l'ora e le interpretazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="f7d56-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="f7d56-183">Movimento</span><span class="sxs-lookup"><span data-stu-id="f7d56-183">Entry</span></span>|<span data-ttu-id="f7d56-184">Interpretazione</span><span class="sxs-lookup"><span data-stu-id="f7d56-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="f7d56-185">131202 132455</span><span class="sxs-lookup"><span data-stu-id="f7d56-185">131202 132455</span></span>|<span data-ttu-id="f7d56-186">13/12/02 13.24.55</span><span class="sxs-lookup"><span data-stu-id="f7d56-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="f7d56-187">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="f7d56-187">1-12-02 10</span></span>|<span data-ttu-id="f7d56-188">01/12/02 10.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="f7d56-189">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="f7d56-189">1.12.02 5</span></span>|<span data-ttu-id="f7d56-190">01/12/02 05.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="f7d56-191">1.12.02</span><span class="sxs-lookup"><span data-stu-id="f7d56-191">1.12.02</span></span>|<span data-ttu-id="f7d56-192">01/12/02 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-193">11 12</span><span class="sxs-lookup"><span data-stu-id="f7d56-193">11 12</span></span>|<span data-ttu-id="f7d56-194">11-mese corrente-anno corrente 12.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="f7d56-195">1112 12</span><span class="sxs-lookup"><span data-stu-id="f7d56-195">1112 12</span></span>|<span data-ttu-id="f7d56-196">11-12-anno corrente 12.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="f7d56-197">t o today</span><span class="sxs-lookup"><span data-stu-id="f7d56-197">t or today</span></span>|<span data-ttu-id="f7d56-198">Data odierna 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-199">t time</span><span class="sxs-lookup"><span data-stu-id="f7d56-199">t time</span></span>|<span data-ttu-id="f7d56-200">Ora corrente in data odierna</span><span class="sxs-lookup"><span data-stu-id="f7d56-200">today's date actual time</span></span>|  
|<span data-ttu-id="f7d56-201">t 10:30</span><span class="sxs-lookup"><span data-stu-id="f7d56-201">t 10:30</span></span>|<span data-ttu-id="f7d56-202">Data odierna 10.30.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="f7d56-203">t 3:3:3</span><span class="sxs-lookup"><span data-stu-id="f7d56-203">t 3:3:3</span></span>|<span data-ttu-id="f7d56-204">Data odierna 03.03.03</span><span class="sxs-lookup"><span data-stu-id="f7d56-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="f7d56-205">w o workdate</span><span class="sxs-lookup"><span data-stu-id="f7d56-205">w or workdate</span></span>|<span data-ttu-id="f7d56-206">Data del lavoro 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-207">lu o lunedì</span><span class="sxs-lookup"><span data-stu-id="f7d56-207">m or Monday</span></span>|<span data-ttu-id="f7d56-208">Lunedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-209">ma o martedì</span><span class="sxs-lookup"><span data-stu-id="f7d56-209">tu or Tuesday</span></span>|<span data-ttu-id="f7d56-210">Martedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-211">me o mercoledì</span><span class="sxs-lookup"><span data-stu-id="f7d56-211">we or Wednesday</span></span>|<span data-ttu-id="f7d56-212">Mercoledì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-213">gi o giovedì</span><span class="sxs-lookup"><span data-stu-id="f7d56-213">th or Thursday</span></span>|<span data-ttu-id="f7d56-214">Giovedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-215">ve o venerdì</span><span class="sxs-lookup"><span data-stu-id="f7d56-215">f or Friday</span></span>|<span data-ttu-id="f7d56-216">Venerdì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-217">sa o sabato</span><span class="sxs-lookup"><span data-stu-id="f7d56-217">s or Saturday</span></span>|<span data-ttu-id="f7d56-218">Sabato della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-219">do o domenica</span><span class="sxs-lookup"><span data-stu-id="f7d56-219">su or Sunday</span></span>|<span data-ttu-id="f7d56-220">Domenica della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="f7d56-221">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="f7d56-221">tu 10:30</span></span>|<span data-ttu-id="f7d56-222">Martedì della settimana corrente 10.30.00</span><span class="sxs-lookup"><span data-stu-id="f7d56-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="f7d56-223">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="f7d56-223">tu 3:3:3</span></span>|<span data-ttu-id="f7d56-224">Martedì della settimana corrente 03.03.03</span><span class="sxs-lookup"><span data-stu-id="f7d56-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="f7d56-225">Immissione della durata</span><span class="sxs-lookup"><span data-stu-id="f7d56-225">Entering Duration</span></span>  
 <span data-ttu-id="f7d56-226">È possibile immettere una durata in caratteri numerici seguiti dalla relativa unità di misura.</span><span class="sxs-lookup"><span data-stu-id="f7d56-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="f7d56-227">Di seguito vengono forniti alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="f7d56-227">Here are some examples.</span></span>  

|<span data-ttu-id="f7d56-228">Durata</span><span class="sxs-lookup"><span data-stu-id="f7d56-228">Duration</span></span>|<span data-ttu-id="f7d56-229">Unità di misura\*\*</span><span class="sxs-lookup"><span data-stu-id="f7d56-229">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="f7d56-230">2h</span><span class="sxs-lookup"><span data-stu-id="f7d56-230">2h</span></span>|<span data-ttu-id="f7d56-231">2 ore</span><span class="sxs-lookup"><span data-stu-id="f7d56-231">2 hrs</span></span>|  
|<span data-ttu-id="f7d56-232">6h 30 m</span><span class="sxs-lookup"><span data-stu-id="f7d56-232">6h 30 m</span></span>|<span data-ttu-id="f7d56-233">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="f7d56-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="f7d56-234">6.5h</span><span class="sxs-lookup"><span data-stu-id="f7d56-234">6.5h</span></span>|<span data-ttu-id="f7d56-235">6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="f7d56-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="f7d56-236">90m</span><span class="sxs-lookup"><span data-stu-id="f7d56-236">90m</span></span>|<span data-ttu-id="f7d56-237">1 ora 30 minuti</span><span class="sxs-lookup"><span data-stu-id="f7d56-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="f7d56-238">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="f7d56-238">2d 6h 30m</span></span>|<span data-ttu-id="f7d56-239">2 giorni 6 ore 30 minuti</span><span class="sxs-lookup"><span data-stu-id="f7d56-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="f7d56-240">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="f7d56-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="f7d56-241">2 giorni 6 ore 30 minuti 56 secondi 600 millisecondi</span><span class="sxs-lookup"><span data-stu-id="f7d56-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="f7d56-242">È inoltre possibile immettere un numero in modo che venga automaticamente convertito in una durata.</span><span class="sxs-lookup"><span data-stu-id="f7d56-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="f7d56-243">Il numero immesso viene convertito in base all'unità di misura predefinita specificata nel campo relativo alla durata.</span><span class="sxs-lookup"><span data-stu-id="f7d56-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="f7d56-244">Per visualizzare l'unità di misura utilizzata in un campo di durata, immettere un numero e controllare l'unità di misura in cui viene convertito.</span><span class="sxs-lookup"><span data-stu-id="f7d56-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="f7d56-245">Il numero 5 viene convertito in 5 h se l'unità di misura è l'ora.</span><span class="sxs-lookup"><span data-stu-id="f7d56-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a><span data-ttu-id="f7d56-246">Utilizzo di formule per le date</span><span class="sxs-lookup"><span data-stu-id="f7d56-246">Using Date Formulas</span></span>  
 <span data-ttu-id="f7d56-247">Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date.</span><span class="sxs-lookup"><span data-stu-id="f7d56-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="f7d56-248">È possibile immettere formule per le date in diversi campi di calcolo e in campi relativi alla frequenza della ricorrenza in registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="f7d56-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f7d56-249">In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="f7d56-250">Di conseguenza, se si immette, ad esempio, 1W, il periodo è effettivamente di otto giorni perché la data odierna è inclusa.</span><span class="sxs-lookup"><span data-stu-id="f7d56-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="f7d56-251">Per specificare un periodo di sette giorni (una settimana) includendo la data di inizio del periodo, è necessario immettere 6D o 1W-1D.</span><span class="sxs-lookup"><span data-stu-id="f7d56-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="f7d56-252">Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:</span><span class="sxs-lookup"><span data-stu-id="f7d56-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="f7d56-253">La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.</span><span class="sxs-lookup"><span data-stu-id="f7d56-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="f7d56-254">La formula nel campo Periodo di dilazione per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza (o dalla data del sollecito precedente) alla creazione del sollecito.</span><span class="sxs-lookup"><span data-stu-id="f7d56-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="f7d56-255">La formula nel campo Calcolo data di scadenza determina la modalità di calcolo della data di scadenza nel sollecito.</span><span class="sxs-lookup"><span data-stu-id="f7d56-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="f7d56-256">La formula per il calcolo della data può contenere un massimo di 20 caratteri, sia numeri che lettere.</span><span class="sxs-lookup"><span data-stu-id="f7d56-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="f7d56-257">È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di tempo diverse.</span><span class="sxs-lookup"><span data-stu-id="f7d56-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f7d56-258">C</span><span class="sxs-lookup"><span data-stu-id="f7d56-258">C</span></span>|<span data-ttu-id="f7d56-259">Corrente</span><span class="sxs-lookup"><span data-stu-id="f7d56-259">Current</span></span>|  
|<span data-ttu-id="f7d56-260">D</span><span class="sxs-lookup"><span data-stu-id="f7d56-260">D</span></span>|<span data-ttu-id="f7d56-261">Giorno/i</span><span class="sxs-lookup"><span data-stu-id="f7d56-261">Day(s)</span></span>|  
|<span data-ttu-id="f7d56-262">W</span><span class="sxs-lookup"><span data-stu-id="f7d56-262">W</span></span>|<span data-ttu-id="f7d56-263">Settimana/e</span><span class="sxs-lookup"><span data-stu-id="f7d56-263">Week(s)</span></span>|  
|<span data-ttu-id="f7d56-264">M</span><span class="sxs-lookup"><span data-stu-id="f7d56-264">M</span></span>|<span data-ttu-id="f7d56-265">Mese/i</span><span class="sxs-lookup"><span data-stu-id="f7d56-265">Month(s)</span></span>|  
|<span data-ttu-id="f7d56-266">Q</span><span class="sxs-lookup"><span data-stu-id="f7d56-266">Q</span></span>|<span data-ttu-id="f7d56-267">Trimestre/i</span><span class="sxs-lookup"><span data-stu-id="f7d56-267">Quarter(s)</span></span>|  
|<span data-ttu-id="f7d56-268">Y</span><span class="sxs-lookup"><span data-stu-id="f7d56-268">Y</span></span>|<span data-ttu-id="f7d56-269">Anno/i</span><span class="sxs-lookup"><span data-stu-id="f7d56-269">Year(s)</span></span>|  

 <span data-ttu-id="f7d56-270">È possibile creare una formula per la data in tre modi diversi.</span><span class="sxs-lookup"><span data-stu-id="f7d56-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="f7d56-271">Nell'esempio seguente viene illustrato come corrente più un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f7d56-272">CW</span><span class="sxs-lookup"><span data-stu-id="f7d56-272">CW</span></span>|<span data-ttu-id="f7d56-273">Settimana corrente</span><span class="sxs-lookup"><span data-stu-id="f7d56-273">Current week</span></span>|  
|<span data-ttu-id="f7d56-274">CM</span><span class="sxs-lookup"><span data-stu-id="f7d56-274">CM</span></span>|<span data-ttu-id="f7d56-275">Mese corrente</span><span class="sxs-lookup"><span data-stu-id="f7d56-275">Current month</span></span>|  

 <span data-ttu-id="f7d56-276">Nell'esempio seguente viene illustrato come un numero e un'unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="f7d56-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="f7d56-277">Il numero non può essere maggiore di 9999.</span><span class="sxs-lookup"><span data-stu-id="f7d56-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f7d56-278">10D</span><span class="sxs-lookup"><span data-stu-id="f7d56-278">10D</span></span>|<span data-ttu-id="f7d56-279">10 giorni a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="f7d56-279">10 days from today</span></span>|  
|<span data-ttu-id="f7d56-280">2W</span><span class="sxs-lookup"><span data-stu-id="f7d56-280">2W</span></span>|<span data-ttu-id="f7d56-281">2 settimane a partire da oggi</span><span class="sxs-lookup"><span data-stu-id="f7d56-281">2 weeks from today</span></span>|  

 <span data-ttu-id="f7d56-282">Nell'esempio seguente viene illustrato come un'unità di tempo e un numero.</span><span class="sxs-lookup"><span data-stu-id="f7d56-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f7d56-283">D10</span><span class="sxs-lookup"><span data-stu-id="f7d56-283">D10</span></span>|<span data-ttu-id="f7d56-284">Il successivo giorno 10 del mese</span><span class="sxs-lookup"><span data-stu-id="f7d56-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="f7d56-285">WD4</span><span class="sxs-lookup"><span data-stu-id="f7d56-285">WD4</span></span>|<span data-ttu-id="f7d56-286">Il successivo quarto giorno della settimana (giovedì)</span><span class="sxs-lookup"><span data-stu-id="f7d56-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="f7d56-287">Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f7d56-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f7d56-288">CM+10D</span><span class="sxs-lookup"><span data-stu-id="f7d56-288">CM+10D</span></span>|<span data-ttu-id="f7d56-289">Mese corrente + 10 giorni</span><span class="sxs-lookup"><span data-stu-id="f7d56-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="f7d56-290">Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.</span><span class="sxs-lookup"><span data-stu-id="f7d56-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="f7d56-291">-1A</span><span class="sxs-lookup"><span data-stu-id="f7d56-291">-1Y</span></span>|<span data-ttu-id="f7d56-292">1 anno fa da oggi</span><span class="sxs-lookup"><span data-stu-id="f7d56-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="f7d56-293">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7d56-293">See Also</span></span>  
 [<span data-ttu-id="f7d56-294">Ricerca, filtro e ordinamento di dati</span><span class="sxs-lookup"><span data-stu-id="f7d56-294">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="f7d56-295">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7d56-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

