---
title: Come bloccare gli articoli per la vendita o l'acquisto
description: È possibile impedire che un articolo venga utilizzato, ad esempio, nei documenti di vendita o di acquisto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f958600a47daa12a665975d6c41e214fca7cf5ad
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914092"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="5bba2-103">Bloccare gli articoli per la vendita o l'acquisto</span><span class="sxs-lookup"><span data-stu-id="5bba2-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="5bba2-104">È possibile bloccare un articolo in modo che non venga immesso nelle righe dei documenti di acquisto o di vendita ed è possibile bloccarlo in modo che non venga registrato in una qualsiasi transazione.</span><span class="sxs-lookup"><span data-stu-id="5bba2-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="5bba2-105">Ad esempio, questo è utile quando un articolo presenta un difetto noto.</span><span class="sxs-lookup"><span data-stu-id="5bba2-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="5bba2-106">Se qualcuno sceglie un articolo bloccato su un documento di vendita o di acquisto, un messaggio informerà che l'articolo è bloccato.</span><span class="sxs-lookup"><span data-stu-id="5bba2-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="5bba2-107">Nella tabella seguente vengono illustrati diversi scenari che si verificano quando gli articoli sono bloccati.</span><span class="sxs-lookup"><span data-stu-id="5bba2-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="5bba2-108">Opzione</span><span class="sxs-lookup"><span data-stu-id="5bba2-108">Option</span></span>|<span data-ttu-id="5bba2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bba2-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="5bba2-110">**Vendita bloccata**</span><span class="sxs-lookup"><span data-stu-id="5bba2-110">**Sales Blocked**</span></span>|<span data-ttu-id="5bba2-111">Non è possibile immettere l'articolo in un documento di vendita né nel giornale di registrazione articoli di vendita.</span><span class="sxs-lookup"><span data-stu-id="5bba2-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="5bba2-112">**Acquisto bloccato**</span><span class="sxs-lookup"><span data-stu-id="5bba2-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="5bba2-113">Non è possibile immettere l'articolo in un documento di acquisto, in un giornale di registrazione articoli di acquisto o nei processi di pianificazione degli acquisti.</span><span class="sxs-lookup"><span data-stu-id="5bba2-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="5bba2-114">**Bloccato**</span><span class="sxs-lookup"><span data-stu-id="5bba2-114">**Blocked**</span></span>|<span data-ttu-id="5bba2-115">Non è possibile usare l'articolo per alcuna transazione articolo.</span><span class="sxs-lookup"><span data-stu-id="5bba2-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="5bba2-116">Gli articoli bloccati possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="5bba2-116">Blocked items can be returned.</span></span> <span data-ttu-id="5bba2-117">Ciò significa che nessuna delle impostazioni descritte precedentemente è applicabile quando l'articolo viene utilizzato negli ordini di reso e nelle note di credito.</span><span class="sxs-lookup"><span data-stu-id="5bba2-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="5bba2-118">Quando si utilizza la funzione **Copia da documento** per creare nuovi documenti basati su documenti esistenti, si viene avvisati se eventuali elementi nelle righe del documento di origine sono bloccati.</span><span class="sxs-lookup"><span data-stu-id="5bba2-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="5bba2-119">Le righe del documento bloccate sono escluse dal nuovo documento e una notifica mostra una panoramica di tutte le righe del documento che sono bloccate nel documento di origine.</span><span class="sxs-lookup"><span data-stu-id="5bba2-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="5bba2-120">Per bloccare un articolo in modo che non venga immesso in righe di vendita</span><span class="sxs-lookup"><span data-stu-id="5bba2-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="5bba2-121">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="5bba2-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5bba2-122">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Vendita bloccata**.</span><span class="sxs-lookup"><span data-stu-id="5bba2-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="5bba2-123">Per bloccare un articolo in modo che non venga immesso in righe di acquisto</span><span class="sxs-lookup"><span data-stu-id="5bba2-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="5bba2-124">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="5bba2-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5bba2-125">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Acquisto bloccato**.</span><span class="sxs-lookup"><span data-stu-id="5bba2-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="5bba2-126">Per bloccare un articolo in modo che non venga contabilizzato</span><span class="sxs-lookup"><span data-stu-id="5bba2-126">To block an item from being posted</span></span>
1. <span data-ttu-id="5bba2-127">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="5bba2-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5bba2-128">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Bloccato**.</span><span class="sxs-lookup"><span data-stu-id="5bba2-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bba2-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5bba2-129">See Also</span></span>  
[<span data-ttu-id="5bba2-130">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="5bba2-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="5bba2-131">Magazzino</span><span class="sxs-lookup"><span data-stu-id="5bba2-131">Inventory</span></span>](inventory-manage-inventory.md)  
