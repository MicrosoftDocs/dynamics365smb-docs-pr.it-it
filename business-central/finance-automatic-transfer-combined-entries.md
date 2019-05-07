---
title: Trasferimento automatico e movimenti combinati | Microsoft Docs
description: Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata. È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo. Nella seguente tabella vengono illustrate le diverse opzioni.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "941156"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="90e36-105">Trasferimento automatico e movimenti combinati</span><span class="sxs-lookup"><span data-stu-id="90e36-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="90e36-106">Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata.</span><span class="sxs-lookup"><span data-stu-id="90e36-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="90e36-107">È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo.</span><span class="sxs-lookup"><span data-stu-id="90e36-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="90e36-108">Nella seguente tabella vengono illustrate le diverse opzioni.</span><span class="sxs-lookup"><span data-stu-id="90e36-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="90e36-109">Cumula movimenti</span><span class="sxs-lookup"><span data-stu-id="90e36-109">Combine entries</span></span>|<span data-ttu-id="90e36-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90e36-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="90e36-111">Nessuno</span><span class="sxs-lookup"><span data-stu-id="90e36-111">None</span></span>|<span data-ttu-id="90e36-112">Ogni movimento C/G viene trasferito singolarmente al tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="90e36-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="90e36-113">Giorno</span><span class="sxs-lookup"><span data-stu-id="90e36-113">Day</span></span>|<span data-ttu-id="90e36-114">I movimenti C/G con la stessa data di registrazione vengono trasferiti come un unico movimento nel tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="90e36-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="90e36-115">Mese</span><span class="sxs-lookup"><span data-stu-id="90e36-115">Month</span></span>|<span data-ttu-id="90e36-116">Tutti i movimenti C/G dello stesso mese di calendario vengono trasferiti come un unico movimento nel tipo di costo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="90e36-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="90e36-117">Se si è selezionata la casella di controllo **Trasferimento automatico da CG** nella pagina **Setup contabilità industriale**, [!INCLUDE[d365fin](includes/d365fin_md.md)] aggiorna la contabilità dopo ogni registrazione nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="90e36-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="90e36-118">Le entità combinate non sono possibili.</span><span class="sxs-lookup"><span data-stu-id="90e36-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="90e36-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90e36-119">See Also</span></span>  
 <span data-ttu-id="90e36-120">[Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="90e36-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="90e36-121">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90e36-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
