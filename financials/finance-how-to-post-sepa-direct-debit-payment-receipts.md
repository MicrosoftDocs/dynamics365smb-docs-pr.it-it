---
title: Registrare i pagamenti di addebiti diretti SEPA | Microsoft Docs
description: "Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5beb5f6795bd7f4943a6ed9d8b691c05fc5ecb63
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="597c6-103">Procedura: Registrare ricevute di pagamento di addebiti diretti SEPA</span><span class="sxs-lookup"><span data-stu-id="597c6-103">How to: Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="597c6-104">Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate.</span><span class="sxs-lookup"><span data-stu-id="597c6-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="597c6-105">Per ulteriori informazioni, vedere [Procedura: Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="597c6-105">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="597c6-106">È possibile registrare la ricevuta di pagamento direttamente dalla finestra **Riscossioni addebiti diretti** o dalla finestra **Movimenti riscossioni addebiti diretti**.</span><span class="sxs-lookup"><span data-stu-id="597c6-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="597c6-107">In alternativa, è possibile inoltrare il lavoro a un altro utente preparando le righe registrazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="597c6-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="597c6-108">Per registrare una ricevuta di pagamento con addebito diretto dalla finestra Riscossioni di addebiti diretti</span><span class="sxs-lookup"><span data-stu-id="597c6-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="597c6-109">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Riscossioni addebiti diretti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="597c6-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="597c6-110">Selezionare una riga per una riscossione di addebiti diretti esportata in un file della banca ed elaborata correttamente dalla banca.</span><span class="sxs-lookup"><span data-stu-id="597c6-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="597c6-111">Per ulteriori informazioni, vedere [Procedura: Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="597c6-111">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="597c6-112">Scegliere l'azione **Registra ricevute di pagamento**.</span><span class="sxs-lookup"><span data-stu-id="597c6-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="597c6-113">Nella finestra **Registra riscossione addebiti diretti** compilare i campi come indicato nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="597c6-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="597c6-114">Campo</span><span class="sxs-lookup"><span data-stu-id="597c6-114">Field</span></span>|<span data-ttu-id="597c6-115">Description</span><span class="sxs-lookup"><span data-stu-id="597c6-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="597c6-116">**Nr. riscossione di addebiti diretti**</span><span class="sxs-lookup"><span data-stu-id="597c6-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="597c6-117">Specificare la riscossione di addebiti diretti per cui si desidera registrare la ricevuta di pagamento.</span><span class="sxs-lookup"><span data-stu-id="597c6-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="597c6-118">**Definizione registrazioni COGE**</span><span class="sxs-lookup"><span data-stu-id="597c6-118">**General Journal Template**</span></span>|<span data-ttu-id="597c6-119">Specificare quale definizione di registrazione COGE utilizzare per registrare la ricevuta di pagamento, ad esempio le ricevute delle entrate di cassa.</span><span class="sxs-lookup"><span data-stu-id="597c6-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="597c6-120">**Nome batch registrazioni COGE**</span><span class="sxs-lookup"><span data-stu-id="597c6-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="597c6-121">Specificare quale il batch di registrazioni COGE utilizzare per la registrazione della ricevuta di pagamento.</span><span class="sxs-lookup"><span data-stu-id="597c6-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="597c6-122">**Crea solo registrazioni**</span><span class="sxs-lookup"><span data-stu-id="597c6-122">**Create Journal Only**</span></span>|<span data-ttu-id="597c6-123">Selezionare questa casella di controllo se non si desidera registrare la ricevuta di pagamento quando si sceglie il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="597c6-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="597c6-124">La ricevuta di pagamento verrà preparata nella registrazione specificata e non verrà registrata finché non vengono contabilizzate le righe registrazioni in questione.</span><span class="sxs-lookup"><span data-stu-id="597c6-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="597c6-125">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="597c6-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="597c6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="597c6-126">See Also</span></span>  
 <span data-ttu-id="597c6-127">[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="597c6-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="597c6-128">Vendite</span><span class="sxs-lookup"><span data-stu-id="597c6-128">Sales</span></span>](sales-manage-sales.md)

