---
title: Come creare le testate degli ordini di produzione | Microsoft Docs
description: Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 76d4b69de41343815175a7acd4329bb47b889f5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759369"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="c96e9-103">Creare le testate degli ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="c96e9-103">Create Production Order Headers</span></span>
<span data-ttu-id="c96e9-104">Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="c96e9-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="c96e9-105">Gli ordini di produzione vengono in genere creati automaticamente da una funzione di pianificazione per soddisfare una domanda conosciuta.</span><span class="sxs-lookup"><span data-stu-id="c96e9-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="c96e9-106">Per ulteriori informazioni, vedere [Pianificazione](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="c96e9-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="c96e9-107">Nella seguente procedura viene creato un ordine produzione confermato.</span><span class="sxs-lookup"><span data-stu-id="c96e9-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="c96e9-108">È anche possibile creare ordini di produzione con uno stato differente.</span><span class="sxs-lookup"><span data-stu-id="c96e9-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="c96e9-109">Per creare una testata degli ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="c96e9-109">To create a production order header</span></span>  
1.  <span data-ttu-id="c96e9-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ord. produzione confermati** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c96e9-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c96e9-111">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="c96e9-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="c96e9-112">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c96e9-112">In the **No.**</span></span> <span data-ttu-id="c96e9-113">inserire il numero di serie successivo.</span><span class="sxs-lookup"><span data-stu-id="c96e9-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="c96e9-114">Selezionare nel campo **Tipo Origine** l'origine dell'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="c96e9-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="c96e9-115">Qui è possibile selezionare la famiglia di articoli.</span><span class="sxs-lookup"><span data-stu-id="c96e9-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="c96e9-116">Per ulteriori informazioni, vedere [Utilizzare famiglie di prodotti](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="c96e9-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="c96e9-117">Nel campo **Nr. origine** selezionare il numero dell'articolo, della famiglia o della testata di vendita per il quale deve essere generato l'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="c96e9-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="c96e9-118">Compilare i campi **Quantità** e **Data Scadenza** con i dati desiderati.</span><span class="sxs-lookup"><span data-stu-id="c96e9-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="c96e9-119">Quando i requisiti di produzione cambiano, ad esempio componenti o operazioni, è possibile ripianificare rapidamente l'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="c96e9-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="c96e9-120">Per ulteriori informazioni, vedere [Ripianificare o aggiornare direttamente gli ordini di produzione](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c96e9-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="c96e9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c96e9-121">See Also</span></span>  
<span data-ttu-id="c96e9-122">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="c96e9-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="c96e9-123">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="c96e9-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="c96e9-124">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="c96e9-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="c96e9-125">Magazzino</span><span class="sxs-lookup"><span data-stu-id="c96e9-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c96e9-126">Acquisti</span><span class="sxs-lookup"><span data-stu-id="c96e9-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c96e9-127">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c96e9-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
