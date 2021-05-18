---
title: Creare una fattura di vendita per fatturare una commessa| Documenti Microsoft
description: Viene descritto come fatturare ai clienti le spese commessa durante lo svolgimento di un progetto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 873135d2fa6053b7101a999981fb3117ee8689ab
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938148"
---
# <a name="invoice-jobs"></a><span data-ttu-id="40b9c-103">Fatturazione di commesse</span><span class="sxs-lookup"><span data-stu-id="40b9c-103">Invoice Jobs</span></span>
<span data-ttu-id="40b9c-104">Durante il progetto, è possibile che si accumulino i costi di commessa derivanti dall'utilizzo delle risorse, dai materiali e dagli acquisti correlati alla commessa.</span><span class="sxs-lookup"><span data-stu-id="40b9c-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="40b9c-105">A seconda dello stato di avanzamento della commessa, tali transazioni vengono inserite nelle registrazioni commesse.</span><span class="sxs-lookup"><span data-stu-id="40b9c-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="40b9c-106">È importante registrare tutti i costi prima di fatturare al cliente.</span><span class="sxs-lookup"><span data-stu-id="40b9c-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="40b9c-107">Puoi inoltre acquistare risorse esterne non correlate a un processo, ad esempio, per fatturare a un fornitore per il lavoro eseguito.</span><span class="sxs-lookup"><span data-stu-id="40b9c-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="40b9c-108">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="40b9c-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="40b9c-109">È possibile fatturare l'intera commessa dalla pagina **Righe task commessa** oppure fatturare solo le righe fatturabili selezionate dalla pagina **Righe pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="40b9c-110">La fatturazione può essere effettuata dopo la chiusura della commessa oppure durante lo svolgimento delle operazioni correlate alla commessa, a determinati intervalli basati su un'apposita programmazione.</span><span class="sxs-lookup"><span data-stu-id="40b9c-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="40b9c-111">Se si seleziona **Fatturabile** nel campo **Tipo riga commessa** dei documenti di acquisto per gli acquisti correlati alla commessa, vengono create le righe di pianificazione commessa che sono pronte per la fatturazione al cliente.</span><span class="sxs-lookup"><span data-stu-id="40b9c-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="40b9c-112">Per ulteriori informazioni, vedere [Gestire gli approvvigionamenti per un progetto](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="40b9c-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="40b9c-113">Per creare più fatture di vendita commesse</span><span class="sxs-lookup"><span data-stu-id="40b9c-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="40b9c-114">È possibile creare una fattura per una commessa o per uno o più task commessa per un cliente al completamento del lavoro da fatturare o al raggiungimento della data per la fatturazione in base a una programmazione di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="40b9c-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="40b9c-115">Nella procedura che segue viene mostrato come utilizzare un processo batch per fatturare più commesse.</span><span class="sxs-lookup"><span data-stu-id="40b9c-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="40b9c-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Commessa - Crea fattura vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="40b9c-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="40b9c-117">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="40b9c-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="40b9c-118">Impostare i filtri se si desidera limitare le commesse che devono essere elaborate nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="40b9c-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="40b9c-119">Scegliere il pulsante **OK** per creare le fatture di assistenza.</span><span class="sxs-lookup"><span data-stu-id="40b9c-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="40b9c-120">È possibile rivedere e pubblicare le fatture create nella finestra **Fatture vendita**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="40b9c-121">In alternativa, fatturare a un cliente selezionando la commessa, quindi scegliendo l'azione **Crea fattura vendita per commessa**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="40b9c-122">Per creare e registrare una fattura di vendita commessa dalle righe di pianificazione commessa</span><span class="sxs-lookup"><span data-stu-id="40b9c-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="40b9c-123">È possibile creare una fattura da righe di pianificazione commessa e indicare in quella occasione la quantità dell'articolo, la risorsa o il conto di contabilità generale che si desidera fatturare.</span><span class="sxs-lookup"><span data-stu-id="40b9c-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="40b9c-124">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Commesse** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="40b9c-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="40b9c-125">Aprire una commessa appropriata.</span><span class="sxs-lookup"><span data-stu-id="40b9c-125">Open a relevant job.</span></span>
3. <span data-ttu-id="40b9c-126">Selezionare un task commessa per il quale il campo **Tipo task commessa** contiene **Registrazione**, quindi scegliere l'azione **Righe pianificazione commessa**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="40b9c-127">In una riga di pianificazione commessa, nel campo **Qtà da trasferire in fattura** , immettere la quantità dell'articolo, la risorsa, il tipo del conto di contabilità generale che si desidera fatturare.</span><span class="sxs-lookup"><span data-stu-id="40b9c-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="40b9c-128">Scegliere l'azione **Crea fattura di vendita**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="40b9c-129">Nella pagina **Commessa - Crea fattura vendita**, immettere la data di registrazione e se si desidera creare una nuova fattura o aggiungere questa fattura a una esistente.</span><span class="sxs-lookup"><span data-stu-id="40b9c-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="40b9c-130">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="40b9c-131">Nella pagina **Righe pianificazione commessa** scegliere l'azione **Fatture/Note credito vendite**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="40b9c-132">Verrà visualizzata la pagina **Fatture di vendita** nella quale sarà mostrata la quantità che è stata trasferita in fattura.</span><span class="sxs-lookup"><span data-stu-id="40b9c-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="40b9c-133">Apportare tutte le modifiche aggiuntive, quindi scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="40b9c-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="40b9c-134">La procedura sopra riportata è simile per la creazione, la revisione e la registrazione di una nota di credito di vendita correlata a una commessa.</span><span class="sxs-lookup"><span data-stu-id="40b9c-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>


## <a name="see-also"></a><span data-ttu-id="40b9c-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="40b9c-135">See Also</span></span>
[<span data-ttu-id="40b9c-136">Gestione di progetti</span><span class="sxs-lookup"><span data-stu-id="40b9c-136">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="40b9c-137">Finanze</span><span class="sxs-lookup"><span data-stu-id="40b9c-137">Finance</span></span>](finance.md)  
<span data-ttu-id="40b9c-138">[Acquisti](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="40b9c-138">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="40b9c-139">[Vendite](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="40b9c-139">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="40b9c-140">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="40b9c-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
