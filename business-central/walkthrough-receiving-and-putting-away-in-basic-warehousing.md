---
title: 'Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base'
description: In Business Central, i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità differenti a seconda del livello di complessità della warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 674b095c515c6c8be5dde41861ab2cfdc943855f
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035558"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="66b97-103">Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base</span><span class="sxs-lookup"><span data-stu-id="66b97-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

<span data-ttu-id="66b97-104">In [!INCLUDE[prod_short](includes/prod_short.md)], i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.</span><span class="sxs-lookup"><span data-stu-id="66b97-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="66b97-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="66b97-105">Method</span></span>|<span data-ttu-id="66b97-106">Processo in entrata</span><span class="sxs-lookup"><span data-stu-id="66b97-106">Inbound process</span></span>|<span data-ttu-id="66b97-107">Collocazioni</span><span class="sxs-lookup"><span data-stu-id="66b97-107">Bins</span></span>|<span data-ttu-id="66b97-108">Carichi</span><span class="sxs-lookup"><span data-stu-id="66b97-108">Receipts</span></span>|<span data-ttu-id="66b97-109">Stoccaggi</span><span class="sxs-lookup"><span data-stu-id="66b97-109">Put-aways</span></span>|<span data-ttu-id="66b97-110">Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="66b97-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="66b97-111">A</span><span class="sxs-lookup"><span data-stu-id="66b97-111">A</span></span>|<span data-ttu-id="66b97-112">Registrare il carico e lo stoccaggio dalla riga ordine</span><span class="sxs-lookup"><span data-stu-id="66b97-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="66b97-113">X</span><span class="sxs-lookup"><span data-stu-id="66b97-113">X</span></span>|||<span data-ttu-id="66b97-114">2</span><span class="sxs-lookup"><span data-stu-id="66b97-114">2</span></span>|  
|<span data-ttu-id="66b97-115">B</span><span class="sxs-lookup"><span data-stu-id="66b97-115">B</span></span>|<span data-ttu-id="66b97-116">Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino</span><span class="sxs-lookup"><span data-stu-id="66b97-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="66b97-117">X</span><span class="sxs-lookup"><span data-stu-id="66b97-117">X</span></span>|<span data-ttu-id="66b97-118">3</span><span class="sxs-lookup"><span data-stu-id="66b97-118">3</span></span>|  
|<span data-ttu-id="66b97-119">C</span><span class="sxs-lookup"><span data-stu-id="66b97-119">C</span></span>|<span data-ttu-id="66b97-120">Registrare il carico e lo stoccaggio da un documento di carico warehouse</span><span class="sxs-lookup"><span data-stu-id="66b97-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="66b97-121">X</span><span class="sxs-lookup"><span data-stu-id="66b97-121">X</span></span>||<span data-ttu-id="66b97-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="66b97-122">4/5/6</span></span>|  
|<span data-ttu-id="66b97-123">D</span><span class="sxs-lookup"><span data-stu-id="66b97-123">D</span></span>|<span data-ttu-id="66b97-124">Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse</span><span class="sxs-lookup"><span data-stu-id="66b97-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="66b97-125">X</span><span class="sxs-lookup"><span data-stu-id="66b97-125">X</span></span>|<span data-ttu-id="66b97-126">X</span><span class="sxs-lookup"><span data-stu-id="66b97-126">X</span></span>|<span data-ttu-id="66b97-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="66b97-127">4/5/6</span></span>|  

