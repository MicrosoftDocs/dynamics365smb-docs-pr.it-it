---
title: Analisi degli importi effettivi e degli importi di budget| Documenti Microsoft
description: Descrive come analizzare gli importi effettivi e gli importi di budget.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 12/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: e76d590476b1236bf1d82a7f5e4f502ffdd9d02d
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="bc308-103">Procedura: Analisi degli importi effettivi e degli importi di budget</span><span class="sxs-lookup"><span data-stu-id="bc308-103">How to: Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="bc308-104">Come parte della raccolta, dell'analisi e della condivisione dei dati della società, si visualizzano gli importi effettivi rispetto agli importi di budget per tutti i conti e per diversi periodi.</span><span class="sxs-lookup"><span data-stu-id="bc308-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="bc308-105">Per analizzare gli importi di budget, è prima necessario creare budget C/G.</span><span class="sxs-lookup"><span data-stu-id="bc308-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="bc308-106">Per ulteriori informazioni, vedere [Procedura: Creare budget C/G](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="bc308-106">For more information, see [How to: Create G/L Budgets](finance-how-create-budgets.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="bc308-107">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="bc308-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="bc308-108">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="bc308-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="bc308-109">Per visualizzare un budget C/G</span><span class="sxs-lookup"><span data-stu-id="bc308-109">To view a G/L budget</span></span>
<span data-ttu-id="bc308-110">In un budget per cui siano state impostate delle dimensioni è possibile filtrare i movimenti e visualizzare budget specifici.</span><span class="sxs-lookup"><span data-stu-id="bc308-110">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="bc308-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Budget C/G**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bc308-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="bc308-112">Nella finestra **Budget CG** aprire il budget che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="bc308-112">In the **G/L Budgets** window, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="bc308-113">All'inizio della finestra, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="bc308-113">At the top of the window, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="bc308-114">Se è stato selezionato il valore **Periodo** nel campo **Mostra come righe** oppure nel campo **Mostra come colonne**, è necessario compilare il campo **Visualizza per**.</span><span class="sxs-lookup"><span data-stu-id="bc308-114">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="bc308-115">Se non è stato selezionato il valore **Periodo** nel campo **Mostra come righe** o **Mostra come colonne** immettere il periodo appropriato nel campo **Filtro data**.</span><span class="sxs-lookup"><span data-stu-id="bc308-115">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="bc308-116">Sono inclusi nel calcolo solo i movimenti del budget contabilità generale con i codici di filtro che vengono immessi nella Scheda dettaglio **Filtri**.</span><span class="sxs-lookup"><span data-stu-id="bc308-116">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="bc308-117">I movimenti di budget con codici di filtro diversi o privi di codice ne sono esclusi.</span><span class="sxs-lookup"><span data-stu-id="bc308-117">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="bc308-118">Finché il filtro rimane nella finestra nel budget vengono visualizzate unicamente i movimenti con questi codici di filtro.</span><span class="sxs-lookup"><span data-stu-id="bc308-118">As long as the filter remains on the window, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="bc308-119">Se si desidera modificare il budget, è possibile modificare i movimenti del budget.</span><span class="sxs-lookup"><span data-stu-id="bc308-119">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="bc308-120">Scegliere un importo per visualizzare i movimenti del budget della contabilità generale sottostanti.</span><span class="sxs-lookup"><span data-stu-id="bc308-120">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="bc308-121">Per visualizzare gli importi effettivi e preventivati di tutti i conti</span><span class="sxs-lookup"><span data-stu-id="bc308-121">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="bc308-122">È possibile visualizzare budget di contabilità generale e confrontarli con le cifre effettive in diverse aree di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bc308-122">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="bc308-123">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bc308-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc308-124">Nella finestra **Piano dei conti**, selezionare l'azione **Saldo budget C/G**.</span><span class="sxs-lookup"><span data-stu-id="bc308-124">In the **Chart of Accounts** window, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="bc308-125">All'inizio della finestra, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="bc308-125">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="bc308-126">Per visualizzare una specifica che costituisce l'importo mostrato, selezionare il campo.</span><span class="sxs-lookup"><span data-stu-id="bc308-126">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="bc308-127">I filtri impostati nella testata della finestra verranno applicati sia ai movimenti C/G che ai movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="bc308-127">The filters you set in the window header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="bc308-128">Le colonne a sinistra contengono il piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="bc308-128">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="bc308-129">Delle quattro colonne sulla destra, le prime quattro indicano gli importi dare e avere effettivi e previsti per ciascun conto.</span><span class="sxs-lookup"><span data-stu-id="bc308-129">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="bc308-130">La quinta indica la relazione proporzionale tra gli importi effettivi e preventivati del conto C/G.</span><span class="sxs-lookup"><span data-stu-id="bc308-130">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="bc308-131">Utilizzare il campo **Visualizza per** nella finestra **Saldo budget C/G** per selezionare la durata del periodo.</span><span class="sxs-lookup"><span data-stu-id="bc308-131">Use the **View by** field in the **G/L Balance/Budget** window to select the period length.</span></span> <span data-ttu-id="bc308-132">Utilizzare il campo **Visualizza come** per selezionare la modalità di calcolo degli importi, **Saldo periodo** o **Saldo alla data**.</span><span class="sxs-lookup"><span data-stu-id="bc308-132">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="bc308-133">Scegliere l'azione **Periodo precedente** o **Periodo successivo** per modificare il periodo.</span><span class="sxs-lookup"><span data-stu-id="bc308-133">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="bc308-134">Per visualizzare importi effettivi e preventivati per più periodi</span><span class="sxs-lookup"><span data-stu-id="bc308-134">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="bc308-135">Oltre a visualizzare importi effettivi e preventivati di tutti i conti all'interno di un unico periodo è possibile visualizzare un certo numero di periodo per un unico conto.</span><span class="sxs-lookup"><span data-stu-id="bc308-135">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="bc308-136">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bc308-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc308-137">Nella finestra **Piano dei conti**, selezionare il conto di contabilità generale pertinente quindi scegliere l'azione **Confronto budget/contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="bc308-137">In the **Chart of Accounts** window, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="bc308-138">All'inizio della finestra, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="bc308-138">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="bc308-139">Per visualizzare una specifica di un importo mostrato, selezionare il campo.</span><span class="sxs-lookup"><span data-stu-id="bc308-139">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bc308-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc308-140">See Also</span></span>
[<span data-ttu-id="bc308-141">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="bc308-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="bc308-142">Procedura: Utilizzare le situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="bc308-142">How to: Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="bc308-143">Finanze</span><span class="sxs-lookup"><span data-stu-id="bc308-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="bc308-144">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="bc308-144">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="bc308-145">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="bc308-145">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="bc308-146">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

