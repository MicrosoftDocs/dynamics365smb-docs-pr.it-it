---
title: "Dettagli di progettazione: Modifiche relative alla codeunit 12 nelle procedure di registrazione di contabilità generale | Microsoft Docs"
description: Le seguenti modifiche sono state implementate in questa versione di Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 09e52a35909c21eaaf9d2eab37b19dc947a2a8dd
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="codeunit-12-changes-changes-in-general-journal-post-procedures"></a>Modifiche relative alla codeunit 12: modifiche nelle procedure di registrazione di contabilità generale
Le seguenti modifiche sono state implementate in questa versione di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Commento**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GetGLReg|GetGLReg|Aggiornato|  
|RunWithCheck|RunWithCheck|Aggiornato|  
|RunWithoutCheck|RunWithoutCheck|Aggiornato|  
|Code|Code|Aggiornato|  
||PostGenJnlLine|Aggiunto|  
||InitAmounts|Aggiunto|  
||InitLastDocDate|Aggiunto|  
|InitVAT|InitVAT|Aggiornato|  
|PostVAT|PostVAT|Aggiornato|  
|InsertVAT|InsertVAT|Aggiornato|  
|SummarizeVAT|SummarizeVAT|Aggiornato|  
|InsertSummarizedVAT|InsertSummarizedVAT|Aggiornato|  
|PostGLAcc|PostGLAcc|Aggiornato|  
|PostCust|PostCust|Aggiornato|  
|PostVend|PostVend|Aggiornato|  
|PostBankAcc|PostBankAcc|Aggiornato|  
|PostFixedAsset|PostFixedAsset|Aggiornato|  
|PostICPartner|PostICPartner|Aggiornato|  
|InitCodeUnit|StartPosting|Aggiornato|  
||ContinuePosting|Aggiunto|  
|FinishCodeunit|FinishPosting|Aggiornato|  
||PostUnrealizedVAT|Aggiunto|  
||CheckPostUnrealizedVAT|Aggiunto|  
||ExchangeAccounts|Aggiunto|  
|InitGLEntry|InitGLEntry|Aggiornato|  
||InitGLEntryVAT|Aggiunto|  
||InitGLEntryVATCopy|Aggiunto|  
|InsertGLEntry|InsertGLEntry|Aggiornato|  
||CreateGLEntry|Aggiunto|  
||CreateGLEntryBalAcc|Aggiunto|  
||CreateGLEntryVAT|Aggiunto|  
||CreateGLEntryVATCollectAdj|Aggiunto|  
||CreateGLEntryFromVATEntry|Aggiunto|  
||UpdateCheckAmounts|Aggiunto|  
|ApplyCustLedgEntry|ApplyCustLedgEntry|Aggiornato|  
||CalcPmtDiscPossible|Aggiunto|  
||CalcPmtTolerancePossible|Aggiunto|  
|CalcPmtTolerance|CalcPmtTolerance|Aggiornato|  
|CalcPmtDisc|CalcPmtDisc|Aggiornato|  
|CalcPmtDiscIfAdjVAT|CalcPmtDiscIfAdjVAT|Aggiornato|  
|CalcPmtDiscTolerance|CalcPmtDiscTolerance|Aggiornato|  
||CalcPmtDiscVATBases|Aggiunto|  
||CalcPmtDiscVATAmounts|Aggiunto|  
||InsertPmtDiscVATForVATEntry|Aggiunto|  
||InsertPmtDiscVATForGLEntry|Aggiunto|  
|CalcCurrencyApplnRounding|CalcCurrencyApplnRounding|Aggiornato|  
|FindAmtForAppln|FindAmtForAppln|Aggiornato|  
|CalcCurrencyUnrealizedGainLoss|CalcCurrencyUnrealizedGainLoss|Aggiornato|  
|CalcCurrencyRealizedGainLoss|CalcCurrencyRealizedGainLoss|Aggiornato|  
|CalcApplication|CalcApplication|Aggiornato|  
|CalcRemainingPmtDisc|CalcRemainingPmtDisc|Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|CalcAmtLCYAdjustment|CalcAmtLCYAdjustment|Aggiunto|  
|InitNewCVLedgEntry|InitFromGenJnlLine|Spostato nella tabella 383 Dettaglio mov. buffer CF|  
|InitOldCVLedgEntry|CopyFromCVLedgEntryBuf|Spostato nella tabella 383 Dettaglio mov. buffer CF|  
|InsertDtldCVLedgEntry|InsertDtldCVLedgEntry|Spostato nella tabella 383 Dettaglio mov. buffer CF|  
||InitBankAccLedgEntry|Aggiunto|  
||InitCheckLedgEntry|Aggiunto|  
||InitCustLedgEntry|Aggiunto|  
||InitVendLedgEntry|Aggiunto|  
||InsertDtldCustLedgEntry|Aggiunto|  
||InsertDtldVendLedgEntry|Aggiunto|  
|CustUnrealizedVAT|CustUnrealizedVAT|Aggiornato|  
|CustPostApplyCustLedgEntry|CustPostApplyCustLedgEntry|Aggiornato|  
||PrepareTempCustLedgEntry|Aggiunto|  
|UnapplyCustLedgEntry|UnapplyCustLedgEntry|Aggiornato|  
|TransferCustLedgEntry|CopyFromGenJnlLine|Spostato nella tabella 21 Mov. contabili clienti|  
|PostDtldCustLedgEntries|PostDtldCustLedgEntries|Aggiornato|  
||PostDtldCustLedgEntry|Aggiunto|  
||PostDtldCustLedgEntryUnapply|Aggiunto|  
||GetDtldCustLedgEntryAccNo|Aggiunto|  
|ZeroTransNoDtldCustLedgEntries|SetZeroTransNo|Spostato nella tabella 379 Dettagli mov. cliente|  
|AutoEntrForDtldCustLedgEntries||Eseguito il refactoring a PostDtldCustLedgEntryUnapply|  
|CustUpdateDebitCredit|UpdateDebitCredit|Spostato nella tabella 379 Dettagli mov. cliente|  
|ApplyVendLedgEntry|ApplyVendLedgEntry|Aggiornato|  
||PrepareTempVendLedgEntry|Aggiunto|  
|VendPostApplyVendLedgEntry|VendPostApplyVendLedgEntry|Aggiornato|  
|UnapplyVendLedgEntry|UnapplyVendLedgEntry|Aggiornato|  
|TransferVendLedgEntry|CopyFromGenJnlLine|Spostato nella tabella 25 Mov. contabili fornitori|  
|PostDtldVendLedgEntries|PostDtldVendLedgEntries|Aggiornato|  
||PostDtldVendLedgEntry|Aggiunto|  
||PostDtldVendLedgEntryUnapply|Aggiunto|  
||GetDtldVendLedgEntryAccNo|Aggiunto|  
||PostDtldCVLedgEntry|Aggiunto|  
||PostDtldCustVATAdjustment|Aggiunto|  
||PostDtldVendVATAdjustment|Aggiunto|  
|ZeroTransNoDtldVendLedgEntries|SetZeroTransNo|Spostato nella tabella 380 Dettagli mov. fornitore|  
|AutoEntrForDtldVendLedgEntries||Eseguito il refactoring a PostDtldVendLedgEntryUnapply|  
|VendUpdateDebitCredit|UpdateDebitCredit|Spostato nella tabella 380 Dettagli mov. fornitore|  
|VendUnrealizedVAT|VendUnrealizedVAT|Aggiornato|  
||PostUnrealVATEntry|Aggiunto|  
||PostApply|Aggiunto|  
|PostUnrealVATByUnapply|PostUnrealVATByUnapply|Aggiornato|  
||PostUnapply|Aggiunto|  
||InsertDtldCustLedgEntryUnapply|Aggiunto|  
||InsertDtldVendLedgEntryUnapply|Aggiunto|  
||InsertTempVATEntry|Aggiunto|  
||ProcessTempVATEntry|Aggiunto|  
||UpdateCustLedgEntry|Aggiunto|  
||UpdateVendLedgEntry|Aggiunto|  
|UpdateCalcInterest|UpdateCalcInterest|Aggiornato|  
|UpdateCalcInterest2|UpdateCalcInterest2|Aggiornato|  
|GLCalcAddCurrency|GLCalcAddCurrency|Aggiornato|  
|HandleAddCurrResidualGLEntry|HandleAddCurrResidualGLEntry|Aggiornato|  
|CalcLCYToAddCurr|CalcLCYToAddCurr|Aggiornato|  
|CalcAddCurrFactor||Eliminato|  
|GetCurrencyExchRate|GetCurrencyExchRate|Aggiornato|  
|ExchAmount|ExchangeAmount|Spostato nella tabella 330 Tasso di cambio valuta|  
|ExchangeAmtLCYToFCY2|ExchangeAmtLCYToFCY2|Aggiornato|  
|CalcAddCurrForUnapplication|CalcAddCurrForUnapplication|Aggiornato|  
|CheckNonAddCurrCodeOccurred|CheckNonAddCurrCodeOccurred|Aggiornato|  
|CheckCalcPmtDisc||Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|CheckCalcPmtDiscCVCust||Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|CheckCalcPmtDiscCust||Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|CheckCalcPmtDiscGenJnlCust||Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|CheckCalcPmtDiscCVVend||Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|CheckCalcPmtDiscVend||Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|CheckCalcPmtDiscGenJnlVend||Spostato in Codeunit 426 Gestione della tolleranza pagamento|  
|Reverse|Reverse|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|ReverseVendLedgEntry|ReverseVendLedgEntry|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|ReverseVAT|ReverseVAT|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|SetReversalDescription|SetReversalDescription|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Spostato in Codeunit 17 Registrazioni gen. - Storno|  
||CheckDimComb|Aggiunto nella Codeunit 17 Registrazioni gen. - Storno|  
||CopyCustLedgEntry|Aggiunto nella Codeunit 17 Registrazioni gen. - Storno|  
||CopyVendLedgEntry|Aggiunto nella Codeunit 17 Registrazioni gen. - Storno|  
||CopyBankAccLedgEntry|Aggiunto nella Codeunit 17 Registrazioni gen. - Storno|  
|HandlDtlAddjustment|HandleDtldAdjustment|Aggiornato|  
|CollectAddjustment|CollectAdjustment|Aggiornato|  
|SetOverDimErr|SetOverDimErr|Aggiornato|  
|PostJob|PostJob|Aggiornato|  
|InsertVATEntriesFromTemp|InsertVATEntriesFromTemp|Aggiornato|  
|CaptureOrRefundCreditCardPmnt|CaptureOrRefundCreditCardPmnt|Aggiornato|  
|UpdateDOPaymentTransactEntry|UpdateDOPaymentTransactEntry|Aggiornato|  
|ABSMin|ABSMin|Aggiornato|  
|GetApplnRoundPrecision|GetApplnRoundPrecision|Aggiornato|  
|CheckDimValueForDisposal|CheckDimValueForDisposal|Aggiornato|  
|CalculateCurrentBalance|CalculateCurrentBalance|Aggiornato|  
|IncludeVATAmount||Spostato nella tabella 81 Righe registrazioni COGE|  
|CalcVATAmountFromVATEntry|CalcVATAmountFromVATEntry|Aggiornato|  
||TotalVATAmountOnJnlLines|Aggiunto|  
||SetGLRegReverse|Aggiunto|  
||GetGLSetup|Aggiunto|  
||ReadGLSetup|Aggiunto|  
||CheckSalesExtDocNo|Aggiunto|  
||CheckPurchExtDocNo|Aggiunto|  
||CheckGLAccDimError|Aggiunto|  
||GetCurrency|Aggiunto|  
||PostDtldAdjustment|Aggiunto|  
||GetNextEntryNo|Aggiunto|  
||GetNextTransactionNo|Aggiunto|  
||GetNextVATEntryNo|Aggiunto|  
||IncrNextVATEntryNo|Aggiunto|  
||IsNotPayment|Aggiunto|  
||IsTempGLEntryBufEmpty|Aggiunto|  
||IsVATAdjustment|Aggiunto|  
||IsVATExcluded|Aggiunto|  
||UpdateDimensions|Aggiunto|  
||UpdateDimensionsFromCustLedgEntry|Aggiunto|  
||UpdateDimensionsFromVendLedgEntry|Aggiunto|  
||UpdateTotalAmounts|Aggiunto|  
||CreateGLEntriesForTotalAmounts|Aggiunto|  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Modifiche relative alla codeunit 12: variabili globali di mappatura per la riga di registrazione di contabilità generale](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)