<span data-ttu-id="66b97-128">Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="66b97-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="66b97-129">Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="66b97-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="66b97-130">Informazioni sulla procedura dettagliata</span><span class="sxs-lookup"><span data-stu-id="66b97-130">About This Walkthrough</span></span>  
<span data-ttu-id="66b97-131">Nelle configurazioni di warehouse di base in cui un'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi ma non l'elaborazione dei carichi, utilizzare la pagina **Stoccaggio in magazzino** per registrare le informazioni riguardanti lo stoccaggio e il carico per i documenti di origine in entrata.</span><span class="sxs-lookup"><span data-stu-id="66b97-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="66b97-132">Il documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata o un ordine di produzione il cui output è pronto per lo stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="66b97-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="66b97-133">Anche se le impostazioni sono definite **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile registrare carichi e spedizioni direttamente dai documenti commerciali di origine nelle ubicazioni in cui si selezionano queste caselle di controllo.</span><span class="sxs-lookup"><span data-stu-id="66b97-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="66b97-134">In questa procedura dettagliata sono illustrati i task seguenti.</span><span class="sxs-lookup"><span data-stu-id="66b97-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="66b97-135">Impostazione ubicazione ARGENTO per gli stoccaggi magazzino.</span><span class="sxs-lookup"><span data-stu-id="66b97-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="66b97-136">Impostazione ubicazione ARGENTO per la gestione della collocazione.</span><span class="sxs-lookup"><span data-stu-id="66b97-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="66b97-137">Definizione di una collocazione di default per l'articolo LS-81.</span><span class="sxs-lookup"><span data-stu-id="66b97-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="66b97-138">(LS-75 è già impostato in CRONUS).</span><span class="sxs-lookup"><span data-stu-id="66b97-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="66b97-139">Creazione di un ordine di acquisto per il fornitore 10000 per 40 altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="66b97-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="66b97-140">Verificare che le collocazioni di stoccaggio siano preimpostate in base all'impostazione.</span><span class="sxs-lookup"><span data-stu-id="66b97-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="66b97-141">Rilascio dell'ordine di acquisto per la gestione warehouse.</span><span class="sxs-lookup"><span data-stu-id="66b97-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="66b97-142">Creazione di uno stoccaggio in magazzino in base al documento origine rilasciato.</span><span class="sxs-lookup"><span data-stu-id="66b97-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="66b97-143">Verificare che le collocazioni di stoccaggio siano ereditate dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="66b97-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="66b97-144">Registrazione della movimentazione warehouse nella warehouse e registrazione contemporanea della ricezione acquisti per l'ordine di acquisto di origine.</span><span class="sxs-lookup"><span data-stu-id="66b97-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a><span data-ttu-id="66b97-145">Ruoli</span><span class="sxs-lookup"><span data-stu-id="66b97-145">Roles</span></span>  
<span data-ttu-id="66b97-146">Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:</span><span class="sxs-lookup"><span data-stu-id="66b97-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="66b97-147">Manager warehouse</span><span class="sxs-lookup"><span data-stu-id="66b97-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="66b97-148">Rivenditore</span><span class="sxs-lookup"><span data-stu-id="66b97-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="66b97-149">Lavoro warehouse</span><span class="sxs-lookup"><span data-stu-id="66b97-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="66b97-150">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="66b97-150">Prerequisites</span></span>  
<span data-ttu-id="66b97-151">Per completare questa procedura dettagliata, sarà necessario:</span><span class="sxs-lookup"><span data-stu-id="66b97-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="66b97-152">CRONUS International Ltd. installato.</span><span class="sxs-lookup"><span data-stu-id="66b97-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="66b97-153">Per diventare un impiegato warehouse presso l'ubicazione ARGENTO, effettuare i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="66b97-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="66b97-154">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="66b97-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="66b97-155">Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.</span><span class="sxs-lookup"><span data-stu-id="66b97-155">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="66b97-156">Nel campo **Codice ubicazione** immettere ARGENTO.</span><span class="sxs-lookup"><span data-stu-id="66b97-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="66b97-157">Selezionare il campo **Default**.</span><span class="sxs-lookup"><span data-stu-id="66b97-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="66b97-158">Scenario</span><span class="sxs-lookup"><span data-stu-id="66b97-158">Story</span></span>  
<span data-ttu-id="66b97-159">Ellen, responsabile warehouse presso CRONUS International Ltd., crea un ordine di acquisto per 10 unità dell'articolo LS-75 e 30 unità dell'articolo LS-81 per il fornitore 10000 che deve essere consegnato alla warehouse ARGENTO.</span><span class="sxs-lookup"><span data-stu-id="66b97-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="66b97-160">Quando la consegna arriva alla warehouse, Gianni, il lavoratore warehouse, esegue lo stoccaggio degli articoli nelle collocazioni di default per gli articoli.</span><span class="sxs-lookup"><span data-stu-id="66b97-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="66b97-161">Quando Gianni registra lo stoccaggio, gli articoli vengono registrati come ricevuti nel magazzino e disponibili alla vendita o a un'altra domanda.</span><span class="sxs-lookup"><span data-stu-id="66b97-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="66b97-162">Impostazione dell'ubicazione</span><span class="sxs-lookup"><span data-stu-id="66b97-162">Setting up the Location</span></span>  
 <span data-ttu-id="66b97-163">L'impostazione della pagina **Scheda Ubicazione** definisce i flussi della warehouse della società.</span><span class="sxs-lookup"><span data-stu-id="66b97-163">The setup of the **Location Card** page defines the company's warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="66b97-164">Per impostare l'ubicazione</span><span class="sxs-lookup"><span data-stu-id="66b97-164">To set up the location</span></span>  

