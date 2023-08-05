---
title: Impostare lo scambio di dati per inviare e ricevere file
description: 'Imposta il framework di scambio dati per scambiare i dati con i file interessati, inviare e ricevere documenti elettronici o importare ed esportare file della banca.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# Impostazione dello scambio di dati

Prima di poter inviare e ricevere documenti elettronici o importare ed esportare file della banca, è necessario impostare il framework di scambio dati per elaborare i file interessati. È inoltre necessario impostare aree correlate, ad esempio i clienti a cui si inviano fatture elettroniche o l'estensione AMC Banking 365 Fundamentals, qualora si utilizzi il provider di servizi esterno per convertire i file dei conti correnti bancari. Per ulteriori informazioni, vedere [Scambio di dati in modalità elettronica](across-data-exchange.md).  

 Se [!INCLUDE[prod_short](includes/prod_short.md)] è impostato per scambiare i dati con file esterni, gli utenti possono utilizzare l'impostazione in task aziendali comuni, ad esempio l'invio e la ricezione di documenti elettronici, nonché l'importazione e l'esportazione di file bancari.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare il servizio di scambio documenti preconfigurato per abilitare l'invio e la ricezione dei documenti elettronici da e a [!INCLUDE[prod_short](includes/prod_short.md)].|[Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md)|  
|Configurare il servizio OCR preconfigurato per convertire i file PDF o di immagine in documenti elettronici che possono essere convertiti in record di documento in [!INCLUDE[prod_short](includes/prod_short.md)].|[Impostare documenti in entrata](across-how-setup-income-documents.md)|  
|Configurare uno dei due servizi preconfigurati per i tassi di cambio aggiornati in modo da ottenere i tassi di cambio valuta più recenti nella pagina **Valute**.|[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)|  
|È necessario impostare diversi dati master, ad esempio le informazioni sulla società, i clienti, i fornitori, gli articoli e le unità di misura correlati ai dati di mapping in [!INCLUDE[prod_short](includes/prod_short.md)]|[Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Impostare un conto corrente bancario, un fornitore e le registrazioni pagamenti per bonifici SEPA.|[Impostare un bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Preparare i formati dei conti bancari, i metodi di pagamento e gli accordi con i clienti per l'addebito diretto SEPA.|[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)|  
|Impostare l'autenticazione utente e l'URL del provider dell'estensione AMC Banking 365 Fundamentals che deve convertire i file della banca nel formato della banca in uso.|[Utilizzare l'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)|  
|Impostare e abilitare un servizio esterno che consente di importare gli estratti conto bancari direttamente come feed bancari.|[Impostazione del Servizio rendiconti bancari](bank-how-setup-bank-statement-service.md)|  
|Dopo che il servizio Rendiconto bancario è abilitato, collegare i conti bancari in [!INCLUDE[prod_short](includes/prod_short.md)]|[Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md)|  
|Configurare l'esportazione dei dati per il reporting Intrastat in [!INCLUDE[prod_short](includes/prod_short.md)].|[Impostare il reporting Intrastat](finance-how-setup-report-intrastat.md)|
|Preparare l'impostazione di una nuova definizione di scambio di dati per un file o un flusso di dati utilizzando lo schema XML del file per precompilare la Scheda dettaglio **Definizioni colonne** nella pagina **Registrazione definizioni di scambio**.|[Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Impostare il framework di scambio dei dati per consentire agli utenti di ricevere un nuovo formato di documenti di acquisto, inviare un nuovo formato di documenti di vendita, importare un nuovo file bancario o altri tipi di scambio di dati.|[Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md)|  

## Vedi il relativo [training Microsoft](/training/modules/electronic-documents-dynamics-365-business-central/)

## Vedere anche

[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Documenti in entrata](across-income-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
