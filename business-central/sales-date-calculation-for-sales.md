---
title: Calcolo della data per le vendite | Microsoft Docs
description: L'applicazione calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data. Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 49bc91d049ee6c2357323ed4e88f66116322d276
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778899"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="062e0-104">Calcolo della data per le vendite</span><span class="sxs-lookup"><span data-stu-id="062e0-104">Date Calculation for Sales</span></span>
<span data-ttu-id="062e0-105">In [!INCLUDE[prod_short](includes/prod_short.md)] viene automaticamente calcolata la prima data possibile di spedizione di un articolo nella riga ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="062e0-105">[!INCLUDE[prod_short](includes/prod_short.md)] automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="062e0-106">Se il cliente ha richiesto una data di consegna specifica, viene calcolata la data in cui gli articoli devono essere disponibili per il prelievo affinché la consegna avvenga come da richiesta.</span><span class="sxs-lookup"><span data-stu-id="062e0-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="062e0-107">Se il cliente non richiede una data di consegna specifica, la data in cui gli articoli possono essere consegnati viene calcolata, a partire dalla data in cui gli articoli sono disponibili per il prelievo.</span><span class="sxs-lookup"><span data-stu-id="062e0-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="062e0-108">Calcolo con una data di consegna richiesta</span><span class="sxs-lookup"><span data-stu-id="062e0-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="062e0-109">Se si specifica una data di consegna richiesta sulla riga dell'ordine di vendita, questa data diventa la data di partenza per i calcoli successivi.</span><span class="sxs-lookup"><span data-stu-id="062e0-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="062e0-110">data di consegna richiesta - durata spedizione = data di spedizione pianificata</span><span class="sxs-lookup"><span data-stu-id="062e0-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="062e0-111">data di spedizione pianificata - tempo gest. uscita da whse. = data spedizione</span><span class="sxs-lookup"><span data-stu-id="062e0-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="062e0-112">Se gli articoli sono disponibili per il prelievo alla data di spedizione, il processo di vendita può proseguire.</span><span class="sxs-lookup"><span data-stu-id="062e0-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="062e0-113">In caso contrario, viene visualizzato un avviso di esaurimento delle scorte.</span><span class="sxs-lookup"><span data-stu-id="062e0-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="062e0-114">Se il processo si basa sul calcolo indietro, ad esempio, se si utilizza la data di consegna richiesta per ottenere la data di spedizione pianificata, si consiglia di utilizzare formule di data con durate fisse, ad esempio "5D" per cinque giorni o "1W" per una settimana.</span><span class="sxs-lookup"><span data-stu-id="062e0-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="062e0-115">Le formule di data senza durate fisse, come "CW" per settimana corrente o CM per mese corrente, possono comportare calcoli della data errati.</span><span class="sxs-lookup"><span data-stu-id="062e0-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="062e0-116">Per ulteriori informazioni sulle formule di data, vedere [Lavorare con le date e gli orari del calendario ](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="062e0-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="062e0-117">Calcolo della prima data utile per la consegna</span><span class="sxs-lookup"><span data-stu-id="062e0-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="062e0-118">Se nella riga dell'ordine di vendita non si specifica una data di consegna richiesta, o se la data richiesta non può essere rispettata, viene calcolata la prima data in cui gli articoli saranno disponibili.</span><span class="sxs-lookup"><span data-stu-id="062e0-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="062e0-119">Questa data viene quindi immessa nel campo Data spedizione della riga e le date in cui si prevede di spedire gli articoli e in cui essi saranno consegnati al cliente vengono calcolate secondo le seguenti formule.</span><span class="sxs-lookup"><span data-stu-id="062e0-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="062e0-120">data spedizione + tempo gest. uscita da whse. = data di spedizione pianificata</span><span class="sxs-lookup"><span data-stu-id="062e0-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="062e0-121">data di spedizione pianificata + durata spedizione = data di consegna pianificata</span><span class="sxs-lookup"><span data-stu-id="062e0-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="062e0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="062e0-122">See Also</span></span>  
 <span data-ttu-id="062e0-123">[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="062e0-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="062e0-124">Calcolare le date per la promessa ordine</span><span class="sxs-lookup"><span data-stu-id="062e0-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="062e0-125">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="062e0-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]