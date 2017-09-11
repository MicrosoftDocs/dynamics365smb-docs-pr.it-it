---
title: "Funzionalità della catena di approvvigionamento supportate da Financials | Documenti Microsoft"
description: Ottenere una panoramica del prodotto e informazioni sui concetti e i processi chiave della catena di approvvigionamento che fanno parte della soluzione ERP.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product overview, ERP
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3bae84075dc505aa9318590b1fac06e4844ffafe
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="overview-of-supply-chain-functionality"></a><span data-ttu-id="d89f3-103">Panoramica sulla funzionalità di catena di approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="d89f3-103">Overview of Supply Chain Functionality</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d89f3-104"> supporta i comuni processi della catena di approvvigionamento, sebbene limitati alle esigenze delle aziende di distribuzione e vendita all'ingrosso senza gestione warehouse.</span><span class="sxs-lookup"><span data-stu-id="d89f3-104"> supports common supply chain processes, although limited to the needs of wholesale and distribution companies without managed warehouse handling.</span></span>

<span data-ttu-id="d89f3-105">Oltre ai documenti di fatture di vendita è possibile gestire l'evasione ordini con ordini di vendita e la spedizione di parti di quantità di un ordine, ad esempio nel caso in cui non sia ancora disponibile la quantità completa.</span><span class="sxs-lookup"><span data-stu-id="d89f3-105">In addition to sales invoice documents, you can manage your order fulfillment with sales orders allowing you to ship parts of an order quantity, for example, because the full quantity is not available at once.</span></span> <span data-ttu-id="d89f3-106">È possibile gestire spedizioni dirette da un fornitore a un cliente collegando l'ordine di vendita al relativo ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="d89f3-106">You can have items drop shipped directly from a vendor to a customer by linking the sales order to the related purchase order.</span></span>

<span data-ttu-id="d89f3-107">Le quantità di magazzino vengono aggiornate in modo dinamico contestualmente ad acquisti e vendite degli articoli e le informazioni o gli avvisi sulla disponibilità vengono visualizzate per i venditori in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="d89f3-107">Your inventory quantities are dynamically updated as you sell and buy items, and availability information or warnings are shown to sales people in several ways.</span></span> <span data-ttu-id="d89f3-108">È possibile modificare manualmente le quantità di magazzino registrandole direttamente nei movimenti contabili articoli, ad esempio, dopo un conteggio fisico.</span><span class="sxs-lookup"><span data-stu-id="d89f3-108">You can adjust inventory quantities manually by posting directly to the item ledger entries, for example, after a physical count.</span></span> <span data-ttu-id="d89f3-109">È possibile offrire e vendere articoli ai clienti senza gestire un magazzino correlato.</span><span class="sxs-lookup"><span data-stu-id="d89f3-109">You can offer and sell items to your customers without maintaining inventory for them.</span></span> <span data-ttu-id="d89f3-110">Se si desidera includere questi articoli non in stock nel processo della catena di approvvigionamento, si deve semplicemente convertirli in normali articoli.</span><span class="sxs-lookup"><span data-stu-id="d89f3-110">If you want to include such nonstock items to your supply chain process, you simply convert them to normal items.</span></span>

<span data-ttu-id="d89f3-111">Oltre ai documenti fattura di acquisto, è possibile gestire il lato dell'approvvigionamento con gli ordini di acquisto con la possibilità di registrare carichi parziali di una quantità dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="d89f3-111">In addition to purchase invoice documents, you can manage your supply side with purchase orders allowing you to record partial receipts of an order quantity.</span></span> <span data-ttu-id="d89f3-112">Una funzione semplice di pianificazione degli approvvigionamenti consente di avviare un acquisto direttamente dalla fattura di vendita che richiede gli articoli.</span><span class="sxs-lookup"><span data-stu-id="d89f3-112">A simple supply planning function allows you to initiate a purchase directly from the sales invoice that requires the items.</span></span>

<span data-ttu-id="d89f3-113">Entrambi i documenti di vendita e acquisto possono essere registrati solo come spediti o ricevuti oppure come spediti o ricevuti e fatturati, con la possibilità di suddividere le responsabilità tra gestori ordini e ruoli contabili.</span><span class="sxs-lookup"><span data-stu-id="d89f3-113">Both sales and purchase documents can be posted as shipped or received only or as shipped or received and invoiced, allowing you to split the responsibilities of order processors and accounting roles.</span></span>

<span data-ttu-id="d89f3-114">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="d89f3-114">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="d89f3-115">Per</span><span class="sxs-lookup"><span data-stu-id="d89f3-115">To</span></span> | <span data-ttu-id="d89f3-116">Vedere</span><span class="sxs-lookup"><span data-stu-id="d89f3-116">See</span></span> |
| --- | --- |
| <span data-ttu-id="d89f3-117">Registrare i nuovi clienti, apportare le offerte di vendita, vendere i prodotti in ordini o fatture, ad esempio come spedizioni dirette, e gestire i resi di vendita.</span><span class="sxs-lookup"><span data-stu-id="d89f3-117">Register new customers, make sales offers, sell products on orders or invoices, for example as drop shipments, and manage sales returns.</span></span> |[<span data-ttu-id="d89f3-118">Vendite</span><span class="sxs-lookup"><span data-stu-id="d89f3-118">Sales</span></span>](sales-manage-sales.md) |
| <span data-ttu-id="d89f3-119">Registrare nuovi fornitori, articoli del fornitore in ordini o fatture, ad esempio con avvio da una fattura di vendita, e gestire i resi acquisto.</span><span class="sxs-lookup"><span data-stu-id="d89f3-119">Register new vendors, purchase items on orders or invoices, for example initiated from a sales invoice, and manage purchase returns.</span></span> |[<span data-ttu-id="d89f3-120">Acquisti</span><span class="sxs-lookup"><span data-stu-id="d89f3-120">Purchasing</span></span>](purchasing-manage-purchasing.md) |
| <span data-ttu-id="d89f3-121">Registrare nuovi prodotti fisici o di assistenza, rettificare le quantità di magazzino e gestire il valore di magazzino registrando i costi rettificati nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="d89f3-121">Register new physical or service products, adjust inventory quantities, and manage the inventory value by posting adjusted costs to the general ledger.</span></span> |[<span data-ttu-id="d89f3-122">Magazzino</span><span class="sxs-lookup"><span data-stu-id="d89f3-122">Inventory</span></span>](inventory-manage-inventory.md) |

## <a name="see-also"></a><span data-ttu-id="d89f3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d89f3-123">See Also</span></span>
[<span data-ttu-id="d89f3-124">Setup Vendite</span><span class="sxs-lookup"><span data-stu-id="d89f3-124">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="d89f3-125">[Gestione della contabilità clienti](receivables-manage-receivables.md)   </span><span class="sxs-lookup"><span data-stu-id="d89f3-125">[Managing Receivables](receivables-manage-receivables.md)   </span></span>  
[<span data-ttu-id="d89f3-126">Impostazioni acquisti</span><span class="sxs-lookup"><span data-stu-id="d89f3-126">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
<span data-ttu-id="d89f3-127">[Gestione della contabilità fornitori](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="d89f3-127">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="d89f3-128">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d89f3-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d89f3-129">Funzionalità aziendali generali</span><span class="sxs-lookup"><span data-stu-id="d89f3-129">General Business Functionality</span></span>](ui-across-business-areas.md)

