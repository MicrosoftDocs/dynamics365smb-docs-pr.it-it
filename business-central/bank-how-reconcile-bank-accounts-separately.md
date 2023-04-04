---
title: Riconciliazione dei conti correnti bancari
description: Scopri come riconciliare le transazioni in Business Central con le transazioni nei rendiconti della tua banca.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# Riconciliazione dei conti correnti bancari

La riconciliazione bancaria aiuta a garantire che ciò che è nei tuoi libri corrisponda ai rendiconto che ricevi dalla tua banca. La riconciliazione del conto bancario confronta e abbina i movimenti nei conti bancari che hai impostato in [!INCLUDE[prod_short](includes/prod_short.md)] con transazioni bancarie della tua banca. La riconciliazione può quindi registrare i saldi sui tuoi conti bancari in [!INCLUDE[prod_short](includes/prod_short.md)] per metterli a disposizione dei responsabili finanziari. La riconciliazione bancaria è anche un modo pratico per scoprire e risolvere i pagamenti mancanti e gli errori di contabilità.

In questo articolo viene descritto come eseguire la riconciliazione di conti correnti bancari con la pagina **Riconciliazioni C/C bancari**.

Tuttavia, è possibile riconciliare i conti correnti bancari nella pagina **Registrazione riconciliazione pagamenti** quando elabori i pagamenti. Se scegli l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento COGE aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Ciò significa che il conto bancario viene riconciliato automaticamente per i pagamenti registrati. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Nelle versioni per il Nord America è possibile eseguire questa attività nella pagina **Prospetto riconciliazione bancaria**, più adatta per assegni e depositi ma non ti consente di importare i file di rendiconti bancari. Per usare questa pagina anziché quella di **Riconciliazioni C/C bancari**, cancellare il campo **Bank Recon. with Auto. Match** nella pagina **Setup contabilità generale**. Per ulteriori informazioni, vedere [Riconciliazione dei conti correnti bancari](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) nella funzionalità locale per gli Stati Uniti.

Le righe nella pagina **Riconciliazioni C/C bancari** sono suddivise in due riquadri. Il riquadro **Righe rendiconto bancario** mostra le transazioni bancarie importate o movimenti contabili con pagamenti scaduti. Il riquadro **Mov. contabili C/C bancari** mostra i movimenti contabili del conto corrente bancario interno.

La riconciliazione delle transazioni nei rendiconti della banca con i movimenti bancarie in [!INCLUDE[prod_short](includes/prod_short.md)] si chiama *corrispondenza*. Esistono due modi per associare le transazioni alle registrazioni bancarie:

* Automaticamente, utilizzando l'azione **Corrispondenza automatica**.
* Manualmente, selezionando le righe in entrambi i riquadri per collegare ogni riga del rendiconto bancario a uno o più movimenti contabili di conti correnti bancari, quindi utilizzare l'azione **Corrispondenza manuale**.

La casella di controllo **Collegato** è selezionata nelle righe in cui i movimenti corrispondono. Per ulteriori informazioni, vedere [Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md). Se immetti una data di fine dell'estratto conto nella riconciliazione bancaria dopo averne associato le righe con le voci, [!INCLUDE [prod_short](includes/prod_short.md)] annullerà le corrispondenze per le righe e le voci successive a tale data.

> [!NOTE]
> Dopo aver immesso una data nel campo Data fine rendiconto, la pagina Riconciliazioni C/C bancari filtra i movimenti contabili bancari per mostrare solo i movimenti fino a quella data. È possibile registrare riconciliazioni bancarie solo con movimenti contabili bancari alla data di fine estratto conto o prima. Il filtro garantisce che il tuo libro mastro bancario sia bilanciato con il tuo estratto conto bancario alla data di fine dell'estratto conto, con l'unica differenza dei pagamenti e gli assegni in sospeso.

