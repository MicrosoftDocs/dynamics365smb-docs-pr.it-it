---
title: Come tenere traccia delle relazioni tra domanda e approvvigionamento | Microsoft Docs
description: A partire da qualsiasi documento dell'approvvigionamento o della domanda, è possibile tenere traccia della richiesta dell'ordine (quantità tracciata), della previsione, dell'ordine di vendita programmato o del parametro di pianificazione (quantità non tracciata) che ha generato la riga di pianificazione in questione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b164ce7ba4be7e21b7c99c6e38cb9019e3ddc665
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784869"
---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="07c9d-103">Tenere traccia delle relazioni tra domanda e approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="07c9d-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="07c9d-104">A partire da qualsiasi documento dell'approvvigionamento o della domanda, è possibile tenere traccia della richiesta dell'ordine (quantità tracciata), della previsione, dell'ordine di vendita programmato o del parametro di pianificazione (quantità non tracciata) che ha generato la riga di pianificazione in questione.</span><span class="sxs-lookup"><span data-stu-id="07c9d-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="07c9d-105">I prospetti di pianificazione offrono anche informazioni di supporto alla pianificazione relative a entità non di ordine per consentire al responsabile della pianificazione di ottenere un piano di approvvigionamento ottimale.</span><span class="sxs-lookup"><span data-stu-id="07c9d-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="07c9d-106">Per ulteriori informazioni, vedere [Elementi di pianificazione non tracciati](production-how-track-demand-supply.md#untracked-planning-elements).</span><span class="sxs-lookup"><span data-stu-id="07c9d-106">For more information, see [Untracked Planning Elements](production-how-track-demand-supply.md#untracked-planning-elements).</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="07c9d-107">Per tracciare articoli collegati</span><span class="sxs-lookup"><span data-stu-id="07c9d-107">To track linked items</span></span>
<span data-ttu-id="07c9d-108">Tramite i sistemi di impegno e pianificazione, la funzione di tracciabilità degli ordini consente di conoscere la relazione tra ordini di vendita, di produzione e di acquisto e l'ordine di manufacturing.</span><span class="sxs-lookup"><span data-stu-id="07c9d-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="07c9d-109">Di seguito viene descritto come tenere traccia degli articoli collegati in un ordine di produzione pianificato.</span><span class="sxs-lookup"><span data-stu-id="07c9d-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="07c9d-110">I passaggi sono simili per tutti gli altri tipi di ordini e per le righe del prospetto di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="07c9d-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="07c9d-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordine produzione confermato** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="07c9d-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="07c9d-112">Aprire l'ordine di produzione confermato appropriato dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="07c9d-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="07c9d-113">Nella Scheda dettaglio **Righe** scegliere l'azione **Funzioni**, quindi l'azione **Tracciabilità ordine**.</span><span class="sxs-lookup"><span data-stu-id="07c9d-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="07c9d-114">Nelle righe in **Tracciabilità ordine** vengono visualizzati i documenti collegati alla riga dell'ordine di produzione corrente.</span><span class="sxs-lookup"><span data-stu-id="07c9d-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="07c9d-115">Elementi di pianificazione non tracciati</span><span class="sxs-lookup"><span data-stu-id="07c9d-115">Untracked Planning Elements</span></span>
<span data-ttu-id="07c9d-116">Quando si sceglie il campo **Qtà non tracciata** nella pagina **Pianificazione ordini**, viene visualizzata la pagina **Elementi di pianificazione non tracciati**.</span><span class="sxs-lookup"><span data-stu-id="07c9d-116">The **Untracked Planning Elements** page opens when you choose the **Untracked Qty.** field on the **order Planning** page.</span></span> <span data-ttu-id="07c9d-117">Questa finestra è utilizzate per due scopi:</span><span class="sxs-lookup"><span data-stu-id="07c9d-117">It serves two purposes:</span></span>

1. <span data-ttu-id="07c9d-118">Contenere informazioni sulle quantità non tracciate che vengono visualizzate quando l'utente effettua una ricerca dalla pagina Tracciabilità ordine.</span><span class="sxs-lookup"><span data-stu-id="07c9d-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking page to see untracked quantities.</span></span>
2. <span data-ttu-id="07c9d-119">Contenere i messaggi di errore visualizzati quando si sceglie un'icona **Avviso** nella pagina **Prospetto pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="07c9d-119">To hold warning messages displayed when the user chooses the **Warning** icon on the **Planning Worksheet** page.</span></span>

<span data-ttu-id="07c9d-120">In questa pagina sono contenuti movimenti che rappresentano una quantità di surplus non tracciata nella rete di tracciabilità dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="07c9d-120">The page contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="07c9d-121">Questi movimenti vengono generati durante l'esecuzione della pianificazione e indicano la provenienza di tale quantità presente nelle righe di tracciabilità dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="07c9d-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="07c9d-122">Il surplus non tracciato può derivare dai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="07c9d-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="07c9d-123">Previsione di produzione</span><span class="sxs-lookup"><span data-stu-id="07c9d-123">Production forecast</span></span>
- <span data-ttu-id="07c9d-124">Ordini programmati</span><span class="sxs-lookup"><span data-stu-id="07c9d-124">Blanket orders</span></span>
- <span data-ttu-id="07c9d-125">Scorta di sicurezza</span><span class="sxs-lookup"><span data-stu-id="07c9d-125">Safety stock quantity</span></span>
- <span data-ttu-id="07c9d-126">Punto di riordino</span><span class="sxs-lookup"><span data-stu-id="07c9d-126">Reorder point</span></span>
- <span data-ttu-id="07c9d-127">Giacenza massima</span><span class="sxs-lookup"><span data-stu-id="07c9d-127">Maximum inventory</span></span>
- <span data-ttu-id="07c9d-128">Quantità di riordino</span><span class="sxs-lookup"><span data-stu-id="07c9d-128">Reorder quantity</span></span>
- <span data-ttu-id="07c9d-129">Quantità massima dell'ordine</span><span class="sxs-lookup"><span data-stu-id="07c9d-129">Maximum order quantity</span></span>
- <span data-ttu-id="07c9d-130">Quantità minima dell'ordine</span><span class="sxs-lookup"><span data-stu-id="07c9d-130">Minimum order quantity</span></span>
- <span data-ttu-id="07c9d-131">Molteplicità dell'ordine</span><span class="sxs-lookup"><span data-stu-id="07c9d-131">Order multiple</span></span>
- <span data-ttu-id="07c9d-132">Smorzamento (percentuale di dimensione del lotto)</span><span class="sxs-lookup"><span data-stu-id="07c9d-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="07c9d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07c9d-133">See Also</span></span>  
<span data-ttu-id="07c9d-134">[Pianif.](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="07c9d-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="07c9d-135">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="07c9d-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="07c9d-136">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="07c9d-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="07c9d-137">Magazzino</span><span class="sxs-lookup"><span data-stu-id="07c9d-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="07c9d-138">Acquisti</span><span class="sxs-lookup"><span data-stu-id="07c9d-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="07c9d-139">Dettagli di progettazione: Impegno, tracciabilità e messaggistica di azioni</span><span class="sxs-lookup"><span data-stu-id="07c9d-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="07c9d-140">[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="07c9d-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="07c9d-141">Impostare le procedure ottimali: Pianificazione forniture</span><span class="sxs-lookup"><span data-stu-id="07c9d-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="07c9d-142">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="07c9d-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
