---
title: Criteri per trasferire movimenti C/G ai movimenti di costi | Microsoft Docs
description: "È importante comprendere i criteri per trasferire i movimenti C/G nei movimenti di costi. Durante il trasferimento, il processo batch **Trasferisci movimenti C/G a CA** utilizza i seguenti criteri per determinare se e come i movimenti C/G vengono trasferiti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 59faad50504bff05e6cdb1c78d00553e85faf47e
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="69e80-104">Criteri per trasferire movimenti C/G ai movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="69e80-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="69e80-105">È importante comprendere i criteri per trasferire i movimenti C/G nei movimenti di costi.</span><span class="sxs-lookup"><span data-stu-id="69e80-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="69e80-106">Durante il trasferimento, il processo batch **Trasferisci movimenti C/G a CA** utilizza i seguenti criteri per determinare se e come i movimenti C/G vengono trasferiti.</span><span class="sxs-lookup"><span data-stu-id="69e80-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="69e80-107">I movimenti C/G vengono trasferiti nei seguenti casi:</span><span class="sxs-lookup"><span data-stu-id="69e80-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="69e80-108">Ai movimenti sono associati valori dimensioni che corrispondono a un centro di costo o un oggetto di costo.</span><span class="sxs-lookup"><span data-stu-id="69e80-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="69e80-109">Ai movimenti sono associati valori dimensioni che corrispondono a un centro di costo e a un oggetto di costo.</span><span class="sxs-lookup"><span data-stu-id="69e80-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="69e80-110">Per questi movimenti, il centro di costo ha la precedenza.</span><span class="sxs-lookup"><span data-stu-id="69e80-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="69e80-111">Questo consente di evitare una situazione in cui un tipo di costo viene visualizzato sia in un oggetto di costo sia in un centro di costo, venendo pertanto conteggiato due volte nelle statistiche.</span><span class="sxs-lookup"><span data-stu-id="69e80-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="69e80-112">Il numero di documento nei movimenti è vuoto, pertanto verrà visualizzato con un numero di documento pari a 0000 nei movimenti di costo.</span><span class="sxs-lookup"><span data-stu-id="69e80-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="69e80-113">I movimenti vengono trasferiti in un tipo di costo che consente movimenti combinati e tali movimenti vengono trasferiti come movimento combinato mensilmente o giornalmente.</span><span class="sxs-lookup"><span data-stu-id="69e80-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="69e80-114">I movimenti C/G non vengono trasferiti nei seguenti casi:</span><span class="sxs-lookup"><span data-stu-id="69e80-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="69e80-115">Ai movimenti sono associati valori dimensioni che non corrispondono a un centro di costo o un oggetto di costo.</span><span class="sxs-lookup"><span data-stu-id="69e80-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="69e80-116">Ai movimenti è associato un importo pari a zero.</span><span class="sxs-lookup"><span data-stu-id="69e80-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="69e80-117">Ai movimenti è associato un conto di contabilità generale che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="69e80-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="69e80-118">Ai movimenti è associato un conto di contabilità generale che non è di tipo **Conto economico**.</span><span class="sxs-lookup"><span data-stu-id="69e80-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="69e80-119">Ai movimenti è associato un conto di contabilità generale a cui non è assegnato un tipo di costo.</span><span class="sxs-lookup"><span data-stu-id="69e80-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="69e80-120">I movimenti hanno una data di registrazione anteriore alla **Data inizio per trasferimento CG**.</span><span class="sxs-lookup"><span data-stu-id="69e80-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="69e80-121">Registrazione dei movimenti con data chiusura completata.</span><span class="sxs-lookup"><span data-stu-id="69e80-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="69e80-122">Si tratta in genere di movimenti che reimpostano il saldo del conto economico alla fine dell'anno.</span><span class="sxs-lookup"><span data-stu-id="69e80-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69e80-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69e80-123">See Also</span></span>  
[<span data-ttu-id="69e80-124">Contabilizzazione dei costi</span><span class="sxs-lookup"><span data-stu-id="69e80-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="69e80-125">[Procedura: Trasferire movimenti C/G ai movimenti di costi](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="69e80-125">[How to: Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="69e80-126">[Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="69e80-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="69e80-127">Informazioni sulla contabilità industriale</span><span class="sxs-lookup"><span data-stu-id="69e80-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="69e80-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="69e80-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

