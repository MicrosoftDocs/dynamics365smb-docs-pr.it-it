---
title: Impostazione di gruppi mailing per i contatti| Documenti Microsoft
description: "È possibile usare i gruppi di mailing per identificare gruppi di contatti a cui inviare le stesse informazioni, ad esempio per una campagna marketing o promozionale."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 92173c1df5f105ad9156c34ab7050ef1546127bc
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="cf1eb-103">Impostare i gruppi mailing per i contatti</span><span class="sxs-lookup"><span data-stu-id="cf1eb-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="cf1eb-104">È possibile utilizzare i gruppi mailing per identificare gruppi di contatti a cui inviare le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="cf1eb-105">È possibile, ad esempio, impostare un gruppo mailing relativo ai contatti a cui si desidera inviare una notifica di un cambio di ufficio o un altro gruppo per inviare gli auguri delle festività.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="cf1eb-106">L'utilizzo dei gruppi mailing nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="cf1eb-107">Innanzitutto, occorre definire il codice dei gruppi mailing.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-107">First, you define the mailing group code.</span></span> <span data-ttu-id="cf1eb-108">Questo passaggio deve essere eseguito una sola volta per ogni gruppo mailing.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="cf1eb-109">Dopo aver creato un codice di gruppo di mailing, è possibile iniziare ad assegnarlo alle società.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="cf1eb-110">Per definire i codici di gruppo di mailing</span><span class="sxs-lookup"><span data-stu-id="cf1eb-110">To define mailing group codes</span></span>
<span data-ttu-id="cf1eb-111">Il codice gruppo mailing definisce il tipo o la categoria del gruppo, ad esempio SPOSTAMENTO per lo spostamento dell'ufficio o AUGURI per gli auguri festivi.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="cf1eb-112">È possibile impostare più codici di settori industriali.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-112">You can have several industry group codes.</span></span> <span data-ttu-id="cf1eb-113">Per definire i gruppi mailing, utilizzare la finestra **Gruppi mailing**.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="cf1eb-114">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Gruppi mailing**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf1eb-115">Selezionare l'azione **Nuovo** e immettere un codice e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="cf1eb-116">Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="cf1eb-117">Per assegnare gruppi di mailing a un contatto</span><span class="sxs-lookup"><span data-stu-id="cf1eb-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="cf1eb-118">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-118">Open the contact.</span></span>
2. <span data-ttu-id="cf1eb-119">Selezionare l'azione **Gruppi mailing**.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="cf1eb-120">Verrà visualizzata la finestra **Gruppi mailing contatto**.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="cf1eb-121">Nel campo **Codice gruppi mailing** selezionare il gruppo mailing da assegnare.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="cf1eb-122">Ripetere tali passaggi per assegnare altri gruppi mailing.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="cf1eb-123">È inoltre possibile assegnare altri gruppi di mailing dalla lista contatti seguendo la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="cf1eb-124">Il numero di gruppi di mailing assegnati al contatto viene visualizzato nel campo **Nr. di gruppi mailing** nella sezione **Segmentazione** della finestra **Contatto**.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="cf1eb-125">Dopo avere assegnato i gruppi di mailing ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="cf1eb-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="cf1eb-126">Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="cf1eb-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cf1eb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf1eb-127">See Also</span></span>
[<span data-ttu-id="cf1eb-128">Creazione di società contatto</span><span class="sxs-lookup"><span data-stu-id="cf1eb-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="cf1eb-129">Creazione di contatti</span><span class="sxs-lookup"><span data-stu-id="cf1eb-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="cf1eb-130">Utilizzo di Financials</span><span class="sxs-lookup"><span data-stu-id="cf1eb-130">Working with Financials</span></span>](ui-work-product.md)

