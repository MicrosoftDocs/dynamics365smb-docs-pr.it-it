---
title: Gestire i conti correnti bancari| Documenti Microsoft
description: "È necessario riconciliare regolarmente i movimenti contabili bancari in Financials con le transazioni bancarie correlate nei conti bancari."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dcefa921d7e8b901d906085e6bce01d6e0aa6ac4
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="9acdb-103">Gestione di conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="9acdb-103">Managing Bank Accounts</span></span>
<span data-ttu-id="9acdb-104">A intervalli regolari è necessario riconciliare i movimenti contabili bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] con le transazioni bancarie relative nei conti bancari presso la banca e quindi registrare il saldo nel conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="9acdb-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="9acdb-105">È possibile eseguire questa attività come parte dell'elaborazione dei pagamenti rappresentati in un estratto conto bancario in **Registrazione riconciliazione pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="9acdb-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="9acdb-106">In alternativa, è possibile eseguire questa attività in modo distinto dall'elaborazione del pagamento, nella finestra **Riconciliazioni C/C bancari**, che supporta i movimenti contabili degli assegni.</span><span class="sxs-lookup"><span data-stu-id="9acdb-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="9acdb-107">In entrambi i casi compilare le finestre importando l'estratto conto bancario in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9acdb-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="9acdb-108">Talvolta, è necessario trasferire gli importi tra i conti correnti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] per riflettere i trasferimenti alla banca.</span><span class="sxs-lookup"><span data-stu-id="9acdb-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="9acdb-109">È possibile eseguire questa attività nella finestra **Registrazioni COGE** in modi diversi a seconda della valuta dei fondi.</span><span class="sxs-lookup"><span data-stu-id="9acdb-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="9acdb-110">Prima di poter gestire i conti correnti bancari, è necessario impostare ogni conto bancario come scheda conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="9acdb-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="9acdb-111">Inoltre, è necessario impostare i servizi elettronici che è possibile utilizzare per l'importazione dell'estratto conto bancario e l'esportazione del file di pagamento.</span><span class="sxs-lookup"><span data-stu-id="9acdb-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="9acdb-112">Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="9acdb-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="9acdb-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="9acdb-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="9acdb-114">Per</span><span class="sxs-lookup"><span data-stu-id="9acdb-114">To</span></span> | <span data-ttu-id="9acdb-115">Vedere</span><span class="sxs-lookup"><span data-stu-id="9acdb-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="9acdb-116">Riconciliare i conti correnti bancari in relazione all'elaborazione dei pagamenti nella finestra **Registrazione riconciliazione pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="9acdb-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="9acdb-117">Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="9acdb-117">Apply Payments Automatically and Reconcile Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="9acdb-118">Riconciliare i conti bancari, inclusi i movimenti contabili assegni, come attività separata nella finestra **Riconciliazioni C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="9acdb-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="9acdb-119">Procedura: Riconciliare i conti correnti bancari separatamente</span><span class="sxs-lookup"><span data-stu-id="9acdb-119">How to: Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="9acdb-120">Registrare i bonifici tra conti correnti bancari nella stessa valuta o in valute diverse.</span><span class="sxs-lookup"><span data-stu-id="9acdb-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="9acdb-121">Procedura: Trasferire fondi bancari</span><span class="sxs-lookup"><span data-stu-id="9acdb-121">How to: Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="9acdb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9acdb-122">See Also</span></span>
[<span data-ttu-id="9acdb-123">Impostazione delle attività bancarie</span><span class="sxs-lookup"><span data-stu-id="9acdb-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="9acdb-124">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="9acdb-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="9acdb-125">[Gestione della contabilità fornitori](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="9acdb-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="9acdb-126">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9acdb-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9acdb-127">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="9acdb-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

