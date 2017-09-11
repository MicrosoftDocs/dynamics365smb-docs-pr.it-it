---
title: Organizzare gli articoli in categorie| Documenti Microsoft
description: "Per semplificare la ricerca e trovare gli articoli, è possibile assegnare gli attributi degli articoli e organizzare gli articoli in categorie."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: da87c427033d58d92a6a5222bc323c68c4bc3f4e
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-categorize-items"></a><span data-ttu-id="0064f-103">Procedura: Classificare gli articoli</span><span class="sxs-lookup"><span data-stu-id="0064f-103">How to: Categorize Items</span></span>
<span data-ttu-id="0064f-104">Per visualizzare una panoramica degli articoli e semplificare l'ordinamento e la ricerca degli articoli, risulta utile organizzare gli articoli in categorie.</span><span class="sxs-lookup"><span data-stu-id="0064f-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="0064f-105">Per trovare gli articoli in base alle caratteristiche, è possibile assegnare gli attributi ad articoli e a categorie articolo.</span><span class="sxs-lookup"><span data-stu-id="0064f-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="0064f-106">Per ulteriori informazioni, vedere [Procedura: Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0064f-106">For more information, see [How to: Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="0064f-107">Per creare una categoria articolo</span><span class="sxs-lookup"><span data-stu-id="0064f-107">To create an item category</span></span>
1. <span data-ttu-id="0064f-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Categorie articoli**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0064f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="0064f-109">Nella finestra **Categorie articoli** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="0064f-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="0064f-110">Nella finestra **Scheda categoria articolo**, nella Scheda dettaglio **Generale**, compilare i campi in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="0064f-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="0064f-111">Nella Scheda dettaglio **Attributi**, specificare tutti gli attributi per la categoria articolo.</span><span class="sxs-lookup"><span data-stu-id="0064f-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="0064f-112">Per ulteriori informazioni, vedere la sezione "Per assegnare attributi a una categoria articolo" in [Procedura: Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0064f-112">For more information, see the "To assign item attributes to an item category" section in [How to: Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="0064f-113">Se la categoria articolo è una categoria padre, come indicato dal campo **Categoria padre**, gli attributi articoli assegnati a tale categoria padre sono precompilati nella Scheda dettaglio **Attributi**.</span><span class="sxs-lookup"><span data-stu-id="0064f-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0064f-114">Gli attributi degli articoli assegnati a una categoria articolo vengono applicati automaticamente all'articolo a cui la categoria articolo è assegnata.</span><span class="sxs-lookup"><span data-stu-id="0064f-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="0064f-115">Per assegnare una categoria articolo a un articolo</span><span class="sxs-lookup"><span data-stu-id="0064f-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="0064f-116">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0064f-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="0064f-117">Aprire la scheda per l'articolo a cui si desidera assegnare una categoria articolo.</span><span class="sxs-lookup"><span data-stu-id="0064f-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="0064f-118">Nel campo **Codice categoria articolo** scegliere il pulsante di ricerca e selezionare una categoria articolo esistente.</span><span class="sxs-lookup"><span data-stu-id="0064f-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="0064f-119">In alternativa, scegliere l'azione **Nuovo** per creare prima una nuova categoria articolo come descritto nella sezione "Per creare una categoria articolo".</span><span class="sxs-lookup"><span data-stu-id="0064f-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="0064f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0064f-120">See Also</span></span>
[<span data-ttu-id="0064f-121">Procedura: Utilizzare gli attributi degli articoli</span><span class="sxs-lookup"><span data-stu-id="0064f-121">How to: Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="0064f-122">Procedura: Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="0064f-122">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0064f-123">Magazzino</span><span class="sxs-lookup"><span data-stu-id="0064f-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0064f-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0064f-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

