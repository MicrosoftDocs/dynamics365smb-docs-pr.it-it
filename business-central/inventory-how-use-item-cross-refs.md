---
title: Utilizzare Cross reference articoli
description: Impostare i riferimenti tra le descrizioni che l'utente e il fornitore utilizzano per un articolo in modo da poter inserire la descrizione dell'articolo del fornitore nei documenti di acquisto.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0a9f84522598344435ad9c1263fe8cdea2e2a1e0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785650"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="13fc1-103">Utilizzare Cross reference articolo</span><span class="sxs-lookup"><span data-stu-id="13fc1-103">Use Item Cross References</span></span>
<span data-ttu-id="13fc1-104">Se si imposta un cross-reference tra la descrizione articolo utilizzata per un articolo e la descrizione che il fornitore dell'articolo utilizza, la descrizione articolo del fornitore viene inserita automaticamente nei documenti di acquisto per il fornitore quando si compila il campo **Nr. cross-reference**</span><span class="sxs-lookup"><span data-stu-id="13fc1-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="13fc1-105"> </span><span class="sxs-lookup"><span data-stu-id="13fc1-105">field.</span></span> <span data-ttu-id="13fc1-106">La stessa funzionalità è valida per i numeri di articolo cliente nei documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="13fc1-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="13fc1-107">Di seguito viene descritto come utilizzare i cross reference articolo per gli acquisti.</span><span class="sxs-lookup"><span data-stu-id="13fc1-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="13fc1-108">I passaggi sono simili per gli acquisti.</span><span class="sxs-lookup"><span data-stu-id="13fc1-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="13fc1-109">Sta diventando sempre più comune che gli identificatori degli articoli come GTIN o GUID contengano 30 o più caratteri, che è più di quanto la funzionalità corrente per i riferimenti incrociati degli articoli possa gestire.</span><span class="sxs-lookup"><span data-stu-id="13fc1-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="13fc1-110">Se è necessario utilizzare riferimenti che contengono più di 30 caratteri, l'amministratore può attivare la funzionalità **scrittura di riferimenti articolo più lunghi** nella pagina [Gestione delle funzionalità](https://businesscentral.dynamics.com/?page=2610) (il collegamento richiede un tenant [!INCLUDE[prod_short](includes/prod_short.md)]).</span><span class="sxs-lookup"><span data-stu-id="13fc1-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=2610) page (link requires that you have a [!INCLUDE[prod_short](includes/prod_short.md)] tenant).</span></span> <span data-ttu-id="13fc1-111">Il modo in cui si usano i riferimenti non cambia, ma i nomi di cose come pagine e pulsanti cambia.</span><span class="sxs-lookup"><span data-stu-id="13fc1-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="13fc1-112">Ad esempio, la pagina **Cross reference per l'articolo** diventerà la pagina **Movimenti riferimento per l'articolo**.</span><span class="sxs-lookup"><span data-stu-id="13fc1-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="13fc1-113">Per impostare un cross reference articolo per una descrizione articolo di un fornitore</span><span class="sxs-lookup"><span data-stu-id="13fc1-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="13fc1-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="13fc1-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="13fc1-115">Aprire la scheda di un articolo per il quale si desidera creare un cross reference per la descrizione articolo che il fornitore utilizza per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="13fc1-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="13fc1-116">Scegliere l'azione **Cross reference**.</span><span class="sxs-lookup"><span data-stu-id="13fc1-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="13fc1-117">Se non si riesce a trovare l'azione **Cross reference**, scegliere di visualizzare più opzioni, quindi trovarla in **Correlato** > **Articolo**.</span><span class="sxs-lookup"><span data-stu-id="13fc1-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="13fc1-118">In una nuova riga nella pagina **Cross reference per l'articolo**, compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="13fc1-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="13fc1-119">.</span><span class="sxs-lookup"><span data-stu-id="13fc1-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="13fc1-120">Per immettere la descrizione articolo di un fornitore in un ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="13fc1-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="13fc1-121">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="13fc1-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="13fc1-122">Creare un ordine di acquisto per il fornitore per il quale si è impostato un cross-reference articolo nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="13fc1-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="13fc1-123">Creare una riga acquisto per l'articolo per il quale si è impostato un cross reference articolo nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="13fc1-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="13fc1-124">Nel campo **Nr. cross-reference**</span><span class="sxs-lookup"><span data-stu-id="13fc1-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="13fc1-125">selezionare il cross-reference articolo creato quindi scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="13fc1-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="13fc1-126">Il campo **Descrizione** della riga viene sovrascritto con la descrizione articolo del fornitore, come definito nel movimento cross-reference articolo.</span><span class="sxs-lookup"><span data-stu-id="13fc1-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="13fc1-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="13fc1-127">See Also</span></span>
[<span data-ttu-id="13fc1-128">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="13fc1-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="13fc1-129">Magazzino</span><span class="sxs-lookup"><span data-stu-id="13fc1-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="13fc1-130">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13fc1-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]