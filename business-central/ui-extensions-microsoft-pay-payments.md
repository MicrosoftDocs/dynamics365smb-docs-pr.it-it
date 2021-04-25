---
title: Microsoft Pay Standard| Microsoft Docs
description: Fornisce informazioni relative all'estensione Microsoft Pay
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 58c7ff08a7359b4f577b7ba40b23bc1f6310da4c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787329"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="8f2e2-103">Estensione Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="8f2e2-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f2e2-104">A partire dall'8 febbraio 2020, le modifiche del servizio Microsoft Pay interesseranno l'estensione Microsoft Pay in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span><span class="sxs-lookup"><span data-stu-id="8f2e2-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span></span> <span data-ttu-id="8f2e2-105">A causa delle modifiche, dopo l'8 febbraio, il collegamento di pagamento **Paga ora** generato dall'estensione Microsoft Pay per le fatture in [!INCLUDE[prod_short](includes/prod_short.md)] non aprirà Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[prod_short](includes/prod_short.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="8f2e2-106">I clienti che utilizzano l'estensione devono modificare l'impostazione dei servizi di pagamento per iniziare a utilizzare l'estensione PayPal.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="8f2e2-107">Dall'8 gennaio, verrà visualizzata una notifica in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8f2e2-107">From January 8, we will display a notification in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8f2e2-108">La notifica contiene un collegamento alle impostazioni che è necessario modificare e a ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="8f2e2-109">Dopo l'8 febbraio, l'esensione Microsoft Pay non sarà più disponibile in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8f2e2-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span><br /></br>
>
> <span data-ttu-id="8f2e2-110">Le modifiche influiscono sulle seguenti versioni di Business Central:</span><span class="sxs-lookup"><span data-stu-id="8f2e2-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="8f2e2-111">Microsoft Dynamics 365 Business Central ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="8f2e2-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="8f2e2-112">Microsoft Dynamics 365 Business Central aprile 2019</span><span class="sxs-lookup"><span data-stu-id="8f2e2-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="8f2e2-113">Microsoft Dynamics 365 Business Central seconda ondata di rilascio 2019</span><span class="sxs-lookup"><span data-stu-id="8f2e2-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="8f2e2-114">I clienti richiedono continuamente un livello di assistenza clienti più elevato, sia in termini di qualità del prodotto sia in termini di servizi di consegna e di pagamento.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="8f2e2-115">Il servizio Microsoft Pay contribuisce a migliorare l'assistenza clienti.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="8f2e2-116">L'estensione Microsoft Pay aggiunge un collegamento Microsoft Pay ai documenti di vendita in modo che i clienti possano facilmente pagare utilizzando Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="8f2e2-117">Quindi è possibile inviare i documenti tramite e-mail per fornire un servizio clienti più elevato e ridurre il tempo necessario per l'arrivo dei pagamenti dei clienti sul conto bancario.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="8f2e2-118">L'estensione Microsoft Pay offre i seguenti vantaggi:</span><span class="sxs-lookup"><span data-stu-id="8f2e2-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="8f2e2-119">I pagamenti dei clienti arrivano più velocemente nel conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="8f2e2-120">I clienti hanno più modi a disposizione per pagare le fatture.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="8f2e2-121">Microsoft Pay offre un servizio di pagamento affidabile, che i clienti preferiscono all'immissione dei dati delle carte di credito sui siti Web sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="8f2e2-122">Microsoft Pay offre molteplici modalità di gestione dei pagamenti, inclusa l'elaborazione delle carte di credito, come PayPal e Stripe.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="8f2e2-123">Il collegamento Microsoft Pay può essere incorporato automaticamente in ogni documento della fattura o dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="8f2e2-124">Poiché questa funzionalità è progettata come un'estensione, offre il controllo completo dell'abilitazione quando e se i processi aziendali la richiedono.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="8f2e2-125">L'abilitazione delle estensioni del servizio di pagamento è gratuita in [!INCLUDE[prod_short](includes/prod_short.md)], tuttavia, sarà necessario contattare il servizio di pagamento per ottenere un conto.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-125">Enabling payment service extensions is free in [!INCLUDE[prod_short](includes/prod_short.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="8f2e2-126">Per ulteriori informazioni, vedere [Abilitare i pagamenti clienti tramite i servizi di pagamento](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8f2e2-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8f2e2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f2e2-127">See Also</span></span>
<span data-ttu-id="8f2e2-128">[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8f2e2-128">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="8f2e2-129">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="8f2e2-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="8f2e2-130">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f2e2-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]