---
title: Impostare i livelli organizzativi per i contatti| Documenti Microsoft
description: È possibile definire un livello organizzativo e assegnarlo al contatto per indicare la posizione all'interno della rispettiva società, ad esempio alta dirigenza.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: a3c3d33bf7ceaf2bd0f5fae4c4513b1769ed3092
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308838"
---
# <a name="set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="947a5-103">Configurare i livelli organizzativi per i contatti</span><span class="sxs-lookup"><span data-stu-id="947a5-103">Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="947a5-104">È possibile usare i livelli organizzativi con i contatti per specificarne la posizione all'interno della società, ad esempio alta dirigenza.</span><span class="sxs-lookup"><span data-stu-id="947a5-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="947a5-105">È possibile utilizzare queste informazioni quando si inseriscono informazioni sui contatti.</span><span class="sxs-lookup"><span data-stu-id="947a5-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="947a5-106">L'utilizzo dei livelli organizzativi nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="947a5-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="947a5-107">Innanzitutto, occorre definire il codice livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="947a5-107">First, you define the organizational level code.</span></span> <span data-ttu-id="947a5-108">Questo passaggio deve essere eseguito una sola volta per ogni livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="947a5-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="947a5-109">Dopo aver creato un codice livello organizzativo, è possibile iniziare ad assegnarlo ai contatti.</span><span class="sxs-lookup"><span data-stu-id="947a5-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="947a5-110">Per definire un codice livello organizzativo</span><span class="sxs-lookup"><span data-stu-id="947a5-110">To define an organizational level code</span></span>
<span data-ttu-id="947a5-111">Il codice livello organizzativo definisce il tipo o la categoria di livello organizzativo, ad esempio CEO o CFO.</span><span class="sxs-lookup"><span data-stu-id="947a5-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="947a5-112">È possibile impostare più codici di livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="947a5-112">You can have several organizational level codes.</span></span> <span data-ttu-id="947a5-113">Per definire il livello organizzativo, utilizzare la pagina **Livelli organizzativi**.</span><span class="sxs-lookup"><span data-stu-id="947a5-113">To define the organizational level, you use the **Organizational Levels** page.</span></span>

1. <span data-ttu-id="947a5-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Livelli organizzativi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="947a5-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="947a5-115">Selezionare l'azione **Nuovo** e immettere un codice e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="947a5-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="947a5-116">Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.</span><span class="sxs-lookup"><span data-stu-id="947a5-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="947a5-117">Per assegnare livelli organizzativi a un contatto</span><span class="sxs-lookup"><span data-stu-id="947a5-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="947a5-118">È possibile assegnare un livello organizzativo ai contatti costituiti da persone, non alle società contatto.</span><span class="sxs-lookup"><span data-stu-id="947a5-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="947a5-119">È possibile assegnare un livello organizzativo a ciascun contatto.</span><span class="sxs-lookup"><span data-stu-id="947a5-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="947a5-120">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="947a5-120">Open the contact.</span></span>
2. <span data-ttu-id="947a5-121">Nel campo **Livelli organizzativi** scegliere il codice che si desidera assegnare.</span><span class="sxs-lookup"><span data-stu-id="947a5-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="947a5-122">Una volta assegnati livelli organizzativi ai contatti, è possibile utilizzare queste informazioni per la creazione di segmenti.</span><span class="sxs-lookup"><span data-stu-id="947a5-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="947a5-123">Dopo avere assegnato i ruoli professionali ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="947a5-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="947a5-124">Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="947a5-124">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="947a5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="947a5-125">See Also</span></span>
[<span data-ttu-id="947a5-126">Creazione di contatti</span><span class="sxs-lookup"><span data-stu-id="947a5-126">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="947a5-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="947a5-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
