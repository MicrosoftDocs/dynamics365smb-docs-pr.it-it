---
title: "Impostazione di settori industriali per le società contatto| Documenti Microsoft"
description: "Descrive come definire un settore industriale e assegnarlo a una società contatto, ad esempio il settore del commercio al dettaglio o dell'industria automobilistica."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fef570e7e56e348a25ae660fa9248b529d0bfde
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="6b6ff-103">Procedura: Impostare settori industriali per le società contatto</span><span class="sxs-lookup"><span data-stu-id="6b6ff-103">How to: Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="6b6ff-104">I gruppi industriali vengono utilizzati per indicare il tipo di settore industriale a cui appartengono i contatti, ad esempio il settore del commercio al dettaglio o l'industria automobilistica.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="6b6ff-105">L'utilizzo dei settori industriali nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="6b6ff-106">Innanzitutto, occorre definire il codice dei settori industriali.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-106">First, you define the industry group code.</span></span> <span data-ttu-id="6b6ff-107">Questo passaggio deve essere eseguito una sola volta per ogni settore industriale.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="6b6ff-108">Dopo aver creato un codice di settore industriale, è possibile iniziare ad assegnarlo alle società.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6b6ff-109">Per sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="6b6ff-110">Per definire un codice di settore industriale</span><span class="sxs-lookup"><span data-stu-id="6b6ff-110">To define an industry group code</span></span>
<span data-ttu-id="6b6ff-111">Il codice settore industriale definisce il tipo o la categoria del gruppo, ad esempio ANNUNCIO per la pubblicità o STAMPA per la TV e la radio.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="6b6ff-112">È possibile impostare più codici di settori industriali.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-112">You can have several industry group codes.</span></span> <span data-ttu-id="6b6ff-113">Per definire i settori industriali, utilizzare la finestra **Settori industriali**.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="6b6ff-114">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Settori industriali**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="6b6ff-115">Selezionare l'azione **Nuovo** e immettere un codice e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="6b6ff-116">Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="6b6ff-117"><a name="AssignIndustryGroupContact"></a> Per assegnare settori industriali a un contatto</span><span class="sxs-lookup"><span data-stu-id="6b6ff-117"><a name="AssignIndustryGroupContact"></a> To assign industry groups to a contact</span></span>
<span data-ttu-id="6b6ff-118">Non è possibile assegnare i settori industriali a un contatto, ma solo alle società.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="6b6ff-119">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-119">Open the contact.</span></span>
2. <span data-ttu-id="6b6ff-120">Scegliere l'azione **Società**, quindi l'azione **Settori industriali**.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="6b6ff-121">Verrà visualizzata la finestra **Settori industriali contatto**.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="6b6ff-122">Nel campo **Codice settore industriale** selezionare il settore industriale da assegnare.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="6b6ff-123">Ripetere tali passaggi per assegnare altri settori industriali.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="6b6ff-124">È inoltre possibile assegnare settori industriali nella finestra Lista Contatti seguendo la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="6b6ff-125">Il numero di settori industriali assegnati al contatto è visibile nel campo **Nr. settori industriali** della sezione **Segmentazione** della finestra **Contatto**.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="6b6ff-126">Una volta assegnati i settori industriali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="6b6ff-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="6b6ff-127">Per ulteriori informazioni, vedere [Procedura: aggiungere contatti ai segmenti](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="6b6ff-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6b6ff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b6ff-128">See Also</span></span>
[<span data-ttu-id="6b6ff-129">Creazione di società contatto</span><span class="sxs-lookup"><span data-stu-id="6b6ff-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="6b6ff-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6b6ff-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

