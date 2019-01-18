---
title: Panoramica dei task di gestione fornitori| Documenti Microsoft
description: Descrive i task per la gestione dei fornitori, ad esempio, pagare i creditori o collegare i pagamenti in uscita ai movimenti contabili per chiudere fatture o note di credito.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 11/15/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9bc4eaf292c20c1525c499cde715964eb6e6631f
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="managing-payables"></a>Gestione della contabilità fornitori

Una parte importante della gestione della contabilità fornitori consiste nel pagare i fornitori o rimborsare le spese ai dipendenti. È possibile utilizzare funzioni per aggiungere righe di pagamenti per le fatture di acquisto che sono in scadenza nella pagina **Registrazioni pagamenti**. Per inviare transazioni alla banca, è possibile esportare più righe di registrazione pagamenti in un file, che sarà quindi caricato nella banca. È inoltre possibile effettuare i pagamenti con assegno, incluso trasmettere assegni come pagamenti elettronici.

Un'altra attività tipica è il collegamento dei pagamenti in uscita ai relativi movimenti contabili fornitori o dipendenti per chiudere le fatture di acquisto, le note di credito di acquisto o i conti dipendenti come pagati. È possibile eseguire questa attività nella pagina **Registrazione riconciliazione pagamenti** importando un file di rendiconto bancario per registrare i pagamenti. I pagamenti sono collegati ai movimenti contabili aperti per fornitori, clienti o dipendenti abbinando il testo di pagamento e le informazioni sul movimento. Esistono varie modalità di esaminare e modificare le corrispondenze prima di contabilizzare le registrazioni. Quando si effettua la registrazione, è possibile scegliere di chiudere qualsiasi movimento contabile di conto corrente bancario aperto correlato ai movimenti contabili. Il conto bancario viene automaticamente riconciliato una volta che tutti i pagamenti sono collegati.

In alternativa, è possibile collegare i pagamenti in uscita manualmente nella pagina **Registrazioni pagamenti** o dai movimenti contabili fornitori o dipendenti correlati.

Nella tabella seguente viene descritta una sequenza di attività, all'interno della contabilità fornitori, con collegamenti agli argomenti che li descrivono.

| Per | Vedere |
| --- | --- |
| Generare i pagamenti fornitori o i rimborsi ai dipendenti in scadenza, preparare i pagamenti degli assegni ed esportare i pagamenti in un file della banca durante la registrazione. |[Effettuare i pagamenti](payables-make-payments.md) |
| Collegare i pagamenti fornitori automaticamente alle fatture di acquisto non pagate importando un file di rendiconto bancario. |[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
|Impostare le mappature tra testo sui pagamenti e specifici conti debiti, crediti e contropartita in modo che i pagamenti vengano registrati nei conti specificati quando si contabilizzano le registrazioni riconciliazione pagamenti.|[Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)|
| Collegare manualmente i pagamenti fornitori alle fatture di acquisto non pagate. |[Riconciliare manualmente i pagamenti ai fornitori](payables-how-apply-purchase-transactions-manually.md) |
|Applicare automaticamente i pagamenti, sia in entrata che in uscita, registrati come transazioni nel conto bancario in linea per i relativi movimenti aperti dei conti COGE, fornitore e cliente. La lista viene generata a partire da un feed o un file bancario.|[Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md)|
|Gestire manualmente i pagamenti al conto corrente bancario che non possono essere applicati automaticamente, ad esempio, in quanto non esistono documenti a cui possa essere collegato il pagamento o che il documento correlato ha un importo diverso da quello della transazione a causa del cambio della valuta.|[Riconciliare i pagamenti che non possono essere collegati automaticamente](receivables-how-reconcile-payments-cannot-apply-auto.md)|
|È possibile assicurarsi della corretta valutazione di magazzino assegnando i costi degli articoli, come le spese di spedizione, gestione fisica, assicurazione e il trasporto sostenute per gli acquisti.|[Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md)|
|Se si deve pagare il fornitore in contanti o con assegno, è possibile registrare il pagamento mentre si registra la fattura.|[Saldare immediatamente le fatture di acquisto](finance-how-to-settle-purchase-invoices-promptly.md)|
|Rimborsare ai dipendenti le spese personali durante le attività aziendali effettuando i pagamenti sul conto corrente bancario.|[Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

