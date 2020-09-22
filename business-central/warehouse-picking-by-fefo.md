---
title: 'Procedura: Abilitare il prelievo in base al metodo FEFO | Documenti Microsoft'
description: FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 721b980f8c52e07356fe47bc69aaec90c7fc185f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784923"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="51fea-103">Abilitare il prelievo di articoli tramite il metodo FEFO</span><span class="sxs-lookup"><span data-stu-id="51fea-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="51fea-104">FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.</span><span class="sxs-lookup"><span data-stu-id="51fea-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="51fea-105">La funzionalità può essere utilizzata solo quando vengono soddisfatti i seguenti criteri:</span><span class="sxs-lookup"><span data-stu-id="51fea-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="51fea-106">L'articolo deve avere un numero seriale o di lotto.</span><span class="sxs-lookup"><span data-stu-id="51fea-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="51fea-107">Nel setup del codice di tracciabilità dell'articolo è necessario selezionare il campo **Tracciab. NS in warehouse** o **Tracciab. lotto in warehouse**.</span><span class="sxs-lookup"><span data-stu-id="51fea-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="51fea-108">L'articolo deve essere registrato in magazzino con una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="51fea-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="51fea-109">Nella scheda Ubicazione, la casella di controllo **Richiesto prelievo** deve essere selezionata.</span><span class="sxs-lookup"><span data-stu-id="51fea-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="51fea-110">Nella scheda ubicazione è necessario selezionare la casella di controllo **Prelievo in base a FEFO**.</span><span class="sxs-lookup"><span data-stu-id="51fea-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="51fea-111">Nella scheda Ubicazione, la casella di controllo **Collocazione obbligatoria** deve essere selezionata.</span><span class="sxs-lookup"><span data-stu-id="51fea-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="51fea-112">Una volta soddisfatti tutti i criteri, gli articoli con numeri seriali/di lotto da prelevare verranno ordinati con i più vecchi per primi in tutti gli prelievi e tutte le movimentazioni, ad eccezione degli articoli che utilizzano la tracciabilità NS specifico o lotto specifico.</span><span class="sxs-lookup"><span data-stu-id="51fea-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="51fea-113">Se alcuni articoli con numeri seriali/di lotto utilizzano la tracciabilità specifica, questi vengono rispettati per primi e quindi vengono elencati i rimanenti numeri seriali/di lotto in base al metodo FEFO.</span><span class="sxs-lookup"><span data-stu-id="51fea-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="51fea-114">Se due articoli con numeri seriali o di lotto hanno la stessa data di scadenza, viene selezionato automaticamente quello con il numero di lotto o seriale inferiore.</span><span class="sxs-lookup"><span data-stu-id="51fea-114">If two serial/lot-numbered items have the same expiration date, then application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="51fea-115">Quando si prelevano articoli con numeri di serie o di lotto in ubicazioni impostate per stoccaggi e prelievi guidati, solo le quantità nelle collocazioni di tipo *Prelievo* vengono prelevate in base al metodo FEFO.</span><span class="sxs-lookup"><span data-stu-id="51fea-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="51fea-116">Per abilitare le movimentazioni in base al metodo FEFO, nella pagina **Movimento di magazzino** o **Prospetto movimentazioni**, è necessario lasciare vuoto il campo **Dal codice collocazione**.</span><span class="sxs-lookup"><span data-stu-id="51fea-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="51fea-117">Se il campo **Registrazione scadenza vincolante** è selezionato, solo gli articoli che non sono scaduti verranno inclusi nel prelievo.</span><span class="sxs-lookup"><span data-stu-id="51fea-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="51fea-118">Ciò si applica anche se non viene utilizzata l'opzione Prelievo in base a FEFO.</span><span class="sxs-lookup"><span data-stu-id="51fea-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="51fea-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51fea-119">See Also</span></span>  
<span data-ttu-id="51fea-120">[Prelievo di articoli](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="51fea-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="51fea-121">[Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="51fea-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="51fea-122">[Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="51fea-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="51fea-123">Dettagli di progettazione: Gestione warehouse</span><span class="sxs-lookup"><span data-stu-id="51fea-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="51fea-124">Magazzino</span><span class="sxs-lookup"><span data-stu-id="51fea-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="51fea-125">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="51fea-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
