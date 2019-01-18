---
title: Definire i documenti in entrata da visualizzare| Documenti Microsoft
description: Modificare la visualizzazione di default dei documenti in entrata, ad esempio le fatture elettroniche, per migliorare la panoramica dei record elaborati e non elaborati.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 97ca5aab24b04f6c2d0677c6fd9626b93fcd8ca8
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="82c83-103">Gestire più record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="82c83-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="82c83-104">Quando si creano o elaborate i record del documento in entrata, il numero delle righe della pagina **Documenti in entrata** possono aumentare fino a perdere la visibilità di una panoramica.</span><span class="sxs-lookup"><span data-stu-id="82c83-104">As you create or process incoming document records, the number of lines on the **Incoming Documents** page may grow to an extent where you lose overview.</span></span> <span data-ttu-id="82c83-105">Di conseguenza, è possibile impostare i record del documento in entrata su Elaborato per rimuoverli dalla visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="82c83-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="82c83-106">Scegliendo l'azione **Mostra tutto** è possibile visualizzare sia i record elaborati che non elaborati.</span><span class="sxs-lookup"><span data-stu-id="82c83-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="82c83-107">Non è possibile modificare le informazioni, allegare i file o eseguire altri processi sui record del documento in entrata che sono impostati su Elaborato.</span><span class="sxs-lookup"><span data-stu-id="82c83-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="82c83-108">È necessario innanzitutto impostare lo stato Non elaborato.</span><span class="sxs-lookup"><span data-stu-id="82c83-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="82c83-109">La casella di controllo **Elaborato** viene selezionata automaticamente sui record del documento in entrata che sono stati elaborati, ma è anche possibile selezionare o deselezionare la casella di controllo manualmente.</span><span class="sxs-lookup"><span data-stu-id="82c83-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="82c83-110">In base al processo aziendale, un record del documento in entrata può essere elaborato solo quando è stato creato un documento ad esso correlato oppure è stato allegato un file.</span><span class="sxs-lookup"><span data-stu-id="82c83-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="82c83-111">Se si apre la pagina **Documenti in entrata** usando l'azione **Documenti in entrata personali** in Gestione ruolo utente, solo i record del documento in entrata non elaborati vengono visualizzati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="82c83-111">When you open the **Incoming Documents** page with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="82c83-112">In questo argomento questa visualizzazione viene indicata come "la visualizzazione predefinita".</span><span class="sxs-lookup"><span data-stu-id="82c83-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="82c83-113">Per rimuovere i record del documento in entrata dalla visualizzazione predefinita</span><span class="sxs-lookup"><span data-stu-id="82c83-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="82c83-114">Nella pagina **Documenti in entrata** selezionare una o più righe dei record del documento in entrata che si desidera rimuovere dalla visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="82c83-114">On the **Incoming Documents** page, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="82c83-115">Scegliere l'azione **Imposta su elaborato**.</span><span class="sxs-lookup"><span data-stu-id="82c83-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="82c83-116">I record in entrata del documento vengono eliminate dalla visualizzazione predefinita e viene selezionata la casella di controllo **Elaborato** nelle righe.</span><span class="sxs-lookup"><span data-stu-id="82c83-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="82c83-117">È inoltre possibile eseguire questa azione per il singolo record nella pagina **Scheda Documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="82c83-117">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="82c83-118">Per visualizzare tutti i record dei documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="82c83-118">To view all incoming document records</span></span>
1. <span data-ttu-id="82c83-119">In alternativa, nella pagina **Setup documenti in entrata** scegliere l'azione **Mostra tutto**.</span><span class="sxs-lookup"><span data-stu-id="82c83-119">On the **Incoming Documents** page, choose the **Show All** action.</span></span>

<span data-ttu-id="82c83-120">Tutti i record del documento in entrata vengono visualizzati, inclusi quelli in cui non è selezionata la casella di controllo **Elaborato**.</span><span class="sxs-lookup"><span data-stu-id="82c83-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="82c83-121">Per aggiungere i record del documento in entrata alla visualizzazione predefinita</span><span class="sxs-lookup"><span data-stu-id="82c83-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="82c83-122">In alternativa, nella pagina **Setup documenti in entrata** scegliere l'azione **Mostra tutto**.</span><span class="sxs-lookup"><span data-stu-id="82c83-122">On the **Incoming Documents** page, choose the **Show All** action.</span></span>
2. <span data-ttu-id="82c83-123">Selezionare una o più righe per i record del documento in entrata che si desidera mostrare nella visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="82c83-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="82c83-124">Scegliere l'azione **Imposta su non elaborato**.</span><span class="sxs-lookup"><span data-stu-id="82c83-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="82c83-125">È inoltre possibile eseguire questa azione per il singolo record nella pagina **Scheda Documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="82c83-125">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="82c83-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82c83-126">See Also</span></span>
[<span data-ttu-id="82c83-127">Elaborare i documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="82c83-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="82c83-128">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="82c83-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="82c83-129">Acquisti</span><span class="sxs-lookup"><span data-stu-id="82c83-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="82c83-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82c83-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

