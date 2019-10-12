---
title: Come bloccare gli articoli per la vendita o l'acquisto
description: In Business Central, un articolo può essere contrassegnato come bloccato per la vendita, per l'acquisto o per tutti gli scopi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 87cfa1830e461eac2a03a10e917712dba56eaf98
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308622"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="03eea-103">Bloccare gli articoli per la vendita o l'acquisto</span><span class="sxs-lookup"><span data-stu-id="03eea-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="03eea-104">È possibile bloccare un articolo in modo che non venga immesso in righe di acquisto o di vendita ed è possibile bloccarlo in modo che non venga registrato in una qualsiasi transazione.</span><span class="sxs-lookup"><span data-stu-id="03eea-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="03eea-105">Nella tabella seguente vengono descritti diversi scenari che si verificano quando gli articoli sono bloccati.</span><span class="sxs-lookup"><span data-stu-id="03eea-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="03eea-106">Opzione</span><span class="sxs-lookup"><span data-stu-id="03eea-106">Option</span></span>|<span data-ttu-id="03eea-107">Description</span><span class="sxs-lookup"><span data-stu-id="03eea-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="03eea-108">**Vendita bloccata**</span><span class="sxs-lookup"><span data-stu-id="03eea-108">**Sales Blocked**</span></span>|<span data-ttu-id="03eea-109">Non è possibile immettere l'articolo in un documento di vendita né nel giornale di registrazione articoli di vendita.</span><span class="sxs-lookup"><span data-stu-id="03eea-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="03eea-110">**Acquisto bloccato**</span><span class="sxs-lookup"><span data-stu-id="03eea-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="03eea-111">Non è possibile immettere l'articolo in un documento di acquisto, in un giornale di registrazione articoli di acquisto o nei processi di pianificazione degli acquisti.</span><span class="sxs-lookup"><span data-stu-id="03eea-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="03eea-112">**Bloccato**</span><span class="sxs-lookup"><span data-stu-id="03eea-112">**Blocked**</span></span>|<span data-ttu-id="03eea-113">Non è possibile usare l'articolo per alcuna transazione articolo.</span><span class="sxs-lookup"><span data-stu-id="03eea-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="03eea-114">Gli articoli bloccati possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="03eea-114">Blocked items can be returned.</span></span> <span data-ttu-id="03eea-115">Ciò significa che nessuna delle impostazioni descritte precedentemente è applicabile quando l'articolo viene utilizzato negli ordini di reso e nelle note di credito.</span><span class="sxs-lookup"><span data-stu-id="03eea-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="03eea-116">Per bloccare un articolo in modo che non venga immesso in righe di vendita</span><span class="sxs-lookup"><span data-stu-id="03eea-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="03eea-117">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="03eea-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="03eea-118">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Vendita bloccata**.</span><span class="sxs-lookup"><span data-stu-id="03eea-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="03eea-119">Se si tenta di immettere l'articolo in un documento di vendita o in una riga di giornale di registrazione, viene visualizzato un errore indicante che l'articolo è bloccato.</span><span class="sxs-lookup"><span data-stu-id="03eea-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="03eea-120">Per bloccare un articolo in modo che non venga immesso in righe di acquisto</span><span class="sxs-lookup"><span data-stu-id="03eea-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="03eea-121">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="03eea-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="03eea-122">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Acquisto bloccato**.</span><span class="sxs-lookup"><span data-stu-id="03eea-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="03eea-123">Se si tenta di immettere l'articolo in un documento di acquisto o in una riga di giornale di registrazione, viene visualizzato un errore indicante che l'articolo è bloccato.</span><span class="sxs-lookup"><span data-stu-id="03eea-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="03eea-124">Per bloccare un articolo in modo che non venga contabilizzato</span><span class="sxs-lookup"><span data-stu-id="03eea-124">To block an item from being posted</span></span>
1. <span data-ttu-id="03eea-125">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="03eea-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="03eea-126">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Bloccato**.</span><span class="sxs-lookup"><span data-stu-id="03eea-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="03eea-127">Se si tenta di registrare un qualsiasi tipo di transazione per l'articolo, viene visualizzato un messaggio di errore indicante che l'articolo è bloccato.</span><span class="sxs-lookup"><span data-stu-id="03eea-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="03eea-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03eea-128">See Also</span></span>  
[<span data-ttu-id="03eea-129">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="03eea-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="03eea-130">Magazzino</span><span class="sxs-lookup"><span data-stu-id="03eea-130">Inventory</span></span>](inventory-manage-inventory.md)  
