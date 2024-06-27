---
title: Panoramica delle attività per gestire la contabilità clienti
description: Questo articolo descrive le attività per gestire gli incassi e collegare i pagamenti a movimenti contabili cliente o fornitore.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'customer payment, debtor, balance due, AR'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="managing-receivables"></a>Gestione della contabilità clienti

Un passaggio regolare in qualsiasi scenario finanziario è riconciliare i conti bancari. Per chiudere le fatture di vendita e le note di credito di acquisto come pagate, colleghi pagamenti in entrata ai movimenti contabili clienti o fornitori.

Poiché la maggior parte dei clienti negli ambienti di B2B pagano un certo periodo dopo la consegna, lasciando le fatture di vendita registrate aperte per il reparto Contabilità clienti da chiudere (collegare) quando viene ricevuto il pagamento, alcune fatture di vendita possono essere pagate immediatamente, ad esempio nel caso di pagamenti tramite PayPal. Tali fatture vengono immediatamente collegate come pagate quando vengono registrate e, pertanto, non appaiono come pagamenti da elaborare in Contabilità clienti. Per ulteriori informazioni, vedere, ad esempio, [Fatturare le attività di vendita](sales-how-invoice-sales.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] uno dei modi più rapidi per registrare i pagamenti nella pagina **Registrazione riconciliazione pagamenti** consiste nell'importare un file di rendiconto bancario o un feed. I pagamenti sono collegati ai movimenti contabili aperti per clienti o fornitori in base alle corrispondenze tra il testo di pagamento e le informazioni del movimento. È possibile esaminare e modificare le corrispondenze prima di contabilizzare le registrazioni e chiudere i movimenti dei conti correnti bancari per i movimenti contabili quando tale registrazione viene contabilizzata. Il conto bancario viene riconciliato una volta che tutti i pagamenti sono collegati.

Sono disponibili altre pagine in cui è possibile collegare i pagamenti o riconciliare i conti bancari:

* La pagina **Riconciliazione C/C bancari** in cui si possono riconciliare i conti bancari abbinando le righe dell'estratto conto bancario con i movimenti contabili del conto bancario di sistema. Qui è possibile anche riconciliare i pagamenti con assegni. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md). Qui non è possibile collegare i pagamenti.
* La pagina **Registrazione pagamenti** nella quale è possibile collegare manualmente i pagamenti ricevuti come contante, assegno o transazione bancaria rispetto a una lista generata di documenti di vendita non pagati. Questa funzionalità è disponibile solo per i documenti di vendita. Qui non è possibile collegare pagamenti in uscita e non è possibile riconciliare i conti correnti bancari.
* La pagina **Registrazioni incassi**, nella quale vengono registrate manualmente le ricezioni nel relativo conto COGE, cliente o altro conto immettendo una riga di pagamento. È possibile collegare la ricezione o il rimborso a uno o più movimenti aperti prima di contabilizzare le registrazioni incassi oppure è possibile eseguire il collegamento dai movimenti contabili clienti. Qui non è possibile riconciliare i conti correnti bancari.

La pagina **Registrazione riconciliazione pagamenti** utilizza la logica di corrispondenza automatica che è possibile impostare nella pagina **Regole di collegamento pagamenti**. Per ulteriori informazioni, vedere [Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md).  

Altri aspetti della gestione dei crediti includono la riscossione di saldi inevasi, tra cui solleciti e addebiti interessi, nonché l'impostazione di conti correnti bancari per consentire il prelevamento automatico dei pagamenti dei clienti dai relativi conti.

Nella tabella seguente viene descritta una sequenza di attività, con collegamenti agli articoli che le descrivono.  

| A | Vedere |
| --- | --- |
| Collegare pagamenti a movimenti contabili aperti di clienti o fornitori in base a un file o feed di estratto conto importato. Riconciliare il conto corrente bancario dopo aver collegato tutti i pagamenti. |[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Collegare i pagamenti a movimenti contabili clienti aperti in base a una lista di documenti di vendita non pagati nella pagina **Registrazione pagamenti**. |[Riconciliare i pagamenti dei clienti dall'elenco dei documenti di vendita non pagati](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Registrare gli incassi o i rimborsi per i clienti nelle registrazioni incassi e collegare ai movimenti contabili clienti, dalle registrazioni o dai movimenti contabili registrati. |[Riconciliare i pagamenti clienti con la registrazione incassi o da movimenti contabili clienti](receivables-how-apply-sales-transactions-manually.md) |
| Inviare solleciti ai clienti per gli importi insoluti, calcolare interessi e addebiti interessi e gestire i crediti v/clienti. |[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md) |
|Con il consenso del cliente, è possibile riscuotere i pagamenti direttamente dal conto bancario del cliente, solo in Euro.|[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)|
|Blocca l'immissione di un cliente nei documenti o nella registrazione, ad esempio a causa di insolvibilità.|[Blocca clienti](receivables-how-block-customers.md)|
|Impostare una tolleranza da cui il sistema chiude una fattura anche se il pagamento, incluso un eventuale sconto, non copre interamente l'importo della fattura.|[Usare le tolleranze pagamento e le tolleranze sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Prevedere quando i pagamenti verranno ritardati per i documenti di vendita. | [Estensione Previsione pagamento ritardato](ui-extensions-late-payment-prediction.md) |

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
