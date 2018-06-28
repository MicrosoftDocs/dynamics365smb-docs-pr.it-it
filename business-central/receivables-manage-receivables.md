---
title: Panoramica dei task per la gestione degli incassi | Documenti Microsoft
description: Descrive i task per gestire gli incassi e collegare il pagamento ai movimenti contabili cliente o fornitore.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 01a195130a6834256b30efea8c06841c88af354d
ms.contentlocale: it-it
ms.lasthandoff: 05/15/2018

---
# <a name="managing-receivables"></a>Gestione della contabilità clienti
Un passaggio normale nell'iter finanziario consiste nel riconciliare i conti correnti bancari. Per questa operazione è necessario che i pagamenti in entrata vengano collegati ai movimenti del registro fornitori o clienti in modo da chiudere le fatture di vendita e le note di credito di acquisto come pagate.

Poiché la maggior parte dei clienti negli ambienti di B2B pagano un certo periodo dopo la consegna, lasciando le fatture di vendita registrate aperte per il reparto Contabilità clienti da chiudere (collegare) quando viene ricevuto il pagamento, alcune fatture di vendita possono essere pagate immediatamente, ad esempio nel caso di pagamenti tramite PayPal. Tali fatture vengono immediatamente collegate come pagate quando vengono registrate e, pertanto, non appaiono come pagamenti da elaborare in Contabilità clienti. Per ulteriori informazioni, vedere, ad esempio, [Fatturare le attività di vendita](sales-how-invoice-sales.md).  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] uno dei modi più rapidi per registrare pagamenti nella finestra **Registrazione riconciliazione pagamenti** consiste nell'importare un file di rendiconto bancario o un feed. I pagamenti sono collegati ai movimenti contabili aperti per clienti o fornitori in base alle corrispondenze tra il testo di pagamento e le informazioni del movimento. È possibile esaminare e modificare le corrispondenze prima di contabilizzare le registrazioni e chiudere i movimenti dei conti correnti bancari per i movimenti contabili quando tale registrazione viene contabilizzata. Il conto bancario viene riconciliato una volta che tutti i pagamenti sono collegati.

Sono disponibili altre finestre in cui è possibile collegare i pagamenti o riconciliare i conti bancari:

* La finestra **Riconciliazione C/C bancari** in cui si possono riconciliare i conti bancari abbinando le righe dell'estratto conto bancario con i movimenti contabili del conto bancario di sistema. Qui è possibile anche riconciliare i pagamenti con assegni. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari separatamente](bank-how-reconcile-bank-accounts-separately.md). Qui non è possibile collegare i pagamenti.
* La finestra **Registrazione pagamenti** nella quale è possibile collegare manualmente i pagamenti ricevuti come contante, assegno o transazione bancaria rispetto a una lista generata di documenti di vendita non pagati. Questa funzionalità è disponibile solo per i documenti di vendita. Qui, non è possibile applicare i pagamenti in uscita e non è possibile riconciliare i conti bancari.
* La finestra **Registrazioni incassi**, nella quale vengono registrate manualmente le ricezioni nel relativo conto COGE, cliente o altro conto immettendo una riga di pagamento. È possibile collegare la ricezione o il rimborso a uno o più movimenti aperti prima di contabilizzare le registrazioni incassi oppure è possibile eseguire il collegamento dai movimenti contabili clienti. Qui, non è possibile riconciliare i conti bancari.  

Un'altra attività di gestione della contabilità clienti riguarda la riscossione dei saldi inevasi, inclusi gli addebiti interessi e l'emissione dei solleciti. [!INCLUDE[d365fin](includes/d365fin_md.md)] offre modi per effettuare anche tali operazioni. Per ulteriori informazioni, vedere [Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md).  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

| Per | Vedere |
| --- | --- |
| Collegare i pagamenti a movimenti contabili cliente o fornitore aperti in base a un feed bancario o un file di rendiconto bancario importato e riconciliare il conto bancario una volta che tutti i pagamenti sono collegati. |[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Collegare i pagamenti a movimenti contabili clienti aperti in base all'immissione manuale in una lista di documenti di vendita non pagati. |[Riconciliare i pagamenti dei clienti manualmente dall'elenco dei documenti di vendita non pagati](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Registrare gli incassi o i rimborsi per i clienti nelle registrazioni incassi e collegare ai movimenti contabili clienti, dalle registrazioni o dai movimenti contabili registrati. |[Riconciliare manualmente i pagamenti dei clienti](receivables-how-apply-sales-transactions-manually.md) |
| Inviare solleciti ai clienti per gli importi insoluti, calcolare interessi e addebiti interessi e gestire i crediti v/clienti. |[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md) |
|È possibile assicurarsi di conoscere il costo degli articoli spediti assegnando i costi degli articoli, come le spese di spedizione, gestione fisica, assicurazione e il trasporto sostenute dopo la vendita.|[Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md)|
|Impostare una tolleranza da cui il sistema chiude una fattura anche se il pagamento, incluso un eventuale sconto, non copre interamente l'importo della fattura.|[Utilizzare le tolleranze pagamento e le tolleranze sconto pagamento](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

