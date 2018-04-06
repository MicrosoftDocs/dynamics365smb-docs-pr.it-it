---
title: Come fare un'offerta per una vendita assemblaggio su ordine | Microsoft Docs
description: "È possibile utilizzare gestione assemblaggio per personalizzare un articolo di assemblaggio nella richiesta di un cliente durante il processo di vendita."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 402745a9c90d1b82779e436f4a6533d2aed1b344
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="8f098-103">Offerta per una vendita assemblaggio su ordine</span><span class="sxs-lookup"><span data-stu-id="8f098-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="8f098-104">È possibile utilizzare gestione assemblaggio per personalizzare un articolo di assemblaggio nella richiesta di un cliente durante il processo di vendita.</span><span class="sxs-lookup"><span data-stu-id="8f098-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="8f098-105">Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="8f098-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="8f098-106">Come per la vendita di qualsiasi altro tipo di articolo, è inoltre possibile creare un'offerta di vendita di un articolo di assemblaggio personalizzato prima della conversione in ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="8f098-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="8f098-107">Questo processo prevede diversi passaggi aggiuntivi se viene confrontato alla creazione di un'offerta di vendita normale e utilizza una variazione di un ordine di assemblaggio collegato, ossia un'offerta di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="8f098-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="8f098-108">Come in tutti i tipi di offerte, le quantità nelle offerte di assemblaggio non vengono utilizzate per la disponibilità, la pianificazione o gli impegni.</span><span class="sxs-lookup"><span data-stu-id="8f098-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="8f098-109">Per creare un'offerta di vendita per un articolo assemblato su ordine</span><span class="sxs-lookup"><span data-stu-id="8f098-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="8f098-110">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Offerte di vendita**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="8f098-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8f098-111">Creare una riga dell'offerta di vendita con una riga per un articolo di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="8f098-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="8f098-112">Per ulteriori informazioni, vedere  [Fare offerte](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="8f098-112">For more information, see [Make Offers](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="8f098-113">Nel campo **Qtà per assemblaggio su ordine** immettere la quantità completa.</span><span class="sxs-lookup"><span data-stu-id="8f098-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="8f098-114">Non si crea un'offerta per una quantità parziale.</span><span class="sxs-lookup"><span data-stu-id="8f098-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="8f098-115">Di conseguenza, è necessario immettere la stessa quantità immessa nel campo **Quantità** della riga dell'offerta di vendita.</span><span class="sxs-lookup"><span data-stu-id="8f098-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="8f098-116">Nella Scheda dettaglio **Righe** scegliere **Riga**, **Assemblaggio su ordine**, quindi **Righe di assemblaggio su ordine**.</span><span class="sxs-lookup"><span data-stu-id="8f098-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="8f098-117">In alternativa, scegliere il campo **Qtà per assemblaggio su ordine** della riga.</span><span class="sxs-lookup"><span data-stu-id="8f098-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="8f098-118">Nella finestra **Righe di assemblaggio su ordine** esaminare o modificare le righe dell'ordine di assemblaggio in base all'offerta richiesta dal cliente.</span><span class="sxs-lookup"><span data-stu-id="8f098-118">In the **Assemble-to-Order Lines** window, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="8f098-119">Se si desidera visualizzare altre informazioni, scegliere l'azione **Mostra documento** per aprire l'ordine dell'offerta programmata completo.</span><span class="sxs-lookup"><span data-stu-id="8f098-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="8f098-120">Non è possibile modificare il contenuto della maggior parte dei campi né effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="8f098-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="8f098-121">Dopo avere rettificato le righe dell'ordine di assemblaggio in base all'offerta, chiudere la finestra **Righe di assemblaggio su ordine** per tornare alla finestra **Offerta vendita**.</span><span class="sxs-lookup"><span data-stu-id="8f098-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** window to return to the **Sales Quote** window.</span></span>  
7.  <span data-ttu-id="8f098-122">Se il cliente accetta l'offerta, creare un ordine di vendita per l'articolo di assemblaggio offerto.</span><span class="sxs-lookup"><span data-stu-id="8f098-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="8f098-123">Per ulteriori informazioni, vedere  [Fare offerte](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="8f098-123">For more information, see [Make Offers](sales-how-make-offers.md).</span></span> <span data-ttu-id="8f098-124">L'offerta di assemblaggio collegata ed eventuali personalizzazioni sono collegate al nuovo ordine di vendita per preparare l'assemblaggio dell'articolo o degli articoli da vendere.</span><span class="sxs-lookup"><span data-stu-id="8f098-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f098-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f098-125">See Also</span></span>  
[<span data-ttu-id="8f098-126">Gestione assemblaggio</span><span class="sxs-lookup"><span data-stu-id="8f098-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="8f098-127">Utilizzare le distinte base</span><span class="sxs-lookup"><span data-stu-id="8f098-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="8f098-128">Magazzino</span><span class="sxs-lookup"><span data-stu-id="8f098-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8f098-129">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="8f098-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="8f098-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f098-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

