---
title: 'Dettagli di progettazione: Lotto-per-Lotto | Microsoft Docs'
description: "Informazioni su come utilizzare il metodo lotto-per lotto per stabilire la quantità dell'ordine in base alla domanda."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 7bc65fdb33b94b313b7d2b5b046156ca1d0788a2
ms.contentlocale: it-it
ms.lasthandoff: 11/20/2018

---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="a0ad6-103">Dettagli di progettazione: Lotto-per-Lotto</span><span class="sxs-lookup"><span data-stu-id="a0ad6-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="a0ad6-104">I criteri lotto per lotto sono i più flessibili perché il sistema reagisce solo alla domanda effettiva, agiscono inoltre sulla domanda prevista dalla previsione e dagli ordini programmati e stabiliscono la quantità dell'ordine in base alla domanda.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="a0ad6-105">I criteri lotto per lotto sono destinati agli elementi A e B dove il magazzino può essere accettato ma dovrebbe essere evitato.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  

<span data-ttu-id="a0ad6-106">Per certi aspetti, il metodo lotto per lotto è simile al metodo Ordine, ma presenta un approccio generico agli articoli; può accettare quantità in magazzino e aggrega la domanda e il corrispondente approvvigionamento in intervalli di tempo definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  

<span data-ttu-id="a0ad6-107">L'intervallo di tempo è definito nel campo **Intervallo di tempo**.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="a0ad6-108">Il sistema utilizza l'intervallo di tempo minimo pari a un giorno, che è l'unità di misura più piccola per gli eventi di domanda e approvvigionamento offerta dal sistema (sebbene, nella pratica, gli ordini di produzione e le richieste di componenti possano essere misurate in secondi).</span><span class="sxs-lookup"><span data-stu-id="a0ad6-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  

<span data-ttu-id="a0ad6-109">L'intervallo di tempo fissa anche dei limiti sui tempi di riprogrammazione di un ordine di approvvigionamento esistente per soddisfare una domanda specificata.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="a0ad6-110">Se l'approvvigionamento rientra nell'intervallo di tempo, viene riprogrammato all'interno o all'esterno in modo da soddisfare la domanda.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="a0ad6-111">In caso contrario, se risiede in un periodo precedente, causerà un accumulo di magazzino inutile e dovrà essere annullato.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="a0ad6-112">Se risiede dopo, verrà invece creato un nuovo ordine di approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-112">If it lies later, a new supply order will be created instead.</span></span>  

<span data-ttu-id="a0ad6-113">Con questo metodo, è possibile definire una scorta di sicurezza per compensare possibili fluttuazioni nell'approvvigionamento o per soddisfare una domanda improvvisa.</span><span class="sxs-lookup"><span data-stu-id="a0ad6-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  

<span data-ttu-id="a0ad6-114">Poiché la quantità dell'ordine di approvvigionamento è basato sulla domanda effettiva e può essere sensato utilizzare i modificatori di ordini: arrotondare la quantità di ordine fino a soddisfare un multiplo dell'ordine specificato (o unità di misura dell'acquisto), aumentare l'ordine a una quantità ordine minima specificata oppure diminuire la quantità alla quantità massima specificata (e creare quindi due o più approvvigionamenti per raggiungere la quantità necessaria totale).</span><span class="sxs-lookup"><span data-stu-id="a0ad6-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0ad6-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0ad6-115">See Also</span></span>  
<span data-ttu-id="a0ad6-116">[Dettagli di progettazione: Metodi di riordino](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a0ad6-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="a0ad6-117">[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="a0ad6-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="a0ad6-118">[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a0ad6-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="a0ad6-119">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="a0ad6-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

