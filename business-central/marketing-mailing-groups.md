---
title: Impostazione di gruppi mailing per i contatti| Documenti Microsoft
description: È possibile usare i gruppi di mailing per identificare gruppi di contatti a cui inviare le stesse informazioni, ad esempio per una campagna marketing o promozionale.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 6c089b772c139d0c0e9465f383ab39bd3c125dca
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801347"
---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="06173-103">Impostare i gruppi mailing per i contatti</span><span class="sxs-lookup"><span data-stu-id="06173-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="06173-104">È possibile utilizzare i gruppi mailing per identificare gruppi di contatti a cui inviare le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="06173-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="06173-105">È possibile, ad esempio, impostare un gruppo mailing relativo ai contatti a cui si desidera inviare una notifica di un cambio di ufficio o un altro gruppo per inviare gli auguri delle festività.</span><span class="sxs-lookup"><span data-stu-id="06173-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="06173-106">L'utilizzo dei gruppi mailing nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="06173-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="06173-107">Innanzitutto, occorre definire il codice dei gruppi mailing.</span><span class="sxs-lookup"><span data-stu-id="06173-107">First, you define the mailing group code.</span></span> <span data-ttu-id="06173-108">Questo passaggio deve essere eseguito una sola volta per ogni gruppo mailing.</span><span class="sxs-lookup"><span data-stu-id="06173-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="06173-109">Dopo aver creato un codice di gruppo di mailing, è possibile iniziare ad assegnarlo alle società.</span><span class="sxs-lookup"><span data-stu-id="06173-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="06173-110">Per definire i codici di gruppo di mailing</span><span class="sxs-lookup"><span data-stu-id="06173-110">To define mailing group codes</span></span>
<span data-ttu-id="06173-111">Il codice gruppo mailing definisce il tipo o la categoria del gruppo, ad esempio SPOSTAMENTO per lo spostamento dell'ufficio o AUGURI per gli auguri festivi.</span><span class="sxs-lookup"><span data-stu-id="06173-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="06173-112">È possibile impostare più codici di settori industriali.</span><span class="sxs-lookup"><span data-stu-id="06173-112">You can have several industry group codes.</span></span> <span data-ttu-id="06173-113">Per definire i gruppi mailing, utilizzare la pagina **Gruppi mailing**.</span><span class="sxs-lookup"><span data-stu-id="06173-113">To define the industry groups, you use the **Mailing Groups** page.</span></span>

1. <span data-ttu-id="06173-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Gruppi mailing** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="06173-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="06173-115">Selezionare l'azione **Nuovo** e immettere un codice e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="06173-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="06173-116">Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.</span><span class="sxs-lookup"><span data-stu-id="06173-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="06173-117">Per assegnare gruppi di mailing a un contatto</span><span class="sxs-lookup"><span data-stu-id="06173-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="06173-118">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="06173-118">Open the contact.</span></span>
2. <span data-ttu-id="06173-119">Selezionare l'azione **Gruppi mailing**.</span><span class="sxs-lookup"><span data-stu-id="06173-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="06173-120">Verrà visualizzata la pagina **Gruppi mailing contatto**.</span><span class="sxs-lookup"><span data-stu-id="06173-120">The **Contact Mailing Groups** page opens.</span></span>
3. <span data-ttu-id="06173-121">Nel campo **Codice gruppi mailing** selezionare il gruppo mailing da assegnare.</span><span class="sxs-lookup"><span data-stu-id="06173-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="06173-122">Ripetere tali passaggi per assegnare altri gruppi mailing.</span><span class="sxs-lookup"><span data-stu-id="06173-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="06173-123">È inoltre possibile assegnare altri gruppi di mailing dalla lista contatti seguendo la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="06173-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="06173-124">Il numero di gruppi di mailing assegnati al contatto viene visualizzato nel campo **Nr. di gruppi mailing** nella sezione **Segmentazione** della pagina **Contatto**.</span><span class="sxs-lookup"><span data-stu-id="06173-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="06173-125">Dopo avere assegnato i gruppi di mailing ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="06173-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="06173-126">Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="06173-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="06173-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06173-127">See Also</span></span>
[<span data-ttu-id="06173-128">Creazione di contatti</span><span class="sxs-lookup"><span data-stu-id="06173-128">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="06173-129">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="06173-129">Working with Business Central</span></span>](ui-work-product.md)
