---
title: 'Procedura: Utilizzare le distinte base per gestire i componenti | Documenti Microsoft'
description: "Si può creare una distinta base di assemblaggio per specificare i componenti o le risorse richieste per un l'articolo che la distinta base assemblaggio rappresenta ed è possibile visualizzare i componenti di un articolo di assemblaggio."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="57908-103">Procedura: Utilizzare le distinte base</span><span class="sxs-lookup"><span data-stu-id="57908-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="57908-104">La versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene solo la prima parte della funzionalità di gestione assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="57908-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="57908-105">Per ora, è possibile creare solo le DB di assemblaggio e quindi gestire gli articoli padre correlati come articoli di inventario normali.</span><span class="sxs-lookup"><span data-stu-id="57908-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="57908-106">In un aggiornamento futuro, è possibile gestire l'assemblaggio effettivo di articoli dai componenti, sia in flussi di assemblaggio per magazzino che di assemblaggio su ordine, quindi vendere i componenti come kit.</span><span class="sxs-lookup"><span data-stu-id="57908-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="57908-107">Utilizzare le distinte base (DB) per strutturare gli articoli padre da vendere come kit costituiti da componenti del padre o da assemblare su ordine o per magazzino.</span><span class="sxs-lookup"><span data-stu-id="57908-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="57908-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], una distinta base è detta "DB assemblaggio".</span><span class="sxs-lookup"><span data-stu-id="57908-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="57908-109">La DB assemblaggio specifica i componenti contenuti in articoli padre.</span><span class="sxs-lookup"><span data-stu-id="57908-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="57908-110">In questa documentazione, un articolo padre è detto "articolo di assemblaggio".</span><span class="sxs-lookup"><span data-stu-id="57908-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="57908-111">Le DB assemblaggio in genere contengono articoli ma possono anche contenere una o più risorse richieste per l'assemblaggio dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="57908-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="57908-112">Le DB assemblaggio possono essere multilivello, cioè un componente della DB assemblaggio può essere un articolo di assemblaggio esso stesso.</span><span class="sxs-lookup"><span data-stu-id="57908-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="57908-113">In tal caso, il campo **DB assemblaggio** nella riga della DB assemblaggio contiene il valore **Sì**.</span><span class="sxs-lookup"><span data-stu-id="57908-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="57908-114">Requisiti speciali si applicano agli articoli nelle DB assemblaggio correlati alla disponibilità.</span><span class="sxs-lookup"><span data-stu-id="57908-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="57908-115">Per ulteriori informazioni, vedere la sezione "Per visualizzare la disponibilità di un articolo per l'utilizzo in DB di assemblaggio" in [Procedura: Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="57908-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="57908-116">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="57908-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="57908-117">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di Financials](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="57908-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="57908-118">Per creare una DB assemblaggio</span><span class="sxs-lookup"><span data-stu-id="57908-118">To create an assembly BOM</span></span>
<span data-ttu-id="57908-119">Per definire un articolo padre composto da altri articoli e potenzialmente da risorse richieste per l'assemblaggio, è necessario creare una DB assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="57908-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="57908-120">Esistono due passaggi per creare una DB assemblaggio:</span><span class="sxs-lookup"><span data-stu-id="57908-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="57908-121">Impostazione di un nuovo articolo</span><span class="sxs-lookup"><span data-stu-id="57908-121">Setting up a new item</span></span>
- <span data-ttu-id="57908-122">Definizione della struttura della distinta base dell'articolo di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="57908-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="57908-123">Impostare un nuovo articolo.</span><span class="sxs-lookup"><span data-stu-id="57908-123">Set up a new item.</span></span> <span data-ttu-id="57908-124">Per ulteriori informazioni, vedere [Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="57908-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="57908-125">Continuare a inserire componenti o risorse nella distinta base assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="57908-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="57908-126">Nella finestra **Scheda articolo** per un articolo di assemblaggio, scegliere l'azione **Assembla** quindi l'azione **DB assemblaggio**.</span><span class="sxs-lookup"><span data-stu-id="57908-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="57908-127">Nella finestra **DB assemblaggio** compilare i campi secondo le proprie necessità.</span><span class="sxs-lookup"><span data-stu-id="57908-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="57908-128">Per visualizzare i componenti di un articolo di assemblaggio con indentazione in base alla struttura DB</span><span class="sxs-lookup"><span data-stu-id="57908-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="57908-129">Nella finestra **DB assemblaggio**, è possibile aprire una finestra distinta in cui vengono visualizzati i componenti e tutte le risorse indentate in base alla posizione nella distinta base dell'articolo di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="57908-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="57908-130">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="57908-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="57908-131">Aprire la finestra della scheda per l'articolo di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="57908-131">Open the card for an assembly item.</span></span> <span data-ttu-id="57908-132">(Il campo **DB assemblaggio** nella finestra **Articoli** contiene il valore **Sì**.)</span><span class="sxs-lookup"><span data-stu-id="57908-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="57908-133">Nella finestra **Scheda articolo** scegliere l'azione **Assembla** quindi l'azione **DB assemblaggio**.</span><span class="sxs-lookup"><span data-stu-id="57908-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="57908-134">Nella finestra **DB assemblaggio** selezionare l'azione **Mostra DB**.</span><span class="sxs-lookup"><span data-stu-id="57908-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="57908-135">Per acquistare, vendere o trasferire gli articoli di assemblaggio</span><span class="sxs-lookup"><span data-stu-id="57908-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="57908-136">Poiché la versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene solo la funzionalità per definire e assegnare le DB di assemblaggio agli articoli, è possibile gestire gli articoli di assemblaggio nelle righe dei documenti solo come articoli normali.</span><span class="sxs-lookup"><span data-stu-id="57908-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="57908-137">**Avvertenza**: la quantità di magazzino dei componenti della DB non verrà rettificata se si esegue questa operazione.</span><span class="sxs-lookup"><span data-stu-id="57908-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="57908-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57908-138">See Also</span></span>
[<span data-ttu-id="57908-139">Procedura: Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="57908-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="57908-140">[Procedura: Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="57908-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="57908-141">Magazzino</span><span class="sxs-lookup"><span data-stu-id="57908-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="57908-142">[Utilizzo di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57908-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

