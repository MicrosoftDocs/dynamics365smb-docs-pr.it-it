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
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f86fed1b300df98ef120e2f91fdd0785670d04f1
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="784e2-103">Utilizzare le risorse per le commesse</span><span class="sxs-lookup"><span data-stu-id="784e2-103">Use Resources for Jobs</span></span>
<span data-ttu-id="784e2-104">Si registra l'utilizzo di risorse nelle registrazioni commesse per tenere traccia dei costi, dei prezzi e dei tipi di lavoro che sono collegati alle commesse.</span><span class="sxs-lookup"><span data-stu-id="784e2-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="784e2-105">Per ulteriori informazioni, vedere [Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="784e2-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="784e2-106">Si può anche registrare l'utilizzo di una risorsa nelle registrazioni risorse.</span><span class="sxs-lookup"><span data-stu-id="784e2-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="784e2-107">Le voci registrate nelle registrazioni risorse non influiscono sulla contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="784e2-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="784e2-108">Per assegnare le risorse alle commesse</span><span class="sxs-lookup"><span data-stu-id="784e2-108">To assign resources to jobs</span></span>
<span data-ttu-id="784e2-109">È possibile assegnare le risorse alle commesse creando righe di pianificazione commessa per la commessa.</span><span class="sxs-lookup"><span data-stu-id="784e2-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="784e2-110">Per ulteriori informazioni, vedere [Creare le commesse](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="784e2-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="784e2-111">Per registrare l'utilizzo delle risorse per una commessa</span><span class="sxs-lookup"><span data-stu-id="784e2-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="784e2-112">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="784e2-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="784e2-113">Aprire il batch di registrazioni delle commesse interessato e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="784e2-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="784e2-114">Una volta completate le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="784e2-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="784e2-115">Per rettificare i prezzi delle risorse</span><span class="sxs-lookup"><span data-stu-id="784e2-115">To adjust resource prices</span></span>
<span data-ttu-id="784e2-116">Se si desidera modificare i costi o i prezzi di un gran numero di risorse, si può usare un processo batch.</span><span class="sxs-lookup"><span data-stu-id="784e2-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="784e2-117">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Rettifica costi/Prezzi ris.**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="784e2-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="784e2-118">Compilare i campi su una riga in base alle esigenze, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="784e2-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="784e2-119">Questo processo batch non consente di creare o rettificare costi e prezzi alternativi per le risorse.</span><span class="sxs-lookup"><span data-stu-id="784e2-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="784e2-120">Modifica soltanto il contenuto del campo nella scheda risorsa per il campo **Rettifica campo** selezionato nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="784e2-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="784e2-121">Poiché la rettifica diventerà effettiva immediatamente per le risorse, controllare i fattori di rettifica prima di eseguire il processo batch.</span><span class="sxs-lookup"><span data-stu-id="784e2-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="784e2-122">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi esistenti</span><span class="sxs-lookup"><span data-stu-id="784e2-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="784e2-123">Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.</span><span class="sxs-lookup"><span data-stu-id="784e2-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="784e2-124">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modifiche prezzi risorsa**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="784e2-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="784e2-125">Scegliere l'azione **Sugg. modif. prezzo ris. (prezzo)** e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="784e2-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="784e2-126">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="784e2-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="784e2-127">Al termine del processo batch, i relativi risultati saranno visualizzati nella finestra **Modifiche prezzi risorsa**.</span><span class="sxs-lookup"><span data-stu-id="784e2-127">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="784e2-128">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi standard</span><span class="sxs-lookup"><span data-stu-id="784e2-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="784e2-129">Se si desidera impostare più prezzi di risorsa alternativi basati sui prezzi standard nelle schede risorse, è possibile utilizzare un processo batch .</span><span class="sxs-lookup"><span data-stu-id="784e2-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="784e2-130">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modifiche prezzi risorsa**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="784e2-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="784e2-131">Scegliere l'azione **Sugg. mod. prezzo ris. (ris.)** e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="784e2-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="784e2-132">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="784e2-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="784e2-133">Al termine del processo batch, aprire la finestra **Modifiche prezzi risorsa** per visualizzarne i risultati.</span><span class="sxs-lookup"><span data-stu-id="784e2-133">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="784e2-134">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi</span><span class="sxs-lookup"><span data-stu-id="784e2-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="784e2-135">Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.</span><span class="sxs-lookup"><span data-stu-id="784e2-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="784e2-136">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Sugg. mod. prezzo ris.(prezzo)**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="784e2-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="784e2-137">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="784e2-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="784e2-138">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="784e2-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="784e2-139">Al termine del processo batch, aprire la finestra **Modifiche prezzi risorsa** per visualizzarne i risultati.</span><span class="sxs-lookup"><span data-stu-id="784e2-139">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="784e2-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="784e2-140">See Also</span></span>
[<span data-ttu-id="784e2-141">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="784e2-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="784e2-142">Finanze</span><span class="sxs-lookup"><span data-stu-id="784e2-142">Finance</span></span>](finance.md)  
<span data-ttu-id="784e2-143">[Acquisti](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="784e2-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="784e2-144">[Vendite](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="784e2-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="784e2-145">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="784e2-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

