---
title: Creare nuovi movimenti di valorizzazione per gli articoli in magazzino| Documenti Microsoft
description: Descrive come rivalutare o ammortizzare i movimenti di valorizzazione di uno o più articoli in magazzino registrandone il corrente valore calcolato.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3fe164e6e71756ee56990610bc6c6cb0557ad2c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785850"
---
# <a name="revalue-inventory"></a><span data-ttu-id="1cad4-103">Rivalutare il magazzino</span><span class="sxs-lookup"><span data-stu-id="1cad4-103">Revalue Inventory</span></span>
<span data-ttu-id="1cad4-104">Per rivalutare o ammortizzare un determinato articolo o movimento contabile articolo, è necessario utilizzare le registrazioni rivalutazioni.</span><span class="sxs-lookup"><span data-stu-id="1cad4-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="1cad4-105">Per rivalutare il magazzino</span><span class="sxs-lookup"><span data-stu-id="1cad4-105">To revalue inventory</span></span>
1. <span data-ttu-id="1cad4-106">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni rivalutazioni** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1cad4-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="1cad4-107">Scegliere l'azione **Calcola valore magazzino**.</span><span class="sxs-lookup"><span data-stu-id="1cad4-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="1cad4-108">Nella pagina **Calcola valore magazzino** compilare i campi secondo le necessità.</span><span class="sxs-lookup"><span data-stu-id="1cad4-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="1cad4-109">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cad4-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="1cad4-110">In ciascuna riga nella pagina **Registrazioni rivalutazioni**, nel campo **Costo unitario (rivalutato)**, immettere il nuovo costo unitario.</span><span class="sxs-lookup"><span data-stu-id="1cad4-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="1cad4-111">In alternativa, immettere il nuovo importo totale nel campo **Costo unitario (rivalutato)**.</span><span class="sxs-lookup"><span data-stu-id="1cad4-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="1cad4-112">I dati pertinenti vengono automaticamente aggiornati.</span><span class="sxs-lookup"><span data-stu-id="1cad4-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="1cad4-113">Si noti che il campo **Importo** mostra la modifica effettiva del valore di magazzino per il movimento contabile articolo selezionato.</span><span class="sxs-lookup"><span data-stu-id="1cad4-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="1cad4-114">Calcola la differenza tra il campo **Valore Magazzino (Calcolato)** e il campo **Valore Magazzino (Rivalutato)**.</span><span class="sxs-lookup"><span data-stu-id="1cad4-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="1cad4-115">Una volta completate tutte le righe nelle registrazioni rivalutazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="1cad4-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="1cad4-116">Vengono a questo punto creati i nuovi movimenti di valorizzazione che riflettono le rivalutazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="1cad4-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="1cad4-117">È possibile visualizzare i nuovi valori nelle rispettive schede articolo.</span><span class="sxs-lookup"><span data-stu-id="1cad4-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cad4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cad4-118">See Also</span></span>
[<span data-ttu-id="1cad4-119">Dettagli di progettazione: Rivalutazione</span><span class="sxs-lookup"><span data-stu-id="1cad4-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="1cad4-120">Magazzino</span><span class="sxs-lookup"><span data-stu-id="1cad4-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1cad4-121">Vendite</span><span class="sxs-lookup"><span data-stu-id="1cad4-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="1cad4-122">Acquisti</span><span class="sxs-lookup"><span data-stu-id="1cad4-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1cad4-123">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1cad4-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]