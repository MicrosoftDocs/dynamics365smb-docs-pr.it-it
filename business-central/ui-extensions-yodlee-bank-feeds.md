---
title: Riconciliazione dei pagamenti con l'estensione Envestnet Yodlee Bank Feeds | Microsoft Docs
description: Descrive l'estensione Envestnet Yodlee Bank Feeds, che consente di collegare i conti bancari in modo che sia possibile riconciliare rapidamente i pagamenti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6089a51a0ef27175988ed0c00fdb353cd3c7e96c
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692946"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="4c17e-103">Estensione Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="4c17e-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="4c17e-104">Per riconciliare rapidamente i pagamenti effettuati sui conti correnti bancari, il servizio Envestnet Yodlee Bank Feeds consente di collegare il proprio conto bancario di sistema al conto bancario online.</span><span class="sxs-lookup"><span data-stu-id="4c17e-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="4c17e-105">Ciò significa che l'ultimo rendiconto bancario viene caricato automaticamente o manualmente nella registrazione riconciliazione. In questo modo viene garantito che si elaborino sempre gli ultimi pagamenti con il rischio minimo di errori.</span><span class="sxs-lookup"><span data-stu-id="4c17e-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="4c17e-106">Il servizio Envestnet Yodlee Bank Feeds è supportato solo negli Stati Uniti e in Canada.</span><span class="sxs-lookup"><span data-stu-id="4c17e-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="4c17e-107">Il servizio Envestnet Yodlee Bank Feeds è supportato solo nella versione online di Business Central.</span><span class="sxs-lookup"><span data-stu-id="4c17e-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="4c17e-108">Per utilizzare questa funzionalità in locale, è necessario ottenere un conto cobrand di Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="4c17e-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="4c17e-109">Il servizio Envestnet Yodlee Bank Feeds è supportato solo negli Stati Uniti e in Canada.</span><span class="sxs-lookup"><span data-stu-id="4c17e-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="4c17e-110">Sono supportate solo le banche residenti in questi paesi, anche se le banche di altri paesi possono comparire nella finestra di selezione della banca Envestnet Yodlee Bank Feeds in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4c17e-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c17e-111">A causa della nuova direttiva sui servizi di pagamento in Europa (PSD2), dopo il 14 settembre 2019, non sarà più possibile importare automaticamente gli estratti conto bancari dalle banche del Regno Unito in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4c17e-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4c17e-112">Stiamo esaminando la possibilità di offrire nuovamente questa funzionalità in futuro.</span><span class="sxs-lookup"><span data-stu-id="4c17e-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="4c17e-113">Il servizio Envestnet Yodlee Bank Feeds offre i seguenti vantaggi:</span><span class="sxs-lookup"><span data-stu-id="4c17e-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="4c17e-114">Elimina la necessità dell'immissione manuale.</span><span class="sxs-lookup"><span data-stu-id="4c17e-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="4c17e-115">Migliora l'efficienza e l'accuratezza nella riconciliazione dei pagamenti.</span><span class="sxs-lookup"><span data-stu-id="4c17e-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="4c17e-116">Supporta un elevato numero di banche.</span><span class="sxs-lookup"><span data-stu-id="4c17e-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="4c17e-117">Offre informazioni aggiornate sulle transazioni bancarie da [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4c17e-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="4c17e-118">Supporta i feed bancari manuali e automatici.</span><span class="sxs-lookup"><span data-stu-id="4c17e-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="4c17e-119">Consente di assegnare in outsourcing la riconciliazione dei pagamenti a un ragioniere fornendo l'accesso ai rendiconti bancari.</span><span class="sxs-lookup"><span data-stu-id="4c17e-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="4c17e-120">Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="4c17e-120">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c17e-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4c17e-121">See Also</span></span>
<span data-ttu-id="4c17e-122">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="4c17e-122">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="4c17e-123">Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="4c17e-123">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="4c17e-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c17e-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
