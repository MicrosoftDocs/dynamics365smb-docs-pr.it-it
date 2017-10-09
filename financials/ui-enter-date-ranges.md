---
title: Impostare gli intervalli di date in Dynamics 365 for Financials | Documenti Microsoft
description: Informazioni su come ottenere un report per visualizzare i dati relativi a periodi di tempo specifici utilizzando gli intervalli di date in Dynamics 365 for Financials.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dc7cd392843ce7c39200bb2331c09cc44c7a394a
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="entering-date-ranges-in-dynamics-365-for-financials"></a><span data-ttu-id="0ad3a-103">Immettere intervalli di date in Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="0ad3a-103">Entering Date Ranges in Dynamics 365 for Financials</span></span>
<span data-ttu-id="0ad3a-104">È possibile impostare filtri contenenti una data di inizio e una data di fine per visualizzare solo la data inclusa in un intervallo di date o di ore specifico.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="0ad3a-105">All'impostazione di intervalli di date si applicano regole speciali.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="0ad3a-106">Si consideri come esempio la **Lista primi 10 clienti**:</span><span class="sxs-lookup"><span data-stu-id="0ad3a-106">Let's take the **Customer Top 10** as an example:</span></span>

![Impostare un intervallo di date nella pagina di richiesta per la Lista primi 10 clienti](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="0ad3a-108">In questo campo è possibile limitare il report a un intervallo di date, ad esempio, alle ultime 2 settimane o a un totale di 6 settimane o a qualsiasi intervallo che si desidera.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="0ad3a-109">Per impostare gli intervalli di date, immettere le date quindi utilizzare **..**</span><span class="sxs-lookup"><span data-stu-id="0ad3a-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="0ad3a-110">o **|** per impostare l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-110">or **|** to set the range.</span></span> <span data-ttu-id="0ad3a-111">Nell'esempio, per visualizzare i 10 clienti principali per le prime 2 settimane di maggio, impostare il filtro data come *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="0ad3a-112">Di seguito vengono proposti altri esempi:</span><span class="sxs-lookup"><span data-stu-id="0ad3a-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="0ad3a-113">Significato</span><span class="sxs-lookup"><span data-stu-id="0ad3a-113">Meaning</span></span> | <span data-ttu-id="0ad3a-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="0ad3a-114">Example</span></span> | <span data-ttu-id="0ad3a-115">movimenti inclusi</span><span class="sxs-lookup"><span data-stu-id="0ad3a-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="0ad3a-116">uguale a</span><span class="sxs-lookup"><span data-stu-id="0ad3a-116">Equal to</span></span>| <span data-ttu-id="0ad3a-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="0ad3a-117">12 15 16</span></span> |<span data-ttu-id="0ad3a-118">Solo i movimenti registrati il 15 dicembre 2016.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="0ad3a-119">intervallo</span><span class="sxs-lookup"><span data-stu-id="0ad3a-119">Interval</span></span>| <span data-ttu-id="0ad3a-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="0ad3a-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="0ad3a-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="0ad3a-121">..12 15 16</span></span>|<span data-ttu-id="0ad3a-122">Movimenti registrati in date comprese tra il 15 dicembre 2016 e il 15 gennaio 2017, inclusi.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="0ad3a-123">Movimenti registrati prima del 15 dicembre 2016, incluso.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="0ad3a-124">oppure</span><span class="sxs-lookup"><span data-stu-id="0ad3a-124">Either/or</span></span>|<span data-ttu-id="0ad3a-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="0ad3a-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="0ad3a-126">Movimenti registrati il 15 dicembre o il 16 dicembre 2016.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="0ad3a-127">Se sono presenti movimenti registrati in entrambi i giorni, verranno visualizzati tutti.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="0ad3a-128">È inoltre possibile combinare i vari tipi di formato.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="0ad3a-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="0ad3a-129">Example</span></span> | <span data-ttu-id="0ad3a-130">movimenti inclusi</span><span class="sxs-lookup"><span data-stu-id="0ad3a-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="0ad3a-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="0ad3a-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="0ad3a-132">Movimenti registrati il 15 dicembre 2016 o in date comprese tra il 01° dicembre 2016 e il 31 maggio 2017 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="0ad3a-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="0ad3a-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="0ad3a-134">Movimenti registrati il 14 dicembre, o in giorni precedenti, o movimenti registrati il 30 dicembre, o successivamente, ossia tutti i movimenti esclusi quelli registrati in date comprese tra il 15 e il 29 dicembre, incluse.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="0ad3a-135">Si noti che negli esempi è stato utilizzato il formato data MMGGAA degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="0ad3a-136">Quando [!INCLUDE[d365fin](includes/d365fin_md.md)] sarà disponibile in altri mercati, sarà possibile utilizzare i formati abituali per il proprio paese.</span><span class="sxs-lookup"><span data-stu-id="0ad3a-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ad3a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ad3a-137">See Also</span></span>
<span data-ttu-id="0ad3a-138">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ad3a-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0ad3a-139">Immissione di criteri di filtro</span><span class="sxs-lookup"><span data-stu-id="0ad3a-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="0ad3a-140">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="0ad3a-140">General Business Functionality</span></span>](ui-across-business-areas.md)

