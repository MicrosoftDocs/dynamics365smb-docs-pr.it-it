---
title: Registrare e rimborsare le spese di lavoro dei dipendenti
description: Registrare le spese di un dipendente con le registrazioni COGE nel conto del dipendente e successivamente registrare un pagamento verso il conto bancario del dipendente per rimborsarlo delle spese sostenute per il lavoro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184401"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="af4df-103">Registrare e rimborsare le spese dei dipendenti</span><span class="sxs-lookup"><span data-stu-id="af4df-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="af4df-104">supporta le transazioni per i dipendenti in modo simile alle transazioni per i fornitori.</span><span class="sxs-lookup"><span data-stu-id="af4df-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="af4df-105">Di conseguenza, sono disponibili alcune categorie di registrazione dipendenti che consentono di assicurarsi che i movimenti contabili per i dipendenti siano registrati nei conti di pertinenza nella contabilità COGE.</span><span class="sxs-lookup"><span data-stu-id="af4df-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="af4df-106">Le transazioni relative ai dipendenti possono essere registrate solo nella valuta locale.</span><span class="sxs-lookup"><span data-stu-id="af4df-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="af4df-107">I rimborsi ai dipendenti non supportano sconti e e tolleranze sui pagamenti.</span><span class="sxs-lookup"><span data-stu-id="af4df-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="af4df-108">Se i dipendenti spendono denaro personale durante le attività lavorative, è possibile registrare le spese nei conti dei dipendenti.</span><span class="sxs-lookup"><span data-stu-id="af4df-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="af4df-109">È quindi possibile rimborsare il dipendente effettuando un pagamento sul conto bancario del dipendente, analogamente a quando si pagano i fornitori.</span><span class="sxs-lookup"><span data-stu-id="af4df-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="af4df-110">Questo articolo spiega come registrare le spese nei libri e come rimborsare il dipendente.</span><span class="sxs-lookup"><span data-stu-id="af4df-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="af4df-111">L'organizzazione potrebbe avere un portale o un'app in cui i dipendenti possono inviare le proprie note spese.</span><span class="sxs-lookup"><span data-stu-id="af4df-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="af4df-112">[!INCLUDE [prod_short](includes/prod_short.md)] è sufficientemente flessibile per adattarsi a molte pratiche diverse.</span><span class="sxs-lookup"><span data-stu-id="af4df-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="af4df-113">I numeri di account esatti da utilizzare dipendono dalla configurazione e dai processi dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="af4df-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="af4df-114">Per registrare le spese di un dipendente</span><span class="sxs-lookup"><span data-stu-id="af4df-114">To record an employee's expense</span></span>

<span data-ttu-id="af4df-115">Le spese del dipendente vengono registrate nella pagina **Contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="af4df-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="af4df-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="af4df-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="af4df-117">Aprire il batch registrazioni COGE appropriato.</span><span class="sxs-lookup"><span data-stu-id="af4df-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="af4df-118">Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="af4df-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="af4df-119">In una nuova riga di registrazione, compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="af4df-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="af4df-120">Ripetere il passaggio 3 per le spese che il dipendente ha pagato.</span><span class="sxs-lookup"><span data-stu-id="af4df-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="af4df-121">Se si desidera immettere più righe di spesa sopra una riga di contropartita per il conto bancario del dipendente, selezionare la casella di controllo **Suggerisci importo contropartita** nella riga del batch nella pagina **Batch registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="af4df-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="af4df-122">Il campo **Importo** nella riga di contropartita viene precompilato automaticamente con il valore necessario per pareggiare le spese.</span><span class="sxs-lookup"><span data-stu-id="af4df-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="af4df-123">Scegliere l'azione **Registra** per registrare spese nel conto del dipendente.</span><span class="sxs-lookup"><span data-stu-id="af4df-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="af4df-124">Per rimborsare un dipendente</span><span class="sxs-lookup"><span data-stu-id="af4df-124">To reimburse an employee</span></span>

<span data-ttu-id="af4df-125">I dipendenti vengono rimborsati registrando i pagamenti nei relativi conti bancari nella pagina **Registrazioni pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="af4df-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="af4df-126">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="af4df-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="af4df-127">Aprire il batch registrazioni pagamenti appropriato.</span><span class="sxs-lookup"><span data-stu-id="af4df-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="af4df-128">Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="af4df-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="af4df-129">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="af4df-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="af4df-130">Per ulteriori informazioni, vedere [Effettuare i pagamenti](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="af4df-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="af4df-131">In alternativa, scegliere l'azione **Suggerisci pagamenti dipendente** per inserire automaticamente righe di registrazione per rimborsi in sospeso al dipendente.</span><span class="sxs-lookup"><span data-stu-id="af4df-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="af4df-132">Scegliere l'azione **Registra** per registrare il rimborso.</span><span class="sxs-lookup"><span data-stu-id="af4df-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="af4df-133">Per riconciliare i rimborsi con movimenti contabili del dipendente</span><span class="sxs-lookup"><span data-stu-id="af4df-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="af4df-134">I pagamenti dei dipendenti si applicano ai movimenti contabili aperti correlati come si fa per i pagamenti dei fornitori, ad esempio nella pagina **Registrazione riconciliazione pagamenti**, in base ai movimenti relativi dell'estratto conto.</span><span class="sxs-lookup"><span data-stu-id="af4df-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="af4df-135">Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="af4df-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="af4df-136">In alternativa, è possibile applicarli manualmente nella pagina **Movimenti contabili dipendente**.</span><span class="sxs-lookup"><span data-stu-id="af4df-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="af4df-137">Per ulteriori informazioni, vedere [Riconciliare manualmente i pagamenti ai fornitori con la registrazioni pagamenti o dai movimenti contabili fornitori](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="af4df-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="af4df-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af4df-138">See Also</span></span>

[<span data-ttu-id="af4df-139">Registrare le transazioni direttamente nella contabilità generale</span><span class="sxs-lookup"><span data-stu-id="af4df-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="af4df-140">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="af4df-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="af4df-141">Stornare le registrazioni e annullare carichi/spedizioni errati.</span><span class="sxs-lookup"><span data-stu-id="af4df-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="af4df-142">Finanze</span><span class="sxs-lookup"><span data-stu-id="af4df-142">Finance</span></span>](finance.md)  
<span data-ttu-id="af4df-143">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af4df-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]