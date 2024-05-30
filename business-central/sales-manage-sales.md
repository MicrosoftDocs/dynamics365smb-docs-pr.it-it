---
title: Panoramica delle attività per gestire le vendite
description: 'Leggi come utilizzare i servizi di Business Central per la gestione delle attività di vendita dei tuoi clienti con fatture di vendita, ordini, offerte e altro.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'trade, sell'
ms.search.form: '253,'
ms.date: 01/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="sales"></a>Vendite

Si crea una fattura di vendita o un ordine di vendita per registrare il contratto con un cliente per vendere alcuni prodotti con determinate condizioni di consegna e pagamento.

È necessario utilizzare gli ordini di vendita se il processo di vendita richiede la spedizione di parti di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile immediatamente. Se si vendono articoli con consegna diretta dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di vendita. In tutti gli altri aspetti, gli ordini di vendita funzionano come le fatture di vendita. Con gli ordini di vendita è possibile anche utilizzare la funzionalità Promesse ordine per comunicare determinate date di consegna ai clienti.  

È possibile negoziare con il cliente prima di tutto creando un'offerta di vendita, che è possibile convertire in una fattura di vendita o un ordine di vendita quando ci si accorda sulla vendita. Dopo che il cliente ha confermato il contratto, è possibile inviare una conferma dell'ordine per registrare l'obbligo di consegnare i prodotti come concordato.

È possibile correggere o annullare in modo semplice una fattura di vendita registrata prima del pagamento del cliente. Ad esempio, per correggere un errore di digitazione o se il cliente richiede una modifica in anticipo nell'elaborazione dell'ordine. Se la fattura di vendita registrata è stata pagata, allora sarà necessario creare una nota di credito di vendita o un ordine di reso da vendita per stornare la vendita.

Per garantire la buona riuscita delle iniziative di marketing e la chiusura delle vendite, è fondamentale prendere le decisioni ottimali nel momento appropriato. La funzionalità di marketing in [!INCLUDE[prod_short](includes/prod_short.md)] offre un quadro accurato e tempestivo delle informazioni sui contatti consentendo di presentarsi in modo efficace a potenziali clienti, nonché di incrementare il livello di soddisfazione dei clienti. Ulteriori informazioni in [Relationship Management](marketing-relationship-management.md).

