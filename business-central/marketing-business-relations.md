---
title: Definire codici di relazioni d'affari per i contatti| Documenti Microsoft
description: Utilizzare le relazioni d'affari in Business Central per supportare il marketing e per indicare il tipo di relazione commerciale che intercorre con prospetti e clienti, ad esempio, una banca o un fornitore di servizi.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ffeb19820b29453750ca9c03258d455dddff287c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "941867"
---
# <a name="setting-up-business-relations-on-contacts"></a><span data-ttu-id="0b721-103">Impostazione delle relazioni d'affari nei contatti</span><span class="sxs-lookup"><span data-stu-id="0b721-103">Setting Up Business Relations on Contacts</span></span>
<span data-ttu-id="0b721-104">È possibile utilizzare le relazioni d'affari vengono utilizzate per indicare il tipo di relazione commerciale che intercorre con i contatti, ad esempio potenziale cliente, banca, consulente e fornitore di servizi e così via.</span><span class="sxs-lookup"><span data-stu-id="0b721-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="0b721-105">L'utilizzo delle relazioni d'affari nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="0b721-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="0b721-106">Innanzitutto, occorre definire il codice relazioni d'affari.</span><span class="sxs-lookup"><span data-stu-id="0b721-106">First, you define the business relation code.</span></span> <span data-ttu-id="0b721-107">Questo passaggio deve essere eseguito una sola volta per ogni relazione d'affari.</span><span class="sxs-lookup"><span data-stu-id="0b721-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="0b721-108">Dopo aver creato un codice di relazione d'affari, è possibile iniziare ad assegnarlo alle società.</span><span class="sxs-lookup"><span data-stu-id="0b721-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0b721-109">Per sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.</span><span class="sxs-lookup"><span data-stu-id="0b721-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="0b721-110">Per definire un codice relazioni d'affari</span><span class="sxs-lookup"><span data-stu-id="0b721-110">To define a business relation code</span></span>
<span data-ttu-id="0b721-111">Il codice relazione d'affari definisce una categoria o un tipo della relazione d'affari, ad esempio BANCA o Legge.</span><span class="sxs-lookup"><span data-stu-id="0b721-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="0b721-112">È possibile impostare più codici di relazione d'affari.</span><span class="sxs-lookup"><span data-stu-id="0b721-112">You can have several business relation codes.</span></span> <span data-ttu-id="0b721-113">Per definire la relazione d'affari, utilizzare la pagina **Relazioni d'affari**.</span><span class="sxs-lookup"><span data-stu-id="0b721-113">To define the business relation, you use the **Business Relations** page.</span></span>

1. <span data-ttu-id="0b721-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Relazioni d'affari** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0b721-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="0b721-115">Selezionare l'azione **Nuovo** e immettere un codice e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="0b721-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="0b721-116">Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.</span><span class="sxs-lookup"><span data-stu-id="0b721-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="0b721-117">Per assegnare relazioni d'affari a un contatto</span><span class="sxs-lookup"><span data-stu-id="0b721-117">To assign business relations to a contact</span></span>
<span data-ttu-id="0b721-118">Non è possibile assegnare relazioni d'affari a un contatto, ma solo alle società.</span><span class="sxs-lookup"><span data-stu-id="0b721-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="0b721-119">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="0b721-119">Open the contact.</span></span>
2. <span data-ttu-id="0b721-120">Scegliere l'azione **Società**, quindi l'azione **Relazioni d'affari**.</span><span class="sxs-lookup"><span data-stu-id="0b721-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="0b721-121">Verrà aperta la pagina **Relazioni d'affari contatto**.</span><span class="sxs-lookup"><span data-stu-id="0b721-121">The **Contact Business Relations** page opens.</span></span>
3. <span data-ttu-id="0b721-122">Nel campo **Codice relazione d'affari** selezionare la relazione d'affari da assegnare.</span><span class="sxs-lookup"><span data-stu-id="0b721-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="0b721-123">Ripetere questi passaggi per assegnare altre relazioni d'affari.</span><span class="sxs-lookup"><span data-stu-id="0b721-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="0b721-124">È inoltre possibile assegnare altre relazioni d'affari dalla lista Contatti seguendo la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="0b721-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="0b721-125">Il numero di relazioni d'affari assegnate al contatto viene visualizzato nel campo **Nr. relazione d'affari** nella sezione **Segmentazione** nella pagina **Contatto**.</span><span class="sxs-lookup"><span data-stu-id="0b721-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="0b721-126">Una volta assegnate le relazioni d'affari ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="0b721-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="0b721-127">Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="0b721-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0b721-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b721-128">See Also</span></span>
<span data-ttu-id="0b721-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0b721-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
