---
title: Creazione dei budget| Documenti Microsoft
description: "Descrive come creare i budget per prevedere diverse attività finanziarie e assegnare le dimensioni per scopi di business intelligence."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7dfd3cc7efe00b48a39982bb220ccc21b7409da4
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create--budgets"></a><span data-ttu-id="2cff9-103">Procedura: Creare budget</span><span class="sxs-lookup"><span data-stu-id="2cff9-103">How to: Create  Budgets</span></span>
<span data-ttu-id="2cff9-104">È possibile mantenere più budget per periodi di tempo identici creando budget con nomi separati.</span><span class="sxs-lookup"><span data-stu-id="2cff9-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="2cff9-105">Innanzitutto è necessario impostare il nome del budget e immettere le relative cifre.</span><span class="sxs-lookup"><span data-stu-id="2cff9-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="2cff9-106">Il nome del budget viene quindi inserito in tutti i movimenti di budget che vengono creati.</span><span class="sxs-lookup"><span data-stu-id="2cff9-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="2cff9-107">Quando si crea un budget, è possibile definire quattro dimensioni per ogni budget.</span><span class="sxs-lookup"><span data-stu-id="2cff9-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="2cff9-108">Queste quattro dimensioni specifiche per un singolo budget sono definite dimensioni budget.</span><span class="sxs-lookup"><span data-stu-id="2cff9-108">These budget\-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="2cff9-109">Le dimensioni budget possono essere scelte tra le dimensioni impostate</span><span class="sxs-lookup"><span data-stu-id="2cff9-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="2cff9-110">Le dimensioni budget possono essere utilizzate per applicare filtri ai budget oppure per aggiungere informazioni sulle dimensioni ai movimenti budget.</span><span class="sxs-lookup"><span data-stu-id="2cff9-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="2cff9-111">Per ulteriori informazioni, vedere [Utilizzo delle dimensioni](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="2cff9-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="2cff9-112">I budget giocano un ruolo importante in business intelligence, ad esempio nel rendiconto finanziario definito in base alle situazioni contabili che includono movimenti budget oppure quando si analizzano gli importi a budget rispetto agli importi effettivi nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="2cff9-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="2cff9-113">Per ulteriori informazioni, vedere [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="2cff9-113">For more information, see [Business Intelligence](bi.md).</span></span>   

 > [!NOTE]  
>   <span data-ttu-id="2cff9-114">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="2cff9-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="2cff9-115">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="2cff9-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

### <a name="to-create-a-new-budget"></a><span data-ttu-id="2cff9-116">Per creare un nuovo budget</span><span class="sxs-lookup"><span data-stu-id="2cff9-116">To create a new budget</span></span>  

1. <span data-ttu-id="2cff9-117">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Budget C/G**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="2cff9-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2cff9-118">Scegliere l'azione **Modifica lista** e compilare i campi necessari.</span><span class="sxs-lookup"><span data-stu-id="2cff9-118">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="2cff9-119">Scegliere l'azione **Modifica budget**.</span><span class="sxs-lookup"><span data-stu-id="2cff9-119">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="2cff9-120">All'inizio della finestra **Budget**, compilare i campi secondo le necessità per definire cosa viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2cff9-120">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="2cff9-121">Verranno visualizzati solo i movimenti che contengono il nome del budget indicato nel campo **Nome budget**.</span><span class="sxs-lookup"><span data-stu-id="2cff9-121">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="2cff9-122">Poiché il nome budget è appena stato creato non ci saranno movimenti corrispondenti al filtro.</span><span class="sxs-lookup"><span data-stu-id="2cff9-122">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="2cff9-123">Di conseguenza, la finestra sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="2cff9-123">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="2cff9-124">Per immettere un importo, selezionare la appropriata nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2cff9-124">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="2cff9-125">Verrà visualizzata la finestra **Movimenti budget C/G**.</span><span class="sxs-lookup"><span data-stu-id="2cff9-125">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="2cff9-126">Creare una nuova riga e compilare il campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="2cff9-126">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="2cff9-127">Chiudere la finestra **Movimenti budget C/G**.</span><span class="sxs-lookup"><span data-stu-id="2cff9-127">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="2cff9-128">Ripetere i passaggi da 5 a 6 per immettere tutti gli importi del budget.</span><span class="sxs-lookup"><span data-stu-id="2cff9-128">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2cff9-129">Nella Scheda dettaglio **Filtri** è possibile filtrare le informazioni in base alle dimensioni di budget impostate per il nome del budget.</span><span class="sxs-lookup"><span data-stu-id="2cff9-129">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="2cff9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cff9-130">See Also</span></span>
[<span data-ttu-id="2cff9-131">Finanze</span><span class="sxs-lookup"><span data-stu-id="2cff9-131">Finance</span></span>](finance.md)  
[<span data-ttu-id="2cff9-132">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="2cff9-132">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="2cff9-133">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="2cff9-133">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="2cff9-134">Contabilità generale e piano dei conti</span><span class="sxs-lookup"><span data-stu-id="2cff9-134">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="2cff9-135">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2cff9-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

