---
title: Come creare le testate degli ordini di produzione | Microsoft Docs
description: Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione.
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
ms.openlocfilehash: 70a6f2e583e5ba78eecae0a25d6533d8265414ca
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "913631"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="ec559-103">Creare le testate degli ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="ec559-103">Create Production Order Headers</span></span>
<span data-ttu-id="ec559-104">Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="ec559-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="ec559-105">Gli ordini di produzione vengono in genere creati automaticamente da una funzione di pianificazione per soddisfare una domanda conosciuta.</span><span class="sxs-lookup"><span data-stu-id="ec559-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="ec559-106">Per ulteriori informazioni, vedere [Pianificazione](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="ec559-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="ec559-107">Nella seguente procedura viene creato un ordine produzione confermato.</span><span class="sxs-lookup"><span data-stu-id="ec559-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="ec559-108">È anche possibile creare ordini di produzione con uno stato differente.</span><span class="sxs-lookup"><span data-stu-id="ec559-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="ec559-109">Per creare una testata degli ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="ec559-109">To create a production order header</span></span>  
1.  <span data-ttu-id="ec559-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ord. produzione confermati** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ec559-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ec559-111">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="ec559-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="ec559-112">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="ec559-112">In the **No.**</span></span> <span data-ttu-id="ec559-113">inserire il numero di serie successivo.</span><span class="sxs-lookup"><span data-stu-id="ec559-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="ec559-114">Selezionare nel campo **Tipo Origine** l'origine dell'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="ec559-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="ec559-115">Qui è possibile selezionare la famiglia di articoli.</span><span class="sxs-lookup"><span data-stu-id="ec559-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="ec559-116">Per ulteriori informazioni, vedere [Utilizzare famiglie di prodotti](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="ec559-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="ec559-117">Nel campo **Nr. origine** selezionare il numero dell'articolo, della famiglia o della testata di vendita per il quale deve essere generato l'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="ec559-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="ec559-118">Compilare i campi **Quantità** e **Data Scadenza** con i dati desiderati.</span><span class="sxs-lookup"><span data-stu-id="ec559-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="ec559-119">Quando i requisiti di produzione cambiano, ad esempio componenti o operazioni, è possibile ripianificare rapidamente l'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="ec559-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="ec559-120">Per ulteriori informazioni, vedere [Ripianificare o aggiornare direttamente gli ordini di produzione](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="ec559-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="ec559-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec559-121">See Also</span></span>  
<span data-ttu-id="ec559-122">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ec559-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="ec559-123">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="ec559-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ec559-124">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="ec559-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="ec559-125">Magazzino</span><span class="sxs-lookup"><span data-stu-id="ec559-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ec559-126">Acquisti</span><span class="sxs-lookup"><span data-stu-id="ec559-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ec559-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ec559-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
