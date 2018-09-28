---
title: 'Dettagli di progettazione: Gestione dimensioni della codeunit 408 | Microsoft Docs'
description: "La gestione delle dimensioni della Codeunit 408 è una libreria di funzione che gestisce le attività comuni correlate alle dimensioni, ad esempio copia da una tabella a un'altra oppure da un documento a un altro."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 34d4314357aa590304885585016124100ead4ca3
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-codeunit-408-dimension-management"></a>Dettagli di progettazione: Gestione dimensioni della codeunit 408
La gestione delle dimensioni della Codeunit 408 è una libreria di funzione che gestisce le attività comuni correlate alle dimensioni, ad esempio copia da una tabella a un'altra oppure da un documento a un altro. In questo argomento sono elencate le funzioni che vengono modificate in Microsoft Dynamics NAV 2013 R2 e vengono specificate le azioni da intraprendere per le funzioni. Numerose funzioni sono state eliminate in quanto non è necessario eseguire copie tra le tabelle delle dimensioni.  

## <a name="modified-functions"></a>Funzioni modificate  

|Nome funzione|Descrizione modifica|  
|-------------------|------------------------------|  
|CheckDimSetIDComb|Nuova funzione che sostituisce le altre funzioni di controllo e accetta un ID di set di dimensioni come argomento anziché una tabella delle dimensioni.|  
|CheckDimSetIDComb<br /><br /> CheckDocDimComb<br /><br /> CheckServContractDimComb<br /><br /> CheckDimBuffer<br /><br /> CheckDimComb<br /><br /> CheckDimValueComb|Elimina. Tutti gli utilizzi devono essere modificati in CheckDimSetIDComb.|  
|GetDefaultDim|Modificare per restituire un ID di set di dimensioni sotto forma di valore intero anziché un set di record.|  
|CopyJnlLineDimToICJnlDim<br /><br /> CopyICJnlDimToJnlLineDim<br /><br /> CopyDocDimtoICDocDim<br /><br /> CopyICDocDimtoICDocDim|Modificare per utilizzare DimSetID -> ICJnlLineDim|  

## <a name="deleted-functions"></a>Funzioni eliminate  
 Le funzioni che vengono eliminate dalla codeunit 408 in relazione alla funzionalità Movimenti set di dimensioni sono elencate di seguito.  

> [!CAUTION]  
>  Durante l'aggiornamento del codice dell'applicazione da Microsoft Dynamics NAV 2009 o versioni precedenti a Microsoft Dynamics NAV 2016, le seguenti funzioni non sono disponibili in Microsoft Dynamics NAV 2016. Se si dispone di personalizzazioni in cui vengono utilizzate una o più funzioni, è necessario aggiornare il codice di conseguenza.

 InsertJnlLineDim  

 UpdateJnlLineDefaultDim  

 GetJnlLineDefaultDim  

 GetPreviousDocDefaultDim  

 GetPreviousProdDocDefaultDim  

 InsertDocDim  

 UpdateDocDefaultDim  

 ExtractDocDefaultDim  

 InsertProdDocDim  

 UpdateProdDocDefaultDim  

 InsertServContractDim  

 UpdateServcontractDim  

 UpdateDefaultDimNewDimValue  

 GetDocDim  

 GetProdDocDim  

 TypeToTableID1  

 TypeToTableID2  

 TypeToTableID3  

 TypeToTableID4  

 TypeToTableID5  

 DeleteJnlLineDim  

 DeleteDocDim  

 DeletePostedDocDim  

 DeleteProdDocDim  

 DeleteServContractDim  

 ShowJnlLineDim  

 SaveJnlLineDim  

 ShowJnlLineNewDim  

 SaveJnlLineNewDim  

 ShowDocDim  

 SaveDocDim  

 ShowProdDocDim  

 SaveProdDocDim  

 ShowTempDim  

 SaveTempDim  

 ShowTempNewDim  

 SaveTempNewDim  

 SaveServContractDim  

 MoveJnlLineDimToLedgEntryDim  

 MoveDocDimToPostedDocDim  

 MoveOneDocDimToPostedDocDim  

 MoveLedgEntryDimToJnlLineDim  

 MoveDimBufToJnlLineDim  

 MoveDimBufToLedgEntryDim  

 MoveDimBufToPostedDocDim  

 MoveDimBufToGLBudgetDim  

 CopyJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToJnlLineDim  

 CopyDocDimToDocDim  

 CopyPostedDocDimToPostedDocDim  

 CopyDocDimToJnlLineDim  

 CopyDimBufToJnlLineDim  

 CopyDimBufToDocDim  

 CopySCDimToDocDim  

 MoveDocDimToLedgEntryDim  

 MoveDocDimToDocDim  

 MoveDocDimArchvToDocDim  

 MoveLedgEntryDimToDocDim  

 MoveProdDocDimToProdDocDim  

 MoveJnlLineDimToProdDocDim  

 MoveJnlLineDimToDocDim  

 MoveJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToLedgEntryDim  

 MoveTempFromDimToTempToDim  

 TransferTempToDimToDocDim  

 MoveJnlLineDimToBuf  

 CopyICJnlDimToICJnlDim  

 TestDimValue  

 TestNewDimValue  

 MoveDimBufToItemBudgetDim. (Eliminare perché la tabella ItemBudgetDim viene eliminata).  

 GetServContractDim  

 MoveTempDimToBuf  

 UpdateSCInvLineDim  

 CopyJnlLineDimToBuffer  

 UpdateDocDefaultDim2  

## <a name="see-also"></a>Vedi anche
 [Dettagli di progettazione: Movimenti set di dimensioni](design-details-dimension-set-entries.md)   
 [Dettagli di progettazione: Sintesi movimenti set di dimensioni](design-details-dimension-set-entries-overview.md)   
 [Dettagli di progettazione: Ricerca delle combinazioni di dimensione](design-details-searching-for-dimension-combinations.md)   
 [Dettagli di progettazione: Struttura della tabella](design-details-table-structure.md)   
 [Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche](design-details-code-examples-of-changed-patterns-in-modifications.md)

