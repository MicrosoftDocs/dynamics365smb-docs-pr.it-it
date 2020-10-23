---
title: Tenere traccia dei segmenti e delle interazioni correlate| Documenti Microsoft
description: Informazioni su come creare segmenti per definire gruppi di contatti e specificare delle interazioni per i segmenti.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6a363007ece179430949d0fc0c62cb9df3fc9dac
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923647"
---
# <a name="manage-interactions-for-segments"></a><span data-ttu-id="61087-103">Gestire interazioni per i segmenti</span><span class="sxs-lookup"><span data-stu-id="61087-103">Manage Interactions for Segments</span></span>
<span data-ttu-id="61087-104">La pagina **Segmento** è una sorta di prospetto in cui è possibile:</span><span class="sxs-lookup"><span data-stu-id="61087-104">The **Segment** page is a type of worksheet where you can:</span></span>

* <span data-ttu-id="61087-105">Creare segmenti.</span><span class="sxs-lookup"><span data-stu-id="61087-105">Create segments.</span></span>
* <span data-ttu-id="61087-106">Salvare i criteri di segmentazione utilizzati per selezionare i contatti.</span><span class="sxs-lookup"><span data-stu-id="61087-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="61087-107">Registrare il segmento e le interazioni che coinvolgono i contatti all'interno del segmento.</span><span class="sxs-lookup"><span data-stu-id="61087-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="61087-108">Segmentazione</span><span class="sxs-lookup"><span data-stu-id="61087-108">Segmenting</span></span>
<span data-ttu-id="61087-109">Esistono numerosi modi per creare segmenti:</span><span class="sxs-lookup"><span data-stu-id="61087-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="61087-110">È possibile inserire manualmente i contatti che si desidera includere nel segmento in corrispondenza delle righe del segmento.</span><span class="sxs-lookup"><span data-stu-id="61087-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="61087-111">È possibile selezionare i contatti:</span><span class="sxs-lookup"><span data-stu-id="61087-111">You can select contacts.</span></span>
* <span data-ttu-id="61087-112">È possibile riutilizzare un segmento registrato come base per la creazione di un nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="61087-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="61087-113">È possibile riutilizzare i criteri di segmentazione creati.</span><span class="sxs-lookup"><span data-stu-id="61087-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="61087-114">Interazioni</span><span class="sxs-lookup"><span data-stu-id="61087-114">Interactions</span></span>
<span data-ttu-id="61087-115">Nella pagina **Segmento** è possibile creare interazioni per più contatti contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="61087-115">On the **Segment** page, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="61087-116">È ad esempio possibile unire un segmento con un documento di Microsoft Word, in modo da inviare una lettera a tutti i contatti all'interno del segmento.</span><span class="sxs-lookup"><span data-stu-id="61087-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="61087-117">È possibile specificare informazioni relative all'interazione di un determinato segmento nella testata **Segmento**.</span><span class="sxs-lookup"><span data-stu-id="61087-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="61087-118">È ad esempio possibile decidere quale modello di interazione utilizzare per tutti i contatti, specificare una descrizione, un tipo di corrispondenza e così via.</span><span class="sxs-lookup"><span data-stu-id="61087-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="61087-119">Queste informazioni possono tuttavia essere modificate nella riga del segmento per ogni contatto, ad esempio specificando un'altra descrizione relativa a un determinato contatto.</span><span class="sxs-lookup"><span data-stu-id="61087-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="61087-120">Se si effettua l'unione tra un segmento e un documento di Microsoft Word, è possibile personalizzare tale documento affinché sia inviato a uno o più contatti all'interno del segmento, ad esempio aggiungendo commenti personalizzati al documento.</span><span class="sxs-lookup"><span data-stu-id="61087-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="61087-121">Registrazione</span><span class="sxs-lookup"><span data-stu-id="61087-121">Logging</span></span>
<span data-ttu-id="61087-122">Facendo clic su **Registrazione** nella pagina **Segmento**, le interazioni vengono salvate nella pagina **Mov. log interazione** e il segmento viene registrato.</span><span class="sxs-lookup"><span data-stu-id="61087-122">On the **Segment** page, when you choose **Log**, the application records the interactions on the **Interaction Log Entry** page, and logs the segment.</span></span> <span data-ttu-id="61087-123">Dopo aver registrato il segmento, è possibile trovarlo solo nella pagina **Segmenti registrati**.</span><span class="sxs-lookup"><span data-stu-id="61087-123">After you have logged the segment, you can only find it on the **Logged Segments** page.</span></span>

<span data-ttu-id="61087-124">Nella pagina **Segmenti registrati**, è possibile decidere di creare un segmento di follow-up contenente gli stessi identici contatti del segmento registrato.</span><span class="sxs-lookup"><span data-stu-id="61087-124">On the **Logged Segments** page, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="61087-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61087-125">See Also</span></span>
[<span data-ttu-id="61087-126">Creare segmenti</span><span class="sxs-lookup"><span data-stu-id="61087-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="61087-127">Creare interazioni per segmenti</span><span class="sxs-lookup"><span data-stu-id="61087-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="61087-128">Gestione dei segmenti</span><span class="sxs-lookup"><span data-stu-id="61087-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="61087-129">Registrazione di interazioni con i contatti</span><span class="sxs-lookup"><span data-stu-id="61087-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="61087-130">Gestione delle opportunità di vendita</span><span class="sxs-lookup"><span data-stu-id="61087-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="61087-131">Creazione e gestione di contatti</span><span class="sxs-lookup"><span data-stu-id="61087-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="61087-132">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="61087-132">Working with Business Central</span></span>](ui-work-product.md)
