---
title: Come aggiornare i costi standard | Microsoft Docs
description: Periodicamente è necessario aggiornare i costi standard dei componenti ed eseguire il rollup dei nuovi costi nell'articolo padre.
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
ms.openlocfilehash: c1f8f0bf70a72944d216f2b948224cd9f706bdff
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238810"
---
# <a name="update-standard-costs"></a><span data-ttu-id="13b17-103">Aggiornare i costi standard</span><span class="sxs-lookup"><span data-stu-id="13b17-103">Update Standard Costs</span></span>
<span data-ttu-id="13b17-104">Periodicamente è necessario aggiornare i costi standard dei componenti ed eseguire il rollup dei nuovi costi nell'articolo padre.</span><span class="sxs-lookup"><span data-stu-id="13b17-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="13b17-105">Il processo in genere è costituito dai quattro passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="13b17-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="13b17-106">Aggiornare i costi ai livelli di capacità e componente.</span><span class="sxs-lookup"><span data-stu-id="13b17-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="13b17-107">Per ulteriori informazioni, vedere il processo batch **Suggerisci costo std. articolo**.</span><span class="sxs-lookup"><span data-stu-id="13b17-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="13b17-108">Consolidamento e roll up dei costi dei componenti e della capacità per calcolare il costo totale di produzione o di assemblaggio degli articoli.</span><span class="sxs-lookup"><span data-stu-id="13b17-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="13b17-109">Implementare i costi standard che vengono registrati quando si eseguono i processi batch precedenti.</span><span class="sxs-lookup"><span data-stu-id="13b17-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="13b17-110">I costi standard non saranno effettivi finché non verranno implementati.</span><span class="sxs-lookup"><span data-stu-id="13b17-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="13b17-111">Per ulteriori informazioni, vedere Implementare modifiche costo std..</span><span class="sxs-lookup"><span data-stu-id="13b17-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="13b17-112">Implementare le modifiche per aggiornare il campo **Costo unitario** nella scheda articolo ed eseguire la rivalutazione di magazzino.</span><span class="sxs-lookup"><span data-stu-id="13b17-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="13b17-113">Per ulteriori informazioni, vedere [Rivalutare il magazzino](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="13b17-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="13b17-114">Per ulteriori informazioni, vedere [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="13b17-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="13b17-115">Per aggiornare i costi standard</span><span class="sxs-lookup"><span data-stu-id="13b17-115">To update standard costs</span></span>  
1.  <span data-ttu-id="13b17-116">Eseguire il processo batch **Rettifica costo - Movimenti articoli**.</span><span class="sxs-lookup"><span data-stu-id="13b17-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="13b17-117">Eseguire il processo batch **Registra costo magazzino in C/G**.</span><span class="sxs-lookup"><span data-stu-id="13b17-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="13b17-118">Aprire il **Prospetto costo standard** e utilizzare una o più delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="13b17-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="13b17-119">Eseguire il processo batch **Suggerisci costo std. articolo**.</span><span class="sxs-lookup"><span data-stu-id="13b17-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="13b17-120">Analizzare i risultati e apportare le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="13b17-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="13b17-121">Eseguire il processo batch **Suggerisci costo standard capacità**.</span><span class="sxs-lookup"><span data-stu-id="13b17-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="13b17-122">Analizzare i risultati e apportare le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="13b17-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="13b17-123">Eseguire il processo batch **Roll up del costo standard**.</span><span class="sxs-lookup"><span data-stu-id="13b17-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="13b17-124">Analizzare i risultati e apportare le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="13b17-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="13b17-125">Eseguire il processo batch **Implementa modifiche costo std.**</span><span class="sxs-lookup"><span data-stu-id="13b17-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="13b17-126">Analizzare e contabilizzare la pagina **Registrazioni rivalutazioni**, in cui sono stati inseriti i dati ricavati tramite i passaggi precedenti del processo.</span><span class="sxs-lookup"><span data-stu-id="13b17-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="13b17-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13b17-127">See Also</span></span>  
 <span data-ttu-id="13b17-128">[Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="13b17-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="13b17-129">[Gestione dei costi di magazzino](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="13b17-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="13b17-130">[Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md) [Contabilità](finance.md)</span><span class="sxs-lookup"><span data-stu-id="13b17-130">[Design Details: Costing Methods](design-details-costing-methods.md) [Finance](finance.md)</span></span>  
 <span data-ttu-id="13b17-131">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13b17-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
