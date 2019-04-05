---
title: Creare un'offerta di acquisto per richiedere un'offerta | Documenti Microsoft
description: Descrive come creare un documento di un'offerta di vendita o una richiesta di offerta (RdO) per registrare la propria offerta a un cliente per la vendita di prodotti in base a termini determinati.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: a243df7928e6468cc3490966331b325134f6cc37
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801893"
---
# <a name="request-quotes"></a><span data-ttu-id="a3bcf-103">Richiedere le offerte</span><span class="sxs-lookup"><span data-stu-id="a3bcf-103">Request Quotes</span></span>
<span data-ttu-id="a3bcf-104">Un'offerta di acquisto può essere utilizzata come bozza preliminare di un ordine di acquisto e l'ordine può essere in seguito convertito in ordine o fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="a3bcf-105">Per creare un'offerta di acquisto</span><span class="sxs-lookup"><span data-stu-id="a3bcf-105">To create a purchase quote</span></span>
1. <span data-ttu-id="a3bcf-106">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Offerte acquisto** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="a3bcf-107">Creare un nuovo documento nello stesso modo in cui si crea un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="a3bcf-108">Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="a3bcf-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="a3bcf-109">Per convertire un'offerta di acquisto in un ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="a3bcf-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="a3bcf-110">Una volta che l'offerta del fornitore viene accettata, può essere convertita in ordine o fattura di acquisto per elaborare l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="a3bcf-111">Aprire un'offerta di acquisto pronta per essere convertita e scegliere l'azione **Crea ordine**.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="a3bcf-112">L'offerta di acquisto viene rimossa dal database.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="a3bcf-113">Viene creato un ordine o una fattura di acquisto sulla base delle informazioni contenute nell'offerta di acquisto nella quale è possibile elaborare l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="a3bcf-114">Nel campo **Nr. offerta** dell'ordine o della fattura di acquisto è presente il numero dell'offerta di acquisto da cui è stato convertito.</span><span class="sxs-lookup"><span data-stu-id="a3bcf-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3bcf-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3bcf-115">See Also</span></span>
[<span data-ttu-id="a3bcf-116">Acquisti</span><span class="sxs-lookup"><span data-stu-id="a3bcf-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a3bcf-117">Impostazioni acquisti</span><span class="sxs-lookup"><span data-stu-id="a3bcf-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="a3bcf-118">Inviare documenti via e-mail</span><span class="sxs-lookup"><span data-stu-id="a3bcf-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="a3bcf-119">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3bcf-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
