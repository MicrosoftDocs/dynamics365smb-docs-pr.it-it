---
title: Impostare i conti correnti bancari (video)
description: Scopri come vengono utilizzati i conti bancari in Business Central e come riconciliare gli importi con la tua banca.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: 816b46e859fb4125c93346243f57f88b5f941a70
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029276"
---
# <a name="set-up-bank-accounts"></a>Impostare i conti correnti bancari

I conti correnti bancari vengono utilizzati in [!INCLUDE[prod_short](includes/prod_short.md)] per tenere traccia delle transazioni bancarie. I conti possono essere denominati in valuta locale o estera. Dopo aver impostato i conti correnti bancari è possibile utilizzare l'opzione per la stampa di assegni. I conti bancari includono funzionalità extra per la [riconciliazione dei pagamenti](receivables-apply-payments-auto-reconcile-bank-accounts.md), la [riconciliazione bancaria](bank-how-reconcile-bank-accounts-separately.md) e l'importazione e l'esportazione di file bancari. I conti bancari possono essere inclusi anche in transazioni nelle registrazioni COGE. Ciascun conto bancario è collegato a un conto del piano dei conti tramite il gruppo di registrazione del conto bancario assegnato. L'utilizzo di un conto bancario in una transazione di pagamento crea automaticamente una voce sia nel conto bancario che nel conto C/G collegato.  

I conti bancari funzionano in modo diverso a seconda che venga specificato un codice valuta:

- Il codice valuta è vuoto

  Tutte le transazioni nel conto bancario saranno nella valuta locale (LCY) dell'azienda corrente. Se viene effettuata una transazione sul conto in un'altra valuta, gli importi vengono registrati sul conto in VL in base al tasso di cambio della valuta pertinente. Tutti gli assegni emessi da questo conto devono essere emessi in VL. Se il conto bancario viene utilizzato in una registrazione, la riga di registrazione erediterà automaticamente il codice valuta vuoto.  
- Il codice valuta è specificato

  Tutte le transazioni effettuate su questo conto devono essere nella stessa valuta specificata sul conto. Anche tutti gli assegni emessi da questo conto devono avere questa valuta.  

Un conto bancario è parte integrante di [!INCLUDE[prod_short](includes/prod_short.md)] e svolge un ruolo in molte altre capacità. L'illustrazione seguente mostra le relazioni più importanti:

![Illustrazione delle relazioni di un conto bancario.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Ciò significa che la creazione di un conto bancario, lo rende disponibile in tutte le posizioni sopra indicate oltre ad essere rispecchiato per il relativo conto C/G e nella pagina **Informazioni società**.

Un conto bancario viene solitamente monitorato quotidianamente per assicurarsi che eventuali nuovi pagamenti da parte dei clienti vengano registrati il più rapidamente possibile. Questo aiuta a garantire che lo stato effettivo dei clienti si rifletta in [!INCLUDE[prod_short](includes/prod_short.md)] in modo che venditori, contabili e altri dipendenti abbiano accesso a informazioni pertinenti e aggiornate. In questo modo, evitano chiamate inutili al cliente per fatture scadute o ritardi nelle spedizioni.  

![Illustrazione del pagamento bancario.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Un'altra attività consiste nell'importare i pagamenti in valuta del fornitore con i tassi di valuta realizzati per assicurarsi che lo stato effettivo dei fornitori sia aggiornato. Il modo più semplice per assicurarsi che il conto bancario sia aggiornato è utilizzare la capacità [riconciliazione dei pagamenti](receivables-apply-payments-auto-reconcile-bank-accounts.md). Nella **Registrazione riconciliazione pagamenti**, puoi importare le transazioni bancarie direttamente da un'applicazione bancaria online e registrarle più o meno automaticamente. La registrazione identifica e registra automaticamente quanto segue:  

- Pagamenti con addebito diretto dai clienti  
- Pagamenti dei clienti di singole fatture  
- Pagamenti forfettari dai clienti  
- Pagamenti dei clienti in valuta estera  
- Pagamenti dei fornitore  
- Pagamenti dei fornitori in valuta estera  
- Sottoscrizioni e pagamenti ricorrenti dei fornitori  
- Addebiti e interessi bancari  

La riconciliazione dei pagamenti offre un enorme risparmio di tempo nella registrazione dei pagamenti in entrata e in uscita. Tuttavia, le transazioni sul conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)] non sono considerate corrette al 100% finché non si esegue una riconciliazione bancaria.  

La riconciliazione bancaria è il modo in cui ti assicuri che il conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)] corrisponda al conto esterno presso la banca.  

 ![Illustrazione della riconciliazione di un conto bancario.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Nell'illustrazione sopra, il lato sinistro rappresenta il conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)] e il lato destro rappresenta le transazioni importate dalla banca tramite l'applicazione bancaria online. Il diagramma al centro mostra le transazioni da entrambi i lati, ovvero la riconciliazione bancaria.

Dal conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)], la maggior parte delle transazioni deve essere notificata alla banca fisica. Le uniche eccezioni includono i seguenti casi:  

