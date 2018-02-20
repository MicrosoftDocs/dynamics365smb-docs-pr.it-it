---
title: Trasferimento automatico e movimenti combinati | Microsoft Docs
description: "Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata. È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo. Nella seguente tabella vengono illustrate le diverse opzioni."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f4796d9796788d2fbbf5706688aec75a4ed9a6d8
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="c377f-105">Trasferimento automatico e movimenti combinati</span><span class="sxs-lookup"><span data-stu-id="c377f-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="c377f-106">Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata.</span><span class="sxs-lookup"><span data-stu-id="c377f-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="c377f-107">È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo.</span><span class="sxs-lookup"><span data-stu-id="c377f-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="c377f-108">Nella seguente tabella vengono illustrate le diverse opzioni.</span><span class="sxs-lookup"><span data-stu-id="c377f-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="c377f-109">Cumula movimenti</span><span class="sxs-lookup"><span data-stu-id="c377f-109">Combine entries</span></span>|<span data-ttu-id="c377f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c377f-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="c377f-111">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c377f-111">None</span></span>|<span data-ttu-id="c377f-112">Ogni movimento C/G viene trasferito singolarmente al tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c377f-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="c377f-113">Giorno</span><span class="sxs-lookup"><span data-stu-id="c377f-113">Day</span></span>|<span data-ttu-id="c377f-114">I movimenti C/G con la stessa data di registrazione vengono trasferiti come un unico movimento nel tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c377f-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="c377f-115">Mese</span><span class="sxs-lookup"><span data-stu-id="c377f-115">Month</span></span>|<span data-ttu-id="c377f-116">Tutti i movimenti C/G dello stesso mese di calendario vengono trasferiti come un unico movimento nel tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c377f-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="c377f-117">Se si è selezionata la casella di controllo **Trasferimento automatico da CG** nella finestra **Setup contabilità industriale**, [!INCLUDE[d365fin](includes/d365fin_md.md)] aggiorna la contabilità dopo ogni registrazione nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="c377f-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="c377f-118">Le entità combinate non sono possibili.</span><span class="sxs-lookup"><span data-stu-id="c377f-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c377f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c377f-119">See Also</span></span>  
 <span data-ttu-id="c377f-120">[Trasferire movimenti C/G a movimenti di costi](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c377f-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="c377f-121">[Criteri per trasferire movimenti C/G ai movimenti di costi](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c377f-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="c377f-122">[Risultati del trasferimento](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="c377f-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="c377f-123">Trasferimento e registrazione di movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="c377f-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="c377f-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c377f-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

