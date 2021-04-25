---
title: Registrare le entrate o le spese direttamente nella contabilità generale| Documenti Microsoft
description: Per le attività aziendali che non vengono rappresentate da un documento, ad esempio le spese più piccole o le ricevute di pagamento, è possibile creare le transazioni correlate registrando le righe nella pagina Registrazioni COGE.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e0beff15352fb8e57f57c9d0ffdcd76bc28afbb9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782381"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="737aa-103">Registrare le transazioni direttamente nella contabilità generale</span><span class="sxs-lookup"><span data-stu-id="737aa-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="737aa-104">Le registrazioni generali vengono utilizzate per la contabilizzazione diretta nei conti C/G e in altri conti delle transazioni finanziarie, ad esempio i conti correnti bancari, i conti clienti, fornitori e dipendenti.</span><span class="sxs-lookup"><span data-stu-id="737aa-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="737aa-105">Un tipico utilizzo delle registrazioni COGE consiste nel registrare le spese dei dipendenti effettuate con denaro personale durante le attività lavorative, al fine di provvedere successivamente al rimborso.</span><span class="sxs-lookup"><span data-stu-id="737aa-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="737aa-106">Per altre informazioni, vedere [Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="737aa-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="737aa-107">Le registrazioni COGE includono le transazioni finanziarie direttamente nei conti di contabilità generale e in altri conti, ad esempio i conti correnti bancari, i conti clienti e i conti fornitori.</span><span class="sxs-lookup"><span data-stu-id="737aa-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="737aa-108">La contabilizzazione mediante una registrazione generale crea sempre movimenti nei conti di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="737aa-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="737aa-109">Ciò è vero anche quando, ad esempio, viene contabilizzata una riga di registrazione in un conto cliente, in quanto tramite una categoria di registrazione viene registrata una riga in un conto crediti nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="737aa-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="737aa-110">È possibile personalizzare la versione delle registrazioni generali impostando un batch o una definizione di registrazioni.</span><span class="sxs-lookup"><span data-stu-id="737aa-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="737aa-111">Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="737aa-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="737aa-112">Diversamente dai movimenti che vengono registrati con i documenti che richiedono un processo di nota di credito, è possibile stornare correttamente i movimenti che vengono registrati con le registrazioni COGE.</span><span class="sxs-lookup"><span data-stu-id="737aa-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="737aa-113">Per ulteriori informazioni, vedere [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="737aa-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="737aa-114">Per registrare una transazione direttamente in un conto di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="737aa-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="737aa-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="737aa-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="737aa-116">Aprire il batch registrazioni COGE appropriato.</span><span class="sxs-lookup"><span data-stu-id="737aa-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="737aa-117">Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="737aa-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="737aa-118">In una nuova riga di registrazione, compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="737aa-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="737aa-119">Ripetere il passaggio 3 tutte le transazioni separate da registrare.</span><span class="sxs-lookup"><span data-stu-id="737aa-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="737aa-120">Se si immettono più righe di transazione sopra a una riga di contropartita, ad esempio, per un conto corrente bancario, seleziona la casella di controllo **Suggerisci importo contropartita** nella riga per il batch nella pagina **Batch registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="737aa-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="737aa-121">Il campo **Importo** nella riga di contropartita viene precompilato automaticamente con il valore necessario per pareggiare le transazioni.</span><span class="sxs-lookup"><span data-stu-id="737aa-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="737aa-122">Scegliere l'azione **Registra** per registrare le transazioni nei conti C/G specificati.</span><span class="sxs-lookup"><span data-stu-id="737aa-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="737aa-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="737aa-123">See Also</span></span>

[<span data-ttu-id="737aa-124">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="737aa-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="737aa-125">Registrare e rimborsare le spese dei dipendenti</span><span class="sxs-lookup"><span data-stu-id="737aa-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="737aa-126">Stornare le registrazioni e annullare carichi/spedizioni errati.</span><span class="sxs-lookup"><span data-stu-id="737aa-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="737aa-127">Finanze</span><span class="sxs-lookup"><span data-stu-id="737aa-127">Finance</span></span>](finance.md)  
<span data-ttu-id="737aa-128">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="737aa-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]