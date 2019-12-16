---
title: 'Procedura: Impostare gli spedizionieri | Documenti Microsoft'
description: È possibile impostare un codice per ciascuno degli spedizionieri di cui si avvale l'azienda e immettere informazioni relative a ognuno di essi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b1c5b0940998531601f0ab1c604c31328ce2bd66
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882856"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="6d2e0-103">Impostare gli spedizionieri</span><span class="sxs-lookup"><span data-stu-id="6d2e0-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="6d2e0-104">È possibile impostare un codice per ciascuno degli spedizionieri di cui si avvale l'azienda e immettere informazioni relative a ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="6d2e0-105">Se viene immesso l'indirizzo Internet di uno spedizioniere che fornisce servizi per rintracciare colli su Internet, è possibile utilizzare la funzione di tracciabilità automatica dei colli.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="6d2e0-106">Per ulteriori informazioni, vedere [Rintracciare i colli](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="6d2e0-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="6d2e0-107">Quando sugli ordini di vendita vengono impostati i relativi spedizionieri è possibile specificare anche i servizi offerti da ciascuno spedizioniere.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="6d2e0-108">Per ciascuno di essi è possibile impostare un numero qualsiasi di servizi e per ogni servizio si può impostare il tempo di spedizione.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="6d2e0-109">Quando a una riga di ordine di vendita viene assegnato un servizio spedizioniere, il tempo di spedizione del servizio sarà compreso nel calcolo della promessa d'ordine relativa a quella riga.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="6d2e0-110">Per ulteriori informazioni, vedere [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="6d2e0-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="6d2e0-111">Per impostare uno spedizioniere</span><span class="sxs-lookup"><span data-stu-id="6d2e0-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="6d2e0-112">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Spedizionieri** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6d2e0-113">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="6d2e0-114">.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-114">.</span></span>  
3.  <span data-ttu-id="6d2e0-115">Scegliere l'azione **Servizi spedizioniere**.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="6d2e0-116">In **Servizi spedizioniere** compilare tutti i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="6d2e0-117">Se uno spedizioniere viene eliminato dalla riga di ordine, verrà eliminato anche il codice di servizio spedizioniere.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="6d2e0-118">Il contenuto di campi parzialmente basato sul servizio spedizioniere verrà ricalcolato.</span><span class="sxs-lookup"><span data-stu-id="6d2e0-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6d2e0-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6d2e0-119">See Also</span></span>
[<span data-ttu-id="6d2e0-120">Impostare i metodi di pagamento:</span><span class="sxs-lookup"><span data-stu-id="6d2e0-120">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)  
<span data-ttu-id="6d2e0-121">[Rintracciare i colli](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="6d2e0-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="6d2e0-122">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="6d2e0-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="6d2e0-123">Magazzino</span><span class="sxs-lookup"><span data-stu-id="6d2e0-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6d2e0-124">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="6d2e0-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="6d2e0-125">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="6d2e0-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="6d2e0-126">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="6d2e0-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6d2e0-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d2e0-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
