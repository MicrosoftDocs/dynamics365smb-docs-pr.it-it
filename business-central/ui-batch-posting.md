---
title: Come registrare più documenti contemporaneamente | Microsoft Docs
description: Anziché registrare un singolo documento alla volta, è possibile selezionare più documenti non registrati in un elenco per la registrazione batch, per una registrazione immediata o programmata, ad esempio, per la fine della giornata.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912723"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="b2d02-103">Registrare più documenti contemporaneamente</span><span class="sxs-lookup"><span data-stu-id="b2d02-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="b2d02-104">Anziché registrare un singolo documento alla volta, è possibile selezionare più documenti non registrati in un elenco per una registrazione immediata o una registrazione batch programmata, ad esempio, per la fine della giornata.</span><span class="sxs-lookup"><span data-stu-id="b2d02-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="b2d02-105">Ciò può essere utile se solo un supervisore può registrare documenti creati da altri utenti o per evitare problemi di prestazioni del sistema dovuti alla registrazione durante l'orario di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b2d02-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="b2d02-106">Per registrare immediatamente più ordini di acquisto</span><span class="sxs-lookup"><span data-stu-id="b2d02-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="b2d02-107">La seguente procedura descrive come registrare immediatamente più ordini di acquisto.</span><span class="sxs-lookup"><span data-stu-id="b2d02-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="b2d02-108">I passaggi sono simili per tutti i documenti di acquisto e vendita.</span><span class="sxs-lookup"><span data-stu-id="b2d02-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="b2d02-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b2d02-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b2d02-110">Nella pagina **Ordini acquisto**, selezionare tutti gli ordini da registrare:</span><span class="sxs-lookup"><span data-stu-id="b2d02-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="b2d02-111">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b2d02-111">In the **No.**</span></span> <span data-ttu-id="b2d02-112">selezionare i tre punti verticali per aprire il menu di scelta rapida, quindi scegliere il l'azione **Seleziona più elementi**.</span><span class="sxs-lookup"><span data-stu-id="b2d02-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="b2d02-113">Selezionare la casella di controllo per tutte le righe che rappresentano gli ordini che si desidera registrare contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="b2d02-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="b2d02-114">Scegliere l'azione **Registrazione** e quindi l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="b2d02-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="b2d02-115">Scegliere il pulsante **Sì** nel messaggio di conferma.</span><span class="sxs-lookup"><span data-stu-id="b2d02-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="b2d02-116">Per eseguire registrazioni batch di ordini di acquisto</span><span class="sxs-lookup"><span data-stu-id="b2d02-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="b2d02-117">La seguente procedura descrive come eseguire registrazioni batch di ordini di acquisto.</span><span class="sxs-lookup"><span data-stu-id="b2d02-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="b2d02-118">I passaggi sono simili per tutti i documenti di acquisto e vendita in cui l'azione **Registra batch** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="b2d02-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="b2d02-119">La registrazione in batch dei documenti avviene in background.</span><span class="sxs-lookup"><span data-stu-id="b2d02-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="b2d02-120">[!INCLUDE [prodshort](includes/prodshort.md)] online include processi predefiniti per la registrazione in background e la registrazione in batch.</span><span class="sxs-lookup"><span data-stu-id="b2d02-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="b2d02-121">Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="b2d02-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="b2d02-122">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b2d02-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b2d02-123">Nella pagina **Ordini acquisto**, selezionare tutti gli ordini da registrare:</span><span class="sxs-lookup"><span data-stu-id="b2d02-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="b2d02-124">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b2d02-124">In the **No.**</span></span> <span data-ttu-id="b2d02-125">selezionare i tre punti verticali per aprire il menu di scelta rapida, quindi scegliere il l'azione **Seleziona più elementi**.</span><span class="sxs-lookup"><span data-stu-id="b2d02-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="b2d02-126">Selezionare la casella di controllo per tutte le righe che rappresentano gli ordini che si desidera registrare contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="b2d02-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="b2d02-127">Scegliere l'azione **Registrazione** e quindi l'azione **Registra batch**.</span><span class="sxs-lookup"><span data-stu-id="b2d02-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="b2d02-128">Nella pagina **Aggior. batch ordini acquisto**, riempire i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="b2d02-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="b2d02-129">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2d02-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="b2d02-130">Per visualizzare potenziali problemi verificatisi durante la registrazione batch di documenti, aprire la pagina **Registro messaggi di errore**.</span><span class="sxs-lookup"><span data-stu-id="b2d02-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="b2d02-131">Gli ordini di acquisto verranno ora aggiunti a un movimento coda processi dedicato, che definisce quando i documenti vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="b2d02-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="b2d02-132">Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="b2d02-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="b2d02-133">Se si seleziona **PDF** nel campo **Tipo di output report**, gli ordini di acquisto registrati correttamente saranno disponibili nella parte **Report elaborati** in Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="b2d02-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2d02-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b2d02-134">See Also</span></span>

[<span data-ttu-id="b2d02-135">Contabilizzazione dei documenti e delle registrazioni</span><span class="sxs-lookup"><span data-stu-id="b2d02-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="b2d02-136">Utilizzare le code processi per pianificare le attività</span><span class="sxs-lookup"><span data-stu-id="b2d02-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="b2d02-137">Modificare i documenti registrati</span><span class="sxs-lookup"><span data-stu-id="b2d02-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="b2d02-138">Correggere o annullare le fatture di acquisto non pagate</span><span class="sxs-lookup"><span data-stu-id="b2d02-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="b2d02-139">Individuare pagine e informazioni con la funzionalità delle informazioni</span><span class="sxs-lookup"><span data-stu-id="b2d02-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="b2d02-140">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b2d02-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
