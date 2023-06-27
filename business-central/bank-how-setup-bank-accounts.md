---
title: Impostare i conti correnti bancari (video)
description: Scopri come vengono utilizzati i conti bancari in Business Central e come riconciliare gli importi con la tua banca.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 01/24/2022
ms.author: edupont
---
# <a name="set-up-bank-accounts" />Impostare i conti correnti bancari

I conti correnti bancari vengono utilizzati in [!INCLUDE[prod_short](includes/prod_short.md)] per tenere traccia delle transazioni bancarie. I conti possono essere denominati in valuta locale o estera. Dopo aver impostato i conti correnti bancari è possibile utilizzare l'opzione per la stampa di assegni. I conti bancari includono funzionalità extra per la [riconciliazione dei pagamenti](receivables-apply-payments-auto-reconcile-bank-accounts.md), la [riconciliazione bancaria](bank-how-reconcile-bank-accounts-separately.md) e l'importazione e l'esportazione di file bancari. I conti bancari possono essere inclusi anche in transazioni nelle registrazioni COGE. Ciascun conto bancario è collegato a un conto del piano dei conti tramite il gruppo di registrazione del conto bancario assegnato. L'utilizzo di un conto bancario in una transazione di pagamento crea automaticamente una voce sia nel conto bancario che nel conto di contabilità generale (C/G) collegato.  

I conti bancari funzionano in modo diverso a seconda che venga specificato un codice valuta:

- Se il codice valuta è vuoto

  Tutte le transazioni nel conto bancario sono nella valuta locale (VL) dell'azienda corrente. Se viene effettuata una transazione sul conto in un'altra valuta, gli importi vengono registrati sul conto in VL in base al tasso di cambio della valuta pertinente. Tutti gli assegni emessi da questo conto devono essere emessi in VL. Se il conto bancario viene utilizzato in una registrazione, la riga di registrazione erediterà automaticamente il codice valuta vuoto.  
  
- Il codice valuta è specificato

  Tutte le transazioni effettuate e gli assegni emessi da questo conto devono essere nella stessa valuta specificata sul conto.

È possibile risparmiare tempo sull'immissione dei dati impostando un conto bancario come conto predefinito da utilizzare per la valuta specificata per il conto. In tal modo, il conto è assegnato ai documenti di vendita e di servizio che utilizzano la valuta. Per rendere il conto predefinito per i documenti di vendita e di servizio, nella pagina **Scheda conto bancario**, attiva l'interruttore **Usa come predefinito per la valuta**. Se necessario, puoi scegliere un conto diverso quando lavori su un documento.

Un conto bancario è parte integrante di [!INCLUDE[prod_short](includes/prod_short.md)] e svolge un ruolo in molte altre capacità. L'illustrazione seguente mostra le relazioni più importanti:

![Illustrazione delle relazioni di un conto bancario.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Ciò significa che la creazione di un conto bancario, lo rende disponibile in tutte le posizioni sopra indicate oltre ad essere rispecchiato per il relativo conto C/G e nella pagina **Informazioni società**.

Un conto bancario viene solitamente monitorato quotidianamente per assicurarsi che eventuali nuovi pagamenti da parte dei clienti vengano registrati il più rapidamente possibile. Questo aiuta a garantire che lo stato effettivo di un cliente si rifletta in [!INCLUDE[prod_short](includes/prod_short.md)]. Ciò consente a venditori, contabili e altri dipendenti di accedere alle informazioni più rilevanti e aggiornate in modo da evitare di effettuare chiamate non necessarie al cliente in merito a fatture scadute o ritardi nelle spedizioni.  

![Illustrazione del pagamento bancario.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Un'altra attività consiste nell'importare i pagamenti in valuta del fornitore con i tassi di valuta realizzati per assicurarsi che lo stato effettivo dei fornitori sia aggiornato. La capacità [riconciliazione dei pagamenti](receivables-apply-payments-auto-reconcile-bank-accounts.md) è il modo più semplice per farlo. Nella **Registrazione riconciliazione pagamenti**, puoi importare le transazioni bancarie direttamente da un'applicazione bancaria online e registrarle più o meno automaticamente. La registrazione identifica e registra automaticamente quanto segue:  

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

Dal conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)], la maggior parte delle transazioni deve essere notificata alla banca fisica. Le poche eccezioni includono i seguenti casi:  

- Correzioni pubblicate in [!INCLUDE[prod_short](includes/prod_short.md)]  
- Assegni emessi non ancora incassati 
- Pagamenti del fornitore non ancora approvati dalla banca  

