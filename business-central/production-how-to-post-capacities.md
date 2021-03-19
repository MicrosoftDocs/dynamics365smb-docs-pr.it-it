---
title: Come registrare le capacità | Microsoft Docs
description: Nelle registrazioni delle rettifiche delle capacità vengono registrate le capacità utilizzate che non sono assegnate all'ordine di produzione. La manutenzione, ad esempio, deve essere assegnata alla capacità ma non a un ordine di produzione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cab8b2e4670a04e52bdc1edcc91c50a44da06b0d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381242"
---
# <a name="post-capacities"></a><span data-ttu-id="361b9-104">Registrare le capacità</span><span class="sxs-lookup"><span data-stu-id="361b9-104">Post Capacities</span></span>
<span data-ttu-id="361b9-105">Nelle registrazioni delle rettifiche delle capacità vengono registrate le capacità utilizzate che non sono assegnate all'ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="361b9-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="361b9-106">La manutenzione, ad esempio, deve essere assegnata alla capacità ma non a un ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="361b9-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="361b9-107">Per registrare le capacità</span><span class="sxs-lookup"><span data-stu-id="361b9-107">To post capacities</span></span>  
1.  <span data-ttu-id="361b9-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni capacità** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="361b9-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="361b9-109">Immettere la **data di registrazione** e il **nr. di documento** .</span><span class="sxs-lookup"><span data-stu-id="361b9-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="361b9-110">Immettere nel campo **Tipo** il tipo di capacità, **Centri di Lavoro** o **Aree di Produzione** che si sta registrando.</span><span class="sxs-lookup"><span data-stu-id="361b9-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="361b9-111">Nel campo **Nr.**</span><span class="sxs-lookup"><span data-stu-id="361b9-111">In the **No.**</span></span> <span data-ttu-id="361b9-112">immettere il numero del centro di lavoro o dell'area di produzione.</span><span class="sxs-lookup"><span data-stu-id="361b9-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="361b9-113">Compilare i campi rimanenti **Ora Inizio**, **Ora Fine**, **Quantità** e **Scarto** inserendo i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="361b9-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="361b9-114">Per registrare le capacità scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="361b9-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="361b9-115">Per visualizzare i movimenti contabili relativi alle aree di produzione:</span><span class="sxs-lookup"><span data-stu-id="361b9-115">To view work center ledger entries</span></span>  
<span data-ttu-id="361b9-116">Nelle pagine **Scheda area di produzione** e **Scheda centri lavoro**, è possibile visualizzare le capacità registrate come risultato di ordini di produzione chiusi.</span><span class="sxs-lookup"><span data-stu-id="361b9-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="361b9-117">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Aree di produzione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="361b9-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="361b9-118">Aprire la scheda **Area di produzione** pertinente dall'elenco e scegliere l'azione **Movimenti contabili capacità**.</span><span class="sxs-lookup"><span data-stu-id="361b9-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="361b9-119">Nella pagina **Movimenti Contabili Capacità** vengono visualizzati i movimenti registrati relativi all'area di produzione in ordine di registrazione.</span><span class="sxs-lookup"><span data-stu-id="361b9-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="361b9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="361b9-120">See Also</span></span>  
<span data-ttu-id="361b9-121">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="361b9-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="361b9-122">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="361b9-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="361b9-123">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="361b9-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="361b9-124">Magazzino</span><span class="sxs-lookup"><span data-stu-id="361b9-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="361b9-125">Acquisti</span><span class="sxs-lookup"><span data-stu-id="361b9-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="361b9-126">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="361b9-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]