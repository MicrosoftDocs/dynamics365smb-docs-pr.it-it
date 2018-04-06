---
title: Creazione di budget C/G | Microsoft Docs
description: "Descrive come creare i budget C/G per prevedere diverse attività finanziarie e assegnare le dimensioni per scopi di business intelligence."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dd3be77519075b67a942402bd01d5a2a562a1c32
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="dafee-103">Creare budget C/G</span><span class="sxs-lookup"><span data-stu-id="dafee-103">Create G/L Budgets</span></span>
<span data-ttu-id="dafee-104">È possibile mantenere più budget per periodi di tempo identici creando budget con nomi separati.</span><span class="sxs-lookup"><span data-stu-id="dafee-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="dafee-105">Innanzitutto è necessario impostare il nome del budget e immettere le relative cifre.</span><span class="sxs-lookup"><span data-stu-id="dafee-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="dafee-106">Il nome del budget viene quindi inserito in tutti i movimenti di budget che vengono creati.</span><span class="sxs-lookup"><span data-stu-id="dafee-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="dafee-107">Quando si crea un budget, è possibile definire quattro dimensioni per ogni budget.</span><span class="sxs-lookup"><span data-stu-id="dafee-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="dafee-108">Queste quattro dimensioni specifiche per un singolo budget sono definite dimensioni budget.</span><span class="sxs-lookup"><span data-stu-id="dafee-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="dafee-109">Le dimensioni budget possono essere scelte tra le dimensioni impostate</span><span class="sxs-lookup"><span data-stu-id="dafee-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="dafee-110">Le dimensioni budget possono essere utilizzate per applicare filtri ai budget oppure per aggiungere informazioni sulle dimensioni ai movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="dafee-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="dafee-111">Per ulteriori informazioni, vedere [Utilizzo delle dimensioni](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="dafee-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="dafee-112">I budget giocano un ruolo importante in business intelligence, ad esempio nel rendiconto finanziario definito in base alle situazioni contabili che includono movimenti budget oppure quando si analizzano gli importi a budget rispetto agli importi effettivi nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="dafee-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="dafee-113">Per ulteriori informazioni, vedere [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="dafee-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="dafee-114">I budget giocano un ruolo importante in business intelligence, ad esempio nel rendiconto finanziario definito in base alle situazioni contabili che includono movimenti budget oppure quando si analizzano gli importi a budget rispetto agli importi effettivi nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="dafee-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="dafee-115">Per ulteriori informazioni, vedere [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="dafee-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="dafee-116">Nella contabilità industriale si utilizzano i budget costi in modo simile.</span><span class="sxs-lookup"><span data-stu-id="dafee-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="dafee-117">Per altre informazioni, vedere [Creazione di budget di costi](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="dafee-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="dafee-118">Per creare un nuovo budget C/G</span><span class="sxs-lookup"><span data-stu-id="dafee-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="dafee-119">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Budget C/G**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="dafee-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dafee-120">Scegliere l'azione **Modifica lista** e compilare i campi necessari.</span><span class="sxs-lookup"><span data-stu-id="dafee-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="dafee-121">Scegliere l'azione **Modifica budget**.</span><span class="sxs-lookup"><span data-stu-id="dafee-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="dafee-122">All'inizio della finestra **Budget**, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="dafee-122">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="dafee-123">Verranno visualizzati solo i movimenti che contengono il nome del budget indicato nel campo **Nome budget**.</span><span class="sxs-lookup"><span data-stu-id="dafee-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="dafee-124">Poiché il nome budget è appena stato creato non ci saranno movimenti corrispondenti al filtro.</span><span class="sxs-lookup"><span data-stu-id="dafee-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="dafee-125">Di conseguenza, la finestra sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="dafee-125">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="dafee-126">Per immettere un importo, selezionare la appropriata nella matrice.</span><span class="sxs-lookup"><span data-stu-id="dafee-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="dafee-127">Verrà visualizzata la finestra **Movimenti budget C/G**.</span><span class="sxs-lookup"><span data-stu-id="dafee-127">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="dafee-128">Creare una nuova riga e compilare il campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="dafee-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="dafee-129">Chiudere la finestra **Movimenti budget C/G**.</span><span class="sxs-lookup"><span data-stu-id="dafee-129">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="dafee-130">Ripetere i passaggi da 5 a 6 per immettere tutti gli importi del budget.</span><span class="sxs-lookup"><span data-stu-id="dafee-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dafee-131">Nella Scheda dettaglio **Filtri** è possibile filtrare le informazioni in base alle dimensioni di budget impostate per il nome del budget.</span><span class="sxs-lookup"><span data-stu-id="dafee-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="dafee-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dafee-132">See Also</span></span>
[<span data-ttu-id="dafee-133">Finanze</span><span class="sxs-lookup"><span data-stu-id="dafee-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="dafee-134">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="dafee-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="dafee-135">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="dafee-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="dafee-136">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="dafee-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="dafee-137">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dafee-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