Se il valore nel campo **Saldo totale** del riquadro **Righe rendiconto bancario** è pari al valore totale del campo **Saldo da riconciliare** e del campo **Saldo ultimo estratto conto** del riquadro **Mov. contabili C/C bancari** puoi scegliere l'azione **Registra**. I movimenti contabili del conto bancario non corrispondenti rimarranno nella pagina, indicando le discrepanze che è necessario risolvere per riconciliare il conto bancario.

Per ricontrollare la riconciliazione del tuo conto bancario prima di pubblicarla, usa l'azione **Report test** per preparare un'anteprima della riconciliazione. Il report è disponibile nei seguenti contesti:

* Quando stai preparando una riconciliazione bancaria sulla pagina **Riconciliazioni C/C bancari**.
* Quando esegui la riconciliazione dei pagamenti nella pagina **Registrazioni riconciliazione pagamenti**.

Qualsiasi riga che non può essere corrisposta, indicata da un valore nel campo **Differenza**, rimarrà nella pagina **Riconciliazioni C/C bancari** dopo la registrazione. Rappresenta una sorta di discrepanza che è necessario risolvere prima di poter completare la riconciliazione del conto bancario. La tabella seguente descrive alcune situazioni aziendali tipiche che possono causare differenze.

| Differenza | Motivo | Risoluzione |
|------------|--------|------------|
| Una transazione nel conto bancario in [!INCLUDE[prod_short](includes/prod_short.md)] non è sull'estratto conto. | La transazione bancaria non è stata creata nonostante sia stata effettuata una registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. | Crea la transazione mancante (o chiedi a un debitore di effettuarla). Quindi reimporta il file dell'estratto conto o inserisci manualmente la transazione. |
| Una transazione sull'estratto conto non esiste come documento o riga di registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. | È stata effettuata una transazione bancaria senza una registrazione corrispondente in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio la registrazione di una riga per una spesa. | Creare e registrare il movimento mancante. Per informazioni su un modo rapido per eseguire questa operazione, vedi [Per creare i movimenti contabili mancanti per applicare la corrispondenza con le transazioni bancarie](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Una transazione nel conto bancario interno corrisponde a una transazione bancaria, ma alcune informazioni sono troppo diverse per fornire una corrispondenza. | Le informazioni, come l'importo o il nome del cliente, sono state inserite diversamente nella transazione bancaria o nella registrazione interna. | Rivedere le informazioni, quindi corrisponderle manualmente. Facoltativamente, correggi la mancata corrispondenza. |

È necessario risolvere le differenze, ad esempio creando movimenti mancanti e correggendo le informazioni non corrispondenti oppure effettuando le transazioni di denaro mancanti, fino a quando non completi e registri la riconciliazione del conto bancario.

È possibile compilare il riquadro **Righe rendiconto bancario** nella pagina **Riconciliazioni C/C bancari** nei seguenti modi:

* Automaticamente, utilizzando la funzione **Importa rendiconto bancario** per compilare le **Righe rendiconto bancario** con le transazioni bancarie in base a un file o un flusso importato fornito dalla banca.
* Manualmente, utilizzando la funzione **Suggerisci righe** per compilare il riquadro **Righe rendiconto bancario** in base alle fatture in [!INCLUDE[prod_short](includes/prod_short.md)] con pagamenti scaduti.

## Per aggiungere le righe dell'estratto conto bancario importando un estratto conto bancario

Il riquadro **Righe rendiconto bancario** verrà riempito con le transazioni bancarie in base a un file o un flusso importato fornito dalla banca.

