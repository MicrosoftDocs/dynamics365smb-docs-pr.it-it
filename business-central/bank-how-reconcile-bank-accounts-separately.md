---
title: Riconciliazione dei conti correnti bancari
description: Scopri come riconciliare le transazioni in Business Central con le transazioni nei rendiconti della tua banca.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 10/24/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---
# <a name="reconcile-bank-accounts"></a>Riconciliazione dei conti correnti bancari

La riconciliazione bancaria aiuta a garantire che ciò che è nei tuoi libri corrisponda ai rendiconto che ricevi dalla tua banca. La riconciliazione del conto corrente bancario confronta e associa i movimenti nei conti bancari che hai impostato in [!INCLUDE[prod_short](includes/prod_short.md)] a transazioni bancarie della tua banca. La riconciliazione può quindi registrare i saldi sui tuoi conti correnti bancari in [!INCLUDE[prod_short](includes/prod_short.md)] per metterli a disposizione dei responsabili finanziari. La riconciliazione bancaria è anche un modo pratico per scoprire e risolvere i pagamenti mancanti e gli errori di contabilità.

In questo articolo viene descritto come eseguire la riconciliazione di conti correnti bancari con la pagina **Riconciliazioni C/C bancari**.

Tuttavia, è possibile riconciliare i conti correnti bancari nella pagina **Registrazione riconciliazione pagamenti** quando elabori i pagamenti. Se scegli l'azione **Registra pagamenti e riconcilia conto bancario**, qualsiasi movimento contabile C/C bancario aperto correlato ai movimenti contabilità fornitori o clienti collegati verrà chiuso. Ciò significa che il conto corrente bancario viene riconciliato automaticamente per i pagamenti registrati. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Nelle versioni per il Nord America è possibile eseguire questa attività nella pagina **Prospetto riconciliazione bancaria**, più adatta per assegni e depositi ma non ti consente di importare i file di rendiconti bancari. Per usare questa pagina anziché quella di **Riconciliazioni C/C bancari**, cancellare il campo **Riconciliazione bancaria con corrispondenza automatica** nella pagina **Setup contabilità generale**. Per ulteriori informazioni, vedere [Riconciliazione dei conti correnti bancari](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) nella funzionalità locale per gli Stati Uniti.

Le righe nella pagina **Riconciliazioni C/C bancari** sono suddivise in due riquadri. Il riquadro **Righe rendiconto bancario** mostra le transazioni bancarie importate o movimenti contabili con pagamenti scaduti. Il riquadro **Mov. contabili C/C bancari** mostra i movimenti contabili del conto corrente bancario interno.

## <a name="about-bank-reconciliation"></a>Informazioni sulla riconciliazione bancaria

La riconciliazione delle transazioni nei rendiconti della banca con i movimenti bancarie in [!INCLUDE[prod_short](includes/prod_short.md)] si chiama *corrispondenza*. Esistono tre modi per creare corrispondenze tra transazioni e movimenti bancari:

* Automaticamente, utilizzando l'azione **Corrispondenza automatica**.

