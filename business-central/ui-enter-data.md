---
title: Immettere dati in Business Central
description: 'Sono disponibili numerose funzionalità generali che consentono di immettere dati più facilmente, più velocemente e in modo più preciso. Sono descritti i principi di base e le funzionalità avanzate.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'decimal separator, data entry, focus'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 03/23/2022
ms.author: jswymer
---
# <a name="entering-data" />Immissione di dati

Sono disponibili numerose funzionalità generali che consentono di immettere dati più facilmente, più velocemente e in modo più preciso. In questo articolo sono descritte tutte le funzionalità avanzate e i principi di base per l'immissione di dati.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Gli esempi in questo articolo utilizzano dati di esempio.

## <a name="work-with-editable-fields" />Utilizzare i campi modificabili

I campi in [!INCLUDE[prod_short](includes/prod_short.md)] possono contenere diversi dati modificabili, ad esempio importi in valuta o testo. I campi modificabili in genere mostrano una casella di input in cui è possibile digitare o scegliere un valore. I campi non modificabili sono in genere visualizzati con uno sfondo grigio.   

Alcuni campi modificabili forniscono un selettore per consentire di specificare un valore.  

<!-- TODO: Add illustrations or images of each picker -->
|**Addetto al prelievo**        |**Come consente di specificare un valore**|
|------------------|------------------------------------|
|Selettore di data       |Questo selettore visualizza un calendario basato sulle impostazioni internazionali correnti. Consente di scegliere una singola data.|
|Menu a discesa          |I menu a discesa offrono una scelta di valori fissi o record di riferimento da un'altra tabella.|
|Interruttore o casella di controllo|Alcuni campi offrono una semplice scelta di valori *Sì* o *No*. L'interruttore viene utilizzato per specificare questo valore ed è sempre visualizzato come una casella di controllo negli elenchi.|
|Assist-edit       |Alcuni campi offrono selettori personalizzati adatti a cercare e scegliere il valore migliore per quel campo, come la finestra popup.|

### <a name="modifying-a-field-value" />Modifica di un valore di campo

Per modificare il valore di un campo, è necessario innanzitutto impostare lo stato attivo su quel campo. È possibile impostare lo stato attivo tramite le seguenti azioni:

- Utilizzare il tasto <kbd>TAB</kbd>. L'azione seleziona l'intero valore.
- Fare clic con il tasto sinistro del mouse o dispositivo di input simile. Questa azione selezionerà l'intero valore di campo solo se il campo è in un elenco.  

Quando si interagisce con i campi nell'interfaccia utente, [!INCLUDE[prod_short](includes/prod_short.md)] in genere favorisce la selezione dell'intero valore di campo per semplificare la sostituzione di tale valore.

Quando viene selezionato l'intero valore di campo:
- Sostituire il valore semplicemente digitando per specificare un nuovo valore. Se il campo offre un selettore, è possibile attivarlo utilizzando i tasti di scelta rapida <kbd>Alt</kbd>+<kbd>freccia GIÙ</kbd>.
- Utilizzare il tasto <kbd>CANC</kbd> o <kbd>BACKSPACE</kbd> per cancellare il valore.

Premi il tasto <kbd>F2</kbd> per passare dalla selezione dell'intero valore di campo al posizionamento del cursore alla fine del valore di campo. Posizionando il cursore alla fine del valore, è più facile accodarsi al valore esistente.

Quando il cursore viene visualizzato alla fine del valore di campo:
- Aggiungere al valore semplicemente digitando.
- Usa i tasti <kbd>HOME</kbd>, <kbd>FINE</kbd>, <kbd>freccia SINISTRA</kbd> e <kbd>Freccia DESTRA</kbd> per spostare il cursore all'interno del valore. Se modifichi un campo in un elenco, premi il tasto <kbd>Freccia SINISTRA</kbd> di nuovo quando il cursore si trova all'inizio del valore metterà lo stato attivo sul campo precedente. Allo stesso modo, premendo il tasto <kbd>Freccia DESTRA</kbd> di nuovo quando il cursore si trova alla fine del valore metterà lo stato attivo sul campo successivo.

> [!NOTE]
> Dopo aver specificato un valore, Business Central verificherà che sia valido solo dopo aver fatto clic all'esterno del campo o impostato lo stato attivo su un altro elemento, ad esempio il campo successivo.  

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]

## <a name="keyboard-shortcuts" />Tasti di scelta rapida

Esistono diversi tasti di scelta rapida che consentono di lavorare "senza mouse" e di velocizzare l'immissione dei dati. Questi tasti di scelta rapida sono particolarmente utili con immissioni su larga scala e attività di digitazione ripetitive.

