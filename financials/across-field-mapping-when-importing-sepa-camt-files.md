---
title: Mapping dei campi durante l'importazione dei file SEPA CAMT | Microsoft Docs
description: "Nei mercati europei è possibile importare i file del rendiconto bancario negli standard SEPA (Single Euro Payments Area) locali."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 95d4104be55bcaf77dffd47e1bec0afcbe95a1da
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Mapping dei campi durante l'importazione dei file SEPA CAMT
La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta gli standard SEPA (Single Euro Payments Area)per l'importazione dei rendiconti bancari SEPA (formato CAMT). Per ulteriori informazioni, vedere [Procedura: Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-data-conversion-service.md).  

 Lo standard SEPA CAMT include di per sé variazioni locali. Di conseguenza, è possibile che si debba modificare la definizione di scambio dati generica rappresentata dal codice **SEPA CAMT** nella finestra **Registrazione definizioni di scambio** per adattarla a una variazione locale dello standard. Nelle seguenti tabelle viene mostrato il mapping tra elementi e campi per le tabelle 81, 273 e 274 nell'implementazione SEPA CAMT in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Per informazioni sulla creazione o la modifica della definizione di scambio dati, vedere [Procedura: Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>Mapping dei dati CAMT ai campi nella tabella Contabilità generale (81)  

|Percorso dell'articolo|Elemento messaggio|Tipo di dati|Descrizione|Identificatore segno negativo|Nr. campo|Nome campo|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Importo|Decimale|Specifica l'importo di denaro nel movimento cassa.||13|Importo|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Testo|Indica se il movimento è un credito o un debito|DBIT|13|Importo|  
|Stmt/Ntry/BookgDt/Dt|Data|Data|Data in cui un movimento viene registrato in un conto nei registri di chi utilizza il conto||5|Data di registrazione:|  
|Stmt/Ntry/BookgDt/DtTm|DataOra|DataOra|Data e ora in cui un movimento viene registrato in un conto nei registri di chi utilizza il conto||5|Data di registrazione:|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nome|Testo|Nome della parte che deve una somma di denaro al creditore (finale)||1221|Informazioni sul pagante|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Non strutturato|Testo|Informazioni fornite per consentire la corrispondenza o riconciliazione di un movimento con gli articoli oggetto del pagamento, come le fatture aziendali in un sistema conto clienti, in un form non strutturato||8|Descrizione|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Testo|Informazioni aggiuntive relative al movimento||1222|Informazioni sulla transazione|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>Mapping dei dati CAMT ai campi nella tabella Riconc. C/C bancari (273)  

|Percorso dell'articolo|Elemento messaggio|Tipo di dati|Descrizione|Identificatore segno negativo|Nr. campo|Nome campo|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Data|Data e ora di creazione del messaggio||3|Data estratto conto|  
|Stmt/Bal/Amt|Importo|Decimale|Importo risultante dagli importi al netto per tutti i movimenti dare e avere||4|Saldo finale estratto conto|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>Mapping dei dati CAMT ai campi nella tabella Righe riconc. C/C bancari (274)  

|Percorso dell'articolo|Elemento messaggio|Tipo di dati|Descrizione|Identificatore segno negativo|Nr. campo|Nome campo|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Importo|Decimale|Specifica l'importo di denaro nel movimento cassa.||7|Importo estratto conto|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Testo|Indica se il movimento è un credito o un debito|DBIT|7|Importo estratto conto|  
|Stmt/Ntry/BookgDt/Dt|Data|Data|Data in cui un movimento viene registrato in un conto nei registri di chi utilizza il conto||5|Data transazione|  
|Stmt/Ntry/BookgDt/DtTm|DataOra|DataOra|Data e ora in cui un movimento viene registrato in un conto nei registri di chi utilizza il conto||5|Data transazione|  
|Stmt/Ntry/ValDt/Dt|Data|Data|Data in cui i cespiti diventano disponibili al proprietario del conto nel caso di un movimento in avere o cessano di essere disponibili nel caso di un movimento in dare||12|Data valuta|  
|Stmt/Ntry/ValDt/DtTm|DataOra|DataOra|Data e ora in cui i cespiti diventano disponibili al proprietario del conto nel caso di un movimento in avere o cessano di essere disponibili nel caso di un movimento in dare||12|Data valuta|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nome|Testo|Nome della parte che deve una somma di denaro al creditore (finale)||15|Informazioni sul pagante|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Non strutturato|Testo|Informazioni fornite per consentire la corrispondenza o riconciliazione di un movimento con gli articoli oggetto del pagamento, come le fatture aziendali in un sistema conto clienti, in un form non strutturato||6|Descrizione|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Testo|Informazioni aggiuntive relative al movimento||16|Informazioni sulla transazione|  

 Gli elementi nel nodo **Ntry** importati in [!INCLUDE[d365fin](includes/d365fin_md.md)], ma di cui non è stato eseguito il mapping ad alcun campo, vengono memorizzati nella tabella **Registrazione definizione colonna scambio dati**. Gli utenti possono vedere gli elementi nelle finestre **Registrazione riconciliazione pagamenti**, **Collegamento pagamenti** e **Riconciliazioni C/C bancari** scegliendo l'azione **Dettagli riga rendiconto bancario**. Per ulteriori informazioni, vedere [Procedura: Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).  
## <a name="see-also"></a>Vedi anche  
[Impostare lo scambio di dati](across-set-up-data-exchange.md)  
[Scambio di dati come documenti elettronici](across-data-exchange.md)  
[Procedura: Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-data-conversion-service.md)   
[Procedura: Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Procedura: Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md)  

