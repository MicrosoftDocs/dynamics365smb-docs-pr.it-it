---
title: Prelievo e spedizione nelle configurazioni della warehouse di base | Documenti Microsoft
description: In Business Central, i processi in uscita per il prelievo e la spedizione possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96a837eaded2cf9be5e1fabb4d7f81415a171f96
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393451"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="87eb5-103">Procedura dettagliata: prelievo e spedizione nelle configurazioni della warehouse di base</span><span class="sxs-lookup"><span data-stu-id="87eb5-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="87eb5-104">In [!INCLUDE[prod_short](includes/prod_short.md)], i processi in uscita per il prelievo e la spedizione possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.</span><span class="sxs-lookup"><span data-stu-id="87eb5-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="87eb5-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="87eb5-105">Method</span></span>|<span data-ttu-id="87eb5-106">Processo in entrata</span><span class="sxs-lookup"><span data-stu-id="87eb5-106">Inbound process</span></span>|<span data-ttu-id="87eb5-107">Collocazioni</span><span class="sxs-lookup"><span data-stu-id="87eb5-107">Bins</span></span>|<span data-ttu-id="87eb5-108">Prelievi</span><span class="sxs-lookup"><span data-stu-id="87eb5-108">Picks</span></span>|<span data-ttu-id="87eb5-109">Spedizioni</span><span class="sxs-lookup"><span data-stu-id="87eb5-109">Shipments</span></span>|<span data-ttu-id="87eb5-110">Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="87eb5-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="87eb5-111">A</span><span class="sxs-lookup"><span data-stu-id="87eb5-111">A</span></span>|<span data-ttu-id="87eb5-112">Registra prelievo e spedizione dalla riga ordine</span><span class="sxs-lookup"><span data-stu-id="87eb5-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="87eb5-113">X</span><span class="sxs-lookup"><span data-stu-id="87eb5-113">X</span></span>|||<span data-ttu-id="87eb5-114">2</span><span class="sxs-lookup"><span data-stu-id="87eb5-114">2</span></span>|  
|<span data-ttu-id="87eb5-115">B</span><span class="sxs-lookup"><span data-stu-id="87eb5-115">B</span></span>|<span data-ttu-id="87eb5-116">Registra prelievo e spedizione da un documento di prelievo magazzino</span><span class="sxs-lookup"><span data-stu-id="87eb5-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="87eb5-117">X</span><span class="sxs-lookup"><span data-stu-id="87eb5-117">X</span></span>||<span data-ttu-id="87eb5-118">3</span><span class="sxs-lookup"><span data-stu-id="87eb5-118">3</span></span>|  
|<span data-ttu-id="87eb5-119">C</span><span class="sxs-lookup"><span data-stu-id="87eb5-119">C</span></span>|<span data-ttu-id="87eb5-120">Registra prelievo e spedizione da un documento di spedizione warehouse</span><span class="sxs-lookup"><span data-stu-id="87eb5-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="87eb5-121">X</span><span class="sxs-lookup"><span data-stu-id="87eb5-121">X</span></span>|<span data-ttu-id="87eb5-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="87eb5-122">4/5/6</span></span>|  
|<span data-ttu-id="87eb5-123">D</span><span class="sxs-lookup"><span data-stu-id="87eb5-123">D</span></span>|<span data-ttu-id="87eb5-124">Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse</span><span class="sxs-lookup"><span data-stu-id="87eb5-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="87eb5-125">X</span><span class="sxs-lookup"><span data-stu-id="87eb5-125">X</span></span>|<span data-ttu-id="87eb5-126">X</span><span class="sxs-lookup"><span data-stu-id="87eb5-126">X</span></span>|<span data-ttu-id="87eb5-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="87eb5-127">4/5/6</span></span>|  

<span data-ttu-id="87eb5-128">Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="87eb5-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="87eb5-129">Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="87eb5-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a><span data-ttu-id="87eb5-130">Informazioni sulla procedura dettagliata</span><span class="sxs-lookup"><span data-stu-id="87eb5-130">About This Walkthrough</span></span>

