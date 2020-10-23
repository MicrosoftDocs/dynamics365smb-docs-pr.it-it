---
title: Impostare documenti in entrata| Documenti Microsoft
description: Utilizzare la funzione Documenti in entrata per creare documenti elettronici, gestire le attività OCR, importare le fatture e convertire i file immagine.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0be6c730664d5162bd2359e029f9a387eae0d5d8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915912"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="03da9-103">Impostare documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="03da9-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="03da9-104">Se si creano righe registrazioni COGE da record di documenti in entrata, è necessario specificare nella pagina **Setup documenti in entrata** quale definizione registrazioni e quale batch contabile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="03da9-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="03da9-105">Se non si desidera che gli utenti creino fatture o righe registrazioni COGE dai record di documenti in arrivo prima che i documenti siano approvati, è necessario impostare i responsabili dell'approvazione.</span><span class="sxs-lookup"><span data-stu-id="03da9-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="03da9-106">Per trasformare file PDF e file di immagine in documenti elettronici convertibili, ad esempio, in fatture di acquisto [!INCLUDE[d365fin](includes/d365fin_md.md)]', è necessario innanzitutto impostare la funzionalità OCR e abilitare il servizio.</span><span class="sxs-lookup"><span data-stu-id="03da9-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span> <span data-ttu-id="03da9-107">Scegliere un pacchetto di servizi appropriato per l'organizzazione e/o paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="03da9-107">Choose a service package that is appropriate for your organization and/or country/region.</span></span> <span data-ttu-id="03da9-108">In alternativa, è possibile creare manualmente voci per rappresentare i documenti esterni.</span><span class="sxs-lookup"><span data-stu-id="03da9-108">Alternatively, you can create entries manually to represent the external documents.</span></span>  

<span data-ttu-id="03da9-109">Se la funzionalità Documenti in entrata è impostata, è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="03da9-109">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="03da9-110">I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti.</span><span class="sxs-lookup"><span data-stu-id="03da9-110">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="03da9-111">Per ulteriori informazioni, vedere [Elaborazione di documenti in entrata](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="03da9-111">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="03da9-112">Per impostare la funzione Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="03da9-112">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="03da9-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup documenti in entrata** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="03da9-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="03da9-114">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="03da9-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="03da9-115">Come parte del setup, è necessario decidere se si desidera richiedere l'approvazione dei documenti in arrivo.</span><span class="sxs-lookup"><span data-stu-id="03da9-115">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="03da9-116">Per richiedere l'approvazione, è necessario impostare responsabili approvazione e workflow di approvazione.</span><span class="sxs-lookup"><span data-stu-id="03da9-116">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="03da9-117">Se l'organizzazione non intende richiedere l'approvazione, è possibile ignorare la sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="03da9-117">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="03da9-118">Infine, se si utilizza un servizio per convertire file PDF o di immagine che rappresentano documenti in arrivo, è necessario configurarlo.</span><span class="sxs-lookup"><span data-stu-id="03da9-118">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="03da9-119">In caso contrario, è possibile ignorare anche quella sezione.</span><span class="sxs-lookup"><span data-stu-id="03da9-119">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="03da9-120">Per impostare i responsabili dell'approvazione dei record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="03da9-120">To set up approvers of incoming document records</span></span>

<span data-ttu-id="03da9-121">Facoltativamente, impostare un processo di approvazione per i documenti in arrivo.</span><span class="sxs-lookup"><span data-stu-id="03da9-121">Optionally, set up an approval process for the incoming documents.</span></span> <span data-ttu-id="03da9-122">I responsabili dell'approvazione dei documenti in ingresso devono essere impostati come utenti del workflow di approvazione.</span><span class="sxs-lookup"><span data-stu-id="03da9-122">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="03da9-123">Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione.</span><span class="sxs-lookup"><span data-stu-id="03da9-123">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="03da9-124">Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale.</span><span class="sxs-lookup"><span data-stu-id="03da9-124">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="03da9-125">Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="03da9-125">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="03da9-126">Per impostare un servizio OCR</span><span class="sxs-lookup"><span data-stu-id="03da9-126">To set up an OCR service</span></span>

1. <span data-ttu-id="03da9-127">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup servizio OCR** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="03da9-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="03da9-128">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="03da9-128">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="03da9-129">I dati di accesso vengono automaticamente crittografati.</span><span class="sxs-lookup"><span data-stu-id="03da9-129">You login data is automatically encrypted.</span></span>

<span data-ttu-id="03da9-130">Per ulteriori informazioni, vedere [Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="03da9-130">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="03da9-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03da9-131">See Also</span></span>

[<span data-ttu-id="03da9-132">Elaborare i documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="03da9-132">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="03da9-133">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="03da9-133">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="03da9-134">Acquisti</span><span class="sxs-lookup"><span data-stu-id="03da9-134">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="03da9-135">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="03da9-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
