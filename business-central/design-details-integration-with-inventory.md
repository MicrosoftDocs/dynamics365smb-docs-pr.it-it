---
title: 'Dettagli di progettazione: Integrazione con il magazzino | Microsoft Docs'
description: L'area di applicazione Gestione warehouse e l'area di applicazione Magazzino interagiscono tra loro nell'inventario fisico e nella rettifica della warehouse o di magazzino.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 94eb1e0efa5c2a7ab54c46627b9d09ded6fae13f
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215155"
---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="55497-103">Dettagli di progettazione: Integrazione con il magazzino</span><span class="sxs-lookup"><span data-stu-id="55497-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="55497-104">L'area di applicazione Gestione warehouse e l'area di applicazione Magazzino interagiscono tra loro nell'inventario fisico e nella rettifica della warehouse o di magazzino.</span><span class="sxs-lookup"><span data-stu-id="55497-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="55497-105">Inventario fisico</span><span class="sxs-lookup"><span data-stu-id="55497-105">Physical Inventory</span></span>  
 <span data-ttu-id="55497-106">La pagina **Registrazioni Inventario Whse.** viene utilizzata con la pagina **Registrazioni inventario fis.** per tutte le ubicazioni warehouse avanzate.</span><span class="sxs-lookup"><span data-stu-id="55497-106">The **Whse. Phys. Inventory Journal** page is used with the **Phys. Inventory Journal** page for all advanced warehouse locations.</span></span> <span data-ttu-id="55497-107">Il magazzino a livello di collocazione viene calcolato e viene stampato un elenco per l'impiegato warehouse.</span><span class="sxs-lookup"><span data-stu-id="55497-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="55497-108">L'elenco indica quali elementi devono essere conteggiati in quali collocazioni.</span><span class="sxs-lookup"><span data-stu-id="55497-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="55497-109">Un impiegato warehouse immette la quantità conteggiata nella pagina **Registrazioni Inventario Whse.**, quindi effettua le registrazioni.</span><span class="sxs-lookup"><span data-stu-id="55497-109">The warehouse employee enters the counted quantity on the **Whse. Phys. Inventory Journal** page and then posts the journal.</span></span>  
  
 <span data-ttu-id="55497-110">Se la quantità conteggiata è maggiore della quantità nella riga delle registrazioni, verrà registrato un movimento per questa differenza dalla collocazione rettifica predefinita alla collocazione conteggiata.</span><span class="sxs-lookup"><span data-stu-id="55497-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="55497-111">In questo modo viene aumentata la quantità nella collocazione conteggiata e viene diminuita la quantità nella collocazione rettifica predefinita.</span><span class="sxs-lookup"><span data-stu-id="55497-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="55497-112">Se la quantità conteggiata è minore della quantità nella riga delle registrazioni, verrà registrato un movimento per questa differenza dalla collocazione conteggiata alla collocazione rettifica predefinita.</span><span class="sxs-lookup"><span data-stu-id="55497-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="55497-113">In questo modo la quantità nella collocazione conteggiata diminuisce e la quantità nella collocazione rettifica predefinita aumenta.</span><span class="sxs-lookup"><span data-stu-id="55497-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="55497-114">Nelle configurazioni avanzate della warehouse, il valore nel campo **Quantità (calcolata)** viene recuperato dai movimenti contabili articoli e il valore nel campo **Qtà (inv. fisico)** viene recuperato dai movimenti warehouse, escluso il contenuto della collocazione rettifica.</span><span class="sxs-lookup"><span data-stu-id="55497-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="55497-115">Il campo **Quantità** specifica la differenza tra i primi due campi, che devono essere uguali al contenuto della collocazione di rettifica.</span><span class="sxs-lookup"><span data-stu-id="55497-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="55497-116">Quando si effettuano le registrazioni di inventario, vengono aggiornati il magazzino e la collocazione rettifica predefinita.</span><span class="sxs-lookup"><span data-stu-id="55497-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="55497-117">Rettifiche di warehouse nel movimento contabile articolo</span><span class="sxs-lookup"><span data-stu-id="55497-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="55497-118">La pagina **Registrazioni magazzino** e la funzione **Calcola rettifica whse** consentono di rettificare il magazzino nei movimenti magazzino conformemente a una rettifica che è stata eseguita sulla quantità di articoli in una collocazione warehouse.</span><span class="sxs-lookup"><span data-stu-id="55497-118">You use the **Item Journal** page and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="55497-119">Per creare un collegamento tra il magazzino e la warehouse, è necessario definire una collocazione di rettifica predefinita per ubicazione.</span><span class="sxs-lookup"><span data-stu-id="55497-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="55497-120">La collocazione rettifica predefinita registra gli articoli nella warehouse quando si registra un aumento del magazzino.</span><span class="sxs-lookup"><span data-stu-id="55497-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="55497-121">Tuttavia, se si registra una riduzione, anche la quantità nella collocazione predefinita viene diminuita.</span><span class="sxs-lookup"><span data-stu-id="55497-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="55497-122">In entrambi i casi, vengono creati movimenti contabili articoli e movimenti warehouse.</span><span class="sxs-lookup"><span data-stu-id="55497-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="55497-123">La collocazione rettifica non è inclusa nel calcolo della disponibilità.</span><span class="sxs-lookup"><span data-stu-id="55497-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="55497-124">Se si desidera rettificare il contenuto collocazione, è possibile utilizzare le registrazioni articoli warehouse, da cui è possibile immettere il numero di articolo, il codice zona, il codice collocazione e la quantità da rettificare.</span><span class="sxs-lookup"><span data-stu-id="55497-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="55497-125">Se si immette una quantità positiva e si registra la riga, il magazzino archiviato nella collocazione aumenta e la quantità della collocazione di rettifica predefinita diminuisce di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="55497-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55497-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55497-126">See Also</span></span>  
 <span data-ttu-id="55497-127">[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="55497-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="55497-128">Dettagli di progettazione: Disponibilità nella warehouse</span><span class="sxs-lookup"><span data-stu-id="55497-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]