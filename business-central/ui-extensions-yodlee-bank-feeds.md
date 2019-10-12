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
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315350"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="2dd50-103">Estensione Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="2dd50-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="2dd50-104">Per riconciliare rapidamente i pagamenti effettuati sui conti correnti bancari, il servizio Envestnet Yodlee Bank Feeds consente di collegare il proprio conto bancario di sistema al conto bancario online.</span><span class="sxs-lookup"><span data-stu-id="2dd50-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="2dd50-105">Ciò significa che l'ultimo rendiconto bancario viene caricato automaticamente o manualmente nella registrazione riconciliazione. In questo modo viene garantito che si elaborino sempre gli ultimi pagamenti con il rischio minimo di errori.</span><span class="sxs-lookup"><span data-stu-id="2dd50-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="2dd50-106">Il servizio Envestnet Yodlee Bank Feeds è supportato solo negli Stati Uniti e in Canada.</span><span class="sxs-lookup"><span data-stu-id="2dd50-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="2dd50-107">Questa funzione è supportata solo nella versione online di Business Central.</span><span class="sxs-lookup"><span data-stu-id="2dd50-107">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="2dd50-108">Per utilizzare questa funzionalità in locale, è necessario ottenere un conto cobrand di Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="2dd50-108">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />

> [!IMPORTANT]
> <span data-ttu-id="2dd50-109">A causa della nuova direttiva sui servizi di pagamento in Europa (PSD2), dopo il 14 settembre 2019, non sarà più possibile importare automaticamente gli estratti conto bancari dalle banche del Regno Unito in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2dd50-109">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2dd50-110">Stiamo esaminando la possibilità di offrire nuovamente questa funzionalità in futuro.</span><span class="sxs-lookup"><span data-stu-id="2dd50-110">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="2dd50-111">Il servizio Envestnet Yodlee Bank Feeds offre i seguenti vantaggi:</span><span class="sxs-lookup"><span data-stu-id="2dd50-111">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="2dd50-112">Elimina la necessità dell'immissione manuale.</span><span class="sxs-lookup"><span data-stu-id="2dd50-112">Removes the need for manual entry.</span></span>
* <span data-ttu-id="2dd50-113">Migliora l'efficienza e l'accuratezza nella riconciliazione dei pagamenti.</span><span class="sxs-lookup"><span data-stu-id="2dd50-113">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="2dd50-114">Supporta un elevato numero di banche.</span><span class="sxs-lookup"><span data-stu-id="2dd50-114">Supports a large number of banks.</span></span>
* <span data-ttu-id="2dd50-115">Offre informazioni aggiornate sulle transazioni bancarie da [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2dd50-115">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="2dd50-116">Supporta i feed bancari manuali e automatici.</span><span class="sxs-lookup"><span data-stu-id="2dd50-116">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="2dd50-117">Consente di assegnare in outsourcing la riconciliazione dei pagamenti a un ragioniere fornendo l'accesso ai rendiconti bancari.</span><span class="sxs-lookup"><span data-stu-id="2dd50-117">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="2dd50-118">Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="2dd50-118">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2dd50-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2dd50-119">See Also</span></span>
<span data-ttu-id="2dd50-120">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="2dd50-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="2dd50-121">Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="2dd50-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="2dd50-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2dd50-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