Per ulteriori informazioni sui tasti di scelta rapida, vedere [Tasti di scelta rapida](keyboard-shortcuts.md). Alcuni dei tasti di scelta rapida vengono discussi in questo articolo.

## <a name="a-namequickentryaaccelerating-data-entry-using-quick-entry" /><a name="QuickEntry"></a>Accelerazione dell'immissione di dati utilizzando Accesso rapido

Accesso rapido è una funzionalità concepita per l'immissione di dati utilizzando la tastiera. La funzionalità di Accesso rapido viene utilizzata nei campi (come nelle pagine scheda) e negli elenchi (righe e colonne). È utile quando si eseguono attività di digitazione ripetitive che richiedono la creazione di più record in sequenza. Gli esempi includono un batch di ordini di vendita o la registrazione di nuovi articoli.

È possibile usare il tasto TAB per spostarsi da un campo in una pagina al campo modificabile successivo. Uno svantaggio inerente all'utilizzo del tasto TAB è che sposta sempre lo stato attivo al campo seguente in modo sequenziale. <!-- even if the field is non-editable or seldom filled it in.-->Accesso rapido funziona in un altro modo. Con la funzione Accesso rapido è possibile di utilizzare il tasto <kbd>INVIO</kbd> per spostarsi solo tra i campi interessati. Accesso rapido ignora i campi non modificabili e i campi che in genere non vengono compilati. È possibile che questo comportamento sia già stato osservato in alcune pagine. Questo comportamento perché i campi da includere quando si preme invio e quali ignorare sono stati predefiniti. È possibile personalizzare Accesso rapido personalizzando l'area di lavoro e ottimizzando il modo di immissione dei dati in ogni pagina.

### <a name="how-quick-entry-works" />Funzionamento di Accesso rapido

Ogni campo può essere contrassegnato come *incluso in Accesso rapido* o *escluso da Accesso rapido*. I campi inclusi in Accesso rapido verranno inclusi nel percorso quando si preme <kbd>INVIO</kbd>. I campi esclusi da Accesso rapido non lo saranno.

Al termine dell'immissione dei dati in un campo, premi semplicemente <kbd>INVIO</kbd> per confermare le modifiche e accedere al campo seguente. Per invertire la direzione e accedere al campo precedente, premi <kbd>MAIUSC</kbd>+<kbd>INVIO</kbd>. Per ulteriori informazioni sui tasti di scelta rapida, vedere [Scelte rapide di Accesso rapido per campi](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks" />Suggerimenti e trucchi

L'elenco di seguito fornisce alcune informazioni utili sull'utilizzo di Accesso rapido.

- È disponibile per qualsiasi campo modificabile.
- Funziona anche con colonne e righe.
- Non impedisce l'accesso ad altri elementi di una pagina, ad esempio le azioni. Questi elementi sono sempre accessibili utilizzando <kbd>Tab</kbd> e <kbd>MAIUSC</kbd>+<kbd>Tab</kbd>.  
- Non è necessario che le Schede dettaglio siano espanse affinché Accesso rapido funzioni. Se il campo Accesso rapido successivo si trova in una Scheda dettaglio compressa, quella scheda verrà espansa automaticamente e lo stato attivo sarà sul campo scelto. [!INCLUDE[prod_short](includes/prod_short.md)] ricorderà che la Scheda dettaglio dovrebbe essere espansa alla successiva visita della pagina.  
- Il funzionamento di Accesso rapido è indipendente dal fatto che i campi siano obbligatori o meno. È quindi opportuno assicurarsi che i campi obbligatori siano inclusi in Accesso rapido.
- Per impostazione predefinita, la maggior parte dei campi vengono automaticamente inclusi in Accesso rapido. Quindi inizialmente la task escluderà probabilmente i campi da Accesso rapido.

### <a name="to-change-quick-entry-fields" />Come modificare i campi Accesso rapido

Per impostare Accesso rapido nei campi, utilizzare la personalizzazione.

1. Inizia la personalizzazione selezionando l'icona ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") e poi l'azione **Personalizza**.
2. Selezionare un campo da modificare. Negli elenchi, selezionare l'intestazione di colonna corrispondente. Quindi, scegliere **Includi in Accesso rapido** o **Escludi da Accesso rapido**.

Per ulteriori informazioni sulla personalizzazione, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

## <a name="mandatory-fields" />Campi obbligatori

Quando si immettono dati nelle pagine, alcuni campi sono contrassegnati con un asterisco rosso. L'asterisco rosso indica che il campo deve essere compilato per completare un determinato processo. Un esempio è il caso in cui si registra una transazione che utilizza il valore nel campo.  

