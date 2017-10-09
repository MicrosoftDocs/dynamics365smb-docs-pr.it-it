---
title: 'Dettagli di progettazione: Panoramica warehouse | Microsoft Docs'
description: "Per supportare la gestione fisica degli articoli a livello di collocazione e di zona, è necessario tenere traccia di tutte le informazioni per ogni transazione o spostamento nella warehouse. Le informazioni sono gestite nella tabella **Movimento warehouse**. Ogni transazione viene memorizzata in un registro warehouse."
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
ms.openlocfilehash: f5dc30ab398ae41ab8c36b6c207d2f48036cc98c
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="b5e32-105">Dettagli di progettazione: Panoramica warehouse</span><span class="sxs-lookup"><span data-stu-id="b5e32-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="b5e32-106">Per supportare la gestione fisica degli articoli a livello di collocazione e di zona, è necessario tenere traccia di tutte le informazioni per ogni transazione o spostamento nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="b5e32-107">Le informazioni sono gestite nella tabella **Movimento warehouse**.</span><span class="sxs-lookup"><span data-stu-id="b5e32-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="b5e32-108">Ogni transazione viene memorizzata in un registro warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="b5e32-109">I documenti warehouse e le registrazioni di warehouse vengono utilizzati per registrare i movimenti degli articoli nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="b5e32-110">Ogni volta che viene spostato, ricevuto, stoccato, selezionare, spedito o rettificato un articolo nel magazzino, i movimenti di magazzino vengono registrati per archiviare le informazioni fisiche sull'area, la collocazione e la quantità.</span><span class="sxs-lookup"><span data-stu-id="b5e32-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span> <span data-ttu-id="b5e32-111">Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in entrata](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="b5e32-111">For more information, see [Design Details: Inbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="b5e32-112">La tabella **Contenuto collocazione** viene utilizzata per gestire tutte le dimensioni diverse del contenuto di una collocazione per articolo, ad esempio l'unità di misura, la quantità massima e quella minima.</span><span class="sxs-lookup"><span data-stu-id="b5e32-112">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="b5e32-113">La tabella **Contenuto collocazione** contiene anche campi di flusso ai movimenti della warehouse, istruzioni di warehouse e righe delle registrazioni di warehouse, grazie ai quali è possibile calcolare rapidamente la disponibilità di un articolo per collocazione e la collocazione per un articolo.</span><span class="sxs-lookup"><span data-stu-id="b5e32-113">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="b5e32-114">Per ulteriori informazioni, vedere [Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="b5e32-114">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="b5e32-115">Quando le registrazioni degli articoli avvengono in una posizione diversa dal modulo warehouse, viene utilizzata una collocazione di rettifica predefinita per ubicazione per sincronizzare i movimenti warehouse con i movimenti di magazzino.</span><span class="sxs-lookup"><span data-stu-id="b5e32-115">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="b5e32-116">Durante l'inventario fisico del magazzino, tutte le differenze tra le quantità calcolate e quelle conteggiate vengono registrate nella collocazione di rettifica e quindi registrate come movimenti contabili articoli di rettifica.</span><span class="sxs-lookup"><span data-stu-id="b5e32-116">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="b5e32-117">Per ulteriori informazioni, vedere [Dettagli di progettazione: Integrazione con il magazzino](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="b5e32-117">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="b5e32-118">Nell'illustrazione seguente sono descritti i tipici flussi di warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-118">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="b5e32-119">![Panoramica dei processi della warehouse](media/design_details_warehouse_management_overview.png "design_details_warehouse_management_overview")</span><span class="sxs-lookup"><span data-stu-id="b5e32-119">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "design_details_warehouse_management_overview")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="b5e32-120">Gestione avanzata o di base della warehouse</span><span class="sxs-lookup"><span data-stu-id="b5e32-120">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="b5e32-121">La funzionalità di warehouse in [!INCLUDE[d365fin](includes/d365fin_md.md)] può essere implementata in diversi livelli di complessità, a seconda dei processi e del volume degli ordini di una società.</span><span class="sxs-lookup"><span data-stu-id="b5e32-121">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="b5e32-122">La principale differenza consiste nel fatto che le attività sono eseguite ordine per ordine nella gestione di base della warehouse, mentre vengono eseguite al momento del consolidamento per più ordini nella gestione avanzata della warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-122">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="b5e32-123">Per differenziare tra i diversi livelli di complessità, questa documentazione fa riferimento a due termini generali, gestione di base della warehouse e gestione avanzata della warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-123">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="b5e32-124">Questa semplice differenziazione copre numerosi livelli di complessità come definito dal setup dell'ubicazione e i sottoprodotti, ciascuno supportato da documenti di interfaccia utente differenti.</span><span class="sxs-lookup"><span data-stu-id="b5e32-124">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="b5e32-125">Per ulteriori informazioni, vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b5e32-125">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b5e32-126">Il livello più avanzato della gestione della warehouse è denominato "Installazioni WMS" in questa documentazione, poiché questo livello richiede la funzionalità più avanzata, vale a dire Sistema di gestione warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-126">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="b5e32-127">I seguenti documenti dell'interfaccia utente vengono utilizzati nelle gestioni di base e avanzata della warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-127">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="b5e32-128">Documenti di base dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b5e32-128">Basic UI Documents</span></span>  

-   <span data-ttu-id="b5e32-129">**Stoccaggio in magazzino**</span><span class="sxs-lookup"><span data-stu-id="b5e32-129">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="b5e32-130">**Prelievi magazzino**</span><span class="sxs-lookup"><span data-stu-id="b5e32-130">**Inventory Pick**</span></span>  
-   <span data-ttu-id="b5e32-131">**Movimento di magazzino**</span><span class="sxs-lookup"><span data-stu-id="b5e32-131">**Inventory Movement**</span></span>  
-   <span data-ttu-id="b5e32-132">**Reg. Magazzino**</span><span class="sxs-lookup"><span data-stu-id="b5e32-132">**Item Journal**</span></span>  
-   <span data-ttu-id="b5e32-133">**Registrazioni riclassificazione articolo**</span><span class="sxs-lookup"><span data-stu-id="b5e32-133">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="b5e32-134">(Vari report)</span><span class="sxs-lookup"><span data-stu-id="b5e32-134">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="b5e32-135">Documenti dell'interfaccia utente avanzati</span><span class="sxs-lookup"><span data-stu-id="b5e32-135">Advanced UI Documents</span></span>  

-   <span data-ttu-id="b5e32-136">**Carico warehouse**</span><span class="sxs-lookup"><span data-stu-id="b5e32-136">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="b5e32-137">**Prospetto stoccaggi**</span><span class="sxs-lookup"><span data-stu-id="b5e32-137">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="b5e32-138">**Stoccaggio warehouse**</span><span class="sxs-lookup"><span data-stu-id="b5e32-138">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="b5e32-139">**Prospetto prelievi**</span><span class="sxs-lookup"><span data-stu-id="b5e32-139">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="b5e32-140">**Prelievo warehouse**</span><span class="sxs-lookup"><span data-stu-id="b5e32-140">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="b5e32-141">**Movimento worksheet**</span><span class="sxs-lookup"><span data-stu-id="b5e32-141">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="b5e32-142">**Movimentazione warehouse**</span><span class="sxs-lookup"><span data-stu-id="b5e32-142">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="b5e32-143">**Prelievo interno whse.**</span><span class="sxs-lookup"><span data-stu-id="b5e32-143">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="b5e32-144">**Stocc. int. whse.**</span><span class="sxs-lookup"><span data-stu-id="b5e32-144">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="b5e32-145">**Prospetto creaz. collocazione**</span><span class="sxs-lookup"><span data-stu-id="b5e32-145">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="b5e32-146">**Prospetto creaz. cont. colloc.**</span><span class="sxs-lookup"><span data-stu-id="b5e32-146">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="b5e32-147">**Registrazioni articoli whse.**</span><span class="sxs-lookup"><span data-stu-id="b5e32-147">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="b5e32-148">**Reg. ricl. articoli whse**</span><span class="sxs-lookup"><span data-stu-id="b5e32-148">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="b5e32-149">(Vari report)</span><span class="sxs-lookup"><span data-stu-id="b5e32-149">(Various reports)</span></span>  

<span data-ttu-id="b5e32-150">Per ulteriori informazioni su ogni documento, vedere i rispettivi argomenti della finestra.</span><span class="sxs-lookup"><span data-stu-id="b5e32-150">For more information about each document, see the respective window topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="b5e32-151">Terminologia</span><span class="sxs-lookup"><span data-stu-id="b5e32-151">Terminology</span></span>  
<span data-ttu-id="b5e32-152">Per allinearsi ai concetti finanziari di acquisti e vendite, la documentazione della warehouse di [!INCLUDE[d365fin](includes/d365fin_md.md)] si riferisce ai seguenti termini per il flusso degli articoli nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="b5e32-152">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="b5e32-153">Termine</span><span class="sxs-lookup"><span data-stu-id="b5e32-153">Term</span></span>|<span data-ttu-id="b5e32-154">Description</span><span class="sxs-lookup"><span data-stu-id="b5e32-154">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="b5e32-155">Flusso in entrata</span><span class="sxs-lookup"><span data-stu-id="b5e32-155">Inbound flow</span></span>|<span data-ttu-id="b5e32-156">Spostamento articoli nell'ubicazione della warehouse, ad esempio gli acquisti e i trasferimenti in entrata.</span><span class="sxs-lookup"><span data-stu-id="b5e32-156">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="b5e32-157">Flusso interno</span><span class="sxs-lookup"><span data-stu-id="b5e32-157">Internal flow</span></span>|<span data-ttu-id="b5e32-158">Spostamento articoli nell'ubicazione della warehouse, ad esempio i componenti di produzione e l'output.</span><span class="sxs-lookup"><span data-stu-id="b5e32-158">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="b5e32-159">Flusso in uscita</span><span class="sxs-lookup"><span data-stu-id="b5e32-159">Outbound flow</span></span>|<span data-ttu-id="b5e32-160">Spostamento articoli all'esterno dell'ubicazione della warehouse, ad esempio le vendite e i trasferimenti in uscita.</span><span class="sxs-lookup"><span data-stu-id="b5e32-160">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="b5e32-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5e32-161">See Also</span></span>  
 [<span data-ttu-id="b5e32-162">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="b5e32-162">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

