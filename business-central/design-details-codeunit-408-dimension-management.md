---
title: 'Dettagli di progettazione: Gestione dimensioni della codeunit 408 | Microsoft Docs'
description: La gestione delle dimensioni della Codeunit 408 è una libreria di funzione che gestisce le attività comuni correlate alle dimensioni, ad esempio copia da una tabella a un'altra oppure da un documento a un altro.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: 3b3cc817ac79fa18a5f0b68b97a54fab9ac6711b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307326"
---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="e639c-103">Dettagli di progettazione: Gestione dimensioni della codeunit 408</span><span class="sxs-lookup"><span data-stu-id="e639c-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="e639c-104">La gestione delle dimensioni della Codeunit 408 è una libreria di funzione che gestisce le attività comuni correlate alle dimensioni, ad esempio copia da una tabella a un'altra oppure da un documento a un altro.</span><span class="sxs-lookup"><span data-stu-id="e639c-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="e639c-105">In questo argomento sono elencate le funzioni che vengono modificate in Microsoft Dynamics NAV 2013 R2 e vengono specificate le azioni da intraprendere per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="e639c-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="e639c-106">Numerose funzioni sono state eliminate in quanto non è necessario eseguire copie tra le tabelle delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e639c-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="e639c-107">Funzioni modificate</span><span class="sxs-lookup"><span data-stu-id="e639c-107">Modified Functions</span></span>  

|<span data-ttu-id="e639c-108">Nome funzione</span><span class="sxs-lookup"><span data-stu-id="e639c-108">Function Name</span></span>|<span data-ttu-id="e639c-109">Descrizione modifica</span><span class="sxs-lookup"><span data-stu-id="e639c-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="e639c-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="e639c-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="e639c-111">Nuova funzione che sostituisce le altre funzioni di controllo e accetta un ID di set di dimensioni come argomento anziché una tabella delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e639c-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="e639c-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="e639c-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="e639c-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="e639c-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="e639c-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="e639c-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="e639c-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="e639c-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="e639c-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="e639c-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="e639c-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="e639c-117">CheckDimValueComb</span></span>|<span data-ttu-id="e639c-118">Elimina.</span><span class="sxs-lookup"><span data-stu-id="e639c-118">Delete.</span></span> <span data-ttu-id="e639c-119">Tutti gli utilizzi devono essere modificati in CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="e639c-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="e639c-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-120">GetDefaultDim</span></span>|<span data-ttu-id="e639c-121">Modificare per restituire un ID di set di dimensioni sotto forma di valore intero anziché un set di record.</span><span class="sxs-lookup"><span data-stu-id="e639c-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="e639c-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="e639c-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="e639c-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="e639c-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="e639c-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="e639c-126">Modificare per utilizzare DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="e639c-127">Funzioni eliminate</span><span class="sxs-lookup"><span data-stu-id="e639c-127">Deleted Functions</span></span>  
 <span data-ttu-id="e639c-128">Le funzioni che vengono eliminate dalla codeunit 408 in relazione alla funzionalità Movimenti set di dimensioni sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="e639c-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="e639c-129">Durante l'aggiornamento del codice dell'applicazione da Microsoft Dynamics NAV 2009 o versioni precedenti a Microsoft Dynamics NAV 2016, le seguenti funzioni non sono disponibili in Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="e639c-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="e639c-130">Se si dispone di personalizzazioni in cui vengono utilizzate una o più funzioni, è necessario aggiornare il codice di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="e639c-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="e639c-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="e639c-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="e639c-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="e639c-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="e639c-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="e639c-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-136">InsertDocDim</span></span>  

 <span data-ttu-id="e639c-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="e639c-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="e639c-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="e639c-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="e639c-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="e639c-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="e639c-141">InsertServContractDim</span></span>  

 <span data-ttu-id="e639c-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="e639c-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="e639c-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="e639c-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="e639c-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-144">GetDocDim</span></span>  

 <span data-ttu-id="e639c-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-145">GetProdDocDim</span></span>  

 <span data-ttu-id="e639c-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="e639c-146">TypeToTableID1</span></span>  

 <span data-ttu-id="e639c-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="e639c-147">TypeToTableID2</span></span>  

 <span data-ttu-id="e639c-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="e639c-148">TypeToTableID3</span></span>  

 <span data-ttu-id="e639c-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="e639c-149">TypeToTableID4</span></span>  

 <span data-ttu-id="e639c-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="e639c-150">TypeToTableID5</span></span>  

 <span data-ttu-id="e639c-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="e639c-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-152">DeleteDocDim</span></span>  

 <span data-ttu-id="e639c-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="e639c-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="e639c-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="e639c-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="e639c-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="e639c-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="e639c-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="e639c-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="e639c-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="e639c-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="e639c-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-160">ShowDocDim</span></span>  

 <span data-ttu-id="e639c-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-161">SaveDocDim</span></span>  

 <span data-ttu-id="e639c-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="e639c-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="e639c-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="e639c-164">ShowTempDim</span></span>  

 <span data-ttu-id="e639c-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="e639c-165">SaveTempDim</span></span>  

 <span data-ttu-id="e639c-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="e639c-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="e639c-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="e639c-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="e639c-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="e639c-168">SaveServContractDim</span></span>  

 <span data-ttu-id="e639c-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="e639c-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="e639c-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="e639c-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="e639c-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="e639c-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="e639c-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="e639c-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="e639c-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="e639c-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="e639c-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="e639c-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="e639c-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="e639c-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="e639c-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="e639c-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="e639c-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="e639c-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="e639c-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="e639c-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="e639c-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="e639c-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="e639c-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="e639c-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="e639c-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="e639c-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="e639c-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="e639c-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="e639c-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="e639c-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="e639c-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="e639c-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="e639c-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="e639c-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="e639c-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="e639c-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="e639c-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="e639c-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="e639c-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="e639c-198">TestDimValue</span></span>  

 <span data-ttu-id="e639c-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="e639c-199">TestNewDimValue</span></span>  

 <span data-ttu-id="e639c-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="e639c-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="e639c-201">(Eliminare perché la tabella ItemBudgetDim viene eliminata).</span><span class="sxs-lookup"><span data-stu-id="e639c-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="e639c-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="e639c-202">GetServContractDim</span></span>  

 <span data-ttu-id="e639c-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="e639c-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="e639c-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="e639c-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="e639c-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="e639c-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="e639c-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="e639c-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="e639c-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e639c-207">See Also</span></span>
 <span data-ttu-id="e639c-208">[Dettagli di progettazione: Movimenti set di dimensioni](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="e639c-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="e639c-209">[Dettagli di progettazione: Sintesi movimenti set di dimensioni](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="e639c-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="e639c-210">[Dettagli di progettazione - Ricerca di combinazioni di dimensioni](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="e639c-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 [<span data-ttu-id="e639c-211">Dettagli di progettazione - Struttura della tabella</span><span class="sxs-lookup"><span data-stu-id="e639c-211">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
