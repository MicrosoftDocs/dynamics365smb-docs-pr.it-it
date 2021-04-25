---
title: Registrare il consumo tramite processo batch
description: Se il metodo di consuntivazione è **Manuale**, i componenti devono essere registrati manualmente nelle registrazioni consumi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787904"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="9e8c2-103">Registrare il consumo produzione tramite processo batch</span><span class="sxs-lookup"><span data-stu-id="9e8c2-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="9e8c2-104">Se il metodo di consuntivazione è **Manuale**, i componenti devono essere registrati manualmente nelle registrazioni consumi.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="9e8c2-105">Se è stato immesso un segno di spunta nel campo **Richiesto prelievo** della scheda Ubicazione per indicare che l'ubicazione richiede l'elaborazione dei prelievi di magazzino, non sarà necessario utilizzare questo processo batch.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="9e8c2-106">gestirà il consumo quando si registra il prelievo di magazzino.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="9e8c2-107">Per ulteriori informazioni, vedi [Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="9e8c2-107">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span></span> 

<span data-ttu-id="9e8c2-108">È inoltre possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] sulla registrazione (*consuntivazione*) automatica dei componenti quando si avviano o si chiudono ordini di produzione.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="9e8c2-109">Per ulteriori informazioni vedere [Attivare la consuntivazione dei componenti in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="9e8c2-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="9e8c2-110">Per registrare il consumo per una o più righe dell'ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="9e8c2-110">To post consumption for one or more production order lines</span></span>

1.  <span data-ttu-id="9e8c2-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni consumi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9e8c2-112">Compilare i campi inserendo i dati relativi agli ordini di produzione e al consumo.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="9e8c2-113">Uso dell'azione **Calcolo basato su** per generare le righe di registrazione dagli ordini di produzione in base all'output attuale (la quantità di merci finite prodotte effettivamente) o sull'output previsto (la quantità di merci finite che ti aspetti di produrre).</span><span class="sxs-lookup"><span data-stu-id="9e8c2-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="9e8c2-114">Se è stata configurata la scheda Ubicazione per richiedere l'elaborazione del prelievo in magazzino, puoi immettere nel campo solo le quantità già prelevate tramite un'attività di magazzino nel campo **Quantità** nella pagina **Registrazioni consumi**, non qualsiasi quantità calcolata.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="9e8c2-115">Per ulteriori informazioni, vedi [Prelevare per produzione o assemblaggio in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="9e8c2-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3.  <span data-ttu-id="9e8c2-116">Per registrare il consumo scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="9e8c2-117">Si riducono le relative scorte.</span><span class="sxs-lookup"><span data-stu-id="9e8c2-117">The related inventories are reduced.</span></span>



## <a name="see-also"></a><span data-ttu-id="9e8c2-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9e8c2-118">See Also</span></span>

<span data-ttu-id="9e8c2-119">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9e8c2-119">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="9e8c2-120">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="9e8c2-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="9e8c2-121">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="9e8c2-121">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="9e8c2-122">Magazzino</span><span class="sxs-lookup"><span data-stu-id="9e8c2-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9e8c2-123">Acquisti</span><span class="sxs-lookup"><span data-stu-id="9e8c2-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9e8c2-124">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9e8c2-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
