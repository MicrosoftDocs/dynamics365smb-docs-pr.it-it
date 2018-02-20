---
title: Calcolo della data per gli acquisti | Documenti Microsoft
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
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7a37b1ef9e4a73faf8d04398dbc4023eb04ab9f6
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="6d27f-104">Calcolo della data per gli acquisti</span><span class="sxs-lookup"><span data-stu-id="6d27f-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6d27f-105"> calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data.</span><span class="sxs-lookup"><span data-stu-id="6d27f-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="6d27f-106">Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo.</span><span class="sxs-lookup"><span data-stu-id="6d27f-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="6d27f-107">Se si specifica una data di carico richiesta nella testata di un ordine di acquisto, la data dell'ordine calcolata è la data in cui si deve effettuare l'ordine per ricevere gli articoli alla data richiesta.</span><span class="sxs-lookup"><span data-stu-id="6d27f-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="6d27f-108">Quindi, la data in cui gli articoli saranno disponibili per il prelievo viene calcolata e immessa nel campo **Data carico prevista**.</span><span class="sxs-lookup"><span data-stu-id="6d27f-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="6d27f-109">Se non si specifica una data di carico richiesta, la data d'ordine presente sulla riga verrà usata come data di partenza per il calcolo della data prevedibile per la ricezione degli articoli e della data in cui gli articoli saranno disponibili per il prelievo.</span><span class="sxs-lookup"><span data-stu-id="6d27f-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="6d27f-110">Calcolo con una data di carico richiesta</span><span class="sxs-lookup"><span data-stu-id="6d27f-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="6d27f-111">Se è presente una data di carico richiesta sulla riga dell'ordine di acquisto, questa data verrà utilizzata come data di partenza per i calcoli successivi.</span><span class="sxs-lookup"><span data-stu-id="6d27f-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="6d27f-112">data di carico richiesta - calcolo lead time = data ordine</span><span class="sxs-lookup"><span data-stu-id="6d27f-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="6d27f-113">data di carico richiesta + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista</span><span class="sxs-lookup"><span data-stu-id="6d27f-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="6d27f-114">Se è stata immessa una data di carico richiesta sulla testata dell'ordine di acquisto, questa data viene copiata nel campo corrispondente in tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="6d27f-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="6d27f-115">È possibile modificare questa data in qualsiasi riga oppure rimuoverla.</span><span class="sxs-lookup"><span data-stu-id="6d27f-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="6d27f-116">Calcolo senza una data di consegna richiesta</span><span class="sxs-lookup"><span data-stu-id="6d27f-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="6d27f-117">Se si immette una riga di ordine di acquisto senza una data di consegna richiesta, il campo **Data ordine** nella riga viene compilato con la data nel campo **Data ordine** dell'intestazione dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="6d27f-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="6d27f-118">Si tratta della data immessa o della work date.</span><span class="sxs-lookup"><span data-stu-id="6d27f-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="6d27f-119">Le date seguenti vengono quindi calcolate per la riga dell'ordine di acquisto, con la data dell'ordine come punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="6d27f-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="6d27f-120">data ordine + calcolo lead time = data carico pianificato</span><span class="sxs-lookup"><span data-stu-id="6d27f-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="6d27f-121">data carico pianificato + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista</span><span class="sxs-lookup"><span data-stu-id="6d27f-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="6d27f-122">Se si modifica la data dell'ordine sulla riga, ad esempio quando gli articoli non sono disponibili presso il fornitore fino a una data successiva, le date corrispondenti nella riga saranno ricalcolate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6d27f-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="6d27f-123">Se si modifica la data dell'ordine nell'intestazione, questa viene copiata nel campo **Data ordine** in tutte le righe e tutti i campi data correlati vengono ricalcolati.</span><span class="sxs-lookup"><span data-stu-id="6d27f-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6d27f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d27f-124">See Also</span></span>  
 <span data-ttu-id="6d27f-125">[Calcolo della data per le vendite](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="6d27f-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="6d27f-126">Calcolare le date per la promessa ordine</span><span class="sxs-lookup"><span data-stu-id="6d27f-126">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="6d27f-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d27f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