1.  <span data-ttu-id="66b97-165">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="66b97-165">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="66b97-166">Aprire la scheda ubicazione ARGENTO.</span><span class="sxs-lookup"><span data-stu-id="66b97-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="66b97-167">Selezionare la casella di controllo **Richiesto stoccaggio**.</span><span class="sxs-lookup"><span data-stu-id="66b97-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="66b97-168">Impostare una collocazione di default per i due numeri articolo per controllare dove vengono stoccati.</span><span class="sxs-lookup"><span data-stu-id="66b97-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="66b97-169">Scegliere l'azione **Collocazioni**.</span><span class="sxs-lookup"><span data-stu-id="66b97-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="66b97-170">Selezionare la prima riga, per la collocazione S-01-0001, quindi scegliere l'azione **Contenuti**.</span><span class="sxs-lookup"><span data-stu-id="66b97-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="66b97-171">Notare che nella pagina **Contenuto collocazione** l'articolo LS-75 è già impostato come contenuto nella collocazione S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="66b97-171">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="66b97-172">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="66b97-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="66b97-173">Selezionare i campi **Fisso** e **Default**.</span><span class="sxs-lookup"><span data-stu-id="66b97-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="66b97-174">Nel campo **Nr. articolo** immettere LS-81.</span><span class="sxs-lookup"><span data-stu-id="66b97-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="66b97-175">Creazione dell'ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="66b97-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="66b97-176">Gli ordini di acquisto sono il tipo più comune di documenti origine in entrata.</span><span class="sxs-lookup"><span data-stu-id="66b97-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="66b97-177">Per creare l'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="66b97-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="66b97-178">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="66b97-178">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="66b97-179">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="66b97-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="66b97-180">Creare un ordine di acquisto per il fornitore 10000 alla data di lavoro (23 gennaio) con le righe di ordine di acquisto seguenti.</span><span class="sxs-lookup"><span data-stu-id="66b97-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="66b97-181">Articolo</span><span class="sxs-lookup"><span data-stu-id="66b97-181">Item</span></span>|<span data-ttu-id="66b97-182">Cod. ubicazione</span><span class="sxs-lookup"><span data-stu-id="66b97-182">Location code</span></span>|<span data-ttu-id="66b97-183">Codice collocazione</span><span class="sxs-lookup"><span data-stu-id="66b97-183">Bin code</span></span>|<span data-ttu-id="66b97-184">Quantità</span><span class="sxs-lookup"><span data-stu-id="66b97-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="66b97-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="66b97-185">LS_75</span></span>|<span data-ttu-id="66b97-186">ARGENTO</span><span class="sxs-lookup"><span data-stu-id="66b97-186">SILVER</span></span>|<span data-ttu-id="66b97-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="66b97-187">S-01-0001</span></span>|<span data-ttu-id="66b97-188">10</span><span class="sxs-lookup"><span data-stu-id="66b97-188">10</span></span>|  
    |<span data-ttu-id="66b97-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="66b97-189">LS-81</span></span>|<span data-ttu-id="66b97-190">ARGENTO</span><span class="sxs-lookup"><span data-stu-id="66b97-190">SILVER</span></span>|<span data-ttu-id="66b97-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="66b97-191">S-01-0001</span></span>|<span data-ttu-id="66b97-192">30</span><span class="sxs-lookup"><span data-stu-id="66b97-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="66b97-193">Il codice di collocazione viene immesso automaticamente in base al setup eseguito nella sezione "Impostazione dell'ubicazione".</span><span class="sxs-lookup"><span data-stu-id="66b97-193">The bin code is entered automatically according to the setup that you performed in the "Setting up the Location" section.</span></span>  

    <span data-ttu-id="66b97-194">Comunicare alla warehouse che l'ordine di acquisto è pronto per la gestione warehouse al momento della consegna.</span><span class="sxs-lookup"><span data-stu-id="66b97-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="66b97-195">Scegliere l'azione **Rilascia**.</span><span class="sxs-lookup"><span data-stu-id="66b97-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="66b97-196">La consegna degli altoparlanti dal fornitore 10000 è arrivata alla warehouse ARGENTO e Gianni continua lo stoccaggio.</span><span class="sxs-lookup"><span data-stu-id="66b97-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="66b97-197">Ricezione e stoccaggio di articoli</span><span class="sxs-lookup"><span data-stu-id="66b97-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="66b97-198">Nella pagina **Stoccaggio in magazzino** è possibile gestire tutte le attività di warehouse in entrata per un documento origine specifico, ad esempio un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="66b97-198">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="66b97-199">Per ricevere e stoccare gli articoli</span><span class="sxs-lookup"><span data-stu-id="66b97-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="66b97-200">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stoccaggi magazzino** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="66b97-200">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="66b97-201">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="66b97-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="66b97-202">Selezionare il campo **Documento origine**, quindi selezionare **Ordine acquisto**.</span><span class="sxs-lookup"><span data-stu-id="66b97-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="66b97-203">Selezionare il campo **Nr. origine**, selezionare la riga per gli acquisti dal fornitore 10000 e fare clic sul pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="66b97-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="66b97-204">In alternativa, scegliere l'azione **Prendi documento origine**, quindi selezionare l'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="66b97-204">Alternatively, choose the **Get Source Document** action, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="66b97-205">Scegliere l'azione **Autocompil. qtà da gestire**.</span><span class="sxs-lookup"><span data-stu-id="66b97-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="66b97-206">In alternativa, nel campo **Qtà da gestire** immettere 10 e 30 rispettivamente nelle due righe di stoccaggio magazzino.</span><span class="sxs-lookup"><span data-stu-id="66b97-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="66b97-207">Scegliere l'azione **Registra**, selezionare l'azione **Ricevi**, quindi il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="66b97-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="66b97-208">I 40 altoparlanti ora sono registrati come stoccati nella collocazione S-01-0001 e viene creato un movimento contabile articolo positivo che riflette la ricezione acquisti registrata.</span><span class="sxs-lookup"><span data-stu-id="66b97-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="66b97-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66b97-209">See Also</span></span>  
 <span data-ttu-id="66b97-210">[Eseguire lo stoccaggio con Stoccaggi Magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="66b97-210">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="66b97-211">[Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="66b97-211">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="66b97-212">[Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="66b97-212">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="66b97-213">[Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="66b97-213">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="66b97-214">[Spostare articoli ad hoc nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="66b97-214">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="66b97-215">[Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="66b97-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="66b97-216">Procedure dettagliate per i processi aziendali</span><span class="sxs-lookup"><span data-stu-id="66b97-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="66b97-217">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="66b97-217">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
