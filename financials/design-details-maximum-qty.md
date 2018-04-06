---
title: "Dettagli di progettazione: Qtà massima | Microsoft Docs"
description: "Il criterio Quantità massima è un modo per mantenere il magazzino utilizzando un punto di riordino."
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
ms.openlocfilehash: 26bed0b8832d5b12ce5d697df8ec6194ac7ae9b2
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-maximum-qty"></a><span data-ttu-id="1b90f-103">Dettagli di progettazione: Qtà Massima</span><span class="sxs-lookup"><span data-stu-id="1b90f-103">Design Details: Maximum Qty.</span></span>
<span data-ttu-id="1b90f-104">Il criterio Quantità massima è un modo per mantenere il magazzino utilizzando un punto di riordino.</span><span class="sxs-lookup"><span data-stu-id="1b90f-104">The Maximum Quantity policy is a way to maintain inventory using a reorder point.</span></span>  
  
 <span data-ttu-id="1b90f-105">Tutto ciò che riguarda il metodo Qtà Riordino Fissa si applica anche a questi criteri.</span><span class="sxs-lookup"><span data-stu-id="1b90f-105">Everything regarding the Fixed Reorder Qty. policy also applies to this policy.</span></span> <span data-ttu-id="1b90f-106">L'unica differenza è la quantità dell'approvvigionamento suggerito.</span><span class="sxs-lookup"><span data-stu-id="1b90f-106">The only difference is the quantity of the suggested supply.</span></span> <span data-ttu-id="1b90f-107">Se si utilizza il metodo della quantità massima, la quantità di riordino verrà definita in modo dinamico in base al livello delle giacenze disponibili e quindi in genere differirà da ordine a ordine.</span><span class="sxs-lookup"><span data-stu-id="1b90f-107">When using the maximum quantity policy, the reorder quantity will be defined dynamically based on the projected inventory level and will therefore usually differ from order to order.</span></span>  
  
## <a name="calculated-per-time-bucket"></a><span data-ttu-id="1b90f-108">Calcolato per intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="1b90f-108">Calculated per Time Bucket</span></span>  
 <span data-ttu-id="1b90f-109">La quantità di riordino viene determinata in un punto del tempo (alla fine di un intervallo di tempo) quando il sistema di pianificazione rileva che il punto di riordino è stato superato.</span><span class="sxs-lookup"><span data-stu-id="1b90f-109">The reorder quantity is determined at the point of time (the end of a time bucket) when the planning system detects that the reorder point has been crossed.</span></span> <span data-ttu-id="1b90f-110">A questo punto, il sistema misura l'interruzione dal livello di magazzino previsto corrente fino al magazzino massimo specificato.</span><span class="sxs-lookup"><span data-stu-id="1b90f-110">At this time, the system measures the gap from the current projected inventory level up to the specified maximum inventory.</span></span> <span data-ttu-id="1b90f-111">Ciò costituisce la quantità che deve essere riordinata.</span><span class="sxs-lookup"><span data-stu-id="1b90f-111">This constitutes the quantity that should be reordered.</span></span> <span data-ttu-id="1b90f-112">Il sistema controlla quindi se l'approvvigionamento è già stato ordinato altrove in modo che possa essere caricato entro il lead time e, in caso affermativo, riduce la quantità del nuovo ordine di approvvigionamento della quantità già ordinata.</span><span class="sxs-lookup"><span data-stu-id="1b90f-112">The system then checks if supply has already been ordered elsewhere to be received within the lead time and, if so, reduces the quantity of the new supply order by already ordered quantities.</span></span>  
  
 <span data-ttu-id="1b90f-113">Il sistema assicurerà che la giacenza disponibile raggiunga almeno il livello del punto di riordino, nel caso l'utente abbia dimenticato di specificare una quantità di magazzino massima.</span><span class="sxs-lookup"><span data-stu-id="1b90f-113">The system will ensure that the projected inventory at least reaches the reorder point level – in case the user has forgotten to specify a maximum inventory quantity.</span></span>  
  
## <a name="combines-with-order-modifiers"></a><span data-ttu-id="1b90f-114">Combina con i modificatori di ordine</span><span class="sxs-lookup"><span data-stu-id="1b90f-114">Combines with Order Modifiers</span></span>  
 <span data-ttu-id="1b90f-115">In base all'impostazione, è consigliabile combinare i criteri Quantità massima con i modificatori di ordini per garantire una quantità minima dell'ordine o per arrotondarla a un numero intero di unità di misura di acquisto, o suddividerla in più lotti come definito dalla quantità massima ordine.</span><span class="sxs-lookup"><span data-stu-id="1b90f-115">Depending on the setup, it may be best to combine the Maximum Quantity policy with order modifiers to ensure a minimum order quantity or round it to an integer number of purchase units of measure, or split it into more lots as defined by the maximum order quantity.</span></span>  
  
## <a name="combines-with-calendars"></a><span data-ttu-id="1b90f-116">Associazioni con i calendari</span><span class="sxs-lookup"><span data-stu-id="1b90f-116">Combines with Calendars</span></span>  
 <span data-ttu-id="1b90f-117">Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione verifica che l'ordine sia programmato per un giorno non lavorativo, in base ai calendari definiti nel campo **Codice calendario base** delle finestre **Informazioni società** e **Scheda Ubicazione**.</span><span class="sxs-lookup"><span data-stu-id="1b90f-117">Before suggesting a new supply order to meet a reorder point, the planning system checks if the order is scheduled for a non-working day, according to any calendars that are  defined in the **Base Calendar Code** field in the **Company Information** and **Location Card** windows.</span></span>  
  
 <span data-ttu-id="1b90f-118">Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino.</span><span class="sxs-lookup"><span data-stu-id="1b90f-118">If the scheduled date is a non-working day, the planning system moves the order forward to the nearest working date.</span></span> <span data-ttu-id="1b90f-119">In questo modo, potrebbe verificarsi che un ordine soddisfi un punto di riordino ma non una richiesta specifica.</span><span class="sxs-lookup"><span data-stu-id="1b90f-119">This may result in an order that meets a reorder point but does not meet some specific demand.</span></span> <span data-ttu-id="1b90f-120">Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="1b90f-120">For such unbalanced demand, the planning system creates an extra supply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b90f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b90f-121">See Also</span></span>  
 <span data-ttu-id="1b90f-122">[Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="1b90f-122">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="1b90f-123">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="1b90f-123">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="1b90f-124">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="1b90f-124">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="1b90f-125">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="1b90f-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
