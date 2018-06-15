---
title: Generare report finanziari con le situazioni contabili
description: Descrive come utilizzare le situazioni contabili per creare le visualizzazioni e i report per analizzare i dati finanziari.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: it-it
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="0820f-103">Utilizzare le situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="0820f-103">Work with Account Schedules</span></span>
<span data-ttu-id="0820f-104">Utilizzare le situazioni contabili per ottenere informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="0820f-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="0820f-105">Le situazioni contabili analizzano le cifre nei conti di contabilità generale e confrontano i movimenti di contabilità generale con i movimenti budget di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="0820f-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="0820f-106">I risultati vengono visualizzati in grafici nella Gestione ruolo utente, ad esempio il grafico Flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="0820f-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0820f-107"> fornisce alcune situazioni contabili di esempio che è possibile utilizzare immediatamente oppure è possibile impostare le proprie righe e colonne per specificare le cifre da confrontare.</span><span class="sxs-lookup"><span data-stu-id="0820f-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="0820f-108">È ad esempio possibile creare piani dei conti per calcolare i margini di profitto in dimensioni quali reparti o gruppi di clienti.</span><span class="sxs-lookup"><span data-stu-id="0820f-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="0820f-109">È possibile creare quanti rendiconti finanziari personalizzati si desidera.</span><span class="sxs-lookup"><span data-stu-id="0820f-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="0820f-110">L'impostazione delle situazioni contabili richiede una comprensione dei dati finanziari nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="0820f-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="0820f-111">Per esempio, è possibile visualizzare i movimenti C/G come percentuali di movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="0820f-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="0820f-112">Tale operazione richiede che i budget siano creati.</span><span class="sxs-lookup"><span data-stu-id="0820f-112">This requires that budgets are created.</span></span> <span data-ttu-id="0820f-113">Per ulteriori informazioni, vedere [Creare budget C/G](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="0820f-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="0820f-114">Categorie di conti e situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="0820f-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="0820f-115">Le categorie di conto consentono di modificare il layout dei rendiconti finanziari.</span><span class="sxs-lookup"><span data-stu-id="0820f-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="0820f-116">Dopo aver impostato le categorie di conto nella finestra **Categorie conto C/G** scegliere l'azione **Genera situazioni contabili**, le situazioni contabili sottostanti i report finanziari principali verranno aggiornate.</span><span class="sxs-lookup"><span data-stu-id="0820f-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="0820f-117">Alla successiva esecuzione di uno dei report, ad esempio l'estratto conto, nuovi totali e voci secondarie vengono aggiunte, in base alle modifiche.</span><span class="sxs-lookup"><span data-stu-id="0820f-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="0820f-118">Per ulteriori informazioni, vedere [Contabilità generale e piano dei conti](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="0820f-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="0820f-119">Per creare nuove situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="0820f-119">To create new account schedules</span></span>  
 <span data-ttu-id="0820f-120">Utilizzare situazioni contabili per analizzare le cifre nei conti di contabilità generale o confrontare i movimenti di contabilità generale con i movimenti budget di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="0820f-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="0820f-121">Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="0820f-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="0820f-122">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0820f-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0820f-123">Nella finestra **Descr. situazioni contabili** scegliere l'azione **Nuovo** per creare una nuova descrizione situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="0820f-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="0820f-124">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="0820f-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="0820f-125">Scegliere l'azione **Modifica situazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="0820f-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="0820f-126">Compilare i campi necessari nella finestra **Situazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="0820f-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="0820f-127">Dopo aver creato una nuova situazione contabile e averne impostato le righe, è necessario impostare le colonne.</span><span class="sxs-lookup"><span data-stu-id="0820f-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="0820f-128">Le colonne possono essere impostate manualmente oppure assegnando un layout di colonne di default alla situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="0820f-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="0820f-129">Scegliere l'azione **Modifica setup layout colonna**.</span><span class="sxs-lookup"><span data-stu-id="0820f-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="0820f-130">Compilare i campi necessari nella finestra **Layout colonna**.</span><span class="sxs-lookup"><span data-stu-id="0820f-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0820f-131">Se non è stato assegnato un default layout colonna alla situazione contabile, è necessario impostare le colonne manualmente.</span><span class="sxs-lookup"><span data-stu-id="0820f-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="0820f-132">Per creare una colonna per il calcolo delle percentuali</span><span class="sxs-lookup"><span data-stu-id="0820f-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="0820f-133">A volte, potrebbe essere necessario includere in una situazione contabile una colonna per il calcolo delle percentuali di un totale.</span><span class="sxs-lookup"><span data-stu-id="0820f-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="0820f-134">Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, è possibile inserire una colonna per indicare la percentuale delle vendite totale rappresentata da ogni riga.</span><span class="sxs-lookup"><span data-stu-id="0820f-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="0820f-135">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0820f-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="0820f-136">Nella finestra **Descr. situazioni contabili** selezionare una situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="0820f-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="0820f-137">Selezionare l'azione **Modifica situazione contabile** per impostare una riga della situazione contabile per calcolare il totale su cui saranno basate le percentuali.</span><span class="sxs-lookup"><span data-stu-id="0820f-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="0820f-138">Inserire una riga immediatamente sopra la prima riga per la quale si desidera visualizzare una percentuale.</span><span class="sxs-lookup"><span data-stu-id="0820f-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="0820f-139">Compilare i campi della riga nel modo seguente: Nel campo **Tipo totale** immettere **Imposta base per percentuale**.</span><span class="sxs-lookup"><span data-stu-id="0820f-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="0820f-140">Nel campo **Totale** immettere una formula del totale su cui sarà basata la percentuale.</span><span class="sxs-lookup"><span data-stu-id="0820f-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="0820f-141">Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.</span><span class="sxs-lookup"><span data-stu-id="0820f-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="0820f-142">Scegliere l'azione **Modifica setup layout colonna** per impostare una colonna.</span><span class="sxs-lookup"><span data-stu-id="0820f-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="0820f-143">Compilare i campi della riga nel modo seguente: nel campo **Tipo colonna** selezionare **Formula**.</span><span class="sxs-lookup"><span data-stu-id="0820f-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="0820f-144">Nel campo **Formula** immettere una formula per l'importo per il quale si desidera calcolare la percentuale, seguita dalla percentuale (%).</span><span class="sxs-lookup"><span data-stu-id="0820f-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="0820f-145">Ad esempio, se il numero di colonna N contiene il saldo periodo, immettere **N%**.</span><span class="sxs-lookup"><span data-stu-id="0820f-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="0820f-146">Ripetere i passaggi da 4 a 7 per ogni gruppo di righe che di desidera suddividere per percentuale.</span><span class="sxs-lookup"><span data-stu-id="0820f-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="0820f-147">Per impostare situazioni contabili con sintesi</span><span class="sxs-lookup"><span data-stu-id="0820f-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="0820f-148">È possibile utilizzare una situazione contabile per creare un rendiconto in cui vengono confrontate le cifre C/G con le cifre del budget C/G.</span><span class="sxs-lookup"><span data-stu-id="0820f-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="0820f-149">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0820f-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="0820f-150">Nella finestra **Descr. situazioni contabili** selezionare una situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="0820f-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="0820f-151">Scegliere l'azione **Modifica situazione contabile**</span><span class="sxs-lookup"><span data-stu-id="0820f-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="0820f-152">Nella finestra **Situazione contabile** selezionare il nome della situazione contabile di default nel campo **Nome**.</span><span class="sxs-lookup"><span data-stu-id="0820f-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="0820f-153">Scegliere l'azione **Inserisci conti**.</span><span class="sxs-lookup"><span data-stu-id="0820f-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="0820f-154">Selezionare i conti che si intendono includere nella dichiarazione e selezionare il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="0820f-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="0820f-155">I conti sono stati inseriti nella situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="0820f-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="0820f-156">È inoltre possibile modificare il layout colonna.</span><span class="sxs-lookup"><span data-stu-id="0820f-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="0820f-157">Scegliere l'azione **Sintesi**.</span><span class="sxs-lookup"><span data-stu-id="0820f-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="0820f-158">Fare clic sulla Scheda dettaglio **Filtri dimensione** e impostare il filtro budget con il nome di filtro desiderato.</span><span class="sxs-lookup"><span data-stu-id="0820f-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="0820f-159">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="0820f-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="0820f-160">Ora è possibile copiare e incollare la dichiarazione di budget in un foglio elettronico.</span><span class="sxs-lookup"><span data-stu-id="0820f-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="0820f-161">Confronto dei periodi contabili con le formule periodo</span><span class="sxs-lookup"><span data-stu-id="0820f-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="0820f-162">La situazione contabile consente di confrontare i risultati di diversi periodi contabili, ad esempio mese corrente rispetto allo stesso mese dell'anno precedente.</span><span class="sxs-lookup"><span data-stu-id="0820f-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="0820f-163">Per fare ciò, aggiungere una colonna con il campo **Formula confronto periodo** quindi impostare tale campo su una formula periodo.</span><span class="sxs-lookup"><span data-stu-id="0820f-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="0820f-164">Un periodo contabile non deve corrispondere esattamente al calendario, ma ogni anno fiscale deve avere lo stesso numero di periodi contabili, che possono tuttavia avere una durata distinta.</span><span class="sxs-lookup"><span data-stu-id="0820f-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0820f-165"> usa la formula periodo per calcolare l'importo dal periodo di confronto in relazione al periodo rappresentato dal filtro data nella richiesta del report.</span><span class="sxs-lookup"><span data-stu-id="0820f-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="0820f-166">Il periodo di confronto si basa sul periodo indicato dalla data di inizio del filtro data.</span><span class="sxs-lookup"><span data-stu-id="0820f-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="0820f-167">Le abbreviazioni per l'indicazione dei periodi sono:</span><span class="sxs-lookup"><span data-stu-id="0820f-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0820f-168">Abbreviazione</span><span class="sxs-lookup"><span data-stu-id="0820f-168">Abbreviation</span></span></th>
