---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788563"
---
<span data-ttu-id="d1cba-101">Quando si immettono dati di tipo datetime che corrispondono a una data e un'ora combinate in un campo, è necessario inserire uno spazio tra la data e l'ora.</span><span class="sxs-lookup"><span data-stu-id="d1cba-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="d1cba-102">La parte della data può contenere solo spazi nella forma del separatore della data ufficiale delle impostazioni del paese.</span><span class="sxs-lookup"><span data-stu-id="d1cba-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="d1cba-103">L'ora può contenere spazi attorno all'indicatore AM/PM nelle impostazioni regionali rilevanti.</span><span class="sxs-lookup"><span data-stu-id="d1cba-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="d1cba-104">Nella tabella seguente sono elencati i vari formati in cui è possibile immettere la data e l'ora e le interpretazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="d1cba-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="d1cba-105">Immissione</span><span class="sxs-lookup"><span data-stu-id="d1cba-105">Entry</span></span>|<span data-ttu-id="d1cba-106">Interpretazione</span><span class="sxs-lookup"><span data-stu-id="d1cba-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="d1cba-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="d1cba-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="d1cba-108">08\-01\-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="d1cba-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="d1cba-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="d1cba-109">131222 132455</span></span>|<span data-ttu-id="d1cba-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="d1cba-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="d1cba-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="d1cba-111">1-12-22 10</span></span>|<span data-ttu-id="d1cba-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="d1cba-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="d1cba-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="d1cba-113">1.12.22 5</span></span>|<span data-ttu-id="d1cba-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="d1cba-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="d1cba-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="d1cba-115">1.12.22</span></span>|<span data-ttu-id="d1cba-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d1cba-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="d1cba-117">11 12</span><span class="sxs-lookup"><span data-stu-id="d1cba-117">11 12</span></span>|<span data-ttu-id="d1cba-118">11/mese corrente/anno corrente 12.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="d1cba-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="d1cba-119">1112 12</span></span>|<span data-ttu-id="d1cba-120">11/12/anno corrente 12.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="d1cba-121">o oppure oggi</span><span class="sxs-lookup"><span data-stu-id="d1cba-121">t or today</span></span>|<span data-ttu-id="d1cba-122">Data odierna 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="d1cba-123">o ora</span><span class="sxs-lookup"><span data-stu-id="d1cba-123">t time</span></span>|<span data-ttu-id="d1cba-124">Ora corrente in data odierna</span><span class="sxs-lookup"><span data-stu-id="d1cba-124">today's date actual time</span></span>|
|<span data-ttu-id="d1cba-125">o 10:30</span><span class="sxs-lookup"><span data-stu-id="d1cba-125">t 10:30</span></span>|<span data-ttu-id="d1cba-126">Data odierna 10.30.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="d1cba-127">o 3:3:3</span><span class="sxs-lookup"><span data-stu-id="d1cba-127">t 3:3:3</span></span>|<span data-ttu-id="d1cba-128">Data odierna 03.03.03</span><span class="sxs-lookup"><span data-stu-id="d1cba-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="d1cba-129">l o data di lavoro</span><span class="sxs-lookup"><span data-stu-id="d1cba-129">w or workdate</span></span>|<span data-ttu-id="d1cba-130">Data del lavoro 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="d1cba-131">lu o lunedì</span><span class="sxs-lookup"><span data-stu-id="d1cba-131">m or Monday</span></span>|<span data-ttu-id="d1cba-132">Lunedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="d1cba-133">ma o martedì</span><span class="sxs-lookup"><span data-stu-id="d1cba-133">tu or Tuesday</span></span>|<span data-ttu-id="d1cba-134">Martedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="d1cba-135">me o mercoledì</span><span class="sxs-lookup"><span data-stu-id="d1cba-135">we or Wednesday</span></span>|<span data-ttu-id="d1cba-136">Mercoledì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="d1cba-137">gi o giovedì</span><span class="sxs-lookup"><span data-stu-id="d1cba-137">th or Thursday</span></span>|<span data-ttu-id="d1cba-138">Giovedì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="d1cba-139">ve o venerdì</span><span class="sxs-lookup"><span data-stu-id="d1cba-139">f or Friday</span></span>|<span data-ttu-id="d1cba-140">Venerdì della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="d1cba-141">sa o sabato</span><span class="sxs-lookup"><span data-stu-id="d1cba-141">s or Saturday</span></span>|<span data-ttu-id="d1cba-142">Sabato della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="d1cba-143">do o domenica</span><span class="sxs-lookup"><span data-stu-id="d1cba-143">su or Sunday</span></span>|<span data-ttu-id="d1cba-144">Domenica della settimana corrente 00.00.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="d1cba-145">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="d1cba-145">tu 10:30</span></span>|<span data-ttu-id="d1cba-146">Martedì della settimana corrente 10.30.00</span><span class="sxs-lookup"><span data-stu-id="d1cba-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="d1cba-147">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="d1cba-147">tu 3:3:3</span></span>|<span data-ttu-id="d1cba-148">Martedì della settimana corrente 03.03.03</span><span class="sxs-lookup"><span data-stu-id="d1cba-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="d1cba-149">m23 o</span><span class="sxs-lookup"><span data-stu-id="d1cba-149">t23 t</span></span>|<span data-ttu-id="d1cba-150">Martedì della settimana 23 dell'anno della data di lavoro, ora corrente del giorno</span><span class="sxs-lookup"><span data-stu-id="d1cba-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="d1cba-151">m23</span><span class="sxs-lookup"><span data-stu-id="d1cba-151">t23</span></span>|<span data-ttu-id="d1cba-152">Martedì della settimana 23 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="d1cba-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="d1cba-153">m 23</span><span class="sxs-lookup"><span data-stu-id="d1cba-153">t 23</span></span>|<span data-ttu-id="d1cba-154">Oggi 23:00:00</span><span class="sxs-lookup"><span data-stu-id="d1cba-154">Today 23:00:00</span></span>|
|<span data-ttu-id="d1cba-155">m-1</span><span class="sxs-lookup"><span data-stu-id="d1cba-155">t-1</span></span>|<span data-ttu-id="d1cba-156">Martedì della settimana 1 dell'anno della data di lavoro</span><span class="sxs-lookup"><span data-stu-id="d1cba-156">Tuesday of week 1 of the work date year</span></span>|


