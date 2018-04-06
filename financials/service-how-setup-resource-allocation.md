---
title: Impostare l'assegnazione delle risorse | Documenti Microsoft
description: "Informazioni su come il sistema può aiutare a garantire che l'assegnazione venga fatta a chi ha le competenze necessarie per fornire a un servizio di assistenza."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b16ba9366aefc108f39667678fe8ab70ce421b83
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-resource-allocation"></a><span data-ttu-id="d965d-103">Impostare l'assegnazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="d965d-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="d965d-104">Per assicurarsi che un compito di assistenza sia eseguito correttamente, è importante trovare una risorsa qualificata per il lavoro.</span><span class="sxs-lookup"><span data-stu-id="d965d-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="d965d-105">È possibile configurare [!INCLUDE[d365fin](includes/d365fin_md.md)] di modo che sia semplice assegnare una risorsa che disponga delle competenze necessarie per il compito.</span><span class="sxs-lookup"><span data-stu-id="d965d-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="d965d-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)] questa funzionalità è detta _assegnazione delle risorse_.</span><span class="sxs-lookup"><span data-stu-id="d965d-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="d965d-107">È possibile assegnare le risorse in base alla loro competenza, disponibilità o se si trovano nella stessa zona di assistenza del cliente.</span><span class="sxs-lookup"><span data-stu-id="d965d-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="d965d-108">Per utilizzare l'assegnazione delle risorse, è necessario impostare:</span><span class="sxs-lookup"><span data-stu-id="d965d-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="d965d-109">Le competenze necessarie per riparare e gestire gli articoli in assistenza.</span><span class="sxs-lookup"><span data-stu-id="d965d-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="d965d-110">Queste devono essere assegnate agli articoli in assistenza e alle risorse.</span><span class="sxs-lookup"><span data-stu-id="d965d-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="d965d-111">Le aree geografiche, chiamate zone, definite per il proprio mercato.</span><span class="sxs-lookup"><span data-stu-id="d965d-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="d965d-112">Ad esempio, Est, Ovest, Centro e così via.</span><span class="sxs-lookup"><span data-stu-id="d965d-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="d965d-113">Queste devono essere assegnate ai clienti e alle risorse.</span><span class="sxs-lookup"><span data-stu-id="d965d-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="d965d-114">Scegliere se visualizzare le zone e le competenze delle risorse e se visualizzare un avviso quando qualcuno sceglie una risorsa non qualificata o che non si trova nella zona cliente.</span><span class="sxs-lookup"><span data-stu-id="d965d-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="d965d-115">Per impostare le competenze</span><span class="sxs-lookup"><span data-stu-id="d965d-115">To set up skills</span></span>
1. <span data-ttu-id="d965d-116">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Competenze**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d965d-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d965d-117">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="d965d-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="d965d-118">Per assegnare le competenze agli articoli in assistenza e alle risorse</span><span class="sxs-lookup"><span data-stu-id="d965d-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="d965d-119">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report") , immettere **Articoli in assistenza** o **Risorse** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d965d-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d965d-120">Aprire la scheda relativa all'articolo in assistenza o alla risorsa, quindi scegliere una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="d965d-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="d965d-121">Per gli articoli in assistenza, scegliere **Competenze risorse**.</span><span class="sxs-lookup"><span data-stu-id="d965d-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="d965d-122">Per le risorse, scegliere **Competenze**.</span><span class="sxs-lookup"><span data-stu-id="d965d-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="d965d-123">Per impostare le zone</span><span class="sxs-lookup"><span data-stu-id="d965d-123">To set up zones</span></span>
1. <span data-ttu-id="d965d-124">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Zone**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d965d-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d965d-125">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="d965d-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="d965d-126">Per assegnare le zone ai clienti e alle risorse</span><span class="sxs-lookup"><span data-stu-id="d965d-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="d965d-127">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report") , immettere **Clienti** o **Risorse** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d965d-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d965d-128">Aprire la scheda relativa all'articolo in assistenza o alla risorsa, quindi scegliere una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="d965d-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="d965d-129">Per i clienti, scegliere una zona nel campo **Codice zona di assistenza**.</span><span class="sxs-lookup"><span data-stu-id="d965d-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="d965d-130">Per le risorse, scegliere l'azione **Zone assistenza**.</span><span class="sxs-lookup"><span data-stu-id="d965d-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="d965d-131">Per specificare il contenuto da visualizzare quando si sceglie una risorsa</span><span class="sxs-lookup"><span data-stu-id="d965d-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="d965d-132">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup assistenza**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d965d-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="d965d-133">Nel campo **Opzione competenze risorse** scegliere una delle opzioni descritte nella seguente tabella.</span><span class="sxs-lookup"><span data-stu-id="d965d-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="d965d-134">**Opzione**</span><span class="sxs-lookup"><span data-stu-id="d965d-134">**Option**</span></span>|<span data-ttu-id="d965d-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="d965d-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="d965d-136">Mostra codice</span><span class="sxs-lookup"><span data-stu-id="d965d-136">Code Shown</span></span> | <span data-ttu-id="d965d-137">Viene visualizzato solo il codice.</span><span class="sxs-lookup"><span data-stu-id="d965d-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="d965d-138">Warning visualizzato</span><span class="sxs-lookup"><span data-stu-id="d965d-138">Warning Displayed</span></span> | <span data-ttu-id="d965d-139">Le informazioni vengono visualizzate e appare un avviso se si sceglie una risorsa che non è qualificata.</span><span class="sxs-lookup"><span data-stu-id="d965d-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="d965d-140">Non usato</span><span class="sxs-lookup"><span data-stu-id="d965d-140">Not Used</span></span> | <span data-ttu-id="d965d-141">Le informazioni non vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="d965d-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="d965d-142">Per aggiornare la capacità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d965d-142">To update resource capacity</span></span>  
<span data-ttu-id="d965d-143">Potrebbe essere necessario modificare la capacità delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d965d-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="d965d-144">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Capacità risorsa**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d965d-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d965d-145">Scegliere la risorsa, quindi scegliere l'azione **Imposta capacità**.</span><span class="sxs-lookup"><span data-stu-id="d965d-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="d965d-146">Apportare le modifiche, quindi scegliere **Aggiorna capacità**.</span><span class="sxs-lookup"><span data-stu-id="d965d-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="d965d-147">Per aggiornare le competenze per gli articoli, gli articoli in assistenza o i gruppi di articoli in assistenza</span><span class="sxs-lookup"><span data-stu-id="d965d-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="d965d-148">Se si desidera modificare i codici competenza assegnati agli articoli, ad esempio da **PC** a **PCS**, è possibile effettuare questa operazione per un articolo, un articolo in assistenza o per tutti gli articoli in un gruppo di articoli in assistenza.</span><span class="sxs-lookup"><span data-stu-id="d965d-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="d965d-149">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli** o **Articolo in assistenza** o **Gruppo articoli in assistenza**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d965d-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d965d-150">Scegliere l'entità da aggiornare, quindi scegliere l'azione **Competenze risorse**.</span><span class="sxs-lookup"><span data-stu-id="d965d-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="d965d-151">Sulla riga contenente il codice da modificare, nel campo **Codice competenza**, scegliere il codice competenza appropriato.</span><span class="sxs-lookup"><span data-stu-id="d965d-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="d965d-152">Se all'articolo sono associati articoli in assistenza, verrà visualizzata una finestra di dialogo con le due opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d965d-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="d965d-153">Modificare i codici competenze nel valore selezionato: selezionare questa opzione per sostituire il vecchio codice con il nuovo in tutti gli articoli in assistenza correlati.</span><span class="sxs-lookup"><span data-stu-id="d965d-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="d965d-154">Eliminare i codici competenze o aggiornarne la relazione: selezionare questa opzione se si desidera modificare il codice competenza solo per l'articolo selezionato.</span><span class="sxs-lookup"><span data-stu-id="d965d-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="d965d-155">Il codice competenza degli articoli in assistenza correlati verrà riassegnato, ovvero, il campo **Assegnato da** verrà aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d965d-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d965d-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d965d-156">See Also</span></span>
[<span data-ttu-id="d965d-157">Assegnare risorse</span><span class="sxs-lookup"><span data-stu-id="d965d-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="d965d-158">Impostare le ore di lavoro e le ore di assistenza</span><span class="sxs-lookup"><span data-stu-id="d965d-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="d965d-159">Impostare il reporting dei guasti</span><span class="sxs-lookup"><span data-stu-id="d965d-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="d965d-160">Impostare codici per servizi standard</span><span class="sxs-lookup"><span data-stu-id="d965d-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 