<th><span data-ttu-id="0820f-169">Description</span><span class="sxs-lookup"><span data-stu-id="0820f-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0820f-170">P</span><span class="sxs-lookup"><span data-stu-id="0820f-170">P</span></span></p></td>
<td><p><span data-ttu-id="0820f-171">Periodo</span><span class="sxs-lookup"><span data-stu-id="0820f-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0820f-172">UP</span><span class="sxs-lookup"><span data-stu-id="0820f-172">LP</span></span></p></td>
<td><p><span data-ttu-id="0820f-173">Ultimo periodo di un trimestre, semestre o anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="0820f-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0820f-174">CP</span><span class="sxs-lookup"><span data-stu-id="0820f-174">CP</span></span></p></td>
<td><p><span data-ttu-id="0820f-175">Periodo corrente di un trimestre, semestre o anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="0820f-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0820f-176">AF</span><span class="sxs-lookup"><span data-stu-id="0820f-176">FY</span></span></p></td>
<td><p><span data-ttu-id="0820f-177">Anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="0820f-177">Fiscal year.</span></span> <span data-ttu-id="0820f-178">Ad esempio, AF[1..3] indica il primo trimestre dall'anno fiscale corrente</span><span class="sxs-lookup"><span data-stu-id="0820f-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0820f-179">Esempi di formule</span><span class="sxs-lookup"><span data-stu-id="0820f-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0820f-180">Formula</span><span class="sxs-lookup"><span data-stu-id="0820f-180">Formula</span></span></th>
<th><span data-ttu-id="0820f-181">Description</span><span class="sxs-lookup"><span data-stu-id="0820f-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0820f-182">&lt;Vuoto&gt;</span><span class="sxs-lookup"><span data-stu-id="0820f-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="0820f-183">Periodo corrente</span><span class="sxs-lookup"><span data-stu-id="0820f-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0820f-184">-1P</span><span class="sxs-lookup"><span data-stu-id="0820f-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="0820f-185">Periodo precedente</span><span class="sxs-lookup"><span data-stu-id="0820f-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0820f-186">-1AF[1..LP]</span><span class="sxs-lookup"><span data-stu-id="0820f-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="0820f-187">Intero anno fiscale precedente</span><span class="sxs-lookup"><span data-stu-id="0820f-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0820f-188">-1AF</span><span class="sxs-lookup"><span data-stu-id="0820f-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="0820f-189">Periodo corrente nel precedente anno fiscale</span><span class="sxs-lookup"><span data-stu-id="0820f-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0820f-190">-1AF[1..3]</span><span class="sxs-lookup"><span data-stu-id="0820f-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="0820f-191">Primo trimestre dell'anno fiscale trascorso</span><span class="sxs-lookup"><span data-stu-id="0820f-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0820f-192">-1AF[1..CP]</span><span class="sxs-lookup"><span data-stu-id="0820f-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="0820f-193">Dall'inizio dell'anno fiscale trascorso al periodo corrente dell'anno fiscale trascorso compreso</span><span class="sxs-lookup"><span data-stu-id="0820f-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0820f-194">-1AF[CP..LP]</span><span class="sxs-lookup"><span data-stu-id="0820f-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="0820f-195">Dal periodo corrente dell'anno fiscale trascorso all'ultimo periodo dell'anno fiscale trascorso compreso</span><span class="sxs-lookup"><span data-stu-id="0820f-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0820f-196">Se si desidera eseguire i calcoli in base a periodi di tempo regolari, è necessario invece immettere una formula nel campo **Formula confronto data**.</span><span class="sxs-lookup"><span data-stu-id="0820f-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="0820f-197">Non è sempre trasparente quali periodi si stanno confrontando perché è possibile impostare un filtro per data su un report che si estende su date diverse rispetto ai periodi contabili che si riflettono nei dati nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="0820f-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="0820f-198">Ad esempio, si crea una situazione contabile in cui si desidera confrontare il periodo corrente con lo stesso periodo dell'anno precedente, quindi si imposta il campo **Filtro periodo di confronto** su *-1AF*.</span><span class="sxs-lookup"><span data-stu-id="0820f-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="0820f-199">Quindi, si esegue il report il 28 febbraio e si imposta il filtro della data su gennaio e febbraio.</span><span class="sxs-lookup"><span data-stu-id="0820f-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="0820f-200">Di conseguenza, la situazione contabile confronta gennaio e febbraio di quest'anno con gennaio dell'anno scorso, che è l'unico periodo contabile completato dei due per l'anno prima.</span><span class="sxs-lookup"><span data-stu-id="0820f-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="0820f-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0820f-201">See Also</span></span>
[<span data-ttu-id="0820f-202">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="0820f-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="0820f-203">Finanze</span><span class="sxs-lookup"><span data-stu-id="0820f-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="0820f-204">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="0820f-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="0820f-205">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="0820f-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="0820f-206">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0820f-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

