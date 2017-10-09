---
title: "Impostare le origini Web per le società contatto| Documenti Microsoft"
description: "È possibile definire origini Web o Internet e assegnarle a una società contatto per consentire l'identificazione delle modalità di ricerca delle informazioni sui contatti."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b81deefcdf79a93cc988d216f80b08794efb8ab6
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a><span data-ttu-id="dea7d-103">Procedura: Impostare le origini Web per le società contatto</span><span class="sxs-lookup"><span data-stu-id="dea7d-103">How to: Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="dea7d-104">È possibile utilizzare le origini Web con le società contatto per identificare, ad esempio, motori di ricerca e siti Web dove effettuare la ricerca di informazioni sui contatti.</span><span class="sxs-lookup"><span data-stu-id="dea7d-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="dea7d-105">Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="dea7d-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="dea7d-106">L'utilizzo delle origini Web nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="dea7d-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="dea7d-107">Innanzitutto, occorre definire il codice origine Web.</span><span class="sxs-lookup"><span data-stu-id="dea7d-107">First, you define the web source code.</span></span> <span data-ttu-id="dea7d-108">Questo passaggio deve essere eseguito una sola volta per ogni origine Web.</span><span class="sxs-lookup"><span data-stu-id="dea7d-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="dea7d-109">Dopo aver creato un codice origine Web, è possibile iniziare ad assegnarlo ai contatti.</span><span class="sxs-lookup"><span data-stu-id="dea7d-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="dea7d-110">Per definire un codice origine Web</span><span class="sxs-lookup"><span data-stu-id="dea7d-110">To define a web source code</span></span>
1. <span data-ttu-id="dea7d-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Origini Web**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="dea7d-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="dea7d-112">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="dea7d-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="dea7d-113">Compilare i campi **Codice**, **Descrizione** e **URL**.</span><span class="sxs-lookup"><span data-stu-id="dea7d-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="dea7d-114">Nel campo **URL** immettere %1 per inserire un segnaposto per una parola di ricerca nell'URL.</span><span class="sxs-lookup"><span data-stu-id="dea7d-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="dea7d-115">Quando si apre l'origine Web da un contatto, %1 verrà automaticamente sostituito con la parola da ricercare (ad esempio il nome della società) inserita nella finestra **Origini Web contatto**.</span><span class="sxs-lookup"><span data-stu-id="dea7d-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="dea7d-116">Ripetere tali passaggi per impostare altre origini Web.</span><span class="sxs-lookup"><span data-stu-id="dea7d-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="dea7d-117">Per assegnare origini Web a una società contatto</span><span class="sxs-lookup"><span data-stu-id="dea7d-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="dea7d-118">Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="dea7d-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="dea7d-119">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="dea7d-119">Open the contact.</span></span>
2. <span data-ttu-id="dea7d-120">Scegliere l'azione **Società**, quindi l'azione **Origini Web**.</span><span class="sxs-lookup"><span data-stu-id="dea7d-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="dea7d-121">Verrà visualizzata la finestra **Origine Web contatto**.</span><span class="sxs-lookup"><span data-stu-id="dea7d-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="dea7d-122">Nel campo **Codice origine Web** scegliere l'origine Web che si desidera assegnare.</span><span class="sxs-lookup"><span data-stu-id="dea7d-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="dea7d-123">Nel campo **Parola ricerca** inserire la parola ricerca che verrà utilizzata per individuare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="dea7d-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="dea7d-124">Ripetere tali passaggi per assegnare altre origini Web.</span><span class="sxs-lookup"><span data-stu-id="dea7d-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="dea7d-125">È inoltre possibile assegnare l'origine Web dalla finestra **Lista contatti** seguendo la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="dea7d-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="dea7d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dea7d-126">See Also</span></span>
[<span data-ttu-id="dea7d-127">Creazione di società contatto</span><span class="sxs-lookup"><span data-stu-id="dea7d-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="dea7d-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dea7d-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

