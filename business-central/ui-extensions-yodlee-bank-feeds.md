---
title: Riconciliazione dei pagamenti con l'estensione Feed bancario di Envestnet Yodlee | Documenti Microsoft
description: Descrive l'estensione Feed bancario di Envestnet Yodlee, che consente di collegare i conti bancari in modo che sia possibile riconciliare rapidamente i pagamenti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 02/26/2019
ms.author: sgroespe
ms.openlocfilehash: 36400b3265517c29f68f7eb59d17d968334e0fb1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802266"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="76c94-103">Estensione Feed bancari Envestnet Yodlee</span><span class="sxs-lookup"><span data-stu-id="76c94-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="76c94-104">Per riconciliare rapidamente i pagamenti effettuati sui conti correnti bancari, il servizio Feed bancari di Envestnet Yodlee consente di collegare il proprio conto bancario di sistema al conto bancario online.</span><span class="sxs-lookup"><span data-stu-id="76c94-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="76c94-105">Ciò significa che l'ultimo rendiconto bancario viene caricato automaticamente o manualmente nella registrazione riconciliazione. In questo modo viene garantito che si elaborino sempre gli ultimi pagamenti con il rischio minimo di errori.</span><span class="sxs-lookup"><span data-stu-id="76c94-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

> [!NOTE]
> <span data-ttu-id="76c94-106">Questa funzione è supportata solo nella versione online di Business Central.</span><span class="sxs-lookup"><span data-stu-id="76c94-106">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="76c94-107">Per utilizzare questa funzionalità in locale, è necessario ottenere un conto cobrand di Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="76c94-107">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span>

<span data-ttu-id="76c94-108">Il servizio Feed bancari di Envestnet Yodlee fornisce i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="76c94-108">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="76c94-109">Elimina la necessità dell'immissione manuale.</span><span class="sxs-lookup"><span data-stu-id="76c94-109">Removes the need for manual entry.</span></span>
* <span data-ttu-id="76c94-110">Migliora l'efficienza e l'accuratezza nella riconciliazione dei pagamenti.</span><span class="sxs-lookup"><span data-stu-id="76c94-110">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="76c94-111">Supporta un elevato numero di banche.</span><span class="sxs-lookup"><span data-stu-id="76c94-111">Supports a large number of banks.</span></span>
* <span data-ttu-id="76c94-112">Offre informazioni aggiornate sulle transazioni bancarie da [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="76c94-112">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="76c94-113">Supporta i feed bancari manuali e automatici.</span><span class="sxs-lookup"><span data-stu-id="76c94-113">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="76c94-114">Consente di assegnare in outsourcing la riconciliazione dei pagamenti a un ragioniere fornendo l'accesso ai rendiconti bancari.</span><span class="sxs-lookup"><span data-stu-id="76c94-114">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="76c94-115">Per ulteriori informazioni, vedere [Impostare il servizio Feed bancari di Envestnet Yodlee](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="76c94-115">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="76c94-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76c94-116">See Also</span></span>
<span data-ttu-id="76c94-117">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="76c94-117">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="76c94-118">Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="76c94-118">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="76c94-119">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76c94-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
