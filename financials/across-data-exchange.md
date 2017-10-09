---
title: Documenti elettronici in Dynamics 365 for Financials | Microsoft Docs
description: Introduzione all'invio e alla ricezione di documenti elettronici in [!INCLUDE[d365fin](includes/d365fin_md.md)].
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
ms.openlocfilehash: 0c0ca1b5da823d31bba4961e8724dfb98e842317
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
## <a name="exchanging-data-as-electronic-documents"></a>Scambio di dati come documenti elettronici  
Come alternativa all'invio tramite e-mail dei file come allegati, è possibile inviare e ricevere documenti elettronicamente. Per documento elettronico si intende un file conforme agli standard che rappresenta un documento aziendale, come ad esempio la fattura di un fornitore che può essere ricevuta e convertita in fattura di acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lo scambio di documenti elettronici tra due partner commerciali viene eseguito da un provider esterno dei servizi di Exchange per documenti. La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta l'invio e la ricezione delle fatture e delle note di credito elettroniche e la ricezione delle fatture elettroniche nel formato PEPPOL, che è supportato dai principali provider di servizi di Exchange per documenti. Un provider importante dei servizi di Exchange per documenti è preconfigurato e pronto per l'installazione nell'azienda. Per fornire il supporto per altri formati di documento elettronico, è necessario creare nuove definizioni di scambio dati utilizzando il framework di scambio dati.  

Dai PDF o dai file di immagine che rappresentano i documenti in entrata, è possibile impostare un servizio esterno OCR (Optical Character Recognition, riconoscimento ottico dei caratteri) in modo che crei documenti elettronici che è possibile convertire in record di documenti in [!INCLUDE[d365fin](includes/d365fin_md.md)], come per i documenti elettronici PEPPOL. Ad esempio, quando si riceve una fattura nel formato PDF dal fornitore, è possibile inviarla al servizio OCR dalla finestra **Documenti in entrata**. Dopo alcuni secondi, viene ricevuto il file come fattura elettronica che può essere convertita in una fattura di acquisto per il fornitore. Se si invia il file al servizio OCR tramite e-mail, un nuovo record del documento in entrata viene creato quando si riceve nuovamente il documento elettronico.  

Per inviare, ad esempio, una fattura di vendita come documento elettronico PEPPOL, selezionare l'opzione **Documento elettronico** nella finestra di dialogo **Registra e invia**. Nella finestra è inoltre possibile impostare il profilo di invio documenti predefinito del cliente. Innanzitutto, è necessario impostare diversi dati principali, ad esempio le informazioni sulla società, i clienti, gli articoli e le unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati nei campi di [!INCLUDE[d365fin](includes/d365fin_md.md)] in articoli nel file di documento in uscita. La conversione dei dati e l'invio delle fatture di vendita PEPPOL vengono eseguiti da codeunit e XMLport dedicati, rappresentati dal formato di documento elettronico **PEPPOL**.  

