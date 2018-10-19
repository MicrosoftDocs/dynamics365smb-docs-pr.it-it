---
title: Organizzare gli articoli in categorie| Documenti Microsoft
description: "Per semplificare la ricerca e trovare gli articoli, è possibile assegnare gli attributi degli articoli e organizzare gli articoli in categorie."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c62d26dc9dc444359c0d8b5a9354b29132857de1
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="categorize-items"></a><span data-ttu-id="b8ec3-103">Classificare gli articoli</span><span class="sxs-lookup"><span data-stu-id="b8ec3-103">Categorize Items</span></span>
<span data-ttu-id="b8ec3-104">Per visualizzare una panoramica degli articoli e semplificare l'ordinamento e la ricerca degli articoli, risulta utile organizzare gli articoli in categorie.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="b8ec3-105">Per trovare gli articoli in base alle caratteristiche, è possibile assegnare gli attributi ad articoli e a categorie articolo.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="b8ec3-106">Per ulteriori informazioni, vedere [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b8ec3-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="b8ec3-107">Per creare una categoria articolo</span><span class="sxs-lookup"><span data-stu-id="b8ec3-107">To create an item category</span></span>
1. <span data-ttu-id="b8ec3-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Categorie articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="b8ec3-109">Nella finestra **Categorie articoli** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="b8ec3-110">Nella finestra **Scheda categoria articolo**, nella Scheda dettaglio **Generale**, compilare i campi in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="b8ec3-111">Nella Scheda dettaglio **Attributi**, specificare tutti gli attributi per la categoria articolo.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="b8ec3-112">Per ulteriori informazioni, vedere la sezione "Per assegnare attributi a una categoria articolo" in [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b8ec3-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="b8ec3-113">Se la categoria articolo è una categoria padre, come indicato dal campo **Categoria padre**, gli attributi articoli assegnati a tale categoria padre sono precompilati nella Scheda dettaglio **Attributi**.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b8ec3-114">Gli attributi degli articoli assegnati a una categoria articolo vengono applicati automaticamente all'articolo a cui la categoria articolo è assegnata.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="b8ec3-115">Per assegnare una categoria articolo a un articolo</span><span class="sxs-lookup"><span data-stu-id="b8ec3-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="b8ec3-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b8ec3-117">Aprire la scheda per l'articolo a cui si desidera assegnare una categoria articolo.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="b8ec3-118">Nel campo **Codice categoria articolo** scegliere il pulsante di ricerca e selezionare una categoria articolo esistente.</span><span class="sxs-lookup"><span data-stu-id="b8ec3-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="b8ec3-119">In alternativa, scegliere l'azione **Nuovo** per creare prima una nuova categoria articolo come descritto nella sezione "Per creare una categoria articolo".</span><span class="sxs-lookup"><span data-stu-id="b8ec3-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8ec3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8ec3-120">See Also</span></span>
[<span data-ttu-id="b8ec3-121">Utilizzare gli attributi degli articoli</span><span class="sxs-lookup"><span data-stu-id="b8ec3-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="b8ec3-122">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="b8ec3-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="b8ec3-123">Magazzino</span><span class="sxs-lookup"><span data-stu-id="b8ec3-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b8ec3-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8ec3-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

