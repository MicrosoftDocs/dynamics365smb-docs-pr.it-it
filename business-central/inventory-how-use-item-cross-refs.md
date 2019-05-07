---
title: Utilizzare cross reference articolo | Microsoft Docs
description: "Se si imposta un cross-reference tra la descrizione articolo utilizzata per un articolo e la descrizione che il fornitore dell'articolo utilizza, la descrizione articolo del fornitore viene inserita automaticamente nei documenti di acquisto per il fornitore quando si compila il campo **Nr. cross-reference**  "
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "927104"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="c9d68-104">Utilizzare Cross reference articolo</span><span class="sxs-lookup"><span data-stu-id="c9d68-104">Use Item Cross References</span></span>
<span data-ttu-id="c9d68-105">Se si imposta un cross-reference tra la descrizione articolo utilizzata per un articolo e la descrizione che il fornitore dell'articolo utilizza, la descrizione articolo del fornitore viene inserita automaticamente nei documenti di acquisto per il fornitore quando si compila il campo **Nr. cross-reference**</span><span class="sxs-lookup"><span data-stu-id="c9d68-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="c9d68-106"> </span><span class="sxs-lookup"><span data-stu-id="c9d68-106">field.</span></span> <span data-ttu-id="c9d68-107">La stessa funzionalità è valida per i numeri di articolo cliente nei documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="c9d68-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="c9d68-108">Di seguito viene descritto come utilizzare i cross reference articolo per gli acquisti.</span><span class="sxs-lookup"><span data-stu-id="c9d68-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="c9d68-109">I passaggi sono simili per gli acquisti.</span><span class="sxs-lookup"><span data-stu-id="c9d68-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="c9d68-110">Per impostare un cross reference articolo per una descrizione articolo di un fornitore</span><span class="sxs-lookup"><span data-stu-id="c9d68-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="c9d68-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c9d68-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9d68-112">Aprire la scheda di un articolo per il quale si desidera creare un cross reference per la descrizione articolo che il fornitore utilizza per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="c9d68-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="c9d68-113">Scegliere l'azione **Cross reference**.</span><span class="sxs-lookup"><span data-stu-id="c9d68-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="c9d68-114">In una nuova riga nella pagina **Cross reference per l'articolo**, compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="c9d68-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="c9d68-115">.</span><span class="sxs-lookup"><span data-stu-id="c9d68-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="c9d68-116">Per immettere la descrizione articolo di un fornitore in un ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="c9d68-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="c9d68-117">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c9d68-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9d68-118">Creare un ordine di acquisto per il fornitore per il quale si è impostato un cross-reference articolo nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="c9d68-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="c9d68-119">Creare una riga acquisto per l'articolo per il quale si è impostato un cross reference articolo nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="c9d68-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="c9d68-120">Nel campo **Nr. cross-reference**</span><span class="sxs-lookup"><span data-stu-id="c9d68-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="c9d68-121">selezionare il cross-reference articolo creato quindi scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9d68-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="c9d68-122">Il campo **Descrizione** della riga viene sovrascritto con la descrizione articolo del fornitore, come definito nel movimento cross-reference articolo.</span><span class="sxs-lookup"><span data-stu-id="c9d68-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9d68-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9d68-123">See Also</span></span>
[<span data-ttu-id="c9d68-124">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="c9d68-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c9d68-125">Magazzino</span><span class="sxs-lookup"><span data-stu-id="c9d68-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c9d68-126">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9d68-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
