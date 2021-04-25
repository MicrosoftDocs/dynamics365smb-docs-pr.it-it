---
title: 'Procedura: Abilitare il prelievo in base al metodo FEFO | Documenti Microsoft'
description: FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784069"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="085d3-103">Abilitare il prelievo di articoli tramite il metodo FEFO</span><span class="sxs-lookup"><span data-stu-id="085d3-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="085d3-104">FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.</span><span class="sxs-lookup"><span data-stu-id="085d3-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="085d3-105">La funzionalità può essere utilizzata solo quando vengono soddisfatti i seguenti criteri:</span><span class="sxs-lookup"><span data-stu-id="085d3-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="085d3-106">L'articolo deve avere un numero seriale o di lotto.</span><span class="sxs-lookup"><span data-stu-id="085d3-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="085d3-107">Nel setup del codice di tracciabilità dell'articolo è necessario selezionare il campo **Tracciab. NS in warehouse** o **Tracciab. lotto in warehouse**.</span><span class="sxs-lookup"><span data-stu-id="085d3-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="085d3-108">L'articolo deve essere registrato in magazzino con una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="085d3-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="085d3-109">Sul posto, i toggle **Richiesto prelievo**, **Prelievo in base a FEFO** e **Collocazione obbligatoria** devono essere attivate.</span><span class="sxs-lookup"><span data-stu-id="085d3-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="085d3-110">Una volta soddisfatti tutti i criteri, gli articoli con numeri seriali/di lotto da prelevare verranno ordinati con i più vecchi per primi in tutti gli prelievi e tutte le movimentazioni, ad eccezione degli articoli che utilizzano la tracciabilità NS specifico o lotto specifico.</span><span class="sxs-lookup"><span data-stu-id="085d3-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="085d3-111">Se alcuni articoli con numeri seriali o di lotto utilizzano la tracciabilità specifica, questi vengono rispettati per primi e quindi vengono elencati i rimanenti numeri seriali/di lotto in base al metodo FEFO.</span><span class="sxs-lookup"><span data-stu-id="085d3-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="085d3-112">Se due articoli con numeri seriali o di lotto hanno la stessa data di scadenza, viene selezionato automaticamente quello con il numero di lotto o seriale inferiore.</span><span class="sxs-lookup"><span data-stu-id="085d3-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="085d3-113">Quando si prelevano articoli con numeri di serie o di lotto in ubicazioni impostate per stoccaggi e prelievi guidati, solo le quantità nelle collocazioni di tipo *Prelievo* vengono prelevate in base al metodo FEFO.</span><span class="sxs-lookup"><span data-stu-id="085d3-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="085d3-114">Per abilitare le movimentazioni in base al metodo FEFO, lasciare il campo **Dal codice collocazione** vuoto nella pagina **Movimento di magazzino** o nelle pagine **Movimento worksheet**.</span><span class="sxs-lookup"><span data-stu-id="085d3-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="085d3-115">Se il campo **Registrazione scadenza vincolante** è selezionato in **Scheda cod. tracciab. articolo**, nel prelievo verranno inclusi solo gli articoli non scaduti e le righe verranno ordinate secondo il principio FEFO.</span><span class="sxs-lookup"><span data-stu-id="085d3-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="085d3-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="085d3-116">See Also</span></span>  
<span data-ttu-id="085d3-117">[Prelievo di articoli](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="085d3-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="085d3-118">[Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="085d3-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="085d3-119">[Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="085d3-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="085d3-120">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="085d3-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="085d3-121">Magazzino</span><span class="sxs-lookup"><span data-stu-id="085d3-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="085d3-122">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="085d3-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]