* Automaticamente, utilizzando l'azione **Riconcilia con Copilot**.

  Questa azione è disponibile come parte dell'assistenza per la riconciliazione dei conti correnti bancari (anteprima), che è una funzionalità basata sull'intelligenza artificiale. [Ulteriori informazioni sull'assistenza per la riconciliazione dei conti correnti bancari](bank-reconciliation-with-copilot.md).
* Manualmente, selezionando le righe in entrambi i riquadri per collegare ogni riga del rendiconto bancario a uno o più movimenti contabili C/C bancari, quindi utilizzare l'azione **Corrispondenza manuale**.

La casella di controllo **Collegato** è selezionata nelle righe in cui i movimenti corrispondono. Per ulteriori informazioni, vedere [Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md). Se immetti una data di fine dell'estratto conto nella riconciliazione bancaria dopo avere creato corrispondenze tra le relative righe e i movimenti, [!INCLUDE [prod_short](includes/prod_short.md)] annullerà le corrispondenze per le righe e i movimenti successivi a tale data.

> [!NOTE]
> Dopo aver immesso una data nel campo **Data estratto conto**, la pagina **Riconciliazioni C/C bancari** filtra i movimenti contabili bancari per mostrare solo i movimenti fino a quella data. È possibile registrare riconciliazioni bancarie solo con movimenti contabili bancari alla data di fine estratto conto o prima. Il filtro garantisce che il tuo libro mastro bancario sia bilanciato con il tuo estratto conto bancario alla data di fine dell'estratto conto, con l'unica differenza dei pagamenti e gli assegni in sospeso.

Se il valore nel campo **Saldo totale** del riquadro **Righe rendiconto bancario** è pari al valore totale del campo **Saldo da riconciliare** e del campo **Saldo ultimo estratto conto** del riquadro **Mov. contabili C/C bancari** puoi scegliere l'azione **Registra**. I movimenti contabili C/C bancari senza corrispondenze rimarranno nella pagina, indicando le discrepanze che è necessario risolvere per riconciliare il conto corrente bancario.

Qualsiasi riga per la quale non è possibile creare corrispondenze, indicata da un valore nel campo **Differenza**, rimarrà nella pagina **Riconciliazioni C/C bancari** dopo la registrazione. Rappresenta una sorta di discrepanza che è necessario risolvere prima di poter completare la riconciliazione del conto corrente bancario. La tabella seguente descrive alcune situazioni aziendali tipiche che possono causare differenze.

| Differenza | Motivo | Risoluzione |
|------------|--------|------------|
| Una transazione nel conto corrente bancario in [!INCLUDE[prod_short](includes/prod_short.md)] non è sull'estratto conto. | La transazione bancaria non è stata creata nonostante sia stata effettuata una registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. | Crea la transazione mancante (o chiedi a un debitore di effettuarla). Quindi reimporta il file dell'estratto conto o inserisci manualmente la transazione. |
| Una transazione sull'estratto conto non esiste come documento o riga di registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. | È stata effettuata una transazione bancaria senza una registrazione corrispondente in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio la registrazione di una riga per una spesa. | Creare e registrare il movimento mancante. Per informazioni su un modo rapido per eseguire questa operazione, vedi [Per creare i movimenti contabili mancanti e corrispondenze con le transazioni bancarie](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Una transazione nel conto corrente bancario interno corrisponde a una transazione bancaria, ma alcune informazioni sono troppo diverse per fornire una corrispondenza. | Le informazioni, come l'importo o il nome del cliente, sono state inserite diversamente nella transazione bancaria o nella registrazione interna. | Esamina le informazioni, quindi crea una corrispondenza tra le due. Facoltativamente, correggi la mancata corrispondenza. |

È necessario risolvere le differenze, ad esempio creando movimenti mancanti e correggendo le informazioni non corrispondenti oppure effettuando le transazioni di denaro mancanti, fino a quando non completi e registri la riconciliazione del conto corrente bancario.

È possibile compilare il riquadro **Righe rendiconto bancario** nella pagina **Riconciliazioni C/C bancari** nei seguenti modi:

* Automaticamente, utilizzando la funzione **Importa rendiconto bancario** per compilare le **Righe rendiconto bancario** con le transazioni bancarie in base a un file o un flusso importato fornito dalla banca.
* Manualmente, utilizzando la funzione **Suggerisci righe** per compilare il riquadro **Righe rendiconto bancario** in base alle fatture in [!INCLUDE[prod_short](includes/prod_short.md)] con pagamenti scaduti.

## <a name="add-bank-statement-lines-by-importing-a-bank-statement"></a>Aggiungere righe dell'estratto conto bancario importando un estratto conto bancario

Il riquadro **Righe rendiconto bancario** verrà riempito con le transazioni bancarie in base a un file o un flusso importato fornito dalla banca.

Per importare estratti conto come feed bancari, è necessario impostare il servizio Envestnet Yodlee Bank Feed. Il setup include il collegamento dei conti correnti bancari in [!INCLUDE[prod_short](includes/prod_short.md)] ai conti correnti bancari online corrispondenti. Per ulteriori informazioni, vedere [Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Puoi anche importare file di estratti conto bancari in formato delimitato da virgole o punti e virgola (.CSV). Usa il setup assistito **Imposta un formato di file dell'estratto conto bancario** per definire i formati di importazione dell'estratto conto e allegare il formato a un conto corrente bancario. È quindi possibile utilizzare questi formati quando si importano estratti conto bancari nella pagina **Riconciliazione conto corrente bancario**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Riconciliazione conto corrente bancario**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr. conto corrente bancario** seleziona il conto corrente bancario importante. I movimenti contabili C/C bancari esistenti nel conto corrente bancario vengono visualizzati nel riquadro **Mov. contabili C/C bancari**.
4. Nel campo **Data Estratto Conto** immettere la data dell'estratto conto.
5. Nel campo **Saldo Finale Estratto Conto** immettere il saldo che appare sull'estratto conto.
6. Se si dispone di un file dell'estratto conto, selezionare l'azione **Importa rendiconto bancario**.
7. Individuare il file, quindi selezionare il pulsante **Apri** per importare le transazioni bancarie nel riquadro **Righe rendiconto bancario** della pagina **Riconciliazioni C/C bancari**.

## <a name="to-fill-in-bank-reconciliation-lines-with-the-suggest-lines-action"></a>Per compilare le righe di riconciliazione con l'azione Suggerisci righe

Il riquadro **Righe rendiconto bancario** verrà compilato in base alle fatture in [!INCLUDE[prod_short](includes/prod_short.md)] che hanno pagamenti in sospeso.  

1. Nella pagina **Riconciliazioni C/C bancari** scegliere l'azione **Suggerisci righe**.
2. Nel campo **Data Inizio** immettere la prima data di registrazione dei movimenti contabili che devono essere riconciliati.
3. Nel campo **Data di fine** immettere l'ultima data di registrazione dei movimenti contabili che devono essere riconciliati.

    > [!NOTE]
    > In genere, la data finale corrisponde alla data specificata nel campo **Data estratto conto** . Tuttavia, se si desidera riconciliare le transazioni solo per una parte di un periodo, è possibile inserire una data finale diversa.

4. Se non desideri che i movimenti contabili C/C bancari includano movimenti stornati aperti non corrispondenti, scegli l'interruttore **Escludi movimenti stornati**. Per impostazione predefinita, l'elenco dei movimenti contabili C/C bancari include i movimenti stornati fino alla data dell'estratto conto.
5. Scegli il pulsante **OK**.

## <a name="match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Creare automaticamente corrispondenze tra righe dell'estratto conto e movimenti contabili C/C bancari

La pagina **Riconciliazioni C/C bancari** offre funzionalità di corrispondenza automatica in base a una corrispondenza di testo su una riga del rendiconto (riquadro a sinistra) con testo su uno o più movimenti contabili C/C bancari (riquadro a destra). Puoi sovrascrivere la corrispondenza automatica suggerita e scegliere di non utilizzare affatto la corrispondenza automatica. Per ulteriori informazioni, vedi [Creare manualmente corrispondenze tra righe dell'estratto conto e movimenti contabili C/C bancari](#match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Puoi analizzare la base delle corrispondenze usando l'azione **Dettagli corrispondenza**. Per esempio, i dettagli includeranno i nomi dei campi che contengono valori corrispondenti.  

1. Nella pagina **Riconciliazioni C/C bancari** scegliere l'azione **Corrispondenza automatica**. Verrà visualizzata la pagina **Movimenti bancari corrispondenti**.
2. Nel campo **Tolleranza data transazione (giorni)** specificare l'intervallo di giorni prima e dopo la data di registrazione del movimento contabile C/C bancario entro cui l'azione eseguirà la ricerca delle date di transazione corrispondenti nel rendiconto bancario.

    Se si inserisce 0 o si lascia il campo vuoto, l'azione **Corrispondenza automatica** cercherà solo le date delle transazioni corrispondenti alla data di registrazione del movimento contabile C/C bancario.
3. Scegli il pulsante **OK**.

    Le righe sono codificate a colori per facilitare la comprensione di cosa farne. Le righe del rendiconto bancario e i movimenti contabili C/C bancari che hanno corrispondenze nella riconciliazione bancaria attuale sono visualizzati con carattere verde grassetto. I movimenti contabili C/C bancari che hanno corrispondenze in altre riconciliazioni bancarie sono visualizzati in carattere blu corsivo.
4. Per rimuovere una corrispondenza, selezionare la riga dell'estratto conto bancario quindi selezionare l'azione **Rimuovi corrispondenza**.

> [!TIP]
> Puoi usare un mix di corrispondenza manuale e automatica. Se hai creato manualmente corrispondenze con i movimenti, la corrispondenza automatica non sovrascriverà le tue selezioni.

## <a name="match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Creare manualmente corrispondenze tra righe dell'estratto conto e movimenti contabili C/C bancari

> [!TIP]
> Quando si creano manualmente corrispondenze tra righe e movimenti, le azioni **Mostra tutto**, **Mostra movimenti stornati**, **Nascondi movimenti stornati**, e **Mostra non collegati** possono rendere più facile ottenere una panoramica. Per impostazione predefinita, i movimenti contabili C/C bancari non includono movimenti stornati non corrispondenti. Per includere questi movimenti nell'elenco e creare manualmente corrispondenze con gli stessi, scegli l'azione **Mostra movimenti stornati**. Se scegli di nascondere i movimenti stornati dopo aver effettuato una o più corrispondenze, i movimenti corrispondenti vengono comunque visualizzati.

> [!NOTE]
> Non è possibile registrare una riconciliazione bancaria se si esegue una corrispondenza molti a uno e gli importi combinati contengono differenze. Questo è vero anche se le differenze combinate equivalgono a zero.
>
> Di seguito è riportato un esempio di corrispondenza molti a uno con differenze. Il valore 200 per il movimento 1 dell'estratto conto viene collegato a due movimenti contabili bancari che hanno un valore totale di 180. La differenza è 20. Il valore 350 per il movimento 2 dell'estratto conto viene collegato ad altri due movimenti contabili bancari che hanno un valore totale di 370. La differenza è -20, che bilancia il valore di 20 per l'estratto conto 1.  
>
> Per registrare una riconciliazione bancaria con differenze nelle righe, pubblica le differenze e quindi crea corrispondenze con i movimenti pubblicati.

1. Nella pagina **Riconciliazioni C/C bancari** selezionare una riga non collegata nel riquadro **Righe rendiconto bancario**.
2. Nel riquadro **Mov. contabili C/C bancari** selezionare uno o più movimenti contabili del conto corrente bancario che possono corrispondere alla riga selezionata del rendiconto bancario. Per scegliere più righe, tieni premuto il tasto <kbd>CTRL</kbd> e scegli le righe.

   > [!TIP]
   > Puoi anche creare manualmente corrispondenze tra più righe dell'estratto conto e un movimento contabile C/C bancario. Per esempio, questo potrebbe essere utile se il tuo deposito bancario contiene diversi metodi di pagamento, come carte di credito di diversi emittenti, e la tua banca li elenca come linee separate.
3. Selezionare l'azione **Corrispondenza manuale**.

    La riga del rendiconto bancario selezionata e i movimenti contabili C/C bancari selezionati cambiano in un tipo di carattere verde e la casella di controllo **Collegato** nel riquadro di destra viene selezionata.
4. Ripeti i passaggi da 1 a 3 per tutte le righe del rendiconto bancario senza corrispondenze.

> [!TIP]
> Per rimuovere una corrispondenza, selezionare la riga dell'estratto conto bancario quindi selezionare l'azione **Rimuovi corrispondenza**. Se hai creato corrispondenze tra più righe dell'estratto conto e un movimento contabile e hai bisogno di rimuovere una o più delle righe con corrispondenze, tutte le corrispondenze manuali vengono rimosse per il movimento contabile quando scegli **Rimuovi corrispondenza**.

## <a name="validate-your-bank-reconciliation"></a>Convalidare la riconciliazione bancaria

Per ricontrollare la riconciliazione del tuo conto corrente bancario prima di pubblicarla, usa l'azione **Report test** per visualizzare un'anteprima della riconciliazione. Il report è disponibile nei seguenti contesti:

* Quando stai preparando una riconciliazione bancaria sulla pagina **Riconciliazioni C/C bancari**.
* Quando esegui la riconciliazione dei pagamenti nella pagina **Registrazioni riconciliazione pagamenti**.

Le righe per le quali non è possibile creare corrispondenze rimangono nella pagina **Riconciliazioni C/C bancari** dopo la pubblicazione. Queste righe contengono un valore nel campo **Differenza**. La differenza rappresenta una sorta di discrepanza che è necessario risolvere prima di poter completare la riconciliazione del conto corrente bancario. La tabella seguente descrive alcune situazioni aziendali tipiche che possono causare differenze.

| Differenza | Motivo | Risoluzione |
|------------|--------|------------|
| Una transazione nel conto corrente bancario in [!INCLUDE[prod_short](includes/prod_short.md)] non è sull'estratto conto. | La transazione bancaria non è stata creata nonostante sia stata effettuata una registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. | Crea la transazione mancante (o chiedi a un debitore di effettuarla). Quindi reimporta il file dell'estratto conto o inserisci manualmente la transazione. |
| Una transazione sull'estratto conto non esiste come documento o riga di registrazione in [!INCLUDE[prod_short](includes/prod_short.md)]. | È stata effettuata una transazione bancaria senza una registrazione corrispondente in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio la registrazione di una riga per una spesa. | Creare e registrare il movimento mancante. Per informazioni su un modo rapido per eseguire questa operazione, vedi [Per creare i movimenti contabili mancanti e corrispondenze con le transazioni bancarie](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Una transazione nel conto corrente bancario interno corrisponde a una transazione bancaria, ma alcune informazioni sono troppo diverse per fornire una corrispondenza. | Le informazioni, come l'importo o il nome del cliente, sono state inserite diversamente nella transazione bancaria o nella registrazione interna. | Esamina le informazioni, quindi crea una corrispondenza tra le due. Facoltativamente, correggi la mancata corrispondenza. |

È necessario risolvere le differenze, ad esempio creando movimenti mancanti e correggendo le informazioni non corrispondenti oppure effettuando le transazioni di denaro mancanti, fino a quando non completi e registri la riconciliazione del conto corrente bancario.

> [!NOTE]
> La pagina Riconciliazione bancaria e il report di prova presumono che tu stia effettuando la riconciliazione solo entro il periodo fino alla data di fine dell'estratto conto. Se crei una corrispondenza tra una riga dell'estratto conto bancario e un movimento contabile bancario prima di immettere una data di fine estratto conto e quindi si immette una data di fine estratto conto successiva alla data finale per il movimento contabile bancario, i dati nel report di prova non saranno corretti.

La seguente tabella descrive i campi del report di prova che possono aiutarti a completare la riconciliazione bancaria.

|Campo  |Descrizione  |
|---------|---------|
|Data estratto conto| La data specificata nel campo **Data estratto conto** della pagina **Riconciliazioni C/C bancari**.|
|Saldo ultimo estratto conto|Il saldo specificato nel campo **Saldo ultimo estratto conto** della pagina **Riconciliazioni C/C bancari**. Questo viene compilato automaticamente dalla riconciliazione più recente per lo stesso conto corrente bancario. Il valore è zero se si tratta della prima riconciliazione del conto corrente bancario.|
|Saldo finale estratto conto|Il saldo specificato nel campo **Saldo finale estratto conto** della pagina **Riconciliazioni C/C bancari**. |
|N. conto Co.Ge. <*numero*> Saldo alla <*data*> | Il saldo del conto Co.Ge. alla data di chiusura dell'estratto conto. Questo è il saldo non filtrato a quella data. Se la tua banca utilizza la tua valuta locale, questo saldo dovrebbe essere uguale al saldo del tuo conto corrente bancario (mostrato sul lato destro dell'intestazione del rapporto) dopo aver creato corrispondenze con tutte le righe dell'estratto conto. Un campo vuoto **()** nel nome di questo campo indica che la tua banca utilizza la valuta locale.<br><br>Una discrepanza in questo e nei campi precedenti potrebbe indicare che hai registrato direttamente nel conto Co.Ge. o che stai utilizzando lo stesso conto Co.Ge. per più banche, il che non è consigliato. Le banche sono collegate alla contabilità generale tramite il gruppo di registrazione del conto corrente bancario specificato per il conto.<br><br>Il Test Report mostra un avviso se si dispone di registrazioni dirette, anche se il saldo per la registrazione è pari a zero. Le registrazioni dirette non bilanciate spesso portano a differenze accumulate per future riconciliazioni bancarie. È necessario controllare il saldo della contabilità generale e i movimenti contabili prima di registrare la riconciliazione bancaria. Per ulteriori informazioni sulla pubblicazione diretta, vai a [Evita la pubblicazione diretta](#avoid-direct-posting).|
|N. conto Co.Ge. <*numero*> Saldo (<*LCY*>) alla <*data*>| Il saldo del conto Co.Ge. alla data di chiusura dell'estratto conto in valuta locale. Il saldo viene convertito nella valuta del conto corrente bancario utilizzando il tasso di cambio valido alla data di chiusura dell'estratto conto. Questo è il saldo non filtrato a quella data. Confrontalo con il campo **Nr. conto C/G <* numero *> Saldo alla <* data*>* se la tua banca utilizza una valuta estera. Il valore nel conto Co.Ge. nel campo <* number *> Saldo alla <* date*> per la valuta locale potrebbe differire leggermente perché la conversione di valuta può comportare piccole differenze. Il saldo della tua banca dovrebbe essere molto vicino a questo saldo.  |
|Saldo conto corrente bancario al <*data*>| Il saldo del conto corrente bancario alla data di chiusura dell'estratto conto.|
|Somma delle differenze    | La somma delle differenze per le righe dell'estratto conto bancario. Per accedere ai dettagli, attivare il toggle **Stampa transazioni inevase** quando si inseriscono i criteri per il report. Una differenza è una riga dell'estratto conto bancario che non ha corrispondenze con uno o più movimenti contabili bancari. Non è possibile registrare una riconciliazione del conto corrente bancario con differenze. È possibile registrare una riconciliazione bancaria che contiene movimenti contabili bancari che non hanno corrispondenze con le righe dell'estratto conto. Questo valore è mostrato nel campo **Transazioni bancarie inevase** e in una sezione separata se si attiva il toggle Stampa transazioni inevase.      |
|Saldo estratto conto     | Il valore specificato nel campo **Saldo finale estratto conto** della pagina **Riconciliazioni C/C bancari**.  |
|Transazioni bancarie inevase     | La somma dei movimenti contabili bancari senza corrispondenze e senza assegni con una data di registrazione corrispondente o precedente alla data di fine dell'estratto conto. Ciò accade quando registri le transazioni prima che vengano registrate nella tua banca. Ad esempio, alla fine di un periodo. Quando si crea la successiva riconciliazione bancaria, è possibile riconciliare questi movimenti.        |
|Assegni inevasi     | La somma dei movimenti contabili bancari senza corrispondenze per assegni con una data di registrazione corrispondente o precedente alla data di fine dell'estratto conto. Ciò accade quando registri le transazioni prima che vengano registrate nella tua banca. Ad esempio, questo può accadere per gli assegni se un venditore non incassa un assegno nello stesso periodo in cui lo hai registrato. Quando si crea la successiva riconciliazione bancaria, è possibile riconciliare questi movimenti.        |
|Saldo conto corrente bancario     | La somma dei valori per il saldo finale dell'estratto conto, le transazioni bancarie in sospeso e gli assegni in sospeso. Dopo aver gestito tutte le differenze sui movimenti con corrispondenze, questo saldo corrisponde al tuo saldo bancario. Ad esempio, per questo estratto conto bancario sono stati contabilizzati tutti i movimenti con corrispondenze nonché i movimenti senza corrispondenze. È ora possibile registrare la riconciliazione.        |

> [!TIP]
> Se esegui il **Report di prova** dalla pagina **Registrazione riconciliazione pagamenti**, [!INCLUDE [prod_short](includes/prod_short.md)] calcola il valore in **Saldo finale estratto conto** come segue:
>
> * saldo ultimo estratto conto + somma di tutte le righe nel giornale di registrazione riconciliazione pagamenti
>
> Puoi utilizzare il valore per confrontarlo con il tuo estratto conto bancario.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines"></a>Per creare movimenti contabili mancanti e corrispondenze con le righe dell'estratto conto

Talvolta un estratto conto contiene importi corrispondenti ad interessi o all'addebito di commissioni. Per le righe dell'estratto conto non può essere creata alcuna corrispondenza perché non vi sono movimenti contabili correlati in [!INCLUDE[prod_short](includes/prod_short.md)]. È quindi necessario registrare una riga di registrazione per ogni transazione per creare un movimento contabile correlato con il quale può essere creata una corrispondenza.

1. Nella pagina **Riconciliazioni C/C bancari** scegliere l'azione **Trasferisci a registrazioni COGE**.  
2. Nella pagina **Trans. ric. banc. in reg. gen.** specificare quali registrazioni COGE utilizzare, quindi scegliere **OK**.

    Verrà visualizzata la pagina **Registrazioni COGE** con le nuove righe registrazioni per tutte le righe rendiconto bancario con movimenti contabili mancanti.
3. Completare la riga di registrazione con le informazioni rilevanti, ad esempio il conto profitti/perdite. Per ulteriori informazioni, vedi [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).  
4. Per rivedere il risultato della pubblicazione prima di eseguire la pubblicazione, scegli l'azione **Report di prova**, quindi sceglie un'opzione per accedere al report. Il report **Estratto conto bancario** mostra gli stessi campi dell'intestazione della pagina **Riconciliazioni C/C bancari**.
5. Scegli l'azione **Registra**.

    Dopo aver registrato il movimento, crea una corrispondenza con la riga dell'estratto conto.
6. Aggiornare o riaprire la pagina **Riconciliazioni C/C bancari**. Il nuovo movimento contabile verrà visualizzato nel riquadro **Mov. contabili C/C bancari**.
7. Crea automaticamente o manualmente una corrispondenza tra la riga dell'estratto conto e il movimento contabile C/C bancario.

## <a name="find-outstanding-transactions-in-previous-periods"></a>Trovare le transazioni in sospeso nei periodi precedenti

È possibile utilizzare il report dell'estratto conto per trovare le transazioni in sospeso nei periodi precedenti. Le transazioni in sospeso sono state aperte prima della data dell'estratto conto e non sono state chiuse oppure sono state chiuse dopo la registrazione della riconciliazione bancaria.

Quando esegui il report dell'estratto conto dalla pagina Elenco estratti conto, puoi attivare l'interruttore **Movimenti in sospeso** e il report includerà una sezione che elenca i movimenti in sospeso.

**Esempio** Abbiamo i movimenti contabili C/C bancari A, B e C nel nostro conto corrente bancario per il mese di agosto. Quando riconciliamo il nostro conto corrente bancario per agosto, troviamo una riga dell'estratto conto che corrisponde al movimento A, ma nessuna per B e C. Quindi registriamo la riconciliazione con il movimento A riconciliato e B e C come movimenti in sospeso.

A settembre riceviamo un pagamento per il movimento B e decidiamo di riconciliare il nostro conto corrente bancario. Se eseguiamo il report dell'estratto conto prima di registrare la riconciliazione, avremo una transazione riconciliata e una in sospeso.

Se stampiamo il report per agosto avremo transazioni in sospeso per i movimenti B e C, anche se abbiamo chiuso il movimento B a settembre.

## <a name="undo-a-bank-account-reconciliation"></a>Annullare la riconciliazione di un C/C bancario

Se trovi un errore in una riconciliazione bancaria registrata, puoi utilizzare l'azione **Annulla** nella pagina **Lista dich. C/C bancari** per correggerlo. Quando annulli una riconciliazione bancaria registrata, i movimenti verranno spostati nella pagina **Riconciliazione bancaria** e contrassegnati come **Aperti**, nel senso che non sono riconciliati. Puoi quindi possibile correggere la riconciliazione bancaria e registrarla di nuovo.

> [!NOTE]
> Nella versione nordamericana, per utilizzare la funzionalità Annulla per riconciliazioni bancarie registrate ed estratti conto, è necessario attivare l'interruttore **Riconc. bancaria con corrispondenza automatica** nella pagina **Setup contabilità generale**. La funzionalità Annulla non è disponibile per gli estratti conto registrati dai fogli di lavoro di riconciliazione bancaria.

### <a name="reusing-the-bank-statement-number"></a>Riutilizzo del numero dell'estratto conto

Il numero dell'estratto conto utilizzato per la nuova riconciliazione bancaria viene ottenuto dal conto corrente bancario così come il saldo dell'ultimo estratto conto. È possibile modificare questi valori prima di avviare una nuova riconciliazione bancaria. Tuttavia, quando crei una nuova riconciliazione bancaria, [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se il numero dell'estratto conto è già assegnato a un estratto conto registrato. Se il numero è in uso, ma desideri che venga utilizzato il nuovo estratto conto, puoi utilizzare l'azione **Cambia nr. estratto conto** nella pagina **Riconciliazioni C/C bancari**.

### <a name="examples"></a>Esempi

Di seguito sono riportati gli esempi per correggere un errore in una riconciliazione bancaria registrata con o senza l'utilizzo dello stesso numero di estratto conto.

#### <a name="example-1"></a>Esempio 1

Hai effettuato riconciliazioni bancarie per gennaio, febbraio e marzo. Il numero dell'estratto conto bancario era 100 per marzo. Successivamente, scopri che marzo include solo movimenti fino al 30, il che significa che mancano quelli del 31. Quindi, devi ripetere la riconciliazione bancaria per marzo. In questo caso, apriremo la pagina **Estratto conto bancario**, scegli l'estratto conto di marzo, quindi **Annulla**. 

Alla nuova riconciliazione bancaria viene assegnato il numero 101. Per riassegnare il numero 100, scegli **Cambia nr. estratto conto** e immetti **100**. 

> [!TIP]
> Ricorda di impostare la data fine dell'estratto conto appropriata (in questo esempio, il 31 marzo) e modifica il campo **Saldo ultimo estratto conto**. 

#### <a name="example-2"></a>Esempio 2

Hai effettuato riconciliazioni bancarie per gennaio, giugno e luglio. Scopri che febbraio non è corretto. Supponiamo che avesse il numero di estratto conto 100. Come nell'esempio 1, utilizzi le azioni Annulla e Cambia nr. estratto conto per modificare il numero dell'estratto conto come nell'esempio 1 sopra e ora puoi ripetere la riconciliazione bancaria di febbraio.  

Dopo aver registrato la riconciliazione bancaria corretta per febbraio, nella scheda Conto bancario corrispondente, il campo **Nr. ultimo E/C** viene visualizzato **100**, e il campo **Saldo ultimo estratto conto** mostrerà il saldo finale per l'estratto conto di febbraio. 

Se la riconciliazione bancaria successiva è per marzo, [!INCLUDE[d365fin](includes/d365fin_md.md)] assegnerà 101 come numero di estratto conto e il **Saldo ultimo estratto conto** corretto.

Se la riconciliazione bancaria successiva che esegui è per agosto, valuta la possibilità di modificare i valori nei campi **Nr. ultimo E/C** e **Saldo ultimo estratto conto** nella scheda **Conto bancario** prima di creare la riconciliazione bancaria successiva o di utilizzare l'azione **Cambia nr. estratto conto** e di modificare anche il valore nel campo **Saldo ultimo estratto conto** nella pagina Riconciliazione bancaria.

> [!NOTE]
> Il numero di estratto conto è importante quando esegui riconciliazioni bancarie con file CAMT importati che contengono numeri di estratto conto o quando esegui la riconciliazione in base a estratti conto bancari stampati. Se scarichi solo una serie di transazioni bancarie dalla tua banca online, il numero dell'estratto conto di solito non è importante.  
>
> Il saldo dell'ultimo estratto conto viene conservato nel conto corrente bancario per ridurre al minimo gli errori durante le riconciliazioni bancarie, ma è anche modificabile, consentendoti di eseguire le riconciliazioni bancarie nell'ordine che desideri. Ciò significa anche che se annulli un estratto conto, il nuovo saldo finale potrebbe non essere l'ultimo saldo nell'estratto conto successivo. Non esiste alcuna funzionalità che ti consenta di spostare un saldo in tutti gli estratti conto bancari successivi, quindi tieni presente questo quando utilizzi Annulla.  

## <a name="avoid-direct-posting"></a>Evitare la registrazione diretta

Non utilizzare un conto C/G che consente la registrazione diretta nella categoria di registrazione del conto corrente bancario. La registrazione diretta interrompe la connessione tra il movimento contabile del conto bancario e il movimento contabile del conto C/G. Quando effettui la riconciliazione del tuo conto corrente bancario, i movimenti registrati direttamente sul conto C/G non verranno inclusi e sarà difficile completare la riconciliazione.

Questo errore si verifica spesso quando si inserisce un saldo di apertura per un conto corrente bancario. È importante non registrare il saldo di apertura direttamente nella contabilità generale. I movimenti nel conto C/G che vengono registrati direttamente nel conto C/G causeranno problemi. Ad esempio, questi movimenti potrebbero impedirti di riconciliare il tuo conto corrente bancario. Per i conti bancari in valuta estera, i movimenti possono causare l'accumulo di differenze dopo la registrazione di più riconciliazioni bancarie a causa delle rettifiche del tasso di cambio valuta. Spesso si registra il saldo bancario di apertura direttamente sul conto corrente bancario e l'importo finisce quindi nel conto C/G. In alternativa, lo annulli in un secondo momento rispetto a un conto C/G che usi per bilanciare il saldo della contabilità generale di apertura. In entrambi i casi, è necessario bilanciare qualsiasi registrazione diretta sul conto C/G prima di iniziare la prima riconciliazione bancaria, soprattutto se il conto corrente bancario è in una valuta estera.


## <a name="see-also"></a>Vedi anche

[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Riconciliare conti correnti bancari utilizzando l'assistenza per la riconciliazione di conti correnti bancari (anteprima)](bank-reconciliation-with-copilot.md)
[Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Impostare le regole per il collegamento automatico dei pagamenti](receivables-how-set-up-payment-application-rules.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
