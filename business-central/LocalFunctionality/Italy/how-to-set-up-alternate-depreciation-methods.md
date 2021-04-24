---
title: Come impostare metodi di ammortamento alternativi
description: I metodi di ammortamento alternativi includono l'ammortamento anticipato, accelerato e ridotto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c3f68623add0ce7bfb2b79d2e969894815c4adee
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771444"
---
# <a name="set-up-alternate-depreciation-methods"></a><span data-ttu-id="38120-103">Impostare metodi di ammortamento alternativi</span><span class="sxs-lookup"><span data-stu-id="38120-103">Set Up Alternate Depreciation Methods</span></span>
<span data-ttu-id="38120-104">Di seguito sono indicati alcuni metodi di ammortamento alternativi:</span><span class="sxs-lookup"><span data-stu-id="38120-104">Alternate depreciation methods include the following:</span></span>  

- <span data-ttu-id="38120-105">Ammortamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="38120-105">Anticipated depreciation.</span></span>  
- <span data-ttu-id="38120-106">Ammortamento accelerato.</span><span class="sxs-lookup"><span data-stu-id="38120-106">Accelerated depreciation.</span></span>  
- <span data-ttu-id="38120-107">Ammortamento ridotto.</span><span class="sxs-lookup"><span data-stu-id="38120-107">Reduced depreciation.</span></span>  

<span data-ttu-id="38120-108">Per impostare questi metodi di ammortamento, è necessario creare tabelle di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="38120-108">You must create depreciation tables to set up these depreciation methods.</span></span>  

## <a name="to-set-up-alternate-depreciation-methods"></a><span data-ttu-id="38120-109">Per impostare metodi di ammortamento alternativi</span><span class="sxs-lookup"><span data-stu-id="38120-109">To set up alternate depreciation methods</span></span>  

1.  <span data-ttu-id="38120-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Tabelle ammortamento** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="38120-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Depreciation Tables**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="38120-111">Nella pagina **Lista tabelle ammortamento** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="38120-111">On the **Depreciation Table List** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="38120-112">Nella Scheda Dettaglio **Generale** compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="38120-112">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="38120-113">Campo</span><span class="sxs-lookup"><span data-stu-id="38120-113">Field</span></span>|<span data-ttu-id="38120-114">Description</span><span class="sxs-lookup"><span data-stu-id="38120-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="38120-115">**Codice**</span><span class="sxs-lookup"><span data-stu-id="38120-115">**Code**</span></span>|<span data-ttu-id="38120-116">Codice per la tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="38120-116">The code for the depreciation table.</span></span>|  
    |<span data-ttu-id="38120-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="38120-117">**Description**</span></span>|<span data-ttu-id="38120-118">Descrizione per la tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="38120-118">The description for the depreciation table.</span></span>|  
    |<span data-ttu-id="38120-119">**Durata periodo**</span><span class="sxs-lookup"><span data-stu-id="38120-119">**Period Length**</span></span>|<span data-ttu-id="38120-120">Durata del periodo a cui si applicherà ogni riga della tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="38120-120">The length of the period to which each of the depreciation table lines will apply.</span></span>|  
    |<span data-ttu-id="38120-121">**Nr. totale di unità**</span><span class="sxs-lookup"><span data-stu-id="38120-121">**Total No. of Units**</span></span>|<span data-ttu-id="38120-122">Numero totale di unità che si prevede che il cespite produrrà nella sua durata.</span><span class="sxs-lookup"><span data-stu-id="38120-122">The total number of units that the asset is expected to produce in its lifetime.</span></span>|  

4.  <span data-ttu-id="38120-123">Nella Scheda dettaglio **Righe** compilare i campi come descritto nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="38120-123">On the **Lines** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="38120-124">Campo</span><span class="sxs-lookup"><span data-stu-id="38120-124">Field</span></span>|<span data-ttu-id="38120-125">Description</span><span class="sxs-lookup"><span data-stu-id="38120-125">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="38120-126">**% ammortamento periodo**</span><span class="sxs-lookup"><span data-stu-id="38120-126">**Period Depreciation %**</span></span>|<span data-ttu-id="38120-127">Percentuale di ammortamento da applicare al periodo.</span><span class="sxs-lookup"><span data-stu-id="38120-127">The depreciation percentage to apply to the period.</span></span>|  
    |<span data-ttu-id="38120-128">**Nr. unità nel periodo**</span><span class="sxs-lookup"><span data-stu-id="38120-128">**No. of Units in Period**</span></span>|<span data-ttu-id="38120-129">Numero di unità prodotte dal cespite a cui si applica la tabella di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="38120-129">The number of units produced by the asset to which this depreciation table applies.</span></span>|  
    |<span data-ttu-id="38120-130">**% anticipata**</span><span class="sxs-lookup"><span data-stu-id="38120-130">**Anticipated %**</span></span>|<span data-ttu-id="38120-131">Percentuale di ammortamento anticipata.</span><span class="sxs-lookup"><span data-stu-id="38120-131">The anticipated depreciation percentage.</span></span>|  
    |<span data-ttu-id="38120-132">**% accelerata/ridotta**</span><span class="sxs-lookup"><span data-stu-id="38120-132">**Accelerated/Reduced %**</span></span>|<span data-ttu-id="38120-133">Percentuale di ammortamento effettiva.</span><span class="sxs-lookup"><span data-stu-id="38120-133">The actual depreciation percentage.</span></span>|  

5.  <span data-ttu-id="38120-134">Nel campo **% totale ammortamento** immettere la percentuale totale di ammortamento.</span><span class="sxs-lookup"><span data-stu-id="38120-134">In the **Total Depreciation %** field, enter the total depreciation percentage.</span></span>  
6.  <span data-ttu-id="38120-135">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="38120-135">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="38120-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38120-136">See Also</span></span>  
 <span data-ttu-id="38120-137">[Impostare l'ammortamento dei cespiti](../../fa-how-setup-depreciation.md) </span><span class="sxs-lookup"><span data-stu-id="38120-137">[Set Up Fixed Asset Depreciation](../../fa-how-setup-depreciation.md) </span></span>  
 <span data-ttu-id="38120-138">[Cespiti italiani](italian-fixed-assets.md) </span><span class="sxs-lookup"><span data-stu-id="38120-138">[Italian Fixed Assets](italian-fixed-assets.md) </span></span>  
 <span data-ttu-id="38120-139">[Creare più schede cespite](how-to-create-multiple-fixed-asset-cards.md) </span><span class="sxs-lookup"><span data-stu-id="38120-139">[Create Multiple Fixed Asset Cards](how-to-create-multiple-fixed-asset-cards.md) </span></span>  
 <span data-ttu-id="38120-140">[Impostazione dell'ammortamento compresso dei cespiti](how-to-set-up-compressed-depreciation-of-fixed-assets.md) </span><span class="sxs-lookup"><span data-stu-id="38120-140">[Set Up Compressed Depreciation of Fixed Assets](how-to-set-up-compressed-depreciation-of-fixed-assets.md) </span></span>  
 [<span data-ttu-id="38120-141">Stampare report dei registri dei beni ammortizzabili</span><span class="sxs-lookup"><span data-stu-id="38120-141">Print Depreciation Book Reports</span></span>](how-to-print-depreciation-book-reports.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]