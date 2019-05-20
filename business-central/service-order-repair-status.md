---
title: Impostare gli stati per gli ordini di assistenza e le riparazioni | Documenti Microsoft
description: È necessario impostare nove opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 64afbccba0573445902efdaf3c3919dacdb40e8c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250574"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="93703-103">Come impostare gli stati per gli ordini di assistenza e le riparazioni</span><span class="sxs-lookup"><span data-stu-id="93703-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="93703-104">È necessario impostare opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza.</span><span class="sxs-lookup"><span data-stu-id="93703-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="93703-105">È necessario impostare almeno nove opzioni di stato di riparazione che indichino le situazioni o le azioni intraprese durante le operazioni di assistenza effettuate sull'articolo.</span><span class="sxs-lookup"><span data-stu-id="93703-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="93703-106">È possibile impostare il livello di priorità per le opzioni relative allo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="93703-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="93703-107">Esistono quattro livelli di priorità: Alta, Medio Alta, Medio Bassa, Bassa.</span><span class="sxs-lookup"><span data-stu-id="93703-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  

<span data-ttu-id="93703-108">Ogni volta che si modifica lo stato di riparazione di un articolo in assistenza in un ordine di assistenza, lo stato dell'ordine di assistenza viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="93703-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="93703-109">Lo stato di riparazione di ogni articolo in assistenza è collegato allo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="93703-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="93703-110">Se gli articoli in assistenza sono collegati a due o più opzioni di stato dell'ordine di assistenza, viene selezionato lo stato dell'ordine con la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="93703-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="93703-111">Per impostare uno stato di riparazione</span><span class="sxs-lookup"><span data-stu-id="93703-111">To set up a repair status</span></span>  
1. <span data-ttu-id="93703-112">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stato riparazione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="93703-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="93703-113">Creare un nuovo stato di riparazione.</span><span class="sxs-lookup"><span data-stu-id="93703-113">Create a new repair status.</span></span>  
3. <span data-ttu-id="93703-114">Compilare i campi **Codice** e **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="93703-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="93703-115">Nel campo **Stato ordine assistenza** selezionare lo stato dell'ordine a cui collegare lo stato della riparazione.</span><span class="sxs-lookup"><span data-stu-id="93703-115">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="93703-116">Nel campo **Priorità** viene visualizzata la priorità corrispondente allo stato dell'ordine di assistenza scelto.</span><span class="sxs-lookup"><span data-stu-id="93703-116">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="93703-117">Scegliere lo stato di riparazione.</span><span class="sxs-lookup"><span data-stu-id="93703-117">Choose a repair status.</span></span> <span data-ttu-id="93703-118">È possibile sceglierne uno solo.</span><span class="sxs-lookup"><span data-stu-id="93703-118">You can choose only one.</span></span>  
6. <span data-ttu-id="93703-119">Per poter registrare ordini di assistenza, inclusi articoli in assistenza, con questo stato di riparazione, scegliere il campo **Registrazione permessa**.</span><span class="sxs-lookup"><span data-stu-id="93703-119">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="93703-120">Per modificare manualmente l'opzione di stato dell'ordine di assistenza in **Non iniziato** negli ordini che contengono articoli in assistenza con questo stato di riparazione, selezionare la casella di controllo **Stato Non iniziato abilitato**.</span><span class="sxs-lookup"><span data-stu-id="93703-120">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="93703-121">Analogamente, selezionare le caselle di controllo **Stato In Corso abilitato**, **Stato Completato abilitato** e **Stato In attesa abilitato**.</span><span class="sxs-lookup"><span data-stu-id="93703-121">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="93703-122">Per impostare le priorità di stato di assistenza</span><span class="sxs-lookup"><span data-stu-id="93703-122">To set up service status priorities</span></span>  
1. <span data-ttu-id="93703-123">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stato ordine assistenza** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="93703-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93703-124">Selezionare lo stato dell'ordine di assistenza per cui si desidera impostare una priorità.</span><span class="sxs-lookup"><span data-stu-id="93703-124">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="93703-125">Nel campo **Priorità** scegliere la priorità che si desidera assegnare a questo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="93703-125">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="93703-126">Ripetere questo passaggio per ogni stato.</span><span class="sxs-lookup"><span data-stu-id="93703-126">Repeat this step for each status.</span></span>  

## <a name="see-also"></a><span data-ttu-id="93703-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93703-127">See Also</span></span>  
[<span data-ttu-id="93703-128">Stato ordine assistenza e stato riparazione</span><span class="sxs-lookup"><span data-stu-id="93703-128">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="93703-129">Impostazione della gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="93703-129">Setting Up Service Management</span></span>](service-setup-service.md)  
