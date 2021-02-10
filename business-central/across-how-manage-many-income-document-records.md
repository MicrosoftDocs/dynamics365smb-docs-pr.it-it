---
title: Definire i documenti in entrata da visualizzare| Documenti Microsoft
description: Modificare la visualizzazione di default dei documenti in entrata, ad esempio le fatture elettroniche, per migliorare la panoramica dei record elaborati e non elaborati.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6ff52767bbd0a5661cad2dd80abb20885f3fca6d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754944"
---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="26e64-103">Gestire più record di documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="26e64-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="26e64-104">Quando si creano o elaborate i record del documento in entrata, il numero delle righe della pagina **Documenti in entrata** possono aumentare fino a perdere la visibilità di una panoramica.</span><span class="sxs-lookup"><span data-stu-id="26e64-104">As you create or process incoming document records, the number of lines on the **Incoming Documents** page may grow to an extent where you lose overview.</span></span> <span data-ttu-id="26e64-105">Di conseguenza, è possibile impostare i record del documento in entrata su Elaborato per rimuoverli dalla visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26e64-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="26e64-106">Scegliendo l'azione **Mostra tutto** è possibile visualizzare sia i record elaborati che non elaborati.</span><span class="sxs-lookup"><span data-stu-id="26e64-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="26e64-107">Non è possibile modificare le informazioni, allegare i file o eseguire altri processi sui record del documento in entrata che sono impostati su Elaborato.</span><span class="sxs-lookup"><span data-stu-id="26e64-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="26e64-108">È necessario innanzitutto impostare lo stato Non elaborato.</span><span class="sxs-lookup"><span data-stu-id="26e64-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="26e64-109">La casella di controllo **Elaborato** viene selezionata automaticamente sui record del documento in entrata che sono stati elaborati, ma è anche possibile selezionare o deselezionare la casella di controllo manualmente.</span><span class="sxs-lookup"><span data-stu-id="26e64-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="26e64-110">In base al processo aziendale, un record del documento in entrata può essere elaborato solo quando è stato creato un documento ad esso correlato oppure è stato allegato un file.</span><span class="sxs-lookup"><span data-stu-id="26e64-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="26e64-111">Se si apre la pagina **Documenti in entrata** usando l'azione **Documenti in entrata personali** in Gestione ruolo utente, solo i record del documento in entrata non elaborati vengono visualizzati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26e64-111">When you open the **Incoming Documents** page with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="26e64-112">In questo argomento questa visualizzazione viene indicata come "la visualizzazione predefinita".</span><span class="sxs-lookup"><span data-stu-id="26e64-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="26e64-113">Per rimuovere i record del documento in entrata dalla visualizzazione predefinita</span><span class="sxs-lookup"><span data-stu-id="26e64-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="26e64-114">Nella pagina **Documenti in entrata** selezionare una o più righe dei record del documento in entrata che si desidera rimuovere dalla visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26e64-114">On the **Incoming Documents** page, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="26e64-115">Scegliere l'azione **Imposta su elaborato**.</span><span class="sxs-lookup"><span data-stu-id="26e64-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="26e64-116">I record in entrata del documento vengono eliminate dalla visualizzazione predefinita e viene selezionata la casella di controllo **Elaborato** nelle righe.</span><span class="sxs-lookup"><span data-stu-id="26e64-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="26e64-117">È inoltre possibile eseguire questa azione per il singolo record nella pagina **Scheda Documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="26e64-117">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="26e64-118">Per visualizzare tutti i record dei documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="26e64-118">To view all incoming document records</span></span>
1. <span data-ttu-id="26e64-119">In alternativa, nella pagina **Setup documenti in entrata** scegliere l'azione **Mostra tutto**.</span><span class="sxs-lookup"><span data-stu-id="26e64-119">On the **Incoming Documents** page, choose the **Show All** action.</span></span>

<span data-ttu-id="26e64-120">Tutti i record del documento in entrata vengono visualizzati, inclusi quelli in cui non è selezionata la casella di controllo **Elaborato**.</span><span class="sxs-lookup"><span data-stu-id="26e64-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="26e64-121">Per aggiungere i record del documento in entrata alla visualizzazione predefinita</span><span class="sxs-lookup"><span data-stu-id="26e64-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="26e64-122">In alternativa, nella pagina **Setup documenti in entrata** scegliere l'azione **Mostra tutto**.</span><span class="sxs-lookup"><span data-stu-id="26e64-122">On the **Incoming Documents** page, choose the **Show All** action.</span></span>
2. <span data-ttu-id="26e64-123">Selezionare una o più righe per i record del documento in entrata che si desidera mostrare nella visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26e64-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="26e64-124">Scegliere l'azione **Imposta su non elaborato**.</span><span class="sxs-lookup"><span data-stu-id="26e64-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="26e64-125">È inoltre possibile eseguire questa azione per il singolo record nella pagina **Scheda Documento in entrata**.</span><span class="sxs-lookup"><span data-stu-id="26e64-125">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="26e64-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26e64-126">See Also</span></span>
[<span data-ttu-id="26e64-127">Elaborare i documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="26e64-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="26e64-128">Documenti in entrata</span><span class="sxs-lookup"><span data-stu-id="26e64-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="26e64-129">Acquisti</span><span class="sxs-lookup"><span data-stu-id="26e64-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="26e64-130">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26e64-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
