---
title: Gestire i conti correnti bancari| Documenti Microsoft
description: "È necessario riconciliare regolarmente i movimenti contabili bancari con le transazioni bancarie correlate nei conti bancari."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: it-it
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="06e0e-103">Gestione di conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="06e0e-103">Managing Bank Accounts</span></span>
<span data-ttu-id="06e0e-104">A intervalli regolari è necessario riconciliare i movimenti contabili bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] con le transazioni bancarie relative nei conti bancari presso la banca e quindi registrare il saldo nel conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="06e0e-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="06e0e-105">È possibile eseguire questa attività come parte dell'elaborazione dei pagamenti rappresentati in un estratto conto bancario in **Registrazione riconciliazione pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="06e0e-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="06e0e-106">In alternativa, è possibile eseguire separatamente il task dall'elaborazione del pagamento nella finestra **Riconciliazioni C/C bancari** in cui associare (riconciliare) le righe del rendiconto bancario nel riquadro a sinistra con i movimenti contabili interni del conto corrente nel riquadro di destra.</span><span class="sxs-lookup"><span data-stu-id="06e0e-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="06e0e-107">In entrambe le finestre è possibile compilare le informazioni sull'estratto conto bancario importando un file o feed ed è possibile utilizzare i suggerimenti automatici di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="06e0e-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="06e0e-108">Nelle versioni per il Nord America è possibile eseguire la riconciliazione bancaria nella finestra **Prospetto riconciliazione bancaria**, più adatta per assegni e depositi ma non offre l'importazione di file di rendiconti bancari.</span><span class="sxs-lookup"><span data-stu-id="06e0e-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="06e0e-109">Per utilizzare questa finestra al posto della finestra **Riconciliazioni C/C bancari**, deselezionare il campo **Riconciliazione bancaria con collegamento automatico** nella finestra **Setup contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="06e0e-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="06e0e-110">Per ulteriori informazioni, vedere “Riconciliazione dei conti correnti bancari" nella funzionalità locale per gli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="06e0e-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="06e0e-111">Talvolta, è necessario trasferire gli importi tra i conti correnti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] per riflettere i trasferimenti alla banca.</span><span class="sxs-lookup"><span data-stu-id="06e0e-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="06e0e-112">È possibile eseguire questa attività nella finestra **Registrazioni COGE** in modi diversi a seconda della valuta dei fondi.</span><span class="sxs-lookup"><span data-stu-id="06e0e-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="06e0e-113">Prima di poter gestire i conti correnti bancari, è necessario impostare ogni conto bancario come scheda conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="06e0e-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="06e0e-114">Inoltre, è necessario impostare i servizi elettronici che è possibile utilizzare per l'importazione dell'estratto conto bancario e l'esportazione del file di pagamento.</span><span class="sxs-lookup"><span data-stu-id="06e0e-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="06e0e-115">Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="06e0e-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="06e0e-116">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="06e0e-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="06e0e-117">Per</span><span class="sxs-lookup"><span data-stu-id="06e0e-117">To</span></span> | <span data-ttu-id="06e0e-118">Vedere</span><span class="sxs-lookup"><span data-stu-id="06e0e-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="06e0e-119">Riconciliare i conti correnti bancari in relazione all'elaborazione dei pagamenti nella finestra **Registrazione riconciliazione pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="06e0e-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="06e0e-120">Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="06e0e-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="06e0e-121">Riconciliare i conti bancari, inclusi i movimenti contabili assegni, come attività separata nella finestra **Riconciliazioni C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="06e0e-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="06e0e-122">Riconciliare i conti correnti bancari separatamente</span><span class="sxs-lookup"><span data-stu-id="06e0e-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="06e0e-123">Registrare i bonifici tra conti correnti bancari nella stessa valuta o in valute diverse.</span><span class="sxs-lookup"><span data-stu-id="06e0e-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="06e0e-124">Trasferimento di fondi bancari</span><span class="sxs-lookup"><span data-stu-id="06e0e-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="06e0e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06e0e-125">See Also</span></span>
[<span data-ttu-id="06e0e-126">Impostazione delle attività bancarie</span><span class="sxs-lookup"><span data-stu-id="06e0e-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="06e0e-127">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="06e0e-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="06e0e-128">[Gestione della contabilità fornitori](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="06e0e-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="06e0e-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="06e0e-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="06e0e-130">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="06e0e-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

