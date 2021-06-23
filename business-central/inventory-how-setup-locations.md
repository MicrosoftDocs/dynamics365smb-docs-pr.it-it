---
title: Impostare una scheda Ubicazione e definire i percorsi di trasferimento
description: È possibile creare una scheda ubicazione per ogni area in cui vengono immagazzinati gli articoli in magazzino, ad esempio warehouse o centro di distribuzione, per impostare percorsi per il trasferimento degli articoli tra le ubicazioni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184326"
---
# <a name="set-up-locations"></a><span data-ttu-id="d71e2-103">Impostare le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="d71e2-103">Set Up Locations</span></span>

<span data-ttu-id="d71e2-104">Se si acquista, immagazzina o si vendono articoli in più aree o warehouse, è necessario impostare ogni ubicazione con una scheda ubicazione e definire i percorsi di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="d71e2-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="d71e2-105">[!INCLUDE [prod_short](includes/prod_short.md)] utilizza le ubicazioni per tenere traccia dell'inventario sia nei casi più semplici che nei processi di magazzino più complessi.</span><span class="sxs-lookup"><span data-stu-id="d71e2-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="d71e2-106">È quindi possibile creare le righe del documento per una specifica ubicazione, visualizzare la disponibilità per ubicazione e trasferire il magazzino tra le ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="d71e2-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="d71e2-107">Per ulteriori informazioni, vedere [Gestire il magazzino](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="d71e2-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="d71e2-108">Schede Ubicazione</span><span class="sxs-lookup"><span data-stu-id="d71e2-108">Location cards</span></span>

<span data-ttu-id="d71e2-109">La scheda Ubicazione specifica le informazioni su un'ubicazione, ad esempio un warehouse o un centro di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d71e2-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="d71e2-110">A ogni ubicazione vengono assegnati un nome e un codice che la rappresenta.</span><span class="sxs-lookup"><span data-stu-id="d71e2-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="d71e2-111">Quando si desidera registrare le transazioni per una determinata ubicazione, è possibile immettere il codice ubicazione in altre aree del programma.</span><span class="sxs-lookup"><span data-stu-id="d71e2-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="d71e2-112">È possibile immettere informazioni sui criteri di logistica warehouse per ogni ubicazione.</span><span class="sxs-lookup"><span data-stu-id="d71e2-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="d71e2-113">In base ai criteri di logistica warehouse selezionati, sarà possibile utilizzare le opzioni della Scheda dettaglio **Collocazioni** per definire le collocazioni di default che verranno utilizzate durante l'esecuzione delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="d71e2-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="d71e2-114">Se è previsto l'utilizzo di stoccaggi e prelievi guidati, utilizzare la maggior parte delle opzioni della Scheda dettaglio **Criteri per collocazione** per definire le modalità di utilizzo delle varie funzioni di logistica avanzate.</span><span class="sxs-lookup"><span data-stu-id="d71e2-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="d71e2-115">Alcuni campi opzione sono visualizzati in grigio e disabilitati da altre impostazioni nella pagina **Scheda Ubicazione** per limitare le combinazioni di setup non supportate.</span><span class="sxs-lookup"><span data-stu-id="d71e2-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="d71e2-116">Selezionare l'azione **Zone** o **Collocazioni** per visualizzare le informazioni relative a zone e collocazioni che possono essere definite per l'ubicazione.</span><span class="sxs-lookup"><span data-stu-id="d71e2-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="d71e2-117">Per creare una nuova scheda Ubicazione</span><span class="sxs-lookup"><span data-stu-id="d71e2-117">To create a location card</span></span>

1. <span data-ttu-id="d71e2-118">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d71e2-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="d71e2-119">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="d71e2-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="d71e2-120">Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="d71e2-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="d71e2-121">Ripetere i passaggi 2 e 3 per ogni ubicazione in cui si desidera mantenere il magazzino.</span><span class="sxs-lookup"><span data-stu-id="d71e2-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="d71e2-122">Molti campi della scheda ubicazione fanno riferimento alla gestione degli articoli nei processi della warehouse in entrata e in uscita.</span><span class="sxs-lookup"><span data-stu-id="d71e2-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="d71e2-123">I campi non sono rilevanti per le aziende che non richiedono la funzionalità di magazzino più complessa.</span><span class="sxs-lookup"><span data-stu-id="d71e2-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="d71e2-124">Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d71e2-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="d71e2-125">È possibile modificare la configurazione di un'ubicazione in un secondo momento, ma non è possibile modificare l'impostazione delle ubicazioni con movimenti contabili articoli.</span><span class="sxs-lookup"><span data-stu-id="d71e2-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="d71e2-126">Successivamente, se disponi di più sedi, puoi definire percorsi di trasferimento tra le sedi.</span><span class="sxs-lookup"><span data-stu-id="d71e2-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="d71e2-127">Per creare i percorsi di trasferimento</span><span class="sxs-lookup"><span data-stu-id="d71e2-127">To create a transfer route</span></span>

