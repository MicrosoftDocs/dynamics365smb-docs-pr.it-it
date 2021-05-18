---
title: Registrare il consumo tramite processo batch
description: Se il metodo di consuntivazione è Manuale, i componenti devono essere registrati manualmente nelle registrazioni consumi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b3ee6ca54e21605b4e9cf340b04656694c9801e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935188"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="764fb-103">Registrare il consumo produzione tramite processo batch</span><span class="sxs-lookup"><span data-stu-id="764fb-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="764fb-104">Se il metodo di consuntivazione è **Manuale**, i componenti devono essere registrati manualmente nelle registrazioni consumi.</span><span class="sxs-lookup"><span data-stu-id="764fb-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="764fb-105">Se è stato immesso un segno di spunta nel campo **Richiesto prelievo** della scheda Ubicazione per indicare che l'ubicazione richiede l'elaborazione dei prelievi di magazzino, non sarà necessario utilizzare questo processo batch.</span><span class="sxs-lookup"><span data-stu-id="764fb-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="764fb-106">gestirà il consumo quando si registra il prelievo di magazzino.</span><span class="sxs-lookup"><span data-stu-id="764fb-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="764fb-107">Per ulteriori informazioni, vedere [Prelevare per la produzione in configurazioni della warehouse di base](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="764fb-107">For more information, see [Pick for Production in Basic Warehouse Configurations](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span></span>  

<span data-ttu-id="764fb-108">È inoltre possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] sulla registrazione (*consuntivazione*) automatica dei componenti quando si avviano o si chiudono ordini di produzione.</span><span class="sxs-lookup"><span data-stu-id="764fb-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="764fb-109">Per ulteriori informazioni vedere [Attivare la consuntivazione dei componenti in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="764fb-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="764fb-110">Per registrare il consumo per una o più righe dell'ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="764fb-110">To post consumption for one or more production order lines</span></span>

1. <span data-ttu-id="764fb-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni consumi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="764fb-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="764fb-112">Compilare i campi inserendo i dati relativi agli ordini di produzione e al consumo.</span><span class="sxs-lookup"><span data-stu-id="764fb-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="764fb-113">Uso dell'azione **Calcolo basato su** per generare le righe di registrazione dagli ordini di produzione in base all'output attuale (la quantità di merci finite prodotte effettivamente) o sull'output previsto (la quantità di merci finite che ti aspetti di produrre).</span><span class="sxs-lookup"><span data-stu-id="764fb-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="764fb-114">Se è stata configurata la scheda Ubicazione per richiedere l'elaborazione del prelievo in magazzino, puoi immettere nel campo solo le quantità già prelevate tramite un'attività di magazzino nel campo **Quantità** nella pagina **Registrazioni consumi**, non qualsiasi quantità calcolata.</span><span class="sxs-lookup"><span data-stu-id="764fb-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="764fb-115">Per ulteriori informazioni, vedi [Prelevare per produzione o assemblaggio in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="764fb-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3. <span data-ttu-id="764fb-116">Per registrare il consumo scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="764fb-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="764fb-117">Si riducono le relative scorte.</span><span class="sxs-lookup"><span data-stu-id="764fb-117">The related inventories are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="764fb-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="764fb-118">See Also</span></span>

[<span data-ttu-id="764fb-119">Manufacturing</span><span class="sxs-lookup"><span data-stu-id="764fb-119">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="764fb-120">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="764fb-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="764fb-121">Pianif.</span><span class="sxs-lookup"><span data-stu-id="764fb-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="764fb-122">Magazzino</span><span class="sxs-lookup"><span data-stu-id="764fb-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="764fb-123">Acquisti</span><span class="sxs-lookup"><span data-stu-id="764fb-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="764fb-124">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="764fb-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]
