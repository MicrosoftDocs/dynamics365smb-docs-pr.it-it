---
title: "Procedura: Impostare le unità di stockkeeping | Documenti Microsoft"
description: "Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3c368af3347c72f2cf355876ed5574151095f993
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="ef650-103">Impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="ef650-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="ef650-104">Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.</span><span class="sxs-lookup"><span data-stu-id="ef650-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="ef650-105">Le unità di stockkeeping rappresentano un'integrazione alle schede articolo.</span><span class="sxs-lookup"><span data-stu-id="ef650-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="ef650-106">Non le sostituiscono, anche se sono correlate.</span><span class="sxs-lookup"><span data-stu-id="ef650-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="ef650-107">Queste unità consentono di differenziare le informazioni relative ad un articolo per una specifica ubicazione, ad esempio una warehouse o un centro di distribuzione, o una specifica variante, ad esempio numeri scaffale e diverse informazioni relative al riapprovvigionamento, per lo stesso articolo.</span><span class="sxs-lookup"><span data-stu-id="ef650-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="ef650-108">Per impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="ef650-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="ef650-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Unità di stockkeeping** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ef650-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ef650-110">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="ef650-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="ef650-111">Compilare i campi della scheda.</span><span class="sxs-lookup"><span data-stu-id="ef650-111">Fill in the fields on the card.</span></span> <span data-ttu-id="ef650-112">I campi seguenti sono obbligatori: **Nr. articolo**, **Cod. ubicazione**e/o **Cod. variante**.</span><span class="sxs-lookup"><span data-stu-id="ef650-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="ef650-113">Una volta impostata la prima unità di stockkeeping per un articolo, la casella di controllo **Unità di stockkeeping esisten.** nella scheda **Articolo** risulta selezionata.</span><span class="sxs-lookup"><span data-stu-id="ef650-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="ef650-114">Per creare diverse unità di stockkeeping per un articolo, utilizzare il processo batch **Crea unità di stockkeeping**.</span><span class="sxs-lookup"><span data-stu-id="ef650-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ef650-115">Le informazioni contenute nella scheda **Unità di stockkeeping** sono prioritarie rispetto a quelle della scheda **Articolo**.</span><span class="sxs-lookup"><span data-stu-id="ef650-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef650-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef650-116">See Also</span></span>  
[<span data-ttu-id="ef650-117">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="ef650-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="ef650-118">Impostazione gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="ef650-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="ef650-119">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="ef650-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ef650-120">Magazzino</span><span class="sxs-lookup"><span data-stu-id="ef650-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ef650-121">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ef650-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ef650-122">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="ef650-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ef650-123">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef650-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

