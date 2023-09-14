---
title: Panoramica dei task di gestione dei pagamenti ai fornitori
description: 'Descrive i task per gestire i pagamenti ai fornitori o ai creditori, inclusa la registrazione delle righe di pagamento e la visualizzazione di una panoramica del saldo dovuto.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Effettuare i pagamenti

Quando si eseguono i pagamenti ai fornitori, ai clienti o i rimborsi ai dipendenti, si registrano le relative righe di pagamento nella pagina **Registrazioni pagamenti**. Le registrazioni pagamenti sono registrazioni generali ottimizzate per effettuare pagamenti e includono una serie di potenti funzioni come **Sugg. pagamenti fornitore** che consente di individuare i pagamenti fornitore in scadenza e il report **Fornitori - Scadenziario riepilogativo** che mostra una panoramica dei pagamenti scadenza dei fornitori.  

È possibile avviare il processo di eseguire il pagamento da elenchi, schede e movimenti contabili per fornitori, clienti e dipendenti. In ciascuna di tali pagine è presente un pulsante che avvia il flusso di pagamento e aiuta a compilare le registrazioni pagamenti.  

Dalle registrazioni pagamenti è possibile stampare assegni automatici o registrare l'emissione degli assegni. Se si seleziona **Assegno automatico** nel campo **Tipo pagamento banca**, tutte le righe che rappresentano assegni devono essere stampate prima che le registrazioni pagamenti possano essere contabilizzate.

Quando si registrano i pagamenti, è possibile esportarli in un file della banca da caricare nella banca per l'elaborazione.

Una volta effettuati i pagamenti presso la banca, è necessario collegarli ai relativi movimenti contabili fornitori o dipendenti aperti. Questa operazione può essere eseguita manualmente o importando un file del rendiconto bancario e collegando i pagamenti automaticamente. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| A | Vedere |
| --- | --- |
|Comprendere la funzioni di base della pagina **Registrazioni pagamenti**, su cui si basano le registrazioni COGE, per preparare la registrazione dei pagamenti ai fornitori o ai dipendenti.|[Utilizzare le registrazioni COGE](ui-work-general-journals.md)|
|Registrare i pagamenti ai fornitori o ai dipendenti e i rimborsi ai clienti ed eventualmente collegare i pagamenti alle fatture o note di credito non pagate correlati per consentirne la chiusura come pagate.|[Registrare pagamenti e rimborsi](payables-how-post-payments-refunds.md)|
| Utilizzare una funzione nella pagina **Registrazioni pagamenti** per suggerire i pagamenti fornitore in base ai criteri selezionati, ad esempio la data di scadenza, l'idoneità allo sconto e la liquidità. |[Sugg. pagamenti fornitore](payables-how-suggest-vendor-payments.md) |
| Emettere assegni per i pagamenti fornitore o i rimborsi ai clienti, come stampati o come assegni automatici. Annullare gli assegni prima o dopo la registrazione. |[Effettuare pagamenti tramite assegno](payables-how-work-checks.md) |
|Effettuare pagamenti elettronici in base al bonifico SEPA standard per i paesi dell'UE.|[Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Pagare un fornitore in contanti o con assegno e registrare il pagamento mentre si registra la fattura. |[Saldare immediatamente le fatture di acquisto](finance-how-to-settle-purchase-invoices-promptly.md) |
| Assicurarsi che la banca compensi solo gli assegni e gli importi convalidati inviandole un file che contenga informazioni sul fornitore, l'assegno e il pagamento. |[Esportare un file Positive Pay](finance-how-positive-pay.md) |

## Vedi il relativo [training Microsoft](/training/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## Vedere anche

[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