- Correzioni pubblicate in [!INCLUDE[prod_short](includes/prod_short.md)]  
- Assegni emessi non ancora incassati  
- Pagamenti del fornitore che non sono stati approvati dalla banca  

Dal conto fisico in banca arrivano continuamente transazioni sconosciute che non sono state identificate nella registrazione riconciliazione pagamenti, come le seguenti:  

- Nuove sottoscrizioni del fornitore  
- Pagamenti del cliente senza descrizione
- Interessi bancari
- Addebiti bancari
- Addebiti sulla carta di credito che non sono stati ancora registrati

Migliori sono le informazioni di mapping fornite nella registrazione riconciliazione pagamenti, più transazioni vengono registrate automaticamente e più semplice diventa la riconciliazione bancaria periodica.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Alcuni campi possono contenere dati sensibili, come i campi **Nr. filiale banca**, **Nr. conto bancario**, **Codice SWIFT**, e **Codice IBAN**. Per ulteriori informazioni, vedere [Monitoraggio di campi sensibili](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Per impostare i conti correnti bancari

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Nella pagina **C/C bancari** scegliere l'azione **Nuovo**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ad esempio, il campo **Categoria registrazione C/C bancario** collega il conto bancario al conto C/G sottostante nel bilancio. Per ulteriori informazioni, vedere [Impostare le categorie registrazione](finance-posting-groups.md).

> [!TIP]
> Alcuni campi sono nascosti finché non scegli l'azione **Mostra di più**, in genere perché vengono utilizzati raramente. Altri campi devono essere aggiunti tramite la personalizzazione. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

Puoi creare tutti i conti bancari di cui hai bisogno per la tua attività. Per ogni conto bancario, è necessario specificare le informazioni che rendono il conto bancario identificabile in modo univoco. Queste informazioni includono l'indirizzo geografico della banca, le numerazioni per i diversi tipi di transazioni, quali addebiti diretti e bonifici, la valuta in cui sono specificati gli importi e le informazioni utilizzate per l'importazione degli estratti conto bancari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->
> [!NOTE]
> Per compilare il campo **Saldo** con un saldo iniziale, è necessario registrare un movimento contabile del conto corrente bancario con la quantità in questione. È possibile effettuare questa operazione eseguendo un una riconciliazione bancaria. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).  
>
> In alternativa, è possibile implementare il saldo iniziale come parte della creazione di dati generali in nuove aziende utilizzando la guida al setup assistito **Migra dati aziendali**. Per ulteriori informazioni, vedere [Preparazione al business](ui-get-ready-business.md).  

> [!IMPORTANT]
> È importante non registrare il saldo di apertura direttamente nella contabilità generale. Avere voci nel conto C/G che vengono registrate direttamente nel conto C/G in genere comporterà l'impossibilità di riconciliare il conto bancario o, in caso di conti bancari in valuta estera, comporterà l'accumulo di differenze durante la pubblicazione di più riconciliazioni bancarie. Spesso si registra il saldo bancario di apertura direttamente sul conto bancario e l'importo finisce quindi nel conto C/G. In alternativa, lo annulli in un secondo momento rispetto a un conto C/G che hai usato per bilanciare il saldo della contabilità generale di apertura. In entrambi i casi, è necessario bilanciare qualsiasi registrazione diretta sul conto C/G prima di iniziare la prima riconciliazione bancaria, soprattutto se il conto bancario è in una valuta estera.  

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Per impostare il conto corrente bancario per l'importazione o l'esportazione di file dei conti correnti bancari

