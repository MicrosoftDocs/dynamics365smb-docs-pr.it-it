---
title: Analisi degli importi effettivi e degli importi di budget| Documenti Microsoft
description: Descrive come analizzare gli importi effettivi e gli importi di budget.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: cc0497b4e0add53ce983883cd58c10475c9d9a6e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783479"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="88c6e-103">Analisi degli importi effettivi e degli importi di budget</span><span class="sxs-lookup"><span data-stu-id="88c6e-103">Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="88c6e-104">Come parte della raccolta, dell'analisi e della condivisione dei dati della società, si visualizzano gli importi effettivi rispetto agli importi di budget per tutti i conti e per diversi periodi.</span><span class="sxs-lookup"><span data-stu-id="88c6e-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="88c6e-105">Per analizzare gli importi di budget, è prima necessario creare budget C/G.</span><span class="sxs-lookup"><span data-stu-id="88c6e-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="88c6e-106">Per ulteriori informazioni, vedere [Creare budget C/G](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="88c6e-106">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="88c6e-107">Per visualizzare un budget C/G</span><span class="sxs-lookup"><span data-stu-id="88c6e-107">To view a G/L budget</span></span>
<span data-ttu-id="88c6e-108">In un budget per cui siano state impostate delle dimensioni è possibile filtrare i movimenti e visualizzare budget specifici.</span><span class="sxs-lookup"><span data-stu-id="88c6e-108">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="88c6e-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Budget C/G** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="88c6e-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="88c6e-110">Nella pagina **Budget CG** aprire il budget che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="88c6e-110">On the **G/L Budgets** page, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="88c6e-111">All'inizio della pagina, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="88c6e-111">At the top of the page, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="88c6e-112">Se è stato selezionato il valore **Periodo** nel campo **Mostra come righe** oppure nel campo **Mostra come colonne**, è necessario compilare il campo **Visualizza per**.</span><span class="sxs-lookup"><span data-stu-id="88c6e-112">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="88c6e-113">Se non è stato selezionato il valore **Periodo** nel campo **Mostra come righe** o **Mostra come colonne** immettere il periodo appropriato nel campo **Filtro data**.</span><span class="sxs-lookup"><span data-stu-id="88c6e-113">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="88c6e-114">Sono inclusi nel calcolo solo i movimenti del budget contabilità generale con i codici di filtro che vengono immessi nella Scheda dettaglio **Filtri**.</span><span class="sxs-lookup"><span data-stu-id="88c6e-114">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="88c6e-115">I movimenti di budget con codici di filtro diversi o privi di codice ne sono esclusi.</span><span class="sxs-lookup"><span data-stu-id="88c6e-115">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="88c6e-116">Finché il filtro rimane nella pagina nel budget vengono visualizzate unicamente i movimenti con questi codici di filtro.</span><span class="sxs-lookup"><span data-stu-id="88c6e-116">As long as the filter remains on the page, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="88c6e-117">Se si desidera modificare il budget, è possibile modificare i movimenti del budget.</span><span class="sxs-lookup"><span data-stu-id="88c6e-117">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="88c6e-118">Scegliere un importo per visualizzare i movimenti del budget della contabilità generale sottostanti.</span><span class="sxs-lookup"><span data-stu-id="88c6e-118">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="88c6e-119">Per visualizzare gli importi effettivi e preventivati di tutti i conti</span><span class="sxs-lookup"><span data-stu-id="88c6e-119">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="88c6e-120">È possibile visualizzare budget di contabilità generale e confrontarli con le cifre effettive in diverse aree di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="88c6e-120">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="88c6e-121">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="88c6e-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="88c6e-122">Nella pagina **Piano dei conti**, selezionare l'azione **Saldo budget C/G**.</span><span class="sxs-lookup"><span data-stu-id="88c6e-122">On the **Chart of Accounts** page, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="88c6e-123">All'inizio della pagina, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="88c6e-123">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="88c6e-124">Per visualizzare una specifica che costituisce l'importo mostrato, selezionare il campo.</span><span class="sxs-lookup"><span data-stu-id="88c6e-124">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="88c6e-125">I filtri impostati nella testata della pagina verranno applicati sia ai movimenti C/G che ai movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="88c6e-125">The filters you set on the page header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="88c6e-126">Le colonne a sinistra contengono il piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="88c6e-126">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="88c6e-127">Delle quattro colonne sulla destra, le prime quattro indicano gli importi dare e avere effettivi e previsti per ciascun conto.</span><span class="sxs-lookup"><span data-stu-id="88c6e-127">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="88c6e-128">La quinta indica la relazione proporzionale tra gli importi effettivi e preventivati del conto C/G.</span><span class="sxs-lookup"><span data-stu-id="88c6e-128">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="88c6e-129">Utilizzare il campo **Visualizza per** nella pagina **Saldo budget C/G** per selezionare la durata del periodo.</span><span class="sxs-lookup"><span data-stu-id="88c6e-129">Use the **View by** field on the **G/L Balance/Budget** page to select the period length.</span></span> <span data-ttu-id="88c6e-130">Utilizzare il campo **Visualizza come** per selezionare la modalità di calcolo degli importi, **Saldo periodo** o **Saldo alla data**.</span><span class="sxs-lookup"><span data-stu-id="88c6e-130">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="88c6e-131">Scegliere l'azione **Periodo precedente** o **Periodo successivo** per modificare il periodo.</span><span class="sxs-lookup"><span data-stu-id="88c6e-131">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="88c6e-132">Per visualizzare importi effettivi e preventivati per più periodi</span><span class="sxs-lookup"><span data-stu-id="88c6e-132">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="88c6e-133">Oltre a visualizzare importi effettivi e preventivati di tutti i conti all'interno di un unico periodo è possibile visualizzare un certo numero di periodo per un unico conto.</span><span class="sxs-lookup"><span data-stu-id="88c6e-133">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="88c6e-134">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="88c6e-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="88c6e-135">Nella pagina **Piano dei conti**, selezionare il conto di contabilità generale pertinente quindi scegliere l'azione **Confronto budget/contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="88c6e-135">On the **Chart of Accounts** page, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="88c6e-136">All'inizio della pagina, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="88c6e-136">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="88c6e-137">Per visualizzare una specifica di un importo mostrato, selezionare il campo.</span><span class="sxs-lookup"><span data-stu-id="88c6e-137">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="88c6e-138">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="88c6e-138">See Related Training at [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="88c6e-139">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="88c6e-139">See Also</span></span>
[<span data-ttu-id="88c6e-140">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="88c6e-140">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="88c6e-141">Utilizzare le situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="88c6e-141">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="88c6e-142">Finanze</span><span class="sxs-lookup"><span data-stu-id="88c6e-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="88c6e-143">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="88c6e-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="88c6e-144">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="88c6e-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="88c6e-145">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="88c6e-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
