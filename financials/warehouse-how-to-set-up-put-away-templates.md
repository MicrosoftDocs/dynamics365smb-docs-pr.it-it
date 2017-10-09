---
title: 'Procedura: Impostare i modelli di stoccaggio | Documenti Microsoft'
description: "Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5a81b904a9180d7370a00f94a129ec707398e89a
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-put-away-templates"></a><span data-ttu-id="42cc3-103">Procedura: Impostare i modelli di stoccaggio</span><span class="sxs-lookup"><span data-stu-id="42cc3-103">How to: Set Up Put-away Templates</span></span>
<span data-ttu-id="42cc3-104">Grazie alla funzionalità per stoccaggi e prelievi guidati, viene suggerita in qualsiasi momento la collocazione più appropriata per gli articoli sulla base del modello di stoccaggio impostato per la warehouse, le valutazioni assegnate alle collocazioni e le quantità minima e massima impostate per le collocazioni fisse.</span><span class="sxs-lookup"><span data-stu-id="42cc3-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="42cc3-105">È possibile impostare più modelli di stoccaggio e selezionarne uno per gestire gli stoccaggi nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="42cc3-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="42cc3-106">È inoltre possibile selezionare un modello di stoccaggio per qualsiasi articolo o unità di stockkeeping che presenta speciali requisiti di stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="42cc3-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="42cc3-107">Per impostare i modelli di stoccaggio</span><span class="sxs-lookup"><span data-stu-id="42cc3-107">To set up put-away templates</span></span>  
1.  <span data-ttu-id="42cc3-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Modelli stoccaggio**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="42cc3-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="42cc3-109">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="42cc3-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="42cc3-110">Specificare un codice che costituisce l'identificatore unico del modello da creare.</span><span class="sxs-lookup"><span data-stu-id="42cc3-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4.  <span data-ttu-id="42cc3-111">Se lo si desidera, immettere una breve descrizione.</span><span class="sxs-lookup"><span data-stu-id="42cc3-111">Enter a short description, if you wish.</span></span>  
5.  <span data-ttu-id="42cc3-112">Compilare la prima riga specificando i requisiti prioritari relativi alle collocazioni che dovranno essere soddisfatti nei suggerimenti per uno stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="42cc3-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>  
6.  <span data-ttu-id="42cc3-113">Compilare la seconda riga specificando i requisiti relativi alle collocazioni che dovranno essere soddisfatti in seconda istanza durante la ricerca di una collocazione per lo stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="42cc3-113">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="42cc3-114">La seconda riga viene utilizzata solo se non è possibile trovare una collocazione che soddisfi i requisiti specificati nella prima riga.</span><span class="sxs-lookup"><span data-stu-id="42cc3-114">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7.  <span data-ttu-id="42cc3-115">Compilare le righe successive fino a completa definizione di tutte le collocazioni accettabili che si desidera vengano utilizzate nel processo di stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="42cc3-115">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8.  <span data-ttu-id="42cc3-116">Nell'ultima riga del modello di stoccaggio selezionare la casella di controllo **Trova collocazione variabile**.</span><span class="sxs-lookup"><span data-stu-id="42cc3-116">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="42cc3-117">È possibile creare diversi modelli di stoccaggio e applicarli in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="42cc3-117">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="42cc3-118">Viene utilizzato innanzitutto il modello di stoccaggio selezionato per l'articolo o l'unità di stockkeeping, qualora disponibile.</span><span class="sxs-lookup"><span data-stu-id="42cc3-118">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="42cc3-119">Se questi campi non vengono compilati, verrà utilizzato il modello di stoccaggio selezionato per la warehouse nella Scheda dettaglio **Criteri per collocazione** della scheda ubicazione.</span><span class="sxs-lookup"><span data-stu-id="42cc3-119">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="42cc3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42cc3-120">See Also</span></span>  
[<span data-ttu-id="42cc3-121">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="42cc3-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="42cc3-122">Magazzino</span><span class="sxs-lookup"><span data-stu-id="42cc3-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="42cc3-123">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="42cc3-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="42cc3-124">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="42cc3-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="42cc3-125">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="42cc3-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="42cc3-126">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="42cc3-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

