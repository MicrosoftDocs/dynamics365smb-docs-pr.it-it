---
title: 'Procedura: Pianificare movimentazioni warehouse nei prospetti | Documenti Microsoft'
description: Pianificare i movimenti nel prospetto utilizzando la funzione di rifornimento collocazione o manualmente pianificando le righe che si desidera creare come istruzioni di movimento.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 397b7d3de0355ce6be1be6607e5cfc7f61b5f55d
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="60a7d-103">Pianificare movimentazioni warehouse nei prospetti</span><span class="sxs-lookup"><span data-stu-id="60a7d-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="60a7d-104">Pianificare i movimenti nel prospetto utilizzando la funzione di rifornimento collocazione o manualmente pianificando le righe che si desidera creare come istruzioni di movimento.</span><span class="sxs-lookup"><span data-stu-id="60a7d-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="60a7d-105">Per calcolare un movimento di rifornimento</span><span class="sxs-lookup"><span data-stu-id="60a7d-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="60a7d-106">Man mano che gli articoli nella warehouse vengono spediti ai clienti, le collocazioni con le valutazioni più elevate contengono un numero di articoli sempre minore.</span><span class="sxs-lookup"><span data-stu-id="60a7d-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="60a7d-107">Per reintegrare le collocazioni di prelievo a valutazione elevata mediante gli articoli disponibili in altre collocazioni, è possibile eseguire la funzione **Calcola rifornimento collocazione** nella finestra **Prospetto movimentazioni**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function in the **Movement Worksheet** window</span></span>

1.  <span data-ttu-id="60a7d-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Movimento worksheet**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="60a7d-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="60a7d-109">Sceliere l'azione **Calcola rifornimento collocazione**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="60a7d-110"> crea alcune righe con indicazioni precise in merito allo spostamento di articoli dalle collocazioni con valutazione inferiore alle collocazioni con valutazione più elevata.</span><span class="sxs-lookup"><span data-stu-id="60a7d-110"> creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60a7d-111">Una movimentazione viene suggerita in base al metodo FEFO quando si attiva la funzione **Crea movimento** se vengono soddisfatte le seguenti condizioni per un articolo:</span><span class="sxs-lookup"><span data-stu-id="60a7d-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="60a7d-112">L'articolo ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="60a7d-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="60a7d-113">La casella di controllo **Prelievo in base a FEFO** della scheda ubicazione viene selezionata.</span><span class="sxs-lookup"><span data-stu-id="60a7d-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60a7d-114">Nella scheda Ubicazione viene selezionata la casella di controllo **Collocazione obbligatoria**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60a7d-115">I campi **Dal codice zona** e **Dal codice collocazione** sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="60a7d-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="60a7d-116">Per ulteriori informazioni, vedere [Prelievo in base al metodo FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="60a7d-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="60a7d-117">Esaminare le righe e, se necessario, modificarle oppure eliminarne alcune nel caso in cui non sia possibile eseguire tutte le indicazioni riportate poiché richiedono troppo tempo.</span><span class="sxs-lookup"><span data-stu-id="60a7d-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="60a7d-118">Scegliere l'azione **Crea movimento** per creare un'istruzione warehouse destinata agli impiegati warehouse.</span><span class="sxs-lookup"><span data-stu-id="60a7d-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="60a7d-119">Per spostare l'intero contenuto di una o più collocazioni tramite la funzione Prendi contenuto collocazione</span><span class="sxs-lookup"><span data-stu-id="60a7d-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="60a7d-120">Il prospetto movimentazioni consente anche di pianificare altri movimenti delle giacenze all'interno della warehouse.</span><span class="sxs-lookup"><span data-stu-id="60a7d-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="60a7d-121">Ad esempio, quando si desidera posizionare gli articoli in una collocazione per il controllo qualità, è possibile pianificare questa azione utilizzando il prospetto movimenti, quindi creare un movimento per ottenere le istruzioni da fornire a un impiegato della warehouse.</span><span class="sxs-lookup"><span data-stu-id="60a7d-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="60a7d-122">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Movimento worksheet**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="60a7d-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="60a7d-123">Scegliere l'azione **Ottieni contenuto collocazione**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="60a7d-124">Utilizzare la finestra di richiesta per applicare un filtro in modo da determinare le collocazioni e gli articoli da visualizzare nelle righe del prospetto movimentazioni.</span><span class="sxs-lookup"><span data-stu-id="60a7d-124">Use the request window to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="60a7d-125">Compilare i campi pertinenti nella finestra di richiesta del processo batch.</span><span class="sxs-lookup"><span data-stu-id="60a7d-125">Fill in the relevant fields in the batch job request window.</span></span> <span data-ttu-id="60a7d-126">Se, ad esempio, si desidera visualizzare il contenuto di tutte le collocazioni di una determinata zona dell'ubicazione, compilare il campo **Cod. zona**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="60a7d-127">Se si desidera recuperare le righe per ogni collocazione contenente un articolo specifico, compilare il campo **Nr. articolo**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60a7d-128">Non è possibile spostare manualmente gli articoli all'interno o all'esterno di una collocazione di tipo Ricevi poiché gli articoli presenti in questo tipo di collocazione devono essere registrati come stoccati prima di essere inseriti nella giacenza disponibile.</span><span class="sxs-lookup"><span data-stu-id="60a7d-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="60a7d-129">Se si desidera recuperare un numero elevato di righe, scegliere **Ordina** per selezionare un metodo di ordinamento per le righe visualizzate nel prospetto, quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60a7d-130">Le righe movimento vengono richiamate in base al metodo FEFO quando si attiva la funzione **Ottieni contenuto collocazione** se vengono soddisfatte le seguenti condizioni per un articolo:</span><span class="sxs-lookup"><span data-stu-id="60a7d-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="60a7d-131">L'articolo ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="60a7d-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="60a7d-132">La casella di controllo **Prelievo in base a FEFO** della scheda ubicazione viene selezionata.</span><span class="sxs-lookup"><span data-stu-id="60a7d-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60a7d-133">Nella scheda Ubicazione viene selezionata la casella di controllo **Collocazione obbligatoria**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60a7d-134">I campi **Dal codice zona** e **Dal codice collocazione** sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="60a7d-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="60a7d-135">Completare alcune delle righe recuperate per riflettere le modifiche che si desidera apportare.</span><span class="sxs-lookup"><span data-stu-id="60a7d-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="60a7d-136">Per ogni articolo da spostare, è necessario compilare i campi **Nr. articolo**, **Dal codice collocazione**, **A codice collocazione** e **Quantità**.</span><span class="sxs-lookup"><span data-stu-id="60a7d-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="60a7d-137">Eliminare le righe incomplete utilizzate a scopo informativo.</span><span class="sxs-lookup"><span data-stu-id="60a7d-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="60a7d-138">Quando le righe del prospetto movimenti rifletteranno accuratamente il modo in cui si desidera venga eseguita l'azione, scegliere l'azione **Crea movimento** per creare le istruzioni destinate all'impiegato della warehouse.</span><span class="sxs-lookup"><span data-stu-id="60a7d-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="60a7d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60a7d-139">See Also</span></span>  
[<span data-ttu-id="60a7d-140">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="60a7d-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="60a7d-141">Magazzino</span><span class="sxs-lookup"><span data-stu-id="60a7d-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="60a7d-142">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="60a7d-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="60a7d-143">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="60a7d-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="60a7d-144">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="60a7d-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="60a7d-145">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="60a7d-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

