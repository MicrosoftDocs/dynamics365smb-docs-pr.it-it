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
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4870e82d4390e0a96a137579d035fee0e54b19eb
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="367cd-103">Impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="367cd-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="367cd-104">Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.</span><span class="sxs-lookup"><span data-stu-id="367cd-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="367cd-105">Le unità di stockkeeping rappresentano un'integrazione alle schede articolo.</span><span class="sxs-lookup"><span data-stu-id="367cd-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="367cd-106">Non le sostituiscono, anche se sono correlate.</span><span class="sxs-lookup"><span data-stu-id="367cd-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="367cd-107">Queste unità consentono di differenziare le informazioni relative ad un articolo per una specifica ubicazione, ad esempio una warehouse o un centro di distribuzione, o una specifica variante, ad esempio numeri scaffale e diverse informazioni relative al riapprovvigionamento, per lo stesso articolo.</span><span class="sxs-lookup"><span data-stu-id="367cd-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="367cd-108">Per impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="367cd-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="367cd-109">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Unità di stockkeeping**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="367cd-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="367cd-110">Scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="367cd-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="367cd-111">Compilare i campi della scheda.</span><span class="sxs-lookup"><span data-stu-id="367cd-111">Fill in the fields on the card.</span></span> <span data-ttu-id="367cd-112">I campi seguenti sono obbligatori: **Nr. articolo**, **Cod. ubicazione**e/o **Cod. variante**.</span><span class="sxs-lookup"><span data-stu-id="367cd-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="367cd-113">Una volta impostata la prima unità di stockkeeping per un articolo, la casella di controllo **Unità di stockkeeping esisten.** nella scheda **Articolo** risulta selezionata.</span><span class="sxs-lookup"><span data-stu-id="367cd-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="367cd-114">Per creare diverse unità di stockkeeping per un articolo, utilizzare il processo batch **Crea unità di stockkeeping**.</span><span class="sxs-lookup"><span data-stu-id="367cd-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="367cd-115">Le informazioni contenute nella scheda **Unità di stockkeeping** sono prioritarie rispetto a quelle della scheda **Articolo**.</span><span class="sxs-lookup"><span data-stu-id="367cd-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="367cd-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="367cd-116">See Also</span></span>  
[<span data-ttu-id="367cd-117">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="367cd-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="367cd-118">Impostazione gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="367cd-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="367cd-119">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="367cd-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="367cd-120">Magazzino</span><span class="sxs-lookup"><span data-stu-id="367cd-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="367cd-121">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="367cd-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="367cd-122">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="367cd-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="367cd-123">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="367cd-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

