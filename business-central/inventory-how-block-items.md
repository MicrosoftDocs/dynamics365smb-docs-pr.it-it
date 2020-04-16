---
title: Come bloccare gli articoli per la vendita o l'acquisto
description: In Business Central, un articolo può essere contrassegnato come bloccato per la vendita, per l'acquisto o per tutti gli scopi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182302"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="371be-103">Bloccare gli articoli per la vendita o l'acquisto</span><span class="sxs-lookup"><span data-stu-id="371be-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="371be-104">È possibile bloccare un articolo in modo che non venga immesso in righe di acquisto o di vendita ed è possibile bloccarlo in modo che non venga registrato in una qualsiasi transazione.</span><span class="sxs-lookup"><span data-stu-id="371be-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="371be-105">Nella tabella seguente vengono descritti diversi scenari che si verificano quando gli articoli sono bloccati.</span><span class="sxs-lookup"><span data-stu-id="371be-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="371be-106">Opzione</span><span class="sxs-lookup"><span data-stu-id="371be-106">Option</span></span>|<span data-ttu-id="371be-107">Description</span><span class="sxs-lookup"><span data-stu-id="371be-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="371be-108">**Vendita bloccata**</span><span class="sxs-lookup"><span data-stu-id="371be-108">**Sales Blocked**</span></span>|<span data-ttu-id="371be-109">Non è possibile immettere l'articolo in un documento di vendita né nel giornale di registrazione articoli di vendita.</span><span class="sxs-lookup"><span data-stu-id="371be-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="371be-110">**Acquisto bloccato**</span><span class="sxs-lookup"><span data-stu-id="371be-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="371be-111">Non è possibile immettere l'articolo in un documento di acquisto, in un giornale di registrazione articoli di acquisto o nei processi di pianificazione degli acquisti.</span><span class="sxs-lookup"><span data-stu-id="371be-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="371be-112">**Bloccato**</span><span class="sxs-lookup"><span data-stu-id="371be-112">**Blocked**</span></span>|<span data-ttu-id="371be-113">Non è possibile usare l'articolo per alcuna transazione articolo.</span><span class="sxs-lookup"><span data-stu-id="371be-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="371be-114">Gli articoli bloccati possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="371be-114">Blocked items can be returned.</span></span> <span data-ttu-id="371be-115">Ciò significa che nessuna delle impostazioni descritte precedentemente è applicabile quando l'articolo viene utilizzato negli ordini di reso e nelle note di credito.</span><span class="sxs-lookup"><span data-stu-id="371be-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="371be-116">Quando si utilizza la funzione **Copia da documento** per creare nuovi documenti basati su documenti esistenti, si viene avvisati se eventuali elementi nelle righe del documento di origine sono bloccati.</span><span class="sxs-lookup"><span data-stu-id="371be-116">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="371be-117">Le righe del documento bloccate sono escluse dal nuovo documento e una notifica mostra una panoramica di tutte le righe del documento che sono bloccate nel documento di origine.</span><span class="sxs-lookup"><span data-stu-id="371be-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="371be-118">Per bloccare un articolo in modo che non venga immesso in righe di vendita</span><span class="sxs-lookup"><span data-stu-id="371be-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="371be-119">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="371be-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="371be-120">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Vendita bloccata**.</span><span class="sxs-lookup"><span data-stu-id="371be-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="371be-121">Se si tenta di immettere l'articolo in un documento di vendita o in una riga di giornale di registrazione, viene visualizzato un errore indicante che l'articolo è bloccato.</span><span class="sxs-lookup"><span data-stu-id="371be-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="371be-122">Per bloccare un articolo in modo che non venga immesso in righe di acquisto</span><span class="sxs-lookup"><span data-stu-id="371be-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="371be-123">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="371be-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="371be-124">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Acquisto bloccato**.</span><span class="sxs-lookup"><span data-stu-id="371be-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="371be-125">Se si tenta di immettere l'articolo in un documento di acquisto o in una riga di giornale di registrazione, viene visualizzato un errore indicante che l'articolo è bloccato.</span><span class="sxs-lookup"><span data-stu-id="371be-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="371be-126">Per bloccare un articolo in modo che non venga contabilizzato</span><span class="sxs-lookup"><span data-stu-id="371be-126">To block an item from being posted</span></span>
1. <span data-ttu-id="371be-127">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="371be-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="371be-128">Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Bloccato**.</span><span class="sxs-lookup"><span data-stu-id="371be-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="371be-129">Se si tenta di registrare un qualsiasi tipo di transazione per l'articolo, viene visualizzato un messaggio di errore indicante che l'articolo è bloccato.</span><span class="sxs-lookup"><span data-stu-id="371be-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="371be-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="371be-130">See Also</span></span>  
[<span data-ttu-id="371be-131">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="371be-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="371be-132">Magazzino</span><span class="sxs-lookup"><span data-stu-id="371be-132">Inventory</span></span>](inventory-manage-inventory.md)  
