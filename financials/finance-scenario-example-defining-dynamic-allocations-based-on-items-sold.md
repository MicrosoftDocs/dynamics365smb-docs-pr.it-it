---
title: Esempio di scenario - Definizione delle allocazioni dinamiche in base agli articoli venduti | Documenti Microsoft
description: In questo argomento viene visualizzato un esempio su come definire le allocazioni utilizzando il metodo di allocazione dinamica.
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
ms.openlocfilehash: d8622d11cd23e506d1b85b18dbe5facb740c7753
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="48d69-103">Esempio dello scenario: definizione delle allocazioni dinamiche in base agli articoli venduti</span><span class="sxs-lookup"><span data-stu-id="48d69-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="48d69-104">In questo argomento viene visualizzato un esempio su come definire le allocazioni utilizzando il metodo di allocazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="48d69-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="48d69-105">Nell'esempio è possibile modificare l'assegnazione dinamica dei costi per il centro di costo VENDITE per supportare il nuovo oggetto di costo ATTREZZATURA IT.</span><span class="sxs-lookup"><span data-stu-id="48d69-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="48d69-106">I numeri degli articoli dei colli di ATTREZZATURA IT sono inclusi nell'intervallo compreso tra 8904-W e 8924-W.</span><span class="sxs-lookup"><span data-stu-id="48d69-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="48d69-107">Utilizzare le cifre di vendita dell'anno precedente per calcolare la quota.</span><span class="sxs-lookup"><span data-stu-id="48d69-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="48d69-108">L'allocazione viene registrata nel tipo di costo di supporto 9903.</span><span class="sxs-lookup"><span data-stu-id="48d69-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="48d69-109">Nell'esempio vengono utilizzati i dati di esempio di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="48d69-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="48d69-110">Per definire le allocazioni dinamiche in base agli articoli venduti nell'anno precedente</span><span class="sxs-lookup"><span data-stu-id="48d69-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="48d69-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Allocazioni costi**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="48d69-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48d69-112">Nella finestra **Allocazione costi** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="48d69-112">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="48d69-113">Nel campo **ID** premere INVIO o immettere un ID.</span><span class="sxs-lookup"><span data-stu-id="48d69-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="48d69-114">Nel campo **Livello** immettere **1**.</span><span class="sxs-lookup"><span data-stu-id="48d69-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="48d69-115">Nei campi **Data di inizio validità** e **Data di fine validità**, immettere le date appropriate.</span><span class="sxs-lookup"><span data-stu-id="48d69-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="48d69-116">Nel campo **Codice centro di costo** immettere **VENDITE**.</span><span class="sxs-lookup"><span data-stu-id="48d69-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="48d69-117">Nel campo **Importo dare in tipo di costo** immettere il tipo di costo **9903**.</span><span class="sxs-lookup"><span data-stu-id="48d69-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="48d69-118">Nel campo **Tipo di costo di destinazione** immettere il tipo di costo **9903**.</span><span class="sxs-lookup"><span data-stu-id="48d69-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="48d69-119">Nel campo **Oggetto di costo di destinazione** selezionare **Nuovo** per creare un nuovo oggetto di costo ATTREZZATURA IT e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="48d69-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="48d69-120">Selezionare **ATTREZZATURA IT**.</span><span class="sxs-lookup"><span data-stu-id="48d69-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="48d69-121">Lasciare vuoto il campo **Centro di costo di destinazione**.</span><span class="sxs-lookup"><span data-stu-id="48d69-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="48d69-122">Nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi accumulati.</span><span class="sxs-lookup"><span data-stu-id="48d69-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="48d69-123">Nel campo **Base** selezionare la base di allocazione **Articoli venduti (importo)**.</span><span class="sxs-lookup"><span data-stu-id="48d69-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="48d69-124">Nel campo **Filtro nr.** immettere **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="48d69-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="48d69-125">Nel campo **Codice filtro data**, immettere **Anno Precedente**.</span><span class="sxs-lookup"><span data-stu-id="48d69-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="48d69-126">Per calcolare la quota, scegliere l'azione **Calcola chiave di allocazione**.</span><span class="sxs-lookup"><span data-stu-id="48d69-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="48d69-127">In [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono utilizzate le cifre di vendita degli anni precedenti per calcolare una quota di 1.596,50 VL con il 100% dei colli di ATTREZZATURA IT.</span><span class="sxs-lookup"><span data-stu-id="48d69-127">[!INCLUDE[d365fin](includes/d365fin_md.md)] uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="48d69-128">Pertanto, tutti gli articoli venduti nell'ultimo anno verranno assegnati all'oggetto di costo ATTREZZATURA IT.</span><span class="sxs-lookup"><span data-stu-id="48d69-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="48d69-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48d69-129">See Also</span></span>  
 <span data-ttu-id="48d69-130">[Impostazione di filtri per le basi di allocazione dinamica](finance-setting-filters-for-dynamic-allocation-bases.md) </span><span class="sxs-lookup"><span data-stu-id="48d69-130">[Setting Filters for Dynamic Allocation Bases](finance-setting-filters-for-dynamic-allocation-bases.md) </span></span>  
 <span data-ttu-id="48d69-131">[Impostare origini e destinazioni dell'allocazione](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="48d69-131">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
 <span data-ttu-id="48d69-132">[Definizione e allocazione dei costi](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="48d69-132">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
 <span data-ttu-id="48d69-133">[Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="48d69-133">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="48d69-134">Informazioni sulla contabilità industriale</span><span class="sxs-lookup"><span data-stu-id="48d69-134">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

