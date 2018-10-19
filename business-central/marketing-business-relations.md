---
title: Definire codici di relazioni d'affari per i contatti| Documenti Microsoft
description: Utilizzare le relazioni d'affari in Business Central per supportare il marketing e per indicare il tipo di relazione commerciale che intercorre con prospetti e clienti, ad esempio, una banca o un fornitore di servizi.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8a950b87b7e7947de1602db76805a0b1f41d8274
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a><span data-ttu-id="bf9f2-103">Impostazione delle relazioni d'affari nelle società contatto</span><span class="sxs-lookup"><span data-stu-id="bf9f2-103">Setting Up Business Relations on Contact Companies</span></span>
<span data-ttu-id="bf9f2-104">È possibile utilizzare le relazioni d'affari vengono utilizzate per indicare il tipo di relazione commerciale che intercorre con i contatti, ad esempio potenziale cliente, banca, consulente e fornitore di servizi e così via.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="bf9f2-105">L'utilizzo delle relazioni d'affari nei contatti è un processo a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="bf9f2-106">Innanzitutto, occorre definire il codice relazioni d'affari.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-106">First, you define the business relation code.</span></span> <span data-ttu-id="bf9f2-107">Questo passaggio deve essere eseguito una sola volta per ogni relazione d'affari.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="bf9f2-108">Dopo aver creato un codice di relazione d'affari, è possibile iniziare ad assegnarlo alle società.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="bf9f2-109">Per sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="bf9f2-110">Per definire un codice relazioni d'affari</span><span class="sxs-lookup"><span data-stu-id="bf9f2-110">To define a business relation code</span></span>
<span data-ttu-id="bf9f2-111">Il codice relazione d'affari definisce una categoria o un tipo della relazione d'affari, ad esempio BANCA o Legge.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="bf9f2-112">È possibile impostare più codici di relazione d'affari.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-112">You can have several business relation codes.</span></span> <span data-ttu-id="bf9f2-113">Per definire la relazione d'affari, utilizzare la finestra **Relazioni d'affari**.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-113">To define the business relation, you use the **Business Relations** window.</span></span>

1. <span data-ttu-id="bf9f2-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Relazioni d'affari** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="bf9f2-115">Selezionare l'azione **Nuovo** e immettere un codice e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="bf9f2-116">Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="bf9f2-117">Per assegnare relazioni d'affari a un contatto</span><span class="sxs-lookup"><span data-stu-id="bf9f2-117">To assign business relations to a contact</span></span>
<span data-ttu-id="bf9f2-118">Non è possibile assegnare relazioni d'affari a un contatto, ma solo alle società.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="bf9f2-119">Aprire il contatto.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-119">Open the contact.</span></span>
2. <span data-ttu-id="bf9f2-120">Scegliere l'azione **Società**, quindi l'azione **Relazioni d'affari**.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="bf9f2-121">Verrà aperta la finestra **Relazioni d'affari contatto**.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-121">The **Contact Business Relations** window opens.</span></span>
3. <span data-ttu-id="bf9f2-122">Nel campo **Codice relazione d'affari** selezionare la relazione d'affari da assegnare.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="bf9f2-123">Ripetere questi passaggi per assegnare altre relazioni d'affari.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="bf9f2-124">È inoltre possibile assegnare altre relazioni d'affari dalla lista Contatti seguendo la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="bf9f2-125">Il numero di relazioni d'affari assegnate al contatto viene visualizzato nel campo **Nr. relazione d'affari** nella sezione **Segmentazione** nella finestra **Contatto**.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="bf9f2-126">Una volta assegnate le relazioni d'affari ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti.</span><span class="sxs-lookup"><span data-stu-id="bf9f2-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="bf9f2-127">Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="bf9f2-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bf9f2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf9f2-128">See Also</span></span>
[<span data-ttu-id="bf9f2-129">Creazione di società contatto</span><span class="sxs-lookup"><span data-stu-id="bf9f2-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="bf9f2-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf9f2-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