Anche se il campo è obbligatorio, non è obbligatorio compilarlo prima di continuare con altri campi o chiudere la pagina. L'asterisco rosso è solo un promemoria che segnala che l'utente sarà bloccato e non potrà completare un determinato processo.  

## <a name="finding-data-as-you-type" />Trovare dati durante la digitazione

 Quando si inizia a digitare dei caratteri in un campo, un elenco a discesa visualizza i valori di campo possibili. L'elenco cambia se si digitano ulteriori caratteri ed è possibile selezionare il valore corretto quando viene visualizzato.  

 In molti campi è disponibile un pulsante Freccia GIÙ che è possibile selezionare. Facendo clic sulla freccia, è possibile ottenere un elenco di tutti i dati disponibili in un quel campo. Il pulsante ha due funzioni, a seconda del tipo di campo:  

- Lookup - Vengono visualizzate informazioni di un'altra tabella che possono essere immesse nel campo. È possibile selezionare soltanto un dato alla volta.  

- DropDown - Vengono visualizzate le scelte possibili per il campo. È possibile selezionare soltanto una delle opzioni.  

## <a name="copying-and-pasting-faq-fields-and-lines" />Copiare e incollare campi e righe

È possibile copiare una o più righe da un elenco o da un singolo campo in una pagina. Quindi incollare ciò che è stato copiato nella stessa pagina, in un'altra pagina o in un documento esterno. Ad esempio, è possibile incollare Microsoft Excel o e-mail di Outlook. In breve, per copiare, premi <kbd>Ctrl</kbd>+<kbd>C</kbd> (cmd+C in macOS) sulla tastiera. Per incollare, premi <kbd>Ctrl</kbd>+<kbd>V</kbd> o <kbd>cmd+V</kbd> in macOS.

In un elenco, per copiare il campo nella stessa colonna della riga precedente e incollarlo nella riga corrente, premi <kbd>F8</kbd>.

Per ulteriori informazioni, vedere [Domande frequenti sulla funzionalità di copia e incolla](faq-copy-paste.yml).

## <a name="filtering-line-items" />Filtri delle voci

