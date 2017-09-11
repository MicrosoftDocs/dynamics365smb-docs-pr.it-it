---
title: Trasferire articoli tra le warehouse | Documenti Microsoft
description: Viene descritto come spostare il magazzino da un'area o una warehouse a un'altra con le registrazioni di riclassificazione o gli ordini di trasferimento.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d54b75240cb0a2dddcfabc488a18e0bf9635f82c
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-transfer-inventory-between-locations"></a><span data-ttu-id="90a6a-103">Procedura: Trasferire il magazzino tra le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="90a6a-103">How to: Transfer Inventory Between Locations</span></span>
<span data-ttu-id="90a6a-104">È possibile trasferire articoli di magazzino tra ubicazioni creando ordini di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="90a6a-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="90a6a-105">In alternativa, è possibile utilizzare le registrazioni di riclassificazione articoli.</span><span class="sxs-lookup"><span data-stu-id="90a6a-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="90a6a-106">Con gli ordini di trasferimento, si spedisce il trasferimento in uscita da un'ubicazione e si riceve il trasferimento in entrata presso un'altra ubicazione.</span><span class="sxs-lookup"><span data-stu-id="90a6a-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="90a6a-107">Ciò consente di gestire le attività di warehouse implicate e offre maggiore certezza che le quantità di magazzino di vengano aggiornate correttamente.</span><span class="sxs-lookup"><span data-stu-id="90a6a-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="90a6a-108">Con la registrazione di riclassificazione, si compila semplicemente i campi **Codice ubicazione** e **Nuovo codice ubicazione**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="90a6a-109">Quando si contabilizza la registrazione, i movimenti contabili articoli vengono rettificati nelle ubicazioni in questione.</span><span class="sxs-lookup"><span data-stu-id="90a6a-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="90a6a-110">Con questo metodo, le attività di warehouse non vengono gestite.</span><span class="sxs-lookup"><span data-stu-id="90a6a-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="90a6a-111">Se sono stati registrati articoli in magazzino senza un codice ubicazione, ad esempio a partire da un periodo in cui era disponibile solo una warehouse, non è possibile trasferire gli articoli tramite ordini di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="90a6a-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="90a6a-112">Al contrario, è necessario utilizzare le registrazioni di riclassificazione per riclassificare gli articoli da un codice di un'ubicazione vuota a un codice di ubicazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="90a6a-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="90a6a-113">Per ulteriori informazioni, vedere il passaggio 3 nella sezione "Per trasferire gli articoli con le registrazioni di riclassificazione articolo".</span><span class="sxs-lookup"><span data-stu-id="90a6a-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="90a6a-114">Per trasferire gli articoli, le ubicazioni e i percorsi di trasferimento devono essere impostati.</span><span class="sxs-lookup"><span data-stu-id="90a6a-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="90a6a-115">Per ulteriori informazioni, vedere [Procedura: Impostare le ubicazioni](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="90a6a-115">For more information, see [How to: Set Up Locations](inventory-how-setup-locations.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="90a6a-116">Questa funzionalità richiede che l'esperienza sia impostata su **Suite**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="90a6a-117">Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="90a6a-117">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="90a6a-118">Per trasferire gli articoli con un ordine di trasferimento</span><span class="sxs-lookup"><span data-stu-id="90a6a-118">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="90a6a-119">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di trasferimento**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="90a6a-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="90a6a-120">Nella finestra **Ordine di trasferimento** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="90a6a-120">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="90a6a-121">Se sono stati compilati i campi **Codice in transito**, **Codice spedizioniere** e **Codice servizio spedizioniere** nella finestra **Specifica percorso trasf.**</span><span class="sxs-lookup"><span data-stu-id="90a6a-121">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.**</span></span> <span data-ttu-id="90a6a-122">quando si imposta il percorso di trasferimento, i campi corrispondenti dell'ordine di trasferimento verranno compilati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="90a6a-122">window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="90a6a-123">Se si compila il campo **Servizio spedizioniere**, il programma calcola la data di ricezione nell'ubicazione di trasferimento sommando il tempo di spedizione del servizio spedizioniere alla data di spedizione.</span><span class="sxs-lookup"><span data-stu-id="90a6a-123">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="90a6a-124">Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la spedizione degli articoli.</span><span class="sxs-lookup"><span data-stu-id="90a6a-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="90a6a-125">Scegliere l'azione **Registra**, selezionare l'opzione **Spedizione**, quindi il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="90a6a-126">Gli articoli sono ora in transito tra le ubicazioni specificate, in base al percorso indicato per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="90a6a-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="90a6a-127">Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la ricezione degli articoli.</span><span class="sxs-lookup"><span data-stu-id="90a6a-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="90a6a-128">Scegliere l'azione **Registra**, selezionare l'opzione **Ricevi**, quindi il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-128">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="90a6a-129">Per trasferire gli articoli con le registrazioni di riclassificazione articolo</span><span class="sxs-lookup"><span data-stu-id="90a6a-129">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="90a6a-130">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riclassificazioni articoli**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="90a6a-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="90a6a-131">Nella finestra **Batch reg. riclass. articoli** compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="90a6a-131">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="90a6a-132">Nel campo **Cod. ubicazione** immettere l'ubicazione in cui gli articoli si trovano attualmente.</span><span class="sxs-lookup"><span data-stu-id="90a6a-132">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="90a6a-133">Per trasferire gli articoli che non presentano codice ubicazione, lasciare vuoto il campo **Codice ubicazione**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-133">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="90a6a-134">Nel campo **Nuovo codice ubicazione** immettere l'ubicazione verso cui si intende trasferire gli articoli.</span><span class="sxs-lookup"><span data-stu-id="90a6a-134">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="90a6a-135">Scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-135">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="90a6a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90a6a-136">See Also</span></span>
[<span data-ttu-id="90a6a-137">Gestire i costi del magazzino</span><span class="sxs-lookup"><span data-stu-id="90a6a-137">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="90a6a-138">Procedura: Impostare le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="90a6a-138">How to: Set Up Locations</span></span>](inventory-how-setup-locations.md)  
[<span data-ttu-id="90a6a-139">Catena di approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="90a6a-139">Supply Chain</span></span>](madeira-supply-chain.md)  
<span data-ttu-id="90a6a-140">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90a6a-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="90a6a-141">[Personalizzazione dell'esperienza [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="90a6a-141">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="90a6a-142">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="90a6a-142">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
