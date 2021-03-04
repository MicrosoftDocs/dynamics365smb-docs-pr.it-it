---
title: Riconciliare i conti correnti bancari e collegare i pagamenti | Documenti Microsoft
description: Descrive i task per riconciliare conti correnti bancari, conti di contabilità clienti, fornitori, registrazione incassi o spese e per applicare i pagamenti automaticamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2eb3b42c5b76487d579065b9a60ae614bbb71dda
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748620"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari
È necessario riconciliare periodicamente i conti debiti, crediti e bancari collegando i pagamenti registrati nella banca alle relative fatture aperte non pagate e note di credito o altri movimenti aperti in [!INCLUDE[prod_short](includes/prod_short.md)].  

Questa operazione può essere eseguita nella pagina **Registrazione riconciliazione pagamenti**, ad esempio importando un file di rendiconto della banca o un feed per registrare rapidamente i pagamenti. I pagamenti sono collegati ai movimenti contabili aperti per clienti o fornitori in base alle corrispondenze tra il testo di pagamento e le informazioni del movimento. È possibile rivedere e modificare i collegamenti automatici prima di effettuare la registrazione. Quando si effettua la registrazione, è possibile scegliere di chiudere qualsiasi movimento contabile di conto corrente bancario aperto correlato ai movimenti contabili. Il conto bancario viene automaticamente riconciliato una volta che tutti i pagamenti sono collegati.

La logica che regola il modo in cui il testo del pagamento viene automaticamente abbinato alle informazioni del movimento è impostato nella pagina **Regole di collegamento pagamenti** come un numero di regole prioritarie che è possibile modificare.

È anche possibile riconciliare i conti correnti bancari senza collegare i pagamenti simultaneamente. Questa operazione viene eseguita nella pagina **Riconciliazioni C/C bancari**. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).   

Per abilitare l'importazione degli estratti conto bancari come feed bancario, è necessario innanzitutto abilitare il servizio Envestnet Yodlee Bank Feeds e successivamente collegare i conti correnti bancari ai conti bancari in linea correlati. Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

In alternativa, è possibile utilizzare l'estensione AMC Banking 365 Fundamentals per convertire un file di rendiconto bancario da un formato qualsiasi a un flusso di dati importabile in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Uso dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

| Per | Vedere |
| --- | --- |
| Collegare i pagamenti per aprire i movimenti contabili cliente o fornitore importando un rendiconto bancario e riconciliare il conto corrente bancario quando tutti i pagamenti sono collegati. |[Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md) |
| Collegare manualmente i pagamenti visualizzando le informazioni dettagliate sui dati corrispondenti e i suggerimenti sui movimenti aperti da collegare ai pagamenti. |[Esaminare o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md) |
| Risolvere i pagamenti che non possono essere collegati automaticamente ai movimenti contabili aperti correlati. Ad esempio perché gli importi differiscono o perché non esiste un movimento contabile correlato. |[Riconciliare i pagamenti che non possono essere collegati automaticamente](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Collegare il testo sui pagamenti a specifici conti cliente, fornitore o di contabilità generale per registrare sempre incassi o spese ricorrenti in tali conti quando non esistono documenti da applicare. |[Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Impostare le regole per stabilire in che modo i pagamenti e le transazioni bancarie devono essere collegati automaticamente ai relativi movimenti contabili aperti quando si utilizza la funzione **Collega automaticamente** nella pagina **Registrazione riconciliazione pagamenti**.|[Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Riconciliazione dei conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]