Se si utilizza Microsoft Dynamics 365 Sales per l'interazione con i clienti, puoi sfruttare un'integrazione ottimale nel processo dai lead agli incassi utilizzando [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio, per elaborare gli ordini, gestire l'inventario e gestire le tue finanze. Scopri di più in [Utilizzare Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md).

Negli ambienti aziendali in cui il cliente deve pagare prima che vengano consegnati i prodotti, ad esempio nelle vendita al dettaglio, è necessario attendere la ricezione del pagamento prima di consegnare i prodotti. Nella maggior parte dei casi, i pagamenti in entrata vengono elaborati alcune settimane dopo la consegna collegando i pagamenti alle relative fatture di vendita non pagate registrate. Ulteriori informazioni in [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

I documenti di vendita possono essere inviati come file PDF allegati all'e-mail. Il corpo e-mail contiene un estratto del documento di vendita, ad esempio i prodotti, l'importo totale e un collegamento al sito di PayPal. Ulteriori informazioni in [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Per tutti i processi di vendita, puoi incorporare un flusso di lavoro di approvazione. Ad esempio, un flusso di lavoro di approvazione può richiedere che un responsabile approvi le vendite di grandi dimensioni a determinati clienti. Ulteriori informazioni in [Utilizzare i flussi di lavoro](across-use-workflows.md).

Nella sezione seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.

## <a name="get-started-with-sales-capabilities"></a>Iniziare con le funzionalità delle vendite

Prima di vendere, specifica come vuoi gestire i processi di vendita della tua azienda.

|Per...| Vedere |
|---|---|
| Creare una scheda cliente per ogni cliente a cui si effettua una vendita.|[Registrare nuovi clienti](sales-how-register-new-customers.md) |
| Configura la modalità di vendita, ad esempio prezzi e sconti, prezzo cliente e gruppi di sconto, venditori, metodi di spedizione e agenti. | [Impostare le vendite](sales-setup-sales.md) |

## <a name="sales-analytics"></a>Analisi delle vendite

In questa sezione vengono descritti gli strumenti analitici che puoi utilizzare per ottenere informazioni dettagliate sui dati delle vendite.

| Per... | Vedere |
| --- | --- |
| Scopri le funzionalità per l'analisi dei dati delle vendite. | [Panoramica dell'analisi delle vendite](sales-analytics-overview.md) |
| Esegui analisi ad hoc dei dati delle vendite direttamente nelle pagine di elenco e nelle query. | [Creare report di analisi delle vendite](bi-how-create-analysis-views-reports.md) |
| Esplora i report delle vendite integrati. | [Report delle vendite predefiniti](sales-reports.md) |

## <a name="quote-to-order-to-sales-invoice"></a>Offerta su ordine nella fattura di vendita

La tabella seguente descrive come utilizzare semplici processi di vendita.

|Per...| Vedere |
|---|---|
| Creare un'offerta di vendita in cui si presentano prodotti a condizioni negoziabili prima della conversione dell'offerta in una fattura di vendita. |[Creare offerte di vendita](sales-how-make-offers.md) |
| Elaborare un ordine di vendita (magari con una spedizione parziale o utilizzando una spedizione diretta). |[Vendere prodotti](sales-how-sell-products.md) |
| Creare una fattura di vendita per registrare il contratto con un cliente per vendere prodotti con determinate condizioni di consegna e pagamento. |[Fatturazione delle vendite](sales-how-invoice-sales.md) |
|Capire cosa accade quando si registrano documenti di vendita.|[Registrazione di vendite](ui-post-sales.md)|

Se hai bisogno di processi di vendita più complessi, la tabella seguente elenca gli articoli che spiegano cosa puoi fare [!INCLUDE[prod_short](includes/prod_short.md)].

|Per...| Vedere |
|---|---|
| Soddisfare un ordine di vendita con più spedizioni parziali. | [Elaborare spedizioni parziali](sales-how-send-partial-shipments.md) |
| Impostare righe di vendita o acquisto standard da inserire nei documenti, ad esempio, per ordini di approvvigionamento ricorrenti.|[Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md)|  
|Gestire l'impegno del cliente per acquistare grandi quantità consegnate nel tempo in diverse spedizioni.|[Usare gli ordini di vendita programmati](sales-how-to-create-blanket-sales-orders.md)|
|Fatturare al cliente una volta per più spedizioni combinando le spedizioni in una sola fattura.|[Combinare le spedizioni in una singola fattura](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Vendi gli articoli di assemblaggio che al momento non sono disponibili creando un ordine di assemblaggio. L'ordine di assemblaggio può fornire la quantità totale o parziale dell'ordine cliente.|[Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md)|

## <a name="pick-and-ship"></a>Preleva e spedisci

Nella tabella seguente viene descritto come prelevare gli articoli per un ordine cliente e spedirli al cliente.

| A | Vedere |
| --- | --- |
|Prepararsi a prelevare articoli per la spedizione.|[Stampare la lista prelievo](sales-how-print-picking-list.md)|
| Collegare un ordine di vendita a un ordine di acquisto per vender un articolo con spedizione diretta che verrà consegnato direttamente dal fornitore al cliente. |[Effettuare spedizioni dirette](sales-how-drop-shipment.md) |
|Ricevere un articolo di catalogo spedito da un fornitore al magazzino in modo da spedire l'articolo al cliente.|[Creare ordini speciali](sales-how-to-create-special-orders.md)|
|Comunicare ai clienti le date di consegna dell'ordine calcolando la data CTP (Capable-To-Promise) o ATP (Available-To-Promise).|[Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)|
| Scopri come tene traccia di un pacco da una spedizione di vendita registrata. | [Rintracciare i colli](sales-how-track-packages.md) |

## <a name="canceled-orders-refunds-and-returns"></a>Ordini annullati, rimborsi e resi

La seguente tabella descrive come gestire gli ordini annullati, i rimborsi e i resi dei beni.

| A | Vedere |
| --- | --- |
| Eseguire un'azione in una fattura di vendita registrata non pagata per creare automaticamente una nota di credito e per annullare la fattura di vendita o per ricrearla in modo da apportare correzioni. |[Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md) |
| Creare una nota di credito vendita per stornare una fattura di vendita registrata specifica per riflettere i prodotti resi dal cliente e l'importo del rimborso. |[Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md) |

## <a name="other-processes-in-sales"></a>Altri processi nelle vendite

La tabella seguente descrive come gestire altri processi di vendita.

| A | Vedere |
| --- | --- |
|Eliminare la confusione quando due o più record sono presenti per lo stesso cliente.|[Unire record duplicati](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Vedere anche

[Setup Vendite](sales-setup-sales.md)  
[Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Panoramica delle analisi delle vendite](sales-analytics-overview.md)   
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
