---
title: Impostare gli stati per gli ordini di assistenza e le riparazioni | Documenti Microsoft
description: È necessario impostare nove opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 4c28fcfbc2cbc7493ba183812383225754fd3dfa
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389651"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="878af-103">Come impostare gli stati per gli ordini di assistenza e le riparazioni</span><span class="sxs-lookup"><span data-stu-id="878af-103">Set Up Statuses for Service Orders and Repairs</span></span>

<span data-ttu-id="878af-104">È necessario impostare opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza.</span><span class="sxs-lookup"><span data-stu-id="878af-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="878af-105">È necessario impostare almeno nove opzioni di stato di riparazione che indichino le situazioni o le azioni intraprese durante le operazioni di assistenza effettuate sull'articolo.</span><span class="sxs-lookup"><span data-stu-id="878af-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="878af-106">È possibile impostare il livello di priorità per le opzioni relative allo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="878af-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="878af-107">Le quattro priorità sono **Alta**, **Medio Alta**, **Medio Bassa** e **Bassa**.</span><span class="sxs-lookup"><span data-stu-id="878af-107">The four priorities are **High**, **Medium High**, **Medium Low**, and **Low**.</span></span>  

<span data-ttu-id="878af-108">Ogni volta che si modifica lo stato di riparazione di un articolo in assistenza in un ordine di assistenza, lo stato dell'ordine di assistenza viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="878af-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="878af-109">Lo stato di riparazione di ogni articolo in assistenza è collegato allo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="878af-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="878af-110">Se gli articoli in assistenza sono collegati a due o più opzioni di stato dell'ordine di assistenza, viene selezionato lo stato dell'ordine con la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="878af-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

<span data-ttu-id="878af-111">Prima di poter impostare uno stato di riparazione, è necessario impostare le priorità dello stato di assistenza.</span><span class="sxs-lookup"><span data-stu-id="878af-111">Before you can set up a repair status, you must set up service status priorities.</span></span>

## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="878af-112">Per impostare le priorità di stato di assistenza</span><span class="sxs-lookup"><span data-stu-id="878af-112">To set up service status priorities</span></span>

1. <span data-ttu-id="878af-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stato ordine assistenza** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="878af-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="878af-114">Selezionare lo stato dell'ordine di assistenza per cui si desidera impostare una priorità.</span><span class="sxs-lookup"><span data-stu-id="878af-114">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="878af-115">Nel campo **Priorità** scegliere la priorità che si desidera assegnare a questo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="878af-115">In the **Priority** field, choose the priority you want for this service order status.</span></span>  

<span data-ttu-id="878af-116">Ripetere i passaggi 2 e 3 per impostare la priorità per ciascuna delle quattro opzioni di stato, ovvero **Non iniziato**, **In corso**, **Completato** e **In attesa**.</span><span class="sxs-lookup"><span data-stu-id="878af-116">Repeat steps 2 and 3 until you have set the priority for each of the four status options: **Pending**, **In Process**, **Finished**, and **On Hold**.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="878af-117">Per impostare uno stato di riparazione</span><span class="sxs-lookup"><span data-stu-id="878af-117">To set up a repair status</span></span>

1. <span data-ttu-id="878af-118">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stato riparazione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="878af-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="878af-119">Creare un nuovo stato di riparazione.</span><span class="sxs-lookup"><span data-stu-id="878af-119">Create a new repair status.</span></span>  
3. <span data-ttu-id="878af-120">Compilare i campi **Codice** e **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="878af-120">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="878af-121">Nel campo **Stato ordine assistenza** selezionare lo stato dell'ordine a cui collegare lo stato della riparazione.</span><span class="sxs-lookup"><span data-stu-id="878af-121">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="878af-122">Nel campo **Priorità** viene visualizzata la priorità corrispondente allo stato dell'ordine di assistenza scelto.</span><span class="sxs-lookup"><span data-stu-id="878af-122">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="878af-123">Scegliere lo stato di riparazione.</span><span class="sxs-lookup"><span data-stu-id="878af-123">Choose a repair status.</span></span> <span data-ttu-id="878af-124">È possibile sceglierne uno solo.</span><span class="sxs-lookup"><span data-stu-id="878af-124">You can choose only one.</span></span> <span data-ttu-id="878af-125">Lo stato di riparazione non può essere collegato a più di una opzione di stato di riparazione.</span><span class="sxs-lookup"><span data-stu-id="878af-125">A repair status cannot be linked more than one repair status option.</span></span>  
6. <span data-ttu-id="878af-126">Per poter registrare ordini di assistenza, inclusi articoli in assistenza, con questo stato di riparazione, scegliere il campo **Registrazione permessa**.</span><span class="sxs-lookup"><span data-stu-id="878af-126">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="878af-127">Per modificare manualmente l'opzione di stato dell'ordine di assistenza in **Non iniziato** negli ordini che contengono articoli in assistenza con questo stato di riparazione, selezionare la casella di controllo **Stato Non iniziato abilitato**.</span><span class="sxs-lookup"><span data-stu-id="878af-127">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="878af-128">Analogamente, selezionare le caselle di controllo **Stato In Corso abilitato**, **Stato Completato abilitato** e **Stato In attesa abilitato**.</span><span class="sxs-lookup"><span data-stu-id="878af-128">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>

<span data-ttu-id="878af-129">Ripetere i passaggi indicati per ogni opzione dello stato di riparazione che si intende creare.</span><span class="sxs-lookup"><span data-stu-id="878af-129">Repeat these steps for each of the repair status options you want to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="878af-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="878af-130">See Also</span></span>

[<span data-ttu-id="878af-131">Stato ordine assistenza e stato riparazione</span><span class="sxs-lookup"><span data-stu-id="878af-131">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="878af-132">Impostazione della gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="878af-132">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]