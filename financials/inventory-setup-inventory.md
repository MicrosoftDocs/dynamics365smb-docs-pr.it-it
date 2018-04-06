---
title: Impostazione del magazzino | Documenti Microsoft
description: Viene descritto come impostare i processi di magazzino e stock, inclusi i percorsi di trasferimento e le ubicazioni, come le warehouse.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5a667f28bd50bbd1149526e08e0d786da83bc8a6
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="9290b-103">Impostazione del magazzino</span><span class="sxs-lookup"><span data-stu-id="9290b-103">Setting Up Inventory</span></span>
<span data-ttu-id="9290b-104">Prima di poter gestire le attività di warehouse e i costi di magazzino, è necessario configurare le regole e i valori che definiscono i criteri di acquisto del magazzino.</span><span class="sxs-lookup"><span data-stu-id="9290b-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="9290b-105">È possibile offrire assistenza clienti e ottimizzare la catena di approvvigionamento organizzando il magazzino presso indirizzi diversi.</span><span class="sxs-lookup"><span data-stu-id="9290b-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="9290b-106">È quindi possibile acquistare, archiviare o vendere articoli in ubicazioni diverse e trasferire il magazzino tra loro.</span><span class="sxs-lookup"><span data-stu-id="9290b-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="9290b-107">Dopo aver impostato il magazzino, è possibile gestire i vari processi relativi alle transazioni di articoli.</span><span class="sxs-lookup"><span data-stu-id="9290b-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="9290b-108">Per ulteriori informazioni, vedere e [Gestire i costi del magazzino](inventory-manage-inventory.md) e [Gestione warehouse](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="9290b-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="9290b-109">A</span><span class="sxs-lookup"><span data-stu-id="9290b-109">To</span></span> | <span data-ttu-id="9290b-110">Vedere</span><span class="sxs-lookup"><span data-stu-id="9290b-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="9290b-111">Definire il setup generale del magazzino, ad esempio la numerazione e le modalità di utilizzo delle ubicazioni.</span><span class="sxs-lookup"><span data-stu-id="9290b-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="9290b-112">Impostare le informazioni generali di magazzino</span><span class="sxs-lookup"><span data-stu-id="9290b-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="9290b-113">Configurare un modello di distribuzione efficiente con una combinazione di ubicazioni e centri di responsabilità diversi assegnati a impiegati o partner aziendali.</span><span class="sxs-lookup"><span data-stu-id="9290b-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="9290b-114">Utilizzare i centri di responsabilità</span><span class="sxs-lookup"><span data-stu-id="9290b-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="9290b-115">Organizzare le scorte presenti in più ubicazioni, inclusi i percorsi di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="9290b-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="9290b-116">Impostare le ubicazioni</span><span class="sxs-lookup"><span data-stu-id="9290b-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="9290b-117">Creare le schede articolo per gli articoli di magazzino trattati.</span><span class="sxs-lookup"><span data-stu-id="9290b-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="9290b-118">Registrare nuovi articoli</span><span class="sxs-lookup"><span data-stu-id="9290b-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="9290b-119">Impostare più unità di misura per un articolo che può essere utilizzato come UDM alternativa, ad esempio, nelle transazioni di vendita, acquisto o produzione.</span><span class="sxs-lookup"><span data-stu-id="9290b-119">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="9290b-120">Impostare unità di misura articolo</span><span class="sxs-lookup"><span data-stu-id="9290b-120">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="9290b-121">In aggiunta alle schede articolo, registrare le informazioni relative agli articoli in una specifica ubicazione e/o di una specifica variante.</span><span class="sxs-lookup"><span data-stu-id="9290b-121">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="9290b-122">Impostare le unità di stockkeeping</span><span class="sxs-lookup"><span data-stu-id="9290b-122">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="9290b-123">Assegnare articoli alle categorie e dare loro attributi per consentire alla propria azienda e ai clienti la ricerca degli articoli.</span><span class="sxs-lookup"><span data-stu-id="9290b-123">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="9290b-124">Classificare gli articoli</span><span class="sxs-lookup"><span data-stu-id="9290b-124">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="9290b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9290b-125">See Also</span></span>
[<span data-ttu-id="9290b-126">Gestione dei costi del magazzino</span><span class="sxs-lookup"><span data-stu-id="9290b-126">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9290b-127">Gestione acquisti</span><span class="sxs-lookup"><span data-stu-id="9290b-127">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9290b-128">[Gestione vendite](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="9290b-128">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="9290b-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9290b-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9290b-130">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="9290b-130">General Business Functionality</span></span>](ui-across-business-areas.md)

