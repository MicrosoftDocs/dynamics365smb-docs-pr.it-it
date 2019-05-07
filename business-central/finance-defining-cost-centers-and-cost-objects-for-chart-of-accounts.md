---
title: Definizione dei centri di costo e degli oggetti di costo per il piano dei conti | Microsoft Docs
description: È possibile trasferire automaticamente i movimenti delle entrate e delle spese della contabilità generale alla contabilità industriale per ogni registrazione di contabilità generale o tramite un processo batch. Durante il trasferimento, il sistema trasferisce solo i movimenti che sono già stati collegati a un centro di costo o a un oggetto di costo. Per stabilire un trasferimento significativo, è necessario assicurarsi che i centri di costo e gli oggetti di costi siano correttamente definiti.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "923324"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="81296-105">Definizione dei centri di costo e degli oggetti di costo per il piano dei conti</span><span class="sxs-lookup"><span data-stu-id="81296-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="81296-106">È possibile trasferire automaticamente i movimenti delle entrate e delle spese della contabilità generale alla contabilità industriale per ogni registrazione di contabilità generale o tramite un processo batch.</span><span class="sxs-lookup"><span data-stu-id="81296-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="81296-107">Durante il trasferimento, con [!INCLUDE[d365fin](includes/d365fin_md.md)] è possibile trasferire solo i movimenti che sono già stati collegati a un centro di costo o a un oggetto di costo.</span><span class="sxs-lookup"><span data-stu-id="81296-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="81296-108">Per stabilire un trasferimento significativo, è necessario assicurarsi che i centri di costo e gli oggetti di costi siano correttamente definiti.</span><span class="sxs-lookup"><span data-stu-id="81296-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="81296-109">Definizione dei valori dimensioni di default per i conti di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="81296-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="81296-110">Per ogni conto di contabilità generale, è possibile definire i valori dimensioni di default nella tabella **Dimensione di default**.</span><span class="sxs-lookup"><span data-stu-id="81296-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="81296-111">Nell'esempio seguente viene illustrato come sia sempre necessaria la presenza di un centro di costo REPARTO e mai quella di un oggetto di costo PROGETTO quando si effettua una registrazione in un conto di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="81296-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="81296-112">**Codice dimensione**</span><span class="sxs-lookup"><span data-stu-id="81296-112">**Dimension Code**</span></span>|<span data-ttu-id="81296-113">**Registrazione valore**</span><span class="sxs-lookup"><span data-stu-id="81296-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="81296-114">Reparto</span><span class="sxs-lookup"><span data-stu-id="81296-114">Department</span></span>|<span data-ttu-id="81296-115">Codice obbligatorio</span><span class="sxs-lookup"><span data-stu-id="81296-115">Code Mandatory</span></span>|  
|<span data-ttu-id="81296-116">Progetto</span><span class="sxs-lookup"><span data-stu-id="81296-116">Project</span></span>|<span data-ttu-id="81296-117">Nessun Cod.</span><span class="sxs-lookup"><span data-stu-id="81296-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="81296-118">Definizione dei valori dimensioni per i costi generali e diretti</span><span class="sxs-lookup"><span data-stu-id="81296-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="81296-119">È possibile trasferire i costi generali a un centro di costo e i costi diretti a un oggetto di costo.</span><span class="sxs-lookup"><span data-stu-id="81296-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="81296-120">Nella tabella seguente viene mostrata la combinazione ottimale dei valori di impostazione delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="81296-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="81296-121">Trasferisci a</span><span class="sxs-lookup"><span data-stu-id="81296-121">Transfer To</span></span>|<span data-ttu-id="81296-122">Registrazione del centro di costo</span><span class="sxs-lookup"><span data-stu-id="81296-122">Cost Center Posting</span></span>|<span data-ttu-id="81296-123">Registrazione dell'oggetto di costo</span><span class="sxs-lookup"><span data-stu-id="81296-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="81296-124">Centro di costo</span><span class="sxs-lookup"><span data-stu-id="81296-124">Cost Center</span></span>|<span data-ttu-id="81296-125">Codice obbligatorio</span><span class="sxs-lookup"><span data-stu-id="81296-125">Code Mandatory</span></span>|<span data-ttu-id="81296-126">Nessun Cod.</span><span class="sxs-lookup"><span data-stu-id="81296-126">No Code</span></span>|  
|<span data-ttu-id="81296-127">Oggetto di costo</span><span class="sxs-lookup"><span data-stu-id="81296-127">Cost Object</span></span>|<span data-ttu-id="81296-128">Nessun Cod.</span><span class="sxs-lookup"><span data-stu-id="81296-128">No Code</span></span>|<span data-ttu-id="81296-129">Codice obbligatorio</span><span class="sxs-lookup"><span data-stu-id="81296-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="81296-130">Per garantire che il centro di costo e l'oggetto di costo predefiniti impostati nella contabilità generale vengano riportati automaticamente nella contabilità industriale, selezionare la casella di controllo **Verifica registrazioni CG** nella pagina Setup contabilità industriale.</span><span class="sxs-lookup"><span data-stu-id="81296-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="81296-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81296-131">See Also</span></span>  
[<span data-ttu-id="81296-132">Contabilizzazione dei costi</span><span class="sxs-lookup"><span data-stu-id="81296-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="81296-133">Impostazione della contabilità industriale</span><span class="sxs-lookup"><span data-stu-id="81296-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="81296-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81296-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
