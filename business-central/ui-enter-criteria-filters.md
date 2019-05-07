---
title: Ricerca, filtro e ordinamento di elenchi | Documenti Microsoft
description: Utilizzare in modo efficiente gli elenchi cercando nei dati, ordinando colonne e perfezionando i risultati con potenti simboli di filtro e tasti di scelta rapida da tastiera.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 5cd8bce29b1973274cda673e22dd07e6b50f830f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "928071"
---
# <a name="sorting-searching-and-filtering-lists"></a>Ricerca, filtro e ordinamento di elenchi
La ricerca e l'individuazione di record in un elenco risultano più semplici grazie a l'ordinamento, la ricerca e il filtro. di ordinamento, ricerca e filtro. È possibile collegare alcune o tutte le procedure contemporaneamente a rapidamente per trovare o analizzare rapidamente i dati.

> [!TIP]
> Quando si visualizzano i dati come riquadri, è possibile cercare e utilizzare il filtro di base. Per utilizzare il set completo di potenti funzionalità per l'ordinamento, la ricerca e il filtro, scegliere l'icona ![Mostra come lista](media/ui_show_as_list_icon.png "Icona Mostra come lista") per visualizzare in forma di elenco.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Ordinamento
L'ordinamento consente di ottenere in modo semplice e rapido una panoramica dei dati. Se si dispone di molti clienti, ad esempio, è possibile scegliere di ordinarli in base a **Nr. cliente**, **Cat. reg. cliente**, **Codice valuta**, **Codice paese** o **Identificativo fiscale** per ottenere la panoramica desiderata.

Per ordinare un elenco, fare clic sull'intestazione di una colonna per passare dall'ordine crescente a quello decrescente e viceversa, oppure scegliere la piccola freccia verso il basso nell'intestazione della colonna e scegliere **Crescente** o **Decrescente**.  

> [!NOTE]  
>   L'ordinamento non è supportato nelle immagini, nei campi BLOB, in FlowFilter e nei campi che non appartengono a una tabella.  

## <a name="searching"></a>Ricerca
<!--## Searching by using the Quick Filter -->
Nella parte superiore di ogni pagina elenco, c'è un'icona ![Icona di ricerca](media/ui-search/search-list.png "Icona di ricerca") **Cerca** che fornisce un modo rapido e semplice per ridurre i record in un elenco e visualizzare solo quei record che contengono i dati che interessa vedere.

Per cercare, è sufficiente selezionare l'icona di ricerca, quindi nella casella digitare il testo che si sta cercando. È possibile immettere lettere, numeri e altri simboli.

### <a name="fine-tune-the-search"></a>Perfezionare la ricerca
In generale, la ricerca tenterà di far corrispondere il testo in tutti i campi, non distingue tra caratteri maiuscoli e minuscoli (in altre parole, maiuscole e minuscole) e corrisponderà al testo inserito nel campo (all'inizio, alla fine o al centro).

Tuttavia, è possibile effettuare una ricerca più precisa utilizzando i seguenti caratteri speciali:

- Per trovare solo i valori dei campi che corrispondono esattamente all'intero testo e al caso, posizionare il testo di ricerca tra virgolette singole `''` (ad esempio `'man'`).

- Per trovare valori di campo che iniziano con un determinato testo e corrispondono al caso, posizionare `*` dopo il testo di ricerca (ad esempio `man*`).

- Per trovare valori di campo che terminano con un determinato testo e corrispondono al caso, posizionare `*` prima del testo di ricerca (ad esempio `*man`).

- Quando si utilizza `''` o `*`, la ricerca è sensibile alla distinzione maiuscola/minuscola. Se si desidera ignorare la distinzione tra maiuscole e minuscole, posizionare `@` prima del testo di ricerca, (ad esempio `@man*`).

Nella tabella seguente sono riportati alcuni esempi per spiegare come è possibile utilizzare la funzionalità di ricerca.

|Criteri di ricerca|Trova…|
|---------------|----------|
|`man`<br />oppure <br />`Man`|Tutti i record con campi che contengono il testo **man**, indipendentemente dal caso. Ad esempio, **Manchester**, **manual** o **Sportsman**. |
|`'Man'`|Tutti i record con campi che contengono solo il testo **Man**, che corrisponde al caso.|
|`Man*`|Tutti i record con campi che iniziano con il testo <b>man</b>, con corrispondenza al caso. Ad esempio, **Manchester**, ma non **manual** o **Sportsman**.|
|`@Man*`|Tutti i record con campi che iniziano con il testo **man**, indipendentemente dal caso. Ad esempio, **Manchester** e **manual**, ma non **Sportsman**.|
|`@*man`|Tutti i record con campi che finiscono con il testo **man**, indipendentemente dal caso. Ad esempio, **Sportsman**, ma non **Manchester** o **manual**.|

> [!TIP]
> È possibile premere F3 per attivare e disattivare la casella di ricerca. Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).

