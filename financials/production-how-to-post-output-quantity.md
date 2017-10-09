---
title: Come registrare l'output e i tempi di lavorazione tramite processo batch| Microsoft Docs
description: "La quantità di output rappresenta la quantità finita nel WIP ( work in progress)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ee5ee5d08804439a79f8029eaa25ab7547349a1b
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-output-and-run-times"></a><span data-ttu-id="6c355-103">Procedura: Registrare l'output e i tempi di lavorazione tramite processo batch</span><span class="sxs-lookup"><span data-stu-id="6c355-103">How to: Batch Post Output and Run Times</span></span>
<span data-ttu-id="6c355-104">La quantità di output rappresenta la quantità finita nel WIP (work in progress).</span><span class="sxs-lookup"><span data-stu-id="6c355-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="6c355-105">il magazzino viene aggiornato automaticamente solo quando si registra la quantità di output per l'ultima operazione.</span><span class="sxs-lookup"><span data-stu-id="6c355-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="6c355-106">Per registrare quantità di output per una o più righe dell'ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="6c355-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="6c355-107">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni output**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6c355-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6c355-108">Compilare i campi inserendo i dati relativi agli ordini di produzione e all'output.</span><span class="sxs-lookup"><span data-stu-id="6c355-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="6c355-109">Se l'operazione è stata completata, selezionare il campo **Completato** .</span><span class="sxs-lookup"><span data-stu-id="6c355-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="6c355-110">Se l'ubicazione della warehouse in cui devono essere stoccati gli articoli prevede l'utilizzo di collocazioni, ma non richiede l'elaborazione degli stoccaggi,  assegnare un codice collocazione alla riga delle registrazioni per specificare dove dovranno essere immagazzinati gli articoli nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="6c355-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="6c355-111">Per ulteriori informazioni, vedere [Procedura: Stoccare l'output produzione o l'output assemblaggio](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="6c355-111">For more information, see [How to: Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="6c355-112">Per registrare le operazioni scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="6c355-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="6c355-113">La quantità di output verrà registrata.</span><span class="sxs-lookup"><span data-stu-id="6c355-113">The output quantity will be posted.</span></span> <span data-ttu-id="6c355-114">A questo punto, l'articolo è disponibile per la spedizione.</span><span class="sxs-lookup"><span data-stu-id="6c355-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="6c355-115">Per registrare il tempo di lavorazione per una o più righe dell'ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="6c355-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="6c355-116">Il tempo di lavorazione rappresenta le ore di lavoro necessarie per il WIP (work in progress).</span><span class="sxs-lookup"><span data-stu-id="6c355-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="6c355-117">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni output**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6c355-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6c355-118">Compilare i campi inserendo i dati relativi agli ordini di produzione e all'output.</span><span class="sxs-lookup"><span data-stu-id="6c355-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="6c355-119">Se l'operazione è terminata, selezionare il campo **Completato** .</span><span class="sxs-lookup"><span data-stu-id="6c355-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="6c355-120">Scegliere l'azione **Registra** per registrare il tempo impiegato per operazione.</span><span class="sxs-lookup"><span data-stu-id="6c355-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="6c355-121">I movimenti contabili capacità vengono aggiornati per le aree di produzione o i centri di lavoro utilizzati.</span><span class="sxs-lookup"><span data-stu-id="6c355-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c355-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c355-122">See Also</span></span>  
<span data-ttu-id="6c355-123">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6c355-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="6c355-124">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="6c355-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="6c355-125">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="6c355-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="6c355-126">Magazzino</span><span class="sxs-lookup"><span data-stu-id="6c355-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6c355-127">Acquisti</span><span class="sxs-lookup"><span data-stu-id="6c355-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6c355-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6c355-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

