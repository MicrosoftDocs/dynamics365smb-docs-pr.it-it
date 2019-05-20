---
title: 'Dettagli di progettazione: Movimenti set di dimensioni | Microsoft Docs'
description: Questa documentazione fornisce informazioni tecniche dettagliate sui concetti e sui principi utilizzati per riprogettare la funzionalità di archiviazione e registrazione dei movimenti dimensioni.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242746"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="fa058-103">Dettagli di progettazione: Movimenti set di dimensioni</span><span class="sxs-lookup"><span data-stu-id="fa058-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="fa058-104">Questa documentazione fornisce informazioni tecniche dettagliate sui concetti e sui principi della funzionalità di archiviazione e registrazione dei movimenti dimensioni in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fa058-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fa058-105">Viene innanzitutto illustrata una panoramica dei concetti.</span><span class="sxs-lookup"><span data-stu-id="fa058-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="fa058-106">Successivamente, viene descritta l'architettura tecnica.</span><span class="sxs-lookup"><span data-stu-id="fa058-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="fa058-107">Infine, vengono forniti esempi di codice per preparare l'utente alla migrazione e all'aggiornamento dalle versioni precedenti alla versione Dynamics NAV 2013R2.</span><span class="sxs-lookup"><span data-stu-id="fa058-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="fa058-108">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="fa058-108">In This Section</span></span>  
[<span data-ttu-id="fa058-109">Sintesi movimenti set di dimensioni</span><span class="sxs-lookup"><span data-stu-id="fa058-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="fa058-110">Dettagli di progettazione: Ricerca delle combinazioni di dimensione</span><span class="sxs-lookup"><span data-stu-id="fa058-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="fa058-111">Dettagli di progettazione: Struttura della tabella</span><span class="sxs-lookup"><span data-stu-id="fa058-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="fa058-112">Dettagli di progettazione: Gestione dimensioni della codeunit 408</span><span class="sxs-lookup"><span data-stu-id="fa058-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="fa058-113">Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche</span><span class="sxs-lookup"><span data-stu-id="fa058-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