<span data-ttu-id="87eb5-131">Nelle configurazioni della warehouse di base in cui un'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, utilizzare la pagina **Prelievi magazzino** per registrare le informazioni riguardanti il prelievo e la spedizione per i documenti di origine in uscita.</span><span class="sxs-lookup"><span data-stu-id="87eb5-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="87eb5-132">Il documento di origine in uscita può essere un ordine di vendita, un ordine di reso da acquisto, un ordine di trasferimento in uscita o un ordine di produzione i cui componenti sono necessari.</span><span class="sxs-lookup"><span data-stu-id="87eb5-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="87eb5-133">In questa procedura dettagliata sono illustrati i task seguenti:</span><span class="sxs-lookup"><span data-stu-id="87eb5-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="87eb5-134">Impostazione ubicazione ARGENTO per i prelievi magazzino.</span><span class="sxs-lookup"><span data-stu-id="87eb5-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="87eb5-135">Creazione di un ordine di vendita per il cliente 10000 per 30 altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="87eb5-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="87eb5-136">Rilascio dell'ordine di vendita per la gestione warehouse.</span><span class="sxs-lookup"><span data-stu-id="87eb5-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="87eb5-137">Creazione di un prelievo di magazzino in base al documento origine rilasciato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="87eb5-138">Registrazione della movimentazione warehouse dalla warehouse e registrazione contemporanea della spedizione vendita per l'ordine di vendita di origine.</span><span class="sxs-lookup"><span data-stu-id="87eb5-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a><span data-ttu-id="87eb5-139">Ruoli</span><span class="sxs-lookup"><span data-stu-id="87eb5-139">Roles</span></span>

<span data-ttu-id="87eb5-140">Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:</span><span class="sxs-lookup"><span data-stu-id="87eb5-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="87eb5-141">Manager warehouse</span><span class="sxs-lookup"><span data-stu-id="87eb5-141">Warehouse Manager</span></span>  
- <span data-ttu-id="87eb5-142">Gestore ordini</span><span class="sxs-lookup"><span data-stu-id="87eb5-142">Order Processor</span></span>  
- <span data-ttu-id="87eb5-143">Lavoro warehouse</span><span class="sxs-lookup"><span data-stu-id="87eb5-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="87eb5-144">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="87eb5-144">Prerequisites</span></span>

<span data-ttu-id="87eb5-145">Per completare questa procedura dettagliata, sarà necessario:</span><span class="sxs-lookup"><span data-stu-id="87eb5-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="87eb5-146">Per [!INCLUDE[prod_short](includes/prod_short.md)] online, una società basata sull'opzione **Valutazione avanzata - Dati di esempio completi** in un ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="87eb5-146">For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="87eb5-147">Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, CRONUS International Ltd. installato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-147">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="87eb5-148">Per diventare un impiegato warehouse presso l'ubicazione ARGENTO, effettuare i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="87eb5-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="87eb5-149">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="87eb5-150">Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="87eb5-151">Nel campo **Codice ubicazione** immettere ARGENTO.</span><span class="sxs-lookup"><span data-stu-id="87eb5-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="87eb5-152">Selezionare il campo **Default**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="87eb5-153">Rendere l'articolo LS-81 disponibile nell'ubicazione ARGENTO seguendo i passaggi di seguito riportati:</span><span class="sxs-lookup"><span data-stu-id="87eb5-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="87eb5-154">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni magazzino** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="87eb5-155">Aprire il giornale di default e quindi creare due righe registrazioni magazzino con le informazioni seguenti sulla data di lavoro (23 gennaio).</span><span class="sxs-lookup"><span data-stu-id="87eb5-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="87eb5-156">Tipo movimento</span><span class="sxs-lookup"><span data-stu-id="87eb5-156">Entry Type</span></span>|<span data-ttu-id="87eb5-157">Numero di articolo</span><span class="sxs-lookup"><span data-stu-id="87eb5-157">Item Number</span></span>|<span data-ttu-id="87eb5-158">Cod. ubicazione</span><span class="sxs-lookup"><span data-stu-id="87eb5-158">Location Code</span></span>|<span data-ttu-id="87eb5-159">Codice collocazione</span><span class="sxs-lookup"><span data-stu-id="87eb5-159">Bin Code</span></span>|<span data-ttu-id="87eb5-160">Quantità</span><span class="sxs-lookup"><span data-stu-id="87eb5-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="87eb5-161">Rettifica positiva</span><span class="sxs-lookup"><span data-stu-id="87eb5-161">Positive Adjmt.</span></span>|<span data-ttu-id="87eb5-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="87eb5-162">LS-81</span></span>|<span data-ttu-id="87eb5-163">ARGENTO</span><span class="sxs-lookup"><span data-stu-id="87eb5-163">SILVER</span></span>|<span data-ttu-id="87eb5-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="87eb5-164">S-01-0001</span></span>|<span data-ttu-id="87eb5-165">20</span><span class="sxs-lookup"><span data-stu-id="87eb5-165">20</span></span>|  
        |<span data-ttu-id="87eb5-166">Rettifica positiva</span><span class="sxs-lookup"><span data-stu-id="87eb5-166">Positive Adjmt.</span></span>|<span data-ttu-id="87eb5-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="87eb5-167">LS-81</span></span>|<span data-ttu-id="87eb5-168">ARGENTO</span><span class="sxs-lookup"><span data-stu-id="87eb5-168">SILVER</span></span>|<span data-ttu-id="87eb5-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="87eb5-169">S-01-0002</span></span>|<span data-ttu-id="87eb5-170">20</span><span class="sxs-lookup"><span data-stu-id="87eb5-170">20</span></span>|  

  3. <span data-ttu-id="87eb5-171">Scegliere l'azione **Registra**, quindi selezionare il pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="87eb5-172">Scenario</span><span class="sxs-lookup"><span data-stu-id="87eb5-172">Story</span></span>

