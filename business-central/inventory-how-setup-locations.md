---
title: Impostare una scheda ubicazione e definire i percorsi di trasferimento | Documenti Microsoft
description: È possibile creare una scheda ubicazione per ogni area in cui vengono immagazzinati gli articoli in magazzino, ad esempio warehouse o centro di distribuzione, per impostare percorsi per il trasferimento degli articoli tra le ubicazioni.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2018
ms.author: SorenGP
ms.openlocfilehash: 828979bf181f1cd7f7a66d2c7c8ac8a2700b732b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802128"
---
# <a name="set-up-locations"></a><span data-ttu-id="96410-103">Impostare le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="96410-103">Set Up Locations</span></span>
<span data-ttu-id="96410-104">Se si acquista, immagazzina o si vendono articoli in più aree o warehouse, è necessario impostare ogni ubicazione con una scheda ubicazione e definire i percorsi di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="96410-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="96410-105">È quindi possibile creare le righe del documento per una specifica ubicazione, visualizzare la disponibilità per ubicazione e trasferire il magazzino tra le ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="96410-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="96410-106">Per ulteriori informazioni, vedere [Gestire il magazzino](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="96410-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="96410-107">Per creare una nuova scheda Ubicazione</span><span class="sxs-lookup"><span data-stu-id="96410-107">To create a location card</span></span>
1. <span data-ttu-id="96410-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="96410-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="96410-109">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="96410-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="96410-110">Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="96410-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="96410-111">Ripetere i passaggi 2 e 3 per ogni ubicazione in cui si desidera mantenere il magazzino.</span><span class="sxs-lookup"><span data-stu-id="96410-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="96410-112">Molti campi della scheda ubicazione fanno riferimento alla gestione degli articoli nei processi della warehouse in entrata e in uscita.</span><span class="sxs-lookup"><span data-stu-id="96410-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="96410-113">Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="96410-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="96410-114">Per creare i percorsi di trasferimento</span><span class="sxs-lookup"><span data-stu-id="96410-114">To create a transfer route</span></span>
1. <span data-ttu-id="96410-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Percorsi di trasferimento** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="96410-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="96410-116">In alternativa, da una qualsiasi pagina **Scheda Ubicazione** scegliere l'azione **Percorsi trasferimento**.</span><span class="sxs-lookup"><span data-stu-id="96410-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="96410-117">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="96410-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="96410-118">Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="96410-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="96410-119">A questo punto è possibile trasferire agli articoli di magazzino tra due ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="96410-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="96410-120">Per ulteriori informazioni, vedere [Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="96410-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="96410-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96410-121">See Also</span></span>
[<span data-ttu-id="96410-122">Gestire i costi del magazzino</span><span class="sxs-lookup"><span data-stu-id="96410-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="96410-123">[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="96410-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="96410-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="96410-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="96410-125">Modifica delle funzionalità visualizzate</span><span class="sxs-lookup"><span data-stu-id="96410-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="96410-126">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="96410-126">General Business Functionality</span></span>](ui-across-business-areas.md)
