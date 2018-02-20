---
title: "Attività della warehouse | Documenti Microsoft"
description: "Dopo che le merci sono state ricevute e prima di venire spedite, viene eseguita una serie di attività di warehouse interne per garantire un flusso efficace nella warehouse e per organizzare e gestire l'inventario della società."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: c8d4ee33395c18cb7755fd1877b2af813fb9da43
ms.contentlocale: it-it
ms.lasthandoff: 02/02/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="fdd26-103">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="fdd26-103">Warehouse Management</span></span>
<span data-ttu-id="fdd26-104">Dopo che le merci sono state ricevute e prima di venire spedite, viene eseguita una serie di attività di warehouse interne per garantire un flusso efficace nella warehouse e per organizzare e gestire l'inventario della società.</span><span class="sxs-lookup"><span data-stu-id="fdd26-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="fdd26-105">In genere, le attività di warehouse includono lo stoccaggio degli articoli, il loro spostamento all'interno della warehouse o tra warehouse e il loro prelievo per l'assemblaggio, la produzione o la spedizione.</span><span class="sxs-lookup"><span data-stu-id="fdd26-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="fdd26-106">Gli articoli di assemblaggio da vendere o il magazzino possono inoltre essere considerati attività di warehouse ma vengono trattati altrove.</span><span class="sxs-lookup"><span data-stu-id="fdd26-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="fdd26-107">Per ulteriori informazioni, vedere [Gestione assemblaggio](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="fdd26-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="fdd26-108">Nelle warehouse di grandi dimensioni, queste diverse attività di gestione possono essere separate in base ai reparti e l'integrazione può essere gestita da un flusso di lavoro guidato.</span><span class="sxs-lookup"><span data-stu-id="fdd26-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="fdd26-109">Nelle installazioni più semplici, il flusso è meno formale e le attività di warehouse vengono eseguite tramite stoccaggi e prelievi di magazzino.</span><span class="sxs-lookup"><span data-stu-id="fdd26-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="fdd26-110">Per ulteriori informazioni sulle configurazioni di warehouse di base rispetto alle configurazioni avanzate, vedere [Dettagli di progettazione: Panoramica warehouse](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fdd26-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="fdd26-111">Prima di eseguire attività di warehouse, è necessario impostare il sistema per la complessità della relativa elaborazione di warehouse.</span><span class="sxs-lookup"><span data-stu-id="fdd26-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="fdd26-112">Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="fdd26-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="fdd26-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="fdd26-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="fdd26-114">**Per**</span><span class="sxs-lookup"><span data-stu-id="fdd26-114">**To**</span></span>|<span data-ttu-id="fdd26-115">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="fdd26-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="fdd26-116">Registrare il carico degli articoli nelle ubicazioni di warehouse, solo con un ordine di acquisto, nelle impostazioni semplici dell'ubicazione, o con un carico warehouse, in caso di processi warehouse parzialmente o completamente automatici nell'ubicazione.</span><span class="sxs-lookup"><span data-stu-id="fdd26-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="fdd26-117">Ricevere articoli</span><span class="sxs-lookup"><span data-stu-id="fdd26-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="fdd26-118">Ignorare i processi di stoccaggio e prelievo per velocizzare le operazioni dal carico o dalla produzione alla spedizione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="fdd26-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="fdd26-119">Sottoporre gli articoli a cross-dock</span><span class="sxs-lookup"><span data-stu-id="fdd26-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="fdd26-120">Stoccare articoli ricevuti da acquisti, resi di vendita, trasferimenti o output di produzione, in base al processo warehouse configurato.</span><span class="sxs-lookup"><span data-stu-id="fdd26-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="fdd26-121">Stoccaggio di articoli</span><span class="sxs-lookup"><span data-stu-id="fdd26-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="fdd26-122">Spostare gli articoli tra collocazioni nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="fdd26-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="fdd26-123">Spostamento di articoli</span><span class="sxs-lookup"><span data-stu-id="fdd26-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="fdd26-124">Prelevare articoli da spedire, trasferire o utilizzare in assemblaggio o produzione, in base al processo warehouse configurato.</span><span class="sxs-lookup"><span data-stu-id="fdd26-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="fdd26-125">Prelievo di articoli</span><span class="sxs-lookup"><span data-stu-id="fdd26-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="fdd26-126">Registrare la spedizione degli articoli dalle ubicazioni di warehouse, solo con un ordine di vendita, nelle impostazioni semplici dell'ubicazione, o con una spedizione warehouse, in caso di processi warehouse parzialmente o completamente automatici nell'ubicazione.</span><span class="sxs-lookup"><span data-stu-id="fdd26-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="fdd26-127">Spedire articoli</span><span class="sxs-lookup"><span data-stu-id="fdd26-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="fdd26-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdd26-128">See Also</span></span>  
[<span data-ttu-id="fdd26-129">Magazzino</span><span class="sxs-lookup"><span data-stu-id="fdd26-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="fdd26-130">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="fdd26-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="fdd26-131">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="fdd26-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="fdd26-132">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="fdd26-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="fdd26-133">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fdd26-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

