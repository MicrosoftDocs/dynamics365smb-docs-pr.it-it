---
title: 'Dettagli di progettazione: riga di registrazione di contabilità generale | Microsoft Docs'
description: Questo argomento fornisce informazioni dettagliate sui concetti e sui principi utilizzati per riprogettare la funzionalità della riga di registrazione di contabilità generale in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215230"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="84957-103">Dettagli di progettazione: riga di registrazione di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="84957-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="84957-104">Questa documentazione fornisce informazioni tecniche dettagliate sui concetti e sui principi utilizzati per riprogettare la funzionalità della riga di registrazione di contabilità generale in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="84957-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="84957-105">La riprogettazione ha semplificato e resa più facile la manutenzione di codeunit 12.</span><span class="sxs-lookup"><span data-stu-id="84957-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="84957-106">Viene innanzitutto illustrata una panoramica dei concetti alla base della riprogettazione.</span><span class="sxs-lookup"><span data-stu-id="84957-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="84957-107">Viene quindi illustrata l'architettura tecnica per mostrare le modifiche conseguenti alla riprogettazione.</span><span class="sxs-lookup"><span data-stu-id="84957-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="84957-108">Le informazioni in questa sezione si applicano alla riprogettazione in una versione precedente del prodotto, Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="84957-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84957-109">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="84957-109">In This Section</span></span>

[<span data-ttu-id="84957-110">Sintesi della riga di registrazione di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="84957-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="84957-111">Dettagli di progettazione: Struttura dell'interfaccia di registrazione</span><span class="sxs-lookup"><span data-stu-id="84957-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="84957-112">Dettagli di progettazione: struttura del motore di registrazione</span><span class="sxs-lookup"><span data-stu-id="84957-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="84957-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="84957-113">See Also</span></span>

<span data-ttu-id="84957-114">[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)
[Dettagli di progettazione: Riga di registrazione di contabilità generale (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="84957-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]