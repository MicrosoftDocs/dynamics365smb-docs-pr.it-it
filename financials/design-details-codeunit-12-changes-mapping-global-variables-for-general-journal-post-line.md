---
title: "Dettagli di progettazione: Modifiche relative alla codeunit 12 nelle variabili globali di mappatura per la riga di registrazione di contabilità generale | Microsoft Docs"
description: Le seguenti modifiche sono state implementate in questa versione di Dynamics 365.
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 253043c8f3b2a15f2ed6d0990192977772e98b87
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Modifiche relative alla codeunit 12: variabili globali di mappatura per la riga di registrazione di contabilità generale
Le seguenti modifiche sono state implementate in questa versione di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Commento**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009: Record 98;|GLSetup@1009: Record 98;|Invariato|  
|SalesSetup@1010: Record 311;||Modificato in locale|  
|PurchSetup@1011: Record 312;||Modificato in locale|  
|AccountingPeriod@1012: Record 50;||Modificato in locale|  
|GLAcc@1013: Record 15;||Modificato in locale|  
|GLEntry@1014: Record 17;|GlobalGLEntry@1014: Record 17;|Rinominato|  
|GLEntryTmp@1015: TEMPORARY Record 17;|TempGLEntryBuf@1010: TEMPORARY Record 17;|Rinominato|  
|TempGLEntryVAT@1016: TEMPORARY Record 17;|TempGLEntryVAT@1016: TEMPORARY Record 17;|Invariato|  
|OrigGLEntry@1017: Record 17;||Eliminato|  
|VATPostingSetup@1019: Record 325;||Modificato in locale|  
|Cust@1020: Record 18;||Modificato in locale|  
|Vend@1021: Record 23;||Modificato in locale|  
|GenJnlLine@1022: Record 81;||Modificato in locale|  
|GLReg@1029: Record 45;|GLReg@1029: Record 45;|Invariato|  
|CustPostingGr@1030: Record 92;||Modificato in locale|  
|VendPostingGr@1031: Record 93;||Modificato in locale|  
|Currency@1032: Record 4;||Modificato in locale|  
|AddCurrency@1033: Record 4;|AddCurrency@1033: Record 4;|Invariato|  
|ApplnCurrency@1034: Record 4;||Modificato in locale|  
|CurrExchRate@1035: Record 330;|CurrExchRate@1035: Record 330;|Invariato|  
|VATEntry@1038: Record 254;|VATEntry@1038: Record 254;|Invariato|  
|BankAcc@1039: Record 270;||Modificato in locale|  
|BankAccLedgEntry@1040: Record 271;||Modificato in locale|  
|CheckLedgEntry@1041: Record 272;||Modificato in locale|  
|CheckLedgEntry2@1042: Record 272;||Modificato in locale|  
|BankAccPostingGr@1043: Record 277;||Modificato in locale|  
|GenJnlTemplate@1044: Record 80;||Modificato in locale|  
|TaxJurisdiction@1045: Record 320;||Modificato in locale|  
|TaxDetail@1046: Record 322;|TaxDetail@1046: Record 322;|Invariato|  
|FAGLPostBuf@1047: TEMPORARY Record 5637;||Modificato in locale|  
|UnrealizedCustLedgEntry@1084: Record 21;|UnrealizedCustLedgEntry@1084: Record 21;|Invariato|  
|UnrealizedVendLedgEntry@1085: Record 25;|UnrealizedVendLedgEntry@1085: Record 25;|Invariato|  
|GLEntryVATEntryLink@1087: Record 253;|GLEntryVATEntryLink@1087: Record 253;|Invariato|  
|TempVATEntry@1088: TEMPORARY Record 254;|TempVATEntry@1088: TEMPORARY Record 254;|Invariato|  
|ReversedGLEntryTemp@1089: TEMPORARY Record 17;||Spostato in Codeunit17|  
|CostAccSetup@1092: Record 1108;||Modificato in locale|  
|GenJnlCheckLine@1048: Codeunit 11;|GenJnlCheckLine@1001: Codeunit 11;|Invariato|  
|ExchAccGLJnlLine@1049: Codeunit 366;||Modificato in locale|  
|FAJnlPostLine@1050: Codeunit 5632;||Modificato in locale|  
|SalesTaxCalculate@1051: Codeunit 398;||Modificato in locale|  
|GenJnlApply@1052: Codeunit 225;||Modificato in locale|  
|DimMgt@1053: Codeunit 408;||Modificato in locale|  
|JobPostLine@1028: Codeunit 1001;||Modificato in locale|  
|TransferGlEntriesToCA@1091: Codeunit 1105;||Modificato in locale|  
||PaymentToleranceMgt@1002: Codeunit 426;|Aggiunto|  
||AddCurrencyCode@1117 : Code[10];|Aggiunto|  
|FiscalYearStartDate@1054: Data;|FiscalYearStartDate@1011: Data;|Invariato|  
|NextEntryNo@1055: Nr. intero;|NextEntryNo@1022: Nr. intero;|Invariato|  
|BalanceCheckAmount@1056: Decimale;|BalanceCheckAmount@1056: Decimale;|Invariato|  
|BalanceCheckAmount2@1057: Decimale;|BalanceCheckAmount2@1057: Decimale;|Invariato|  
|BalanceCheckAddCurrAmount@1058: Decimale;|BalanceCheckAddCurrAmount@1058: Decimale;|Invariato|  
|BalanceCheckAddCurrAmount2@1059: Decimale;|BalanceCheckAddCurrAmount2@1059: Decimale;|Invariato|  
|CurrentBalance@1060: Decimale;|CurrentBalance@1060: Decimale;|Invariato|  
|SalesTaxBaseAmount@1061: Decimale;||Modificato in locale|  
|TotalAddCurrAmount@1062: Decimale;|TotalAddCurrAmount@1062: Decimale;|Invariato|  
|TotalAmount@1063: Decimale;|TotalAmount@1063: Decimale;|Invariato|  
|UnrealizedRemainingAmountCust@1086: Decimale;|UnrealizedRemainingAmountCust@1086: Decimale;|Invariato|  
|UnrealizedRemainingAmountVend@1074: Decimale;|UnrealizedRemainingAmountVend@1074: Decimale;|Invariato|  
|NextVATEntryNo@1064: Nr. intero;|NextVATEntryNo@1064: Nr. intero;|Invariato|  
|FirstNewVATEntryNo@1065: Nr. intero;|FirstNewVATEntryNo@1065: Nr. intero;|Invariato|  
|NextTransactionNo@1066: Nr. intero;|NextTransactionNo@1066: Nr. intero;|Invariato|  
|NextConnectionNo@1067: Nr. intero;|NextConnectionNo@1067: Nr. intero;|Invariato|  
|InsertedTempGLEntryVAT@1068: Nr. intero;|InsertedTempGLEntryVAT@1027: Nr. intero;|Invariato|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Invariato|  
|LastLineNo@1070: Nr. intero;||Eliminato|  
|LastDate@1071: Data;|LastDate@1021: Data;|Invariato|  
|LastDocType@1072: " ,Pagamento,Fattura,Nota di credito,Nota di addebito,Sollecito";|LastDocType@1025: " ,Pagamento,Fattura,Nota di credito,Nota di addebito,Sollecito'';|Invariato|  
|NextCheckEntryNo@1073: Nr. intero;|NextCheckEntryNo@1028: Nr. intero;|Invariato|  
|AddCurrGLEntryVATAmt@1075: Decimale;|AddCurrGLEntryVATAmt@1017: Decimale;|Invariato|  
|CurrencyDate@1076: Data;|CurrencyDate@1020: Data;|Invariato|  
|CurrencyFactor@1077: Decimale;|CurrencyFactor@1019: Decimale;|Invariato|  
|UseCurrFactorOnly@1078: Boolean;|UseCurrFactorOnly@1078: Boolean;|Invariato|  
|NonAddCurrCodeOccured@1079: Boolean;|NonAddCurrCodeOccured@1079: Boolean;|Invariato|  
|FADimAlreadyChecked@1080: Boolean;|FADimAlreadyChecked@1080: Boolean;|Invariato|  
|AllApplied@1081: Boolean;||Modificato in locale|  
|OverrideDimErr@1018: Boolean;|OverrideDimErr@1018: Boolean;|Invariato|  
|JobLine@1036: Boolean;|JobLine@1036: Boolean;|Invariato|  
|Prepayment@1037: Boolean;||Eliminato|  
|CheckUnrealizedCust@1082: Boolean;|CheckUnrealizedCust@1082: Boolean;|Invariato|  
|CheckUnrealizedVend@1083: Boolean;|CheckUnrealizedVend@1083: Boolean;|Invariato|  
|GLEntryNo@1090: Nr. intero;|GLEntryNo@1026: Nr. intero;|Invariato|  
||GLSetupRead@1015: Boolean;|Aggiunto|  
||AmountRoundingPrecision@1012: Decimale;|Aggiunto|  
||CrCardTransactionEntryNo@1013: Nr. intero;|Aggiunto|  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Modifiche relative alla codeunit 12: modifiche nelle procedure di registrazione di contabilità generale](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

