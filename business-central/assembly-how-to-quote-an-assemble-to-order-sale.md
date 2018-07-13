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
ms.search.keywords: kit, kitting
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 046a42582dc66368fded90a4bb45add71a95d979
ms.openlocfilehash: 497d19dfdc8c972ff22aa0bcb65d96791bc8390e
ms.contentlocale: it-it
ms.lasthandoff: 07/02/2018

---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="1e4ea-103">Offerta per una vendita assemblaggio su ordine</span><span class="sxs-lookup"><span data-stu-id="1e4ea-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="1e4ea-104">È possibile utilizzare gestione assemblaggio per personalizzare un articolo di assemblaggio nella richiesta di un cliente durante il processo di vendita.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="1e4ea-105">Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="1e4ea-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="1e4ea-106">Come per la vendita di qualsiasi altro tipo di articolo, è inoltre possibile creare un'offerta di vendita di un articolo di assemblaggio personalizzato prima della conversione in ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="1e4ea-107">Questo processo prevede diversi passaggi aggiuntivi se viene confrontato alla creazione di un'offerta di vendita normale e utilizza una variazione di un ordine di assemblaggio collegato, ossia un'offerta di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="1e4ea-108">Come in tutti i tipi di offerte, le quantità nelle offerte di assemblaggio non vengono utilizzate per la disponibilità, la pianificazione o gli impegni.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="1e4ea-109">Per creare un'offerta di vendita per un articolo assemblato su ordine</span><span class="sxs-lookup"><span data-stu-id="1e4ea-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="1e4ea-110">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Offerte di vendita**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1e4ea-111">Creare una riga dell'offerta di vendita con una riga per un articolo di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="1e4ea-112">Per ulteriori informazioni, vedere [Creare offerte di vendita](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="1e4ea-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="1e4ea-113">Nel campo **Qtà per assemblaggio su ordine** immettere la quantità completa.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="1e4ea-114">Non si crea un'offerta per una quantità parziale.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="1e4ea-115">Di conseguenza, è necessario immettere la stessa quantità immessa nel campo **Quantità** della riga dell'offerta di vendita.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="1e4ea-116">Nella Scheda dettaglio **Righe** scegliere **Riga**, **Assemblaggio su ordine**, quindi **Righe di assemblaggio su ordine**.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="1e4ea-117">In alternativa, scegliere il campo **Qtà per assemblaggio su ordine** della riga.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="1e4ea-118">Nella finestra **Righe di assemblaggio su ordine** esaminare o modificare le righe dell'ordine di assemblaggio in base all'offerta richiesta dal cliente.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-118">In the **Assemble-to-Order Lines** window, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="1e4ea-119">Se si desidera visualizzare altre informazioni, scegliere l'azione **Mostra documento** per aprire l'ordine dell'offerta programmata completo.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="1e4ea-120">Non è possibile modificare il contenuto della maggior parte dei campi né effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="1e4ea-121">Dopo avere rettificato le righe dell'ordine di assemblaggio in base all'offerta, chiudere la finestra **Righe di assemblaggio su ordine** per tornare alla finestra **Offerta vendita**.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** window to return to the **Sales Quote** window.</span></span>  
7.  <span data-ttu-id="1e4ea-122">Se il cliente accetta l'offerta, creare un ordine di vendita per l'articolo di assemblaggio offerto.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="1e4ea-123">Per ulteriori informazioni, vedere [Creare offerte di vendita](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="1e4ea-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="1e4ea-124">L'offerta di assemblaggio collegata ed eventuali personalizzazioni sono collegate al nuovo ordine di vendita per preparare l'assemblaggio dell'articolo o degli articoli da vendere.</span><span class="sxs-lookup"><span data-stu-id="1e4ea-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1e4ea-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e4ea-125">See Also</span></span>  
[<span data-ttu-id="1e4ea-126">Gestione assemblaggio</span><span class="sxs-lookup"><span data-stu-id="1e4ea-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="1e4ea-127">Utilizzare le distinte base</span><span class="sxs-lookup"><span data-stu-id="1e4ea-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="1e4ea-128">Magazzino</span><span class="sxs-lookup"><span data-stu-id="1e4ea-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1e4ea-129">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="1e4ea-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1e4ea-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1e4ea-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

