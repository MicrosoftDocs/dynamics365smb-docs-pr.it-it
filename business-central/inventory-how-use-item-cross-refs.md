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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8f7c409759716e741edfe1a352ff81da9fdea0db
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309654"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="0a1ab-104">Utilizzare Cross reference articolo</span><span class="sxs-lookup"><span data-stu-id="0a1ab-104">Use Item Cross References</span></span>
<span data-ttu-id="0a1ab-105">Se si imposta un cross-reference tra la descrizione articolo utilizzata per un articolo e la descrizione che il fornitore dell'articolo utilizza, la descrizione articolo del fornitore viene inserita automaticamente nei documenti di acquisto per il fornitore quando si compila il campo **Nr. cross-reference**</span><span class="sxs-lookup"><span data-stu-id="0a1ab-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="0a1ab-106"> </span><span class="sxs-lookup"><span data-stu-id="0a1ab-106">field.</span></span> <span data-ttu-id="0a1ab-107">La stessa funzionalità è valida per i numeri di articolo cliente nei documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="0a1ab-108">Di seguito viene descritto come utilizzare i cross reference articolo per gli acquisti.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="0a1ab-109">I passaggi sono simili per gli acquisti.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="0a1ab-110">Per impostare un cross reference articolo per una descrizione articolo di un fornitore</span><span class="sxs-lookup"><span data-stu-id="0a1ab-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="0a1ab-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a1ab-112">Aprire la scheda di un articolo per il quale si desidera creare un cross reference per la descrizione articolo che il fornitore utilizza per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="0a1ab-113">Scegliere l'azione **Cross reference**.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="0a1ab-114">In una nuova riga nella pagina **Cross reference per l'articolo**, compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="0a1ab-115">.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="0a1ab-116">Per immettere la descrizione articolo di un fornitore in un ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="0a1ab-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="0a1ab-117">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a1ab-118">Creare un ordine di acquisto per il fornitore per il quale si è impostato un cross-reference articolo nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="0a1ab-119">Creare una riga acquisto per l'articolo per il quale si è impostato un cross reference articolo nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="0a1ab-120">Nel campo **Nr. cross-reference**</span><span class="sxs-lookup"><span data-stu-id="0a1ab-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="0a1ab-121">selezionare il cross-reference articolo creato quindi scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="0a1ab-122">Il campo **Descrizione** della riga viene sovrascritto con la descrizione articolo del fornitore, come definito nel movimento cross-reference articolo.</span><span class="sxs-lookup"><span data-stu-id="0a1ab-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a1ab-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a1ab-123">See Also</span></span>
[<span data-ttu-id="0a1ab-124">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="0a1ab-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0a1ab-125">Magazzino</span><span class="sxs-lookup"><span data-stu-id="0a1ab-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0a1ab-126">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a1ab-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
