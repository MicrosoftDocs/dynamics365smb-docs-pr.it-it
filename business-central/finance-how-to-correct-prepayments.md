---
title: Come rettificare i pagamenti anticipati | Microsoft Docs
description: È possibile apportare una correzione a un ordine dopo aver registrato una fattura pagamento anticipato per l'ordine stesso. È possibile aggiungere nuove righe a un ordine dopo avere emesso un pagamento anticipato, quindi registrare un'altra fattura pagamento anticipato, ma non è possibile eliminare una riga da un ordine dopo che per tale riga è stato registrato un pagamento anticipato.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ed9bed71ca73e25197869f1f670251ae523648c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783536"
---
# <a name="correct-prepayments"></a><span data-ttu-id="e2310-104">Rettificare i pagamenti anticipati</span><span class="sxs-lookup"><span data-stu-id="e2310-104">Correct Prepayments</span></span>

<span data-ttu-id="e2310-105">È possibile apportare una correzione a un ordine dopo aver registrato una fattura pagamento anticipato per l'ordine stesso.</span><span class="sxs-lookup"><span data-stu-id="e2310-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="e2310-106">È possibile aggiungere nuove righe a un ordine dopo avere emesso un pagamento anticipato, quindi registrare un'altra fattura pagamento anticipato, ma non è possibile eliminare una riga da un ordine dopo che per tale riga è stato registrato un pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="e2310-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

> [!TIP]
> <span data-ttu-id="e2310-107">Se è stata registrata una fattura di pagamento anticipato per una fattura di vendita che si corregge o si annulla, è necessario correggere o annullare anche il pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="e2310-107">If you have posted a prepayment invoice for a sales invoice that you then correct or cancel, you must correct or cancel the prepayment as well.</span></span>

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="e2310-108">Per rettificare un pagamento anticipato</span><span class="sxs-lookup"><span data-stu-id="e2310-108">To correct a prepayment</span></span>

<span data-ttu-id="e2310-109">La procedura seguente illustra come emettere una nota di credito di pagamento anticipato per annullare tutti i pagamenti anticipati fatturati per un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="e2310-109">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  

1. <span data-ttu-id="e2310-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e2310-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e2310-111">Aprire l'ordine di vendita appropriato.</span><span class="sxs-lookup"><span data-stu-id="e2310-111">Open the relevant sales order.</span></span>
3. <span data-ttu-id="e2310-112">Scegliere l'azione **Pagamento anticipato**, quindi scegliere l'azione **Registra nota credito pagamento anticipato** o l'azione **Registra e stampa nota cr. pagam. ant.**</span><span class="sxs-lookup"><span data-stu-id="e2310-112">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="e2310-113">Nella pagina **Nota credito vendita** rettificare i movimenti desiderati, come per qualsiasi nota di credito vendita.</span><span class="sxs-lookup"><span data-stu-id="e2310-113">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="e2310-114">Per ulteriori informazioni vedere [Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="e2310-114">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="e2310-115">Per ridurre l'importo nel campo **Importo riga**, è necessario prima aumentare la percentuale pagamento anticipato nella riga in modo che il valore nel campo **Importo riga pagam. ant.** non scenda sotto il valore del campo **Fattura importo pagam. ant.**.</span><span class="sxs-lookup"><span data-stu-id="e2310-115">To reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="e2310-116">Per creare una fattura pagamento anticipato per le nuove righe nota di credito di vendita,, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Registra fattura pagamento anticipato** o l'azione **Registra e stampa fattura pagam. ant.**.</span><span class="sxs-lookup"><span data-stu-id="e2310-116">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="e2310-117">Per emettere una fattura pagamento anticipato aggiuntiva, aumentare l'importo pagamento anticipato in una o più righe e registrare la fattura pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="e2310-117">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="e2310-118">Verrà creata una nuova fattura per la differenza tra gli importi di pagamenti anticipati fatturati e i nuovi importi di pagamenti anticipati.</span><span class="sxs-lookup"><span data-stu-id="e2310-118">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2310-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2310-119">See Also</span></span>

[<span data-ttu-id="e2310-120">Fatturazione dei pagamenti anticipati</span><span class="sxs-lookup"><span data-stu-id="e2310-120">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="e2310-121">Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite</span><span class="sxs-lookup"><span data-stu-id="e2310-121">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="e2310-122">Finanze</span><span class="sxs-lookup"><span data-stu-id="e2310-122">Finance</span></span>](finance.md)  
<span data-ttu-id="e2310-123">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2310-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]