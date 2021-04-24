---
title: Riconciliazione dei pagamenti con l'estensione Envestnet Yodlee Bank Feeds
description: Descrive l'estensione Envestnet Yodlee Bank Feeds, che consente di collegare i conti bancari in modo che sia possibile riconciliare rapidamente i pagamenti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9bdbcc208429bba15e30bc56cc8a4477312c1cdd
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771237"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="aa9f6-103">Estensione Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="aa9f6-103">The Envestnet Yodlee Bank Feeds Extension</span></span>

<span data-ttu-id="aa9f6-104">Per riconciliare rapidamente i pagamenti effettuati sui conti correnti bancari, il servizio Envestnet Yodlee Bank Feeds consente di collegare il proprio conto bancario di sistema al conto bancario online.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="aa9f6-105">Ciò significa che l'ultimo rendiconto bancario viene caricato automaticamente o manualmente nella registrazione riconciliazione. In questo modo viene garantito che si elaborino sempre gli ultimi pagamenti con il rischio minimo di errori.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="aa9f6-106">Il servizio Envestnet Yodlee Bank Feeds è supportato solo negli Stati Uniti e in Canada.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="aa9f6-107">Il servizio Envestnet Yodlee Bank Feeds è supportato solo nella versione online di Business Central.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="aa9f6-108">Per utilizzare questa funzionalità in locale, è necessario ottenere un conto cobrand di Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="aa9f6-109">Il servizio Envestnet Yodlee Bank Feeds è supportato solo negli Stati Uniti e in Canada.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="aa9f6-110">Sono supportate solo le banche residenti in questi paesi, anche se le banche di altri paesi possono comparire nella finestra di selezione della banca Envestnet Yodlee Bank Feeds in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="aa9f6-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa9f6-111">A causa della nuova direttiva sui servizi di pagamento in Europa (PSD2), dopo il 14 settembre 2019, non sarà più possibile importare automaticamente gli estratti conto bancari dalle banche del Regno Unito in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="aa9f6-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="aa9f6-112">Stiamo esaminando la possibilità di offrire nuovamente questa funzionalità in futuro.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="aa9f6-113">Il servizio Envestnet Yodlee Bank Feeds offre i seguenti vantaggi:</span><span class="sxs-lookup"><span data-stu-id="aa9f6-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="aa9f6-114">Elimina la necessità dell'immissione manuale.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="aa9f6-115">Migliora l'efficienza e l'accuratezza nella riconciliazione dei pagamenti.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="aa9f6-116">Supporta un elevato numero di banche.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="aa9f6-117">Offre informazioni aggiornate sulle transazioni bancarie da [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="aa9f6-117">Allows up-to-date information about bank transactions from within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
* <span data-ttu-id="aa9f6-118">Supporta i feed bancari manuali e automatici.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="aa9f6-119">Consente di assegnare in outsourcing la riconciliazione dei pagamenti a un ragioniere fornendo l'accesso ai rendiconti bancari.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="aa9f6-120">Feed bancari disponibili</span><span class="sxs-lookup"><span data-stu-id="aa9f6-120">Available Bank Feeds</span></span>
<span data-ttu-id="aa9f6-121">È possibile verificare se una banca è supportata configurando la connessione al servizio Envestnet Yodlee Bank Feeds.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="aa9f6-122">La banca apparirà nell'elenco se è supportata da Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="aa9f6-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="aa9f6-123">Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="aa9f6-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="aa9f6-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aa9f6-124">See Also</span></span>
<span data-ttu-id="aa9f6-125">[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="aa9f6-125">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="aa9f6-126">Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="aa9f6-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="aa9f6-127">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa9f6-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]