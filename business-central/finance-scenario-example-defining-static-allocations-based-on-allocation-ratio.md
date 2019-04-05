---
title: Definizione della allocazioni statiche in base al rapporto di allocazione | Microsoft Docs
description: Il metodo di allocazione statica è basato su un valore definito, ad esempio i metri quadri utilizzati, o su un rapporto di allocazione stabilito, quale 5:2:4.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: d35fd5de7a0583c3864268d0749384322bf947ed
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802223"
---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="a9c30-103">Esempio dello scenario: definizione della allocazioni statiche in base al rapporto di allocazione</span><span class="sxs-lookup"><span data-stu-id="a9c30-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="a9c30-104">Il metodo di allocazione statica è basato su un valore definito, ad esempio i metri quadri utilizzati, o su un rapporto di allocazione stabilito, quale 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="a9c30-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="a9c30-105">In questo argomento viene descritto come definire i tre nuovi oggetti di costo di destinazione di allocazione per il centro di costo PROD di origine di allocazione utilizzando il rapporto di allocazione stabilito 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="a9c30-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="a9c30-106">I tre oggetti di costo di destinazione sono ACCESSORI, VERNICE e ARREDI.</span><span class="sxs-lookup"><span data-stu-id="a9c30-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a9c30-107">Nell'esempio vengono utilizzati i dati di esempio di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a9c30-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="a9c30-108">Per definire il centro di costo PROD di origine di allocazione nella Scheda dettaglio Generale</span><span class="sxs-lookup"><span data-stu-id="a9c30-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="a9c30-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Allocazione costi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="a9c30-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a9c30-110">Nella pagina **Allocazione costi** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-110">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="a9c30-111">Nel campo **ID** premere INVIO o immettere un ID.</span><span class="sxs-lookup"><span data-stu-id="a9c30-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="a9c30-112">Nel campo **Livello** immettere **1**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="a9c30-113">Nei campi **Data di inizio validità** e **Data di fine validità**, immettere le date appropriate.</span><span class="sxs-lookup"><span data-stu-id="a9c30-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="a9c30-114">Nel campo **Codice centro di costo** immettere **PROD**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="a9c30-115">Nel campo **Importo dare in tipo di costo** immettere il tipo di costo **9903**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="a9c30-116">Per definire gli oggetti di costo di destinazione di allocazione nella Scheda dettaglio Righe</span><span class="sxs-lookup"><span data-stu-id="a9c30-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="a9c30-117">Nel campo **Tipo di costo di destinazione** della prima riga immettere **9903**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="a9c30-118">Nel campo **Oggetto di costo di destinazione** della prima riga selezionare **ACCESSO**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="a9c30-119">Nella prima riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.</span><span class="sxs-lookup"><span data-stu-id="a9c30-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="a9c30-120">Nella prima riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.</span><span class="sxs-lookup"><span data-stu-id="a9c30-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="a9c30-121">Nella prima riga nel campo **Quota** immettere il rapporto di allocazione **5**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="a9c30-122">Nel campo **Tipo di costo di destinazione** della seconda riga immettere **9903**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="a9c30-123">Nel campo **Oggetto di costo di destinazione** della seconda riga selezionare **VERNICE**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="a9c30-124">Nella seconda riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.</span><span class="sxs-lookup"><span data-stu-id="a9c30-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="a9c30-125">Nella seconda riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.</span><span class="sxs-lookup"><span data-stu-id="a9c30-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="a9c30-126">Nella seconda riga nel campo **Quota** immettere il rapporto di allocazione **2**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="a9c30-127">Nel campo **Tipo di costo di destinazione** della terza riga immettere **9903**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="a9c30-128">Nel campo **Oggetto di costo di destinazione** della terza riga selezionare **ARREDI**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="a9c30-129">Nella terza riga nel campo **Tipo di destinazione allocazione** selezionare **Tutti i costi** per definire la modalità di allocazione di tutti i costi sospesi.</span><span class="sxs-lookup"><span data-stu-id="a9c30-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="a9c30-130">Nella terza riga nel campo **Base** selezionare **Statica** per utilizzare il metodo di allocazione statica.</span><span class="sxs-lookup"><span data-stu-id="a9c30-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="a9c30-131">Nella terza riga nel campo **Quota** immettere il rapporto di allocazione **4**.</span><span class="sxs-lookup"><span data-stu-id="a9c30-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="a9c30-132">In [!INCLUDE[d365fin](includes/d365fin_md.md)] il campo **Percentuale** viene calcolato automaticamente utilizzando un tasso percentuale che dipende da tutti e tre i rapporti di allocazione immessi nel campo **Quota**  per tutte e tre le righe.</span><span class="sxs-lookup"><span data-stu-id="a9c30-132">[!INCLUDE[d365fin](includes/d365fin_md.md)] automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a9c30-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9c30-133">See Also</span></span>  
[<span data-ttu-id="a9c30-134">Definizione e allocazione dei costi</span><span class="sxs-lookup"><span data-stu-id="a9c30-134">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)   
