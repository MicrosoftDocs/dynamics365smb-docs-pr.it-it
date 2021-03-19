---
title: 'Dettagli di progettazione: Costing di magazzino | Microsoft Docs'
description: In questa documentazione sono fornite informazioni tecniche dettagliate sui concetti e sui principi utilizzati nelle funzionalità di magazzino e costing in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a14c2a81a6aa36ce57384decb9342660297f9a84
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389926"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="9bca4-103">Dettagli di progettazione: Costing di magazzino</span><span class="sxs-lookup"><span data-stu-id="9bca4-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="9bca4-104">In questa documentazione sono fornite informazioni tecniche dettagliate sui concetti e sui principi utilizzati nelle funzionalità di magazzino e costing in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9bca4-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="9bca4-105">Il costing di magazzino, detto anche gestione costing riguarda la registrazione e il reporting dei costi operativi business.</span><span class="sxs-lookup"><span data-stu-id="9bca4-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="9bca4-106">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="9bca4-106">In This Section</span></span>  
[<span data-ttu-id="9bca4-107">Dettagli di progettazione: Metodi di costing</span><span class="sxs-lookup"><span data-stu-id="9bca4-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="9bca4-108">Dettagli di progettazione: Collegamento articoli</span><span class="sxs-lookup"><span data-stu-id="9bca4-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="9bca4-109">Dettagli di progettazione: Problema noto di collegamento articoli</span><span class="sxs-lookup"><span data-stu-id="9bca4-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="9bca4-110">Dettagli di progettazione: Rettifica costo</span><span class="sxs-lookup"><span data-stu-id="9bca4-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="9bca4-111">Dettagli di progettazione: Data di registrazione del movimento di valorizzazione della rettifica</span><span class="sxs-lookup"><span data-stu-id="9bca4-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="9bca4-112">Dettagli di progettazione: Registrazione del costo previsto</span><span class="sxs-lookup"><span data-stu-id="9bca4-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="9bca4-113">Dettagli di progettazione: Costo medio</span><span class="sxs-lookup"><span data-stu-id="9bca4-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="9bca4-114">Dettagli di progettazione: Scostamento</span><span class="sxs-lookup"><span data-stu-id="9bca4-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="9bca4-115">Dettagli di progettazione: Arrotondamento</span><span class="sxs-lookup"><span data-stu-id="9bca4-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="9bca4-116">Dettagli di progettazione: Componenti costo</span><span class="sxs-lookup"><span data-stu-id="9bca4-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="9bca4-117">Dettagli di progettazione: Periodi di magazzino</span><span class="sxs-lookup"><span data-stu-id="9bca4-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="9bca4-118">Dettagli di progettazione: Registrazione di magazzino</span><span class="sxs-lookup"><span data-stu-id="9bca4-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="9bca4-119">Dettagli di progettazione: Registrazione dell'ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="9bca4-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="9bca4-120">Dettagli di progettazione: Registrazione dell'ordine di assemblaggio</span><span class="sxs-lookup"><span data-stu-id="9bca4-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="9bca4-121">Dettagli di progettazione: Riconciliazione con la contabilità generale</span><span class="sxs-lookup"><span data-stu-id="9bca4-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="9bca4-122">Dettagli di progettazione: Conti nella contabilità generale</span><span class="sxs-lookup"><span data-stu-id="9bca4-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="9bca4-123">Dettagli di progettazione: Valutazione di magazzino</span><span class="sxs-lookup"><span data-stu-id="9bca4-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="9bca4-124">Dettagli di progettazione: Rivalutazione</span><span class="sxs-lookup"><span data-stu-id="9bca4-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]