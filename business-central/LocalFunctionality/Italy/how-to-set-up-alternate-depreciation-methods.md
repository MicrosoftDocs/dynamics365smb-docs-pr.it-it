---
title: Come impostare metodi di ammortamento alternativi
description: I metodi di ammortamento alternativi includono l'ammortamento anticipato, accelerato e ridotto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 542ea4a52f5a8269afbebd30e51bb1489b0a2257
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677061"
---
# <a name="set-up-alternate-depreciation-methods"></a><span data-ttu-id="92ded-103">Impostare metodi di ammortamento alternativi</span><span class="sxs-lookup"><span data-stu-id="92ded-103">Set Up Alternate Depreciation Methods</span></span>
<span data-ttu-id="92ded-104">Di seguito sono indicati alcuni metodi di ammortamento alternativi:</span><span class="sxs-lookup"><span data-stu-id="92ded-104">Alternate depreciation methods include the following:</span></span>  

- <span data-ttu-id="92ded-105">Ammortamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="92ded-105">Anticipated depreciation.</span></span>  
- <span data-ttu-id="92ded-106">Ammortamento accelerato.</span><span class="sxs-lookup"><span data-stu-id="92ded-106">Accelerated depreciation.</span></span>  
- <span data-ttu-id="92ded-107">Ammortamento ridotto.</span><span class="sxs-lookup"><span data-stu-id="92ded-107">Reduced depreciation.</span></span>  

<span data-ttu-id="92ded-108">Per impostare questi metodi di ammortamento, è necessario creare tabelle di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="92ded-108">You must create depreciation tables to set up these depreciation methods.</span></span>  

## <a name="to-set-up-alternate-depreciation-methods"></a><span data-ttu-id="92ded-109">Per impostare metodi di ammortamento alternativi</span><span class="sxs-lookup"><span data-stu-id="92ded-109">To set up alternate depreciation methods</span></span>  

1.  <span data-ttu-id="92ded-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Tabelle ammortamento** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="92ded-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Depreciation Tables**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="92ded-111">Nella pagina **Lista tabelle ammortamento** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="92ded-111">On the **Depreciation Table List** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="92ded-112">Nella Scheda Dettaglio **Generale** compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="92ded-112">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="92ded-113">Campo</span><span class="sxs-lookup"><span data-stu-id="92ded-113">Field</span></span>|<span data-ttu-id="92ded-114">Description</span><span class="sxs-lookup"><span data-stu-id="92ded-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="92ded-115">**Codice**</span><span class="sxs-lookup"><span data-stu-id="92ded-115">**Code**</span></span>|<span data-ttu-id="92ded-116">Codice per la tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="92ded-116">The code for the depreciation table.</span></span>|  
    |<span data-ttu-id="92ded-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="92ded-117">**Description**</span></span>|<span data-ttu-id="92ded-118">Descrizione per la tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="92ded-118">The description for the depreciation table.</span></span>|  
    |<span data-ttu-id="92ded-119">**Durata periodo**</span><span class="sxs-lookup"><span data-stu-id="92ded-119">**Period Length**</span></span>|<span data-ttu-id="92ded-120">Durata del periodo a cui si applicherà ogni riga della tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="92ded-120">The length of the period to which each of the depreciation table lines will apply.</span></span>|  
    |<span data-ttu-id="92ded-121">**Nr. totale di unità**</span><span class="sxs-lookup"><span data-stu-id="92ded-121">**Total No. of Units**</span></span>|<span data-ttu-id="92ded-122">Numero totale di unità che si prevede che il cespite produrrà nella sua durata.</span><span class="sxs-lookup"><span data-stu-id="92ded-122">The total number of units that the asset is expected to produce in its lifetime.</span></span>|  

4.  <span data-ttu-id="92ded-123">Nella Scheda dettaglio **Righe** compilare i campi come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="92ded-123">On the **Lines** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="92ded-124">Campo</span><span class="sxs-lookup"><span data-stu-id="92ded-124">Field</span></span>|<span data-ttu-id="92ded-125">Description</span><span class="sxs-lookup"><span data-stu-id="92ded-125">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="92ded-126">**% ammortamento periodo**</span><span class="sxs-lookup"><span data-stu-id="92ded-126">**Period Depreciation %**</span></span>|<span data-ttu-id="92ded-127">Percentuale di ammortamento da applicare al periodo.</span><span class="sxs-lookup"><span data-stu-id="92ded-127">The depreciation percentage to apply to the period.</span></span>|  
    |<span data-ttu-id="92ded-128">**Nr. unità nel periodo**</span><span class="sxs-lookup"><span data-stu-id="92ded-128">**No. of Units in Period**</span></span>|<span data-ttu-id="92ded-129">Numero di unità prodotte dal cespite a cui si applica la tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="92ded-129">The number of units produced by the asset to which this depreciation table applies.</span></span>|  
    |<span data-ttu-id="92ded-130">**% anticipata**</span><span class="sxs-lookup"><span data-stu-id="92ded-130">**Anticipated %**</span></span>|<span data-ttu-id="92ded-131">Percentuale di ammortamento anticipata.</span><span class="sxs-lookup"><span data-stu-id="92ded-131">The anticipated depreciation percentage.</span></span>|  
    |<span data-ttu-id="92ded-132">**% accelerata/ridotta**</span><span class="sxs-lookup"><span data-stu-id="92ded-132">**Accelerated/Reduced %**</span></span>|<span data-ttu-id="92ded-133">Percentuale di ammortamento effettiva.</span><span class="sxs-lookup"><span data-stu-id="92ded-133">The actual depreciation percentage.</span></span>|  

5.  <span data-ttu-id="92ded-134">Nel campo **% totale ammortamento** immettere la percentuale totale di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="92ded-134">In the **Total Depreciation %** field, enter the total depreciation percentage.</span></span>  
6.  <span data-ttu-id="92ded-135">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="92ded-135">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="92ded-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92ded-136">See Also</span></span>  
 <span data-ttu-id="92ded-137">[Impostare l'ammortamento dei cespiti](../../fa-how-setup-depreciation.md) </span><span class="sxs-lookup"><span data-stu-id="92ded-137">[Set Up Fixed Asset Depreciation](../../fa-how-setup-depreciation.md) </span></span>  
 <span data-ttu-id="92ded-138">[Cespiti italiani](italian-fixed-assets.md) </span><span class="sxs-lookup"><span data-stu-id="92ded-138">[Italian Fixed Assets](italian-fixed-assets.md) </span></span>  
 <span data-ttu-id="92ded-139">[Creare più schede cespite](how-to-create-multiple-fixed-asset-cards.md) </span><span class="sxs-lookup"><span data-stu-id="92ded-139">[Create Multiple Fixed Asset Cards](how-to-create-multiple-fixed-asset-cards.md) </span></span>  
 <span data-ttu-id="92ded-140">[Impostazione dell'ammortamento compresso dei cespiti](how-to-set-up-compressed-depreciation-of-fixed-assets.md) </span><span class="sxs-lookup"><span data-stu-id="92ded-140">[Set Up Compressed Depreciation of Fixed Assets](how-to-set-up-compressed-depreciation-of-fixed-assets.md) </span></span>  
 [<span data-ttu-id="92ded-141">Stampare report dei registri dei beni ammortizzabili</span><span class="sxs-lookup"><span data-stu-id="92ded-141">Print Depreciation Book Reports</span></span>](how-to-print-depreciation-book-reports.md)
