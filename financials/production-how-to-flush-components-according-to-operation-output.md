---
title: Come eseguire la consuntivazione dei componenti in base all'output dell'operazione | Microsoft Docs
description: Per gli articoli impostati con il metodo di consuntivazione a ritroso, il comportamento di default prevede di calcolare e registrare il consumo di componenti quando si modifica lo stato di un ordine di produzione rilasciato in **Completato**. Per ulteriori informazioni, vedere Metodo consuntivazione.
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
ms.openlocfilehash: b58e897768848b50232b360f3822846d6dd316df
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-flush-components-according-to-operation-output"></a><span data-ttu-id="6d482-104">Procedura: Eseguire la consuntivazione dei componenti in base all'output dell'operazione</span><span class="sxs-lookup"><span data-stu-id="6d482-104">How to: Flush Components According to Operation Output</span></span>
<span data-ttu-id="6d482-105">Per gli articoli impostati con il metodo di consuntivazione a ritroso, il comportamento di default prevede di calcolare e registrare il consumo di componenti quando si modifica lo stato di un ordine di produzione rilasciato in **Completato**.</span><span class="sxs-lookup"><span data-stu-id="6d482-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="6d482-106">Se inoltre si definiscono i codici legame tra ciclo e distinta base, il calcolo e la registrazione si verificano una volta completata ogni operazione e la quantità effettivamente consumata nell'operazione viene registrata.</span><span class="sxs-lookup"><span data-stu-id="6d482-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="6d482-107">Per ulteriori informazioni, vedere [Procedura: Creare cicli](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="6d482-107">For more information, see [How to: Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="6d482-108">Ad esempio, se un ordine di produzione per produrre 800 metri richiede 8 chilogrammi di un componente, quando si registrano 200 metri come output, 2 chilogrammi vengono automaticamente registrati come consumo.</span><span class="sxs-lookup"><span data-stu-id="6d482-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="6d482-109">Questa funzionalità si rivela particolarmente utile per i seguenti motivi:</span><span class="sxs-lookup"><span data-stu-id="6d482-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="6d482-110">**Valutazione di magazzino** - i movimenti di valorizzazione per output e consumo vengono creati in parallelo con lo stato di avanzamento dell'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="6d482-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="6d482-111">Senza codice legame tra ciclo e distinta base, il valore di magazzino aumenterà man mano che l'output viene registrato e diminuirà in un momento successivo quando il valore di consumo di componenti viene registrato insieme all'ordine di produzione chiuso.</span><span class="sxs-lookup"><span data-stu-id="6d482-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="6d482-112">**Disponibilità di magazzino** - con la registrazione graduale del consumo, la disponibilità degli articoli componenti è più aggiornata, il che è importante per mantenere l'equilibrio interno tra offerta e domanda.</span><span class="sxs-lookup"><span data-stu-id="6d482-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="6d482-113">Senza codice legame tra ciclo e distinta base, altre domande del componente potrebbero ritenere che sia disponibile finché è in sospeso una registrazione di consumo in ritardo.</span><span class="sxs-lookup"><span data-stu-id="6d482-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="6d482-114">**JIT (just-in-time)** – grazie alla possibilità di personalizzare i prodotti alle richieste del cliente, è possibile ridurre lo spreco assicurandosi che le modifiche di sistema e di lavoro si verifichino solo quando è necessario.</span><span class="sxs-lookup"><span data-stu-id="6d482-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="6d482-115">La procedura che segue mostra come combinare la consuntivazione a ritroso e i codici di legame tra ciclo e distinta base in modo che la quantità di cui è stata effettuata la consuntivazione per operazione sia proporzionale all'effettivo output dell'operazione completata.</span><span class="sxs-lookup"><span data-stu-id="6d482-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="6d482-116">Per eseguire la consuntivazione dei componenti in base all'output dell'operazione</span><span class="sxs-lookup"><span data-stu-id="6d482-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="6d482-117">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6d482-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6d482-118">Scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="6d482-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="6d482-119">Nella Scheda dettaglio **Rifornimento**, nel campo **Metodo consuntivazione**, selezionare **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="6d482-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6d482-120">Selezionare **Prelievo+ Avanti** se il componente è utilizzato in un'ubicazione impostata per l'utilizzo di stoccaggi e prelievi guidati.</span><span class="sxs-lookup"><span data-stu-id="6d482-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="6d482-121">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cicli**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6d482-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="6d482-122">Definire codici di legame tra ciclo e distinta base per ogni operazione che consuma il componente.</span><span class="sxs-lookup"><span data-stu-id="6d482-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="6d482-123">Per ulteriori informazioni, vedere [Procedura: Creare cicli](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="6d482-123">For more information, see [How to: Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="6d482-124">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **DB produzione**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6d482-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="6d482-125">Definire codici di legame tra ciclo e distinta base da ogni istanza del componente all'operazione in cui viene consumato.</span><span class="sxs-lookup"><span data-stu-id="6d482-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="6d482-126">Il componente deve avere un collegamento ciclo all'ultima operazione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="6d482-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6d482-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d482-127">See Also</span></span>  
[<span data-ttu-id="6d482-128">Procedura: Creare distinte base di produzione</span><span class="sxs-lookup"><span data-stu-id="6d482-128">How to: Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="6d482-129">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="6d482-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="6d482-130">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6d482-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="6d482-131">[Pianif.](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="6d482-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="6d482-132">Magazzino</span><span class="sxs-lookup"><span data-stu-id="6d482-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6d482-133">Acquisti</span><span class="sxs-lookup"><span data-stu-id="6d482-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6d482-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d482-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

