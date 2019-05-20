---
title: Organizzare gli articoli in categorie| Documenti Microsoft
description: Per semplificare la ricerca e trovare gli articoli, è possibile assegnare gli attributi degli articoli e organizzare gli articoli in categorie.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: dd5ca3a3e109f565448d0c5698a6e1ee6dce331c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240136"
---
# <a name="categorize-items"></a><span data-ttu-id="8c862-103">Classificare gli articoli</span><span class="sxs-lookup"><span data-stu-id="8c862-103">Categorize Items</span></span>
<span data-ttu-id="8c862-104">Per visualizzare una panoramica degli articoli e semplificare l'ordinamento e la ricerca degli articoli, risulta utile organizzare gli articoli in categorie.</span><span class="sxs-lookup"><span data-stu-id="8c862-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="8c862-105">Per trovare gli articoli in base alle caratteristiche, è possibile assegnare gli attributi ad articoli e a categorie articolo.</span><span class="sxs-lookup"><span data-stu-id="8c862-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="8c862-106">Per ulteriori informazioni, vedere [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="8c862-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="8c862-107">Per creare una categoria articolo</span><span class="sxs-lookup"><span data-stu-id="8c862-107">To create an item category</span></span>
1. <span data-ttu-id="8c862-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Categorie articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8c862-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="8c862-109">Nella pagina **Categorie articoli** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="8c862-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="8c862-110">Nella pagina **Scheda categoria articolo**, nella Scheda dettaglio **Generale**, compilare i campi in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="8c862-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="8c862-111">Nella Scheda dettaglio **Attributi**, specificare tutti gli attributi per la categoria articolo.</span><span class="sxs-lookup"><span data-stu-id="8c862-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="8c862-112">Per ulteriori informazioni, vedere [Per assegnare attributi articolo alle categorie articoli](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="8c862-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
>   <span data-ttu-id="8c862-113">Se la categoria articolo è una categoria padre, come indicato dal campo **Categoria padre**, gli attributi articoli assegnati a tale categoria padre sono precompilati nella Scheda dettaglio **Attributi**.</span><span class="sxs-lookup"><span data-stu-id="8c862-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8c862-114">Gli attributi degli articoli assegnati a una categoria articolo vengono applicati automaticamente all'articolo a cui la categoria articolo è assegnata.</span><span class="sxs-lookup"><span data-stu-id="8c862-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="8c862-115">Per assegnare una categoria articolo a un articolo</span><span class="sxs-lookup"><span data-stu-id="8c862-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="8c862-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8c862-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="8c862-117">Aprire la scheda per l'articolo a cui si desidera assegnare una categoria articolo.</span><span class="sxs-lookup"><span data-stu-id="8c862-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="8c862-118">Nel campo **Codice categoria articolo** scegliere il pulsante di ricerca e selezionare una categoria articolo esistente.</span><span class="sxs-lookup"><span data-stu-id="8c862-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="8c862-119">In alternativa, scegliere l'azione **Nuovo** per creare prima una nuova categoria articolo come descritto in [Per creare una categoria articolo](inventory-how-categorize-items.md#to-create-an-item-category).</span><span class="sxs-lookup"><span data-stu-id="8c862-119">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c862-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c862-120">See Also</span></span>
[<span data-ttu-id="8c862-121">Utilizzare gli attributi degli articoli</span><span class="sxs-lookup"><span data-stu-id="8c862-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="8c862-122">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="8c862-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="8c862-123">Magazzino</span><span class="sxs-lookup"><span data-stu-id="8c862-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="8c862-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c862-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