Per importare estratti conto come feed bancari, è necessario impostare il servizio Envestnet Yodlee Bank Feed. Il setup include il collegamento dei conti correnti bancari in [!INCLUDE[prod_short](includes/prod_short.md)] ai conti bancari online corrispondenti. Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Puoi anche importare file di estratti conto bancari in formato delimitato da virgole o punti e virgola (.CSV). Usa il setup assistito **Imposta un formato di file dell'estratto conto bancario** per definire i formati di importazione dell'estratto conto e allegare il formato a un conto bancario. È quindi possibile utilizzare questi formati quando si importano estratti conto bancari nella pagina **Riconciliazione del conto bancario**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Riconciliazione bancaria**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr. conto corrente** selezionare il conto corrente bancario importante. I movimenti contabili di conti correnti bancari esistenti nel conto corrente bancario vengono visualizzati nel riquadro **Mov. contabili C/C bancari**.
4. Nel campo **Data Estratto Conto** immettere la data dell'estratto conto.
5. Nel campo **Saldo Finale Estratto Conto** immettere il saldo che appare sull'estratto conto.
6. Se si dispone di un file dell'estratto conto, selezionare l'azione **Importa rendiconto bancario**.
7. Individuare il file, quindi selezionare il pulsante **Apri** per importare le transazioni bancarie nel riquadro **Righe rendiconto bancario** della pagina **Riconciliazioni C/C bancari**.

## Per compilare le righe di riconciliazione con l'azione Suggerisci righe

Il riquadro **Righe rendiconto bancario** verrà compilato in base alle fatture in [!INCLUDE[prod_short](includes/prod_short.md)] che hanno pagamenti in sospeso.  

1. Nella pagina **Riconciliazioni C/C bancari** scegliere l'azione **Suggerisci righe**.
2. Nel campo **Data Inizio** immettere la prima data di registrazione dei movimenti contabili che devono essere riconciliati.
3. Nel campo **Data di fine** immettere l'ultima data di registrazione dei movimenti contabili che devono essere riconciliati.

    > [!NOTE]
    > In genere, la data finale corrisponde alla data specificata nel campo **Data estratto conto** . Tuttavia, se si desidera riconciliare le transazioni solo per una parte di un periodo, è possibile inserire una data finale diversa.

4. Se non desideri che i movimenti contabili del conto bancario includano movimenti stornati aperti non corrispondenti, scegli l'interruttore **Escludi movimenti stornati**. Per impostazione predefinita, l'elenco dei movimenti contabili del conto bancario include i movimenti stornati fino alla data dell'estratto conto.
5. Scegli il pulsante **OK**.

## Per associare automaticamente le righe del rendiconto bancario con i movimenti contabili di conti correnti bancari

