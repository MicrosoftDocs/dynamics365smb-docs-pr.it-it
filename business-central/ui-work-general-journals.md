---
title: Utilizzo delle registrazioni COGE per registrare direttamente in contabilità generale
description: 'Informazioni su come è possibile utilizzare le registrazioni per la contabilizzazione nei conti C/G e in altri conti delle transazioni finanziarie, ad esempio i conti correnti bancari e i conti fornitori.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/29/2023
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# Utilizzare le registrazioni COGE

La maggior parte delle transazioni finanziarie vengono registrate nella contabilità generale attraverso i documenti quali fatture di acquisto e ordini di vendita. Tuttavia, puoi anche elaborare attività commerciali come:

* Acquisti
* Pagamenti
* Utilizzo di registrazioni periodiche per contabilizzare i ratei
* Rimborso delle spese dei dipendenti registrando le righe di registrazione commesse nelle registrazioni  

La maggior parte delle registrazioni sono basate Contabilità generale ed è possibile elaborare tutte le operazioni nella pagina **Contabilità generale**. Ulteriori informazioni in [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).  

Ad esempio, puoi utilizzare le spese dei dipendenti per il rimborso. Ulteriori informazioni in [Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md).

Tuttavia, [!INCLUDE [prod_short](includes/prod_short.md)] offre inoltre le registrazioni ottimizzate per specifici tipi di transazioni, ad esempio le **Registrazioni pagamenti** per la registrazione dei pagamenti. Per ulteriori informazioni, vedi [Registrare pagamenti e resi nelle Registrazioni pagamenti](payables-how-post-payments-refunds.md).  

Usi le registrazioni COGE per includere le transazioni finanziarie nei conti di contabilità generale e in vari altri conti. Gli altri conti includono conti bancari, conti clienti, fornitori e conti dipendenti. La contabilizzazione mediante una registrazione generale crea movimenti nei conti di contabilità generale anche quando, ad esempio, viene contabilizzata una riga di registrazione in un conto cliente. Il movimento viene registrato in un conto crediti C/G tramite una categoria di registrazione.