## <a name="Filtering"> </a>Filtri
l filtraggio fornisce un modo più avanzato e versatile per controllare quali record vengono visualizzati in un elenco. Esistono due principali differenze tra la ricerca e il filtro, come descritto nella tabella seguente.

|| **Ricerca** | **Filtri** |
|--|----------|------------|
| **Campi applicabili** | Cerca in tutti i campi visibili nella pagina. | Filtra uno o più campi singolarmente, selezionando da qualsiasi campo sulla tabella, inclusi i campi che non sono visibili sulla pagina. |
| **Corrispondenza** | Visualizza i record con campi che corrispondono al testo di ricerca, indipendentemente dal caso o dal posizionamento del testo. | Visualizza i record in cui il campo corrisponde esattamente al filtro e fa distinzione tra maiuscole e minuscole, a meno che non vengano inseriti simboli di filtro speciali.

Il filtro consente di visualizzare record per account o clienti specifici, date, importi e altre informazioni specificando i criteri di filtro. Solo i record che rispondono a tali criteri vengono visualizzati. Se si specificano i criteri per più campi, verranno visualizzati solo i record che soddisfano tutti i criteri.

### <a name="working-in-the-filter-pane"></a>Utilizzo del riquadro Filtri

Per visualizzare il riquadro Filtri, selezionare ![icona riquadro Filtri](media/open-filter-pane-icon.png "Icona riquadro Filtri") nella parte superiore dell'elenco o premere **MAIUSC+F3**. Per gli elenchi all'interno di Gestione ruolo utente, è possibile anche scegliere la freccia verso il basso accanto al titolo della pagina nella barra di spostamento sopra l'elenco, quindi scegliere **Mostra riquadro Filtri**come mostrato di seguito:

![Mostra riquadro Filtri](media/open-filter-pane.png "Mostra riquadro Filtri")

Il riquadro dei filtri visualizza i filtri correnti per un elenco e consente di impostare i propri filtri personalizzati su uno o più campi. La figura seguente mostra un riquadro dei filtri di esempio per un elenco di offerte di vendita.

![Panoramica del riquadro Filtro ](media/filter-pane-overview.png "Icona Filtro")

Un riquadro dei filtri è diviso in tre sezioni: **Visualizzazioni**, **Filtra elenco per** e **Filtra totali per**:

- **Visualizzazioni**

  Alcuni elenchi includono la sezione **Visualizzazioni**. Le visualizzazioni sono variazioni dell'elenco che sono state preconfigurate con i filtri. Per passare a una diversa visualizzazione del tuo elenco, selezionare semplicemente un altro collegamento. È possibile modificare temporaneamente i filtri su una visualizzazione, ma le modifiche non verranno salvate in modo permanente.

- **Filtra elenco per**

  La sezione **Filtra elenco per:** consente di aggiungere filtri in campi specifici per ridurre il numero di record visualizzati. Per aggiungere un filtro, selezionare **+ Filtro** , selezionare il campo che si desidera filtrare da qualsiasi campo nella tabella, quindi inserire i criteri di filtro nella casella.

