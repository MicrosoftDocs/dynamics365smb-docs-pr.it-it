---
title: Riconciliazione dei pagamenti con l'estensione Envestnet Yodlee Bank Feeds | Documenti Microsoft
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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53ee8bb7ee798c473e1053ea8413be28f9185d1b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248205"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="c17d2-103">Estensione Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="c17d2-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="c17d2-104">Per riconciliare rapidamente i pagamenti effettuati sui conti correnti bancari, il servizio Envestnet Yodlee Bank Feeds consente di collegare il proprio conto bancario di sistema al conto bancario online.</span><span class="sxs-lookup"><span data-stu-id="c17d2-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="c17d2-105">Ciò significa che l'ultimo rendiconto bancario viene caricato automaticamente o manualmente nella registrazione riconciliazione. In questo modo viene garantito che si elaborino sempre gli ultimi pagamenti con il rischio minimo di errori.</span><span class="sxs-lookup"><span data-stu-id="c17d2-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

> [!NOTE]
> <span data-ttu-id="c17d2-106">Questa funzione è supportata solo nella versione online di Business Central.</span><span class="sxs-lookup"><span data-stu-id="c17d2-106">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="c17d2-107">Per utilizzare questa funzionalità in locale, è necessario ottenere un conto cobrand di Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="c17d2-107">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span>

<span data-ttu-id="c17d2-108">Il servizio Envestnet Yodlee Bank Feeds fornisce i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c17d2-108">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="c17d2-109">Elimina la necessità dell'immissione manuale.</span><span class="sxs-lookup"><span data-stu-id="c17d2-109">Removes the need for manual entry.</span></span>
* <span data-ttu-id="c17d2-110">Migliora l'efficienza e l'accuratezza nella riconciliazione dei pagamenti.</span><span class="sxs-lookup"><span data-stu-id="c17d2-110">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="c17d2-111">Supporta un elevato numero di banche.</span><span class="sxs-lookup"><span data-stu-id="c17d2-111">Supports a large number of banks.</span></span>
* <span data-ttu-id="c17d2-112">Offre informazioni aggiornate sulle transazioni bancarie da [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c17d2-112">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="c17d2-113">Supporta i feed bancari manuali e automatici.</span><span class="sxs-lookup"><span data-stu-id="c17d2-113">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="c17d2-114">Consente di assegnare in outsourcing la riconciliazione dei pagamenti a un ragioniere fornendo l'accesso ai rendiconti bancari.</span><span class="sxs-lookup"><span data-stu-id="c17d2-114">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="c17d2-115">Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="c17d2-115">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c17d2-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c17d2-116">See Also</span></span>
<span data-ttu-id="c17d2-117">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="c17d2-117">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="c17d2-118">Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="c17d2-118">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="c17d2-119">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c17d2-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
