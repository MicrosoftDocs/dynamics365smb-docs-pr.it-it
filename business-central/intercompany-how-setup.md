---
title: Impostazione della registrazione delle transazioni interaziendali
description: Scopri come impostare una partnership intercompany.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 01/31/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
---
# <a name="set-up-intercompany-transactions" />Impostare transazioni intercompany

Le partnership intercompany semplificano la gestione dei processi contabili quando due o più filiali di una società fanno spesso affari tra loro. I partner possono scambiare transazioni, come vendite e acquisti, e gestirle manualmente o automaticamente. Ad esempio, quando un partner invia una riga di registrazione vendite a un altro partner, viene creata una riga di registrazione acquisti per il partner ricevente.

Il piano dei conti intercompany può essere dato, ad esempio, da una versione del piano dei conti del partner di sincronizzazione. Ciascun partner associa i propri conti al piano dei conti intercompany. Ciascun partner associa inoltre le proprie dimensioni e i propri valori alle dimensioni intercompany.

> [!NOTE]
> Nel primo ciclo di rilascio del 2023 abbiamo introdotto una pagina **Setup intercompany** migliorata. La nuova pagina semplifica l'impostazione di una partnership intercompany consolidando tutte le attività impostate in un'unica pagina. I nuovi utenti di [!INCLUDE [prod_short](includes/prod_short.md)] già stanno usando la nuova esperienza. Se sei un cliente esistente, l'amministratore può attivare l'opzione **Accetta automaticamente transazioni di registrazioni COGE intercompany** nella pagina **Gestione funzionalità**.
>
> Le attività in questo articolo presuppongono che l'interruttore della funzionalità sia attivato. Se hai già impostato una partnership intercompany, puoi continuare a utilizzarla.

## <a name="before-you-start" />Operazioni preliminari

Prima di iniziare a impostare la tua partnership intercompany, ci sono alcune decisioni da prendere.

