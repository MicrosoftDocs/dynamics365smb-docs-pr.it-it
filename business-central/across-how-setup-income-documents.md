---
title: Impostare documenti in entrata| Documenti Microsoft
description: Utilizzare la funzione Documenti in entrata per creare documenti elettronici, gestire le attività OCR, importare le fatture e convertire i file immagine.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 12/09/2019
ms.author: sgroespe
ms.openlocfilehash: e67ca1c0b26d7e4a81e53854ca31efc64a366c3f
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910494"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="f8ed6-103">Impostare documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="f8ed6-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="f8ed6-104">Se si creano righe registrazioni COGE da record di documenti in entrata, è necessario specificare nella pagina **Setup documenti in entrata** quale definizione registrazioni e quale batch contabile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="f8ed6-105">Se non si desidera che gli utenti creino fatture o righe registrazioni COGE dai record di documenti in arrivo prima che i documenti siano approvati, è necessario impostare i responsabili dell'approvazione.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="f8ed6-106">Per trasformare file PDF e file di immagine in documenti elettronici convertibili, ad esempio, in fatture di acquisto [!INCLUDE[d365fin](includes/d365fin_md.md)]', è necessario innanzitutto impostare la funzionalità OCR e abilitare il servizio.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="f8ed6-107">Se la funzionalità Documenti in entrata è impostata, è possibile utilizzare diverse funzioni per esaminare le ricevute relative alle spese, gestire le attività OCR e convertire i file dei documenti in entrata, manualmente o automaticamente, nei relativi documenti o in righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="f8ed6-108">I file esterni possono essere allegati in qualsiasi fase dell'elaborazione, ad esempio ai documenti registrati, nonché ai fornitori, clienti e movimenti di contabilità generale risultanti.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="f8ed6-109">Per ulteriori informazioni, vedere [Elaborazione di documenti in entrata](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="f8ed6-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="f8ed6-110">Per impostare la funzione Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="f8ed6-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="f8ed6-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup documenti in entrata** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f8ed6-112">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="f8ed6-113">Per impostare i responsabili dell'approvazione dei record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="f8ed6-113">To set up approvers of incoming document records</span></span>
<span data-ttu-id="f8ed6-114">I responsabili dell'approvazione dei documenti in ingresso devono essere impostati come utenti del workflow di approvazione.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-114">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="f8ed6-115">Prima di creare workflow che coinvolgono passaggi di approvazione, è necessario impostare gli utenti del workflow coinvolti nei processi di approvazione.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-115">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="f8ed6-116">Nella pagina **Setup utente approvazione** è possibile anche impostare i limiti quantitativi per specifici tipi di richiesta e definire i responsabili di approvazione sostitutivi ai quali vengono delegate le richieste di approvazione in assenza del responsabile originale.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-116">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="f8ed6-117">Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="f8ed6-117">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="f8ed6-118">Per impostare un servizio OCR</span><span class="sxs-lookup"><span data-stu-id="f8ed6-118">To set up an OCR service</span></span>
1. <span data-ttu-id="f8ed6-119">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup servizio OCR** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f8ed6-120">Compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="f8ed6-121">I dati di accesso vengono automaticamente crittografati.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-121">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8ed6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8ed6-122">See Also</span></span>
[<span data-ttu-id="f8ed6-123">Elaborare i documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="f8ed6-123">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="f8ed6-124">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="f8ed6-124">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="f8ed6-125">Acquisti</span><span class="sxs-lookup"><span data-stu-id="f8ed6-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f8ed6-126">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8ed6-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
