---
title: 'Procedura: Impostare i modelli di stoccaggio | Documenti Microsoft'
description: Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: edupont
ms.openlocfilehash: 8e6f248768f558f3bc5e12002234ffb56b006759
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780012"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="7e15f-103">Impostare i modelli di stoccaggio</span><span class="sxs-lookup"><span data-stu-id="7e15f-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="7e15f-104">Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse.</span><span class="sxs-lookup"><span data-stu-id="7e15f-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="7e15f-105">È possibile impostare più modelli di stoccaggio e selezionarne uno per gestire gli stoccaggi nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="7e15f-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="7e15f-106">È inoltre possibile selezionare un modello di stoccaggio per qualsiasi articolo o unità di stockkeeping che presenta speciali requisiti di stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="7e15f-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="7e15f-107">Per impostare i modelli di stoccaggio</span><span class="sxs-lookup"><span data-stu-id="7e15f-107">To set up put-away templates</span></span>

1. <span data-ttu-id="7e15f-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modelli stoccaggio** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="7e15f-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7e15f-109">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="7e15f-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="7e15f-110">Specificare un codice che costituisce l'identificatore unico del modello da creare.</span><span class="sxs-lookup"><span data-stu-id="7e15f-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="7e15f-111">Se lo si desidera, immettere una breve descrizione.</span><span class="sxs-lookup"><span data-stu-id="7e15f-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="7e15f-112">Compilare la prima riga specificando i requisiti prioritari relativi alle collocazioni che dovranno essere soddisfatti nei suggerimenti per uno stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="7e15f-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="7e15f-113">Ad esempio, se si desidera che il metodo di stoccaggio predefinito sia basato su collocazioni fisse scegliere il campo **Trova collocazione fissa**.</span><span class="sxs-lookup"><span data-stu-id="7e15f-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="7e15f-114">Compilare la seconda riga specificando i requisiti relativi alle collocazioni che dovranno essere soddisfatti in seconda istanza durante la ricerca di una collocazione per lo stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="7e15f-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="7e15f-115">La seconda riga viene utilizzata solo se non è possibile trovare una collocazione che soddisfi i requisiti specificati nella prima riga.</span><span class="sxs-lookup"><span data-stu-id="7e15f-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="7e15f-116">Compilare le righe successive fino a completa definizione di tutte le collocazioni accettabili che si desidera vengano utilizzate nel processo di stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="7e15f-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="7e15f-117">Nell'ultima riga del modello di stoccaggio selezionare la casella di controllo **Trova collocazione variabile**.</span><span class="sxs-lookup"><span data-stu-id="7e15f-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="7e15f-118">È possibile creare diversi modelli di stoccaggio e applicarli in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="7e15f-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="7e15f-119">Viene utilizzato innanzitutto il modello di stoccaggio selezionato per l'articolo o l'unità di stockkeeping, qualora disponibile.</span><span class="sxs-lookup"><span data-stu-id="7e15f-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="7e15f-120">Se questi campi non vengono compilati, verrà utilizzato il modello di stoccaggio selezionato per la warehouse nella Scheda dettaglio **Criteri per collocazione** della scheda ubicazione.</span><span class="sxs-lookup"><span data-stu-id="7e15f-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e15f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e15f-121">See Also</span></span>

[<span data-ttu-id="7e15f-122">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="7e15f-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="7e15f-123">Magazzino</span><span class="sxs-lookup"><span data-stu-id="7e15f-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7e15f-124">Impostazione gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="7e15f-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="7e15f-125">Gestione assemblaggio</span><span class="sxs-lookup"><span data-stu-id="7e15f-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="7e15f-126">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="7e15f-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="7e15f-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e15f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