<span data-ttu-id="87eb5-173">Ellen, responsabile warehouse presso CRONUS, imposta la warehouse ARGENTO per la gestione dei prelievi di base in cui gli addetti alla warehouse elaborano ordini in uscita singoli.</span><span class="sxs-lookup"><span data-stu-id="87eb5-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="87eb5-174">Elisabetta, il gestore ordini, crea un ordine di vendita per 30 unità dell'articolo LS-81 da spedire al cliente 10000 dalla warehouse ARGENTO.</span><span class="sxs-lookup"><span data-stu-id="87eb5-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="87eb5-175">Gianni, il lavoratore warehouse deve assicurarsi che la spedizione sia preparata e consegnata al cliente.</span><span class="sxs-lookup"><span data-stu-id="87eb5-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="87eb5-176">Gianni gestisce tutte le attività interessate nella pagina **Prelievo magazzino** che automaticamente punta alle collocazioni in cui viene archiviato LS-81.</span><span class="sxs-lookup"><span data-stu-id="87eb5-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="87eb5-177">Impostazione dell'ubicazione</span><span class="sxs-lookup"><span data-stu-id="87eb5-177">Setting Up the Location</span></span>

<span data-ttu-id="87eb5-178">L'impostazione della pagina **Scheda Ubicazione** definisce i flussi della warehouse della società.</span><span class="sxs-lookup"><span data-stu-id="87eb5-178">The setup of the **Location Card** page defines the company's warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="87eb5-179">Per impostare l'ubicazione</span><span class="sxs-lookup"><span data-stu-id="87eb5-179">To set up the location</span></span>

1. <span data-ttu-id="87eb5-180">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87eb5-181">Aprire la scheda ubicazione ARGENTO.</span><span class="sxs-lookup"><span data-stu-id="87eb5-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="87eb5-182">Nella Scheda Dettaglio **Warehouse** scegliere la casella di controllo **Richiesto prelievo**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="87eb5-183">Creazione dell'ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="87eb5-183">Creating the Sales Order</span></span>

<span data-ttu-id="87eb5-184">Gli ordini di vendita sono il tipo più comune di documenti origine in uscita.</span><span class="sxs-lookup"><span data-stu-id="87eb5-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="87eb5-185">Per creare l'ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="87eb5-185">To create the sales order</span></span>

