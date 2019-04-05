---
title: 'Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche | Microsoft Docs'
description: Vengono forniti esempi di codice per mostrare i modelli modificati nella modifica e nella migrazione di codice dimensione per cinque scenari diversi. Confronta gli esempi di codice nelle versioni precedenti con gli esempi di codice in Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 3a5806711b693dadbbaf033ffd769c5eabebe8de
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801402"
---
# <a name="design-details-code-examples-of-changed-patterns-in-modifications"></a><span data-ttu-id="eb04f-104">Dettagli di progettazione: Esempi di codice dei modelli modificati nelle modifiche</span><span class="sxs-lookup"><span data-stu-id="eb04f-104">Design Details: Code Examples of Changed Patterns in Modifications</span></span>
<span data-ttu-id="eb04f-105">In questo argomento vengono forniti esempi di codice per mostrare i modelli modificati nella modifica e nella migrazione di codice dimensione per cinque scenari diversi.</span><span class="sxs-lookup"><span data-stu-id="eb04f-105">This topic provides code examples to show changed patterns in dimension code modification and migration for five different scenarios.</span></span> <span data-ttu-id="eb04f-106">Confronta gli esempi di codice nelle versioni precedenti con gli esempi di codice in Business Central.</span><span class="sxs-lookup"><span data-stu-id="eb04f-106">It compares the code examples in earlier versions to the code examples in Business Central.</span></span>

## <a name="posting-a-journal-line"></a><span data-ttu-id="eb04f-107">Registrazione di una riga delle registrazioni</span><span class="sxs-lookup"><span data-stu-id="eb04f-107">Posting a Journal Line</span></span>  
<span data-ttu-id="eb04f-108">Le modifiche fondamentali sono elencate di seguito:</span><span class="sxs-lookup"><span data-stu-id="eb04f-108">Key changes are listed as follows:</span></span>  
  
- <span data-ttu-id="eb04f-109">Le tabelle delle dimensioni per la riga di registrazione magazzino vengono eliminate.</span><span class="sxs-lookup"><span data-stu-id="eb04f-109">Journal line dimension tables are removed.</span></span>  
  
- <span data-ttu-id="eb04f-110">Un ID set di dimensioni viene creato nel campo **ID set di dimensioni**.</span><span class="sxs-lookup"><span data-stu-id="eb04f-110">A dimension set ID is created in the **Dimension Set ID** field.</span></span>  
  
<span data-ttu-id="eb04f-111">**Versioni precedenti**</span><span class="sxs-lookup"><span data-stu-id="eb04f-111">**Earlier Versions**</span></span>  
  
```  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  
  
TempJnlLineDim.DELETEALL;  
TempDocDim.RESET;  
TempDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Line");  
TempDocDim.SETRANGE(  
  "Line No.",SalesLine."Line No.");  
DimMgt.CopyDocDimToJnlLineDim(  
  TempDocDim,TempJnlLineDim);  
ResJnlPostLine.RunWithCheck(  
  ResJnlLine,TempJnlLineDim);  
  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  
  
ResJnlLine."Dimension Set ID" :=   
  SalesLine." Dimension Set ID ";  
ResJnlPostLine.Run(ResJnlLine);  
  
```  
  
## <a name="posting-a-document"></a><span data-ttu-id="eb04f-112">Registrazione di un documento</span><span class="sxs-lookup"><span data-stu-id="eb04f-112">Posting a Document</span></span>  
 <span data-ttu-id="eb04f-113">Quando si registra un documento in [!INCLUDE[d365fin](includes/d365fin_md.md)], non è più necessario copiare le dimensioni di documento.</span><span class="sxs-lookup"><span data-stu-id="eb04f-113">When you post a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you no longer have to copy the document dimensions.</span></span>  
  
 <span data-ttu-id="eb04f-114">**Versioni precedenti**</span><span class="sxs-lookup"><span data-stu-id="eb04f-114">**Earlier Versions**</span></span>  
  
```  
DimMgt.MoveOneDocDimToPostedDocDim(  
  TempDocDim,DATABASE::"Sales Line",  
  "Document Type",  
  "No.",  
  SalesShptLine."Line No.",  
  DATABASE::"Sales Shipment Line",  
  SalesShptHeader."No.");  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
SalesShptLine."Dimension Set ID”  
  := SalesLine."Dimension Set ID”  
```  
  
