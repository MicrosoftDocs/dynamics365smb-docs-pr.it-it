---
title: Effettuare pagamenti con un AMC Banking (US) o un bonifico SEPA (EU)
description: Elaborare i pagamenti ai fornitori esportando un file (EFT) con le informazioni di pagamento dalle righe registrazioni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 07/06/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA

Nella pagina **Registraz. pagamenti** è possibile elaborare i pagamenti ai fornitori esportando un file con le informazioni di pagamento dalle righe registrazioni. È quindi possibile caricare il file sul sito elettronico della banca dove vengono elaborati i trasferimenti di denaro correlati. [!INCLUDE[prod_short](includes/prod_short.md)] supporta il formato di bonifico SEPA, ma nel proprio paese potrebbero essere disponibili anche altri formati di pagamento elettronico.

> [!NOTE]
> Nella versione generica di [!INCLUDE[prod_short](includes/prod_short.md)], viene installato e connesso un provider di servizi globale per convertire i dati bancari in qualsiasi formato di file richiesto dalla banca. Nelle versioni per il Nord America, lo stesso servizio può essere utilizzato per inviare file di pagamento come trasferimento elettronico di fondi (EFT), ad esempio la rete ACH (Automated Clearing House) comunemente utilizzata, tuttavia con un processo leggermente diverso. Vedere la sezione 6 [Per esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Per abilitare i bonifici SEPA, è necessario innanzitutto impostare un conto corrente bancario, un fornitore e il batch registrazioni COGE su cui si basano le registrazioni pagamenti. Successivamente si preparano i pagamenti dei fornitori compilando automaticamente la pagina **Registraz. pagamenti** con i pagamenti in scadenza insieme alle date di registrazione specificate.  

> [!NOTE]  
> Una volta verificato che i pagamenti sono stati elaborati correttamente dalla banca, è possibile passare alla registrazione delle righe di registrazione pagamenti.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Impostazione dell'estensione AMC Banking 365 Fundamentals

Attivare l'estensione AMC Banking 365 Fundamentals per convertire tutti i file di rendiconto bancario in un formato che è possibile importare o per convertire i file dei pagamenti esportati nel formato richiesto dalla banca. Per ulteriori informazioni, vedi [Usare l'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>Impostare un bonifico SEPA

Nella pagina **Registrazioni pagamenti** è possibile esportare i pagamenti in un file da caricare nel sito elettronico della banca per elaborare trasferimenti di denaro correlati. [!INCLUDE[prod_short](includes/prod_short.md)] supporta il formato di bonifico SEPA, ma nel proprio paese potrebbero essere disponibili anche altri formati di pagamento elettronico.  

Per abilitare l'esportazione di formati di file della banca che non sono supportati come predefiniti in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile impostare una definizione di scambio dati utilizzando il framework di scambio dati. Per ulteriori informazioni, vedere [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).  

Prima di elaborare elettronicamente il pagamento esportando i file di pagamento in formato di bonifico SEPA, è necessario effettuare le seguenti operazioni di setup:  

* Impostare il conto corrente bancario in questione per gestire il formato del bonifico SEPA.  
* Impostare le schede fornitori per elaborare i pagamenti esportando i file nel formato di bonifico SEPA.  
* Impostare il batch di registrazioni COGE correlato per abilitare l'esportazione dei pagamenti dalla pagina **Registrazioni pagamenti**.  
* Connettere la definizione di scambio dati per uno o più tipi di pagamento con uno o più metodi di pagamento rilevanti  

> [!TIP]
> Questo articolo si applica alla versione generica di [!INCLUDE [prod_short](includes/prod_short.md)]. Nel tuo paese o regione, potrebbero essere stati aggiunti ulteriori campi obbligatori alle varie pagine. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Per impostare un conto bancario per il bonifico SEPA

1. Nella casella **Cerca** immettere **C/C bancari**, quindi selezionare il collegamento correlato.  
2. Aprire la scheda del conto corrente bancario da cui si esporteranno i file di pagamento nel formato di bonifico SEPA.  
3. Nella Scheda dettaglio **Trasferimento**, nel campo **Formato esportazione pagamento** scegliere **SEPACT**.  
4. Nella scheda dettaglio **Generale** nel campo **Nr. messaggi bonifico**, scegliere una serie numerica da cui i numeri vengono assegnati ai movimenti di bonifici SEPA.  
5. Assicurarsi che il campo **IBAN** sia compilato.  

    > [!NOTE]  
    > Il campo **Codice valuta** deve essere impostato su **EUR**, perché i bonifici SEPA possono essere eseguiti solo in valuta EURO.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Per impostare una scheda fornitore per il bonifico SEPA

1. Nella casella **Cerca** immettere **Fornitori**, quindi selezionare il collegamento correlato.  
2. Aprire la scheda del fornitore che si pagherà in via elettronica esportando i file di pagamento nel formato di bonifico SEPA.  
3. Nella Scheda dettaglio **Pagamento**, nel campo **Codice metodo di pagamento** scegliere **BANCA**.  
4. Nel campo **Conto bancario preferito** scegliere la banca a cui sarà trasferito il denaro una volta elaborato in via elettronica dalla banca.  

    Se non hai ancora creato una banca per questo fornitore, puoi farlo ora. Per ulteriori informazioni, vedi [Per impostare conti bancari fornitori per l'esportazione di file bancari](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Il valore nel campo **Conto bancario preferito** viene copiato nel campo **Conto bancario destinatario** nella pagina **Registrazioni pagamenti**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Per impostare le registrazioni pagamenti fino per esportare i file di pagamento

1. Nella casella **Cerca** immettere **Registrazioni pagamenti**, quindi selezionare il collegamento correlato.  
2. Nel campo **Nome batch** scegliere il pulsante\-a discesa.  
3. Nella pagina **Batch registrazioni COGE** scegliere l'azione **Modifica lista**.  
4. Nella riga delle registrazioni pagamenti da utilizzare per esportare i pagamenti, selezionare la casella di controllo **Consenti esportazione pagamento**.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Per connettere la definizione di scambio dati per uno o più tipi di pagamento con uno o più metodi di pagamento rilevanti

1. Nella casella **Cerca** immettere **Metodi di pagamento**, quindi selezionare il collegamento correlato.  
2. Nella pagina **Metodi di pagamento** selezionare il metodo di pagamento che viene utilizzato per esportare i pagamenti e quindi scegliere il campo **Definizione righe esport. pagam.**.  
3. Nella pagina **Definizioni righe esportazione pagamento** selezionare il codice che è stato specificato nel campo **Codice** della Scheda dettaglio **Definizioni righe** nel passaggio 4 della sezione "Per descrivere la formattazione di righe e colonne nel file" della [Impostare le definizioni di scambio di dati](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal"></a>Preparare le registrazioni pagamenti

Compilare le registrazioni di pagamento con le righe per i pagamenti dovuti ai fornitori, con l'opzione di inserire le date di registrazione in base alla data di scadenza dei reltivi documenti di acquisto. Per ulteriori informazioni, vedere [Gestione della contabilità fornitori](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Esportare pagamenti in un file della banca

Quando si è pronti a effettuare i pagamenti ai fornitori o i rimborsi ai dipendenti, nella pagina **Registrazioni pagamenti** è possibile esportare un file con le informazioni di pagamento delle righe. È quindi possibile caricare il file sulla banca per elaborare i relativi trasferimenti di denaro.

Nella versione generica di [!INCLUDE[prod_short](includes/prod_short.md)], l'estensione AMC Banking 365 Fundamentals è disponibile. Nelle versioni per il Nord America, la stessa estensione può essere utilizzata per inviare file di pagamento come trasferimento dei fondi elettronici (EFT), ma con un processo leggermente diverso. Vedere la sezione 6 [Per esportare pagamenti in un file della banca](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Prima di esportare i file di pagamento dalle registrazioni dei pagamenti, è necessario specificare il formato elettronico per il conto corrente bancario di interesse ed è necessario abilitare l'estensione AMC Banking 365 Fundamentals. Per ulteriori informazioni, vedi [Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md) e [Usare l'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md). Inoltre, è necessario selezionare la casella di controllo **Consenti esportazione pagamento** nella pagina **Batch registrazioni COGE**. Per ulteriori informazioni, vedi [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).  

Per visualizzare i file di pagamento che sono stati esportati dalle registrazioni pagamenti, si utilizza la pagina **Registri di bonifici**. Da questa pagina è inoltre possibile riesportare i file di pagamento in caso di errori tecnici o di modifiche al file. Si noti, tuttavia, che i file esportati EFT non sono visualizzati in questa pagina e non possono essere riesportati.  

### <a name="to-export-payments-to-a-bank-file"></a>Per esportare pagamenti in un file della banca

Di seguito viene descritto come pagare un fornitore tramite assegno. I passaggi sono simili al rimborso dei clienti tramite assegno.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.
2. Compilare le righe di registrazione pagamenti. Per ulteriori informazioni, vedere [Registrare pagamenti e rimborsi](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Se si utilizza EFT, è necessario selezionare **Pagamento elettronico** o **Pagamento elettronico IAT** nel campo **Tipo pagamento banca**. Servizi di esportazione file diversi e i rispettivi formati richiedono valori di configurazione differenti nelle pagine **Scheda conto corrente bancario** e **Scheda C/C bancari fornitori**. Si verrà informati sui valori di setup mancanti o non corretti mentre si tenta di esportare il file.
    >
    > La funzione EFT può essere utilizzata solo per i conti bancari nella valuta locale. Non può essere utilizzata con una valuta estera, indicata da un valore nel campo **Codice valuta**. Il valore del campo vuoto indica la valuta locale.

3. Una volta completate tutte le righe di registrazione pagamenti, scegliere l'azione **Esporta pagamenti su file**.
4. Nella pagina **Esporta pagamenti elettronici** compilare i campi secondo le necessità.

    Tutti i messaggi di errore verranno visualizzati nel riquadro Dettaglio informazioni di **Errori nel file di pagamento** dove è anche possibile scegliere un messaggio di errore per visualizzare informazioni dettagliate. È necessario risolvere tutti gli errori prima di esportare il file di pagamento.

    > [!TIP]  
    > Quando si utilizza l'estensione AMC Banking 365 Fundamentals, un messaggio di errore comune informa che il numero di conto corrente bancario non ha la lunghezza richiesta dalla banca. Per evitare o risolvere l'errore, è necessario rimuovere il valore nel campo **IBAN** nella pagina **Scheda conto corrente bancario**, quindi nel campo **Nr. conto bancario** , immettere un numero di conto corrente bancario nel formato richiesto dalla banca.

5. Nella pagina **Salva con nome** specificare il percorso in cui verrà esportato il file e scegliere **Salva**.

    > [!NOTE]  
    > Se si utilizza EFT, salvare il modulo della risultante rimessa del fornitore come documento di Word o selezionare in modo che venga inviato tramite posta elettronica direttamente al fornitore. I pagamenti sono ora aggiunti alla pagina **Genera file EFT** da cui è possibile generare più ordini di pagamento contemporaneamente per ridurre i costi di trasmissione. Per ulteriori informazioni, vedere i seguenti passaggi:
6. Nella pagina **Registrazioni pagamenti** selezionare l'azione **Genera file EFT**.

    Nella pagina **Genera file EFT** tutti i pagamenti impostati per EFT esportati dalle registrazioni pagamento per un conto corrente bancario specificato ma non ancora generati sono elencati nella Scheda dettaglio **Righe**.
7. Scegliere l'opzione l'azione **Genera file EFT** per esportare un file per tutti i pagamenti EFT.
8. Nella pagina **Salva con nome** specificare il percorso in cui verrà esportato il file e scegliere **Salva**.

Il file di pagamento bancario viene esportato verso il percorso specificato, quindi è possibile procedere a caricarlo nel conto corrente bancario elettronico ed effettuare i pagamenti effettivi. Sarà quindi possibile registrare le righe esportate delle registrazioni pagamenti.

### <a name="to-plan-when-to-post-exported-payments"></a>Per pianificare quando registrare i pagamenti esportati

Se non si desidera registrare una riga di registrazione pagamenti per un pagamento esportato, ad esempio perché si sta attendendo la conferma che la transazione sia stata lavorata dalla banca, è possibile eliminare la riga di registrazione. Quando in seguito si crea una riga di registrazione pagamenti per pagare l'importo residuo nella fattura, il campo **Importo totale esportato** visualizza la quantità dell'importo pagamento già esportata. Inoltre, è possibile trovare informazioni dettagliate sul totale esportato scegliendo il pulsante **Movimenti dei registri di bonifici** per visualizzare i dettagli relativi ai file di pagamento esportati.

Se si segue una procedura secondo la quale i pagamenti non vengono registrati fino a quando non si riceve la conferma che sono stati elaborati dalla banca, è possibile controllare la situazione in due modi.

* Nelle registrazioni pagamenti con le righe di pagamento suggerite, è possibile ordinare la colonna **Esportato su file pagamento** o **Importo totale esportato** e poi eliminare i suggerimenti di pagamento per le fatture aperte per le quali i pagamenti sono già stati effettuati e per le quali non si desidera creare pagamenti.
* Nella pagina **Sugg. pagamenti fornitore**, dove si specifica quali pagamenti inserire nelle registrazioni pagamenti, è possibile selezionare la casella di controllo **Ignora pagamenti esportati** se non si desidera inserire le righe di registrazione per i pagamenti che sono già stati esportati.

Per visualizzare le informazioni sui pagamenti esportati, scegliere l'azione **Storico esportazione pagamento**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Per riesportare i pagamenti in un file della banca

È possibile riesportare i file di pagamento dalla pagina **Registri di bonifici**. Prima di eliminare o registrare righe di registrazione pagamenti, è possibile anche riesportare il file di pagamento dalla pagina **Registrazioni pagamenti** semplicemente esportandolo di nuovo. Se sono state eliminate o registrate delle righe di registrazione pagamenti dopo l'esportazione, è possibile riesportare lo stesso file di pagamento dalla pagina **Registri di bonifici**. Selezionare la riga per il batch di bonifici che si desidera riesportare, quindi utilizzare l'azione **Riesporta pagamenti su file**.

> [!NOTE]  
> I file esportati EFT non sono visualizzati nella pagina **Registri di bonifici** e non possono essere riesportati.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registri di bonifici**, quindi seleziona il collegamento correlato.
2. Selezionare un'esportazione pagamento che si desidera riesportare quindi scegliere l'azione **Riesporta pagamenti su file**.

## <a name="posting-the-payments"></a>Registrazione dei pagamenti

Quando il pagamento elettronico viene elaborato correttamente dalla banca, registrare i pagamenti. Per ulteriori informazioni, vedere [Effettuare i pagamenti](payables-make-payments.md).

## <a name="see-also"></a>Vedere anche

[Utilizzare l'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