|Decisione  |Descrizione  |
|---------|---------|
|Quale piano dei conti deve essere la base per il piano dei conti intercompany?     | Tutte le società della partnership devono utilizzare lo stesso piano dei conti intercompany. È possibile basare il piano dei conti intercompany sul piano dei conti di una delle società della partnership oppure creare un nuovo piano dei conti intercompany. Associ i conti da utilizzare nella partnership in entrambe le direzioni, in modo che ogni partner invii e riceva le transazioni nei conti corretti. Ulteriori informazioni sull'impostazione del piano dei conti intercompany sono disponibili in [Impostazione dei piani dei conti intercompany](#set-up-the-intercompany-charts-of-accounts).         |
|Quali dimensioni devono essere la base per le dimensioni intercompany?     | Se utilizzi le dimensioni intercompany, devono essere le stesse per tutte le società della partnership. Dopo aver specificato le dimensioni intercompany, mappa i relativi valori di dimensione. Scopri di più sulla mappatura dei valori delle dimensioni in [Impostare le dimensioni intercompany](#set-up-intercompany-dimensions).        |
|Quali partner sono clienti o fornitori o entrambi?     |  Ulteriori informazioni sull'impostazione di società clienti e fornitori in una partnership intercompany sono disponibili in [Impostazione di partner intercompany come clienti e fornitori](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Vuoi specificare i conti bancari da utilizzare nella partnership?| Puoi velocizzare il processo di registrazione delle transazioni di pagamento specificando il conto bancario da utilizzare per ogni società partner. Scopri di più in [Specificare i conti bancari da utilizzare per i partner intercompany](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Come vuoi identificare le aziende della partnership?     | Tutte le parti devono concordare un codice identificativo univoco del partner intercompany per ciascuna società. Assegnerai il codice alle schede cliente e fornitore per identificare le transazioni correlate. Scopri di più sugli identificatori in [Creare numerazioni](ui-create-number-series.md).        |
|Come vuoi gestire i numeri degli articoli?     | Se le righe intercompany contengono articoli, è possibile utilizzare i propri numeri articolo oppure impostare i numeri articolo del partner per ogni articolo menzionato, nel campo **Nr. articolo fornitore** o nel campo **Nr. articolo comune** della scheda articolo. Puoi anche utilizzare l'azione **Riferimento articolo** per mappare i tuoi numeri di articolo alle descrizioni degli articoli dei tuoi partner intercompany. Per ulteriori informazioni sui riferimenti agli articoli, vai a [Usare i riferimenti agli articoli](inventory-how-use-item-cross-refs.md).        |
|Le risorse sono interessate?     | Se le transazioni di vendita intercompany includono risorse, compila il campo **Nr. conto C/G acq. partner IC** della scheda risorsa per ogni risorsa interessata. Il campo contiene il numero del conto di contabilità generale intercompany in cui verrà contabilizzato l'importo di questa risorsa nella società partner. Per ulteriori informazioni sulle risorse, vai a [Impostazione delle risorse](projects-how-setup-resources.md).<br><br>**NOTA**<br>Le transazioni di acquisto intercompany che includono risorse, cespiti e addebiti articolo non sono completamente supportate. Nella società partner, il campo **Tipo di riga** sarà vuoto nelle righe del documento di acquisto che includono queste entità. Devi aggiornare manualmente il campo.        |

## <a name="overview-of-the-steps-to-get-started" />Panoramica dei passaggi per iniziare

Utilizza la pagina **Setup intercompany** per impostare i seguenti componenti delle transazioni intercompany:

* Le impostazioni intercompany della tua azienda.
* La società che sarà il partner di sincronizzazione.
* Il piano dei conti intercompany che tutti i partner utilizzano per scambiare transazioni.
* Le mappature tra i conti nel piano dei conti e nel piano dei conti intercompany per le transazioni in entrata e in uscita per ciascun partner.
* Le dimensioni intercompany e i valori delle dimensioni da utilizzare e il modo in cui vengono mappati alle dimensioni per ciascun partner.
* Le società che sono i partner intercompany.
* Le aziende che sono fornitori o clienti, o entrambi.

## <a name="set-up-a-synchronization-partner" />Impostare un partner di sincronizzazione

Tutti i partner devono utilizzare lo stesso piano dei conti intercompany e, se necessario, le stesse dimensioni intercompany. È possibile risparmiare tempo durante l'impostazione della partnership utilizzando il piano dei conti e le dimensioni di uno dei partner come riferimento per il piano dei conti e le dimensioni intercompany. L'azienda che utilizzi come riferimento è chiamata *partner di sincronizzazione*. In genere, il partner di sincronizzazione è la società della sede centrale, ma non è obbligatorio che lo sia.

Nella pagina **Configurazione intercompany** ciascun partner specifica il partner di sincronizzazione nel campo **Partner di sincronizzazione**. Successivamente, vengono specificati automaticamente il piano dei conti intercompany e le dimensioni intercompany, in base all'impostazione del partner di sincronizzazione. I partner utilizzano quindi le pagine **Mappatura piano dei conti intercompany** e **Mappatura dimensione intercompany** per mappare il proprio piano dei conti e dimensioni al piano dei conti intercompany e alle dimensioni e viceversa. 

Quando sei pronto per sincronizzare i dati con il tuo partner di sincronizzazione, scegli l'azione **Impostazione sincronizzazione**.

> [!NOTE]
> È importante mappare i conti e le dimensioni in entrambe le direzioni. Ovvero, sia al piano dei conti e alle dimensioni intercompany, sia da questi ai propri conti e dimensioni.

## <a name="set-up-the-intercompany-charts-of-accounts" />Impostare il piano dei conti intercompany

Tutti i partner devono utilizzare lo stesso piano dei conti intercompany e mappare ad esso i conti del proprio piano dei conti. Se il piano dei conti della propria società definisce il piano dei conti intercompany delle società partner, attieniti alla procedura descritta in questa sezione.

Se utilizzi un file XML che contiene il piano dei conti intercompany, segui i passaggi descritti in [Importare o esportare un piano dei conti intercompany](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup IC**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Piano dei conti IC**.
3. Per aggiungere i conti, nella pagina **Piano dei conti intercompany** effettua una delle seguenti operazioni:
    * Scegli **Nuovo**, quindi inserisci ciascun conto su una riga della pagina.  
    * Se il piano dei conti intercompany è identico o simile a quello utilizzato normalmente, è possibile compilare automaticamente la pagina scegliendo l'azione **Copia da piano dei conti**. Le nuove righe possono essere modificate secondo le esigenze.
    * Se è stato impostato un piano dei conti intercompany per un partner di sincronizzazione, utilizza l'azione **Impostazione sincronizzazione** per copiare tali conti.

    > [!TIP]
    > Se copi il piano dei conti intercompany da un partner di sincronizzazione, puoi utilizzare l'azione **Impostazione sincronizzazione** per aggiornare i tuoi conti intercompany con eventuali modifiche apportate dal partner ai propri.

Il passaggio successivo consiste nell'associare il piano dei conti al piano dei conti intercompany. Ulteriori informazioni in [Mappare il piano dei conti intercompany ai piani dei conti della società](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### <a name="import-or-export-an-intercompany-chart-of-accounts" />Importare o esportare un piano dei conti intercompany

La società di sincronizzazione può condividere il proprio piano dei conti con i partner esportandolo in un file. I partner possono importare il file per ottenere il piano dei conti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup IC**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Piano dei conti IC**.
3. Nella pagina **Piano dei conti intercompany** scegli l'azione **Importa/Esporta** e quindi seleziona **Importa** o **Esporta**.
4. Scegli il file da importare o esportare.  

La pagina **Piano dei conti IC** viene compilata con le righe nuove o modificate del conto C/G in base al piano dei conti IC del file. Eventuali righe esistenti e non correlate della pagina restano invariate.

## <a name="map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts" />Mappare il piano dei conti intercompany ai piani dei conti della società

Dopo aver definito o importato il piano dei conti intercompany, mappa ogni conto intercompany a uno dei propri conti. Nella pagina **Piano dei Conti IC** è possibile specificare come mappare i conti C/G intercompany utilizzati nelle transazioni in entrata ai conti C/G del piano dei conti della società.

Se i conti intercompany e i tuoi conti hanno gli stessi numeri, puoi mappare i conti automaticamente.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup IC**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Piano dei conti IC**.

    > [!TIP]
    > Per accedere alle azioni sulla pagina, potrebbe essere necessario espandere la pagina nella visualizzazione layout ampio.

3. Nella pagina **Piano dei conti intercompany**, selezionare l'azione **Mapping del piano dei conti**.
4. Puoi mappare i conti manualmente o automaticamente.

    * Per creare manualmente la mappatura, nei riquadri **Piano dei conti intercompany** e **Piano dei conti C/G** scegli un conti e quindi scegli un conto nei campi **Nr. C/G** e **Nr. IC** .
    * Per mappare automaticamente i conti che hanno gli stessi numeri, seleziona le righe che vuoi mappare, scegli l'azione **Associa a conti con stesso nr.**, quindi scegli il piano dei conti da aggiornare.

    > [!TIP]
    > Se vuoi mappare molti o forse tutti i conti, scegli una riga, scegli :::image type="icon" source="media/show-more-options-icon.png" border="false":::, quindi scegli **Seleziona più elementi**.

## <a name="set-up-intercompany-dimensions" />Impostare le dimensioni intercompany

Se i partner scambieranno transazioni con dimensioni collegate, è necessario concordare le dimensioni che verranno usate da tutti. Ad esempio, la società di sincronizzazione può creare una versione semplificata delle proprie dimensioni, esportarle in un file XML e quindi distribuire il file a ciascun partner. Ogni partner può importare il file XML nella pagina **Dimensioni intercompany** e quindi mappare le dimensioni intercompany alle proprie dimensioni. Ulteriori informazioni in [Mappare le dimensioni intercompany alle dimensioni della società](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Ogni società deve mappare le proprie dimensioni alle dimensioni intercompany per i documenti in uscita e i documenti in entrata. La mappatura dei conti in entrambe le direzioni è importante e aiuta a mantenere la coerenza tra le aziende.

Se i partner utilizzeranno le dimensioni intercompany del partner di sincronizzazione, segui i passaggi in questa sezione. Se vuoi condividere un file XML che contiene le dimensioni intercompany, segui i passaggi descritti in [Importare o esportare le dimensioni intercompany](#import-or-export-intercompany-dimensions).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup IC**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Dimensioni intercompany**.
3. Per aggiungere dimensioni, esegui una delle seguenti operazioni nella pagina **Dimensioni intercompany**:
    * Scegli **Nuovo**, quindi inserisci ciascuna dimensione su una riga.  
    * Se le dimensioni intercompany sono identiche o simile a quelle utilizzate normalmente, è possibile compilare automaticamente la pagina scegliendo l'azione **Copia da dimensioni**. Dopo puoi modificare le righe secondo le esigenze.
    * Se hai specificato dimensioni intercompany per un partner di sincronizzazione, utilizza l'azione **Impostazione sincronizzazione** per copiare tali dimensioni.

    > [!TIP]
    > Se copi le dimensioni intercompany da un partner di sincronizzazione, puoi utilizzare l'azione **Impostazione sincronizzazione** per aggiornare le proprie dimensioni intercompany con eventuali modifiche apportate dal partner alle proprie.  

### <a name="import-or-export-intercompany-dimensions" />Importare o esportare le dimensioni intercompany

La società di sincronizzazione può condividere le proprie dimensioni con i partner esportandole in un file. I partner possono importare il file per ottenere le dimensioni.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup IC**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Dimensioni intercompany**.  
3. Nella pagina **Dimensioni intercompany** scegli l'azione **Importa/Esporta** e quindi seleziona **Importa** o **Esporta**.
4. Scegli il file da importare o esportare.

Il passaggio successivo consiste nel mappare le dimensioni con le dimensioni intercompany. Ulteriori informazioni in [Mappare le dimensioni intercompany alle dimensioni della società](#map-intercompany-dimensions-to-your-companys-dimensions).

### <a name="map-intercompany-dimensions-to-your-companys-dimensions" />Mappare le dimensioni intercompany alle dimensioni della società

Dopo aver specificato le dimensioni che utilizzerai, mappa ogni dimensione intercompany con una delle dimensioni della tua azienda e viceversa. Utilizza la pagina **Mappatura dimensioni intercompany** per specificare la mappatura. Successivamente, ripeti il processo per i valori delle dimensioni.

* Specifica in che modo le dimensioni intercompany nelle transazioni in entrata vengono mappate alle dimensioni dall'elenco di dimensioni della società.
* Specifica come le tue dimensioni verranno tradotte in dimensioni intercompany nelle *transazioni in uscita*.

Le dimensioni intercompany con lo stesso codice delle corrispondenti dimensioni della società possono essere mappate automaticamente.  

Nei passaggi seguenti, si mappano dapprima le dimensioni intercompany alle dimensioni per i documenti in entrata nel riquadro **Dimensioni intercompany**. Quindi, si mappano le dimensioni alle dimensioni intercompany per i documenti in uscita nel riquadro **Dimensioni società corrente**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup IC**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Dimensioni intercompany**.
3. Nella pagina **Piano dei conti intercompany**, seleziona l'azione **Mapping dimensioni**.
4. Puoi mappare le dimensioni manualmente o automaticamente.

    * Per creare manualmente la mappatura, nei riquadri **Dimensioni intercompany** e **Dimensioni società corrente** scegli una dimensione, quindi scegli una dimensione nei campi **Codice dimensione** e **Codice dimensione IC**.
    * Per mappare automaticamente le dimensioni che hanno gli stessi codici, seleziona le righe che vuoi mappare, scegli l'azione **Mappa dimensioni con stesso codice**, quindi scegli le dimensioni da aggiornare. 

    > [!TIP]
    > Se vuoi mappare molti o forse tutte le dimensioni, scegli una riga, scegli :::image type="icon" source="media/show-more-options-icon.png" border="false":::, quindi scegli **Seleziona più elementi**.

5. Scegli l'azione **Mapping valori dimensioni**.
6. Nella pagina **Mapping valori dimensione intercompany** i passaggi per creare la mappatura sono simili a quelli appena eseguiti per le dimensioni.

## <a name="set-up-intercompany-general-journal-templates-and-batches" />Impostare modelli e batch di registrazioni COGE intercompany

È necessario impostare un modello di registrazioni COGE e un batch di registrazioni COGE da utilizzare per impostazione predefinita per le transazioni intercompany. Il modello e il batch sono particolarmente importanti se accetti automaticamente transazioni intercompany dai tuoi partner. Per ulteriori informazioni sull'accettazione automatica delle transazioni, vai a [Accettare automaticamente transazioni da partner intercompany](#auto-accept-transactions-from-intercompany-partners).   

* Le registrazioni COGE vengono utilizzate per la contabilizzazione nei conti di contabilità generale e in altri conti, ad esempio conti correnti bancari, conti clienti e conti fornitori. La contabilizzazione mediante una registrazione generale crea sempre movimenti nei conti di contabilità generale.  Utilizza la pagina **Registrazioni COGE intercompany** per impostare il batch di registrazioni COGE da utilizzare. Le impostazioni specifiche delle transazioni intercompany sono i conti specificati nei campi **Tipo di conto IC** e **Nr. conto IC**.
* Le definizioni di registrazioni consentono di usare in una pagina delle registrazioni ideata con un obiettivo specifico. Ciò significa che i campi in ogni definizione di registrazione sono specifici di una determinata parte del programma. Utilizza la pagina **Definizioni registrazioni COGE** per impostare un modello da utilizzare per le transazioni intercompany.

Per ulteriori informazioni sui modelli e sui batch di registrazioni COGE, vai a [Usare batch e definizioni di registrazioni](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="set-up-a-company-for-intercompany-transactions" />Impostare una società per le transazioni intercompany

I passaggi seguenti presuppongono che sia impostato un partner di sincronizzazione con il piano dei conti e le dimensioni su cui baserai il piano dei conti e le dimensioni intercompany. Puoi configurarli tu stesso, ma in genere è più veloce iniziare e la manutenzione è più semplice se utilizzi un partner di sincronizzazione. Per altre informazioni sul partner di sincronizzazione, vai a [Impostare un partner di sincronizzazione](#set-up-a-synchronization-partner).

> [!TIP]
> È consigliabile compilare i campi nella scheda dettaglio **Generale** nella pagina **Setup intercompany** per ciascun partner prima di aggiungere i partner. Quando aggiungi società partner che si trovano nello stesso tenant, [!INCLUDE [prod_short](includes/prod_short.md)] ottiene il codice IC e il nome della società dalla configurazione nella scheda dettaglio Generale. Il campo **Nome società** verificherà che il codice IC sia univoco.

> [!NOTE]
> Se utilizzerai un partner di sincronizzazione, lascia vuoto il campo **Partner di sincronizzazione** quando imposti la società per la partnership.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup IC**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup intercompany** compila i campi nella scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> In [!INCLUDE[prod_short](includes/prod_short.md)] online, non puoi utilizzare i percorsi dei file per trasferire le transazioni ai partner perché [!INCLUDE[prod_short](includes/prod_short.md)] non ha accesso alla rete locale. Pertanto, se si sceglie **Percorso file** nel campo **Tipo di trasferimento**, il campo **Percorso cartella** non è disponibile. Invece, il file verrà scaricato nella cartella **Download** sul computer. Quindi si invia il file a qualcuno nella società partner, ad esempio, tramite posta elettronica. Per un processo più diretto, ti consigliamo di scegliere **E-mail**.

Il prossimo passaggio è la configurazione delle società partner.

## <a name="set-up-intercompany-partners" />Impostare i partner IC

Ogni partner deve aggiungere tutte le altre società della partnership come partner.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup IC**, quindi scegli il collegamento correlato.
2. Nella scheda dettaglio **Partner IC** scegli **Aggiungi**.
3. Nella pagina **Partner IC** compila i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ripeti i passaggi 2 e 3 per tutte le società della partnership.

> [!NOTE]
> Per la registrazione intercompany, se hai attivato l'interruttore **Accetta automaticamente transazione** nella pagina **Scheda partner intercompany** [!INCLUDE[prod_short](includes/prod_short.md)] sopprime i messaggi di avviso sulle fatture di acquisto che duplicano l'ordine di acquisto originale. È importante disporre di un processo aziendale per la gestione dei duplicati. Ad esempio, eliminando tali ordini di acquisto quando la fattura di acquisto viene ricevuta dal partner IC.

### <a name="set-up-intercompany-partners-as-customers-and-vendors" />Impostare partner IC come clienti e fornitori

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup IC**, quindi scegli il collegamento correlato.
2. Nella scheda dettaglio **Partner IC** apri la pagina della scheda per il partner.
3. A seconda di ciò che vuoi fare, scegli il cliente o il partner nei campi **Nr. cliente** o **Nr. fornitore**.

    > [!NOTE]
    > Se il cliente o il fornitore non è stato creato, puoi scegliere **+Nuovo** nel menu a discesa per configurarli. Per ulteriori informazioni sulla creazione di clienti e fornitori, vai a [Registrazione di nuovi clienti](sales-how-register-new-customers.md) e [Registrazione di nuovi fornitori](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > È inoltre possibile specificare un cliente o un fornitore come partner IC compilando il campo **Codice partner IC** nelle pagine **Scheda cliente** e **Scheda fornitore**.

### <a name="set-up-default-intercompany-partner-general-ledger-accounts" />Impostare i conti C/G predefiniti per i partner IC

Quando si crea una riga di acquisto o vendita intercompany da inviare come transazione in uscita, è necessario immettere un conto del piano dei conti intercompany come impostazione di default per il conto della società partner in cui deve essere registrato l'importo. Nella pagina **Scheda conto C/G** è possibile specificare un conto di contabilità generale partner intercompany di default per i conti utilizzati regolarmente nelle righe di acquisto o di vendita intercompany in uscita. Per i conti crediti vs clienti è ad esempio possibile specificare i conti debiti corrispondenti del piano dei conti intercompany. I conti clienti e fornitori vengono utilizzati come conto di contropartita per il partner intercompany quando si registrano transazioni nei giornali di registrazione generali intercompany.  

Quando si specifica un conto C/G nel campo **Nr. contropartita** di una riga intercompany con **Partner IC** nel campo **Tipo conto**, il campo **Nr. conto C/G partner IC** viene compilato automaticamente.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Apri il conto C/G utilizzato per le transazioni intercompany, e nel campo **Conto C/G partner IC di default**, immetti il conto di contabilità generale intercompany in cui il partner effettuerà le registrazioni al momento della registrazione del conto C/G nella riga.
3. Ripetere il passaggio 2 per ogni conto immesso di frequente nel campo **Nr. contropartita** di una riga di documento o registrazione intercompany.

### <a name="auto-accept-transactions-from-intercompany-partners" />Accettare automaticamente le transazioni da partner IC

Per velocizzare l'elaborazione delle transazioni intercompany, è possibile specificare di creare automaticamente le righe di registrazione basate sulle registrazione di un partner intercompany dalla pagina **Registrazioni COGE IC**. Per creare automaticamente le transazioni in entrata e in uscita, devi attivare le seguenti opzioni per ciascun partner:

* Sulla pagina **Setup intercompany** attiva l'interruttore **Invia automaticamente le transazioni** per il partner di sincronizzazione. Specifica quindi dove creare le transazioni COGE intercompany ricevute compilando i campi **Modello reg. gen. IC di default** e **Batch generale reg. IC di default**.

    > [!TIP]
    > Se il campo **Modello reg. gen. IC di default** è vuoto, è necessario impostare una definizione registrazioni COGE da utilizzare per i giornali di registrazioni COGE intercompany. Per ulteriori informazioni sui modelli e sui batch, vai a [Impostare modelli e batch di registrazioni COGE intercompany](#set-up-intercompany-general-journal-templates-and-batches)    

* Sulla pagina **Partner IC** attiva l'interruttore **Accetta automaticamente transazioni**.

Le righe del giornale di registrazione vengono create per te, ma non registrate.

> [!NOTE]
> Se la tua organizzazione ha utilizzato funzionalità interaziendali in [!INCLUDE [prod_short](includes/prod_short.md)] prima del primo ciclo di rilascio del 2022, per accettare automaticamente le transazioni l'amministratore deve attivare la funzionalità **Accettazione automatica delle transazioni di registrazioni CoGe intercompany** nella pagina **Gestione delle funzionalità**.

### <a name="specify-the-bank-accounts-to-use-for-intercompany-partners" />Specificare i conti bancari da utilizzare per i partner intercompany

Per facilitare i pagamenti rapidi, specifica uno o più conti bancari da utilizzare per i partner intercompany. Quando un partner utilizza un giornale di registrazione COGE intercompany per effettuare un pagamento, può specificare il conto bancario nella riga. Il conto bancario viene utilizzato come conto di contropartita nella società ricevente, il che riduce al minimo la necessità di inserire manualmente le transazioni.

* Per specificare il conto bancario da utilizzare, sulla pagina **Partner intercompany** scegli l'azione **Conto bancario**. Nella **Scheda conto bancario intercompany**, inserisci le informazioni sul conto.

## <a name="troubleshoot-your-intercompany-setup" />Risoluzione dei problemi dell'impostazione intercompany

Sulla pagina **Setup intercompany** il riquadro **Diagnostica setup intercompany** contiene riquadri che indicano se sono stati impostati tutti i componenti necessari per lo scambio di transazioni intercompany. I riquadri sono disponibili anche nella Gestione ruolo utente manager aziendale. Scegli i riquadri per scoprire cosa manca. Per una panoramica dei componenti richiesti, vai a [Panoramica dei passaggi per iniziare](#overview-of-the-steps-to-get-started).

## <a name="see-also" />Vedere anche

[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
