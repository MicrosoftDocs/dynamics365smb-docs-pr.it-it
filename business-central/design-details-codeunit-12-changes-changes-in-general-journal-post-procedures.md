---
title: Modifiche nelle procedure di registrazione di contabilità generale nella codeunit 12
description: Nelle versioni precedenti, codeunit 12 è stata modificata per migliorare le prestazioni di registrazione della contabilità generale. Informazioni sulle modifiche alle procedure di registrazione in questo articolo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: c1ec373b6c7226d6b2548f2b29f326dcd9c6a459
ms.sourcegitcommit: a95681db16e81af109b34f8e5d88028c1552c6a2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367911"
---
# <a name="historical-changes-to-codeunit-12-changes-in-general-journal-post-procedures"></a>Modifiche storiche alla codeunit 12: modifiche nelle procedure di registrazione di contabilità generale

Le seguenti modifiche sono state implementate nelle versioni di [!INCLUDE [navnow_md](includes/navnow_md.md)].  

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
||CheckDimComb|Aggiunto in Codeunit 17 Registrazioni gen. - Storno|  
||CopyCustLedgEntry|Aggiunto in Codeunit 17 Registrazioni gen. - Storno|  
||CopyVendLedgEntry|Aggiunto in Codeunit 17 Registrazioni gen. - Storno|  
||CopyBankAccLedgEntry|Aggiunto in Codeunit 17 Registrazioni gen. - Storno|  
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
|IncludeVATAmount||Spostato nella Tabella 81 Righe registrazioni COGE|  
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


[!INCLUDE[footer-include](includes/footer-banner.md)]