- **Filtra totali per**

  Alcuni elenchi che visualizzano campi calcolati, come importi e quantità, includeranno la sezione **Filtra totali per** in cui è possibile impostare varie dimensioni che influenzano i calcoli. Ad esempio, è possibile analizzare rapidamente il piano dei conti filtrando gli importi in un periodo specifico oppure è possibile visualizzare i totali per gli ordini di vendita solo da un determinato magazzino.

  Per aggiungere un filtro, selezionare **+ Filtro**, selezionare una delle dimensioni predefinite e quindi aggiungere i criteri di filtro nella casella.

  > [!NOTE]
  > I filtri nella sezione **Filtra totali per** sono controllati da FlowFilter nella progettazione della pagina. Per informazioni tecniche, vedere [FlowFilter](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Immissione dei criteri di filtro nel riquadro Filtri
Per selezionare un campo da filtrare, effettuare una delle seguenti operazioni:
  - Nel riquadro dei filtri, scegliere **+ Campo**. Digitare il nome del campo che si desidera filtrare o selezionare un campo dal menu che visualizza tutti i campi nella tabella.

  - In una colonna, scegliere la freccia verso il basso, quindi selezionare **Filtra...**. Questo aprirà il riquadro dei filtri e aggiungerà la colonna al riquadro dei filtri.

A questo punto è possibile immettere o selezionare i criteri di filtro nella casella. Il tipo di campo filtrato determina i criteri che si possono inserire. Ad esempio, il filtro di un campo con valori fissi consente solo di scegliere da tali valori. Per ulteriori informazioni sui simboli speciali del filtro, vedere [Criteri e simboli di filtro](#FilterCriteria) e [Token di filtro](#FilterTokens).

Le colonne che hanno già dei filtri sono indicate dall'intestazione dall'![icona Filtro](media/ui-search/filter-icon.png "icona Filtro") nell'intestazione della colonna. Per rimuovere un filtro, selezionare l'intestazione della colonna, quindi **Cancella filtro**.


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a>Immissione dei criteri di filtro senza il riquadro Filtri
È possibile specificare semplici filtri direttamente all'interno dell'elenco senza dover utilizzare il riquadro dei filtri.
Con qualsiasi campo selezionato su una riga, usa **ALT+F3** per visualizzare solo i record che hanno lo stesso valore. È quindi possibile selezionare un altro campo e utilizzare di nuovo gli stessi tasti di scelta rapida per continuare a perfezionare i filtri. Se il campo selezionato è già filtrato, **ALT + F3** cancellerà quel filtro.

> [!TIP]
> Accelerare la ricerca e l'analisi dei dati utilizzando combinazioni di tasti di scelta rapida da tastiera. Ad esempio, selezionare un campo, usare **MAIUSC + ALT + F3** per aggiungere quel campo al riquadro dei filtri, digitare i criteri del filtro, usare **CTRL + INVIO** per tornare alle righe, selezionare un altro campo e usare **ALT + F3** per filtrare tale valore.
Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Criteri e simboli di filtro
Quando si impostano criteri in un filtro, è possibile immettere tutti i numeri e le lettere in genere consentiti nel campo. È inoltre possibile utilizzare alcuni simboli speciali per filtrare ulteriormente i risultati. Nella tabella seguente sono inclusi i simboli che è possibile utilizzare nei filtri. Per date e ore, è anche possibile fare riferimento a [Utilizzo di date e orari del calendario](ui-enter-date-ranges.md) per informazioni più dettagliate.

> [!IMPORTANT]  
>  In alcuni casi è possibile che alcuni valori campo contengano tali simboli e che si intenda filtrarli. Per farlo, è necessario includere l'espressione di filtro contenente il simbolo tra virgolette ("). Ad esempio, se si desidera filtrare i record che iniziano con il testo *S&R*, l'espressione di filtro è `'S&R*'`.  

### <a name="-interval"></a>(..) Intervallo

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`1100..2100`|Numeri da 1100 a 2100|  
|`..2500`|Fino a 2500 compreso.|  
|`..12 31 00`|Le date fino al 31/12/00 incluso|  
|`P8..`|Informazioni sul periodo contabile 8 e successivi|  
|`..23`|Dalla data di inizio fino al 23-mese corrente-anno corrente ore 23:59:59|  
|`23..`|Dal 23-mese corrente-anno corrente ore 0:00:00 alla fine|  
|`22..23`|Dal 22-mese corrente-anno corrente ore 0:00:00 fino al 23-mese corrente-anno corrente ore 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Oppure  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`1200|1300`|Numeri con 1200 o 1300|  

### <a name="-not-equal-to"></a>(<>) Diverso da  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`<>0`|Tutti i numeri tranne 0<br /><br /> SQL Server Option consente di combinare questo simbolo con un'espressione contenente caratteri jolly. <>A*, ad esempio, si riferisce a un testo diverso da qualunque testo che inizia con la lettera A.|  

### <a name="-greater-than"></a>(>) Maggiore di  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`>1200`|Numeri maggiori di 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Maggiore di o uguale a  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`>=1200`|Numeri maggiori o uguali a 1200|  

### <a name="-less-than"></a>(<) Minore di  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`<1200`|Numeri minori di 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Minore di o uguale a  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`<=1200`|Numeri minori o uguali a 1200|  

### <a name="-and"></a>(&) E  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`>200&<1200`|Numeri maggiori di 200 e minori di 1200.|  

### <a name="-an-exact-character-match"></a>('') Una corrispondenza esatta di carattere  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`'man'`|Testo con corrispondenza esatta a man e con distinzione tra maiuscole e minuscole.|  

### <a name="-case-insensitive"></a>(@) Senza distinzione tra maiuscole e minuscole  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`@man*`|Testo che inizia con man e senza distinzione tra maiuscole e minuscole.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Un numero indefinito di caratteri non noti

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`*Co*`|Testo contenente "Co" per il quale viene osservata la distinzione tra maiuscole e minuscole.|  
|`*Co`|Testo che termina con "Co" e per il quale viene osservata la distinzione tra maiuscole e minuscole.|  
|`Co*`|Testo che inizia con "Co" e per il quale viene osservata la distinzione tra maiuscole e minuscole.|  

> [!NOTE]  
>   Non è possibile utilizzare `*` per filtrare i campi di opzione (enumerazione), ad esempio il campo **Stato** negli ordini di vendita. Per immettere un filtro per il tipo di campo, è possibile immettere il valore numerico come parametro di filtro. Ad esempio, nel campo **Stato** in un ordine di vendita con i valori **Aperto**, **Rilasciato**, **In attesa di approvazione** e **Pagamento anticipato in sospeso,** utilizzare i valori `0`, `1`, `2` e `3` per filtrare in base a queste opzioni.

### <a name="-one-unknown-character"></a>(?) Un carattere non noto  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`Hans?n`|Testo come Marco o Mario|  

### <a name="combined-format-expressions"></a>Espressioni di formato combinate  

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Include qualsiasi record con il numero 5999 oppure con un numero compreso tra 8100 e 8490.|  
|`..1299|1400..`|Include record con un numero minore o uguale a 1299 oppure un numero uguale a 1400 o maggiore, vale a dire tutti i numeri tranne quelli compresi tra 1300 e 1399.|  
|`>50&<100`|Include record con numeri maggiori di 50 e minori di 100, vale a dire i numeri compresi tra 51 e 99.|  


## <a name="FilterTokens"> </a>Token di filtro
Quando si immettono i criteri di filtro, è anche possibile digitare parole che hanno un significato speciale, chiamate token di filtro. Dopo aver immesso la parola token, la parola viene sostituita dal valore o dai valori che rappresenta. Ciò semplifica il filtro riducendo la necessità di passare ad altre pagine per cercare i valori che si desidera aggiungere al filtro. Le tabelle seguenti descrivono alcuni dei token che è possibile immettere a questo scopo.

> [!TIP]
> Un'organizzazione potrebbe utilizzare token personalizzati. Per informazioni sul set completo di token disponibili o per aggiungere altri token personalizzati, contattare l'amministratore. Per informazioni tecniche vedere [Aggiunta di token di filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).


### <a name="me-or-userid-records-assigned-to-you"></a>(%me or %userid) Record assegnati all'utente

Utilizzare `%me` o `%userid` quando si filtrano i campi che contengono l'ID utente, quale il campo **Assegnato a ID utente**, per visualizzare tutti i record assegnati all'utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%me`<br />oppure<br />`%userid`|Record assegnati all'account utente. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) clienti in Clienti personali

Utilizzare `%mycustomers` nel campo **Nessuno** cliente per visualizzare tutti i record per i clienti inclusi nell'elenco **Clienti personali** in Gestione ruolo utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%mycustomers`|Clienti in **Clienti personali** in Gestione ruolo utente. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Articoli in Articoli personali

Utilizzare `%myitems` nel campo **Nessuno** articolo per visualizzare tutti i record per gli articoli inclusi nell'elenco **Articoli personali** in Gestione ruolo utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%myitems`|Articoli in **Articoli personali** in Gestione ruolo utente. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Fornitori in Fornitori personali

Utilizzare `%myvendors` nel campo **Nessuno** fornitori per visualizzare tutti i record per i fornitori inclusi nell'elenco **Fornitori personali** in Gestione ruolo utente.

|espressione di esempio|Record visualizzati|  
|-----------------------|-----------------------|  
|`%myvendors`|Fornitori in **Fornitori personali** in Gestione ruolo utente. |  


## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Domande comuni su ricerca e filtro](ui-search-filter-faq.md)
