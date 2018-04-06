---
title: 'Dettagli di progettazione: Pianificazione approvvigionamento | Microsoft Docs'
description: "Questo argomento fornisce una sintesi dei concetti e dei principi utilizzati nelle funzionalità di pianificazione degli approvvigionamenti in Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b8e664be23db7be871e1775a8b98b006218b7404
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-supply-planning"></a><span data-ttu-id="f19c6-103">Dettagli di progettazione: Pianificazione approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="f19c6-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="f19c6-104">In questa documentazione sono fornite informazioni tecniche dettagliate sui concetti e sui principi utilizzati nelle funzionalità di pianificazione degli approvvigionamenti in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f19c6-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="f19c6-105">Viene descritto il funzionamento del sistema di pianificazione e viene spiegato come rettificare gli algoritmi per soddisfare i requisiti di pianificazione in vari ambienti.</span><span class="sxs-lookup"><span data-stu-id="f19c6-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="f19c6-106">Vengono innanzitutto presentati i concetti di soluzione centrale e viene descritta la logica del meccanismo centrale, il bilanciamento dell'approvvigionamento, prima di spiegare la modalità di esecuzione della pianificazione del magazzino con l'utilizzo dei metodi di riordino.</span><span class="sxs-lookup"><span data-stu-id="f19c6-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="f19c6-107">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="f19c6-107">In This Section</span></span>  
[<span data-ttu-id="f19c6-108">Dettagli di progettazione: Concetti centrali del sistema di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f19c6-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="f19c6-109">Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni</span><span class="sxs-lookup"><span data-stu-id="f19c6-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="f19c6-110">Dettagli di progettazione: Bilanciamento domanda e approvvigionamento</span><span class="sxs-lookup"><span data-stu-id="f19c6-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="f19c6-111">Dettagli di progettazione: Gestione dei metodi di riordino</span><span class="sxs-lookup"><span data-stu-id="f19c6-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="f19c6-112">Dettagli di progettazione: Parametri di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f19c6-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="f19c6-113">Dettagli di progettazione: Tabella Assegnazione pianificazione</span><span class="sxs-lookup"><span data-stu-id="f19c6-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="f19c6-114">Dettagli di progettazione: Domanda nell'ubicazione Vuota</span><span class="sxs-lookup"><span data-stu-id="f19c6-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="f19c6-115">Dettagli di progettazione: Trasferimenti nella pianificazione</span><span class="sxs-lookup"><span data-stu-id="f19c6-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)

