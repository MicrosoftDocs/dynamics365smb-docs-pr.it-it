---
title: 'Dettagli di progettazione: Gestione dimensioni della codeunit 408 | Microsoft Docs'
description: "La gestione delle dimensioni della Codeunit 408 è una libreria di funzione che gestisce le attività comuni correlate alle dimensioni, ad esempio copia da una tabella a un'altra oppure da un documento a un altro."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a811c565a8eb0ce774d35d15776e65b6dce6a31a
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="6ed77-103">Dettagli di progettazione: Gestione dimensioni della codeunit 408</span><span class="sxs-lookup"><span data-stu-id="6ed77-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="6ed77-104">La gestione delle dimensioni della Codeunit 408 è una libreria di funzione che gestisce le attività comuni correlate alle dimensioni, ad esempio copia da una tabella a un'altra oppure da un documento a un altro.</span><span class="sxs-lookup"><span data-stu-id="6ed77-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="6ed77-105">In questo argomento sono elencate le funzioni che vengono modificate in Microsoft Dynamics NAV 2013 R2 e vengono specificate le azioni da intraprendere per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="6ed77-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="6ed77-106">Numerose funzioni sono state eliminate in quanto non è necessario eseguire copie tra le tabelle delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6ed77-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="6ed77-107">Funzioni modificate</span><span class="sxs-lookup"><span data-stu-id="6ed77-107">Modified Functions</span></span>  

|<span data-ttu-id="6ed77-108">Nome funzione</span><span class="sxs-lookup"><span data-stu-id="6ed77-108">Function Name</span></span>|<span data-ttu-id="6ed77-109">Descrizione modifica</span><span class="sxs-lookup"><span data-stu-id="6ed77-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="6ed77-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="6ed77-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="6ed77-111">Nuova funzione che sostituisce le altre funzioni di controllo e accetta un ID di set di dimensioni come argomento anziché una tabella delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6ed77-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="6ed77-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="6ed77-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="6ed77-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="6ed77-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="6ed77-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="6ed77-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="6ed77-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="6ed77-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="6ed77-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="6ed77-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="6ed77-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="6ed77-117">CheckDimValueComb</span></span>|<span data-ttu-id="6ed77-118">Elimina.</span><span class="sxs-lookup"><span data-stu-id="6ed77-118">Delete.</span></span> <span data-ttu-id="6ed77-119">Tutti gli utilizzi devono essere modificati in CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="6ed77-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="6ed77-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-120">GetDefaultDim</span></span>|<span data-ttu-id="6ed77-121">Modificare per restituire un ID di set di dimensioni sotto forma di valore intero anziché un set di record.</span><span class="sxs-lookup"><span data-stu-id="6ed77-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="6ed77-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="6ed77-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="6ed77-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="6ed77-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="6ed77-126">Modificare per utilizzare DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="6ed77-127">Funzioni eliminate</span><span class="sxs-lookup"><span data-stu-id="6ed77-127">Deleted Functions</span></span>  
 <span data-ttu-id="6ed77-128">Le funzioni che vengono eliminate dalla codeunit 408 in relazione alla funzionalità Movimenti set di dimensioni sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="6ed77-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="6ed77-129">Durante l'aggiornamento del codice dell'applicazione da Microsoft Dynamics NAV 2009 o versioni precedenti a Microsoft Dynamics NAV 2016, le seguenti funzioni non sono disponibili in Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="6ed77-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="6ed77-130">Se si dispone di personalizzazioni in cui vengono utilizzate una o più funzioni, è necessario aggiornare il codice di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="6ed77-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="6ed77-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="6ed77-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="6ed77-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="6ed77-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="6ed77-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-136">InsertDocDim</span></span>  

 <span data-ttu-id="6ed77-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="6ed77-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="6ed77-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="6ed77-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="6ed77-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-141">InsertServContractDim</span></span>  

 <span data-ttu-id="6ed77-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="6ed77-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="6ed77-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="6ed77-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-144">GetDocDim</span></span>  

 <span data-ttu-id="6ed77-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-145">GetProdDocDim</span></span>  

 <span data-ttu-id="6ed77-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="6ed77-146">TypeToTableID1</span></span>  

 <span data-ttu-id="6ed77-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="6ed77-147">TypeToTableID2</span></span>  

 <span data-ttu-id="6ed77-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="6ed77-148">TypeToTableID3</span></span>  

 <span data-ttu-id="6ed77-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="6ed77-149">TypeToTableID4</span></span>  

 <span data-ttu-id="6ed77-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="6ed77-150">TypeToTableID5</span></span>  

 <span data-ttu-id="6ed77-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-152">DeleteDocDim</span></span>  

 <span data-ttu-id="6ed77-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="6ed77-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="6ed77-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="6ed77-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="6ed77-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="6ed77-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-160">ShowDocDim</span></span>  

 <span data-ttu-id="6ed77-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-161">SaveDocDim</span></span>  

 <span data-ttu-id="6ed77-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="6ed77-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="6ed77-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-164">ShowTempDim</span></span>  

 <span data-ttu-id="6ed77-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-165">SaveTempDim</span></span>  

 <span data-ttu-id="6ed77-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="6ed77-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="6ed77-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-168">SaveServContractDim</span></span>  

 <span data-ttu-id="6ed77-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="6ed77-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="6ed77-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="6ed77-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="6ed77-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="6ed77-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="6ed77-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="6ed77-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="6ed77-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="6ed77-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="6ed77-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="6ed77-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="6ed77-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="6ed77-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="6ed77-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="6ed77-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="6ed77-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="6ed77-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="6ed77-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="6ed77-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="6ed77-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="6ed77-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="6ed77-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="6ed77-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="6ed77-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="6ed77-198">TestDimValue</span></span>  

 <span data-ttu-id="6ed77-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="6ed77-199">TestNewDimValue</span></span>  

 <span data-ttu-id="6ed77-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="6ed77-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="6ed77-201">(Eliminare perché la Tabella di ItemBudgetDim viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="6ed77-201">(Delete because the ItemBudgetDim Table is deleted.</span></span>  

 <span data-ttu-id="6ed77-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-202">GetServContractDim</span></span>  

 <span data-ttu-id="6ed77-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="6ed77-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="6ed77-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="6ed77-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="6ed77-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="6ed77-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="6ed77-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="6ed77-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ed77-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ed77-207">See Also</span></span>
 <span data-ttu-id="6ed77-208">[Dettagli di progettazione: Movimenti set di dimensioni](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="6ed77-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="6ed77-209">[Dettagli di progettazione: Sintesi movimenti set di dimensioni](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="6ed77-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="6ed77-210">[Dettagli di progettazione: Ricerca delle combinazioni di dimensione](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="6ed77-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="6ed77-211">[Dettagli di progettazione: Struttura della tabella](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="6ed77-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="6ed77-212">Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche</span><span class="sxs-lookup"><span data-stu-id="6ed77-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

