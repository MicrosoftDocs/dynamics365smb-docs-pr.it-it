---
title: Panoramica delle attività per la gestione degli acquisti
description: 'Descrive i task di gestione dei processi di acquisto o approvvigionamento, incluso l''utilizzo delle fatture di acquisto e degli ordini di acquisto.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="purchasing"></a>Acquisti

È possibile creare una fattura o un ordine di acquisto per registrare il costo di acquisto e per tenere traccia del conto fornitori. Se è necessario verificare un magazzino, anche le fatture di acquisto vengono utilizzate per aggiornare in modo dinamico i livelli di magazzino in modo da ridurre i costi di magazzino al minimo e migliorare l'assistenza clienti. I costi di acquisto, incluse le spese di assistenza, e i valori di magazzino derivanti dalla registrazione delle fatture di acquisto contribuiscono alle cifre di profitto e altri indicatori KPI finanziari in Gestione ruolo utente.

Utilizzare gli ordini di acquisto se il processo di acquisto richiede la registrazione delle le ricevute parziali di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile presso il fornitore. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di acquisto. Per ulteriori informazioni, vedere [Effettuare spedizioni dirette](sales-how-drop-shipment.md). In tutti gli altri aspetti, gli ordini di acquisto funzionano come le fatture di acquisto.

È possibile creare le fatture di acquisto automaticamente utilizzando il servizio OCR (riconoscimento ottico dei caratteri) per convertire le fatture PDF ricevute dai fornitori in documenti elettronici, che verranno successivamente convertiti in fatture di acquisto da un workflow. Per utilizzare questa funzionalità, è necessario innanzitutto iscriversi al servizio OCR e quindi impostare varie impostazioni. Per ulteriori informazioni, vedi [Documenti in entrata](across-income-documents.md).

I prodotti possono essere sia articoli di magazzino che servizi. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

Per tutti i processi di acquisto, è possibile incorporare un workflow di approvazione, ad esempio, per richiedere che gli acquisti di grande volume siano approvati dal responsabile della contabilità. Per ulteriori informazioni, vedere [Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md).

Nella sezione seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.

## <a name="get-started-with-purchase-capabilities"></a>Iniziare con le funzionalità per l'acquisto

Prima di acquistare la merce, specifica come vuoi gestire i processi di acquisto della tua azienda.

|Per...| Vedere |
|---|---|
| Configura ruoli e valori che definiscono i criteri di acquisto della società. | [Impostare gli acquisti](purchasing-setup-purchasing.md) |
| Registra ogni fornitore da cui si acquista con una scheda fornitore. | [Registrare nuovi fornitori](purchasing-how-register-new-vendors.md) |

## <a name="purchase-analytics"></a>Analisi degli acquisti

In questa sezione vengono descritti gli strumenti analitici che puoi utilizzare per ottenere informazioni dettagliate sui processi di acquisto.

| Per... | Vedere |
| --- | --- |
| Scopri le funzionalità per l'analisi dei dati di acquisto. | [Panoramica dell'analisi degli acquisti](purchasing-analytics-overview.md) |
| Esegui analisi ad hoc dei dati di acquisto direttamente nelle pagine di elenco e nelle query. | [Analisi ad hoc dei dati sugli acquisti](ad-hoc-analysis-purchasing.md) |
| Esplora report sul'acquisto integrati. | [Report degli acquisti predefiniti](purchase-reports.md) |

## <a name="quote-to-order-to-purchase-invoice"></a>Offerta su ordine nella fattura di acquisto

La tabella seguente descrive come utilizzare semplici processi di acquisto.

| A | Vedere |
| --- | --- |
|Creare un'offerta di acquisto per riflettere una richiesta di offerta di un fornitore che è possibile convertire successivamente in ordine di acquisto.|[Richiedere le offerte](purchasing-how-request-quotes.md)|
| Creare una fattura di acquisto per tutte le righe o quelle selezionate in una fattura di vendita. |[Acquistare articoli per una vendita](purchasing-how-purchase-products-sale.md) |
| Creare una fattura di acquisto per registrare il contratto con un fornitore per acquistare prodotti con determinate condizioni di consegna e pagamento. |[Registrare gli acquisti](purchasing-how-record-purchases.md) |
| Informazioni su come vengono effettuati i calcoli [!INCLUDE[prod_short](includes/prod_short.md)] quando è necessario ordinare un articolo per riceverlo in una determinata data.|[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)|
|Capire cosa accade quando si registrano documenti di acquisto.|[Registrazione di acquisti](ui-post-purchases.md)|

Se hai bisogno di processi di acquisto più complessi, la tabella seguente elenca gli articoli che spiegano cosa puoi fare [!INCLUDE[prod_short](includes/prod_short.md)].

| A | Vedere |
| --- | --- |
| Eseguire un'azione in una fattura di acquisto registrata non pagata per creare automaticamente una nota di credito e per annullare la fattura di acquisto o per ricrearla in modo da apportare correzioni. |[Correggere o annullare le fatture di vendita non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Creare una nota di credito di acquisto per stornare una fattura di acquisto registrata specifica per riflettere i prodotti resi al fornitore e l'importo di pagamento che verrà ricevuto. |[Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md) |
|Gestire l'impegno di un fornitore per acquistare grandi quantità consegnate nel tempo in diverse spedizioni.|[Usare gli ordini di acquisto programmati](sales-how-to-create-blanket-sales-orders.md)|


## <a name="canceled-orders-refunds-and-returns"></a>Ordini annullati, rimborsi e resi

La seguente tabella descrive come gestire gli ordini annullati, i rimborsi e i resi dei beni acquistati.

| A | Vedere |
| --- | --- |
|Preparare la fattura per più carichi dallo stesso fornitore dopo aver combinato i carichi in una sola fattura.|[Combinare i carichi in una singola fattura](purchasing-how-to-combine-receipts.md)|
|Convertire, ad esempio, le fatture elettroniche dei fornitori in fatture di acquisto in Business Central.|[Ricevere e convertire documenti elettronici](purchasing-how-to-receive-and-convert-electronic-documents.md)|


## <a name="other-processes-in-sales"></a>Altri processi nelle vendite

La tabella seguente descrive come gestire altri processi di acquisto.

| A | Vedere |
| --- | --- |
|Eliminare la confusione quando due o più record sono presenti per lo stesso fornitore.|[Unire record duplicati](sales-how-merge-duplicate-records.md)|


## <a name="external-document-numbers"></a>Numeri di documento esterno

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-also"></a>Vedere anche

[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Panoramica dell'analisi degli acquisti](purchasing-analytics-overview.md)   
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
