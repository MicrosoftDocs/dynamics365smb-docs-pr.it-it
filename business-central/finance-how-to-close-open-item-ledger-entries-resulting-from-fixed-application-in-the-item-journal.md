---
title: Chiudere i movimenti contabili articoli derivanti dall'utilizzo del collegamento fisso
description: Scopri come creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale nelle registrazioni articoli.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 2cc663d580da4738247b9fcdbe5fc4504c37fa73
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013873"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="7a4ea-103">Chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="7a4ea-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="7a4ea-104">Utilizzare il campo **Collega da mov.** nella pagina **Registrazioni magazzino** per creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="7a4ea-105">Ad esempio, per correggere la transazione in uscita o elaborare il suo reso.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="7a4ea-106">I collegamenti fissi creati in questo modo collegano solo il costo, non la quantità.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="7a4ea-107">Di conseguenza, il movimento contabile articoli positivo registrato non chiuderà il movimento in uscita collegato e rimarrà aperto.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="7a4ea-108">Ciò si applica anche quando si registra un collegamento fisso per un movimento positivo a un movimento negativo che non è stato chiuso da un movimento positivo normale, pertanto sia il movimento positivo che quello negativo rimarranno aperti.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="7a4ea-109">Questo significa inoltre che non è possibile chiudere un periodo di magazzino se esiste tale movimento.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="7a4ea-110">È possibile modificare e riapplicare i movimenti di collegamento a certe condizioni utilizzando la pagina **Prospetto collegamento**.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="7a4ea-111">La seguente procedura illustra come chiudere tali movimenti con due registrazioni correttive nelle registrazioni magazzino.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="7a4ea-112">Per chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino</span><span class="sxs-lookup"><span data-stu-id="7a4ea-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="7a4ea-113">Utilizzare il campo **Collega-da mov.** per registrare una rettifica positiva con la quantità corrispondente.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="7a4ea-114">In questo modo si chiude il movimento negativo originale con un collegamento fisso.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="7a4ea-115">Il campo **Collegare da - Movimento** specifica il numero del movimento contabile articoli in uscita il cui costo è inoltrato al movimento contabile articoli in ingresso quando si registra una transazione in ingresso di tipo **Rettifiche Positive** o **Acquisto** con le registrazioni magazzino.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="7a4ea-116">Utilizzare il campo **Collega-da mov.** per registrare una rettifica negativa.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="7a4ea-117">In questo modo si chiude il movimento positivo correttivo originale con un collegamento fisso.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="7a4ea-118">Il campo **Collegare a - Movimento** specifica se la quantità nella riga di registrazione magazzino deve essere collegata a un documento già registrato.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="7a4ea-119">In questo caso, immettere il numero del movimento contabile articolo a cui la riga di registrazione magazzino deve essere collegata.</span><span class="sxs-lookup"><span data-stu-id="7a4ea-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a4ea-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7a4ea-120">See Also</span></span>

[<span data-ttu-id="7a4ea-121">Rimuovere e ricollegare movimenti contabili articolo</span><span class="sxs-lookup"><span data-stu-id="7a4ea-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="7a4ea-122">Elaborare i resi e gli annullamenti vendite</span><span class="sxs-lookup"><span data-stu-id="7a4ea-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="7a4ea-123">Impostazione della valutazione magazzino e i costi</span><span class="sxs-lookup"><span data-stu-id="7a4ea-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="7a4ea-124">Gestione dei costi di magazzino</span><span class="sxs-lookup"><span data-stu-id="7a4ea-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="7a4ea-125">Dettagli di progettazione: Metodi di costing</span><span class="sxs-lookup"><span data-stu-id="7a4ea-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
