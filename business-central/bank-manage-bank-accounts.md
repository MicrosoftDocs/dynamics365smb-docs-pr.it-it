---
title: Gestire i conti correnti bancari| Documenti Microsoft
description: "È necessario riconciliare regolarmente i movimenti contabili bancari in Financials con le transazioni bancarie correlate nei conti bancari."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bfc83194a1010e3ac628484952bd0c6b1046481b
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="managing-bank-accounts"></a>Gestione di conti correnti bancari
A intervalli regolari è necessario riconciliare i movimenti contabili bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] con le transazioni bancarie relative nei conti bancari presso la banca e quindi registrare il saldo nel conto corrente bancario. È possibile eseguire questa attività come parte dell'elaborazione dei pagamenti rappresentati in un estratto conto bancario in **Registrazione riconciliazione pagamenti**. In alternativa, è possibile eseguire questa attività in modo distinto dall'elaborazione del pagamento, nella finestra **Riconciliazioni C/C bancari**, che supporta i movimenti contabili degli assegni. In entrambi i casi compilare le finestre importando l'estratto conto bancario in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Talvolta, è necessario trasferire gli importi tra i conti correnti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] per riflettere i trasferimenti alla banca. È possibile eseguire questa attività nella finestra **Registrazioni COGE** in modi diversi a seconda della valuta dei fondi.

Prima di poter gestire i conti correnti bancari, è necessario impostare ogni conto bancario come scheda conto corrente bancario. Inoltre, è necessario impostare i servizi elettronici che è possibile utilizzare per l'importazione dell'estratto conto bancario e l'esportazione del file di pagamento. Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-setup-banking.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| Per | Vedere |
| --- | --- |
| Riconciliare i conti correnti bancari in relazione all'elaborazione dei pagamenti nella finestra **Registrazione riconciliazione pagamenti**. |[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Riconciliare i conti bancari, inclusi i movimenti contabili assegni, come attività separata nella finestra **Riconciliazioni C/C bancari**. |[Riconciliare i conti correnti bancari separatamente](bank-how-reconcile-bank-accounts-separately.md) |
| Registrare i bonifici tra conti correnti bancari nella stessa valuta o in valute diverse. |[Trasferimento di fondi bancari](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Vedi anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

