---
title: Impostare i metodi di spedizione
description: È possibile impostare un codice per ciascuno dei metodi di spedizione offerti e immettere informazioni relative a ognuno di essi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8390c95083eb02c208e97f0309a725e8ec4d7730
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778574"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="a7f54-103">Impostare i metodi di spedizione</span><span class="sxs-lookup"><span data-stu-id="a7f54-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="a7f54-104">I metodi di spedizione dipendono spesso dagli articoli, dai clienti e dai fornitori.</span><span class="sxs-lookup"><span data-stu-id="a7f54-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="a7f54-105">Se ad esempio il cliente ha sede su un'isola, può scegliere che gli articoli gli vengano spediti sempre per via aerea oppure sempre via mare.</span><span class="sxs-lookup"><span data-stu-id="a7f54-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="a7f54-106">Alcuni clienti potrebbero richiedere la consegna il giorno successivo.</span><span class="sxs-lookup"><span data-stu-id="a7f54-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="a7f54-107">Alcuni potrebbero voler ritirare l'ordine.</span><span class="sxs-lookup"><span data-stu-id="a7f54-107">Some may want to pick up the order.</span></span> <span data-ttu-id="a7f54-108">Nelle schede cliente e fornitore è possibile specificare il tipo di consegna desiderato.</span><span class="sxs-lookup"><span data-stu-id="a7f54-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="a7f54-109">Impostare nella pagina **Metodi di spedizione** la descrizione e il codice di ciascun metodo di spedizione.</span><span class="sxs-lookup"><span data-stu-id="a7f54-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="a7f54-110">È possibile ad esempio impostare il codice FOB e immettere Franco a bordo nel campo **Descrizione**.</span><span class="sxs-lookup"><span data-stu-id="a7f54-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="a7f54-111">Sarà quindi possibile immettere il codice nei campi **Codice metodo di spedizione** altrove nel sistema ad esempio in una scheda cliente.</span><span class="sxs-lookup"><span data-stu-id="a7f54-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="a7f54-112">In seguito, quando si creano nuovi ordini, fatture, note di credito e così via, il sistema immetterà la descrizione rappresentata dal codice.</span><span class="sxs-lookup"><span data-stu-id="a7f54-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="a7f54-113">È possibile modificarla sul documento in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="a7f54-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="a7f54-114">Per impostare un metodo di spedizione</span><span class="sxs-lookup"><span data-stu-id="a7f54-114">To set up a shipment method</span></span>

1. <span data-ttu-id="a7f54-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Metodi di spedizione** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="a7f54-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="a7f54-116">Nella pagina **Metodi di spedizione** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="a7f54-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="a7f54-117">Nella nuova riga specificare un codice e una descrizione per il metodo di spedizione.</span><span class="sxs-lookup"><span data-stu-id="a7f54-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="a7f54-118">Se si utilizzano Incoterm, impostare i metodi di spedizione per rappresentare le regole Incoterm pertinenti.</span><span class="sxs-lookup"><span data-stu-id="a7f54-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a7f54-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a7f54-119">See Also</span></span>

[<span data-ttu-id="a7f54-120">Impostare gli spedizionieri</span><span class="sxs-lookup"><span data-stu-id="a7f54-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="a7f54-121">Rintracciare i colli</span><span class="sxs-lookup"><span data-stu-id="a7f54-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="a7f54-122">Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="a7f54-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="a7f54-123">Magazzino</span><span class="sxs-lookup"><span data-stu-id="a7f54-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a7f54-124">Impostazione gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="a7f54-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="a7f54-125">Gestione assemblaggio</span><span class="sxs-lookup"><span data-stu-id="a7f54-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="a7f54-126">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="a7f54-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="a7f54-127">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a7f54-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a7f54-128">Incoterm su iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="a7f54-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]