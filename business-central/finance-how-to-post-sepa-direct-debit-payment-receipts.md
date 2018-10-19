---
title: Registrare i pagamenti di addebiti diretti SEPA | Microsoft Docs
description: "Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ee07ca7ba498858fac794f1ee1f27f281de8ae02
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="b87da-103">Registrare ricevute di pagamento di addebiti diretti SEPA</span><span class="sxs-lookup"><span data-stu-id="b87da-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="b87da-104">Quando una riscossione di addebiti diretti viene elaborata correttamente dalla banca, è possibile procedere con la registrazione della ricevuta del pagamento per le fatture di vendita interessate.</span><span class="sxs-lookup"><span data-stu-id="b87da-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="b87da-105">Per ulteriori informazioni, vedere [Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="b87da-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="b87da-106">È possibile registrare la ricevuta di pagamento direttamente dalla finestra **Riscossioni addebiti diretti** o dalla finestra **Movimenti riscossioni addebiti diretti**.</span><span class="sxs-lookup"><span data-stu-id="b87da-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="b87da-107">In alternativa, è possibile inoltrare il lavoro a un altro utente preparando le righe registrazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="b87da-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="b87da-108">Per registrare una ricevuta di pagamento con addebito diretto dalla finestra Riscossioni di addebiti diretti</span><span class="sxs-lookup"><span data-stu-id="b87da-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="b87da-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Riscossioni addebiti diretti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b87da-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b87da-110">Selezionare una riga per una riscossione di addebiti diretti esportata in un file della banca ed elaborata correttamente dalla banca.</span><span class="sxs-lookup"><span data-stu-id="b87da-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="b87da-111">Per ulteriori informazioni, vedere [Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="b87da-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="b87da-112">Scegliere l'azione **Registra ricevute di pagamento**.</span><span class="sxs-lookup"><span data-stu-id="b87da-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="b87da-113">Nella finestra **Registra riscossione addebiti diretti** compilare i campi come indicato nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="b87da-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="b87da-114">Campo</span><span class="sxs-lookup"><span data-stu-id="b87da-114">Field</span></span>|<span data-ttu-id="b87da-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b87da-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b87da-116">**Nr. riscossione di addebiti diretti**</span><span class="sxs-lookup"><span data-stu-id="b87da-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="b87da-117">Specificare la riscossione di addebiti diretti per cui si desidera registrare la ricevuta di pagamento.</span><span class="sxs-lookup"><span data-stu-id="b87da-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="b87da-118">**Definizione registrazioni COGE**</span><span class="sxs-lookup"><span data-stu-id="b87da-118">**General Journal Template**</span></span>|<span data-ttu-id="b87da-119">Specificare quale definizione di registrazione COGE utilizzare per registrare la ricevuta di pagamento, ad esempio le ricevute delle entrate di cassa.</span><span class="sxs-lookup"><span data-stu-id="b87da-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="b87da-120">**Nome batch registrazioni COGE**</span><span class="sxs-lookup"><span data-stu-id="b87da-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="b87da-121">Specificare quale il batch di registrazioni COGE utilizzare per la registrazione della ricevuta di pagamento.</span><span class="sxs-lookup"><span data-stu-id="b87da-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="b87da-122">**Crea solo registrazioni**</span><span class="sxs-lookup"><span data-stu-id="b87da-122">**Create Journal Only**</span></span>|<span data-ttu-id="b87da-123">Selezionare questa casella di controllo se non si desidera registrare la ricevuta di pagamento quando si sceglie il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="b87da-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="b87da-124">La ricevuta di pagamento verrà preparata nella registrazione specificata e non verrà registrata finché non vengono contabilizzate le righe registrazioni in questione.</span><span class="sxs-lookup"><span data-stu-id="b87da-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="b87da-125">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="b87da-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b87da-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b87da-126">See Also</span></span>  
 <span data-ttu-id="b87da-127">[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="b87da-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="b87da-128">Vendite</span><span class="sxs-lookup"><span data-stu-id="b87da-128">Sales</span></span>](sales-manage-sales.md)

