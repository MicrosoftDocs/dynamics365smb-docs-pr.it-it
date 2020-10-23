---
title: Saldare immediatamente le fatture di acquisto
description: Se si deve pagare il fornitore in contanti o con assegno, è possibile effettuare la necessaria registrazione contemporaneamente a quella della fattura.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: bac023393d95623a2731ef1b2ada7d30b135063b
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968361"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="6edc6-103">Saldare immediatamente le fatture di acquisto</span><span class="sxs-lookup"><span data-stu-id="6edc6-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="6edc6-104">Se si deve pagare il fornitore in contanti o con assegno, è possibile registrare il pagamento mentre si registra la fattura.</span><span class="sxs-lookup"><span data-stu-id="6edc6-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="6edc6-105">Se le fatture di acquisto sono spesso pagate in contanti, in assegni o con bonifico è una buona idea impostare un metodo di pagamento specifico con una contropartita e immetterlo nel campo **Metodo Pagamento** nella scheda del fornitore.</span><span class="sxs-lookup"><span data-stu-id="6edc6-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="6edc6-106">Il numero della contropartita verrà immesso automaticamente nella testata della fattura ogni volta che ne verrà creata una nuova.</span><span class="sxs-lookup"><span data-stu-id="6edc6-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="6edc6-107">Per ulteriori informazioni, vedere [Definizione dei metodi di pagamento](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6edc6-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="6edc6-108">Per saldare immediatamente le fatture di acquisto</span><span class="sxs-lookup"><span data-stu-id="6edc6-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="6edc6-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6edc6-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6edc6-110">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="6edc6-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="6edc6-111">Per pagare in contanti o tramite bonifico, immettere il numero del conto cassa di contabilità generale o il conto corrente bancario nel campo **Nr. contropartita**.</span><span class="sxs-lookup"><span data-stu-id="6edc6-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="6edc6-112">I campi **Tipo Contropartita** e **Contropartita** non sono inclusi nel layout standard della testata della fattura.</span><span class="sxs-lookup"><span data-stu-id="6edc6-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="6edc6-113">Per registrare il pagamento di una fattura è necessario contattare un partner Microsoft che può aggiungere i campi tramite codice.</span><span class="sxs-lookup"><span data-stu-id="6edc6-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="6edc6-114">Questa personalizzazione è richiesta solo se non si specificano conti di contropartita per i metodi di pagamento come descritto sopra.</span><span class="sxs-lookup"><span data-stu-id="6edc6-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="6edc6-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6edc6-115">See Also</span></span>

[<span data-ttu-id="6edc6-116">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="6edc6-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="6edc6-117">Acquisti</span><span class="sxs-lookup"><span data-stu-id="6edc6-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6edc6-118">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6edc6-118">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
