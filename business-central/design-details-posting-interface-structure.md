---
title: "Dettagli di progettazione: Struttura dell'interfaccia di registrazione | Microsoft Docs"
description: Questo argomento fornisce una sintesi delle procedure globali nella struttura dell'interfaccia di registrazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b852d6e5d7f96cfba64de219ca414de60cea3a31
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777602"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="3b03b-103">Dettagli di progettazione: struttura dell'interfaccia di registrazione</span><span class="sxs-lookup"><span data-stu-id="3b03b-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="3b03b-104">Nella struttura dell'interfaccia di registrazione di [!INCLUDE[prod_short](includes/prod_short.md)] esistono diverse procedure globali che utilizzano la stessa struttura:</span><span class="sxs-lookup"><span data-stu-id="3b03b-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="3b03b-105">Codice della procedura di chiamata di RunWithoutCheck e di RunWithCheck – interfaccia generica di registrazione per riga</span><span class="sxs-lookup"><span data-stu-id="3b03b-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="3b03b-106">registrazioni generali.</span><span class="sxs-lookup"><span data-stu-id="3b03b-106">Jnl Line.</span></span>  
* <span data-ttu-id="3b03b-107">CustPostApplyCustLedgEntry – registrare il collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati.</span><span class="sxs-lookup"><span data-stu-id="3b03b-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="3b03b-108">VendPostApplyVendLedgEntry – registrare il collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati.</span><span class="sxs-lookup"><span data-stu-id="3b03b-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="3b03b-109">UnapplyCustLedgEntry – registrare l'annullamento del collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati</span><span class="sxs-lookup"><span data-stu-id="3b03b-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="3b03b-110">UnapplyVendLedgEntry – registrare l'annullamento del collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati</span><span class="sxs-lookup"><span data-stu-id="3b03b-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b03b-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b03b-111">See Also</span></span>  
[<span data-ttu-id="3b03b-112">Dettagli di progettazione: struttura del motore di registrazione</span><span class="sxs-lookup"><span data-stu-id="3b03b-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]