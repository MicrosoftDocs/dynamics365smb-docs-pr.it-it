---
title: Panoramica della attività per gestire i pagamenti ai fornitori
description: 'Descrive i task per gestire i pagamenti ai fornitori o ai creditori, inclusa la registrazione delle righe di pagamento e la visualizzazione di una panoramica del saldo dovuto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Effettuare i pagamenti

I pagamenti a fornitori o clienti o i rimborsi ai dipendenti vengono effettuati registrando le relative righe di pagamento nella pagina **Registrazioni pagamenti**. La registrazione pagamenti è una registrazione generale ottimizzata per eseguire pagamenti e offrire molte azioni utili. Ad esempio, l'azione **Sugg. pagamenti fornitore** che trova i pagamenti del fornitore dovuti e il report **Fornitori - Scadenziario riepilogativo** che mostra una panoramica dei pagamenti dovuti ai fornitori.  

Puoi avviare il processo di pagamento da elenchi, schede e movimenti contabili per fornitori, clienti e dipendenti. In ciascuna di tali pagine è presente un pulsante che avvia il flusso di pagamento e aiuta a compilare le registrazioni pagamenti.  

Dalle registrazioni pagamenti è possibile stampare assegni automatici o registrare l'emissione degli assegni. Se selezioni **Assegno automatico** nel campo **Tipo pagamento banca**, devi stampare le righe che rappresentano assegni prima di poter contabilizzare la registrazione pagamenti.

Dopo la registrazione dei pagamenti, puoi esportarli in un file della banca che puoi caricare nella banca per l'elaborazione.

Una volta effettuati i pagamenti presso la banca, è necessario applicarli ai relativi movimenti contabili fornitori o dipendenti aperti. Questa operazione può essere eseguita manualmente o importando un file del rendiconto bancario e applicando i pagamenti automaticamente. Per ulteriori informazioni, vedere [Applicare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Nella tabella seguente viene descritta una sequenza di attività, con collegamenti agli articoli che le descrivono.

| A | Vedere |
| --- | --- |
|Comprendere la funzioni di base della pagina **Registrazioni pagamenti**, su cui si basano le registrazioni COGE, per preparare la registrazione dei pagamenti ai fornitori o ai dipendenti.|[Utilizzare le registrazioni COGE](ui-work-general-journals.md)|
|Registrare i pagamenti ai fornitori o ai dipendenti e i rimborsi ai clienti ed eventualmente applicare i pagamenti alle fatture o note di credito non pagate correlati per consentirne la chiusura come pagate.|[Registrare pagamenti e rimborsi](payables-how-post-payments-refunds.md)|
| Utilizzare una funzione nella pagina **Registrazioni pagamenti** per suggerire i pagamenti fornitore in base ai criteri selezionati, ad esempio la data di scadenza, l'idoneità allo sconto e la liquidità. |[Sugg. pagamenti fornitore](payables-how-suggest-vendor-payments.md) |
| Emettere assegni per i pagamenti fornitore o i rimborsi ai clienti, come stampati o come assegni automatici. Annullare gli assegni prima o dopo la registrazione. |[Effettuare pagamenti tramite assegno](payables-how-work-checks.md) |
|Effettuare pagamenti elettronici in base al bonifico SEPA standard per i paesi dell'UE.|[Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Pagare un fornitore in contanti o con assegno e registrare il pagamento mentre si registra la fattura. |[Saldare immediatamente le fatture di acquisto](finance-how-to-settle-purchase-invoices-promptly.md) |
| Assicurarsi che la banca compensi solo gli assegni e gli importi convalidati inviandole un file che contenga informazioni sul fornitore, l'assegno e il pagamento. |[Esportare un file Positive Pay](finance-how-positive-pay.md) |

## Vedere anche

[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
