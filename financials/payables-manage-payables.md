---
title: "Gestione della contabilità fornitori | Documenti Microsoft"
description: "Gestione della contabilità fornitori"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 92b16c52589a07661d9ff080e9ef8a0f6be633f7
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


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

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

