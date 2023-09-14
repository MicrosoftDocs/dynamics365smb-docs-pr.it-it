---
title: Scambio di dati
description: 'Scambia documenti commerciali elettronici, ad esempio file bancari, tra Business Central e parti esterne.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'exchange data, external files, electronic documents, AMC Banking, OCT, SEPA'
ms.date: 06/10/2021
ms.author: bholtorf
---
# <a name="exchanging-data"></a>Scambio di dati
È possibile scambiare i dati tra [!INCLUDE[prod_short](includes/prod_short.md)] e flussi o file esterni in relazione alle attività aziendali, come l'invio e la ricezione di documenti elettronici e l'importazione e l'esportazione di file dalla banca.  

Prima di poter inviare e ricevere documenti elettronici o importare ed esportare file bancari, è necessario impostare il framework di scambio dati per elaborare i flussi o i file di dati. È inoltre necessario impostare aree correlate, ad esempio i clienti a cui si inviano fatture elettroniche e l'estensione AMC Banking 365 Fundamentals, qualora si distribuiscano conversioni di file bancari a un provider di servizi esterno. Per ulteriori informazioni, vedere [Impostazione dello scambio di dati](across-set-up-data-exchange.md).  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Convertire i record del documento di vendita in [!INCLUDE[prod_short](includes/prod_short.md)] in un formato standardizzato e inviarli come documenti elettronici che i clienti possono ricevere nel proprio sistema.|[Inviare documenti elettronici](sales-how-to-send-electronic-documents.md)|  
|Inviare PDF o file immagine a un provider di servizi OCR e riceverli come documenti elettronici che possono essere convertiti in record di documento in [!INCLUDE[prod_short](includes/prod_short.md)].|[Utilizzare OCR per convertire PDF e file di immagine in documenti elettronici](across-how-use-ocr-pdf-images-files.md)|  
|Ricevere i documenti elettronici dal servizio OCR o dal servizio di scambio documenti in un formato standardizzato che viene convertito nei relativi record di documento in [!INCLUDE[prod_short](includes/prod_short.md)].|[Ricevere e convertire documenti elettronici](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Preparare l'importazione di un file dell'estratto conto bancario nella pagina **Registrazione riconciliazione pagamenti** come primo passaggio della riconciliazione dei pagamenti o nella pagina **Riconciliazioni C/C bancari** come primo passaggio nella riconciliazione dei conti bancari.|[Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Esportare i pagamenti dalla pagina **Registrazioni pagamenti** in un file della banca da caricare sul conto corrente bancario elettronico per l'elaborazione.|[Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Effettuare pagamenti elettronici in base al bonifico SEPA standard per i paesi dell'UE.|[Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Indicare alla propria banca di trasferire gli importi dei pagamenti dai conti bancari dei clienti a quello della propria società in base al setup dell'addebito diretto SEPA.|[Creare movimenti riscossione addebiti diretti SEPA ed esportarli in un file della banca](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Utilizzare un provider di servizi per i tassi di cambio valuta per aggiornare la pagina **Valute**.|[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)|  
|Visualizzare di quali elementi del file viene eseguito il mapping ai campi in [!INCLUDE[prod_short](includes/prod_short.md)] durante l'importazione di file di estratto conto SEPA CAMT.|[Mapping dei campi durante l'importazione dei file SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Esportare i dati per il reporting Intrastat in [!INCLUDE[prod_short](includes/prod_short.md)].|[Impostare il reporting Intrastat](finance-how-setup-report-intrastat.md)|
|Visualizzare i campi in [!INCLUDE[prod_short](includes/prod_short.md)] di cui viene eseguito il mapping agli elementi del file durante l'esportazione dei file di pagamento tramite l'estensione AMC Banking 365 Fundamentals.|[Mappatura dei campi quando si esportano file di pagamento utilizzando l'estensione AMC Banking 365 Fundamentals](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Vedere anche
[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)   
[Registrare gli acquisti](purchasing-how-record-purchases.md)  
[Documenti in entrata](across-income-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
