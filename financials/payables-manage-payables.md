---
title: Panoramica dei task di gestione fornitori| Documenti Microsoft
description: Descrive i task per la gestione dei fornitori, ad esempio, pagare i creditori o collegare i pagamenti in uscita ai movimenti contabili per chiudere fatture o note di credito.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Gestione della contabilità fornitori
Una parte importante della gestione della contabilità fornitori consiste nel pagare i fornitori. È possibile utilizzare funzioni per aggiungere righe di pagamenti per le fatture di acquisto che sono in scadenza nella finestra **Registrazioni pagamenti**. Per inviare transazioni alla banca, è possibile esportare più righe di registrazione pagamenti in un file, che sarà quindi caricato nella banca. È inoltre possibile effettuare i pagamenti con assegno, incluso trasmettere assegni come pagamenti elettronici.

Un'altra attività tipica è il collegamento dei pagamenti in uscita ai relativi movimenti contabili fornitori per chiudere le fatture di acquisto o le note di credito di acquisto come pagate. È possibile eseguire questa attività nella finestra **Registrazione riconciliazione pagamenti** importando un file di rendiconto bancario per registrare i pagamenti. I pagamenti sono collegati ai movimenti contabili aperti per clienti o fornitori abbinando il testo di pagamento e le informazioni sul movimento. Esistono varie modalità di esaminare e modificare le corrispondenze prima di contabilizzare le registrazioni. Quando si effettua la registrazione, è possibile scegliere di chiudere qualsiasi movimento contabile di conto corrente bancario aperto correlato ai movimenti contabili. Il conto bancario viene automaticamente riconciliato una volta che tutti i pagamenti sono collegati.

In alternativa, è possibile collegare i pagamenti in uscita manualmente nella finestra **Registrazioni pagamenti** o dai movimenti di contabilità fornitore correlati.

Nella tabella seguente viene descritta una sequenza di attività, all'interno della contabilità fornitori, con collegamenti agli argomenti che li descrivono.

| Per | Vedere |
| --- | --- |
| Generare pagamenti fornitori in scadenza classificati in ordine di priorità in base agli sconti sui pagamenti e alle penalità per i pagamenti scaduti. In alternativa, esportare i pagamenti in un file della banca quando si effettua la registrazione. |[Effettuare i pagamenti](payables-make-payments.md) |
| Collegare i pagamenti fornitori automaticamente alle fatture di acquisto non pagate importando un file di rendiconto bancario. |[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Collegare manualmente i pagamenti fornitori alle fatture di acquisto non pagate. |[Procedura: Riconciliare manualmente i pagamenti ai fornitori](payables-how-apply-purchase-transactions-manually.md) |
|È possibile assicurarsi della corretta valutazione di magazzino assegnando i costi degli articoli, come le spese di spedizione, gestione fisica, assicurazione e il trasporto sostenute per gli acquisti.|[Procedura: Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Procedura: Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

