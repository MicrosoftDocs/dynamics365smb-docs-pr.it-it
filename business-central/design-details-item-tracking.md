---
title: 'Dettagli di progettazione: Tracciabilità articolo | Microsoft Docs'
description: Questo argomento fornisce una sintesi dei dettagli di progettazione per la tracciabilità articolo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6e5f20d2f450f3f544cc2f7023160e4e9babdf33
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772806"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="42910-103">Dettagli di progettazione: Tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="42910-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="42910-104">Quando il flusso delle merci nella catena di approvvigionamento odierna diventerà sempre più complesso, la capacità di tenere traccia degli articoli è sempre più importante per le società interessate.</span><span class="sxs-lookup"><span data-stu-id="42910-104">As the flow of goods in today's supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="42910-105">Il monitoraggio del flusso della transazione di un articolo è un requisito giuridico nell'attività di approvvigionamento medico e chimico, ma in altri settori è possibile che si desideri monitorare i prodotti con garanzie o date di scadenza per motivi di assistenza clienti.</span><span class="sxs-lookup"><span data-stu-id="42910-105">Monitoring an item's transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="42910-106">Un sistema di tracciabilità articolo deve offrire a una società la semplice gestione dei numeri seriali e di lotto, considerando ogni pezzo unico di merce: quando e dove è ricevuto, dove è archiviato, quando dove è stato venduto.</span><span class="sxs-lookup"><span data-stu-id="42910-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> <span data-ttu-id="42910-107">In [!INCLUDE[prod_short](includes/prod_short.md)] la copertura del fabbisogno aziendale è stata ampliata gradualmente e oggi offre una funzionalità a livello di applicazione e un solido nucleo a partire dal quale sviluppare le estensioni.</span><span class="sxs-lookup"><span data-stu-id="42910-107">[!INCLUDE[prod_short](includes/prod_short.md)] has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="42910-108">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="42910-108">In This Section</span></span>  
[<span data-ttu-id="42910-109">Dettagli di progettazione: Progettazione tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="42910-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="42910-110">Dettagli di progettazione: Struttura di registrazione di tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="42910-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="42910-111">Dettagli di progettazione: Movimenti di tracciabilità articolo storici e attivi</span><span class="sxs-lookup"><span data-stu-id="42910-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="42910-112">Dettagli di progettazione: Pagina righe tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="42910-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="42910-113">Dettagli di progettazione: Disponibilità tracciabilità articolo</span><span class="sxs-lookup"><span data-stu-id="42910-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="42910-114">Dettagli di progettazione: Tracciabilità articolo e pianificazione</span><span class="sxs-lookup"><span data-stu-id="42910-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="42910-115">Dettagli di progettazione: Tracciabilità articolo e impegni</span><span class="sxs-lookup"><span data-stu-id="42910-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="42910-116">Dettagli di progettazione: Tracciabilità articolo nel magazzino</span><span class="sxs-lookup"><span data-stu-id="42910-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)

## <a name="see-also"></a><span data-ttu-id="42910-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="42910-117">See Also</span></span>

[<span data-ttu-id="42910-118">Utilizzo dei numeri di serie, di lotto e di pacchetto</span><span class="sxs-lookup"><span data-stu-id="42910-118">Work with Serial, Lot, and Package Numbers</span></span>](inventory-how-work-item-tracking.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]