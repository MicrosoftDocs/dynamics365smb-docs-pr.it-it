---
title: Mapping dei campi durante l'importazione dei file SEPA CAMT | Microsoft Docs
description: Nei mercati europei è possibile importare i file del rendiconto bancario negli standard SEPA (Single Euro Payments Area) locali.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 57488adb784736eaf404cf57f1563f08c517ed6c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753344"
---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Mapping dei campi durante l'importazione dei file SEPA CAMT
[!INCLUDE[prod_short](includes/prod_short.md)]La versione generica di  supporta gli standard SEPA (Single Euro Payments Area)per l'importazione dei rendiconti bancari SEPA (formato CAMT). Per ulteriori informazioni, vedere [Uso dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

 Lo standard SEPA CAMT include di per sé variazioni locali. Di conseguenza, è possibile che si debba modificare la definizione di scambio dati generica (rappresentata dal codice **SEPA CAMT** nella pagina **Registrazione definizioni di scambio**) per adattarla a una variazione locale dello standard. Nelle seguenti tabelle viene mostrato il mapping tra elementi e campi per le tabelle 81, 273 e 274 nell'implementazione SEPA CAMT in [!INCLUDE[prod_short](includes/prod_short.md)].  

 Per informazioni sulla creazione o la modifica della definizione di scambio dati, vedere [Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md).  

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

 Gli elementi nel nodo **Ntry** importati in [!INCLUDE[prod_short](includes/prod_short.md)], ma di cui non è stato eseguito il mapping ad alcun campo, vengono memorizzati nella tabella **Registrazione definizione colonna scambio dati**. Gli utenti possono vedere gli elementi nelle pagine **Registrazione riconciliazione pagamenti**, **Collegamento pagamenti** e **Riconciliazioni C/C bancari** scegliendo l'azione **Dettagli riga rendiconto bancario**. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]
> In un'importazione di estratti conto bancari CAMT, [!INCLUDE[prod_short](includes/prod_short.md)] si aspetta che ogni transazione sia univoca, ossia il campo **ID transazione** che proviene dal tag *Stmt/Ntry/NtryDtls/TxDtls/Refs/EndToEndId* nel file CAMT, deve essere univoco all'interno della riconciliazione del C/C bancario aperto. Se le informazioni non sono presenti, [!INCLUDE[prod_short](includes/prod_short.md)] ignora il pagamento. Se una riconciliazione bancaria precedente sullo stesso C/C bancario è stata registrata con lo stesso ID transazione dell'importazione corrente, la transazione corrente non verrà riconciliata automaticamente ma potrà comunque essere importata.

## <a name="see-also"></a>Vedere anche  
[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Utilizzo dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)   
[Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md)  
