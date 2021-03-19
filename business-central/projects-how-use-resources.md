---
title: Registrare e rettificare l'utilizzo e i prezzi delle risorse| Documenti Microsoft
description: Descrive come registrare l'utilizzo o il consumo di risorse associato a una commessa, per tenere traccia e gestire i costi, i prezzi e i tipi di lavoro.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 48d7615ec32424400133c9dbf6b63c46d450f019
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388376"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="859ea-103">Utilizzare le risorse per le commesse</span><span class="sxs-lookup"><span data-stu-id="859ea-103">Use Resources for Jobs</span></span>
<span data-ttu-id="859ea-104">Si registra l'utilizzo di risorse nelle registrazioni commesse per tenere traccia dei costi, dei prezzi e dei tipi di lavoro che sono collegati alle commesse.</span><span class="sxs-lookup"><span data-stu-id="859ea-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="859ea-105">Per ulteriori informazioni, vedere [Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="859ea-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="859ea-106">Puoi inoltre acquistare risorse esterne, ad esempio, per fatturare a un fornitore per il lavoro eseguito.</span><span class="sxs-lookup"><span data-stu-id="859ea-106">You can also purchase external resources, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="859ea-107">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="859ea-107">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="859ea-108">Si può anche registrare l'utilizzo di una risorsa nelle registrazioni risorse.</span><span class="sxs-lookup"><span data-stu-id="859ea-108">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="859ea-109">Le voci registrate nelle registrazioni risorse non influiscono sulla contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="859ea-109">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="859ea-110">Per assegnare le risorse alle commesse</span><span class="sxs-lookup"><span data-stu-id="859ea-110">To assign resources to jobs</span></span>
<span data-ttu-id="859ea-111">È possibile assegnare le risorse alle commesse creando righe di pianificazione commessa per la commessa.</span><span class="sxs-lookup"><span data-stu-id="859ea-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="859ea-112">Per ulteriori informazioni, vedere [Creare le commesse](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="859ea-112">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="859ea-113">Per registrare l'utilizzo delle risorse per una commessa</span><span class="sxs-lookup"><span data-stu-id="859ea-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="859ea-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni commesse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="859ea-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="859ea-115">Aprire il batch di registrazioni delle commesse interessato e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="859ea-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="859ea-116">Una volta completate le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="859ea-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="859ea-117">Per rettificare i prezzi delle risorse</span><span class="sxs-lookup"><span data-stu-id="859ea-117">To adjust resource prices</span></span>
<span data-ttu-id="859ea-118">Se si desidera modificare i costi o i prezzi di un gran numero di risorse, si può usare un processo batch.</span><span class="sxs-lookup"><span data-stu-id="859ea-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="859ea-119">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Rettifica costi/prezzi risorse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="859ea-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="859ea-120">Compilare i campi su una riga in base alle esigenze, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="859ea-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="859ea-121">Questo processo batch non consente di creare o rettificare costi e prezzi alternativi per le risorse.</span><span class="sxs-lookup"><span data-stu-id="859ea-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="859ea-122">Modifica soltanto il contenuto del campo nella scheda risorsa per il campo **Rettifica campo** selezionato nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="859ea-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="859ea-123">Poiché la rettifica diventerà effettiva immediatamente per le risorse, controllare i fattori di rettifica prima di eseguire il processo batch.</span><span class="sxs-lookup"><span data-stu-id="859ea-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="859ea-124">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi esistenti</span><span class="sxs-lookup"><span data-stu-id="859ea-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="859ea-125">Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.</span><span class="sxs-lookup"><span data-stu-id="859ea-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="859ea-126">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modifiche prezzi risorse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="859ea-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="859ea-127">Scegliere l'azione **Sugg. modif. prezzo ris. (prezzo)** e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="859ea-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="859ea-128">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="859ea-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="859ea-129">Al termine del processo batch, i relativi risultati saranno visualizzati nella pagina **Modifiche prezzi risorsa**.</span><span class="sxs-lookup"><span data-stu-id="859ea-129">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="859ea-130">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi standard</span><span class="sxs-lookup"><span data-stu-id="859ea-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="859ea-131">Se si desidera impostare più prezzi di risorsa alternativi basati sui prezzi standard nelle schede risorse, è possibile utilizzare un processo batch .</span><span class="sxs-lookup"><span data-stu-id="859ea-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="859ea-132">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modifiche prezzi risorse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="859ea-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="859ea-133">Scegliere l'azione **Sugg. mod. prezzo ris. (ris.)** e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="859ea-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="859ea-134">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="859ea-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="859ea-135">Al termine del processo batch, aprire la pagina **Modifiche prezzi risorsa** per visualizzarne i risultati.</span><span class="sxs-lookup"><span data-stu-id="859ea-135">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="859ea-136">Per ottenere suggerimenti per la modifica del prezzo di una risorsa sulla base dei prezzi alternativi</span><span class="sxs-lookup"><span data-stu-id="859ea-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="859ea-137">Se è già stato impostato il prezzo di risorsa alternativo per alcune risorse, è possibile utilizzare un processo batch per impostare più prezzi di risorse alternativi.</span><span class="sxs-lookup"><span data-stu-id="859ea-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="859ea-138">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Sugg. mod. prezzo ris.(prezzo)** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="859ea-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="859ea-139">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="859ea-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="859ea-140">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="859ea-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="859ea-141">Al termine del processo batch, aprire la pagina **Modifiche prezzi risorsa** per visualizzarne i risultati.</span><span class="sxs-lookup"><span data-stu-id="859ea-141">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="859ea-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="859ea-142">See Also</span></span>
[<span data-ttu-id="859ea-143">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="859ea-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="859ea-144">Finanze</span><span class="sxs-lookup"><span data-stu-id="859ea-144">Finance</span></span>](finance.md)  
<span data-ttu-id="859ea-145">[Acquisti](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="859ea-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="859ea-146">[Vendite](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="859ea-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="859ea-147">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="859ea-147">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]