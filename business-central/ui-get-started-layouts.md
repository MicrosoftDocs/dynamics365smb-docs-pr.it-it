---
title: Iniziare a creare layout
description: 'Informazioni su come creare i layout che consentono di personalizzare l''aspetto del report quando viene visualizzato, stampato o salvato.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Iniziare a creare layout di report

Business Central viene fornito con molti layout integrati che puoi utilizzare nei report. Altri layout potrebbero essere stati aggiunti come parte di altre estensioni. Ma è anche possibile creare i propri report da zero o basandosi su un layout esistente.

> [!IMPORTANT]
> Puoi utilizzare i layout anche per aggiungere contenuti ai messaggi di posta elettronica. Ad esempio, i layout dei report possono far risparmiare tempo e contribuire a garantire la coerenza riutilizzando lo stesso contenuto quando comunichi con i clienti. Per utilizzare i layout di report personalizzati con e-mail, il tipo di file per il layout deve essere Word. Non è possibile utilizzare il tipo di file RDLC. Per ulteriori informazioni, vedi [Impostare testi e layout e-mail riutilizzabili](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Sintesi

Quando si lavora con i layout di report, è utile pensare al layout come a un file importato e assegnato a un report. Indipendentemente dal tipo di layout, il modo in cui gestisci i layout in Business Central è sostanzialmente sempre lo stesso. Di solito, lavori dalla pagina **Layout report**. La differenza principale è la modalità di progettazione del layout, che viene eseguita utilizzando il software applicativo su cui è basato il layout, come Word, Excel o il Generatore report di SQL Server.

Occorre tenere questo concetto in mente. Ci sono fondamentalmente tre o quattro attività coinvolte nella creazione di un layout su un report:

1. Decidi il tipo di layout.
2. Esporta una copia di un layout esistente da utilizzare come punto di partenza.
3. Apporta le modifiche al file di layout nell'applicazione appropriata.
4. Aggiungi il nuovo file di layout al report.

> [!IMPORTANT]
> Non puoi modificare o sostituire un layout di estensione, che è un layout che ha origine da un'estensione. Puoi solo modificare o sostituire i layout definiti dall'utente. Nella pagina **Layout report** puoi sapere se il layout è di estensione o definito dall'utente guardando la colonna **Estensione**. Un layout di estensione mostrerà le informazioni sull'estensione di origine nella colonna. La colonna **Estensione** sarà vuota per un layout definito dall'utente.
>
> Per ulteriori informazioni sulla differenza tra i layout delle estensioni e i layout definiti dall'utente, vedi [Origine del layout](ui-manage-report-layouts.md#layout-sources).

## Inizia

A seconda della tua situazione, le attività possono variare. Utilizza la tabella seguente per iniziare.

|Cosa vuoi fare?|Vedi...|
|-----------------------|------|
|Individuare qual è il miglior tipo di layout da utilizzare per la situazione corrente|[Decidere quale tipo di layout usare](#decide)|
|Creare un nuovo layout per un report basato su un layout esistente, mantenendo il layout esistente così com'è.|[Creare un nuovo layout](#create)|
|Apportare modifiche a un layout esistente utilizzato in un report|[Modificare un layout](#modify)|
|Ho una nuova versione di un file di layout per un report. Desidero sostituire il file di layout esistente.|[Sostituire un layout](#replace)|
|Cambiare il layout corrente utilizzato da un report in un altro layout|[Impostare il layout utilizzato da un report](ui-set-report-layout.md)|
|Modificare il nome e la descrizione di un layout|[Rinominare un layout](#rename)|

## <a name="decide"></a>Decidere quale tipo di layout usare

La prima cosa quando si crea un layout è decidere quale [tipo di layout](ui-manage-report-layouts.md#layout-types) usare. Puoi scegliere tra Word, Excel o RDLC. Il tipo di layout dipenderà da come vuoi che appaia il report generato. Inoltre, dipende dalla tua conoscenza del software applicativo per la creazione dei layout, come Word, Excel e il Generatore report di SQL Server.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* I layout di Excel sono generalmente i più facili da creare e modificare perché le funzionalità per il riepilogo dei dati, l'aggiunta di grafica e stile sono funzionalità comuni di Excel.

* Non tutti i report e i documenti dispongono di un set di dati ottimizzato per l'uso di un layout Excel. Ad esempio, le aggregazioni e i calcoli complessi funzionano meglio con i layout RDLC o Word. Lo stesso vale per i documenti.

* Se stai solo apportando modifiche allo stile come il tipo di carattere, la dimensione e i colori, anche un layout di Word è una buona scelta.

* L'aggiunta di campi dati o la riorganizzazione dei campi dati in Word o RDLC è più avanzata rispetto a Excel.

* I layout Word e RDLC sono utili per i report che verranno infine stampati.  

* I concetti di progetto generali dei layout Word e RDLC sono simili. Tuttavia ogni tipologia presenta determinate caratteristiche progettuali che influiscono sulla visualizzazione del report generato in [!INCLUDE[prod_short](includes/prod_short.md)]. Lo stesso report può apparire diverso quando si utilizza il layout di Word rispetto al layout di RDLC.

## <a name="create"></a>Creare un nuovo layout

Esistono due modi per creare un nuovo layout da un layout esistente. Un modo è salvare una copia del layout esistente. L'altro modo è esportare il layout esistente.

## [Copia](#tab/copy)

La copia è un modo rapido per creare un nuovo layout uguale a un layout esistente. Una volta ottenuta la copia, apporterai modifiche esportando il layout. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleziona il layout di cui desideri una copia per il nuovo layout, quindi scegli l'azione **Modifica informazioni**.

    Se hai selezionato un layout di estensione, ti verrà chiesto se desideri modificare una copia. Seleziona **Sì** per continuare.

    > [!TIP]
    > Per trovare il layout, usa la casella **Ricerca**, il riquadro **Filtro** e l'ordinamento delle colonne.
3. Cambia il **Nome layout**.
4. Imposta l'interruttore **Salva le modifiche in una copia** su **Attivo**, quindi seleziona **OK**

   Il nuovo layout viene visualizzato nella pagina **Layout report**.
5. Se desideri apportare modifiche al nuovo layout, vedi [Modificare un layout esistente](#modify).

### [Esportazione/importazione](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleziona il layout di cui desideri una copia per il nuovo layout, quindi scegli l'azione **Esporta layout**.

   Il file di layout viene scaricato sul dispositivo. 

    > [!TIP]
    > Per trovare il layout, usa la casella **Ricerca**, il riquadro **Filtro** e l'ordinamento delle colonne.

3. Apri il file di layout nell'applicazione appropriata, come Word (per un file .docx) o Excel (per un file .xlsx).

   Per ulteriori informazioni, vedi:

   * [Utilizzare i layout di Word](ui-how-add-fields-word-report-layout.md)
   * [Utilizzare i layout di Excel](ui-excel-report-layouts.md)
   * [Utilizzare i layout di RDLC](ui-rdlc-report-layouts.md)

   Apporta le modifiche al file e salvalo.

4. Torna alla pagina **Layout report**, seleziona l'azione **Nuovo layout**.
5. Compila i seguenti campi:

   |Campo|Descrizione|Obbligatorio|
   |-----|-----------|---------|
   |ID report|Impostato sull'ID assegnato al report|si|
   |Nome layout| Digita un nome breve per la descrizione del layout per identificarlo facilmente.|si|
   |Descrizione| Digita informazioni più dettagliate sul layout. |no|
   |Opzioni di formattazione|Imposta questo campo in modo che corrisponda al tipo di layout, come Word, Excel o RDLC.|si|

6. Seleziona **OK**, quindi esegui una delle seguenti operazioni per caricare il file di layout per il report:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Il file selezionato viene caricato nel layout e torni alla pagina **Layout report**.

Se vuoi vedere come appare il report con il nuovo layout, seleziona il layout nell'elenco, quindi seleziona **Esegui report**.

---

## <a name="modify"></a>Modificare un layout

Attieniti alla seguente procedura per modificare un layout definito dall'utente esistente.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Scegli il layout che vuoi modificare, quindi scegli l'azione **Esporta layout**.

   Il file di layout viene scaricato sul dispositivo. 

   > [!TIP]
   > Per trovare il layout, usa la casella **Ricerca**, il riquadro **Filtro** e l'ordinamento delle colonne.

3. Apri il file di layout nell'applicazione appropriata, come Word (per un file .docx) o Excel (per un file .xlsx).

   Per ulteriori informazioni, vedi:

   * [Utilizzare i layout di Word](ui-how-add-fields-word-report-layout.md)
   * [Utilizzare i layout di Excel](ui-excel-report-layouts.md)
   * [Utilizzare i layout di RDLC](ui-rdlc-report-layouts.md)

   Apporta le modifiche al file e salvalo.

4. Torna alla pagina **Layout report**, seleziona il layout esistente, quindi seleziona l'azione **Sostituisci layout**.
5. Seleziona **OK** > **Scegli** di aprire Esplora file sul tuo dispositivo.
6. Trova e seleziona il file di Excel quindi seleziona **Apri**.

   Il file selezionato viene caricato nel layout e torni alla pagina **Layout report**.
7. Se vuoi vedere come appare il report con il nuovo layout, seleziona il layout nell'elenco, quindi seleziona **Esegui report**.

## <a name="replace"></a>Sostituire un layout

Attieniti alla seguente procedura per sostituire il file di layout definito dall'utente esistente con un nuovo file.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleziona il layout esistente, quindi seleziona l'azione **Sostituisci layout**.
3. Seleziona **OK** > **Scegli** di aprire Esplora file sul tuo dispositivo.
4. Trova e seleziona il file di Excel quindi seleziona **Apri**.

   Il file selezionato viene caricato nel layout e torni alla pagina **Layout report**.
5. Se vuoi vedere come appare il report con il nuovo layout, seleziona il layout nell'elenco, quindi seleziona **Esegui report**.

## <a name="rename"></a>Rinominare un layout

Attieniti alla seguente procedura per modificare il nome e la descrizione di un layout definito dall'utente.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Scegli il layout da rinominare quindi seleziona l'azione **Modifica informazioni**.

    > [!TIP]
    > Per trovare il layout, usa la casella **Ricerca**, il riquadro **Filtro** e l'ordinamento delle colonne.
3. Cambia il **Nome layout**, quindi seleziona **OK**.

## Vedi anche

[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Utilizzare i layout di Word](ui-how-add-fields-word-report-layout.md)  
[Utilizzo dei layout di Excel](ui-excel-report-layouts.md)  
[Utilizzo di report, processi batch e XMLport](ui-work-report.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
