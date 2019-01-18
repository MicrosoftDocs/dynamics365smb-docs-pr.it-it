---
title: Come rettificare i pagamenti anticipati | Microsoft Docs
description: "È possibile apportare una correzione a un ordine dopo aver registrato una fattura pagamento anticipato per l'ordine stesso. È possibile aggiungere nuove righe a un ordine dopo avere emesso un pagamento anticipato, quindi registrare un'altra fattura pagamento anticipato, ma non è possibile eliminare una riga da un ordine dopo che per tale riga è stato registrato un pagamento anticipato."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: b19b86b3d5168ee6fa053141af4022f5040743cb
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="correct-prepayments"></a><span data-ttu-id="7fdce-104">Rettificare i pagamenti anticipati</span><span class="sxs-lookup"><span data-stu-id="7fdce-104">Correct Prepayments</span></span>
<span data-ttu-id="7fdce-105">È possibile apportare una correzione a un ordine dopo aver registrato una fattura pagamento anticipato per l'ordine stesso.</span><span class="sxs-lookup"><span data-stu-id="7fdce-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="7fdce-106">È possibile aggiungere nuove righe a un ordine dopo avere emesso un pagamento anticipato, quindi registrare un'altra fattura pagamento anticipato, ma non è possibile eliminare una riga da un ordine dopo che per tale riga è stato registrato un pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="7fdce-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="7fdce-107">Per rettificare un pagamento anticipato</span><span class="sxs-lookup"><span data-stu-id="7fdce-107">To correct a prepayment</span></span>
<span data-ttu-id="7fdce-108">La procedura seguente illustra come emettere una nota di credito di pagamento anticipato per annullare tutti i pagamenti anticipati fatturati per un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="7fdce-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="7fdce-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="7fdce-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7fdce-110">Aprire l'ordine di vendita appropriato.</span><span class="sxs-lookup"><span data-stu-id="7fdce-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="7fdce-111">Scegliere l'azione **Pagamento anticipato**, quindi scegliere l'azione **Registra nota credito pagamento anticipato** o l'azione **Registra e stampa nota cr. pagam. ant.**</span><span class="sxs-lookup"><span data-stu-id="7fdce-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="7fdce-112">Nella pagina **Nota credito vendita** rettificare i movimenti desiderati, come per qualsiasi nota di credito vendita.</span><span class="sxs-lookup"><span data-stu-id="7fdce-112">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="7fdce-113">Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="7fdce-113">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="7fdce-114">Per ridurre l'importo nel campo **Importo riga**, è necessario prima aumentare la percentuale pagamento anticipato nella riga in modo che il valore nel campo **Importo riga pagam. ant.** non scenda sotto il valore del campo **Fattura importo pagam. ant.**.</span><span class="sxs-lookup"><span data-stu-id="7fdce-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="7fdce-115">Per creare una fattura pagamento anticipato per le nuove righe nota di credito di vendita,, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Registra fattura pagamento anticipato** o l'azione **Registra e stampa fattura pagam. ant.**.</span><span class="sxs-lookup"><span data-stu-id="7fdce-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="7fdce-116">Per emettere una fattura pagamento anticipato aggiuntiva, aumentare l'importo pagamento anticipato in una o più righe e registrare la fattura pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="7fdce-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="7fdce-117">Verrà creata una nuova fattura per la differenza tra gli importi di pagamenti anticipati fatturati e i nuovi importi di pagamenti anticipati.</span><span class="sxs-lookup"><span data-stu-id="7fdce-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7fdce-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fdce-118">See Also</span></span>  
[<span data-ttu-id="7fdce-119">Fatturazione dei pagamenti anticipati</span><span class="sxs-lookup"><span data-stu-id="7fdce-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="7fdce-120">Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite</span><span class="sxs-lookup"><span data-stu-id="7fdce-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="7fdce-121">Finanze</span><span class="sxs-lookup"><span data-stu-id="7fdce-121">Finance</span></span>](finance.md)  
<span data-ttu-id="7fdce-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7fdce-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

