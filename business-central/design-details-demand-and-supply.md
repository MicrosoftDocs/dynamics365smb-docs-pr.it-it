---
title: 'Dettagli di progettazione: Domanda e approvvigionamento | Microsoft Docs'
description: La domanda è il termine comune utilizzato per tutti i tipi di domanda lorda, ad esempio un ordine di vendita e un componente necessario da un ordine di produzione. Inoltre, il programma consente i tipi di domanda più tecnici, ad esempio resi di acquisto e delle giacenze negative.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: ad6684bb1fefe10fc965c3c8a7780c6aa8a9d685
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801991"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="7c52d-104">Dettagli di progettazione: Domanda e approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="7c52d-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="7c52d-105">La domanda è il termine comune utilizzato per tutti i tipi di domanda lorda, ad esempio un ordine di vendita e un componente necessario da un ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="7c52d-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="7c52d-106">Inoltre, il programma consente i tipi di domanda più tecnici, ad esempio resi di acquisto e delle giacenze negative.</span><span class="sxs-lookup"><span data-stu-id="7c52d-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  

 <span data-ttu-id="7c52d-107">Approvvigionamento è il termine comune utilizzato per indicare qualsiasi genere di quantità in entrata o positiva, quale il magazzino, gli acquisti, l'assemblaggio, la produzione o i trasferimenti in entrata.</span><span class="sxs-lookup"><span data-stu-id="7c52d-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="7c52d-108">Inoltre, anche un reso di vendita può rappresentare un approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="7c52d-108">In addition, a sales return may also represent supply.</span></span>  

 <span data-ttu-id="7c52d-109">Per ordinare le numerose origini di approvvigionamento e di domanda, il sistema di pianificazione le organizza su due righe chiamate profili di magazzino.</span><span class="sxs-lookup"><span data-stu-id="7c52d-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="7c52d-110">Un profilo conserva gli eventi di domanda e l'altro conserva i corrispondenti eventi di approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="7c52d-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="7c52d-111">Ogni evento rappresenta un'entità di rete di ordini, ad esempio una riga ordine di vendita, un movimento contabile di magazzino o una riga di ordine di produzione.</span><span class="sxs-lookup"><span data-stu-id="7c52d-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  

 <span data-ttu-id="7c52d-112">Quando vengono caricati i profili di magazzino, i differenti set di domanda-approvvigionamento vengono bilanciati in modo da fornire un piano di approvvigionamento che soddisfi gli obiettivi elencati.</span><span class="sxs-lookup"><span data-stu-id="7c52d-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  

 <span data-ttu-id="7c52d-113">I parametri di pianificazione e i livelli di magazzino sono altri tipi rispettivamente di domanda e di approvvigionamento, che subiscono la contropartita integrata per rifornire gli articoli in stock.</span><span class="sxs-lookup"><span data-stu-id="7c52d-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="7c52d-114">Per ulteriori informazioni, vedere [Dettagli di programmazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="7c52d-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c52d-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c52d-115">See Also</span></span>  
 <span data-ttu-id="7c52d-116">[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="7c52d-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="7c52d-117">[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="7c52d-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="7c52d-118">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="7c52d-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
