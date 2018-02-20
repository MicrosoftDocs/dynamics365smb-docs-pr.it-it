---
title: Task per la riconciliazione dei conti correnti bancari e il collegamento dei pagamenti ai relativi movimenti | Documenti Microsoft
description: "Descrive i task per riconciliare conti correnti bancari, conti di contabilità clienti, fornitori, registrazione incassi o spese e per applicare i pagamenti automaticamente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7f6ec01c1ef1fc024326a7a384eb9d252fb6837b
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari
È necessario riconciliare periodicamente i conti debiti, crediti e bancari collegando i pagamenti registrati nella banca alle relative fatture non pagate e note di credito o altri movimenti aperti in [!INCLUDE[d365fin](includes/d365fin_long_md.md)].  

Questa operazione può essere eseguita nella finestra **Registrazione riconciliazione pagamenti** importando un file di rendiconto della banca o un feed per registrare rapidamente i pagamenti. I pagamenti sono collegati ai movimenti contabili aperti per clienti o fornitori in base alle corrispondenze tra il testo di pagamento e le informazioni del movimento. È possibile rivedere e modificare i collegamenti automatici prima di effettuare la registrazione. Quando si effettua la registrazione, è possibile scegliere di chiudere qualsiasi movimento contabile di conto corrente bancario aperto correlato ai movimenti contabili. Il conto bancario viene automaticamente riconciliato una volta che tutti i pagamenti sono collegati.  

Per abilitare l'importazione degli estratti conto bancari come feed bancario, è necessario innanzitutto abilitare il servizio Feed bancari di Envestnet Yodlee e successivamente collegare i conti correnti bancari ai conti bancari in linea correlati. Per ulteriori informazioni, vedere [Impostare il servizio Feed bancari di Envestnet Yodlee](bank-how-setup-bank-statement-service.md).  

In alternativa, è possibile utilizzare il servizio di conversione di dati bancari per convertire un file di rendiconto bancario da un formato qualsiasi a un flusso di dati importabile in [!INCLUDE[d365fin](includes/d365fin_long_md.md)]. Per ulteriori informazioni, vedere [Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-data-conversion-service.md).  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

| Per | Vedere |
| --- | --- |
| Collegare i pagamenti per aprire i movimenti contabili cliente o fornitore importando un rendiconto bancario e riconciliare il conto corrente bancario quando tutti i pagamenti sono collegati. |[Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md) |
| Collegare manualmente i pagamenti visualizzando le informazioni dettagliate sui dati corrispondenti e i suggerimenti sui movimenti aperti da collegare ai pagamenti. |[Esaminare o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md) |
| Risolvere i pagamenti che non possono essere collegati automaticamente ai movimenti contabili aperti correlati. Ad esempio perché gli importi differiscono o perché non esiste un movimento contabile correlato. |[Riconciliare i pagamenti che non possono essere collegati automaticamente](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Collegare il testo sui pagamenti a specifici conti cliente, fornitore o di contabilità generale per registrare sempre incassi o spese ricorrenti in tali conti quando non esistono documenti da applicare. |[Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

