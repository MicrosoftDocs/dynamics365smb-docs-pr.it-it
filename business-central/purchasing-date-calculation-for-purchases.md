---
title: Calcolo della data per gli acquisti | Documenti Microsoft
description: L'applicazione calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data. Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 41b1b1b0459706a8c061a0044824b5b7c4c9aa62
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312582"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="1af14-104">Calcolo della data per gli acquisti</span><span class="sxs-lookup"><span data-stu-id="1af14-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1af14-105">calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data.</span><span class="sxs-lookup"><span data-stu-id="1af14-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="1af14-106">Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo.</span><span class="sxs-lookup"><span data-stu-id="1af14-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="1af14-107">Se si specifica una data di carico richiesta nella testata di un ordine di acquisto, la data dell'ordine calcolata è la data in cui si deve effettuare l'ordine per ricevere gli articoli alla data richiesta.</span><span class="sxs-lookup"><span data-stu-id="1af14-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="1af14-108">Quindi, la data in cui gli articoli saranno disponibili per il prelievo viene calcolata e immessa nel campo **Data carico prevista**.</span><span class="sxs-lookup"><span data-stu-id="1af14-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="1af14-109">Se non si specifica una data di carico richiesta, la data d'ordine presente sulla riga verrà usata come data di partenza per il calcolo della data prevedibile per la ricezione degli articoli e della data in cui gli articoli saranno disponibili per il prelievo.</span><span class="sxs-lookup"><span data-stu-id="1af14-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="1af14-110">Calcolo con una data di carico richiesta</span><span class="sxs-lookup"><span data-stu-id="1af14-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="1af14-111">Se è presente una data di carico richiesta sulla riga dell'ordine di acquisto, questa data verrà utilizzata come data di partenza per i calcoli successivi.</span><span class="sxs-lookup"><span data-stu-id="1af14-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="1af14-112">data di carico richiesta - calcolo lead time = data ordine</span><span class="sxs-lookup"><span data-stu-id="1af14-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="1af14-113">data di carico richiesta + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista</span><span class="sxs-lookup"><span data-stu-id="1af14-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="1af14-114">Se è stata immessa una data di carico richiesta sulla testata dell'ordine di acquisto, questa data viene copiata nel campo corrispondente in tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="1af14-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="1af14-115">È possibile modificare questa data in qualsiasi riga oppure rimuoverla.</span><span class="sxs-lookup"><span data-stu-id="1af14-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!Note]
> <span data-ttu-id="1af14-116">Se il processo si basa sul calcolo indietro, ad esempio, se si utilizza la data carico richiesta per ottenere la data dell'ordine, si consiglia di utilizzare formule di data con durate fisse, ad esempio "5D" per cinque giorni o "1W" per una settimana.</span><span class="sxs-lookup"><span data-stu-id="1af14-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="1af14-117">Le formule di data senza durate fisse, come "CW" per settimana corrente o CM per mese corrente, possono comportare calcoli della data errati.</span><span class="sxs-lookup"><span data-stu-id="1af14-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="1af14-118">Per ulteriori informazioni sulle formule di data, vedere [Lavorare con le date e gli orari del calendario ](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="1af14-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="1af14-119">Calcolo senza una data di consegna richiesta</span><span class="sxs-lookup"><span data-stu-id="1af14-119">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="1af14-120">Se si immette una riga di ordine di acquisto senza una data di consegna richiesta, il campo **Data ordine** nella riga viene compilato con la data nel campo **Data ordine** dell'intestazione dell'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="1af14-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="1af14-121">Si tratta della data immessa o della work date.</span><span class="sxs-lookup"><span data-stu-id="1af14-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="1af14-122">Le date seguenti vengono quindi calcolate per la riga dell'ordine di acquisto, con la data dell'ordine come punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="1af14-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="1af14-123">data ordine + calcolo lead time = data carico pianificato</span><span class="sxs-lookup"><span data-stu-id="1af14-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="1af14-124">data carico pianificato + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista</span><span class="sxs-lookup"><span data-stu-id="1af14-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="1af14-125">Se si modifica la data dell'ordine sulla riga, ad esempio quando gli articoli non sono disponibili presso il fornitore fino a una data successiva, le date corrispondenti nella riga saranno ricalcolate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1af14-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="1af14-126">Se si modifica la data dell'ordine nell'intestazione, questa viene copiata nel campo **Data ordine** in tutte le righe e tutti i campi data correlati vengono ricalcolati.</span><span class="sxs-lookup"><span data-stu-id="1af14-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1af14-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af14-127">See Also</span></span>  
 <span data-ttu-id="1af14-128">[Calcolo della data per le vendite](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="1af14-128">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="1af14-129">Calcolare le date per la promessa ordine</span><span class="sxs-lookup"><span data-stu-id="1af14-129">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="1af14-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1af14-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