Per ricevere, ad esempio, la fattura da un fornitore come documento PEPPOL elettronico, occorre elaborare il documento nella finestra **Documenti in entrata** per convertirlo in una fattura di acquisto in [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile impostare la funzionalità Coda processi per elaborare questi file con regolarità oppure è possibile avviare il processo manualmente. Innanzitutto, è necessario impostare diversi dati principali, come ad esempio le informazioni sulla società, i fornitori, gli articoli e le unità di misura. Questi dati vengono utilizzati per identificare i partner commerciali e gli articoli durante la conversione dei dati presenti negli elementi del file di documento in entrata nei campi di [!INCLUDE[d365fin](includes/d365fin_md.md)]. La ricezione e la conversione dei dati di fatture PEPPOL vengono eseguite dalla struttura di scambio dei dati, rappresentata dalla definizione di scambio di dati **PEPPOL - Fattura**.  

 Per ricevere, ad esempio, una fattura come documento elettronico OCR, si elabora la fattura come quando si riceve un documento PEPPOL elettronico. La ricezione e la conversione dei documenti elettronici da OCR vengono eseguite dalla struttura di scambio dei dati, rappresentata dalla definizione di scambio di dati **OCR - Fattura**.  

## <a name="bank-files"></a>File della banca  
 I formati di file per lo scambio di dati bancari con i sistemi ERP variano a seconda del fornitore del file e a seconda del paese o dell'area geografica. La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta l'importazione e l'esportazione dei file della banca SEPA (Single Euro Payments Area) e un servizio di conversione dati bancari fornito da AMC Consult, un provider esterno. Per fornire supporto per altri formati di documenti elettronici, è possibile utilizzare il framework di scambio dati.  

Per esportare i bonifici SEPA, scegliere il pulsante **Esporta pagamenti su file** nella finestra **Registrazioni pagamenti**, quindi caricare il file per elaborare i pagamenti nella propria banca. È innanzitutto necessario impostare i dati principali, come ad esempio il conto corrente bancario, i fornitori e i metodi di pagamento. La conversione dei dati e l'esportazione dei dati bancari SEPA vengono eseguite da una codeunit e da XMLport dedicati, rappresentati dall'impostazione dell'importazione/esportazione della banca per **Bonifico SEPA**. In alternativa, è possibile impostare il servizio di conversione dati bancari per eseguire l'esportazione, rappresentata dalla definizione dello scambio di dati **Servizio di conversione dati bancari - Bonifico**.  

Per esportare le istruzioni di addebito diretto SEPA, scegliere il pulsante **Esporta file addebiti diretti** nella finestra **Riscossioni addebiti diretti**, quindi inviarlo alla propria banca in modo che raccolga automaticamente i dovuti pagamenti dei clienti. È innanzitutto necessario impostare i conti correnti bancari, i clienti, i mandati di addebito diretto e i metodi di pagamento. La conversione dei dati e l'esportazione dei dati bancari SEPA vengono eseguite da una codeunit e da XMLport dedicati, rappresentati dall'impostazione dell'importazione/esportazione della banca per **Addebito diretto SEPA**.  

Per importare gli estratti conto bancari SEPA, scegliere il pulsante Importa rendiconto bancario nelle finestre **Registrazione riconciliazione pagamenti** e **Riconciliazioni C/C bancari**, quindi applicare ciascuna voce dell'estratto conto ai pagamenti o ai movimenti contabili bancari, manualmente o automaticamente. Innanzitutto è necessario impostare i conti correnti bancari. L'importazione e la conversione dei dati bancari SEPA vengono eseguite dalla struttura di scambio dei dati, rappresentata dalla definizione dello scambio di dati **SEPA CAMT**. In alternativa, è possibile impostare il servizio di conversione dati bancari per eseguire l'importazione, rappresentata dalla definizione dello scambio di dati **Servizio di conversione dati bancari - Rendiconto bancario**.  

 Inoltre, le versioni locali di [!INCLUDE[d365fin](includes/d365fin_md.md)] supportano vari altri formati di file per l'importazione/esportazione dei dati bancari, le transazioni retributive e altri dati. Per altre informazioni, vedere la sezione della Guida "Funzionalità locale" nella versione di [!INCLUDE[d365fin](includes/d365fin_md.md)] del proprio paese.  

## <a name="currency-exchange-rates"></a>Tassi di cambio valuta  
È possibile impostare un servizio esterno per mantenere aggiornati i tassi di cambio delle valute. Il servizio che fornisce i tassi di cambio delle valute aggiornati è abilitato in base a una definizione di scambio di dati. Di conseguenza, la finestra **Setup aggiornamento tasso di cambio in valuta** offre una visualizzazione condensata della finestra **Definizione scambio di dati** per la definizione di scambio dati in questione.  

Per tutti gli scambi di dati in file XML, è possibile preparare le impostazioni di scambio dati caricando il file di schema XML correlato nella finestra **Visualizzatore schema XML**. Qui è possibile selezionare gli elementi dati che si desidera scambiare con [!INCLUDE[d365fin](includes/d365fin_md.md)], quindi inizializzare la definizione di scambio di dati o generare un oggetto XMLport.  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|A|Vedere|  
|--------|---------|  
|Informazioni sul funzionamento della struttura di scambio di dati (Data Exchange Framework).|[Informazioni sul framework di scambio dati](across-about-the-data-exchange-framework.md)|  
|Preparare lo scambio di dati in un file riutilizzando lo schema XML del file. Impostare le definizioni di scambio dei dati. Impostare i dati principali per l'invio dei documenti elettronici. Impostare vari campi di importazione/esportazione della banca.|[Impostare lo scambio di dati](across-set-up-data-exchange.md)|  
|In base alle definizioni di scambio dei dati, inviare le fatture PEPPOL, ricevere le fatture PEPPOL, importare gli estratti conto bancari ed esportare i file di pagamento bancario.|[Scambiare dati](across-exchange-data.md)|  

## <a name="see-also"></a>Vedi anche  
[Informazioni sul framework di scambio dati](across-about-the-data-exchange-framework.md)  
[Procedura: Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Impostare lo scambio di dati](across-set-up-data-exchange.md)  
[Scambiare dati](across-exchange-data.md)  
[Documenti in entrata](across-income-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

