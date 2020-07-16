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
ms.date: 06/23/2020
ms.author: sgroespe
ms.openlocfilehash: 09047315c701bd2076f59b6c3f4840ba95eb06cc
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503546"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="fe74a-103">Impostare documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="fe74a-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="fe74a-104">Se si creano righe registrazioni COGE da record di documenti in entrata, è necessario specificare nella pagina **Setup documenti in entrata** quale definizione registrazioni e quale batch contabile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="fe74a-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="fe74a-105">Se non si desidera che gli utenti creino fatture o righe registrazioni COGE dai record di documenti in arrivo prima che i documenti siano approvati, è necessario impostare i responsabili dell'approvazione.</span><span class="sxs-lookup"><span data-stu-id="fe74a-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="fe74a-106">Per trasformare file PDF e file di immagine in documenti elettronici convertibili, ad esempio, in fatture di acquisto [!INCLUDE[d365fin](includes/d365fin_md.md)]', è necessario innanzitutto impostare la funzionalità OCR e abilitare il servizio.</span><span class="sxs-lookup"><span data-stu-id="fe74a-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="fe74a-107">Se la funzionalità Documenti in entrata è impostata, è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="fe74a-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="fe74a-108">I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti.</span><span class="sxs-lookup"><span data-stu-id="fe74a-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="fe74a-109">Per ulteriori informazioni, vedere [Elaborazione di documenti in entrata](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="fe74a-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="fe74a-110">Per impostare la funzione Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="fe74a-110">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="fe74a-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup documenti in entrata** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fe74a-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe74a-112">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="fe74a-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="fe74a-113">Come parte del setup, è necessario decidere se si desidera richiedere l'approvazione dei documenti in arrivo.</span><span class="sxs-lookup"><span data-stu-id="fe74a-113">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="fe74a-114">Per richiedere l'approvazione, è necessario impostare responsabili approvazione e workflow di approvazione.</span><span class="sxs-lookup"><span data-stu-id="fe74a-114">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="fe74a-115">Se l'organizzazione non intende richiedere l'approvazione, è possibile ignorare la sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="fe74a-115">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="fe74a-116">Infine, se si utilizza un servizio per convertire file PDF o di immagine che rappresentano documenti in arrivo, è necessario configurarlo.</span><span class="sxs-lookup"><span data-stu-id="fe74a-116">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="fe74a-117">In caso contrario, è possibile ignorare anche quella sezione.</span><span class="sxs-lookup"><span data-stu-id="fe74a-117">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="fe74a-118">Per impostare i responsabili dell'approvazione dei record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="fe74a-118">To set up approvers of incoming document records</span></span>

<span data-ttu-id="fe74a-119">I responsabili dell'approvazione dei documenti in ingresso devono essere impostati come utenti del workflow di approvazione.</span><span class="sxs-lookup"><span data-stu-id="fe74a-119">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="fe74a-120">Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione.</span><span class="sxs-lookup"><span data-stu-id="fe74a-120">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="fe74a-121">Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale.</span><span class="sxs-lookup"><span data-stu-id="fe74a-121">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="fe74a-122">Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="fe74a-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="fe74a-123">Per impostare un servizio OCR</span><span class="sxs-lookup"><span data-stu-id="fe74a-123">To set up an OCR service</span></span>

1. <span data-ttu-id="fe74a-124">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup servizio OCR** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fe74a-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe74a-125">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="fe74a-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="fe74a-126">I dati di accesso vengono automaticamente crittografati.</span><span class="sxs-lookup"><span data-stu-id="fe74a-126">You login data is automatically encrypted.</span></span>

<span data-ttu-id="fe74a-127">Per ulteriori informazioni, vedere [Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="fe74a-127">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="fe74a-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fe74a-128">See Also</span></span>

[<span data-ttu-id="fe74a-129">Elaborare i documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="fe74a-129">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="fe74a-130">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="fe74a-130">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="fe74a-131">Acquisti</span><span class="sxs-lookup"><span data-stu-id="fe74a-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="fe74a-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fe74a-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