## <a name="editing-dimensions-from-a-document"></a><span data-ttu-id="eb04f-115">Modifica delle dimensioni da un documento</span><span class="sxs-lookup"><span data-stu-id="eb04f-115">Editing Dimensions from a Document</span></span>  
 <span data-ttu-id="eb04f-116">È possibile modificare le dimensioni da un documento.</span><span class="sxs-lookup"><span data-stu-id="eb04f-116">You can edit dimensions from a document.</span></span> <span data-ttu-id="eb04f-117">Ad esempio, è possibile modificare una riga dell'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="eb04f-117">For example, you can edit a sales order line.</span></span>  
  
 <span data-ttu-id="eb04f-118">**Versioni precedenti**</span><span class="sxs-lookup"><span data-stu-id="eb04f-118">**Earlier Versions**</span></span>  
  
```  
Table 37, function ShowDimensions:  
TESTFIELD("Document No.");  
TESTFIELD("Line No.");  
DocDim.SETRANGE("Table ID",DATABASE::"Sales Line");  
DocDim.SETRANGE("Document Type","Document Type");  
DocDim.SETRANGE("Document No.","Document No.");  
DocDim.SETRANGE("Line No.","Line No.");  
DocDimensions.SETTABLEVIEW(DocDim);  
DocDimensions.RUNMODAL;  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 37, function ShowDimensions:  
"Dimension ID" :=   
  DimSetEntry.EditDimensionSet(  
    "Dimension ID");  
```  
  
## <a name="showing-dimensions-from-posted-entries"></a><span data-ttu-id="eb04f-119">Visualizzazione delle dimensioni da movimenti registrati</span><span class="sxs-lookup"><span data-stu-id="eb04f-119">Showing Dimensions from Posted Entries</span></span>  
 <span data-ttu-id="eb04f-120">È possibile visualizzare le dimensioni dei movimenti registrati, ad esempio righe di spedizione vendita.</span><span class="sxs-lookup"><span data-stu-id="eb04f-120">You can show dimensions from posted entries, such as sales shipment lines.</span></span>  
  
 <span data-ttu-id="eb04f-121">**Versioni precedenti**</span><span class="sxs-lookup"><span data-stu-id="eb04f-121">**Earlier Versions**</span></span>  
  
```  
Table 111, function ShowDimensions:  
TESTFIELD("No.");  
TESTFIELD("Line No.");  
PostedDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Shipment Line");  
PostedDocDim.SETRANGE(  
  "Document No.","Document No.");  
PostedDocDim.SETRANGE("Line No.","Line No.");  
PostedDocDimensions.SETTABLEVIEW(PostedDocDim);  
PostedDocDimensions.RUNMODAL;  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 111, function ShowDimensions:  
DimSetEntry.ShowDimensionSet(  
  "Dimension ID");  
```  
  
## <a name="getting-default-dimensions-for-a-document"></a><span data-ttu-id="eb04f-122">Ottenere le dimensioni predefinite per un documento</span><span class="sxs-lookup"><span data-stu-id="eb04f-122">Getting Default Dimensions for a Document</span></span>  
 <span data-ttu-id="eb04f-123">È possibile ottenere le dimensioni predefinite per un documento, ad esempio di una riga ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="eb04f-123">You can get default dimensions for a document, such as a sales order line.</span></span>  
  
 <span data-ttu-id="eb04f-124">**Versioni precedenti**</span><span class="sxs-lookup"><span data-stu-id="eb04f-124">**Earlier Versions**</span></span>  
  
```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
DimMgt.GetPreviousDocDefaultDim(  
  DATABASE::"Sales Header","Document Type",  
  "Document No.",0,  
  DATABASE::Customer,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
DimMgt.GetDefaultDim(  
  TableID,No,SourceCodeSetup.Sales,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
IF "Line No." <> 0 THEN  
  DimMgt.UpdateDocDefaultDim(  
    DATABASE::"Sales Line","Document Type",  
    "Document No.","Line No.",  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code");  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
GetSalesHeader;  
"Dimension ID" :=  
  DimMgt.GetDefaultDimID(  
    TableID,No,SourceCodeSetup.Sales,  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code",  
    SalesHeader."Dimension ID",  
    DATABASE::"Sales Header");

```  

## <a name="see-also"></a><span data-ttu-id="eb04f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb04f-125">See Also</span></span>  
<span data-ttu-id="eb04f-126">[Dettagli di progettazione: Movimenti set di dimensioni](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="eb04f-126">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
<span data-ttu-id="eb04f-127">[Dettagli di progettazione: Struttura della tabella](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="eb04f-127">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="eb04f-128">Dettagli di progettazione: Gestione dimensioni della codeunit 408</span><span class="sxs-lookup"><span data-stu-id="eb04f-128">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)