---
title: Creare nuovi movimenti di valorizzazione per gli articoli in magazzino| Documenti Microsoft
description: "Descrive come rivalutare o ammortizzare i movimenti di valorizzazione di uno o più articoli in magazzino registrandone il corrente valore calcolato."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8460dac8478fa101a255d93110578fa9ea20516f
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="revalue-inventory"></a><span data-ttu-id="6d40a-103">Rivalutare il magazzino</span><span class="sxs-lookup"><span data-stu-id="6d40a-103">Revalue Inventory</span></span>
<span data-ttu-id="6d40a-104">Per rivalutare o ammortizzare un determinato articolo o movimento contabile articolo, è necessario utilizzare le registrazioni rivalutazioni.</span><span class="sxs-lookup"><span data-stu-id="6d40a-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="6d40a-105">Per rivalutare il magazzino</span><span class="sxs-lookup"><span data-stu-id="6d40a-105">To revalue inventory</span></span>
1. <span data-ttu-id="6d40a-106">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni rivalutazioni**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6d40a-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6d40a-107">Scegliere l'azione **Calcola valore magazzino**.</span><span class="sxs-lookup"><span data-stu-id="6d40a-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="6d40a-108">Nella finestra **Calcola valore magazzino** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="6d40a-108">In the **Calculate Inventory Value** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="6d40a-109">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d40a-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="6d40a-110">In ciascuna riga nella finestra **Registrazioni rivalutazioni**, nel campo **Costo unitario (rivalutato)**, immettere il nuovo costo unitario.</span><span class="sxs-lookup"><span data-stu-id="6d40a-110">On each line in the **Revaluation Journal** window, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="6d40a-111">In alternativa, immettere il nuovo importo totale nel campo **Costo unitario (rivalutato)**.</span><span class="sxs-lookup"><span data-stu-id="6d40a-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="6d40a-112">I dati pertinenti vengono automaticamente aggiornati.</span><span class="sxs-lookup"><span data-stu-id="6d40a-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="6d40a-113">Si noti che il campo **Importo** mostra la modifica effettiva del valore di magazzino per il movimento contabile articolo selezionato.</span><span class="sxs-lookup"><span data-stu-id="6d40a-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="6d40a-114">Calcola la differenza tra il campo **Valore Magazzino (Calcolato)** e il campo **Valore Magazzino (Rivalutato)**.</span><span class="sxs-lookup"><span data-stu-id="6d40a-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="6d40a-115">Una volta completate tutte le righe nelle registrazioni rivalutazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="6d40a-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="6d40a-116">Vengono a questo punto creati i nuovi movimenti di valorizzazione che riflettono le rivalutazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="6d40a-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="6d40a-117">È possibile visualizzare i nuovi valori nelle rispettive schede articolo.</span><span class="sxs-lookup"><span data-stu-id="6d40a-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d40a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d40a-118">See Also</span></span>
[<span data-ttu-id="6d40a-119">Dettagli di progettazione: Rivalutazione</span><span class="sxs-lookup"><span data-stu-id="6d40a-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="6d40a-120">Magazzino</span><span class="sxs-lookup"><span data-stu-id="6d40a-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6d40a-121">Vendite</span><span class="sxs-lookup"><span data-stu-id="6d40a-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="6d40a-122">Acquisti</span><span class="sxs-lookup"><span data-stu-id="6d40a-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6d40a-123">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d40a-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

