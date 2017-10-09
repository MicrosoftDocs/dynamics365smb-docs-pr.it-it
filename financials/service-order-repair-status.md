---
title: Impostare gli stati per gli ordini di assistenza e le riparazioni | Documenti Microsoft
description: "È necessario impostare nove opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 36925a08f7fdfffedf13902a5c6feaaa8b0929a4
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="626e2-103">Procedura: Impostare gli stati per gli ordini di assistenza e le riparazioni</span><span class="sxs-lookup"><span data-stu-id="626e2-103">How to: Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="626e2-104">È necessario impostare opzioni relative allo stato della riparazione che indicano lo stato di avanzamento della riparazione e della manutenzione degli articoli in assistenza negli ordini di assistenza.</span><span class="sxs-lookup"><span data-stu-id="626e2-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="626e2-105">È necessario impostare almeno nove opzioni di stato di riparazione che indichino le situazioni o le azioni intraprese durante le operazioni di assistenza effettuate sull'articolo.</span><span class="sxs-lookup"><span data-stu-id="626e2-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="626e2-106">È possibile impostare il livello di priorità per le opzioni relative allo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="626e2-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="626e2-107">Esistono quattro livelli di priorità: Alta, Medio Alta, Medio Bassa, Bassa.</span><span class="sxs-lookup"><span data-stu-id="626e2-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="626e2-108">Ogni volta che si modifica lo stato di riparazione di un articolo in assistenza in un ordine di assistenza, lo stato dell'ordine di assistenza viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="626e2-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="626e2-109">Lo stato di riparazione di ogni articolo in assistenza è collegato allo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="626e2-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="626e2-110">Se gli articoli in assistenza sono collegati a due o più opzioni di stato dell'ordine di assistenza, viene selezionato lo stato dell'ordine con la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="626e2-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="626e2-111">Per impostare uno stato di riparazione</span><span class="sxs-lookup"><span data-stu-id="626e2-111">To set up a repair status</span></span>  
1. <span data-ttu-id="626e2-112">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Stato riparazione**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="626e2-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="626e2-113">2.</span><span class="sxs-lookup"><span data-stu-id="626e2-113">2.</span></span> <span data-ttu-id="626e2-114">Creare un nuovo stato di riparazione.</span><span class="sxs-lookup"><span data-stu-id="626e2-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="626e2-115">Compilare i campi **Codice** e **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="626e2-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="626e2-116">Nel campo **Stato ordine assistenza** selezionare lo stato dell'ordine a cui collegare lo stato della riparazione.</span><span class="sxs-lookup"><span data-stu-id="626e2-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="626e2-117">Nel campo **Priorità** viene visualizzata la priorità corrispondente allo stato dell'ordine di assistenza scelto.</span><span class="sxs-lookup"><span data-stu-id="626e2-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="626e2-118">Scegliere lo stato di riparazione.</span><span class="sxs-lookup"><span data-stu-id="626e2-118">Choose a repair status.</span></span> <span data-ttu-id="626e2-119">È possibile sceglierne uno solo.</span><span class="sxs-lookup"><span data-stu-id="626e2-119">You can choose only one.</span></span>  
6. <span data-ttu-id="626e2-120">Per poter registrare ordini di assistenza, inclusi articoli in assistenza, con questo stato di riparazione, scegliere il campo **Registrazione permessa**.</span><span class="sxs-lookup"><span data-stu-id="626e2-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="626e2-121">Per modificare manualmente l'opzione di stato dell'ordine di assistenza in **Non iniziato** negli ordini che contengono articoli in assistenza con questo stato di riparazione, selezionare la casella di controllo **Stato Non iniziato abilitato**.</span><span class="sxs-lookup"><span data-stu-id="626e2-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="626e2-122">Analogamente, selezionare le caselle di controllo **Stato In Corso abilitato**, **Stato Completato abilitato** e **Stato In attesa abilitato**.</span><span class="sxs-lookup"><span data-stu-id="626e2-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="626e2-123">Per impostare le priorità di stato di assistenza</span><span class="sxs-lookup"><span data-stu-id="626e2-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="626e2-124">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Stato ordine assistenza**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="626e2-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="626e2-125">Selezionare lo stato dell'ordine di assistenza per cui si desidera impostare una priorità.</span><span class="sxs-lookup"><span data-stu-id="626e2-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="626e2-126">Nel campo **Priorità** scegliere la priorità che si desidera assegnare a questo stato dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="626e2-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="626e2-127">Ripetere questo passaggio per ogni stato.</span><span class="sxs-lookup"><span data-stu-id="626e2-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="626e2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="626e2-128">See Also</span></span>  
[<span data-ttu-id="626e2-129">Informazioni su stato ordine assistenza e stato riparazione</span><span class="sxs-lookup"><span data-stu-id="626e2-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="626e2-130">Impostazione della gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="626e2-130">Setting Up Service Management</span></span>](service-setup-service.md)  

