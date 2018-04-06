---
title: Impostare i livelli organizzativi per i contatti| Documenti Microsoft
description: "È possibile definire un livello organizzativo e assegnarlo al contatto per indicare la posizione all'interno della rispettiva società, ad esempio alta dirigenza."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5b6934b6ea4c07f6e3d90885dfa25d73e14bbb82
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="d5d73-103">Configurare i livelli organizzativi per i contatti</span><span class="sxs-lookup"><span data-stu-id="d5d73-103">Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="d5d73-104">È possibile usare i livelli organizzativi con i contatti per specificarne la posizione all'interno della società, ad esempio alta dirigenza.</span><span class="sxs-lookup"><span data-stu-id="d5d73-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="d5d73-105">È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.</span><span class="sxs-lookup"><span data-stu-id="d5d73-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="d5d73-106">L'utilizzo dei livelli organizzativi nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="d5d73-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="d5d73-107">Innanzitutto, occorre definire il codice livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="d5d73-107">First, you define the organizational level code.</span></span> <span data-ttu-id="d5d73-108">Questo passaggio deve essere eseguito una sola volta per ogni livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="d5d73-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="d5d73-109">Dopo aver creato un codice livello organizzativo, è possibile iniziare ad assegnarlo ai contatti.</span><span class="sxs-lookup"><span data-stu-id="d5d73-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="d5d73-110">Per definire un codice livello organizzativo</span><span class="sxs-lookup"><span data-stu-id="d5d73-110">To define an organizational level code</span></span>
<span data-ttu-id="d5d73-111">Il codice livello organizzativo definisce il tipo o la categoria di livello organizzativo, ad esempio CEO o CFO.</span><span class="sxs-lookup"><span data-stu-id="d5d73-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="d5d73-112">È possibile impostare più codici di livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="d5d73-112">You can have several organizational level codes.</span></span> <span data-ttu-id="d5d73-113">Per definire il livello organizzativo, utilizzare la finestra **Livelli organizzativi**.</span><span class="sxs-lookup"><span data-stu-id="d5d73-113">To define the organizational level, you use the **Organizational Levels** window.</span></span>

1. <span data-ttu-id="d5d73-114">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Livelli organizzativi**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d5d73-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="d5d73-115">Selezionare l'azione **Nuovo** e immettere un codice e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="d5d73-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="d5d73-116">Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.</span><span class="sxs-lookup"><span data-stu-id="d5d73-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="d5d73-117">Per assegnare livelli organizzativi a un contatto</span><span class="sxs-lookup"><span data-stu-id="d5d73-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="d5d73-118">È possibile assegnare un livello organizzativo ai contatti costituiti da persone, non alle società contatto.</span><span class="sxs-lookup"><span data-stu-id="d5d73-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="d5d73-119">È possibile assegnare un livello organizzativo a ciascun contatto.</span><span class="sxs-lookup"><span data-stu-id="d5d73-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="d5d73-120">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="d5d73-120">Open the contact.</span></span>
2. <span data-ttu-id="d5d73-121">Nel campo **Livelli organizzativi** scegliere il codice che si desidera assegnare.</span><span class="sxs-lookup"><span data-stu-id="d5d73-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="d5d73-122">Una volta assegnati livelli organizzativi ai contatti, è possibile utilizzare queste informazioni per la creazione di segmenti.</span><span class="sxs-lookup"><span data-stu-id="d5d73-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="d5d73-123">Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="d5d73-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="d5d73-124">Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="d5d73-124">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d5d73-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5d73-125">See Also</span></span>
[<span data-ttu-id="d5d73-126">Creazione di società contatto</span><span class="sxs-lookup"><span data-stu-id="d5d73-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="d5d73-127">Creazione di contatti</span><span class="sxs-lookup"><span data-stu-id="d5d73-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="d5d73-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5d73-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

