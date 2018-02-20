---
title: Come pianificare gli ordini di progetto | Microsoft Docs
description: "Questa attività di pianificazione viene avviata da un ordine di vendita e utilizza la finestra **Pianifica ordine vendita**. Al termine della creazione di un ordine di produzione progetto, è possibile eseguire un'ulteriore pianificazione mediante la finestra **Pianificazione ordini**."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 27b2571df137b489a72673251fb5a176bfa771fe
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="plan-project-orders"></a><span data-ttu-id="4c536-104">Pianificare gli ordini di progetto</span><span class="sxs-lookup"><span data-stu-id="4c536-104">Plan Project Orders</span></span>
<span data-ttu-id="4c536-105">Questa attività di pianificazione viene avviata da un ordine di vendita e utilizza la finestra **Pianifica ordine vendita**.</span><span class="sxs-lookup"><span data-stu-id="4c536-105">This planning task starts from a sales order and uses the **Sales Order Planning** window.</span></span> <span data-ttu-id="4c536-106">Al termine della creazione di un ordine di produzione progetto, è possibile eseguire un'ulteriore pianificazione mediante la finestra **Pianificazione ordini**.</span><span class="sxs-lookup"><span data-stu-id="4c536-106">Once you have created a project production order, you can plan it further by using the **Order Planning** window.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="4c536-107">Per creare un ordine di produzione progetto</span><span class="sxs-lookup"><span data-stu-id="4c536-107">To create a project production order</span></span>  

1.  <span data-ttu-id="4c536-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini vendita**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="4c536-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4c536-109">Selezionare l'ordine di vendita che rappresenta il progetto di produzione, quindi scegliere l'azione **Pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="4c536-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="4c536-110">Nella finestra **Pianifica ordine vendita** scegliere l'azione **Crea ordine produzione**.</span><span class="sxs-lookup"><span data-stu-id="4c536-110">In the **Sales Order Planning** window, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="4c536-111">Nella finestra **Crea Ordine da Vendite** selezionare l'opzione **Ordine progetto** nel campo **Tipo ordine**.</span><span class="sxs-lookup"><span data-stu-id="4c536-111">In the **Create Order from Sales** window, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="4c536-112">Scegliere il pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="4c536-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="4c536-113">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di produzione**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="4c536-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="4c536-114">Aprire l'ordine di produzione appena creato.</span><span class="sxs-lookup"><span data-stu-id="4c536-114">Open the production order just created.</span></span>  

    <span data-ttu-id="4c536-115">Si noti che il campo **Tipo Origine** dell'ordine di produzione include le **Testate Vendita** e nell'ordine sono disponibili più righe, una per ogni articolo di riga di vendita da produrre.</span><span class="sxs-lookup"><span data-stu-id="4c536-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="4c536-116">Scegliere l'azione **Pianifica**.</span><span class="sxs-lookup"><span data-stu-id="4c536-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="4c536-117">Nella finestra **Pianificazione ordini**, scegliere l'azione **Aggiorna** per calcolare la nuova domanda.</span><span class="sxs-lookup"><span data-stu-id="4c536-117">In the **Order Planning** window, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="4c536-118">La riga di testata ordine per l'ordine progetto verrà visualizzata e tutte le righe di domanda non soddisfatta verranno espanse sotto tale riga.</span><span class="sxs-lookup"><span data-stu-id="4c536-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="4c536-119">Benché l'ordine di produzione includa righe per svariati articoli prodotti, la domanda totale per tutte le righe di ordine di produzione viene elencata sotto una riga di testata ordine nella finestra **Pianificazione ordini** e viene visualizzata la ragione sociale originale del cliente.</span><span class="sxs-lookup"><span data-stu-id="4c536-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line in the **Order Planning** window, and the original customer name is displayed.</span></span> <span data-ttu-id="4c536-120">È ora possibile passare alla pianificazione della domanda, come illustrato in [Pianificare una nuova domanda ordine per ordine](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="4c536-120">You can now proceed to plan for the demand as described in [Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4c536-121">Le righe domanda nell'ordine di produzione progetto che hanno **Ord. prod.** nel campo **Sistema di rifornimento** rappresentano gli ordini di produzione sottostanti.</span><span class="sxs-lookup"><span data-stu-id="4c536-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="4c536-122">Dopo aver generato tali ordini di produzione, occorre ricalcolare il piano nella finestra **Pianificazione ordini** per identificare la domanda di componenti non soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="4c536-122">After you have generated these production orders, you must again calculate a plan in the **Order Planning** window to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="4c536-123">In questo caso, vengono visualizzati come righe domanda in una normale riga di testata dell'ordine di produzione, cioè la relazione di progetto non è più visibile nella finestra.</span><span class="sxs-lookup"><span data-stu-id="4c536-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible in the window.</span></span> <span data-ttu-id="4c536-124">Tuttavia, se si utilizza la funzionalità Tracciabilità ordine, è possibile esaminare tutti gli ordini di approvvigionamento creati nell'ordine di vendita originale.</span><span class="sxs-lookup"><span data-stu-id="4c536-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c536-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c536-125">See Also</span></span>
<span data-ttu-id="4c536-126">[Pianif.](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4c536-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="4c536-127">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="4c536-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4c536-128">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4c536-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4c536-129">Magazzino</span><span class="sxs-lookup"><span data-stu-id="4c536-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4c536-130">Acquisti</span><span class="sxs-lookup"><span data-stu-id="4c536-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4c536-131">[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4c536-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="4c536-132">Impostare le procedure ottimali: Pianificazione forniture</span><span class="sxs-lookup"><span data-stu-id="4c536-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="4c536-133">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c536-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

