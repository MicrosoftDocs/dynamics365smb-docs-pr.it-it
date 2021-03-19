---
title: Come stampare una lista prelievo magazzino da un ordine di vendita
description: È possibile stampare una lista prelievo magazzino direttamente da un ordine di vendita, vendite, fattura e altri documenti di vendita in uscita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 48c1a45e1abc510ce98f405dcdecc5d91d1a9ac5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393726"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="2f47a-103">Stampare la lista prelievo</span><span class="sxs-lookup"><span data-stu-id="2f47a-103">Print the Picking List</span></span>
<span data-ttu-id="2f47a-104">È possibile stampare una lista prelievo magazzino direttamente da un ordine di vendita, una fattura di vendita o qualsiasi altro documento che avvia la spedizione di articoli.</span><span class="sxs-lookup"><span data-stu-id="2f47a-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="2f47a-105">Questo report viene in genere utilizzato in società senza funzionalità dedicata per la gestione del magazzino, in modo che un addetto all'inventario possa semplicemente visualizzare o stampare la lista prelievo dal relativo documento di vendita.</span><span class="sxs-lookup"><span data-stu-id="2f47a-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="2f47a-106">In società con volumi più elevati o processi più complessi, il prelievo viene pianificato ed eseguito in documenti di magazzino dedicati.</span><span class="sxs-lookup"><span data-stu-id="2f47a-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="2f47a-107">Per ulteriori informazioni, vedere [Prelevare articoli](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="2f47a-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="2f47a-108">Per stampare una lista prelievo da un ordine di vendita</span><span class="sxs-lookup"><span data-stu-id="2f47a-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="2f47a-109">La seguente procedura è basata su un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="2f47a-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="2f47a-110">I passaggi sono simili per tutti i documenti di vendita che possono essere utilizzati per avviare la spedizione degli articoli.</span><span class="sxs-lookup"><span data-stu-id="2f47a-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="2f47a-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="2f47a-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f47a-112">Aprire l'ordine di vendita per cui si desidera prelevare gli articoli.</span><span class="sxs-lookup"><span data-stu-id="2f47a-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="2f47a-113">Scegliere l'azione **Report**, quindi scegliere l'azione **Lista prelievo per ordine**.</span><span class="sxs-lookup"><span data-stu-id="2f47a-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="2f47a-114">Scegliere il pulsante **Stampa** per stampare la lista prelievo oppure scegliere il pulsante **Anteprima** per visualizzarla sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2f47a-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="2f47a-115">È inoltre possibile salvare la lista prelievo come documento, ad esempio da inviare a qualcuno o da aggiungere come allegato all'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="2f47a-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="2f47a-116">Per ulteriori informazioni, vedere [Gestire allegati, collegamenti e note in schede e documenti](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="2f47a-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2f47a-117">Se si è utilizzata la funzione **Esplodi DB** nell'ordine di vendita, nel report vengono visualizzati solo i componenti dell'articolo di assemblaggio correlato.</span><span class="sxs-lookup"><span data-stu-id="2f47a-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="2f47a-118">Per altre informazioni, vedere [Utilizzare le distinte base](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="2f47a-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2f47a-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2f47a-119">See Also</span></span>  
[<span data-ttu-id="2f47a-120">Magazzino</span><span class="sxs-lookup"><span data-stu-id="2f47a-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2f47a-121">Prelievo degli articoli</span><span class="sxs-lookup"><span data-stu-id="2f47a-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="2f47a-122">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f47a-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>   


[!INCLUDE[footer-include](includes/footer-banner.md)]