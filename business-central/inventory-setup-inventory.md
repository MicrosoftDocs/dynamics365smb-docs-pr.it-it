---
title: Impostazione del magazzino | Documenti Microsoft
description: Viene descritto come impostare i processi di magazzino e stock, inclusi i percorsi di trasferimento e le ubicazioni, come le warehouse.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e4033412560e8dc847397c4399e12985490bf78
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="acd26-103">Impostazione del magazzino</span><span class="sxs-lookup"><span data-stu-id="acd26-103">Setting Up Inventory</span></span>
<span data-ttu-id="acd26-104">Prima di poter gestire le attività di warehouse e i costi di magazzino, è necessario configurare le regole e i valori che definiscono i criteri di acquisto del magazzino.</span><span class="sxs-lookup"><span data-stu-id="acd26-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="acd26-105">È possibile offrire assistenza clienti e ottimizzare la catena di approvvigionamento organizzando il magazzino presso indirizzi diversi.</span><span class="sxs-lookup"><span data-stu-id="acd26-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="acd26-106">È quindi possibile acquistare, archiviare o vendere articoli in ubicazioni diverse e trasferire il magazzino tra loro.</span><span class="sxs-lookup"><span data-stu-id="acd26-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="acd26-107">Dopo aver impostato il magazzino, è possibile gestire i vari processi relativi alle transazioni di articoli.</span><span class="sxs-lookup"><span data-stu-id="acd26-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="acd26-108">Per ulteriori informazioni, vedere e [Gestire i costi del magazzino](inventory-manage-inventory.md) e [Gestione warehouse](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="acd26-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="acd26-109">A</span><span class="sxs-lookup"><span data-stu-id="acd26-109">To</span></span> | <span data-ttu-id="acd26-110">Vedere</span><span class="sxs-lookup"><span data-stu-id="acd26-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="acd26-111">Definire il setup generale del magazzino, ad esempio la numerazione e le modalità di utilizzo delle ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="acd26-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="acd26-112">Impostare le informazioni generali di magazzino</span><span class="sxs-lookup"><span data-stu-id="acd26-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="acd26-113">Configurare un modello di distribuzione efficiente con una combinazione di ubicazioni e centri di responsabilità diversi assegnati a impiegati o partner aziendali.</span><span class="sxs-lookup"><span data-stu-id="acd26-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="acd26-114">Utilizzare i centri di responsabilità</span><span class="sxs-lookup"><span data-stu-id="acd26-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="acd26-115">Organizzare le scorte presenti in più ubicazioni, inclusi i percorsi di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="acd26-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="acd26-116">Impostare le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="acd26-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="acd26-117">Creare schedhe articolo per ogni articolo di tipo Inventario, Assistenza, non inventario trattato.</span><span class="sxs-lookup"><span data-stu-id="acd26-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="acd26-118">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="acd26-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="acd26-119">Informazioni su come compilare il campo **Tipo** nelle schede articolo in base allo scopo aziendale.</span><span class="sxs-lookup"><span data-stu-id="acd26-119">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="acd26-120">Informazioni sui tipi di articolo</span><span class="sxs-lookup"><span data-stu-id="acd26-120">About Item Types</span></span>](inventory-about-item-types.md)| 
|<span data-ttu-id="acd26-121">Impostare più unità di misura per un articolo che può essere utilizzato come UDM alternativa, ad esempio, nelle transazioni di vendita, acquisto o produzione.</span><span class="sxs-lookup"><span data-stu-id="acd26-121">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="acd26-122">Impostare unità di misura articolo</span><span class="sxs-lookup"><span data-stu-id="acd26-122">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="acd26-123">In aggiunta alle schede articolo, registrare le informazioni relative agli articoli in una specifica ubicazione e/o di una specifica variante.</span><span class="sxs-lookup"><span data-stu-id="acd26-123">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="acd26-124">Impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="acd26-124">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="acd26-125">Assegnare articoli alle categorie e dare loro attributi per consentire alla propria azienda e ai clienti la ricerca degli articoli.</span><span class="sxs-lookup"><span data-stu-id="acd26-125">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="acd26-126">Classificare gli articoli</span><span class="sxs-lookup"><span data-stu-id="acd26-126">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="acd26-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acd26-127">See Also</span></span>
[<span data-ttu-id="acd26-128">Gestione dei costi del magazzino</span><span class="sxs-lookup"><span data-stu-id="acd26-128">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="acd26-129">Gestione acquisti</span><span class="sxs-lookup"><span data-stu-id="acd26-129">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="acd26-130">[Gestione vendite](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="acd26-130">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="acd26-131">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="acd26-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="acd26-132">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="acd26-132">General Business Functionality</span></span>](ui-across-business-areas.md)

