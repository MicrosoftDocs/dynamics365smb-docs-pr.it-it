---
title: Stato ordine assistenza e stato riparazione
description: Il campo Stato nella pagina Ordine assistenza e lo stato di riparazione dell'ordine assistenza, rappresentato dal campo Codice stato riparazione nella pagina Ordine assistenza, sono correlati in Gestione assistenza. Lo stato dell'ordine assistenza corrisponde allo stato di riparazione degli articoli in assistenza nell'ordine assistenza.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08fba6795f288e21c0de457a70ff7fa32e7c2822
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770665"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="5c8e1-104">Stato ordine assistenza e stato riparazione</span><span class="sxs-lookup"><span data-stu-id="5c8e1-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="5c8e1-105">Il campo **Stato** nella pagina **Ordine assistenza** e lo stato di riparazione dell'ordine assistenza, rappresentato dal campo **Codice stato riparazione** nella pagina **Ordine assistenza**, sono correlati in Gestione assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="5c8e1-106">Lo stato dell'ordine assistenza corrisponde allo stato di riparazione degli articoli in assistenza nell'ordine assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="5c8e1-107">I due campi relativi allo stato non sono correlati al campo **Stato rilascio** nella testata dell'ordine assistenza, che determina la gestione della warehouse degli articoli in assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="5c8e1-108">Ogni volta che si modifica lo stato di riparazione di un articolo in assistenza in un ordine assistenza, lo stato dell'ordine viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="5c8e1-109">Affinché lo stato visualizzato corrisponda allo stato generale di riparazione dei singoli articoli in assistenza, occorre specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="5c8e1-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="5c8e1-110">lo stato dell'ordine assistenza a cui è collegata ogni stato di riparazione;</span><span class="sxs-lookup"><span data-stu-id="5c8e1-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="5c8e1-111">il livello di priorità di ogni opzione dell'ordine assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="5c8e1-112">Quando un'offerta di assistenza viene convertita in ordine assistenza, lo stato di riparazione di ogni articolo in assistenza viene convertito in **Iniziale** nell'ordine, mentre lo stato dell'ordine assistenza diventa **Non iniziato**.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c8e1-113">Prima di poter creare ordini assistenza, è necessario impostare gli stati di riparazione e le priorità dello stato di assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="5c8e1-114">Per ulteriori informazioni, vedere [Impostare gli stati per gli ordini di assistenza e le riparazioni](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="5c8e1-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="5c8e1-115">Indicazione dello stato dell'ordine assistenza per lo stato di riparazione</span><span class="sxs-lookup"><span data-stu-id="5c8e1-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="5c8e1-116">Ogni stato di riparazione è collegato a un particolare stato dell'ordine assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="5c8e1-117">Le opzioni per lo stato dell'ordine assistenza sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c8e1-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="5c8e1-118">**In sospeso**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-118">**Pending**</span></span>
* <span data-ttu-id="5c8e1-119">**In corso**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-119">**In Process**</span></span>
* <span data-ttu-id="5c8e1-120">**In sospeso**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-120">**On Hold**</span></span>
* <span data-ttu-id="5c8e1-121">**Completato**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-121">**Finished**</span></span>

<span data-ttu-id="5c8e1-122">Le opzioni dello stato di riparazione sono:</span><span class="sxs-lookup"><span data-stu-id="5c8e1-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="5c8e1-123">**Iniziale**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-123">**Initial**</span></span>
* <span data-ttu-id="5c8e1-124">**In corso**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-124">**In Process**</span></span>
* <span data-ttu-id="5c8e1-125">**Demandato**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-125">**Referred**</span></span>
* <span data-ttu-id="5c8e1-126">**Parzialmente assistito**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-126">**Partly Serviced**</span></span>
* <span data-ttu-id="5c8e1-127">**Offerta completata**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-127">**Quote Finished**</span></span>
* <span data-ttu-id="5c8e1-128">**In attesa del cliente**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="5c8e1-129">**Pezzo di ricambio ordinato**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="5c8e1-130">**Pezzo di ricambio ricevuto**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-130">**Spare Part Received**</span></span>
* <span data-ttu-id="5c8e1-131">**Completato**</span><span class="sxs-lookup"><span data-stu-id="5c8e1-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="5c8e1-132">In sospeso</span><span class="sxs-lookup"><span data-stu-id="5c8e1-132">Pending</span></span>

<span data-ttu-id="5c8e1-133">Lo stato dell'ordine assistenza **Non iniziato** indica che l'assistenza può iniziare o continuare in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="5c8e1-134">Le opzioni dello stato di riparazione **Iniziale**, **Demandato**, **Parzialmente assistito** e **Pezzo di ricambio ricevuto** possono quindi essere collegate a questo stato dell'ordine assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="5c8e1-135">In Corso</span><span class="sxs-lookup"><span data-stu-id="5c8e1-135">In Process</span></span>

<span data-ttu-id="5c8e1-136">Lo stato dell'ordine assistenza **In corso** indica che l'assistenza è in atto.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="5c8e1-137">Le opzioni dello stato di riparazione **In corso** e **Pezzo di ricambio ordinato** possono quindi essere collegate a questo stato dell'ordine assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="5c8e1-138">Se lo stato **Pezzo di ricambio ordinato** viene collegato allo stato dell'ordine assistenza **In corso**, a questo stato occorre collegare anche lo stato **Pezzo di ricambio ricevuto**.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="5c8e1-139">Fermo</span><span class="sxs-lookup"><span data-stu-id="5c8e1-139">On Hold</span></span>

<span data-ttu-id="5c8e1-140">Lo stato dell'ordine assistenza **In sospeso** indica che l'assistenza è temporaneamente interrotta perché si sta aspettando una risposta dal cliente o delle parti di ricambio per iniziare l'assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="5c8e1-141">Le opzioni dello stato di riparazione **Offerta completata**, **Pezzo di ricambio ordinato** e **In attesa del cliente** possono essere collegate a questo stato dell'ordine assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="5c8e1-142">Completato</span><span class="sxs-lookup"><span data-stu-id="5c8e1-142">Finished</span></span>

<span data-ttu-id="5c8e1-143">Lo stato dell'ordine assistenza **Completato** indica che l'assistenza è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="5c8e1-144">Lo stato di riparazione **Completato** viene quindi collegato a questo stato.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="5c8e1-145">Assegnazione di priorità allo stato dell'ordine assistenza</span><span class="sxs-lookup"><span data-stu-id="5c8e1-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="5c8e1-146">Quando lo stato di riparazione di un articolo in assistenza viene modificato, vengono individuate le opzioni di stato dell'ordine assistenza collegate alle diverse opzioni dello stato di riparazione di tutti gli articoli in assistenza nell'ordine.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="5c8e1-147">Se gli articoli in assistenza sono collegati a due o più opzioni di stato dell'ordine assistenza, viene selezionata l'opzione relativa allo stato dell'ordine con la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="5c8e1-148">Occorre decidere quale stato contiene le informazioni più importanti per assegnargli quindi la priorità più alta, e così via.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="5c8e1-149">Quindi, quando si crea un nuovo ordine assistenza e si aggiungono articoli in assistenza, il campo **Priorità** nell'intestazione dell'ordine assistenza viene aggiornato in base alle priorità negli articoli in assistenza.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="5c8e1-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c8e1-150">Example</span></span>

<span data-ttu-id="5c8e1-151">Una tipica assegnazione del livello di priorità potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="5c8e1-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="5c8e1-152">In Corso - Alta</span><span class="sxs-lookup"><span data-stu-id="5c8e1-152">In Process - High</span></span>  
* <span data-ttu-id="5c8e1-153">Non iniziato - Medio alta</span><span class="sxs-lookup"><span data-stu-id="5c8e1-153">Pending - Medium high</span></span>  
* <span data-ttu-id="5c8e1-154">In sospeso - Medio bassa</span><span class="sxs-lookup"><span data-stu-id="5c8e1-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="5c8e1-155">Completato - Bassa</span><span class="sxs-lookup"><span data-stu-id="5c8e1-155">Finished - Low</span></span>  

<span data-ttu-id="5c8e1-156">Se ad esempio un articolo in assistenza ha lo stato di riparazione **Iniziale**, collegato allo stato dell'ordine assistenza **Non iniziato**, un altro è **In corso**, collegato allo stato **In corso** e a un terzo corrisponde lo stato **Pezzo di ricambio ordinato**, collegato allo stato **In sospeso**, lo stato che ne risulterà sarà **In corso**, in quanto ha la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="5c8e1-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5c8e1-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c8e1-157">See Also</span></span>

[<span data-ttu-id="5c8e1-158">Impostare gli stati per gli ordini di assistenza e le riparazioni</span><span class="sxs-lookup"><span data-stu-id="5c8e1-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="5c8e1-159">Impostazione della gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="5c8e1-159">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]