1. <span data-ttu-id="87eb5-186">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87eb5-187">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="87eb5-188">Creare un ordine di vendita per il fornitore 10000 alla data di lavoro (23 gennaio) con la riga di ordine di vendita seguente.</span><span class="sxs-lookup"><span data-stu-id="87eb5-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="87eb5-189">Articolo</span><span class="sxs-lookup"><span data-stu-id="87eb5-189">Item</span></span>|<span data-ttu-id="87eb5-190">Cod. ubicazione</span><span class="sxs-lookup"><span data-stu-id="87eb5-190">Location Code</span></span>|<span data-ttu-id="87eb5-191">Quantità</span><span class="sxs-lookup"><span data-stu-id="87eb5-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="87eb5-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="87eb5-192">LS_81</span></span>|<span data-ttu-id="87eb5-193">ARGENTO</span><span class="sxs-lookup"><span data-stu-id="87eb5-193">SILVER</span></span>|<span data-ttu-id="87eb5-194">30</span><span class="sxs-lookup"><span data-stu-id="87eb5-194">30</span></span>|  

     <span data-ttu-id="87eb5-195">Comunicare alla warehouse che l'ordine di vendita è pronto per la gestione warehouse.</span><span class="sxs-lookup"><span data-stu-id="87eb5-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="87eb5-196">Scegliere l'azione **Rilascia**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="87eb5-197">Gianni procede al prelievo e alla spedizione degli articoli venduti.</span><span class="sxs-lookup"><span data-stu-id="87eb5-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="87eb5-198">Prelievo e spedizione articoli</span><span class="sxs-lookup"><span data-stu-id="87eb5-198">Picking and Shipping Items</span></span>

<span data-ttu-id="87eb5-199">Nella pagina **Prelievo magazzino** è possibile gestire tutte le attività di warehouse in uscita per un documento origine specifico, ad esempio un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="87eb5-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="87eb5-200">Per prelevare gli articoli e procedere alla spedizione</span><span class="sxs-lookup"><span data-stu-id="87eb5-200">To pick and ship items</span></span>

1. <span data-ttu-id="87eb5-201">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prelievi magazzino** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87eb5-202">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="87eb5-203">Assicurarsi che il campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="87eb5-203">Make sure that the **No.**</span></span> <span data-ttu-id="87eb5-204">della Scheda dettaglio **Generale** sia compilato.</span><span class="sxs-lookup"><span data-stu-id="87eb5-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="87eb5-205">Selezionare il campo **Documento origine**, quindi selezionare **Ordine vendita**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-205">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="87eb5-206">Selezionare il campo **Nr. origine**, selezionare la riga per la vendita al cliente 10000 e fare clic sul pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="87eb5-207">In alternativa, scegliere l'azione **Prendi documento origine**, quindi selezionare l'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="87eb5-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="87eb5-208">Scegliere l'azione **Autocompil. qtà da gestire**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="87eb5-209">In alternativa, nel campo **Qtà da gestire** immettere 10 e 20 rispettivamente nelle due righe di prelievo magazzino.</span><span class="sxs-lookup"><span data-stu-id="87eb5-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="87eb5-210">Scegliere l'azione **Registra**, selezionare **Spedizione**, quindi scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="87eb5-210">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="87eb5-211">I 30 altoparlanti ora sono registrati come prelevati dalle collocazioni S-01-0001 e S-01-0002 e viene creato un movimento contabile articolo negativo che riflette la spedizione di vendita registrata.</span><span class="sxs-lookup"><span data-stu-id="87eb5-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87eb5-212">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87eb5-212">See Also</span></span>

[<span data-ttu-id="87eb5-213">Prelevare articoli con prelievi magazzino</span><span class="sxs-lookup"><span data-stu-id="87eb5-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="87eb5-214">Prelevare articoli per la spedizione warehouse</span><span class="sxs-lookup"><span data-stu-id="87eb5-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="87eb5-215">Impostare le warehouse di base con aree di operazioni</span><span class="sxs-lookup"><span data-stu-id="87eb5-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="87eb5-216">Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base</span><span class="sxs-lookup"><span data-stu-id="87eb5-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="87eb5-217">Prelevare per la produzione o l'assemblaggio</span><span class="sxs-lookup"><span data-stu-id="87eb5-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="87eb5-218">Spostare articoli ad hoc nelle configurazioni della warehouse di base</span><span class="sxs-lookup"><span data-stu-id="87eb5-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="87eb5-219">Dettagli di progettazione: Flusso warehouse in uscita</span><span class="sxs-lookup"><span data-stu-id="87eb5-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="87eb5-220">Procedure dettagliate per i processi aziendali</span><span class="sxs-lookup"><span data-stu-id="87eb5-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="87eb5-221">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87eb5-221">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]