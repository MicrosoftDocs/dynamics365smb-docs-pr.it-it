---
title: "Dettagli di progettazione: Struttura dell'interfaccia di registrazione | Microsoft Docs"
description: Questo argomento fornisce una sintesi delle procedure globali nella struttura dell'interfaccia di registrazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 231148c304c5f2dabba5c69c442dfd0cfdc6397d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921944"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="d9804-103">Dettagli di progettazione: struttura dell'interfaccia di registrazione</span><span class="sxs-lookup"><span data-stu-id="d9804-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="d9804-104">Nella struttura dell'interfaccia di registrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] esistono diverse procedure globali che utilizzano la stessa struttura:</span><span class="sxs-lookup"><span data-stu-id="d9804-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="d9804-105">Codice della procedura di chiamata di RunWithoutCheck e di RunWithCheck – interfaccia generica di registrazione per riga</span><span class="sxs-lookup"><span data-stu-id="d9804-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="d9804-106">registrazioni generali.</span><span class="sxs-lookup"><span data-stu-id="d9804-106">Jnl Line.</span></span>  
* <span data-ttu-id="d9804-107">CustPostApplyCustLedgEntry – registrare il collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati.</span><span class="sxs-lookup"><span data-stu-id="d9804-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="d9804-108">VendPostApplyVendLedgEntry – registrare il collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati.</span><span class="sxs-lookup"><span data-stu-id="d9804-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="d9804-109">UnapplyCustLedgEntry – registrare l'annullamento del collegamento del cliente, chiamato da codeunit 226 CustEntry- Collegare i movimenti registrati</span><span class="sxs-lookup"><span data-stu-id="d9804-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="d9804-110">UnapplyVendLedgEntry – registrare l'annullamento del collegamento del fornitore, chiamato da codeunit 227 VendEntry- Collegare i movimenti registrati</span><span class="sxs-lookup"><span data-stu-id="d9804-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9804-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9804-111">See Also</span></span>  
[<span data-ttu-id="d9804-112">Dettagli di progettazione: struttura del motore di registrazione</span><span class="sxs-lookup"><span data-stu-id="d9804-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)