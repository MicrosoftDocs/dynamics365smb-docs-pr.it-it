---
title: Registrare e rettificare l'utilizzo e i prezzi delle risorse| Documenti Microsoft
description: Descrive come registrare l'utilizzo o il consumo di risorse associato a una commessa, per tenere traccia e gestire i costi, i prezzi e i tipi di lavoro.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 48692c9837007c6dd9c3891f0940b6f15b1d6541
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-resources-for-jobs"></a><span data-ttu-id="eb969-103">Procedura: Utilizzare le risorse per le commesse</span><span class="sxs-lookup"><span data-stu-id="eb969-103">How to: Use Resources for Jobs</span></span>
<span data-ttu-id="eb969-104">Si registra l'utilizzo di risorse nelle registrazioni commesse per tenere traccia dei costi, dei prezzi e dei tipi di lavoro che sono collegati alle commesse.</span><span class="sxs-lookup"><span data-stu-id="eb969-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="eb969-105">Per ulteriori informazioni, vedere [Procedura: Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="eb969-105">For more information, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="eb969-106">Si può anche registrare l'utilizzo di una risorsa nelle registrazioni risorse.</span><span class="sxs-lookup"><span data-stu-id="eb969-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="eb969-107">Le voci registrate nelle registrazioni risorse non influiscono sulla contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="eb969-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

> [!NOTE]  
>   <span data-ttu-id="eb969-108">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="eb969-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="eb969-109">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="eb969-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="eb969-110">Per assegnare le risorse alle commesse</span><span class="sxs-lookup"><span data-stu-id="eb969-110">To assign resources to jobs</span></span>
<span data-ttu-id="eb969-111">È possibile assegnare le risorse alle commesse creando righe di pianificazione commessa per la commessa.</span><span class="sxs-lookup"><span data-stu-id="eb969-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="eb969-112">Per ulteriori informazioni, vedere [Procedura: Creare commesse](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="eb969-112">For more information, see [How to: Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="eb969-113">Per registrare l'utilizzo delle risorse per una commessa</span><span class="sxs-lookup"><span data-stu-id="eb969-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="eb969-114">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="eb969-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="eb969-115">Aprire il batch di registrazioni delle commesse interessato e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="eb969-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="eb969-116">Una volta completate le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="eb969-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="eb969-117">Per rettificare i prezzi delle risorse</span><span class="sxs-lookup"><span data-stu-id="eb969-117">To adjust resource prices</span></span>
<span data-ttu-id="eb969-118">Se si desidera modificare i costi o i prezzi di un gran numero di risorse, si può usare un processo batch.</span><span class="sxs-lookup"><span data-stu-id="eb969-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="eb969-119">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Rettifica costi/Prezzi ris.**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="eb969-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="eb969-120">Compilare i campi su una riga in base alle esigenze, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb969-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="eb969-121">Questo processo batch non consente di creare o rettificare costi e prezzi alternativi per le risorse.</span><span class="sxs-lookup"><span data-stu-id="eb969-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="eb969-122">Modifica soltanto il contenuto del campo nella scheda risorsa per il campo **Rettifica campo** selezionato nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="eb969-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="eb969-123">Poiché la rettifica diventerà effettiva immediatamente per le risorse, controllare i fattori di rettifica prima di eseguire il processo batch.</span><span class="sxs-lookup"><span data-stu-id="eb969-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="eb969-124">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi esistenti</span><span class="sxs-lookup"><span data-stu-id="eb969-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="eb969-125">Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.</span><span class="sxs-lookup"><span data-stu-id="eb969-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="eb969-126">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modifiche prezzi risorsa**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="eb969-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="eb969-127">Scegliere l'azione **Sugg. modif. prezzo ris. (prezzo)** e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="eb969-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="eb969-128">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb969-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="eb969-129">Al termine del processo batch, i relativi risultati saranno visualizzati nella finestra **Modifiche prezzi risorsa**.</span><span class="sxs-lookup"><span data-stu-id="eb969-129">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="eb969-130">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi standard</span><span class="sxs-lookup"><span data-stu-id="eb969-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="eb969-131">Se si desidera impostare più prezzi di risorsa alternativi basati sui prezzi standard nelle schede risorse, è possibile utilizzare un processo batch .</span><span class="sxs-lookup"><span data-stu-id="eb969-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="eb969-132">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modifiche prezzi risorsa**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="eb969-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="eb969-133">Scegliere l'azione **Sugg. mod. prezzo ris. (ris.)** e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="eb969-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="eb969-134">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb969-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="eb969-135">Al termine del processo batch, aprire la finestra **Modifiche prezzi risorsa** per visualizzarne i risultati.</span><span class="sxs-lookup"><span data-stu-id="eb969-135">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="eb969-136">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi</span><span class="sxs-lookup"><span data-stu-id="eb969-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="eb969-137">Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.</span><span class="sxs-lookup"><span data-stu-id="eb969-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="eb969-138">Nella casella **Cerca** immettere **Sugg. mod. prezzo ris. (prezzo)**, quindi selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="eb969-138">In the **Search** box, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb969-139">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="eb969-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="eb969-140">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb969-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="eb969-141">Al termine del processo batch, aprire la finestra **Modifiche prezzi risorsa** per visualizzarne i risultati.</span><span class="sxs-lookup"><span data-stu-id="eb969-141">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb969-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb969-142">See Also</span></span>
[<span data-ttu-id="eb969-143">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="eb969-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="eb969-144">Finanze</span><span class="sxs-lookup"><span data-stu-id="eb969-144">Finance</span></span>](finance.md)  
<span data-ttu-id="eb969-145">[Acquisti](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="eb969-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="eb969-146">[Vendite](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="eb969-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="eb969-147">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eb969-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

