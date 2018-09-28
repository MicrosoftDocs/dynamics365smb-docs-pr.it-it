---
title: "Attività della warehouse | Documenti Microsoft"
description: "Dopo che le merci sono state ricevute e prima di venire spedite, viene eseguita una serie di attività di warehouse interne per garantire un flusso efficace nella warehouse e per organizzare e gestire l'inventario della società."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: de9f4a202579f347e8f0ebb3196d9b812a979ca3
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="ff49c-103">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="ff49c-103">Warehouse Management</span></span>
<span data-ttu-id="ff49c-104">Dopo che le merci sono state ricevute e prima di venire spedite, viene eseguita una serie di attività di warehouse interne per garantire un flusso efficace nella warehouse e per organizzare e gestire l'inventario della società.</span><span class="sxs-lookup"><span data-stu-id="ff49c-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="ff49c-105">In genere, le attività di warehouse includono lo stoccaggio degli articoli, il loro spostamento all'interno della warehouse o tra warehouse e il loro prelievo per l'assemblaggio, la produzione o la spedizione.</span><span class="sxs-lookup"><span data-stu-id="ff49c-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="ff49c-106">Gli articoli di assemblaggio da vendere o il magazzino possono inoltre essere considerati attività di warehouse ma vengono trattati altrove.</span><span class="sxs-lookup"><span data-stu-id="ff49c-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="ff49c-107">Per ulteriori informazioni, vedere [Gestione assemblaggio](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="ff49c-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="ff49c-108">Nelle warehouse di grandi dimensioni, queste diverse attività di gestione possono essere separate in base ai reparti e l'integrazione può essere gestita da un flusso di lavoro guidato.</span><span class="sxs-lookup"><span data-stu-id="ff49c-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="ff49c-109">Nelle installazioni più semplici, il flusso è meno formale e le attività di warehouse vengono eseguite tramite stoccaggi e prelievi di magazzino.</span><span class="sxs-lookup"><span data-stu-id="ff49c-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="ff49c-110">Per ulteriori informazioni sulle configurazioni di warehouse di base rispetto alle configurazioni avanzate, vedere [Dettagli di progettazione: Panoramica warehouse](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ff49c-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="ff49c-111">Prima di eseguire attività di warehouse, è necessario impostare il sistema per la complessità della relativa elaborazione di warehouse.</span><span class="sxs-lookup"><span data-stu-id="ff49c-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="ff49c-112">Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ff49c-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="ff49c-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="ff49c-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="ff49c-114">**Per**</span><span class="sxs-lookup"><span data-stu-id="ff49c-114">**To**</span></span>|<span data-ttu-id="ff49c-115">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="ff49c-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ff49c-116">Registrare il carico degli articoli nelle ubicazioni di warehouse, solo con un ordine di acquisto, nelle impostazioni semplici dell'ubicazione, o con un carico warehouse, in caso di processi warehouse parzialmente o completamente automatici nell'ubicazione.</span><span class="sxs-lookup"><span data-stu-id="ff49c-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="ff49c-117">Ricevere articoli</span><span class="sxs-lookup"><span data-stu-id="ff49c-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="ff49c-118">Ignorare i processi di stoccaggio e prelievo per velocizzare le operazioni dal carico o dalla produzione alla spedizione di un articolo.</span><span class="sxs-lookup"><span data-stu-id="ff49c-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="ff49c-119">Sottoporre gli articoli a cross-dock</span><span class="sxs-lookup"><span data-stu-id="ff49c-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="ff49c-120">Stoccare articoli ricevuti da acquisti, resi di vendita, trasferimenti o output di produzione, in base al processo warehouse configurato.</span><span class="sxs-lookup"><span data-stu-id="ff49c-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="ff49c-121">Stoccaggio di articoli</span><span class="sxs-lookup"><span data-stu-id="ff49c-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="ff49c-122">Spostare gli articoli tra collocazioni nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="ff49c-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="ff49c-123">Spostamento di articoli</span><span class="sxs-lookup"><span data-stu-id="ff49c-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="ff49c-124">Prelevare articoli da spedire, trasferire o utilizzare in assemblaggio o produzione, in base al processo warehouse configurato.</span><span class="sxs-lookup"><span data-stu-id="ff49c-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="ff49c-125">Prelievo di articoli</span><span class="sxs-lookup"><span data-stu-id="ff49c-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="ff49c-126">Registrare la spedizione degli articoli dalle ubicazioni di warehouse, solo con un ordine di vendita, nelle impostazioni semplici dell'ubicazione, o con una spedizione warehouse, in caso di processi warehouse parzialmente o completamente automatici nell'ubicazione.</span><span class="sxs-lookup"><span data-stu-id="ff49c-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="ff49c-127">Spedire articoli</span><span class="sxs-lookup"><span data-stu-id="ff49c-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="ff49c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff49c-128">See Also</span></span>  
[<span data-ttu-id="ff49c-129">Magazzino</span><span class="sxs-lookup"><span data-stu-id="ff49c-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ff49c-130">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ff49c-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ff49c-131">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ff49c-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ff49c-132">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="ff49c-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ff49c-133">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff49c-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