Dal conto fisico in banca arrivano continuamente transazioni non identificate nella registrazione riconciliazione pagamenti, come le seguenti:  

- Nuove sottoscrizioni del fornitore  
- Pagamenti del cliente senza descrizione
- Interessi bancari
- Addebiti bancari
- Addebiti su carta di credito non ancora segnalati

Migliori sono le informazioni di mapping fornite nella registrazione riconciliazione pagamenti, più transazioni vengono registrate automaticamente e più semplice diventa la riconciliazione bancaria periodica.

Guarda nel video qui sotto i passaggi di base per impostare un conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Alcuni campi possono contenere dati sensibili, come i campi **Nr. filiale banca**, **Nr. conto bancario**, **Codice SWIFT**, e **Codice IBAN**. Per ulteriori informazioni, vedi [Monitoraggio dei campi riservati](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts" />Per impostare i conti correnti bancari

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Nella pagina **C/C bancari** scegliere l'azione **Nuovo**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ad esempio, il campo **Categoria registrazione C/C bancario** collega il conto bancario al conto C/G sottostante nel bilancio. Per ulteriori informazioni vedi [Impostare le categorie di registrazione](finance-posting-groups.md).

> [!TIP]
> Alcuni campi sono nascosti finché non scegli l'azione **Mostra di più**, in genere perché vengono utilizzati raramente. Altri campi devono essere aggiunti tramite la personalizzazione. Per ulteriori informazioni vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

Puoi creare tutti i conti bancari di cui hai bisogno per la tua attività. Per ogni conto bancario, è necessario specificare le informazioni che rendono il conto bancario identificabile in modo univoco. Queste informazioni includono l'indirizzo geografico della banca, le numerazioni per i diversi tipi di transazioni, quali addebiti diretti e bonifici, la valuta in cui sono specificati gli importi e le informazioni utilizzate per l'importazione degli estratti conto bancari. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## <a name="to-enter-an-opening-balance" />Per immettere un saldo di apertura

Per compilare il campo **Saldo** con un saldo iniziale, è necessario registrare un movimento contabile del conto corrente bancario con la quantità in questione. È possibile effettuare questa operazione eseguendo un una riconciliazione bancaria. Per ulteriori informazioni vedi [Riconciliare i conti bancari](bank-how-reconcile-bank-accounts-separately.md).  
>
> In alternativa, puoi implementare il saldo iniziale come parte della creazione di dati generali in nuove aziende utilizzando la guida al setup assistito **Migra dati aziendali**. Ulteriori informazioni in [Prepararsi a fare affari](ui-get-ready-business.md).  

> [!IMPORTANT]
> Non registrare il saldo di apertura direttamente nella contabilità generale. La presenza di movimenti nel conto C/G che sono stati registrati direttamente comporta in genere l'impossibilità di riconciliare il conto bancario. Con i conti bancari in valuta estera, tale procedura comporta l'accumulo di differenze man mano che si registrano più riconciliazioni bancarie. Di solito registri il saldo bancario di apertura direttamente sul conto bancario e l'importo finisce quindi nel conto C/G. In alternativa, lo annulli in un secondo momento rispetto a un conto C/G che usi per bilanciare il saldo della contabilità generale di apertura. In entrambi i casi, è necessario bilanciare qualsiasi registrazione diretta sul conto C/G prima di iniziare la prima riconciliazione bancaria, soprattutto se il conto bancario è in una valuta estera.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files" />Per impostare il conto corrente bancario per l'importazione o l'esportazione di file dei conti correnti bancari

I campi relativi all'importazione e all'esportazione di feed e file bancari sono nella nella Scheda dettaglio **Trasferimento** della pagina **Scheda conto corrente bancario**. Per ulteriori informazioni, vedi [Utilizzo dell'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) e [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Scegli la ![lampadina che apre la funzione Dimmi 2.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Apri la scheda del conto corrente bancario per il quale vengono esportati o importati i file dei conti correnti bancari.
3. Compilare i campi appropriati nella Scheda dettaglio **Trasferimento**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> I diversi servizi di esportazione file e i rispettivi formati richiedono valori di configurazione differenti nella pagina **Scheda conto corrente bancario**. Ti vengono notificati i valori di setup mancanti o non corretti quando esporti il file. Leggi con attenzione le brevi descrizioni dei campi o fai riferimento agli argomenti di procedura correlati. Ad esempio, esportare un file di pagamento per il trasferimento elettronico dei fondi (EFT) in Nord America richiede che i campi **Nr. ultimo avviso di rimessa** e **Nr. transito** siano entrambi compilati. Per ulteriori informazioni, vedi [Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

I campi della Scheda dettaglio **Transito** sul conto bancario ha scopi diversi, a seconda che il pagamento sia in entrata o in uscita.

L'illustrazione seguente mostra il percorso dei pagamenti in entrata (i numeri nella descrizione corrispondono a quelli nell'illustrazione):

:::row:::
    :::column:::

1. Le transazioni vengono esportate dal conto bancario in un formato .csv leggibile o nel formato della banca.
2. La *definizione di scambio di dati* associa le informazioni nel file ai campi in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni vedi [Impostare lo scambio di dati](across-set-up-data-exchange.md)
3. Il *setup esportazione/importazione dati* definisce l'esportazione o l'importazione e si collega alla definizione di scambio di dati.
4. Il *formato di importazione estratti conto bancari* collega l'impostazione di importazione al conto bancario.
5. I pagamenti vengono importati tramite la pagina **Registrazione riconciliazione pagamenti** o **Riconciliazione C/C bancario**.

  :::column-end:::
  :::column:::

        ![Illustrazione dei pagamenti ricevuti dalla banca sui conti bancari.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

I pagamenti in entrata vengono sempre importati tramite la pagina **Registrazione riconciliazione pagamenti** o direttamente nella **Riconciliazione C/C bancario**. Al contrario, i pagamenti in uscita possono avere origine da qualsiasi registrazione pagamenti. L'unico prerequisito è che il campo **Consenti esportazione pagamento** deve essere selezionato nel batch di registrazioni pagamenti pertinente.

L'illustrazione seguente mostra il percorso dei pagamenti in uscita (i numeri nella descrizione corrispondono a quelli nell'illustrazione):

:::row:::
    :::column:::

6. Le transazioni compilate in una registrazione pagamenti preparata per l'esportazione dei pagamenti in un file.
7. Il *formato di importazione estratti conto bancari* collega l'impostazione di importazione al conto bancario.
8. Il *setup esportazione/importazione dati* definisce l'esportazione o l'importazione e si collega alla definizione di scambio di dati.
9. La *definizione di scambio di dati* associa le informazioni nel file ai campi in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni vedi [Impostare lo scambio di dati](across-set-up-data-exchange.md)
10. I pagamenti vengono esportati dalla registrazione pagamenti e importati nel conto bancario.

  :::column-end:::
  :::column:::

        ![Illustrazione dei pagamenti inviati dai conti bancari alla banca.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files" />Per impostare i conti correnti fornitore per l'esportazione di file dei conti correnti bancari

I campi nella nella Scheda dettaglio **Trasferimento** della pagina **Scheda C/C bancari fornitori** sono correlati all'esportazione dei feed e dei file dei conti correnti bancari. Per ulteriori informazioni, vedi [Utilizzare l'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) ed [Esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account" />Cambiare il conto bancario

Per utilizzare un conto bancario diverso per la tua attività, devi creare il nuovo conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)]. Ti consigliamo di non sostituire semplicemente le informazioni sul conto che stai attualmente utilizzando perché ciò può causare dati errati. Ad esempio, il bilancio di apertura potrebbe essere errato o il feed della banca potrebbe smettere di funzionare correttamente. È importante mantenere separati i conti attuali e nuovi.

Dopo aver creato il nuovo conto bancario, è necessario creare anche una nuova categoria di registrazione bancaria e assegnarla a un nuovo conto di contabilità generale. Puoi riutilizzare una categoria di registrazione bancaria esistente e le transazioni bancarie verranno registrate negli stessi conti di contabilità generale come negli altri conti bancari che condividono la categoria di registrazione bancaria. Tuttavia, ti consigliamo di creare una nuova categoria di registrazione bancaria e un conto di contabilità generale in modo che le riconciliazioni siano più facili da eseguire.

> [!NOTE]
> Ricorda che le informazioni sul conto bancario sulle fatture di vendita aperte mostrano ancora il conto bancario originale. Di conseguenza, è probabile che i pagamenti vengano ancora registrati su tale conto. Ti consigliamo di mantenere attivi entrambi i conti per un periodo di tempo dopo la modifica.

Per ottenere una visione più concisa dei tuoi conti di cassa nei report finanziari, usa i conti **Inizio-Totale** e **Totale finale** nel piano dei conti, le righe **Totale** nei report finanziari o nelle categorie di conti C/G. Per ulteriori informazioni, vedi la sezione [Business Intelligence e Financial Reporting](bi.md).

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

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
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
