---
title: Riconciliare conti correnti bancari e collegare i pagamenti
description: 'Descrive i task per riconciliare conti correnti bancari, conti di contabilità clienti, fornitori, registrazione incassi o spese e per collegare i pagamenti automaticamente.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 07/25/2024
ms.service: dynamics-365-business-central
---

# <a name="apply-payments-automatically-and-reconciling-bank-accounts"></a>Applicare pagamenti automaticamente e riconciliare i conti bancari
È necessario riconciliare periodicamente i conti debiti, crediti e bancari collegando i pagamenti registrati nella banca alle relative fatture aperte non pagate e note di credito o altri movimenti aperti in [!INCLUDE[prod_short](includes/prod_short.md)].  

Questa operazione può essere eseguita nella pagina **Registrazione riconciliazione pagamenti**, ad esempio importando un file di rendiconto della banca o un feed per registrare rapidamente i pagamenti. I pagamenti sono collegati ai movimenti contabili aperti per clienti o fornitori in base alle corrispondenze tra il testo di pagamento e le informazioni del movimento. È possibile rivedere e modificare i collegamenti automatici prima di effettuare la registrazione. Quando si effettua la registrazione, è possibile scegliere di chiudere qualsiasi movimento contabile di conto corrente bancario aperto correlato ai movimenti contabili. Il conto bancario viene automaticamente riconciliato una volta che tutti i pagamenti sono collegati.

Nella pagina **Regole di collegamento pagamenti** puoi impostare regole prioritarie che regolano il modo in cui il testo del pagamento viene automaticamente abbinato alle informazioni del movimento.

È anche possibile riconciliare i conti correnti bancari senza collegare i pagamenti simultaneamente. Questa operazione viene eseguita nella pagina **Riconciliazioni C/C bancari**. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).

Per abilitare l'importazione degli estratti conto bancari come feed bancario, è necessario innanzitutto abilitare il servizio Envestnet Yodlee Bank Feeds e successivamente collegare i conti correnti bancari ai conti bancari in linea correlati. Per ulteriori informazioni, vedere [Configurare il servizio feed bancari Envestnet Yodlee](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Puoi anche importare file di estratti conto bancari in formato delimitato da virgole o punti e virgola (.CSV). Usa il setup assistito **Imposta un formato di file dell'estratto conto bancario** per definire i formati di importazione dell'estratto conto e allegare il formato a un conto corrente bancario. È quindi possibile utilizzare questi formati quando si importano estratti conto bancari nella pagina **Riconciliazione del conto bancario**.

In alternativa, è possibile utilizzare l'estensione AMC Banking 365 Fundamentals per convertire un file di rendiconto bancario da un formato qualsiasi a un flusso di dati importabile in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [utilizzare l'estensione fondamentale di AMC Banking 365](ui-extensions-amc-banking.md).  

Nella tabella seguente viene descritta una sequenza di attività, con collegamenti agli articoli che le descrivono.  

| A | Vedere |
| --- | --- |
| Collegare i pagamenti per aprire i movimenti contabili cliente o fornitore importando un rendiconto bancario e riconciliare il conto corrente bancario dopo il collegamento di tutti i pagamenti. |[Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md) |
| Collegare manualmente i pagamenti visualizzando le informazioni dettagliate sui dati corrispondenti e i suggerimenti sui movimenti aperti da collegare ai pagamenti. |[Esaminare o collegare i pagamenti in seguito al collegamento automatico](receivables-how-review-apply-payments-auto-application.md) |
| Risolvere i pagamenti che non possono essere collegati automaticamente ai movimenti contabili aperti correlati. Ad esempio perché gli importi differiscono o perché non esiste un movimento contabile correlato. |[Riconciliare i pagamenti che non possono essere collegati automaticamente](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Collegare il testo sui pagamenti a specifici conti cliente, fornitore o di contabilità generale per registrare sempre incassi o spese ricorrenti in tali conti quando non esistono documenti da applicare. |[Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Impostare le regole per stabilire in che modo i pagamenti e le transazioni bancarie devono essere collegati automaticamente ai relativi movimenti contabili aperti quando si utilizza la funzione **Collega automaticamente** nella pagina **Registrazione riconciliazione pagamenti**.|[Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-also"></a>Vedere anche
[Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
