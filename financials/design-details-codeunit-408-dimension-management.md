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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 32f67c058570f03d4aa1c84d9bb32289b1f07bec
ms.contentlocale: it-it
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="3fe03-103">Dettagli di progettazione: Gestione dimensioni della codeunit 408</span><span class="sxs-lookup"><span data-stu-id="3fe03-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="3fe03-104">La gestione delle dimensioni della Codeunit 408 è una libreria di funzione che gestisce le attività comuni correlate alle dimensioni, ad esempio copia da una tabella a un'altra oppure da un documento a un altro.</span><span class="sxs-lookup"><span data-stu-id="3fe03-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="3fe03-105">In questo argomento sono elencate le funzioni che vengono modificate in Microsoft Dynamics NAV 2013 R2 e vengono specificate le azioni da intraprendere per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="3fe03-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="3fe03-106">Numerose funzioni sono state eliminate in quanto non è necessario eseguire copie tra le tabelle delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="3fe03-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="3fe03-107">Funzioni modificate</span><span class="sxs-lookup"><span data-stu-id="3fe03-107">Modified Functions</span></span>  

|<span data-ttu-id="3fe03-108">Nome funzione</span><span class="sxs-lookup"><span data-stu-id="3fe03-108">Function Name</span></span>|<span data-ttu-id="3fe03-109">Descrizione modifica</span><span class="sxs-lookup"><span data-stu-id="3fe03-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="3fe03-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="3fe03-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="3fe03-111">Nuova funzione che sostituisce le altre funzioni di controllo e accetta un ID di set di dimensioni come argomento anziché una tabella delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="3fe03-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="3fe03-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="3fe03-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="3fe03-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="3fe03-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="3fe03-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="3fe03-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="3fe03-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="3fe03-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="3fe03-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="3fe03-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="3fe03-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="3fe03-117">CheckDimValueComb</span></span>|<span data-ttu-id="3fe03-118">Elimina.</span><span class="sxs-lookup"><span data-stu-id="3fe03-118">Delete.</span></span> <span data-ttu-id="3fe03-119">Tutti gli utilizzi devono essere modificati in CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="3fe03-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="3fe03-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-120">GetDefaultDim</span></span>|<span data-ttu-id="3fe03-121">Modificare per restituire un ID di set di dimensioni sotto forma di valore intero anziché un set di record.</span><span class="sxs-lookup"><span data-stu-id="3fe03-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="3fe03-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="3fe03-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="3fe03-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="3fe03-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="3fe03-126">Modificare per utilizzare DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="3fe03-127">Funzioni eliminate</span><span class="sxs-lookup"><span data-stu-id="3fe03-127">Deleted Functions</span></span>  
 <span data-ttu-id="3fe03-128">Le funzioni che vengono eliminate dalla codeunit 408 in relazione alla funzionalità Movimenti set di dimensioni sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="3fe03-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="3fe03-129">Durante l'aggiornamento del codice dell'applicazione da Microsoft Dynamics NAV 2009 o versioni precedenti a Microsoft Dynamics NAV 2016, le seguenti funzioni non sono disponibili in Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="3fe03-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="3fe03-130">Se si dispone di personalizzazioni in cui vengono utilizzate una o più funzioni, è necessario aggiornare il codice di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="3fe03-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="3fe03-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="3fe03-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="3fe03-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="3fe03-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="3fe03-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-136">InsertDocDim</span></span>  

 <span data-ttu-id="3fe03-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="3fe03-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="3fe03-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="3fe03-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="3fe03-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-141">InsertServContractDim</span></span>  

 <span data-ttu-id="3fe03-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="3fe03-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="3fe03-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="3fe03-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-144">GetDocDim</span></span>  

 <span data-ttu-id="3fe03-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-145">GetProdDocDim</span></span>  

 <span data-ttu-id="3fe03-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="3fe03-146">TypeToTableID1</span></span>  

 <span data-ttu-id="3fe03-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="3fe03-147">TypeToTableID2</span></span>  

 <span data-ttu-id="3fe03-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="3fe03-148">TypeToTableID3</span></span>  

 <span data-ttu-id="3fe03-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="3fe03-149">TypeToTableID4</span></span>  

 <span data-ttu-id="3fe03-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="3fe03-150">TypeToTableID5</span></span>  

 <span data-ttu-id="3fe03-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-152">DeleteDocDim</span></span>  

 <span data-ttu-id="3fe03-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="3fe03-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="3fe03-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="3fe03-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="3fe03-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="3fe03-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-160">ShowDocDim</span></span>  

 <span data-ttu-id="3fe03-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-161">SaveDocDim</span></span>  

 <span data-ttu-id="3fe03-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="3fe03-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="3fe03-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-164">ShowTempDim</span></span>  

 <span data-ttu-id="3fe03-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-165">SaveTempDim</span></span>  

 <span data-ttu-id="3fe03-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="3fe03-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="3fe03-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-168">SaveServContractDim</span></span>  

 <span data-ttu-id="3fe03-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="3fe03-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="3fe03-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="3fe03-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="3fe03-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="3fe03-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="3fe03-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="3fe03-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="3fe03-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="3fe03-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="3fe03-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="3fe03-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="3fe03-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="3fe03-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="3fe03-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="3fe03-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="3fe03-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="3fe03-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="3fe03-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="3fe03-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="3fe03-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="3fe03-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="3fe03-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="3fe03-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="3fe03-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="3fe03-198">TestDimValue</span></span>  

 <span data-ttu-id="3fe03-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="3fe03-199">TestNewDimValue</span></span>  

 <span data-ttu-id="3fe03-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="3fe03-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="3fe03-201">(Eliminare perché la tabella ItemBudgetDim viene eliminata).</span><span class="sxs-lookup"><span data-stu-id="3fe03-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="3fe03-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-202">GetServContractDim</span></span>  

 <span data-ttu-id="3fe03-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="3fe03-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="3fe03-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="3fe03-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="3fe03-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="3fe03-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="3fe03-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="3fe03-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="3fe03-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fe03-207">See Also</span></span>
 <span data-ttu-id="3fe03-208">[Dettagli di progettazione: Movimenti set di dimensioni](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="3fe03-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="3fe03-209">[Dettagli di progettazione: Sintesi movimenti set di dimensioni](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="3fe03-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="3fe03-210">[Dettagli di progettazione: Ricerca delle combinazioni di dimensione](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="3fe03-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="3fe03-211">[Dettagli di progettazione: Struttura della tabella](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="3fe03-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="3fe03-212">Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche</span><span class="sxs-lookup"><span data-stu-id="3fe03-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

