---
title: 'Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione | Microsoft Docs'
description: In questo argomento vengono descritte le regole che la pianificazione applica agli ordini nella zona bloccata.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: bc594a93987bf8740964b082fed25dc8d7e269fe
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307302"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a><span data-ttu-id="3b290-103">Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione</span><span class="sxs-lookup"><span data-stu-id="3b290-103">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>
<span data-ttu-id="3b290-104">Per evitare che un piano di approvvigionamento mostri suggerimenti impossibili e pertanto inutili, il sistema di pianificazione considera il periodo fino alla data di inizio pianificazione come una zona bloccata nella quale nulla viene pianificato.</span><span class="sxs-lookup"><span data-stu-id="3b290-104">To avoid that a supply plan shows impossible and therefore useless suggestions, the planning system regards the period up until the planning starting date a frozen zone where nothing is planned for.</span></span> <span data-ttu-id="3b290-105">La seguente regola si applica alla zona bloccata:</span><span class="sxs-lookup"><span data-stu-id="3b290-105">The following rule applies to the frozen zone:</span></span>  

<span data-ttu-id="3b290-106">Tutta le domande e l'approvvigionamento prima della data di inizio del periodo di pianificazione verranno considerati come parte del magazzino o saranno spediti.</span><span class="sxs-lookup"><span data-stu-id="3b290-106">All supply and demand before the starting date of the planning period will be considered a part of inventory or shipped.</span></span>  

<span data-ttu-id="3b290-107">Di conseguenza, il sistema di pianificazione non suggerisce, con poche eccezioni, modifiche agli ordini di approvvigionamento nella zona bloccata e nessun collegamento di tracciabilità viene creato o gestito per quel periodo.</span><span class="sxs-lookup"><span data-stu-id="3b290-107">Accordingly, the planning system will not, with a few exceptions, suggest any changes to supply orders in the frozen zone, and no order tracking links are created or maintained for that period.</span></span>  

<span data-ttu-id="3b290-108">Le eccezioni a questa regola sono:</span><span class="sxs-lookup"><span data-stu-id="3b290-108">The exceptions to this rule are as follows:</span></span>  

* <span data-ttu-id="3b290-109">Se le scorte disponibili previste, inclusa la somma di domanda e approvvigionamento nella zona bloccata, è inferiore a zero.</span><span class="sxs-lookup"><span data-stu-id="3b290-109">If the projected available inventory, including the sum of supply and demand in the frozen zone, is below zero.</span></span>  
* <span data-ttu-id="3b290-110">Se i numeri seriali o di lotto sono obbligatori negli ordini retrodatati.</span><span class="sxs-lookup"><span data-stu-id="3b290-110">If serial/lot numbers are required on the backdated order(s).</span></span>  
* <span data-ttu-id="3b290-111">Se il set di approvvigionamento-domanda è collegato da un metodo ordine su ordine.</span><span class="sxs-lookup"><span data-stu-id="3b290-111">If the supply-demand set is linked by an order-to-order policy.</span></span>  

<span data-ttu-id="3b290-112">Se la giacenza disponibile iniziale è minore di zero, il sistema di pianificazione suggerisce un ordine di approvvigionamento di emergenza datato il giorno precedente al periodo di pianificazione per coprire la quantità mancante.</span><span class="sxs-lookup"><span data-stu-id="3b290-112">If the initial available inventory is below zero, the planning system suggests an emergency supply order on the day before the planning period to cover the missing quantity.</span></span> <span data-ttu-id="3b290-113">Di conseguenza, il magazzino previsto e disponibile sarà sempre almeno uguale a zero quando inizia la pianificazione per il periodo futuro.</span><span class="sxs-lookup"><span data-stu-id="3b290-113">Consequently, the projected and available inventory will always be at least zero when planning for the future period begins.</span></span> <span data-ttu-id="3b290-114">Nella riga di pianificazione per questo ordine di approvvigionamento verrà visualizzata un'icona di avviso di emergenza. Verranno inoltre fornite informazioni aggiuntive su ricerca.</span><span class="sxs-lookup"><span data-stu-id="3b290-114">The planning line for this supply order will display an Emergency warning icon and additional information is provided upon lookup.</span></span>  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a><span data-ttu-id="3b290-115">I numeri seriali o di lotto e i collegamenti ordine su ordine sono esenti dalla zona bloccata</span><span class="sxs-lookup"><span data-stu-id="3b290-115">Serial/Lot Numbers and Order-to-Order Links are Exempt from the Frozen Zone</span></span>  
<span data-ttu-id="3b290-116">Se i numeri seriali o di lotto sono obbligatori o è presente un collegamento ordine su ordine, il sistema di pianificazione ignorerà la zona bloccata e includerà tali quantità che sono retrodatate dalla data iniziale e potenzialmente suggerirà delle azioni correttive se la domanda e l'approvvigionamento non sono sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="3b290-116">If serial/lot numbers are required or an order-to-order link exists, the planning system will disregard the frozen zone and incorporate such quantities that are back-dated from the starting date and potentially suggest corrective actions if demand and supply is not synchronized.</span></span> <span data-ttu-id="3b290-117">Il motivo economico di questo principio è che questo specifico set di domanda e approvvigionamento deve corrispondere per garantire che la domanda specifica sia soddisfatta completamente.</span><span class="sxs-lookup"><span data-stu-id="3b290-117">The business reason for this principle is that such specific demand-supply sets must match to ensure that this specific demand is fulfilled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3b290-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b290-118">See Also</span></span>  
<span data-ttu-id="3b290-119">[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="3b290-119">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="3b290-120">[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="3b290-120">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="3b290-121">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="3b290-121">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
