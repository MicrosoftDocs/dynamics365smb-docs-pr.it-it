---
title: Sintesi movimenti set di dimensioni | Microsoft Docs
description: In questo argomento viene descritto il modo in cui i movimenti set di dimensioni vengono memorizzati e registrati in [!INCLUDE[d365fin](includes/d365fin_md.md)].
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53c85ecbb42db92e95921203d24781bcb82f942d
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="a3b01-103">Sintesi movimenti set di dimensioni</span><span class="sxs-lookup"><span data-stu-id="a3b01-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="a3b01-104">In questo argomento viene descritto il modo in cui i movimenti set di dimensioni vengono memorizzati e registrati in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a3b01-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="a3b01-105">Set di dimensioni</span><span class="sxs-lookup"><span data-stu-id="a3b01-105">Dimension Sets</span></span>  
<span data-ttu-id="a3b01-106">Un set di dimensioni è una combinazione univoca di valori dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a3b01-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="a3b01-107">Viene archiviato come movimenti set di dimensioni nel database.</span><span class="sxs-lookup"><span data-stu-id="a3b01-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="a3b01-108">Ogni movimento set di dimensioni rappresenta un valore dimensioni singolo.</span><span class="sxs-lookup"><span data-stu-id="a3b01-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="a3b01-109">Il set di dimensioni è identificato da un ID set di dimensioni comune assegnato a ogni movimento set di dimensioni che appartiene al set di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a3b01-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="a3b01-110">Nel seguente esempio viene mostrato un set di dimensioni in cui sono presenti tre relativi movimenti.</span><span class="sxs-lookup"><span data-stu-id="a3b01-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="a3b01-111">Il set di dimensioni è identificato da un ID set di dimensioni, vale a dire 108.</span><span class="sxs-lookup"><span data-stu-id="a3b01-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="a3b01-112">ID set di dimensioni</span><span class="sxs-lookup"><span data-stu-id="a3b01-112">Dimension Set ID</span></span>|<span data-ttu-id="a3b01-113">Codice Dimensione:</span><span class="sxs-lookup"><span data-stu-id="a3b01-113">Dimension Code</span></span>|<span data-ttu-id="a3b01-114">Codice Valore Dimensioni:</span><span class="sxs-lookup"><span data-stu-id="a3b01-114">Dimension Value Code</span></span>|<span data-ttu-id="a3b01-115">Nome valore dimensioni</span><span class="sxs-lookup"><span data-stu-id="a3b01-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="a3b01-116">108</span><span class="sxs-lookup"><span data-stu-id="a3b01-116">108</span></span>|<span data-ttu-id="a3b01-117">AREA</span><span class="sxs-lookup"><span data-stu-id="a3b01-117">AREA</span></span>|<span data-ttu-id="a3b01-118">70</span><span class="sxs-lookup"><span data-stu-id="a3b01-118">70</span></span>|<span data-ttu-id="a3b01-119">Nord America</span><span class="sxs-lookup"><span data-stu-id="a3b01-119">America North</span></span>|  
|<span data-ttu-id="a3b01-120">108</span><span class="sxs-lookup"><span data-stu-id="a3b01-120">108</span></span>|<span data-ttu-id="a3b01-121">GRUPPOBUSINES</span><span class="sxs-lookup"><span data-stu-id="a3b01-121">BUSINESSGROUP</span></span>|<span data-ttu-id="a3b01-122">HOME</span><span class="sxs-lookup"><span data-stu-id="a3b01-122">HOME</span></span>|<span data-ttu-id="a3b01-123">Home</span><span class="sxs-lookup"><span data-stu-id="a3b01-123">Home</span></span>|  
|<span data-ttu-id="a3b01-124">108</span><span class="sxs-lookup"><span data-stu-id="a3b01-124">108</span></span>|<span data-ttu-id="a3b01-125">REPARTO</span><span class="sxs-lookup"><span data-stu-id="a3b01-125">DEPARTMENT</span></span>|<span data-ttu-id="a3b01-126">VENDITE</span><span class="sxs-lookup"><span data-stu-id="a3b01-126">SALES</span></span>|<span data-ttu-id="a3b01-127">Vendite</span><span class="sxs-lookup"><span data-stu-id="a3b01-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="a3b01-128">Movimenti set di dimensioni</span><span class="sxs-lookup"><span data-stu-id="a3b01-128">Dimension Set Entries</span></span>  
<span data-ttu-id="a3b01-129">I set di dimensioni vengono archiviati nella tabella **Movimento set di dimensioni** come movimenti di set di dimensioni con lo stesso ID set di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a3b01-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="a3b01-130">![Sintesi movimento dimensione](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="a3b01-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="a3b01-131">Quando si crea una nuova riga di registrazione, testata del documento o riga documento, è possibile specificare una combinazione di valori dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a3b01-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="a3b01-132">Anziché archiviare esplicitamente ogni valore dimensioni nel database, viene assegnato un ID set di dimensioni alla riga di registrazione, alla testata del documento o alla riga del documento per specificare il set di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a3b01-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="a3b01-133">Quando si modifica e si chiude la finestra **Modifica movimenti set di dimensioni** , viene eseguito un controllo per verificare se la combinazione dei valori dimensioni esiste come set di dimensioni nella tabella.</span><span class="sxs-lookup"><span data-stu-id="a3b01-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="a3b01-134">Se la combinazione si verifica nella tabella, l'ID set di dimensioni corrispondente viene assegnato alla riga di registrazione, alla testata del documento o alla riga del documento.</span><span class="sxs-lookup"><span data-stu-id="a3b01-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="a3b01-135">In caso contrario, un nuovo set di dimensioni viene aggiunto alla tabella e il nuovo ID set di dimensioni viene assegnato alla riga di registrazione, alla testata del documento o alla riga del documento.</span><span class="sxs-lookup"><span data-stu-id="a3b01-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="a3b01-136">Miglioramento delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="a3b01-136">Performance Improvement</span></span>  
<span data-ttu-id="a3b01-137">Archiviando i set di dimensioni una volta nel database, lo spazio di quest'ultimo viene mantenuto e le prestazioni globali vengono migliorate.</span><span class="sxs-lookup"><span data-stu-id="a3b01-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3b01-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3b01-138">See Also</span></span>  
<span data-ttu-id="a3b01-139">[Dettagli di progettazione: Ricerca delle combinazioni di dimensione](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="a3b01-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="a3b01-140">[Dettagli di progettazione: Struttura della tabella](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="a3b01-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="a3b01-141">[Dettagli di progettazione: Gestione dimensioni della codeunit 408](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="a3b01-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="a3b01-142">[Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="a3b01-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="a3b01-143">Dettagli di progettazione: Movimenti set di dimensioni</span><span class="sxs-lookup"><span data-stu-id="a3b01-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

