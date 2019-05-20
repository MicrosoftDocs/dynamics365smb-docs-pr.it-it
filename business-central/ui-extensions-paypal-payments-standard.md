---
title: Utilizzo dell'estensione PayPal Payments Standard | Documenti Microsoft
description: Descrive come utilizzare l'estensione per consentire ai clienti di eseguire pagamenti con PayPal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f715108b17d355084fee7983e106cd33dd476906
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249769"
---
# <a name="the-paypal-payments-standard-extension"></a><span data-ttu-id="8c9a2-103">Estensione PayPal Payments Standard</span><span class="sxs-lookup"><span data-stu-id="8c9a2-103">The PayPal Payments Standard Extension</span></span>
<span data-ttu-id="8c9a2-104">I clienti richiedono continuamente un livello di assistenza clienti più elevato, sia in termini di qualità del prodotto sia in termini di opzioni di consegna e di pagamento.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="8c9a2-105">Il servizio PayPal Payments Standard contribuisce a migliorare l'assistenza clienti.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="8c9a2-106">Come alternativa alla riscossione dei pagamenti tramite bonifico o carte di credito, è possibile offrire ai clienti di pagare tramite il conto PayPal.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="8c9a2-107">Quando si invia una fattura di vendita o un ordine di vendita tramite e-mail, nel corpo e-mail e nel documento PDF allegato è presente un collegamento a PayPal.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="8c9a2-108">Quando il cliente sceglie il collegamento, viene visualizzata la pagina di assistenza per il conto PayPal nella quale sono disponibili i dettagli di pagamento per la vendita.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="8c9a2-109">Il cliente può quindi pagare la fattura con la stessa modalità di un qualsiasi altro pagamento PayPal.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="8c9a2-110">Il servizio PayPal Payments Standard offre i seguenti vantaggi:</span><span class="sxs-lookup"><span data-stu-id="8c9a2-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="8c9a2-111">I pagamenti dei clienti arrivano più velocemente nel conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="8c9a2-112">I clienti hanno più modi a disposizione per pagare le fatture.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="8c9a2-113">PayPal offre un servizio di pagamento affidabile, che i clienti preferiscono all'immissione dei dati delle carte di credito sui siti Web.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="8c9a2-114">PayPal offre molteplici modalità di gestione dei pagamenti, inclusa l'elaborazione delle carte di credito, i conti PayPal e altre risorse.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="8c9a2-115">È possibile aggiungere automaticamente il collegamento di PayPal ai documenti di vendita. Può farlo anche manualmente l'utente interessato.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="8c9a2-116">Il servizio PayPal Payments Standard non prevede costi mensili o di installazione.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="8c9a2-117">Dal momento che si tratta di un'estensione, il servizio PayPal Payment Standard può essere abilitato facilmente quando e se richiesto.</span><span class="sxs-lookup"><span data-stu-id="8c9a2-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="8c9a2-118">Per ulteriori informazioni, vedere [Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8c9a2-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c9a2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c9a2-119">See Also</span></span>
<span data-ttu-id="8c9a2-120">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8c9a2-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="8c9a2-121">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="8c9a2-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="8c9a2-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c9a2-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
