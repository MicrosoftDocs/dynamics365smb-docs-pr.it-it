---
title: Come chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino | Microsoft Docs
description: Utilizzare il campo **Collega da mov.** nella finestra **Registrazioni magazzino** per creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale. Ad esempio, per correggere la transazione in uscita o elaborare il suo reso.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d30a1316b48bd1b80ab4658ee99b14f0a0217478
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="bb89f-104">Procedura: Chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="bb89f-104">How to: Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="bb89f-105">Utilizzare il campo **Collega da mov.** nella finestra **Registrazioni magazzino** per creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale.</span><span class="sxs-lookup"><span data-stu-id="bb89f-105">You can use the **Applies-from Entry** field in the **Item Journal** window to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="bb89f-106">Ad esempio, per correggere la transazione in uscita o elaborare il suo reso.</span><span class="sxs-lookup"><span data-stu-id="bb89f-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="bb89f-107">Per ulteriori informazioni, vedere Collega da mov.</span><span class="sxs-lookup"><span data-stu-id="bb89f-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="bb89f-108">I collegamenti fissi creati in questo modo collegano solo il costo, non la quantità.</span><span class="sxs-lookup"><span data-stu-id="bb89f-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="bb89f-109">Di conseguenza, il movimento contabile articoli positivo registrato non chiuderà il movimento in uscita collegato e rimarrà aperto.</span><span class="sxs-lookup"><span data-stu-id="bb89f-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="bb89f-110">Ciò si applica anche quando si registra un collegamento fisso per un movimento positivo a un movimento negativo che non è stato chiuso da un movimento positivo normale, pertanto sia il movimento positivo che quello negativo rimarranno aperti.</span><span class="sxs-lookup"><span data-stu-id="bb89f-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="bb89f-111">Questo significa inoltre che non è possibile chiudere un periodo di magazzino se esiste tale movimento.</span><span class="sxs-lookup"><span data-stu-id="bb89f-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="bb89f-112">La seguente procedura illustra come chiudere tali movimenti con due registrazioni correttive nelle registrazioni magazzino.</span><span class="sxs-lookup"><span data-stu-id="bb89f-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="bb89f-113">Per chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="bb89f-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="bb89f-114">Utilizzare il campo **Collega-da mov.** per registrare una rettifica positiva con la quantità corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bb89f-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="bb89f-115">In questo modo si chiude il movimento negativo originale con un collegamento fisso.</span><span class="sxs-lookup"><span data-stu-id="bb89f-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="bb89f-116">Utilizzare il campo **Collega-da mov.** per registrare una rettifica negativa.</span><span class="sxs-lookup"><span data-stu-id="bb89f-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="bb89f-117">In questo modo si chiude il movimento positivo correttivo originale con un collegamento fisso.</span><span class="sxs-lookup"><span data-stu-id="bb89f-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb89f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb89f-118">See Also</span></span>  
[<span data-ttu-id="bb89f-119">Procedura: Rimuovere e ricollegare movimenti contabili articolo</span><span class="sxs-lookup"><span data-stu-id="bb89f-119"> How to: Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="bb89f-120">[Procedura: Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="bb89f-120">[How to: Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="bb89f-121">[Impostazione della valutazione magazzino e i costi](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="bb89f-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="bb89f-122">[Gestione dei costi di magazzino](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="bb89f-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="bb89f-123">Dettagli di progettazione: Metodi di costing</span><span class="sxs-lookup"><span data-stu-id="bb89f-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)