Le informazioni immesse in una registrazione sono temporanee e possono essere modificate mentre si trovano nella registrazione. Quando si contabilizza la registrazione, le informazioni vengono trasferite a movimenti in singoli conti, dove non possono essere modificate. È tuttavia possibile scollegare i movimenti registrati e stornare o correggere i movimenti. Ulteriori informazioni in [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## Aggiungere contesto alle transazioni delle registrazioni COGE

Quando crei una registrazione, puoi aggiungere collegamenti che forniscono contesto alle relative transazioni. Quando contabilizzi la registrazione, [!INCLUDE [prod_short](includes/prod_short.md)] copia i collegamenti nella registrazione contabilizzata e nei movimenti contabili creati dalla registrazione. Ad esempio, fornire collegamenti può semplificare il lavoro del revisore. Se conservi le immagini delle ricevute di spesa nel sito Sharepoint della tua azienda, puoi aggiungere collegamenti ai file. Quando contabilizzi la registrazione per inviare le tue spese, il tuo revisore può accedere rapidamente ai file delle ricevute.

## Usare batch e definizioni di registrazioni

Esistono numerose definizioni registrazioni COGE. Ogni definizione registrazioni è rappresentata da una pagina dedicata con funzioni specifiche e campi necessari per supportare tali funzioni, ad esempio la pagina **Registrazione riconciliazione pagamenti** per elaborare i pagamenti bancari e la pagina **Registrazioni pagamenti** per pagare i fornitori o rimborsare i dipendenti. Per ulteriori informazioni, vedi [Effettuare i pagamenti](payables-make-payments.md) e [Riconciliare i pagamenti clienti con la registrazione incassi o da movimenti contabili clienti](receivables-how-apply-sales-transactions-manually.md).

Per ogni definizione registrazioni è possibile impostare le proprie registrazioni personali come batch registrazioni. Ad esempio, è possibile definire dei batch registrazioni personali per le registrazioni pagamenti che abbiano delle impostazioni e un layout personali. Di seguito viene fornito un suggerimento come esempio per personalizzare una registrazione.

> [!TIP]  
> Se si seleziona la casella di controllo **Suggerisci importo contropartita** nella riga per il proprio batch nella pagina **Batch registrazioni COGE**, il campo **Importo** ad esempio nelle righe di registrazione COGE per lo stesso numero di documento viene precompilato automaticamente con il valore richiesto per saldare il documento. Per ulteriori informazioni vedi [Suggerimento automatico dei valori in [!INCLUDE[prod_short](includes/prod_short.md)]](ui-let-system-suggest-values.md).

> [!TIP]
> Puoi aggiungere o rimuovere i campi nelle registrazioni personalizzandoli. Per ulteriori informazioni vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

### Convalida di batch registrazioni COGE

Puoi abilitare un controllo in background che ti aiuterà a prevenire ritardi durante la registrazione. Il controllo ti avviserà quando un errore nel giornale di registrazione finanziario su cui stai lavorando ti impedirà di pubblicare la registrazione. Nella pagina **Batch registrazioni COGE** è possibile scegliere **Controllo degli errori in background** per permettere a [!INCLUDE[prod_short](includes/prod_short.md)] di convalidare i giornali finanziari, come le registrazioni COGE o pagamenti, mentre ci si lavora.

Quando si abilita la convalida, la scheda dettaglio **Verifica registrazione** mostrerà i problemi nella riga corrente e nell'intero batch. La convalida si verifica quando si carica un batch registrazioni COGE e quando si sceglie un'altra riga di registrazione. Il riquadro **Problemi totali** nella scheda dettaglio mostra il numero totale di problemi rilevati da [!INCLUDE[prod_short](includes/prod_short.md)] ed è possibile selezionarlo per aprire una panoramica dei problemi.

È possibile utilizzare le azioni **Mostra righe con problemi** e **Mostra tutte le righe** per alternare tra le righe di registrazione che presentano o non presentano problemi. La scheda dettaglio **Dettagli riga di registrazione** fornisce una rapida panoramica e l'accesso ai dati dalle righe di registrazione, come il conto CoGe, il cliente o il fornitore e all'impostazione di registrazione per conti specifici.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## Informazioni su conti principali e contropartita

Se sono stati impostati conti di contropartita di default per i batch di registrazioni nella pagina **Registrazioni COGE**, il conto di contropartita verrà compilato automaticamente quando si inserisce un valore nel campo **Nr. conto**. In caso contrario, compila manualmente sia il campo **Nr. conto** che il campo **Contropartita**. Un importo positivo nel campo **Importo** viene addebitato sul conto principale e accreditato nella contropartita. Un importo negativo viene accreditato sul conto principale e addebitato nella contropartita.

> [!NOTE]  
> L'IVA viene calcolata separatamente per il conto principale e il conto di contropartita, quindi possono essere utilizzate percentuali IVA diverse.

## Utilizzare le registrazioni periodiche

Una registrazione periodica è una registrazione generale con campi specifici per la gestione di transazioni registrate frequentemente con poche o nessuna modifica. Ad esempio, transazioni per spese come affitto, sottoscrizioni, elettricità e riscaldamento. L'utilizzo delle registrazioni ricorrenti consente di registrare importi fissi e variabili e di specificare movimenti di storno automatico per il giorno successivo alla data di registrazione. Le chiavi di allocazione ti consentono di suddividere i movimenti ricorrenti tra vari conti. Per ulteriori informazioni vedi [Allocare importi di registrazioni periodiche a vari conti](#allocating-recurring-journal-amounts-to-several-accounts).

Utilizzando registrazioni periodiche, crei i movimenti che verranno registrati regolarmente solo una volta. Ad esempio, i conti, le dimensioni e i valori dimensioni e così via, resteranno nelle registrazioni dopo la contabilizzazione. Se sono necessarie modifiche, puoi apportarle ogni volta che esegui una registrazione.

### Campo Metodo ricorrenza

Il campo **Metodo ricorrenza** è importante. Determina come trattare l'importo nella riga delle registrazioni dopo la contabilizzazione. Se ad esempio utilizzi il medesimo importo per ogni registrazione, l'importo risulta invariato. Se nella riga vengono utilizzati i medesimi conti e testo e l'importo varia a ogni registrazione, sarà possibile eliminare l'importo dopo la registrazione.

| A | Vedere |
| --- | --- |
|F Fisso|l'importo specificato nella riga delle registrazioni rimarrà invariato dopo la contabilizzazione.|
|V Variabile|l'importo specificato nella riga delle registrazioni verrà eliminato dopo la contabilizzazione.|
|S Saldo|L'importo registrato nel conto specificato nella riga verrà allocato tra i conti specificati relativi alla riga nella tabella Allocazioni registrazioni gen. Il saldo nel conto risulterà uguale a zero. Compilare il campo **Allocazione %** nella pagina **Allocazioni**. Per ulteriori informazioni, vedere [Allocare importi di registrazioni periodiche a vari conti](#allocating-recurring-journal-amounts-to-several-accounts).|
|SC Storno costante|l'importo specificato nella riga delle registrazioni rimarrà invariato dopo la contabilizzazione e un movimento di quadratura verrà registrato il giorno seguente.|
|SV Storno variabile|l'importo specificato nella riga delle registrazioni verrà eliminato dopo la contabilizzazione e un movimento di quadratura verrà registrato il giorno seguente.|
|SS Storno saldo|L'importo registrato nel conto specificato nella riga verrà allocato tra i conti specificati relativi alla riga nella pagina **Allocazioni**. Il saldo nel conto verrà impostato su zero e un movimento di contropartita viene registrato il giorno seguente.|
|SD Saldo per dimensioni|La riga di registrazione alloca i costi in base al saldo di un conto C/G per dimensioni. Verrà richiesto di impostare i filtri di dimensione da utilizzare per calcolare il saldo del conto C/G di origine per dimensioni da cui si desidera allocare i costi. In alternativa, scegli l'azione **Imposta filtri dimensione** in un secondo momento.|
|SSD Storno saldo per dimensioni|La riga di registrazione alloca i costi in base allo storno saldo di un conto C/G per dimensioni. Verrà richiesto di impostare i filtri di dimensione da utilizzare per calcolare il saldo del conto C/G di origine per dimensioni da cui si desidera allocare i costi. Puoi anche scegliere l'azione **Imposta filtri dimensione** in un secondo momento.|

> [!NOTE]  
> È possibile immettere informazioni nei campi relativi all'IVA nella riga delle registrazioni periodiche o di allocazione ma non in entrambe. È possibile completarli nella pagina **Allocazioni** soltanto se le righe corrispondenti delle registrazioni periodiche non sono completate.

### Campo Frequenza ricorrenza

Questo campo della formula della data determina la frequenza di registrazione del movimento nella riga di registrazione e deve essere compilato. Ulteriori informazioni in [Usare le formule data](ui-enter-date-ranges.md#use-date-formulas).

#### Esempi

Se è necessario contabilizzare ogni mese la riga delle registrazioni, immettere "1M". Dopo ogni registrazione, la data indicata nel campo **Data di registrazione** verrà aggiornata alla stessa data del mese successivo.

Se si desidera registrare un movimento l'ultimo giorno di ogni mese, è possibile operare in uno dei modi descritti di seguito:

* Registrare il primo movimento l'ultimo giorno di un mese immettendo la formula 1G + 1M - 1G (1 giorno + 1 mese - 1 giorno). Con questa formula, la data di registrazione viene calcolata correttamente indipendentemente dalla lunghezza del mese.

* Registrare il primo movimento in qualsiasi giorno del mese immettendo 1M+CM. Con questa formula, la data di registrazione sarà dopo un mese intero + i giorni rimanenti del mese corrente.

### Campo Data di scadenza

Questo campo determina la data in cui la riga sarà registrata per l’ultima volta. Oltre tale data, la riga non verrà più registrata.

Quando si utilizza il campo Data di scadenza, la riga non viene immediatamente eliminata dalle registrazioni: È possibile inserire una data successiva in modo da poter utilizzare la riga in futuro.

Se il campo rimane vuoto, la riga verrà contabilizzata ogni volta fino a quando non verrà eliminata dalle registrazioni.

### Allocare importi di registrazioni periodiche a vari conti

Nella pagina **Reg. periodiche generali**, puoi scegliere l'azione **Allocazioni** per visualizzare o gestire il modo in cui gli importi nella riga delle registrazioni ricorrenti sono allocati a vari conti e dimensioni. L'allocazione è una riga delle registrazioni periodiche per la riga di contropartita.

Come in una registrazione periodica, immetti un'allocazione una volta e questa verrà conservata nelle registrazioni di allocazione dopo la registrazione. Non è necessario inserire importi e allocazioni ogni volta che si contabilizza la riga del giornale di registrazione ricorrente.

Se il metodo ricorrente nelle registrazioni periodiche viene impostato su **Saldo** o **Saldo a pareggio**, i codici valore dimensioni nelle registrazioni periodiche viene ignorato quando il conto risulta uguale a zero. Se viene allocata una riga ricorrente in valori dimensioni nella pagina **Allocazioni**, viene creato un solo movimento di pareggio.

> [!NOTE]
> Se viene allocata una riga delle registrazioni periodiche contenente un codice valore dimensioni, non immettere il medesimo codice nella pagina **Allocazioni**. In caso contrario, i valori dimensioni non risulteranno corretti.  

Per allocare gli importi di registrazioni periodiche in base alle dimensioni, imposta il campo **Metodo ricorrente** su **Saldo per dimensioni** o **Storno saldo per dimensioni**. Se il metodo ricorrente nelle registrazioni periodiche viene impostato su **Saldo per dimensioni** o **Storno saldo per dimensioni**, il codice valore dimensioni nelle registrazioni periodiche viene considerato quando il conto risulta uguale a zero. Se si assegna pertanto una riga ricorrente a vari valori di dimensione nella pagina **Allocazioni**, viene creato un numero di movimenti di storno corrispondente al numero di combinazioni di valori di dimensione di cui è composto il saldo. Se si alloca il saldo del conto tramite una registrazione ricorrente che contiene un codice valore di dimensioni, ricordarsi di utilizzare **Saldo per dimensioni** o **Storno saldo per dimensioni** per assicurarti che i valori delle dimensioni siano correttamente messe in saldo o stornate dal conto di origine.  

Si supponga ad esempio che una società disponga di un paio di Business Unit e alcuni reparti che i controller hanno impostato come dimensioni. Per velocizzare il processo di immissione delle fatture di acquisto, si decide di richiedere agli addetti alla contabilità fornitori di immettere solo le dimensioni della Business Unit. Poiché ogni Business Unit dispone di chiavi di allocazione specifiche per la dimensione Reparto, ad esempio in base al numero di dipendenti, è possibile utilizzare il metodo ricorrente **SD Saldo per dimensioni** o **SSD Storno saldo per dimensioni** per riallocare le spese per ciascuna Business Unit ai reparti appropriati in base alle chiavi di allocazione.  

> [!NOTE]
> Le dimensioni impostate nelle righe di allocazione non vengono calcolate automaticamente ed è necessario specificare quali valori di dimensioni devono essere impostati nei conti di allocazione. Qualora si desideri mantenere il collegamento tra la dimensione del conto di origine e la dimensione del conto di allocazione, è consigliabile utilizzare le funzionalità di [contabilità industriale](finance-about-cost-accounting.md).

#### Esempio: Allocare pagamenti di affitti a diversi reparti

L'importo dell'affitto mensile è stato immesso nel conto cassa specificato in una riga delle registrazioni periodiche. Nelle pagina **Allocazioni**, è possibile utilizzare la dimensione Reparto per suddividere la spesa tra più reparti. Ad esempio, in base al numero di piedi quadrati occupati da ciascun reparto. Il calcolo si basa sulla percentuale di allocazione relativa a ogni riga. È possibile allocarle in modi diversi:

* Immetti conti diversi su righe di allocazione diverse per suddividere le spese di affitto tra più conti.
* Immetti lo stesso conto ma utilizza codici valore dimensione diversi per la dimensione Reparto su ciascuna riga.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### Calcolare la data storno

Quando si utilizzano le registrazioni COGE ricorrenti per registrare i ratei alla fine di un periodo, è importante avere il pieno controllo sui movimenti di storno. Nella pagina **Registrazioni COGE ricorrenti** il campo **Calcolo data storno** consente di controllare la data in cui verranno registrati i movimenti di storno quando vengono utilizzati metodi ricorrenti di storno.

#### Esempio

I ratei vengono generalmente registrati con i metodi ricorrenti **Fisso**, **Variabile** o **Saldo** nella riga di registrazione. La data di registrazione dell'importo registrato nel conto nella riga di registrazione viene calcolata utilizzando la frequenza ricorrente. La data di registrazione per il movimento di contropartita viene calcolata utilizzando il campo **Calcolo data storno** come segue:

* Se il campo è vuoto, il movimento di contropartita verrà registrata il giorno successivo.
* Se il campo contiene una formula di data (ad esempio, **5G** per cinque giorni), il movimento di contropartita verrà registrato con una data di registrazione calcolata utilizzando il calcolo della data di storno.

> [!NOTE]
> Per impostazione predefinita, il campo **Calcolo data storno** non è disponibile nella pagina **Registrazioni COGE ricorrenti**. Per utilizzare il campo, è necessario aggiungerlo personalizzando la pagina. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

## Utilizzare le registrazioni standard

Quando si creano righe di registrazione che verranno probabilmente create di nuovo successivamente, è possibile scegliere di salvarle come registrazioni standard prima di contabilizzare la registrazione. Lo stesso si applica per le registrazioni di magazzino e le registrazioni COGE.

> [!NOTE]
> Le registrazioni standard possono non contenere tutti i campi che vuoi includere nei movimenti contabili risultanti. Ad esempio, se usi le registrazioni COGE standard per registrare un pagamento, i movimenti contabili non conterranno il campo Codice metodo di pagamento.

> [!NOTE]  
> Le seguenti procedure si riferiscono alle registrazioni magazzino, ma le informazioni sono valide anche per le registrazioni COGE.

### Per salvare una registrazione standard

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni articoli**, quindi scegli il collegamento correlato.
2. Immettere una o più righe di registrazione.
3. Selezionare le righe di registrazione che si desidera riutilizzare.
4. Scegliere l'azione **Salva come registrazioni standard**.
5. Nella pagina di richiesta **Salva come Registrazioni Magazzino Standard**, definire una registrazione di magazzino standard nuova o esistente in cui devono essere salvate le righe:

    Se sono già state create una o più registrazioni magazzino standard e si desidera sostituirne una con il nuovo insieme di righe di registrazione magazzino, seleziona la riga di registrazione magazzino nel campo **Codice**.
6. Scegli **OK** per verificare l'intenzione di sostituire il contenuto della registrazione magazzino standard esistente.
7. Per salvare i valori nel campo **Importo unitario** delle registrazioni magazzino standard, scegli il campo **Salva importo unitario**.
8. Per salvare i valori nel campo **Quantità**, scegli il campo **Salva quantità**.
9. Scegli **OK** per salvare la registrazione di magazzino standard.

Quando si salvano le registrazioni di magazzino standard, viene visualizzata la pagina Registrazioni magazzino in modo da poterle registrare.

### Per riutilizzare registrazioni standard

> [!NOTE]
> Le registrazioni standard non hanno sempre gli stessi campi delle registrazioni COGE. Quando usi l'azione Ottieni registrazioni standard per copiare i campi nelle registrazioni COGE, queste potrebbe contenere meno informazioni rispetto a quando le si creano manualmente. 

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni articoli**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Ottieni registrazioni standard**.
3. Per rivedere una registrazione di magazzino standard prima della relativa selezione a scopo di riutilizzo, scegliere l'azione **Mostra registrazioni**.

    Le modifiche apportate in una registrazione di magazzino standard vengono immediatamente implementate e risulteranno disponibili alla successiva apertura o al successivo riutilizzo della registrazione di magazzino standard. Assicurarsi che la modifica sia sufficientemente importante da essere applicata a livello generale. In caso contrario, apportare la modifica specifica nella registrazione di magazzino dopo l'aggiunta delle righe della registrazione di magazzino standard. Vedere il passaggio 4.
4. Nella pagina **Registrazioni magazzino standard** seleziona la registrazione di magazzino standard da riutilizzare e quindi scegli **OK**.

    La riga di registrazione magazzino contiene le righe salvate. Se la riga di registrazione magazzino contiene già righe, le nuove righe vengono visualizzate dopo di esse.

    Se non hai abilitato l'interruttore **Salva importo unitario** quando hai salvato le registrazioni, il campo **Importo unitario** sulle righe aggiunte dalle registrazioni standard contengono il valore dal campo **Costo unitario** sulla scheda articolo.

    > [!NOTE]  
    > Se hai abilitato gli interruttori **Salva importo unitario** o **Salva quantità** quando hai salvato le registrazioni, assicurati che i nuovi valori siano corretti prima di contabilizzare la registrazione magazzino.
    >
    > Se le righe di registrazione di magazzino inserite contengono importi unitari salvati che non vuoi contabilizzare, è possibile eseguire la rettifica al valore corrente dell'articolo.

5. Selezionare e righe di registrazioni magazzino che si desidera rettificare e scegliere l'azione **Ricalcola importo unitario**. Il campo Importo unitario verrà così aggiornato con il costo unitario corrente dell'articolo.
6. Scegli l'azione **Registra**.

## Rinumerare i documenti nei giornali di registrazione

Per evitare errori di registrazione dovuti al numero di documento, è possibile utilizzare l'azione **Rinumera documenti** prima di effettuare una registrazione.

In tutte le registrazioni basate sulle registrazioni COGE, il campo **Nr. documento** può essere modificato per poter specificare numeri di documento diversi in base alle diverse righe registrazioni o lo stesso numero di documento per le righe registrazioni correlate.

Se il campo **Nr. serie** nel batch registrazioni è compilato, la funzione di registrazione nelle registrazioni COGE richiede che il numero di documento nelle righe registrazioni singole o raggruppate segua un ordine sequenziale. Scegliere l'azione **Rinumera documenti** e i relativi campi **Nr. documento** vengono quindi aggiornati. Se le righe registrazioni correlate sono state raggruppate in base al numero del documento prima dell'utilizzo della funzione, rimarranno raggruppate, anche se potrebbero essere assegnate a un numero di documento diverso.  

Questa funzione può anche essere utilizzata sulle viste filtrate.

La rinumerazione dei documenti rispetterà i collegamenti correlati, ad esempio il collegamento di un pagamento tra il documento nella riga registrazioni e un conto fornitore. Di conseguenza, i campi **Collega-a ID** e **Collega-a nr. doc.** verranno aggiornati nei movimenti contabili fornitori.

### Per rinumerare i documenti nei giornali di registrazione

La procedura riportata di seguito è basata sulla pagina **Registrazione COGE**, ma si applica a tutte le altre registrazioni basate sulle registrazioni COGE, ad esempio la pagina **Registraz. pagamenti**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato.
2. Quando si è pronti per contabilizzare la registrazione, scegliere l'azione **Rinumera documenti**.

I valori nel campo **Nr. documento** vengono modificati, se necessario, in modo che il numero del documento nelle righe registrazioni singole o raggruppate seguano un ordine sequenziale. Dopo la rinumerazione dei documenti, è possibile contabilizzare le registrazioni.

## Vedi anche

[Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md)  
[Stornare le registrazioni e annullare carichi/spedizioni errati.](finance-how-reverse-journal-posting.md)  
[Allocazione di costi e ricavi](year-allocate-costs-income.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Rivalutare il magazzino nelle registrazioni rivalutazioni](inventory-how-revalue-inventory.md)  
[Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md)  
[Riconciliare i pagamenti clienti con la registrazione incassi o da movimenti contabili clienti](receivables-how-apply-sales-transactions-manually.md)  
[Riconciliare manualmente i pagamenti ai fornitori con la registrazioni pagamenti o dai movimenti contabili fornitori](payables-how-apply-purchase-transactions-manually.md)  
[Utilizzo di documenti e registrazioni intercompany](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
