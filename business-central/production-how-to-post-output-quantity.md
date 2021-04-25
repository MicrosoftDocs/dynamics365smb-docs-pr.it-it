---
title: Registrare l'output e i tempi di lavorazione tramite processo batch
description: La quantità di output rappresenta l'avanzamento del lavoro sotto forma di quantità finita e capacità utilizzata del centro lavoro o della macchina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787879"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="9cdaa-103">Registrare l'output e i tempi di lavorazione tramite processo batch</span><span class="sxs-lookup"><span data-stu-id="9cdaa-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="9cdaa-104">La quantità di output rappresenta l'avanzamento del lavoro sotto forma di quantità finita e capacità utilizzata del centro lavoro o della macchina.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="9cdaa-105">È possibile usare le registrazioni output su:</span><span class="sxs-lookup"><span data-stu-id="9cdaa-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="9cdaa-106">Rettifica il magazzino in relazione all'output degli articoli finiti da produzione.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="9cdaa-107">Registrare le quantità e gli scarti per ciascuna operazione nel ciclo di produzione.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="9cdaa-108">Registrare la configurazione e il tempo di esecuzione per il lavoro e i centri lavoro.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="9cdaa-109">Se viene utilizzato un instradamento della produzione, il magazzino viene aggiornato solo quando registri la quantità di output nell'ultima operazione.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="9cdaa-110">Tramite la finestra **Registrazioni di produzione**, è possibile eseguire le stesse attività della finestra **Registrazioni output** e allo stesso tempo le relative attività di registrazione del consumo.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="9cdaa-111">Per ulteriori informazioni, vedi [Registrare i consumi e l'output relativi a una singola riga dell'ordine di produzione rilasciato](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="9cdaa-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="9cdaa-112">Per registrare quantità di output e/o registrare tempi di lavorazione per una o più righe dell'ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="9cdaa-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="9cdaa-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni output** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9cdaa-114">Compilare i campi inserendo i dati relativi agli ordini di produzione e/o ai tempi di lavorazione.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="9cdaa-115">Puoi usare la funzione **Esplodi ciclo** per generare righe di registrazione dagli ordini di produzione.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="9cdaa-116">Se l'operazione è stata completata, selezionare il campo **Completato** .</span><span class="sxs-lookup"><span data-stu-id="9cdaa-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="9cdaa-117">Per registrare le operazioni scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="9cdaa-118">I movimenti contabili capacità vengono aggiornati per il lavoro utilizzato o per i centri lavoro con informazioni su tempo e quantità di produzione e scarto.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="9cdaa-119">Se hai registrato l'ultima operazione, l'articolo verrà aggiunto al magazzino.</span><span class="sxs-lookup"><span data-stu-id="9cdaa-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="9cdaa-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9cdaa-120">See Also</span></span>  
<span data-ttu-id="9cdaa-121">[Registrare lo scarto manualmente](production-how-to-post-scrap.md)
[Stornare la registrazione dell'output](production-how-to-reverse-output-posting.md)
[Produzione](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9cdaa-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="9cdaa-122">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="9cdaa-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="9cdaa-123">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="9cdaa-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="9cdaa-124">Magazzino</span><span class="sxs-lookup"><span data-stu-id="9cdaa-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="9cdaa-125">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9cdaa-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
