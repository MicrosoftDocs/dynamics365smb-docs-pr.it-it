---
title: Creare una fattura di vendita per fatturare una commessa| Documenti Microsoft
description: Viene descritto come fatturare ai clienti le spese commessa durante lo svolgimento di un progetto.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4c00ce50f70cbae3ad0557f0703e80f6b115995a
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="invoice-jobs"></a><span data-ttu-id="ffce8-103">Fatturazione di commesse</span><span class="sxs-lookup"><span data-stu-id="ffce8-103">Invoice Jobs</span></span>
<span data-ttu-id="ffce8-104">Durante il progetto, è possibile che si accumulino i costi di commessa derivanti dall'utilizzo delle risorse, dai materiali e dagli acquisti correlati alla commessa.</span><span class="sxs-lookup"><span data-stu-id="ffce8-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="ffce8-105">A seconda dello stato di avanzamento della commessa, tali transazioni vengono inserite nelle registrazioni commesse.</span><span class="sxs-lookup"><span data-stu-id="ffce8-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="ffce8-106">È importante registrare tutti i costi prima di fatturare al cliente.</span><span class="sxs-lookup"><span data-stu-id="ffce8-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="ffce8-107">È possibile fatturare l'intera commessa dalla finestra **Righe task commessa** oppure fatturare solo le righe fatturabili selezionate dalla finestra **Righe pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-107">You can invoice the whole job from the **Job Task Lines** window or only invoice selected billable lines from the **Planning Lines** window.</span></span> <span data-ttu-id="ffce8-108">La fatturazione può essere effettuata dopo la chiusura della commessa oppure durante lo svolgimento delle operazioni correlate alla commessa, a determinati intervalli basati su un'apposita programmazione.</span><span class="sxs-lookup"><span data-stu-id="ffce8-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ffce8-109">Se si seleziona **Fatturabile** nel campo **Tipo riga commessa** dei documenti di acquisto per gli acquisti correlati alla commessa, vengono create le righe di pianificazione commessa che sono pronte per la fatturazione al cliente.</span><span class="sxs-lookup"><span data-stu-id="ffce8-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="ffce8-110">Per ulteriori informazioni, vedere [Gestire gli approvvigionamenti per un progetto](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="ffce8-110">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="ffce8-111">Per creare e registrare una fattura di vendita per una commessa</span><span class="sxs-lookup"><span data-stu-id="ffce8-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="ffce8-112">È possibile creare una fattura per una commessa o per uno o più task commessa per un cliente al completamento del lavoro da fatturare o al raggiungimento della data per la fatturazione in base a una programmazione di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="ffce8-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="ffce8-113">Dalla finestra **Commesse** è possibile fatturare a un cliente selezionando la commessa, quindi scegliendo l'azione **Crea fattura vendita per commessa**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-113">From the **Jobs** window, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="ffce8-114">Nella procedura che segue viene mostrato come utilizzare un processo batch per fatturare più commesse.</span><span class="sxs-lookup"><span data-stu-id="ffce8-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="ffce8-115">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commessa - Crea fattura vendita**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ffce8-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ffce8-116">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="ffce8-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="ffce8-117">Impostare i filtri se si desidera limitare le commesse che devono essere elaborate nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="ffce8-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="ffce8-118">Scegliere il pulsante **OK** per creare le fatture di assistenza.</span><span class="sxs-lookup"><span data-stu-id="ffce8-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="ffce8-119">Per creare più fatture di vendita commesse dalle righe di pianificazione commessa</span><span class="sxs-lookup"><span data-stu-id="ffce8-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="ffce8-120">È possibile creare una fattura da righe di pianificazione commessa e indicare in quella occasione la quantità dell'articolo, la risorsa o il conto di contabilità generale che si desidera fatturare.</span><span class="sxs-lookup"><span data-stu-id="ffce8-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="ffce8-121">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ffce8-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="ffce8-122">Aprire una commessa appropriata.</span><span class="sxs-lookup"><span data-stu-id="ffce8-122">Open a relevant job.</span></span>
3. <span data-ttu-id="ffce8-123">Selezionare un task commessa per il quale il campo **Tipo task commessa** contiene **Registrazione**, quindi scegliere l'azione **Righe pianificazione commessa**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="ffce8-124">In una riga di pianificazione commessa, nel campo **Qtà da trasferire in fattura** , immettere la quantità dell'articolo, la risorsa, il tipo del conto di contabilità generale che si desidera fatturare.</span><span class="sxs-lookup"><span data-stu-id="ffce8-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="ffce8-125">Scegliere l'azione **Crea fattura di vendita**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="ffce8-126">Nella finestra **Commessa - Crea fattura vendita**, immettere la data di registrazione e se si desidera creare una nuova fattura o aggiungere questa fattura a una esistente.</span><span class="sxs-lookup"><span data-stu-id="ffce8-126">In the **Job Create Sales Invoice** window, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="ffce8-127">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="ffce8-128">Nella riga di pianificazione commessa, nel campo **Qtà trasferita in fattura**, è possibile visualizzare la quantità.</span><span class="sxs-lookup"><span data-stu-id="ffce8-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="ffce8-129">Nella finestra **Righe pianificazione commessa** scegliere l'azione **Fatture/Note credito vendite**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-129">In the **Job Planning Lines** window, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="ffce8-130">Verrà visualizzata la finestra **Fatture di vendita** nella quale sarà mostrata la quantità che è stata trasferita in fattura.</span><span class="sxs-lookup"><span data-stu-id="ffce8-130">The **Sales Invoice** window opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="ffce8-131">Apportare tutte le modifiche aggiuntive, quindi scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ffce8-132">La procedura sopra riportata è simile per la creazione, la revisione e la registrazione di una nota di credito di vendita correlata a una commessa.</span><span class="sxs-lookup"><span data-stu-id="ffce8-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="ffce8-133">Per calcolare e registrare i movimenti di completamento della commessa</span><span class="sxs-lookup"><span data-stu-id="ffce8-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="ffce8-134">Al termine di tutte le operazioni di registrazione e fatturazione dell'utilizzo per una commessa, è necessario aggiornare la commessa in modo che il campo **Stato** sia impostato su **Completato**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="ffce8-135">Successivamente, è necessario stornare eventuali WIP registrati nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="ffce8-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="ffce8-136">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ffce8-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ffce8-137">Selezionare una commessa aperta, quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="ffce8-138">Nel campo **Stato** selezionare **Completato**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="ffce8-139">Seguire i passaggi di assistenza per calcolare e registrare il WIP.</span><span class="sxs-lookup"><span data-stu-id="ffce8-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="ffce8-140">In alternativa, seguire i passaggi 5 e 6 per effettuare questa operazione manualmente.</span><span class="sxs-lookup"><span data-stu-id="ffce8-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="ffce8-141">Scegliere l'azione **Calcola WIP**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="ffce8-142">Nella finestra **Commessa - Calcola WIP** compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ffce8-142">In the **Job Calculate WIP** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="ffce8-143">Per i movimenti WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.</span><span class="sxs-lookup"><span data-stu-id="ffce8-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="ffce8-144">Scegliere l'azione **Commessa - Registra WIP in C/G**.</span><span class="sxs-lookup"><span data-stu-id="ffce8-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="ffce8-145">Nella finestra **Commessa - Registra WIP in C/G** compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ffce8-145">In the **Job Post WIP to G/L** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="ffce8-146">Per i movimenti C/G WIP commessa creati tramite l'esecuzione del processo batch sarà ora selezionata la casella di controllo **Commessa completata**, a indicare che si tratta di movimenti di completamento.</span><span class="sxs-lookup"><span data-stu-id="ffce8-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffce8-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffce8-147">See Also</span></span>
[<span data-ttu-id="ffce8-148">Gestione di progetti</span><span class="sxs-lookup"><span data-stu-id="ffce8-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="ffce8-149">Finanze</span><span class="sxs-lookup"><span data-stu-id="ffce8-149">Finance</span></span>](finance.md)  
<span data-ttu-id="ffce8-150">[Acquisti](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="ffce8-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="ffce8-151">[Vendite](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="ffce8-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="ffce8-152">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ffce8-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

