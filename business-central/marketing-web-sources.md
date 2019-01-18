---
title: "Impostare le origini Web per le società contatto| Documenti Microsoft"
description: "È possibile definire origini Web o Internet e assegnarle a una società contatto per consentire l'identificazione delle modalità di ricerca delle informazioni sui contatti."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 8106eeca31fb5a5c4528d47a27f897454d5dac58
ms.contentlocale: it-it
ms.lasthandoff: 12/11/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="6dfc2-103">Impostare le origini Web per le società contatto</span><span class="sxs-lookup"><span data-stu-id="6dfc2-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="6dfc2-104">È possibile utilizzare le origini Web con le società contatto per identificare, ad esempio, motori di ricerca e siti Web dove effettuare la ricerca di informazioni sui contatti.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="6dfc2-105">Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="6dfc2-106">L'utilizzo delle origini Web nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="6dfc2-107">Innanzitutto, occorre definire il codice origine Web.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-107">First, you define the web source code.</span></span> <span data-ttu-id="6dfc2-108">Questo passaggio deve essere eseguito una sola volta per ogni origine Web.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="6dfc2-109">Dopo aver creato un codice origine Web, è possibile iniziare ad assegnarlo ai contatti.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="6dfc2-110">Per definire un codice origine Web</span><span class="sxs-lookup"><span data-stu-id="6dfc2-110">To define a web source code</span></span>
1. <span data-ttu-id="6dfc2-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Origini Web** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="6dfc2-112">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="6dfc2-113">Compilare i campi **Codice**, **Descrizione** e **URL**.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="6dfc2-114">Nel campo **URL** immettere %1 per inserire un segnaposto per una parola di ricerca nell'URL.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="6dfc2-115">Quando si apre l'origine Web da un contatto, %1 verrà automaticamente sostituito con la parola da ricercare (ad esempio il nome della società) inserita nella pagina **Origini Web contatto**.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered on the **Contact Web Sources** page.</span></span>

<span data-ttu-id="6dfc2-116">Ripetere tali passaggi per impostare altre origini Web.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="6dfc2-117">Per assegnare origini Web a una società contatto</span><span class="sxs-lookup"><span data-stu-id="6dfc2-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="6dfc2-118">Quando si assegna un'origine Web, specificare il motore di ricerca e la parola di ricerca che saranno utilizzati per individuare le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="6dfc2-119">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-119">Open the contact.</span></span>
2. <span data-ttu-id="6dfc2-120">Scegliere l'azione **Società**, quindi l'azione **Origini Web**.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="6dfc2-121">Verrà visualizzata la pagina **Origine Web contatto**.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-121">The **Contact Web Sources** page opens.</span></span>
3. <span data-ttu-id="6dfc2-122">Nel campo **Codice origine Web** scegliere l'origine Web che si desidera assegnare.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="6dfc2-123">Nel campo **Parola ricerca** inserire la parola ricerca che verrà utilizzata per individuare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="6dfc2-124">Ripetere tali passaggi per assegnare altre origini Web.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="6dfc2-125">È inoltre possibile assegnare l'origine Web dalla pagina **Lista Contatti** seguendo la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="6dfc2-125">You can also assign web sources from the **Contact List** page by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dfc2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6dfc2-126">See Also</span></span>
[<span data-ttu-id="6dfc2-127">Creazione di società contatto</span><span class="sxs-lookup"><span data-stu-id="6dfc2-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="6dfc2-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6dfc2-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