La pagina **Riconciliazioni C/C bancari** offre funzionalità di corrispondenza automatica in base a una corrispondenza di testo su una riga del rendiconto (riquadro a sinistra) con testo su uno o più movimenti contabili del conto corrente bancario (riquadro a destra). Puoi sovrascrivere la corrispondenza automatica suggerita e scegliere di non utilizzare affatto la corrispondenza automatica. Per ulteriori informazioni, vedere [Per associare manualmente le righe del rendiconto bancario con i movimenti contabili di conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Puoi indagare la base delle corrispondenze usando l'azione **Dettagli partita** . Per esempio, i dettagli includeranno i nomi dei campi che contengono valori corrispondenti.  

1. Nella pagina **Riconciliazioni C/C bancari** scegliere l'azione **Corrispondenza automatica**. Verrà visualizzata la pagina **Movimenti bancari corrispondenti**.
2. Nel campo **Tolleranza data transazione (giorni)** specificare l'intervallo di giorni prima e dopo la data di registrazione del movimento contabile del conto corrente bancario entro cui l'azione eseguirà la ricerca delle date di transazione corrispondenti nel rendiconto bancario.

    Se si inserisce 0 o si lascia il campo vuoto, l'azione **Abbina automaticamente** cercherà solo le date delle transazioni corrispondenti alla data di registrazione del conto bancario.
3. Scegli il pulsante **OK**.

    Le righe sono codificate a colori per facilitare la comprensione di cosa farne. Tutte le righe del rendiconto bancario e i movimenti contabili di conti correnti bancari che possono corrispondere vengono modificati con carattere verde e la casella di controllo **Collegato** è selezionata. I movimenti contabili del conto bancario già abbinati in altre riconciliazioni bancarie sono visualizzati in carattere blu.
4. Per rimuovere una corrispondenza, selezionare la riga dell'estratto conto bancario quindi selezionare l'azione **Rimuovi corrispondenza**.

> [!TIP]
> Puoi usare un mix di abbinamento manuale e automatico. Se hai abbinato manualmente delle voci, l'abbinamento automatico non sovrascriverà le tue selezioni.

## Per associare manualmente le righe del rendiconto bancario con i movimenti contabili di conti correnti bancari

> [!TIP]
> Quando si abbinano righe e movimenti manualmente, le azioni **Mostra tutto**, **Mostra movimenti stornati**, **Nascondi movimenti stornati**, e **Mostra non collegati** possono rendere più facile ottenere una panoramica. Per impostazione predefinita, i movimenti contabili del conto bancario non includono movimenti stornati non corrispondenti. Per includere questi movimenti nell'elenco e abbinarli manualmente, scegli l'azione **Mostra movimenti stornati**. Se scegli di nascondere i movimenti stornati dopo aver effettuato una o più corrispondenze, i movimenti corrispondenti vengono comunque visualizzati.

1. Nella pagina **Riconciliazioni C/C bancari** selezionare una riga non collegata nel riquadro **Righe rendiconto bancario**.
2. Nel riquadro **Mov. contabili C/C bancari** selezionare uno o più movimenti contabili del conto bancario che possono corrispondere alla riga selezionata del rendiconto bancario. Per scegliere più righe, tieni premuto il tasto <kbd>CTRL</kbd> e scegli le righe.

   > [!TIP]
   > È anche possibile abbinare manualmente più righe di estratto conto con una voce del libro mastro del conto bancario. Per esempio, questo potrebbe essere utile se il tuo deposito bancario contiene diversi metodi di pagamento, come carte di credito di diversi emittenti, e la tua banca li elenca come linee separate.
3. Selezionare l'azione **Corrispondenza manuale**.

    La riga del rendiconto bancario selezionata e i movimenti contabili di conti correnti bancari selezionati cambiano in un tipo di carattere verde e la casella di controllo **Collegato** nel riquadro di destra viene selezionata.
4. Ripeti i passaggi da 1 a 3 per tutte le righe del rendiconto bancario non associate.

> [!TIP]
> Per rimuovere una corrispondenza, selezionare la riga dell'estratto conto bancario quindi selezionare l'azione **Rimuovi corrispondenza**. Se hai abbinato più righe di estratto conto bancario a una voce del libro mastro e hai bisogno di rimuovere una o più delle righe abbinate, tutte le corrispondenze manuali vengono rimosse per la voce del libro mastro quando scegli **Rimuovi corrispondenza**.

## Per creare i movimenti contabili mancanti per applicare la corrispondenza con le righe del rendiconto bancario

Talvolta un estratto conto contiene importi corrispondenti ad interessi o all'addebito di commissioni. Per le righe del rendiconto bancario non può essere effettuata alcuna corrispondenza perché nessun movimento contabile collegato è presente in [!INCLUDE[prod_short](includes/prod_short.md)]. È quindi necessario registrare una riga di registrazione per ogni transazione per creare un movimento contabile collegato per cui può essere effettuata una corrispondenza.

1. Nella pagina **Riconciliazioni C/C bancari** scegliere l'azione **Trasferisci a registrazioni COGE**.  
2. Nella pagina **Trans. ric. banc. in reg. gen.** specificare quali registrazioni COGE utilizzare, quindi scegliere **OK**.

    Verrà visualizzata la pagina **Registrazioni COGE** contenente le nuove righe registrazioni per tutte le righe rendiconto bancario con movimenti contabili mancanti.
3. Completare la riga di registrazione con le informazioni rilevanti, ad esempio il conto profitti/perdite. Per ulteriori informazioni, vedi [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).  
4. Per visualizzare i risultati di una registrazione prima di eseguirla, scegliere l'azione **Report test**. Il report **Estratto conto bancario** si apre e mostra gli stessi campi dell'intestazione della pagina **Riconciliazioni C/C bancari**.
5. Scegli l'azione **Registra**.

    Dopo aver registrato il movimento, collegalo alla riga dell'estratto conto.
6. Aggiornare o riaprire la pagina **Riconciliazioni C/C bancari**. Il nuovo movimento contabile verrà visualizzato nel riquadro **Mov. contabili C/C bancari**.
7. Effettuare la corrispondenza della riga dell'estratto conto con il movimento contabile del conto corrente bancario, manualmente o automaticamente.

## Trovare le transazioni in sospeso nei periodi precedenti

È possibile utilizzare il report dell'estratto conto per trovare le transazioni in sospeso nei periodi precedenti. Le transazioni in sospeso sono state aperte prima della data dell'estratto conto e non sono state chiuse oppure sono state chiuse dopo la registrazione della riconciliazione bancaria.

Quando esegui il report dell'estratto conto dalla pagina Elenco estratti conto, puoi attivare l'interruttore **Movimenti in sospeso** e il report includerà una sezione che elenca i movimenti in sospeso.

**Esempio** Abbiamo i movimenti contabili A, B e C nel nostro conto bancario per il mese di agosto. Quando riconciliamo il nostro conto bancario per agosto, troviamo una riga dell'estratto conto che corrisponde al movimento A, ma nessuna per B e C. Quindi registriamo la riconciliazione con il movimento A riconciliato e B e C come movimenti in sospeso.

A settembre riceviamo un pagamento per il movimento B e decidiamo di riconciliare il nostro conto bancario. Se eseguiamo il report dell'estratto conto prima di registrare la riconciliazione, avremo una transazione riconciliata e una in sospeso.

Se stampiamo il report per agosto avremo transazioni in sospeso per i movimenti B e C, anche se abbiamo chiuso il movimento B a settembre.

## Annullare la riconciliazione di un C/C bancario

Se trovi un errore in una riconciliazione bancaria registrata, puoi utilizzare l'azione **Annulla** nella pagina **Lista dich. C/C bancari** per correggerlo. Quando annulli una riconciliazione bancaria registrata, i movimenti verranno spostati nella pagina **Riconciliazione bancaria** e contrassegnati come **Aperti**, nel senso che non sono riconciliati. Puoi quindi possibile correggere la riconciliazione bancaria e registrarla di nuovo.

> [!NOTE]
> Nella versione nordamericana, per utilizzare la funzionalità Annulla per riconciliazioni bancarie registrate ed estratti conto, è necessario attivare l'interruttore **Riconc. bancaria con abbinamento automatico** nella pagina **Setup contabilità generale**. La funzionalità Annulla non è disponibile per gli estratti conto registrati dai fogli di lavoro di riconciliazione bancaria.

### Riutilizzo del numero dell'estratto conto

Il numero dell'estratto conto utilizzato per la nuova riconciliazione bancaria viene ottenuto dal conto bancario così come il saldo dell'ultimo estratto conto. È possibile modificare questi valori prima di avviare una nuova riconciliazione bancaria. Tuttavia, quando crei una nuova riconciliazione bancaria, [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se il numero dell'estratto conto è già assegnato a un estratto conto registrato. Se il numero è in uso, ma desideri che venga utilizzato il nuovo estratto conto, puoi utilizzare l'azione **Cambia nr. estratto conto** nella pagina **Riconciliazione conto bancario**.

### Esempi

Di seguito sono riportati gli esempi per correggere un errore in una riconciliazione bancaria registrata con o senza l'utilizzo dello stesso numero di estratto conto.

#### Esempio 1

Hai effettuato riconciliazioni bancarie per gennaio, febbraio e marzo. Il numero dell'estratto conto bancario era 100 per marzo. Successivamente, scopri che marzo include solo movimenti fino al 30, il che significa che mancano quelli del 31. Quindi, devi ripetere la riconciliazione bancaria per marzo. In questo caso, apriremo la pagina **Estratto conto bancario**, scegli l'estratto conto di marzo, quindi **Annulla**. 

Alla nuova riconciliazione bancaria viene assegnato il numero 101. Per riassegnare il numero 100, scegli **Cambia nr. estratto conto** e immetti **100**. 

> [!TIP]
> Ricorda di impostare la data fine dell'estratto conto appropriata (in questo esempio, il 31 marzo) e modifica il campo **Saldo ultimo estratto conto**. 

#### Esempio 2

Hai effettuato riconciliazioni bancarie per gennaio, giugno e luglio. Scopri che febbraio non è corretto. Supponiamo che avesse il numero di estratto conto 100. Come nell'esempio 1, utilizzi le azioni Annulla e Cambia nr. estratto conto per modificare il numero dell'estratto conto come nell'esempio 1 sopra e ora puoi ripetere la riconciliazione bancaria di febbraio.  

Dopo aver registrato la riconciliazione bancaria corretta per febbraio, nella scheda Conto bancario corrispondente, il campo **Nr. ultimo E/C** viene visualizzato **100**, e il campo **Saldo ultimo estratto conto** mostrerà il saldo finale per l'estratto conto di febbraio. 

Se la riconciliazione bancaria successiva è per marzo, [!INCLUDE[d365fin](includes/d365fin_md.md)] assegnerà 101 come numero di estratto conto e il **Saldo ultimo estratto conto** corretto.

Se la riconciliazione bancaria successiva che esegui è per agosto, valuta la possibilità di modificare i valori nei campi **Nr. ultimo E/C** e **Saldo ultimo estratto conto** nella scheda **Conto bancario** prima di creare la riconciliazione bancaria successiva o di utilizzare l'azione **Cambia nr. estratto conto** e di modificare anche il valore nel campo **Saldo ultimo estratto conto** nella pagina Riconciliazione bancaria.

> [!NOTE]
> Il numero di estratto conto è importante quando esegui riconciliazioni bancarie con file CAMT importati che contengono numeri di estratto conto o quando esegui la riconciliazione in base a estratti conto bancari stampati. Se scarichi solo una serie di transazioni bancarie dalla tua banca online, il numero dell'estratto conto di solito non è importante.  
>
> Il saldo dell'ultimo estratto conto viene conservato nel conto bancario per ridurre al minimo gli errori durante le riconciliazioni bancarie, ma è anche modificabile, consentendoti di eseguire le riconciliazioni bancarie nell'ordine che desideri. Ciò significa anche che se annulli un estratto conto, il nuovo saldo finale potrebbe non essere l'ultimo saldo nell'estratto conto successivo. Non esiste alcuna funzionalità che ti consenta di spostare un saldo in tutti gli estratti conto bancari successivi, quindi tieni presente questo quando utilizzi Annulla.  

## Evitare la registrazione diretta

Non utilizzare un conto C/G che consente la registrazione diretta nella categoria di registrazione del conto bancario. La registrazione diretta interrompe la connessione tra il movimento contabile del conto bancario e il movimento contabile del conto C/G. Quando effettui la riconciliazione del tuo conto bancario, i movimenti registrati direttamente sul conto C/G non verranno inclusi e sarà difficile completare la riconciliazione.

Questo errore si verifica spesso quando si inserisce un saldo di apertura per un conto bancario. È importante non registrare il saldo di apertura direttamente nella contabilità generale. I movimenti nel conto C/G che vengono registrati direttamente nel conto C/G causeranno problemi. Ad esempio, questi movimenti potrebbero impedirti di riconciliare il tuo conto bancario. Per i conti bancari in valuta estera, i movimenti possono causare l'accumulo di differenze dopo la registrazione di più riconciliazioni bancarie a causa delle rettifiche del tasso di cambio valuta. Spesso si registra il saldo bancario di apertura direttamente sul conto bancario e l'importo finisce quindi nel conto C/G. In alternativa, lo annulli in un secondo momento rispetto a un conto C/G che usi per bilanciare il saldo della contabilità generale di apertura. In entrambi i casi, è necessario bilanciare qualsiasi registrazione diretta sul conto C/G prima di iniziare la prima riconciliazione bancaria, soprattutto se il conto bancario è in una valuta estera.

## Vedi il relativo [training Microsoft](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## Vedi anche
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
