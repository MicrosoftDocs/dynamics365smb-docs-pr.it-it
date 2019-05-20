---
title: Gestire i conti correnti bancari| Documenti Microsoft
description: È necessario riconciliare regolarmente i movimenti contabili bancari con le transazioni bancarie correlate nei conti bancari.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 25e1242541e98cc47e2fcc4f016a860ad08c635d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246958"
---
# <a name="managing-bank-accounts"></a>Gestione di conti correnti bancari
A intervalli regolari è necessario riconciliare i movimenti contabili bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] con le transazioni bancarie relative nei conti bancari presso la banca e quindi registrare il saldo nel conto corrente bancario. È possibile eseguire questa attività come parte dell'elaborazione dei pagamenti rappresentati in un estratto conto bancario in **Registrazione riconciliazione pagamenti**. In alternativa, è possibile eseguire separatamente il task dall'elaborazione del pagamento nella pagina **Riconciliazioni C/C bancari** in cui associare (riconciliare) le righe del rendiconto bancario nel riquadro a sinistra con i movimenti contabili interni del conto corrente nel riquadro di destra. In entrambe le pagina è possibile compilare le informazioni sull'estratto conto bancario importando un file o feed ed è possibile utilizzare i suggerimenti automatici di corrispondenza.

> [!NOTE]  
> Nelle versioni per il Nord America è possibile eseguire la riconciliazione bancaria nella pagina **Prospetto riconciliazione bancaria**, più adatta per assegni e depositi ma non offre l'importazione di file di rendiconti bancari. Per utilizzare questa finestra al posto della pagina **Riconciliazioni C/C bancari**, deselezionare il campo **Riconciliazione bancaria con collegamento automatico** nella pagina **Setup contabilità generale**. Per ulteriori informazioni, vedere “Riconciliazione dei conti correnti bancari" nella funzionalità locale per gli Stati Uniti.

Talvolta, è necessario trasferire gli importi tra i conti correnti bancari in [!INCLUDE[d365fin](includes/d365fin_md.md)] per riflettere i trasferimenti alla banca. È possibile eseguire questa attività nella pagina **Registrazioni COGE** in modi diversi a seconda della valuta dei fondi.

Prima di poter gestire i conti correnti bancari, è necessario impostare ogni conto bancario come scheda conto corrente bancario. Inoltre, è necessario impostare i servizi elettronici che è possibile utilizzare per l'importazione dell'estratto conto bancario e l'esportazione del file di pagamento. Per ulteriori informazioni, vedere [Impostare i conti correnti bancari](bank-setup-banking.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

| Per | Vedere |
| --- | --- |
| Riconciliare i conti correnti bancari in relazione all'elaborazione dei pagamenti nella pagina **Registrazione riconciliazione pagamenti**. |[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Riconciliare i conti bancari, inclusi i movimenti contabili assegni, come attività separata nella pagina **Riconciliazioni C/C bancari**. |[Riconciliare i conti correnti bancari separatamente](bank-how-reconcile-bank-accounts-separately.md) |
| Registrare i bonifici tra conti correnti bancari nella stessa valuta o in valute diverse. |[Trasferimento di fondi bancari](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Vedi anche
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
