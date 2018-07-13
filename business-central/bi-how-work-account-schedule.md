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
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: it-it
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="09c1f-103">Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti</span><span class="sxs-lookup"><span data-stu-id="09c1f-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="09c1f-104">Utilizzare le situazioni contabili per ottenere informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="09c1f-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="09c1f-105">Le situazioni contabili analizzano le cifre nei conti di contabilità generale e confrontano i movimenti di contabilità generale con i movimenti budget di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="09c1f-106">La visualizzazione dei risultati nei grafici nella Gestione ruolo utente, quali il piano del flusso di cassa e nei report, ad esempio i report Conto economico e Conto patrimoniale,</span><span class="sxs-lookup"><span data-stu-id="09c1f-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="09c1f-107">È possibile accedere a questi due report, ad esempio, con l'azione **Rendiconti finanziari** nella Gestione ruolo utente di Manager aziendale e Contabile.</span><span class="sxs-lookup"><span data-stu-id="09c1f-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="09c1f-108"> fornisce alcune situazioni contabili di esempio che è possibile utilizzare immediatamente oppure è possibile impostare le proprie righe e colonne per specificare le cifre da confrontare.</span><span class="sxs-lookup"><span data-stu-id="09c1f-108"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="09c1f-109">È ad esempio possibile creare piani dei conti per calcolare i margini di profitto in dimensioni quali reparti o gruppi di clienti.</span><span class="sxs-lookup"><span data-stu-id="09c1f-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="09c1f-110">È possibile creare quanti rendiconti finanziari personalizzati si desidera.</span><span class="sxs-lookup"><span data-stu-id="09c1f-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="09c1f-111">L'impostazione delle situazioni contabili richiede una comprensione dei dati finanziari nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="09c1f-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="09c1f-112">Per esempio, è possibile visualizzare i movimenti C/G come percentuali di movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="09c1f-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="09c1f-113">Tale operazione richiede che i budget siano creati.</span><span class="sxs-lookup"><span data-stu-id="09c1f-113">This requires that budgets are created.</span></span> <span data-ttu-id="09c1f-114">Per ulteriori informazioni, vedere [Creare budget C/G](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="09c1f-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="09c1f-115">Categorie di conti e situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="09c1f-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="09c1f-116">Le categorie di conto consentono di modificare il layout dei rendiconti finanziari.</span><span class="sxs-lookup"><span data-stu-id="09c1f-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="09c1f-117">Dopo aver impostato le categorie di conto nella finestra **Categorie conto C/G** scegliere l'azione **Genera situazioni contabili**, le situazioni contabili sottostanti i report finanziari principali verranno aggiornate.</span><span class="sxs-lookup"><span data-stu-id="09c1f-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="09c1f-118">Alla successiva esecuzione di uno dei report, ad esempio il report Conto patrimoniale, nuovi totali e voci secondarie vengono aggiunte, in base alle modifiche.</span><span class="sxs-lookup"><span data-stu-id="09c1f-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="09c1f-119">Per ulteriori informazioni, vedere la sezione Categorie di conti in [Informazioni sulla contabilità generale e COA](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="09c1f-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="09c1f-120">Per creare nuove situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="09c1f-120">To create new account schedules</span></span>  
 <span data-ttu-id="09c1f-121">Utilizzare situazioni contabili per analizzare le cifre nei conti di contabilità generale o confrontare i movimenti di contabilità generale con i movimenti budget di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="09c1f-122">Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="09c1f-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="09c1f-123">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="09c1f-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="09c1f-124">Nella finestra **Descr. situazioni contabili** scegliere l'azione **Nuovo** per creare una nuova descrizione situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="09c1f-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="09c1f-125">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="09c1f-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="09c1f-126">Scegliere l'azione **Modifica situazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="09c1f-127">Compilare i campi necessari nella finestra **Situazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="09c1f-128">Dopo aver creato una nuova situazione contabile e averne impostato le righe, è necessario impostare le colonne.</span><span class="sxs-lookup"><span data-stu-id="09c1f-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="09c1f-129">Le colonne possono essere impostate manualmente oppure assegnando un layout di colonne di default alla situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="09c1f-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="09c1f-130">Scegliere l'azione **Modifica setup layout colonna**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="09c1f-131">Compilare i campi necessari nella finestra **Layout colonna**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="09c1f-132">Se non è stato assegnato un default layout colonna alla situazione contabile, è necessario impostare le colonne manualmente.</span><span class="sxs-lookup"><span data-stu-id="09c1f-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="09c1f-133">Per copiare una situazione contabile esistente</span><span class="sxs-lookup"><span data-stu-id="09c1f-133">To copy an existing account schedule</span></span>
<span data-ttu-id="09c1f-134">Le situazioni contabili nella versione standard di [!INCLUDE[d365fin](includes/d365fin_md.md)] sono la base dei report finanziari standard, che potrebbero non essere adatti alle esigenze dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="09c1f-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="09c1f-135">Per creare rapidamente i propri report finanziari, è possibile iniziare copiando una situazione contabile esistente.</span><span class="sxs-lookup"><span data-stu-id="09c1f-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="09c1f-136">Nella finestra **Situazioni contabili**, selezionare una situazione contabile quindi scegliere l'azione **Copia situazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="09c1f-137">Nella finestra **Copia situazione contabile** compilare i campi in base alle esigenze, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="09c1f-138">Per creare una colonna per il calcolo delle percentuali</span><span class="sxs-lookup"><span data-stu-id="09c1f-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="09c1f-139">A volte, potrebbe essere necessario includere in una situazione contabile una colonna per il calcolo delle percentuali di un totale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="09c1f-140">Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, è possibile inserire una colonna per indicare la percentuale delle vendite totale rappresentata da ogni riga.</span><span class="sxs-lookup"><span data-stu-id="09c1f-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="09c1f-141">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="09c1f-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="09c1f-142">Nella finestra **Descr. situazioni contabili** selezionare una situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="09c1f-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="09c1f-143">Selezionare l'azione **Modifica situazione contabile** per impostare una riga della situazione contabile per calcolare il totale su cui saranno basate le percentuali.</span><span class="sxs-lookup"><span data-stu-id="09c1f-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="09c1f-144">Inserire una riga immediatamente sopra la prima riga per la quale si desidera visualizzare una percentuale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="09c1f-145">Compilare i campi della riga nel modo seguente: Nel campo **Tipo totale** immettere **Imposta base per percentuale**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="09c1f-146">Nel campo **Totale** immettere una formula del totale su cui sarà basata la percentuale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="09c1f-147">Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="09c1f-148">Scegliere l'azione **Modifica setup layout colonna** per impostare una colonna.</span><span class="sxs-lookup"><span data-stu-id="09c1f-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="09c1f-149">Compilare i campi della riga nel modo seguente: nel campo **Tipo colonna** selezionare **Formula**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="09c1f-150">Nel campo **Formula** immettere una formula per l'importo per il quale si desidera calcolare la percentuale, seguita dalla percentuale (%).</span><span class="sxs-lookup"><span data-stu-id="09c1f-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="09c1f-151">Ad esempio, se il numero di colonna N contiene il saldo periodo, immettere **N%**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="09c1f-152">Ripetere i passaggi da 4 a 7 per ogni gruppo di righe che di desidera suddividere per percentuale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="09c1f-153">Per impostare situazioni contabili con sintesi</span><span class="sxs-lookup"><span data-stu-id="09c1f-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="09c1f-154">È possibile utilizzare una situazione contabile per creare un rendiconto in cui vengono confrontate le cifre C/G con le cifre del budget C/G.</span><span class="sxs-lookup"><span data-stu-id="09c1f-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="09c1f-155">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Situazioni contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="09c1f-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="09c1f-156">Nella finestra **Descr. situazioni contabili** selezionare una situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="09c1f-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="09c1f-157">Scegliere l'azione **Modifica situazione contabile**</span><span class="sxs-lookup"><span data-stu-id="09c1f-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="09c1f-158">Nella finestra **Situazione contabile** selezionare il nome della situazione contabile di default nel campo **Nome**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="09c1f-159">Scegliere l'azione **Inserisci conti**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="09c1f-160">Selezionare i conti che si intendono includere nella dichiarazione e selezionare il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="09c1f-161">I conti sono stati inseriti nella situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="09c1f-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="09c1f-162">È inoltre possibile modificare il layout colonna.</span><span class="sxs-lookup"><span data-stu-id="09c1f-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="09c1f-163">Scegliere l'azione **Sintesi**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="09c1f-164">Fare clic sulla Scheda dettaglio **Filtri dimensione** e impostare il filtro budget con il nome di filtro desiderato.</span><span class="sxs-lookup"><span data-stu-id="09c1f-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="09c1f-165">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="09c1f-166">Ora è possibile copiare e incollare la dichiarazione di budget in un foglio elettronico.</span><span class="sxs-lookup"><span data-stu-id="09c1f-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="09c1f-167">Confronto dei periodi contabili con le formule periodo</span><span class="sxs-lookup"><span data-stu-id="09c1f-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="09c1f-168">La situazione contabile consente di confrontare i risultati di diversi periodi contabili, ad esempio mese corrente rispetto allo stesso mese dell'anno precedente.</span><span class="sxs-lookup"><span data-stu-id="09c1f-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="09c1f-169">Per fare ciò, aggiungere una colonna con il campo **Formula confronto periodo** quindi impostare tale campo su una formula periodo.</span><span class="sxs-lookup"><span data-stu-id="09c1f-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="09c1f-170">Un periodo contabile non deve corrispondere esattamente al calendario, ma ogni anno fiscale deve avere lo stesso numero di periodi contabili, che possono tuttavia avere una durata distinta.</span><span class="sxs-lookup"><span data-stu-id="09c1f-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="09c1f-171"> usa la formula periodo per calcolare l'importo dal periodo di confronto in relazione al periodo rappresentato dal filtro data nella richiesta del report.</span><span class="sxs-lookup"><span data-stu-id="09c1f-171"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="09c1f-172">Il periodo di confronto si basa sul periodo indicato dalla data di inizio del filtro data.</span><span class="sxs-lookup"><span data-stu-id="09c1f-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="09c1f-173">Le abbreviazioni per l'indicazione dei periodi sono:</span><span class="sxs-lookup"><span data-stu-id="09c1f-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09c1f-174">Abbreviazione</span><span class="sxs-lookup"><span data-stu-id="09c1f-174">Abbreviation</span></span></th>
<th><span data-ttu-id="09c1f-175">Description</span><span class="sxs-lookup"><span data-stu-id="09c1f-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09c1f-176">P</span><span class="sxs-lookup"><span data-stu-id="09c1f-176">P</span></span></p></td>
<td><p><span data-ttu-id="09c1f-177">Periodo</span><span class="sxs-lookup"><span data-stu-id="09c1f-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c1f-178">UP</span><span class="sxs-lookup"><span data-stu-id="09c1f-178">LP</span></span></p></td>
<td><p><span data-ttu-id="09c1f-179">Ultimo periodo di un trimestre, semestre o anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c1f-180">CP</span><span class="sxs-lookup"><span data-stu-id="09c1f-180">CP</span></span></p></td>
<td><p><span data-ttu-id="09c1f-181">Periodo corrente di un trimestre, semestre o anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c1f-182">AF</span><span class="sxs-lookup"><span data-stu-id="09c1f-182">FY</span></span></p></td>
<td><p><span data-ttu-id="09c1f-183">Anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="09c1f-183">Fiscal year.</span></span> <span data-ttu-id="09c1f-184">Ad esempio, AF[1..3] indica il primo trimestre dall'anno fiscale corrente</span><span class="sxs-lookup"><span data-stu-id="09c1f-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09c1f-185">Esempi di formule</span><span class="sxs-lookup"><span data-stu-id="09c1f-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09c1f-186">Formula</span><span class="sxs-lookup"><span data-stu-id="09c1f-186">Formula</span></span></th>
<th><span data-ttu-id="09c1f-187">Description</span><span class="sxs-lookup"><span data-stu-id="09c1f-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09c1f-188">&lt;Vuoto&gt;</span><span class="sxs-lookup"><span data-stu-id="09c1f-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="09c1f-189">Periodo corrente</span><span class="sxs-lookup"><span data-stu-id="09c1f-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c1f-190">-1P</span><span class="sxs-lookup"><span data-stu-id="09c1f-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="09c1f-191">Periodo precedente</span><span class="sxs-lookup"><span data-stu-id="09c1f-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c1f-192">-1AF[1..LP]</span><span class="sxs-lookup"><span data-stu-id="09c1f-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="09c1f-193">Intero anno fiscale precedente</span><span class="sxs-lookup"><span data-stu-id="09c1f-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c1f-194">-1AF</span><span class="sxs-lookup"><span data-stu-id="09c1f-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="09c1f-195">Periodo corrente nel precedente anno fiscale</span><span class="sxs-lookup"><span data-stu-id="09c1f-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c1f-196">-1AF[1..3]</span><span class="sxs-lookup"><span data-stu-id="09c1f-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="09c1f-197">Primo trimestre dell'anno fiscale trascorso</span><span class="sxs-lookup"><span data-stu-id="09c1f-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c1f-198">-1AF[1..CP]</span><span class="sxs-lookup"><span data-stu-id="09c1f-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="09c1f-199">Dall'inizio dell'anno fiscale trascorso al periodo corrente dell'anno fiscale trascorso compreso</span><span class="sxs-lookup"><span data-stu-id="09c1f-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c1f-200">-1AF[CP..LP]</span><span class="sxs-lookup"><span data-stu-id="09c1f-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="09c1f-201">Dal periodo corrente dell'anno fiscale trascorso all'ultimo periodo dell'anno fiscale trascorso compreso</span><span class="sxs-lookup"><span data-stu-id="09c1f-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09c1f-202">Se si desidera eseguire i calcoli in base a periodi di tempo regolari, è necessario invece immettere una formula nel campo **Formula confronto data**.</span><span class="sxs-lookup"><span data-stu-id="09c1f-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="09c1f-203">Non è sempre trasparente quali periodi si stanno confrontando perché è possibile impostare un filtro per data su un report che si estende su date diverse rispetto ai periodi contabili che si riflettono nei dati nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="09c1f-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="09c1f-204">Ad esempio, si crea una situazione contabile in cui si desidera confrontare il periodo corrente con lo stesso periodo dell'anno precedente, quindi si imposta il campo **Filtro periodo di confronto** su *-1AF*.</span><span class="sxs-lookup"><span data-stu-id="09c1f-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="09c1f-205">Quindi, si esegue il report il 28 febbraio e si imposta il filtro della data su gennaio e febbraio.</span><span class="sxs-lookup"><span data-stu-id="09c1f-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="09c1f-206">Di conseguenza, la situazione contabile confronta gennaio e febbraio di quest'anno con gennaio dell'anno scorso, che è l'unico periodo contabile completato dei due per l'anno prima.</span><span class="sxs-lookup"><span data-stu-id="09c1f-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="09c1f-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09c1f-207">See Also</span></span>
[<span data-ttu-id="09c1f-208">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="09c1f-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="09c1f-209">Finanze</span><span class="sxs-lookup"><span data-stu-id="09c1f-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="09c1f-210">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="09c1f-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="09c1f-211">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="09c1f-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="09c1f-212">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="09c1f-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

