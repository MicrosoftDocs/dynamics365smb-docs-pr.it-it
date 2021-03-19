---
title: Impostare i metodi di pagamento
description: Utilizzare i metodi di pagamento, ad esempio, assegni, bonifici, contanti o PayPal, per definire le modalità di pagamento di fatture di vendita e di acquisto.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 01/21/2021
ms.author: bholtorf
ms.openlocfilehash: 7132f96327e468c200ebd1f41c0a1e5b767dea6b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376839"
---
# <a name="set-up-payment-methods"></a><span data-ttu-id="29e78-103">Impostare i metodi di pagamento</span><span class="sxs-lookup"><span data-stu-id="29e78-103">Set Up Payment Methods</span></span>

<span data-ttu-id="29e78-104">I metodi di pagamento consentono di definire il modo in cui si desidera essere pagati dai clienti e quello in cui si intende pagare i fornitori.</span><span class="sxs-lookup"><span data-stu-id="29e78-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="29e78-105">Il metodo può variare per ogni cliente o fornitore.</span><span class="sxs-lookup"><span data-stu-id="29e78-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="29e78-106">Esempi di metodi di pagamento tipici sono **banca**, **contanti**, **assegno**, **conto**.</span><span class="sxs-lookup"><span data-stu-id="29e78-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="29e78-107">È possibile assegnare un metodo di pagamento a clienti e fornitori di modo che lo stesso metodo sia sempre utilizzato per i documenti di vendita e di acquisto create per essi.</span><span class="sxs-lookup"><span data-stu-id="29e78-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="29e78-108">Se necessario, è possibile modificare il metodo nel documento di vendita o di acquisto.</span><span class="sxs-lookup"><span data-stu-id="29e78-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="29e78-109">Ad esempio, se si desidera pagare una determinata fattura di acquisto in contanti anziché tramite assegno.</span><span class="sxs-lookup"><span data-stu-id="29e78-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="29e78-110">Ciò non modifica il metodo di pagamento di default assegnato al fornitore.</span><span class="sxs-lookup"><span data-stu-id="29e78-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="29e78-111">Gli stessi metodi di pagamento sono utilizzati per documenti di vendita e di acquisto.</span><span class="sxs-lookup"><span data-stu-id="29e78-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="29e78-112">Ad esempio, il metodo di pagamento _contanti_ viene utilizzato quando si effettuano e si ricevono pagamenti.</span><span class="sxs-lookup"><span data-stu-id="29e78-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="29e78-113">presuppone che quando si crea una fattura di vendita si prevede di ricevere un pagamento e il contrario per le fatture di acquisto.</span><span class="sxs-lookup"><span data-stu-id="29e78-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="29e78-114">Le note di credito per i resi, tuttavia, sono eccezioni in quanto il flusso di denaro avviene in direzioni opposte, dall'utente al cliente e dal venditore all'utente.</span><span class="sxs-lookup"><span data-stu-id="29e78-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="29e78-115">Di conseguenza, il metodo di pagamento di default non è assegnato alle note di credito.</span><span class="sxs-lookup"><span data-stu-id="29e78-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="29e78-116">Esiste, tuttavia, una soluzione alternativa se sono stati specificati i termini di pagamento per il cliente o il fornitore.</span><span class="sxs-lookup"><span data-stu-id="29e78-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="29e78-117">Sebbene il campo **Calc. sc. pagam. su note credito** non sia destinato a questo scopo, se si sceglie la casella di controllo nella pagina **Condizioni pagamento** il metodo di pagamento di default verrà aggiunto quando si crea una nota di credito.</span><span class="sxs-lookup"><span data-stu-id="29e78-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="29e78-118">Per impostare un metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="29e78-118">To set up a payment method</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="29e78-119">fornisce alcuni metodi di pagamento utilizzati spesso dalle aziende.</span><span class="sxs-lookup"><span data-stu-id="29e78-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="29e78-120">È tuttavia possibile aggiungere tutti quelli desiderati.</span><span class="sxs-lookup"><span data-stu-id="29e78-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="29e78-121">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Metodi di pagamento** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="29e78-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="29e78-122">Compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="29e78-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="29e78-123">Facoltativamente, aggiungi condizioni pagamento al metodo di pagamento.</span><span class="sxs-lookup"><span data-stu-id="29e78-123">Optionally, add payment terms to your payment method.</span></span> <span data-ttu-id="29e78-124">Per ulteriori informazioni, vedi [Impostare le condizioni pagamento](finance-payment-terms.md).</span><span class="sxs-lookup"><span data-stu-id="29e78-124">For more information, see [Set Up Payment Terms](finance-payment-terms.md).</span></span>  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="29e78-125">Per assegnare un metodo di pagamento a un cliente o un fornitore</span><span class="sxs-lookup"><span data-stu-id="29e78-125">To assign a payment method to a customer or vendor</span></span>

1. <span data-ttu-id="29e78-126">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cliente** o **Fornitore** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="29e78-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="29e78-127">Nel campo **Codice metodo di pagamento**, scegliere il metodo da utilizzare per impostazione predefinita per il cliente o il fornitore.</span><span class="sxs-lookup"><span data-stu-id="29e78-127">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="29e78-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="29e78-128">See Also</span></span>

[<span data-ttu-id="29e78-129">Registrare nuovi clienti</span><span class="sxs-lookup"><span data-stu-id="29e78-129">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="29e78-130">Impostare le condizioni pagamento</span><span class="sxs-lookup"><span data-stu-id="29e78-130">Set Up Payment Terms</span></span>](finance-payment-terms.md)  
[<span data-ttu-id="29e78-131">Finanze</span><span class="sxs-lookup"><span data-stu-id="29e78-131">Finance</span></span>](finance.md)  
<span data-ttu-id="29e78-132">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="29e78-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]