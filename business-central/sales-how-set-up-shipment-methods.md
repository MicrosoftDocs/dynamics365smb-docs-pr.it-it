---
title: Come impostare metodi di spedizione | Documenti Microsoft
description: È possibile impostare un codice per ciascuno dei metodi di spedizione offerti e immettere informazioni relative a ognuno di essi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 48a75bd1d5a47e6e91ed64868f15743713e40ec4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926049"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="fa760-103">Impostare i metodi di spedizione</span><span class="sxs-lookup"><span data-stu-id="fa760-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="fa760-104">I metodi di spedizione, denominati anche incoterm, dipendono spesso dagli articoli, dai clienti e dai fornitori.</span><span class="sxs-lookup"><span data-stu-id="fa760-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="fa760-105">Se ad esempio il cliente ha sede su un'isola, può scegliere che gli articoli gli vengano spediti sempre per via aerea oppure sempre via mare.</span><span class="sxs-lookup"><span data-stu-id="fa760-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="fa760-106">Alcuni clienti potrebbero richiedere la consegna il giorno successivo.</span><span class="sxs-lookup"><span data-stu-id="fa760-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="fa760-107">Alcuni potrebbero voler ritirare l'ordine.</span><span class="sxs-lookup"><span data-stu-id="fa760-107">Some may want to pick up the order.</span></span> <span data-ttu-id="fa760-108">Nelle schede cliente e fornitore è possibile specificare il tipo di consegna desiderato.</span><span class="sxs-lookup"><span data-stu-id="fa760-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="fa760-109">Impostare nella pagina **Metodi di spedizione** la descrizione e il codice di ciascun metodo di spedizione.</span><span class="sxs-lookup"><span data-stu-id="fa760-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="fa760-110">È possibile ad esempio impostare il codice FOB e immettere Franco a bordo nel campo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="fa760-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="fa760-111">Sarà quindi possibile immettere il codice nei campi **Codice metodo di spedizione** altrove nel sistema ad esempio in una scheda cliente.</span><span class="sxs-lookup"><span data-stu-id="fa760-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="fa760-112">In seguito, quando si creano nuovi ordini, fatture, note di credito e così via, il sistema immetterà la descrizione rappresentata dal codice.</span><span class="sxs-lookup"><span data-stu-id="fa760-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="fa760-113">È possibile modificarla sul documento in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="fa760-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="fa760-114">Per impostare un codice spedizione</span><span class="sxs-lookup"><span data-stu-id="fa760-114">To set up a shipment code</span></span>
1. <span data-ttu-id="fa760-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Metodi di spedizione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fa760-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="fa760-116">Nella pagina **Metodi di spedizione** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="fa760-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="fa760-117">Nella nuova riga specificare un codice e una descrizione per il metodo di spedizione.</span><span class="sxs-lookup"><span data-stu-id="fa760-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa760-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fa760-118">See Also</span></span>
[<span data-ttu-id="fa760-119">Incoterm</span><span class="sxs-lookup"><span data-stu-id="fa760-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="fa760-120">Impostare gli spedizionieri</span><span class="sxs-lookup"><span data-stu-id="fa760-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="fa760-121">[Rintracciare i colli](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="fa760-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="fa760-122">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="fa760-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="fa760-123">Magazzino</span><span class="sxs-lookup"><span data-stu-id="fa760-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="fa760-124">[Impostazione gestione warehouse](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="fa760-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="fa760-125">[Gestione assemblaggio](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="fa760-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="fa760-126">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="fa760-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="fa760-127">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa760-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
