---
title: 'Dettagli di progettazione: Gestione warehouse | Microsoft Docs'
description: Questo argomento fornisce una panoramica della progettazione, dei concetti e dei principi alla base delle funzionalità di gestione warehouse in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 25e492318d7581780fd9fe9038531e1ba1c24282
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787176"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="a6c63-103">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="a6c63-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="a6c63-104">La documentazione fornisce una sintesi dei concetti e dei principi utilizzati nelle funzionalità di gestione warehouse in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a6c63-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a6c63-105">Viene descritta la progettazione dietro le funzionalità della warehouse centrale e viene spiegato in che modo la gestione della warehouse si integra con altre funzionalità della supply chain.</span><span class="sxs-lookup"><span data-stu-id="a6c63-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="a6c63-106">Per differenziare i diversi livelli di complessità della gestione della warehouse, la documentazione è divisa in due categorie generali, le configurazioni di base e avanzata della warehouse, indicate nei titoli di sezione.</span><span class="sxs-lookup"><span data-stu-id="a6c63-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="a6c63-107">Questa semplice differenziazione copre livelli diversi di complessità come definito dal setup dell'ubicazione e i sottoprodotti.</span><span class="sxs-lookup"><span data-stu-id="a6c63-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="a6c63-108">Per ulteriori informazioni, vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a6c63-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="a6c63-109">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="a6c63-109">In This Section</span></span>  
[<span data-ttu-id="a6c63-110">Dettagli di progettazione: Panoramica warehouse</span><span class="sxs-lookup"><span data-stu-id="a6c63-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="a6c63-111">Dettagli di progettazione: Setup warehouse</span><span class="sxs-lookup"><span data-stu-id="a6c63-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="a6c63-112">Dettagli di progettazione: Flusso warehouse in entrata</span><span class="sxs-lookup"><span data-stu-id="a6c63-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="a6c63-113">Dettagli di progettazione: Flussi warehouse interni</span><span class="sxs-lookup"><span data-stu-id="a6c63-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="a6c63-114">Dettagli di progettazione: Disponibilità nella warehouse</span><span class="sxs-lookup"><span data-stu-id="a6c63-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="a6c63-115">Dettagli di progettazione: Flusso warehouse in uscita</span><span class="sxs-lookup"><span data-stu-id="a6c63-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="a6c63-116">Dettagli di progettazione: Integrazione con il magazzino</span><span class="sxs-lookup"><span data-stu-id="a6c63-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
