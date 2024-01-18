---
title: Informazioni sul framework di scambio dati
description: Questo articolo spiega come utilizzare il framework di scambio dati per gestire lo scambio di dati nei documenti aziendali come le fatture con i partner aziendali.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR'
ms.search.form: '189,'
ms.date: 12/13/2023
ms.author: bholtorf
---
# <a name="about-the-data-exchange-framework"></a>Informazioni sul framework di scambio dei dati

È possibile utilizzare il framework di scambio dati per gestire lo scambio di documenti aziendali, file bancari, tassi di cambio valuta e qualsiasi altro file di dati con i propri partner commerciali o le autorità.

In qualità di amministratore o partner Microsoft, è possibile utilizzare il framework nelle nuove funzionalità di integrazione impostando quali dati scambiare e come scambiarli. Ad esempio, il formato di file per lo scambio di dati in file bancari, documenti elettronici, tassi di cambio e altro mediante i sistemi ERP varia in base al provider del file o del flusso di dati e al paese. [!INCLUDE[prod_short](includes/prod_short.md)] supporta vari formati di file bancari e standard di servizi per i dati. Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.

 Nei seguenti diagrammi viene mostrata l'architettura del framework di scambio dati.  

 ![Framework di scambio dati &#45; Importa.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Framework di scambio dati &#45; Esporta.](media/across-data-exchange/dataexchangeframework_export.png)  

## <a name="electronic-documents"></a>Documenti elettronici

In alternativa all'invio di documenti aziendali via e-mail come allegati, è possibile inviarli e riceverli elettronicamente. Un "documento elettronico" è un file conforme agli standard che rappresenta un documento aziendale, come una fattura da un venditore che si può ricevere e convertire in una fattura di acquisto in [!INCLUDE[prod_short](includes/prod_short.md)]. I partner commerciali si scambiano documenti elettronici attraverso servizi esterni di scambio di documenti. Per impostazione predefinita, [!INCLUDE[prod_short](includes/prod_short.md)] supporta l'invio e la ricezione di fatture elettroniche e note di credito nel formato PEPPOL, che è supportato dai maggiori fornitori di servizi di scambio di documenti. Un importante fornitore di servizi di scambio di documenti, Tradeshift, è preconfigurato e pronto per essere impostato per la tua azienda. Per fornire supporto ad altri formati di documenti elettronici, è necessario creare nuove definizioni di scambio dati.  

Dai PDF o dai file di immagine che rappresentano i documenti in entrata, è possibile impostare un servizio esterno OCR (Optical Character Recognition, riconoscimento ottico dei caratteri) in modo che crei documenti elettronici che è possibile convertire in record di documenti in [!INCLUDE[prod_short](includes/prod_short.md)], come per i documenti elettronici PEPPOL. Ad esempio, quando si riceve una fattura nel formato PDF dal fornitore, è possibile inviarla al servizio OCR dalla pagina **Documenti in entrata**. Dopo alcuni secondi, viene ricevuto il file come fattura elettronica che può essere convertita in una fattura di acquisto per il fornitore. Se si invia il file al servizio OCR tramite e-mail, un nuovo record del documento in entrata viene creato quando si riceve nuovamente il documento elettronico.  

Per inviare, ad esempio, una fattura di vendita come documento elettronico PEPPOL, selezionare l'opzione **Documento elettronico** nella finestra di dialogo **Registra e invia**. Nella finestra è inoltre possibile impostare il profilo di invio documenti predefinito del cliente. Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura. Questi sono usati per identificare i partner commerciali e gli elementi quando si convertono i dati nei campi in [!INCLUDE[prod_short](includes/prod_short.md)] in elementi nel file del documento in uscita. La conversione dei dati e l'invio delle fatture di vendita PEPPOL vengono eseguiti da codeunit e XMLport dedicati, rappresentati dal formato di documento elettronico **PEPPOL**.  

Per ricevere, ad esempio, la fattura da un fornitore come documento PEPPOL elettronico, occorre elaborare il documento nella pagina **Documenti in entrata** per convertirlo in una fattura di acquisto in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile impostare la funzionalità Coda processi per elaborare questi file con regolarità oppure è possibile avviare il processo manualmente. Innanzitutto, è necessario impostare diversi dati principali, come ad esempio le informazioni sulla società, i fornitori, gli articoli e le unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati presenti negli elementi del file di documento in entrata nei campi di [!INCLUDE[prod_short](includes/prod_short.md)]. La ricezione e la conversione dei dati di fatture PEPPOL vengono eseguite dalla struttura di scambio dei dati, rappresentata dalla definizione di scambio di dati **PEPPOL - Fattura**.  

  Per ricevere, ad esempio, una fattura come documento elettronico OCR, si elabora la fattura come quando si riceve un documento PEPPOL elettronico. La ricezione e la conversione dei documenti elettronici da OCR vengono eseguite dalla struttura di scambio dei dati, rappresentata dalla definizione di scambio di dati **OCR - Fattura**.  

## <a name="bank-files"></a>File della banca

I formati dei file per lo scambio di dati bancari con le applicazioni di gestione aziendale variano a seconda del fornitore del file e del paese o regione. [!INCLUDE[prod_short](includes/prod_short.md)] supporta l'importazione e l'esportazione di file bancari dell'Area unica dei pagamenti in euro (SEPA). Inoltre, l'estensione AMC Banking 365 Fundamentals permette di connettersi a un'estensione AMC Banking 365 Fundamentals fornita da un fornitore esterno, AMC Consult. Per maggiori informazioni, vedere [Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.  

Per esportare i bonifici SEPA, scegliere il pulsante **Esporta pagamenti su file** nella pagina **Registrazioni pagamenti**, quindi caricare il file per elaborare i pagamenti nella propria banca. È innanzitutto necessario impostare i dati principali, come ad esempio il conto corrente bancario, i fornitori e i metodi di pagamento. La conversione dei dati e l'esportazione dei dati bancari SEPA vengono eseguite da una codeunit e da XMLport dedicati, rappresentati dall'impostazione dell'importazione/esportazione della banca per **Bonifico SEPA**. In alternativa, è possibile impostare l'estensione AMC Banking 365 Fundamentals per eseguire l'esportazione, rappresentata dalla definizione di scambio dati **Estensione AMC Banking 365 Fundamentals - Bonifico**.  

 Per esportare le istruzioni di addebito diretto SEPA, scegliere il pulsante **Esporta file addebiti diretti** nella pagina **Riscossioni addebiti diretti**, quindi inviarlo alla propria banca in modo che raccolga automaticamente i dovuti pagamenti dei clienti. È innanzitutto necessario impostare i conti correnti bancari, i clienti, i mandati di addebito diretto e i metodi di pagamento. La conversione dei dati e l'esportazione dei dati bancari SEPA vengono eseguite da una codeunit e da XMLport dedicati, rappresentati dall'impostazione dell'importazione/esportazione della banca per **Addebito diretto SEPA**.  

 Per importare gli estratti conto bancari SEPA, scegliere il pulsante Importa rendiconto bancario nelle pagine **Registrazione riconciliazione pagamenti** e **Riconciliazioni C/C bancari**, quindi applicare ciascuna voce dell'estratto conto ai pagamenti o ai movimenti contabili bancari, manualmente o automaticamente. Innanzitutto è necessario impostare i conti correnti bancari. L'importazione e la conversione dei dati bancari SEPA vengono eseguite dalla struttura di scambio dei dati, rappresentata dalla definizione dello scambio di dati **SEPA CAMT**. In alternativa, è possibile impostare l'estensione AMC Banking 365 Fundamentals per eseguire l'importazione, rappresentata dalla definizione di scambio dati **Estensione AMC Banking 365 Fundamentals - Estratto conto bancario**.  

 Inoltre, le versioni locali di [!INCLUDE[prod_short](includes/prod_short.md)] supportano vari altri formati di file per l'importazione e l'esportazione dei dati bancari, le transazioni retributive e altri dati. Per ulteriori informazioni, vedere la pagina di destinazione [Funzionalità locale](about-localization.md) nella Guida.  

## <a name="currency-exchange-rates"></a>Tassi di cambio valuta

È possibile impostare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute. Il servizio che fornisce i tassi di cambio delle valute aggiornati è abilitato in base a una definizione di scambio di dati. Di conseguenza, la pagina **Setup aggiornamento tasso di cambio in valuta** offre una visualizzazione condensata della pagina **Definizione scambio di dati** per la definizione di scambio dati in questione.  

Per tutti gli scambi di dati in file XML, è possibile preparare le impostazioni di scambio dati caricando il file di schema XML correlato nella pagina **Visualizzatore schema XML**. Qui è possibile selezionare gli elementi dati che si desidera scambiare con [!INCLUDE[prod_short](includes/prod_short.md)], quindi inizializzare la definizione di scambio di dati o generare un oggetto XMLport.

## <a name="intrastat"></a>Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] utilizza Framework di scambio dei dati per i report Intrastat in cui è possibile creare facilmente file con timestamp in diversi formati per l'esportazione. [!INCLUDE[prod_short](includes/prod_short.md)] contiene formati preparati per i paesi o le aree geografiche localizzate e per la versione predefinita. Ma puoi modificare il report predefinito o crearne uno tuo.

## <a name="see-also"></a>Vedere anche

[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Usare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Documenti in entrata](across-income-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
