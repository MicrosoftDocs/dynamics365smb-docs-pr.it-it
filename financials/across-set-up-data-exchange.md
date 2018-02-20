---
title: Impostare lo scambio di dati | Microsoft Docs
description: Impostare il framework di scambio dati in Finance and Operations, Business edition.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a043ad387455cf93182689b0c58025be7186c0cd
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-data-exchange"></a>Impostazione dello scambio di dati
Prima di poter inviare e ricevere documenti elettronici o importare ed esportare file della banca, è necessario impostare il framework di scambio dati per elaborare i file interessati. Inoltre, è necessario impostare le aree correlate, ad esempio i dati principali per i clienti a cui si inviano fatture elettroniche o il servizio di conversione dati bancari nel caso in cui si utilizzi il provider di servizi esterno per convertire i propri file bancari. Per ulteriori informazioni, vedere [Scambio di dati in modalità elettronica](across-data-exchange.md).  

 Se [!INCLUDE[d365fin](includes/d365fin_md.md)] è impostato per scambiare i dati con file esterni, gli utenti possono utilizzare l'impostazione in task aziendali comuni, ad esempio l'invio e la ricezione di documenti elettronici, nonché l'importazione e l'esportazione di file bancari.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare il servizio di scambio documenti preconfigurato per abilitare l'invio e la ricezione dei documenti elettronici da e a [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Impostare un servizio di scambio documenti](across-how-to-set-up-a-document-exchange-service.md)|  
|Configurare il servizio OCR preconfigurato per convertire i file PDF o di immagine in documenti elettronici che possono essere convertiti in record di documento in . [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Impostare documenti in entrata](across-how-setup-income-documents.md)|  
|Configurare uno dei due servizi preconfigurati per i tassi di cambio aggiornati in modo da ottenere i tassi di cambio valuta più recenti nella finestra **Valute**.|[Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md)|  
|È necessario impostare diversi dati master, ad esempio le informazioni sulla società, i clienti, i fornitori, gli articoli e le unità di misura correlati ai dati di mapping in  [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Impostare l'invio e la ricezione di documenti elettronici](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Impostare un conto corrente bancario, un fornitore e le registrazioni pagamenti per bonifici SEPA.|[Impostare un bonifico SEPA](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Preparare i formati dei conti bancari, i metodi di pagamento e gli accordi con i clienti per l'addebito diretto SEPA.|[Impostare gli addebiti diretti SEPA](finance-how-to-set-up-sepa-direct-debit.md)|  
|Impostare l'autenticazione utente e l'URL del provider di servizi di conversione di dati bancari che è necessario per convertire i file della banca nel formato della banca in uso.|[Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-data-conversion-service.md)|  
|Impostare e abilitare un servizio esterno che consente di importare gli estratti conto bancari direttamente come feed bancari.|[Impostazione del Servizio rendiconti bancari](bank-how-setup-bank-statement-service.md)|  
|Dopo che il servizio Rendiconto bancario è abilitato, collegare i conti bancari in  [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md)|  
|Preparare l'impostazione di una nuova definizione di scambio di dati per un file o un flusso di dati utilizzando lo schema XML del file per precompilare la Scheda dettaglio **Definizioni colonne** nella finestra **Registrazione definizioni di scambio**.|[Utilizzare gli schemi XML per preparare le definizioni di scambio dati](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Impostare il framework di scambio dei dati per consentire agli utenti di ricevere un nuovo formato di documenti di acquisto, inviare un nuovo formato di documenti di vendita, importare un nuovo file bancario o altri tipi di scambio di dati.|[Impostare le definizioni di scambio dati](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Vedi anche  
[Scambio di dati in modalità elettronica](across-data-exchange.md)  
[Scambio di dati](across-exchange-data.md)   
[Documenti in entrata](across-income-documents.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