Per avviare il filtro, seleziona ![l'icona riquadro Filtro](media/open-filter-pane-icon.png "Icona del riquadro filtri") nella parte superiore dell'elenco o premi <kbd>MAIUSC</kbd>+<kbd>F3</kbd> per aprire il riquadro Filtro. il riquadro Filtro viene utilizzato come qualsiasi altro elenco. Per ulteriori informazioni, vedere [Filtri](ui-enter-criteria-filters.md#filtering).

I filtri sono particolarmente utili quando si visualizzano e analizzano i documenti più lunghi. Si supponga di aprire una fattura di vendita registrata. Quindi, filtrare le voci per visualizzare tutte le voci che hanno uno sconto individuale superiore al 5%. In alternativa, filtrare per visualizzare solo gli accessori per bici con "pro" nel nome.

## <a name="a-namefocusafocusing-on-line-items" /><a name="Focus"></a>Spostamento dello stato attivo sulle voci

Quando si lavora su documenti che includono una parte Voci, è possibile spostare lo stato attivo solo sulle voci. I documenti di esempio sono l'ordine di vendita o la pagina della fattura. La parte Voci si espande in modo da occupare quasi l'intera area di lavoro. Nasconde altre parti della pagina tranne l'area delle azioni in alto. Questo layout offre una migliore panoramica delle voci e maggiore spazio per utilizzarle.

Si rivela particolarmente utile quando si lavora con liste articoli di grandi dimensioni e si desidera inserire dati rapidamente. Questa funzione offre anche funzionalità di filtro avanzate. Come in altre liste, la navigazione e la ricerca tra le voci diventa ancora più semplice.

### <a name="switching-the-focus-on-and-off" />Attivare/disattivare lo stato attivo

Per concentrarti sulle voci, seleziona un punto qualsiasi nella parte della voce, quindi scegli l'![icona Modalità messa a fuoco.](media/focus-mode.png "Icona Modalità messa a fuoco") nell'angolo in alto a destra o premi <kbd>Ctrl</kbd>+<kbd>Maiusc</kbd>+<kbd>F12</kbd>.

Per tornare alla visualizzazione normale, scegli l'![Icona Modalità messa a fuoco.](media/focus-mode.png "Icona Modalità messa a fuoco") oppure premi <kbd>Ctrl</kbd>+<kbd>Maiusc</kbd>+<kbd>F12</kbd> di nuovo.

## <a name="multitasking-across-multiple-pages" />Multitasking in più pagine

È possibile aprire una pagina della scheda o del documento in una nuova finestra. L'apertura di una nuova finestra consente di:

- Lavorare su più attività contemporaneamente.
- Gestire le interruzioni per l'attività corrente, ad esempio rispondere a una chiamata in arrivo.
- Tenere aperta una finestra per un'attività in corso mentre si avvia o si completa un'altra attività in una o più finestre.

Per aprire la scheda o il documento corrente in una nuova finestra, scegli ![Apri in un'altra finestra.](media/open-new-window-icon.png "Icona Apri in un'altra finestra") nell'angolo in alto a destra o premi <kbd>Alt</kbd>+<kbd>Maiusc</kbd>+<kbd>W</kbd>.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->

> [!NOTE]
> Quando apri altre pagine da una scheda o un documento aperto in una nuova finestra, quelle pagine si apriranno in una nuova finestra anche se non scegli ![Apri in un'altra finestra.](media/open-new-window-icon.png "Icona Apri in un'altra finestra").

> [!NOTE]
> Se si utilizza il browser Safari, la funzionalità Blocco popup potrebbe impedire l'apertura della nuova finestra. In tal caso, specificare l'URL del prodotto come sito Web consentito. Per informazioni vedere, [Modificare le preferenze in Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Lo stesso può accadere in altri browser, come Firefox. Per ulteriori informazioni, vedere [Impostazioni di blocco popup in Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Un altro modo per eseguire il multitasking è aprire [!INCLUDE[prod_short](includes/prod_short.md)] su due o più schede del browser. Quando si esegue questa operazione, è necessario creare una nuova scheda e quindi copiare/incollare l'URL della scheda originale nella nuova scheda. Questo crea una nuova sessione.   

> [!NOTE]
> Non utilizzare la funzione **Duplica** del browser per creare la nuova scheda in quanto le azioni su una scheda potrebbero bloccare le azioni su altre schede perché fanno parte della stessa sessione.

## <a name="entering-quantities-by-calculation" />Immettere quantità mediante calcolo

Quando si immettono numeri nei campi numerici come il campo **Quantità** in una riga di registrazione magazzino, è possibile immettere la formula invece della quantità della somma.  

### <a name="examples" />Esempi

- Se si immette 19+19, il valore del campo viene calcolato in 38.  

- Se si immette 41-9, il valore del campo viene calcolato in 32.  

- Se si immette 12*4, il valore del campo viene calcolato in 48.  

- Se si immette 12/4, il valore del campo viene calcolato in 3.  

## <a name="entering-negative-numbers" />Immettere numeri negativi

È possibile immettere numeri negativi in due modi. Il numero -20,5 può essere immesso come:  

- -20,5  

  oppure
- 20,5-  

In entrambi i casi, l'importo verrà registrato come -20,5.  

Se l'ultimo carattere dell'espressione è un **+** o un **-**, l'intera espressione verrà registrata con tale segno. Ad esempio **10-20+** restituirà 10 e non -10.  

## <a name="entering-dates-and-times" />Immissione di date e ore

È possibile immettere date e ore in tutti i campi assegnati alle date (campi di data). È possibile immettere date con o senza separatori.

> [!NOTE]  
> La modalità di immissione di date e ore dipende dalle impostazioni di **Area geografica**. Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).  

### <a name="entering-dates" />Immissione di date

È possibile utilizzare il selettore di data per selezionare una data da un calendario oppure immettere manualmente le date. Questa sezione fornisce una breve panoramica della modalità di immissione di date. Per ulteriori informazioni, vedi [Utilizzare date e orari del calendario](ui-enter-date-ranges.md).

Per l'immissione manuale di date, è possibile due, quattro, sei o otto cifre:  

- Due cifre sono interpretate come il giorno. Aggiungerà il mese e l'anno della data del lavoro.  

- Quattro cifre sono interpretate come il giorno e il mese. Aggiungerà l'anno della data del lavoro.  

- Se la data desiderata è compresa tra il 01/01/1950 e il 31/12/2049, inserire l'anno con due cifre. Altrimenti, inserire l'anno con quattro cifre.

  > [!NOTE]
  > Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] in locale, l'intervallo di anni a due cifre potrebbe essere diverso. Gli amministratori possono modificare l'intervallo modificando l'impostazione **CalendarTwoDigitYearMax** del server [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Configurazione di Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).

È possibile immettere anche una data come giorno della settimana seguito da un numero di settimana. In alternativa, è possibile immettere un anno. Ad esempio, Lun25 o lun25 indica il lunedì della settimana 25.  

Anziché immettere una data specifica, è possibile immettere uno di questi codici.  

|Code|Risultato|  
|--------------|----------------|  
|o|Specifica la data odierna (la data di sistema del computer).|  
|p|Specifica un periodo contabile, dove p indica il primo periodo contabile, p2 indica il secondo periodo contabile e così via. |
|l|Specifica la data del lavoro impostata nell'applicazione. Per modificare la data di lavoro, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md). Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.|
|c|Indica che la data dopo c è una data di chiusura, ad esempio C123101.|  

## <a name="entering-times" />Immissione di ore

Quando si immette l'ora, è possibile inserire qualsiasi separatore tra le unità. L'immissione di un separatore è tuttavia facoltativa. Non è necessario immettere i minuti, i secondi o l'indicazione AM/PM.  

Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti.  

|Immissione|Interpretazione|  
|---------------|------------------------|  
|5|05.00.00|  
|5:30|05.30.00|  
|0530|05.30.00|  
|5:30:5|05.30.05|  
|053005|05.30.05|  
|5:30:5.50|05:30:05,5|  
|053005050|05.30.05,05|  

 Se non si utilizza un separatore, è necessario immettere due cifre per ciascuna unità di tempo.  

## <a name="entering-combined-datetimes" />Immissione di date e ore combinate

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration" />Immissione della durata

È possibile immettere una durata in caratteri numerici seguiti dalla relativa unità di misura.  

Di seguito vengono forniti alcuni esempi.  

|Durata|Unità di misura**|  
|------------------|-------------------------|  
|2h|2 ore|  
|6h 30 m|6 ore 30 minuti|  
|6.5h|6 ore 30 minuti|  
|90m|1 ora 30 minuti|  
|2d 6h 30m|2 giorni 6 ore 30 minuti|  
|2d 6h 30m 56s 600ms|2 giorni 6 ore 30 minuti 56 secondi 600 millisecondi|  

 È inoltre possibile immettere un numero in modo che venga automaticamente convertito in una durata. Il numero immesso viene convertito in base all'unità di misura predefinita specificata nel campo relativo alla durata.  

 Per visualizzare l'unità di misura utilizzata in un campo di durata, immettere un numero e controllare l'unità di misura in cui viene convertito.  

 Il numero 5 viene convertito in 5 h se l'unità di misura è l'ora.  

## <a name="a-namedecimalasetting-the-decimal-separator-used-by-numeric-keyboards" /><a name="decimal"></a>Impostazione del separatore decimale usato dalle tastiere numeriche

Quando usi il tasto <kbd>separatore decimale</kbd> della tastiera numerica per inserire i dati, il separatore decimale effettivo che viene inserito nel campo è determinato dall'impostazione dell'area geografica in Business Central. La maggior parte delle aree geografiche utilizza il simbolo del punto (.) o della virgola (,) come separatore per i valori decimali, come in genere vedi negli importi in valuta. Il tasto decimale sulla tastierina si adatta alla tua area geografica. Spesso è diverso dai tasti punto o virgola sul resto della tastiera. Imposti l'area geografica in Business Central nella pagina **Impostazioni personali** .

Per esempio, supponiamo che stai usando una tastiera numerica che usa un punto (.) come <kbd>tasto separatore decimale</kbd>. Ma, stai inserendo dati per una lingua regionale che usa una virgola (**,**) per il separatore decimale, come il francese (Francia). Quindi, volete che i decimali come "1,23" siano inseriti come "1,23". In questo caso, puoi andare alla pagina **Impostazioni personali** e impostare **Area geografica** sulla lingua regionale di destinazione, come il **francese (Francia)**. Per maggiori informazioni, vedere [Cambiare le impostazioni di base](ui-change-basic-settings.md#region).

> [!TIP]
> Potrebbero esserci occasioni in cui vuoi utilizzare il separatore decimale per inserire un punto (.). Ad esempio, supponi di inserire un intervallo di date in un filtro, ad esempio `01/01/2022..04/01/2022`, o qualsiasi cosa che richieda un punto. Per risolvere questo caso, premi i tasti <kbd>Alt</kbd>+<kbd>Separatore decimale</kbd> sulla tastiera numerica. Questa combinazione di tasti cambia il separatore decimale tra l'emissione di un punto e del separatore decimale determinato dall'impostazione **Area geografica**.

## <a name="see-related-microsoft-trainingtrainingmodulesexplore-modify-info-dynamics--business-central" />Vedi il relativo [training Microsoft](/training/modules/explore-modify-info-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

[Ricerca, filtro e ordinamento di elenchi](ui-enter-criteria-filters.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
