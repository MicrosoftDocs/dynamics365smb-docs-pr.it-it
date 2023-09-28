---
title: 'Ricerca, filtro e ordinamento di elenchi'
description: 'Utilizzare in modo efficiente gli elenchi cercando nei dati, ordinando colonne e perfezionando i risultati con simboli di filtro e tasti di scelta rapida da tastiera.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 04/01/2021
ms.author: jswymer
---
# Ricerca, filtro e ordinamento

Ordinamento, ricerca e filtro sono alcune delle operazioni che semplificano l'individuazione, l'analisi e la limitazione di record in un elenco o in un XMLport o report. È possibile collegare alcune o tutte le procedure contemporaneamente a rapidamente per trovare o analizzare rapidamente i dati.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Per i report e gli XMLport, è possibile impostare filtri come negli elenchi per delimitare i dati da includere in report o XMLport, ma non è possibile ordinare e cercare.

> [!TIP]
> Quando si visualizzano i dati come riquadri, è possibile cercare e utilizzare i filtri. Per utilizzare il set completo delle potenti funzionalità di ordinamento, ricerca e filtro, scegliere l'icona ![Mostra come lista.](media/ui_show_as_list_icon.png "Freccia sinistra Mostra come lista") per visualizzare i record in forma di elenco.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## Ordinamento

L'ordinamento consente di ottenere in modo semplice e rapido una panoramica dei dati. Ad esempio, se si dispone di molti clienti, si potrebbe ordinarli in base a **Nr. cliente**, **Codice valuta** o **Codice paese** per ottenere la panoramica desiderata.

Per ordinare un elenco, è possibile:

- Selezionare il testo di un'intestazione di colonna per passare dall'ordinamento ascendente a quello discendente e viceversa, oppure
- Scegliere la freccia del menu a discesa nell'intestazione della colonna, quindi scegliere l'azione **Ascendente** o **Discendente**.  

> [!NOTE]  
> L'ordinamento non è supportato nelle immagini, nei campi BLOB, in FlowFilter e nei campi che non appartengono a una tabella.  

## Ricerca