1. <span data-ttu-id="d71e2-128">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Percorsi di trasferimento** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d71e2-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="d71e2-129">In alternativa, da una qualsiasi pagina **Scheda Ubicazione** scegliere l'azione **Percorsi trasferimento**.</span><span class="sxs-lookup"><span data-stu-id="d71e2-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="d71e2-130">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="d71e2-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="d71e2-131">Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="d71e2-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="d71e2-132">A questo punto è possibile trasferire agli articoli di magazzino tra due ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="d71e2-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="d71e2-133">Per ulteriori informazioni, vedere [Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="d71e2-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="d71e2-134">Collocazioni</span><span class="sxs-lookup"><span data-stu-id="d71e2-134">Bins</span></span>

<span data-ttu-id="d71e2-135">Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli.</span><span class="sxs-lookup"><span data-stu-id="d71e2-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="d71e2-136">Dopo avere creato le collocazioni desiderate, è possibile definire precisamente il contenuto che si desidera includere in ciascuna collocazione. In alternativa, è possibile utilizzare la collocazione come collocazione variabile, ovvero priva di contenuto specifico.</span><span class="sxs-lookup"><span data-stu-id="d71e2-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="d71e2-137">Le collocazioni vengono utilizzate principalmente nelle operazioni di magazzino di base e anticipate.</span><span class="sxs-lookup"><span data-stu-id="d71e2-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="d71e2-138">Se gestisci l'inventario in una configurazione più semplice, probabilmente non hai bisogno di collocazioni.</span><span class="sxs-lookup"><span data-stu-id="d71e2-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="d71e2-139">Per utilizzare la funzionalità di collocazione in una ubicazione, devi prima attivare la funzionalità sulla scheda **Ubicazione** selezionando il campo **Collocazione obbligatoria** sulla Scheda dettaglio **Warehouse**.</span><span class="sxs-lookup"><span data-stu-id="d71e2-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="d71e2-140">Si progetterà quindi il flusso degli articoli nell'ubicazione specificando i codici di collocazione nei campi di setup che rappresentano i diversi flussi.</span><span class="sxs-lookup"><span data-stu-id="d71e2-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="d71e2-141">Prima di poter specificare i codici di collocazione nella scheda Ubicazione, è necessario creare i codici di collocazione.</span><span class="sxs-lookup"><span data-stu-id="d71e2-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="d71e2-142">Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md) e [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="d71e2-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="d71e2-143">Zone</span><span class="sxs-lookup"><span data-stu-id="d71e2-143">Zones</span></span>

<span data-ttu-id="d71e2-144">Se vuoi strutturare le tue collocazioni in zone, puoi farlo nella pagina **Zone**.</span><span class="sxs-lookup"><span data-stu-id="d71e2-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="d71e2-145">[!INCLUDE [prod_short](includes/prod_short.md)] copia i campi impostati per una determinata zona nelle collocazioni all'interno della zona in questione.</span><span class="sxs-lookup"><span data-stu-id="d71e2-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="d71e2-146">In questo modo sarà quindi possibile assegnare una zona a una collocazione o a una definizione di collocazione (filtro per la creazione delle collocazioni), e diversi altri campi verranno compilati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d71e2-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="d71e2-147">Tuttavia, è possibile scegliere di impostare una singola zona e organizzare la warehouse solo in base alle collocazioni.</span><span class="sxs-lookup"><span data-stu-id="d71e2-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="d71e2-148">Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d71e2-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d71e2-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d71e2-149">See Also</span></span>

[<span data-ttu-id="d71e2-150">Gestire i costi del magazzino</span><span class="sxs-lookup"><span data-stu-id="d71e2-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d71e2-151">Trasferire il magazzino tra le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="d71e2-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="d71e2-152">Creare collocazioni</span><span class="sxs-lookup"><span data-stu-id="d71e2-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="d71e2-153">Impostare i tipi di collocazioni</span><span class="sxs-lookup"><span data-stu-id="d71e2-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="d71e2-154">Impostazione gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="d71e2-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="d71e2-155">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d71e2-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d71e2-156">Modifica delle funzionalità visualizzate</span><span class="sxs-lookup"><span data-stu-id="d71e2-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="d71e2-157">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="d71e2-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]