I campi nella nella Scheda dettaglio **Trasferimento** della pagina **Scheda conto corrente bancario** sono correlati all'importazione e all'esportazione dei feed e dei file della banca. Per ulteriori informazioni, vedere [Utilizzo dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) e [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Aprire la scheda di un conto corrente bancario per il quale verranno esportati o importati i file dei conti correnti bancari.
3. Compilare i campi appropriati nella Scheda dettaglio **Trasferimento**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> I diversi servizi di esportazione file e i rispettivi formati richiedono valori di configurazione differenti nella pagina **Scheda conto corrente bancario**. Si verrà informati sui valori di setup mancanti o non corretti mentre si tenta di esportare il file. Leggere quindi con attenzione le brevi descrizioni dei campi o fare riferimento agli argomenti di procedura correlati. Ad esempio, esportare un file di pagamento per il trasferimento elettronico dei fondi (EFT) in Nord America richiede che sia il campo **Nr. ultimo avviso di rimessa** che il campo **Nr. transito** siano compilati. Per ulteriori informazioni, vedere [Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

I campi della Scheda dettaglio **Transito** sul conto bancario ha scopi diversi, a seconda che il pagamento sia in entrata o in uscita.

L'illustrazione mostra il percorso dei pagamenti in entrata:

:::row:::
    :::column:::
        1. Le transazioni vengono esportate dal conto bancario in un formato .csv leggibile o nel formato della banca.
        <br><br>
2. La *definizione di scambio di dati* associa le informazioni nel file ai campi in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Impostare lo scambio di dati](across-set-up-data-exchange.md)
<br><br>
3. Il *setup esportazione/importazione dati* definisce l'esportazione o l'importazione e si collega alla definizione di scambio di dati.
<br><br>
4. Il *formato di importazione estratti conto bancari* collega l'impostazione di importazione al conto bancario.
<br><br>
5. I pagamenti vengono importati tramite la pagina **Registrazione riconciliazione pagamenti** o **Riconciliazione C/C bancario**.
    :::column-end:::
    :::column:::
        ![Illustrazione dei pagamenti ricevuti dalla banca sui conti bancari.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

I pagamenti in entrata vengono sempre importati tramite la pagina **Registrazione riconciliazione pagamenti** o direttamente nella **Riconciliazione C/C bancario**. Al contrario, i pagamenti in uscita possono avere origine da qualsiasi registrazione pagamenti. L'unico prerequisito è che il campo **Consenti esportazione pagamento** deve essere selezionato nel batch di registrazioni pagamenti pertinente.

L'illustrazione mostra il percorso dei pagamenti in uscita:

:::row:::
    :::column:::
        6. Le transazioni compilate in una registrazione pagamenti preparata per l'esportazione dei pagamenti in un file.
        <br><br>
        7. Il *formato di importazione estratti conto bancari* collega l'impostazione di importazione al conto bancario
        <br><br>
        8. Il *setup esportazione/importazione dati* definisce l'esportazione o l'importazione e si collega alla definizione di scambio di dati.
        <br><br>
        9. La *definizione di scambio di dati* associa le informazioni nel file ai campi in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Impostare lo scambio di dati](across-set-up-data-exchange.md)
        <br><br>
        10. I pagamenti vengono esportati dalla registrazione pagamenti e importati nel conto bancario
    :::column-end:::
    :::column:::
        ![Illustrazione dei pagamenti inviati dai conti bancari alla banca.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Per impostare i conti correnti fornitore per l'esportazione di file dei conti correnti bancari

I campi nella nella Scheda dettaglio **Trasferimento** della pagina **Scheda C/C bancari fornitori** sono correlati all'esportazione dei feed e dei file dei conti correnti bancari. Per ulteriori informazioni, vedere [Utilizzo dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) ed [Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fornitori**, quindi scegli il collegamento correlato.
2. Aprire la scheda di un conto corrente bancario fornitore nel quale verranno esportati i file di pagamento della banca.
3. Scegliere l'azione **C/C bancari**.
4. Dall'**elenco dei conti bancari del fornitore**, scegliere il conto bancario pertinente o aggiungere un nuovo conto bancario.  
5. Nella Scheda dettaglio **Trasferimenti** della pagina **Scheda C/C bancari fornitori** compilare i campi come richiesto. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Alcuni campi del conto bancario del fornitore contengono dati sensibili, come i campi **Nr. filiale banca**, **Nr. conto bancario**, **Codice SWIFT**, e **Codice IBAN**. Per ulteriori informazioni, vedere [Monitoraggio di campi sensibili](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Cambiare il conto bancario

Se desideri utilizzare un conto bancario diverso per la tua attività, devi creare il nuovo conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)]. Ti consigliamo di non sostituire semplicemente le informazioni sul conto che stai attualmente utilizzando perché ciò può causare dati errati. Ad esempio, il bilancio di apertura potrebbe essere errato o il feed della banca potrebbe smettere di funzionare correttamente. È importante mantenere separati i conti attuali e nuovi.

Dopo aver creato il nuovo conto bancario, è necessario creare anche una nuova categoria di registrazione bancaria e assegnarla a un nuovo conto di contabilità generale. Puoi riutilizzare una categoria di registrazione bancaria esistente e le transazioni bancarie verranno registrate negli stessi conti di contabilità generale come negli altri conti bancari che condividono la categoria di registrazione bancaria. Tuttavia, ti consigliamo di creare una nuova categoria di registrazione bancaria e un conto di contabilità generale in modo che le riconciliazioni siano più facili da eseguire.

> [!NOTE]
> Ricorda che le informazioni sul conto bancario sulle fatture di vendita aperte mostrano ancora il conto bancario originale. Di conseguenza, è probabile che i pagamenti vengano ancora registrati su tale conto. Ti consigliamo di mantenere attivi entrambi i conti per un periodo di tempo dopo la modifica.

Per ottenere una visione più concisa dei tuoi conti di cassa nei report finanziari, usa i conti **Inizio-Totale** e **Totale finale** nel piano dei conti, le righe **Totale** nelle situazioni contabili o nelle categorie di conti C/G. Per ulteriori informazioni, vedi la sezione [Business Intelligence e Financial Reporting](bi.md).

## <a name="see-also"></a>Vedere anche

[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Impostazione delle categorie di registrazione](finance-posting-groups.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Addebito diretto SEPA in Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Per impostare il conto bancario per l'addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Per impostare un conto bancario per il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Riconciliazione pagamenti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Informazioni sulla contabilità generale e COA](finance-general-ledger.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
