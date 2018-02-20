---
title: Calcolo della data per le vendite | Microsoft Docs
description: "Il programma calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data. Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c5cb056c7287f4c12b84dcece595a8e97c0a6214
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="681ec-104">Calcolo della data per le vendite</span><span class="sxs-lookup"><span data-stu-id="681ec-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="681ec-105">In  viene automaticamente calcolata la prima data possibile di spedizione di un articolo nella riga ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="681ec-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="681ec-106">Se il cliente ha richiesto una data di consegna specifica, viene calcolata la data in cui gli articoli devono essere disponibili per il prelievo affinché la consegna avvenga come da richiesta.</span><span class="sxs-lookup"><span data-stu-id="681ec-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="681ec-107">Se il cliente non richiede una data di consegna specifica, la data in cui gli articoli possono essere consegnati viene calcolata, a partire dalla data in cui gli articoli sono disponibili per il prelievo.</span><span class="sxs-lookup"><span data-stu-id="681ec-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="681ec-108">Calcolo con una data di consegna richiesta</span><span class="sxs-lookup"><span data-stu-id="681ec-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="681ec-109">Se si specifica una data di consegna richiesta sulla riga dell'ordine di vendita, questa data verrà utilizzata come data di partenza per i calcoli successivi.</span><span class="sxs-lookup"><span data-stu-id="681ec-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="681ec-110">data di consegna richiesta - durata spedizione = data di spedizione pianificata</span><span class="sxs-lookup"><span data-stu-id="681ec-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="681ec-111">data di spedizione pianificata - tempo gest. uscita da whse. = data spedizione</span><span class="sxs-lookup"><span data-stu-id="681ec-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="681ec-112">Se gli articoli sono disponibili per il prelievo alla data di spedizione, il processo di vendita può proseguire.</span><span class="sxs-lookup"><span data-stu-id="681ec-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="681ec-113">Se non esistono articoli disponibili per il prelievo alla data di spedizione, verrà visualizzato un avviso di esaurimento delle scorte.</span><span class="sxs-lookup"><span data-stu-id="681ec-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="681ec-114">Calcolo della prima data utile per la consegna</span><span class="sxs-lookup"><span data-stu-id="681ec-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="681ec-115">Se nella riga dell'ordine di vendita non si specifica una data di consegna richiesta, o se la data richiesta non può essere rispettata, viene calcolata la prima data in cui gli articoli saranno disponibili.</span><span class="sxs-lookup"><span data-stu-id="681ec-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="681ec-116">Questa data viene quindi immessa nel campo Data spedizione della riga e le date in cui si prevede di spedire gli articoli e in cui essi saranno consegnati al cliente vengono calcolate secondo le seguenti formule.</span><span class="sxs-lookup"><span data-stu-id="681ec-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="681ec-117">data spedizione + tempo gest. uscita da whse. = data di spedizione pianificata</span><span class="sxs-lookup"><span data-stu-id="681ec-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="681ec-118">data di spedizione pianificata + durata spedizione = data di consegna pianificata</span><span class="sxs-lookup"><span data-stu-id="681ec-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="681ec-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="681ec-119">See Also</span></span>  
 <span data-ttu-id="681ec-120">[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="681ec-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="681ec-121">Calcolare le date per la promessa ordine</span><span class="sxs-lookup"><span data-stu-id="681ec-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="681ec-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="681ec-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