<!--## Searching by using the Quick Filter -->
Nella parte superiore di ogni pagina elenco, c'è un'azione ![Cerca nell'elenco.](media/ui-search/search-list.png "Icona Cerca nell'elenco") **Cerca** che fornisce un modo rapido e semplice per ridurre i record in un elenco e visualizzare solo i record che contengono i dati che si intende visualizzare.

Per cercare, è sufficiente selezionare l'azione **Cerca**, quindi nella casella digitare il testo che si sta cercando. È possibile immettere lettere, numeri e altri simboli.

In generale, la ricerca tenta di trovare il testo corrispondente in tutti i campi, non fa la distinzione tra maiuscole e minuscole e trova il testo corrispondente ovunque nel campo (all'inizio, alla fine o nel mezzo).

> [!TIP]
> È possibile premere <kbd>F3</kbd> per attivare e disattivare la casella di ricerca. Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> La ricerca non restituisce i valori di immagini, campi BLOB, FlowFilters, FlowField e altri campi che non fanno parte di una tabella.


### Perfezionamento della ricerca con criteri di filtro

È possibile effettuare una ricerca più precisa utilizzando operatori di filtro, espressioni e token di filtro. A differenza dei filtri, questi vengono applicati a tutti i campi quando utilizzati nella casella di ricerca, rendendoli meno efficienti dei filtri.

- Per trovare solo i valori dei campi che corrispondono esattamente all'intero testo e all'uso di maiuscole/minuscole, posizionare il testo di ricerca tra virgolette singole `''` (ad esempio `'man'`).

- Per trovare valori di campo che iniziano con un determinato testo e corrispondono all'uso di maiuscole/minuscole, posizionare `*` dopo il testo di ricerca (ad esempio `man*`).

- Per trovare valori di campo che terminano con un determinato testo e corrispondono all'utilizzo di maiuscole/minuscole, posizionare `*` prima del testo di ricerca (ad esempio `*man`).

- Quando si utilizza `''` o `*`, la ricerca è sensibile alla distinzione maiuscola/minuscola. Se si desidera ignorare la distinzione tra maiuscole e minuscole, posizionare `@` prima del testo di ricerca, (ad esempio `@man*`).

Nella tabella seguente sono riportati alcuni esempi per spiegare come è possibile utilizzare la funzionalità di ricerca.

|Criteri di ricerca|Trova…|
|---------------|----------|
|`man`<br />oppure <br />`Man`|Tutti i record con campi che contengono il testo **man**, indipendentemente dall'uso di maiuscole/minuscole. Ad esempio, **Manchester**, **manual** o **Sportsman**. |
|`'Man'`|Tutti i record con campi che contengono solo il testo **Man**, che corrisponde all'uso di maiuscole/minuscole.|
|`Man*`|Tutti i record con campi che iniziano con il testo <b>man</b>, corrispondenti all'uso di maiuscole/minuscole. Ad esempio, **Manchester**, ma non **manual** o **Sportsman**.|
|`@Man*`|Tutti i record con campi che iniziano con il testo **man**, indipendentemente dall'uso di maiuscole/minuscole. Ad esempio, **Manchester** e **manual**, ma non **Sportsman**.|
|`@*man`|Tutti i record con campi che finiscono con il testo **man**, indipendentemente dall'uso di maiuscole/minuscole. Ad esempio, **Sportsman**, ma non **Manchester** o **manual**.|


## <a name="filtering"></a>Filtro

I filtri forniscono un modo più avanzato e versatile per controllare quali record sono inclusi in un elenco in un report o in XMLport. Esistono due principali differenze tra la ricerca e il filtro, come descritto nella tabella seguente.

|| **Ricerca** | **Filtri** |
|--|----------|------------|
| **Campi applicabili** | Cerca in tutti i campi visibili nella pagina. | Filtra uno o più campi singolarmente, selezionando da qualsiasi campo sulla tabella, inclusi i campi che non sono visibili sulla pagina. |
| **Corrispondenza** | Visualizza i record con campi che corrispondono al testo di ricerca, indipendentemente dall'uso di maiuscole/minuscole. o dal posizionamento del testo nel campo. | Visualizza i record in cui il campo corrisponde esattamente al filtro, incluse maiuscole e minuscole, a meno che non vengano inseriti simboli di filtro speciali.

Il filtro consente di visualizzare record per account o clienti specifici, date, importi e altre informazioni specificando i criteri di filtro. Solo i record che soddisfano i criteri vengono visualizzati nell'elenco o inclusi in un report, processo batch o XMLport. Se si specificano i criteri per più campi, verranno visualizzati solo i record che soddisfano tutti i criteri.

Per gli elenchi, i filtri vengono visualizzati in un riquadro filtri visualizzato a sinistra dell'elenco quando viene attivato. Per report, processi batch e XMLport, i filtri sono visibili direttamente nella pagina di richiesta.

### Filtro con campi di tipo opzione

Per i campi "ordinari" che contengono dati, data di impostazione o dati aziendali, è possibile impostare filtri selezionando i dati e digitando valori di filtro e quindi utilizzare i simboli per definire criteri di filtro avanzati. Per ulteriori informazioni, vedere [Immissione dei criteri di filtro](ui-enter-criteria-filters.md#entering-filter-criteria).

Tuttavia, per i campi di tipo **Opzione**, è possibile soltanto impostare un filtro selezionando una o più opzioni da un elenco a discesa delle opzioni disponibili. Un esempio di campo di tipo opzione è il campo **Stato** nella pagina **Ordini vendita**.

> [!NOTE]
> Quando si selezionano più opzioni come valore di filtro, la relazione tra le opzioni viene definita come *O*. Ad esempio, se si selezionano le caselle di controllo **Aperto** e **Rilasciato** nel campo di filtro **Stato** della pagina **Ordini vendita**, significa che sono visualizzati gli ordini vendita aperti o rilasciati.

### Impostazione di filtri negli elenchi

Negli elenchi, i filtri vengono impostati utilizzando il riquadro filtri. Per visualizzare il riquadro filtri per un elenco, selezionare la freccia rivolta verso il basso accanto al nome della pagina, quindi selezionare l'azione **Mostra riquadro Filtri**. In alternativa, premi <kbd>MAIUSC</kbd>+<kbd>F3</kbd>.

Per visualizzare il riquadro filtri per una colonna in un elenco, selezionare la freccia rivolta verso il basso quindi selezionare l'azione **Filtro**. In alternativa, premi <kbd>MAIUSC</kbd>+<kbd>F3</kbd>. Il riquadro filtri si apre con la colonna selezionata visualizzata come campo di filtro nella sezione **Filtra elenco per**.

Il riquadro filtri visualizza i filtri correnti per un elenco e consente di impostare filtri personalizzati in uno o più campi scegliendo l'azione **+ Filtro**.

 Un riquadro dei filtri è diviso in tre sezioni: **Visualizzazioni**, **Filtra elenco per** e **Filtra totali per**:

- **Visualizzazioni**

  Alcuni elenchi includono la sezione **Visualizzazioni**. Le visualizzazioni sono variazioni dell'elenco che sono state preconfigurate con i filtri. È possibile definire e salvare tutte le visualizzazioni desiderate per elenco. Le visualizzazioni saranno disponibili su qualsiasi dispositivo a cui si accede. Per ulteriori informazioni, vedere [Salvare e personalizzare visualizzazioni elenco](ui-views.md).

- **Filtra elenco per**

  Questa sezione consente di aggiungere filtri in campi specifici per ridurre il numero di record visualizzati. Per aggiungere un filtro, scegliere l'azione **+ Filtro**. Quindi, digitare il nome del campo in base al quale filtrare l'elenco o selezionare un campo dall'elenco a discesa.

- **Filtra totali per**

  Alcuni elenchi che visualizzano campi calcolati, come importi e quantità, includeranno la sezione **Filtra totali per** in cui è possibile impostare varie dimensioni che influenzano i calcoli. Per aggiungere un filtro, scegliere l'azione **+ Filtro**. Quindi, digitare il nome del campo in base al quale filtrare l'elenco o selezionare un campo dall'elenco a discesa.

  > [!NOTE]
  > I filtri nella sezione **Filtra totali per** sono controllati da FlowFilter nella progettazione della pagina. Per informazioni tecniche, vedere [FlowFilter](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

È possibile impostare un filtro semplice direttamente in un elenco utilizzando il riquadro filtri, ovvero un filtro che visualizza solo i record con lo stesso valore della cella selezionata. Selezionare un cella nell'elenco, selezionare la freccia rivolta verso il basso quindi scegliere l'azione **Filtra in base a questo valore**. In alternativa, premi <kbd>Alt</kbd>+<kbd>F3</kbd>.

### Impostazione di filtri in report, processi batch e XMLport

Per report e XMLport, i filtri sono visibili direttamente nella pagina di richiesta. La pagina di richiesta visualizza gli ultimi filtri utilizzati in base alla selezione effettuata nel campo **Utilizza valori predefiniti da**. Per ulteriori informazioni, vedi [Usare le impostazioni salvate](ui-work-report.md#SavedSettings).

La sezione **Filtro** principale mostra i campi di filtro predefiniti utilizzati per delimitare i record da includere in report o XMLport. Per aggiungere un filtro, scegliere l'azione **+ Filtro**. Quindi, digitare il nome del campo in base al quale filtrare o selezionare un campo dall'elenco a discesa.

Nella sezione **Filtra totali per**, è possibile regolare varie dimensioni che influenzano i calcoli in report o XMLport. Per aggiungere un filtro, scegliere l'azione **+ Filtro**. Quindi, digitare il nome del campo in base al quale filtrare o selezionare un campo dall'elenco a discesa.

## Immissione di criteri di filtro

Nel riquadro filtri e in una pagina di richiesta, i criteri di filtro vengono immessi nella casella sotto il campo di filtro.

Il tipo di campo di filtro determina quali criteri è possibile immettere. Ad esempio, il filtro di un campo con valori fissi consente solo di scegliere da tali valori. Per ulteriori informazioni sui simboli speciali del filtro, vedere [Criteri e simboli di filtro](#FilterCriteria) e [Token di filtro](#FilterTokens).

Le colonne che hanno già dei filtri sono indicate dall'icona ![icona Filtro.](media/ui-search/filter-icon.png "Icona Filtro") nell'intestazione della colonna. Per rimuovere un filtro, fare clic sulla freccia rivolta verso il basso, quindi scegliere l'azione **Cancella filtro**.

> [!TIP]
> Accelerare la ricerca e l'analisi dei dati utilizzando combinazioni di tasti di scelta rapida da tastiera. Ad esempio, seleziona un campo, usa <kbd>MAIUSC</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd> per aggiungere quel campo al riquadro dei filtri, digita i criteri del filtro, usa <kbd>CTRL</kbd>+<kbd>INVIO</kbd> per tornare alle righe, seleziona un altro campo e usa <kbd>Alt</kbd>+<kbd>F3</kbd> per filtrare tale valore. Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).

### <a name="FilterCriteria"> </a>Criteri e operatori di filtro

Quando si impostano criteri in un filtro, è possibile immettere tutti i numeri e le lettere in genere utilizzati nel campo. È inoltre possibile utilizzare un set di simboli speciali come operatori per filtrare ulteriormente i risultati. Le sezioni seguenti descrivono questi simboli e come utilizzarli come operatori nei filtri.

> [!TIP]
> Per ulteriori informazioni su come filtrare date e orari, vedi [Lavorare con le date e gli orari del calendario ](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Potrebbero verificarsi situazioni in cui il valore in base al quale si desidera filtrare contiene un simbolo che è un operatore. Per ulteriori informazioni sulla gestione di queste situazioni, vedere [Filtrare in base a valori che contengono simboli](#symbols).
>
> - Se sono presenti più di 200 operatori in un singolo filtro, il sistema raggrupperà automaticamente alcune espressioni tra parentesi `()` ai fini del trattamento. Ciò non ha alcun effetto sul filtro o sui risultati.  

#### (..) Intervallo

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`1100..2100`|Numeri da 1100 a 2100|  
|`..2500`|Fino a 2500 compreso.|  
|`..12 31 00`|Le date fino al 31/12/00 incluso|  
|`P8..`|Informazioni sul periodo contabile 8 e successivi|  
|`..23`|Dalla data di inizio fino al 23-mese corrente-anno corrente ore 23:59:59|  
|`23..`|Dal 23-mese corrente-anno corrente ore 0:00:00 alla fine|  
|`22..23`|Dal 22-mese corrente-anno corrente ore 0:00:00 fino al 23-mese corrente-anno corrente ore 23:59:59| 

> [!TIP]
> Se stai utilizzando un tastierino numerico, il tasto separatore decimale potrebbe restituire un carattere diverso dal punto (.). Per impostare il punto, premi i tasti <kbd>Alt</kbd>+<kbd>Separatore decimale</kbd> sulla tastiera numerica. Quando vuoi tornare indietro, premi di nuovo <kbd>Alt</kbd>+<kbd>Separatore decimale</kbd>. Per ulteriori informazioni, vedi [Impostazione del separatore decimale usato dalle tastiere numeriche](ui-enter-data.md#decimal).

#### (&#124;) Oppure

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`1200|1300`|Numeri con 1200 o 1300|  

#### (<>) Diverso da  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`<>0`|Tutti i numeri tranne 0<br /><br /> SQL Server Option consente di combinare questo simbolo con un'espressione contenente caratteri jolly. <>A*, ad esempio, si riferisce a un testo diverso da qualunque testo che inizia con la lettera A.|  

#### (>) Maggiore di  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`>1200`|Numeri maggiori di 1200|  

#### (>=) Maggiore di o uguale a  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`>=1200`|Numeri maggiori o uguali a 1200|  

#### (<) Minore di  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`<1200`|Numeri minori di 1200|  

#### (<=) Minore di o uguale a  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`<=1200`|Numeri minori o uguali a 1200|  

#### (&) E  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`>200&<1200`|Numeri maggiori di 200 e minori di 1200.|  

#### ('') Una corrispondenza esatta di carattere  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`'man'`|Testo con corrispondenza esatta a **man** e con distinzione tra maiuscole e minuscole.|  
|`''`|Testo vuoto.|  

#### (@) Senza distinzione tra maiuscole e minuscole  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`@man*`|Testo che inizia con **man** e senza distinzione tra maiuscole e minuscole.|  

#### (*) Un numero indefinito di caratteri non noti

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`*Co*`|Testo contenente **Co** e con distinzione tra maiuscole e minuscole.|  
|`*Co`|Testo che termina con **Co** e con distinzione tra maiuscole e minuscole.|  
|`Co*`|Testo che inizia con **Co** e con distinzione tra maiuscole e minuscole.|  

#### (?) Un carattere non noto  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`Hans?n`|Testo come **Marco** o **Mario**|  

#### Espressioni di formato combinate  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Include qualsiasi record con il numero 5999 oppure con un numero compreso tra 8100 e 8490.|  
|`..1299|1400..`|Include record con un numero minore o uguale a 1299 oppure un numero uguale a 1400 o maggiore, vale a dire tutti i numeri tranne quelli compresi tra 1300 e 1399.|  
|`>50&<100`|Include record con numeri maggiori di 50 e minori di 100, vale a dire i numeri compresi tra 51 e 99.|  

### <a name="symbols"></a>Filtrare in base a valori che contengono simboli

Potrebbero verificarsi casi in cui i valori dei campi contengono uno dei seguenti simboli:

- &
- (
- )
- =
- &#124;

Se si desidera filtrare in base a uno qualsiasi di questi simboli, inserire l'espressione di filtro tra virgolette singole (`'<expression with symbol>'`). Ad esempio, se si desidera filtrare i record che iniziano con il testo *J & V*, l'espressione di filtro è `'J & V*'`.

Questo requisito non è necessario per altri simboli.

### <a name="FilterTokens"> </a>Token di filtro

Quando si immettono i criteri di filtro, è anche possibile digitare parole che hanno un significato speciale, chiamate token di filtro. Dopo aver immesso la parola token, la parola viene sostituita dal valore o dai valori che rappresenta. I token di filtro semplificano l'operazione di filtro riducendo la necessità di passare ad altre pagine per cercare i valori che si desidera aggiungere al filtro. Le tabelle seguenti descrivono alcuni dei token che è possibile immettere a questo scopo.

> [!TIP]
> Un'organizzazione potrebbe utilizzare token personalizzati. Per informazioni sul set completo di token disponibili o per aggiungere altri token personalizzati, contattare l'amministratore. Per informazioni tecniche vedere [Aggiunta di token di filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### (%me or %userid) Record assegnati all'utente

Utilizzare `%me` o `%userid` quando si filtrano i campi che contengono l'ID utente, quale il campo **Assegnato a ID utente**, per visualizzare tutti i record assegnati all'utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%me`<br />oppure<br />`%userid`|Record assegnati all'account utente. |  

#### (%mycustomers) clienti in Clienti personali

Utilizzare `%mycustomers` nel campo **Nessuno** cliente per visualizzare tutti i record per i clienti inclusi nell'elenco **Clienti personali** in Gestione ruolo utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%mycustomers`|Clienti in **Clienti personali** in Gestione ruolo utente. |  

#### (%myitems) Articoli in Articoli personali

Utilizzare `%myitems` nel campo **Nessuno** articolo per visualizzare tutti i record per gli articoli inclusi nell'elenco **Articoli personali** in Gestione ruolo utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%myitems`|Articoli in **Articoli personali** in Gestione ruolo utente. |  

#### (%myvendors) Fornitori in Fornitori personali

Utilizzare `%myvendors` nel campo **Nessuno** fornitori per visualizzare tutti i record per i fornitori inclusi nell'elenco **Fornitori personali** in Gestione ruolo utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%myvendors`|Fornitori in **Fornitori personali** in Gestione ruolo utente. |  

## Vedere anche

[Domande frequenti su ricerca e filtro](ui-search-filter-faq.yml)  
[Salvare e personalizzare le visualizzazioni elenco](ui-views.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
