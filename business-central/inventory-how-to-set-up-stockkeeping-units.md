---
title: 'Procedura: Impostare le unità di stockkeeping | Documenti Microsoft'
description: Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 610939cb61c917d5319fc758e582c0d169d7f11b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182014"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="4e41f-103">Impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="4e41f-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="4e41f-104">Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.</span><span class="sxs-lookup"><span data-stu-id="4e41f-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="4e41f-105">Le unità di stockkeeping rappresentano un'integrazione alle schede articolo.</span><span class="sxs-lookup"><span data-stu-id="4e41f-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="4e41f-106">Non le sostituiscono, anche se sono correlate.</span><span class="sxs-lookup"><span data-stu-id="4e41f-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="4e41f-107">Queste unità consentono di differenziare le informazioni relative ad un articolo per una specifica ubicazione, ad esempio una warehouse o un centro di distribuzione, o una specifica variante, ad esempio numeri scaffale e diverse informazioni relative al riapprovvigionamento, per lo stesso articolo.</span><span class="sxs-lookup"><span data-stu-id="4e41f-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="4e41f-108">Per impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="4e41f-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="4e41f-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Unità di stockkeeping** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="4e41f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4e41f-110">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="4e41f-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="4e41f-111">Compilare i campi della scheda.</span><span class="sxs-lookup"><span data-stu-id="4e41f-111">Fill in the fields on the card.</span></span> <span data-ttu-id="4e41f-112">I campi seguenti sono obbligatori: **Nr. articolo**, **Cod. ubicazione**e/o **Cod. variante**.</span><span class="sxs-lookup"><span data-stu-id="4e41f-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="4e41f-113">Una volta impostata la prima unità di stockkeeping per un articolo, la casella di controllo **Unità di stockkeeping esisten.** nella scheda **Articolo** risulta selezionata.</span><span class="sxs-lookup"><span data-stu-id="4e41f-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="4e41f-114">Per creare diverse unità di stockkeeping per un articolo, utilizzare il processo batch **Crea unità di stockkeeping**.</span><span class="sxs-lookup"><span data-stu-id="4e41f-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4e41f-115">Le informazioni contenute nella scheda **Unità di stockkeeping** sono prioritarie rispetto a quelle della scheda **Articolo**.</span><span class="sxs-lookup"><span data-stu-id="4e41f-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="4e41f-116">Se la USK viene fornita tramite produzione, il campo **Costo standard** non è utilizzato quando si fattura e si rettifica il costo effettivo dell'articolo prodotto.</span><span class="sxs-lookup"><span data-stu-id="4e41f-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="4e41f-117">In alternativa, viene utilizzato il campo **Costo standard** nella scheda articolo sottostante e tutti gli scostamenti vengono calcolati rispetto al dettaglio costi di tale articolo.</span><span class="sxs-lookup"><span data-stu-id="4e41f-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="4e41f-118">Poiché le distinte base e il ciclo di produzione non possono essere assegnati a USK, anche il rollup del costo unitario e il calcolo correlato del dettaglio costi non sono disponibili nelle USK.</span><span class="sxs-lookup"><span data-stu-id="4e41f-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="4e41f-119">Per ulteriori informazioni, vedere [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="4e41f-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="4e41f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e41f-120">See Also</span></span>  
[<span data-ttu-id="4e41f-121">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="4e41f-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="4e41f-122">Impostazione gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="4e41f-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="4e41f-123">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="4e41f-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="4e41f-124">Magazzino</span><span class="sxs-lookup"><span data-stu-id="4e41f-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4e41f-125">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="4e41f-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="4e41f-126">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="4e41f-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="4e41f-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e41f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
