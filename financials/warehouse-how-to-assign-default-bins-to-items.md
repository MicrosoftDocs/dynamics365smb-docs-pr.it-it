---
title: Come assegnare collocazioni di default ad articoli | Microsoft Docs
description: "Quando si utilizzano le collocazioni di un'ubicazione, l'assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento. Quando si assegna una collocazione di default a un articolo, tale collocazione viene suggerita ogni volta che viene avviata una transazione per l'articolo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ae0d22fa5384edef167e5ba473977079c6473673
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-assign-default-bins-to-items"></a><span data-ttu-id="c7152-104">Procedura: Assegnare collocazioni di default ad articoli</span><span class="sxs-lookup"><span data-stu-id="c7152-104">How to: Assign Default Bins to Items</span></span>
<span data-ttu-id="c7152-105">Quando si utilizzano le collocazioni di un'ubicazione, l'assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento.</span><span class="sxs-lookup"><span data-stu-id="c7152-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="c7152-106">Quando si assegna una collocazione di default a un articolo, tale collocazione viene suggerita ogni volta che viene avviata una transazione per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="c7152-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="c7152-107">Le collocazioni di default vengono definite nella finestra **Contenuto Collocazione**.</span><span class="sxs-lookup"><span data-stu-id="c7152-107">Default bins are defined in the **Bin Content** window.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="c7152-108">Per assegnare una collocazione di default a un articolo</span><span class="sxs-lookup"><span data-stu-id="c7152-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="c7152-109">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Prospetto creaz. cont. colloc.**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c7152-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="c7152-110">Immettere le informazioni relative all'articolo e al codice collocazione per ogni collocazione da impostare come default per un articolo.</span><span class="sxs-lookup"><span data-stu-id="c7152-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="c7152-111">Assicurarsi selezionare il campo **Default**.</span><span class="sxs-lookup"><span data-stu-id="c7152-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="c7152-112">Scegliere l'azione **Crea contenuto collocazione**.</span><span class="sxs-lookup"><span data-stu-id="c7152-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="c7152-113">Le collocazioni di default vengono assegnate all'articolo.</span><span class="sxs-lookup"><span data-stu-id="c7152-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c7152-114">Quando si esegue lo stoccaggio di un articolo, se a quest'ultimo non è assegnata una collocazione di default, verrà assegnata quella di default come collocazione per lo stoccaggio dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="c7152-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="c7152-115">Per modificare la collocazione di default per un articolo</span><span class="sxs-lookup"><span data-stu-id="c7152-115">To change the default bin for an item</span></span>  
<span data-ttu-id="c7152-116">Potrebbe essere necessario modificare l'assegnazione della collocazione di default per un articolo o assegnare una collocazione di default a un nuovo articolo.</span><span class="sxs-lookup"><span data-stu-id="c7152-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="c7152-117">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Contenuto collocazioni**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c7152-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c7152-118">Selezionare il codice di ubicazione desiderato nel campo **Filtro ubicazione**.</span><span class="sxs-lookup"><span data-stu-id="c7152-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="c7152-119">Individuare il movimento del contenuto collocazione di default corrente per l'articolo e deselezionare la casella di controllo **Collocazione di default**.</span><span class="sxs-lookup"><span data-stu-id="c7152-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="c7152-120">Individuare la riga del contenuto della collocazione che si desidera utilizzare come nuova collocazione di default.</span><span class="sxs-lookup"><span data-stu-id="c7152-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="c7152-121">Selezionare la casella di controllo **Collocazione di default**.</span><span class="sxs-lookup"><span data-stu-id="c7152-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c7152-122">Quando si esegue lo stoccaggio di un articolo per la prima volta, se a quest'ultimo non è assegnata una collocazione di default, il sistema assegnerà la collocazione di stoccaggio dell'articolo come collocazione di default.</span><span class="sxs-lookup"><span data-stu-id="c7152-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c7152-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7152-123">See Also</span></span>  
[<span data-ttu-id="c7152-124">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="c7152-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c7152-125">Magazzino</span><span class="sxs-lookup"><span data-stu-id="c7152-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c7152-126">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="c7152-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="c7152-127">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c7152-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c7152-128">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="c7152-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c7152-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c7152-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

