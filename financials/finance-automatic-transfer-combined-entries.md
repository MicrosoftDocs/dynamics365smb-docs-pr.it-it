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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bd80d0a7a701256dfdae3346e899b84eeb990a40
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="233d4-105">Trasferimento automatico e movimenti combinati</span><span class="sxs-lookup"><span data-stu-id="233d4-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="233d4-106">Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata.</span><span class="sxs-lookup"><span data-stu-id="233d4-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="233d4-107">È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo.</span><span class="sxs-lookup"><span data-stu-id="233d4-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="233d4-108">Nella seguente tabella vengono illustrate le diverse opzioni.</span><span class="sxs-lookup"><span data-stu-id="233d4-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="233d4-109">Cumula movimenti</span><span class="sxs-lookup"><span data-stu-id="233d4-109">Combine entries</span></span>|<span data-ttu-id="233d4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="233d4-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="233d4-111">Nessuno</span><span class="sxs-lookup"><span data-stu-id="233d4-111">None</span></span>|<span data-ttu-id="233d4-112">Ogni movimento C/G viene trasferito singolarmente al tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="233d4-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="233d4-113">Giorno</span><span class="sxs-lookup"><span data-stu-id="233d4-113">Day</span></span>|<span data-ttu-id="233d4-114">I movimenti C/G con la stessa data di registrazione vengono trasferiti come un unico movimento nel tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="233d4-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="233d4-115">Mese</span><span class="sxs-lookup"><span data-stu-id="233d4-115">Month</span></span>|<span data-ttu-id="233d4-116">Tutti i movimenti C/G dello stesso mese di calendario vengono trasferiti come un unico movimento nel tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="233d4-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="233d4-117">Se si è selezionata la casella di controllo **Trasferimento automatico da CG** nella finestra **Setup contabilità industriale**, [!INCLUDE[d365fin](includes/d365fin_md.md)] aggiorna la contabilità dopo ogni registrazione nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="233d4-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="233d4-118">Le entità combinate non sono possibili.</span><span class="sxs-lookup"><span data-stu-id="233d4-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="233d4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="233d4-119">See Also</span></span>  
 <span data-ttu-id="233d4-120">[Procedura: Trasferire movimenti C/G ai movimenti di costi](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="233d4-120">[How to: Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="233d4-121">[Criteri per trasferire movimenti C/G ai movimenti di costi](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="233d4-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="233d4-122">[Risultati del trasferimento](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="233d4-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="233d4-123">Trasferimento e registrazione di movimenti di costi</span><span class="sxs-lookup"><span data-stu-id="233d4-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="233d4-124">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="233d4-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

