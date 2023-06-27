---
title: Immissione di date e ore in Business Central
description: 'Ottenere informazioni su come immettere le date e le ore inclusi suggerimenti relativi alla produttività quali abbreviazioni, espressioni e intervalli.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dates, reporting, filter, calendar, shorthand, range'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="work-with-calendar-dates-and-times"></a>Utilizzare date e orari del calendario

Puoi inserire date e orari in diversi modi. [!INCLUDE[prod_short](includes/prod_long.md)] include potenti funzionalità per accelerare l'immissione dei dati o scrivere espressioni di calendario complesse. È possibile immettere date e orari nei campi in diversi punti dell'applicazione. Ad esempio, in un ordine di vendita, è possibile impostare la data di spedizione. Quando si filtrano gli elenchi o i dati dei report, è possibile immettere date e orari per contrassegnare solo i dati a cui si è interessati.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="check-your-region-and-language-settings"></a>Verificare le impostazioni di lingua e paese

La pagina **Impostazioni personali** specifica l'**Area geografica** e la **Lingua** che si sta utilizzando nell'applicazione. Queste impostazioni influenzano le modalità di immissione delle date e ore.

- L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati.

- Per gli schemi di date che coinvolgono le parole, la lingua delle parole utilizzate deve corrispondere all'impostazione della **Lingua**.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] utilizza il sistema di calendario gregoriano.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a>Immissione di date

In un campo Data, è possibile immettere una data utilizzando il formato standard per le impostazioni di un paese. Diverse regioni possono utilizzare separatori diversi tra i giorni, i mesi e gli anni. Ad esempio, alcune regioni utilizzano i trattini (gg-mm-aaaa) e altri usano le barre (gg/mm/aaaa).  

> [!TIP]
> Puoi utilizzare qualsiasi separatore, anche uno spazio, e la data verrà automaticamente modificata per utilizzare separatori che corrispondono all'area geografica.

> [!NOTE]
> Il formato in cui le date vengono visualizzate sui report stampati o sui documenti inviati via e-mail non è influenzato dalla scelta personale di impostazione dell'area geografica.

Per lavorare in modo più produttivo con date e orari, è possibile utilizzare uno dei metodi o formati descritti nelle sezioni seguenti.

### <a name="picking-dates-from-the-calendar"></a>Selezionare le date dal calendario

Qualsiasi campo che visualizza un'icona di calendario può essere impostato utilizzando il selettore di date del calendario. Per visualizzare il selettore di date del calendario, attiva l'icona del calendario o premi <kbd>Ctrl</kbd>+<kbd>Home</kbd> nel campo.

![Campi data.](media/ui-date-field.png "Esempio di un campo data")

Vedere anche [Tasti di scelta rapida nel calendario (selezione data)](keyboard-shortcuts.md#calendarshortcuts).

### <a name="day-week-year-pattern"></a>Schema giorno\-settimana\-anno

È possibile immettere una data come giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno. Ad esempio, Lun25 o lun25 indica il lunedì della settimana 25. Se non immetti un anno, viene utilizzato l'anno della data di lavoro.

Anziché immettere l'intera parola per il giorno della settimana, è possibile immettere una parte della parola, a partire dall'inizio. In caso di conflitti (come in italiano m che potrebbe essere Martedì o Mercoledì), i giorni vengono valutati in base all'impostazione dell'area geografica. L'input viene prima valutato rispetto alla data di lavoro e alla data odierna, ricorda questa informazione quando usi le abbreviazioni. Ad esempio, in italiano, _s_ indica settimana pertanto non può significare Sabato.

Lo schema del numero della settimana è sempre ISO 8601, dove la settimana 1 è la settimana che include il 4 gennaio o la settimana con il primo giovedì dell'anno.

### <a name="digit-patterns"></a>Schemi con cifre

In un campo di data è possibile immettere due, quattro, sei o otto cifre:

- Se immetti solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.

- Se immetti quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro. L'ordine giorno e il mese è determinato dalle impostazioni di un paese. Anche se le impostazioni del paese hanno l'anno prima del giorno e del mese, le quattro cifre vengono interpretate come giorno e mese.

- Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1950 e 31/12/2049, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.

  > [!NOTE]
  > Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] in locale, l'intervallo di anni a due cifre potrebbe essere diverso. Gli amministratori possono modificare l'intervallo modificando l'impostazione **CalendarTwoDigitYearMax** del server [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Configurazione di Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).
 
### <a name="today"></a>Oggi

Inserisci la parola per _oggi_, nella lingua specificata nella pagina **Impostazioni personali** per impostare la data di un record sulla data odierna. Anziché immettere l'intera parola, è possibile immettere una parte della parola. Ad esempio, in inglese, puoi inserire _t_ o _tod_, purché non sia anche l'inizio di un'altra parola.

### <a name="period"></a>Periodo

Per filtrare uno specifico periodo contabile, in un campo Data immettere la lettera p o la parola periodo, seguita da un numero che identifica il periodo contabile, ad esempio p2 o periodo4. Il periodo contabile è relativo all'anno fiscale della data di lavoro corrente impostata nella Gestione ruolo utente. Ad esempio, se la data di lavoro è **21/03/22**, _p1_ oppure soltanto _p_, filtra il primo periodo contabile dell'anno fiscale 2022 (come 01/01/22..31/01/22). _p15_ filtra il quindicesimo periodo contabile dall'inizio dell'anno fiscale 2022 (come 01/03/23..31/03/23).

I periodi contabili sono definiti nella pagina **Periodi contabili**. Per visualizzare o modificare i periodi contabili, aprire la pagina [qui](https://businesscentral.dynamics.com/?page=100).

### <a name="work-date"></a>Data del lavoro

Utilizza una data di lavoro per specificare una data che non è la data odierna sui record. Ad esempio, una data di lavoro è utile quando è necessario impostare una data particolare per più record. Specifica la data di lavoro nella pagina **Impostazioni personali**. 

Un modo rapido per inserire la data di lavoro sui record è inserire alcune o tutte le parole _lavoro_, partendo dall'inizio della parola, nella lingua in cui stai usando [!INCLUDE[prod_short](includes/prod_long.md)]. Ad esempio, in italiano, puoi inserire _l_ o _lavoro_. La lingua è anche specificata nella pagina **Impostazioni personali**.

Se non hai specificato una data di lavoro, verrà utilizzata la data odierna. Per ulteriori informazioni vedi [Modificare le impostazioni di base, quali l'ora di lavoro](ui-change-basic-settings.md#work-date).

### <a name="closing-date"></a>Data chiusura

Per chiudere un anno fiscale, è possibile utilizzare date di chiusura per indicare un movimento di chiusura. Una data di chiusura è tecnicamente compresa tra due date, ad esempio 31 dicembre e 1 gennaio.

Per specificare che si tratta di una data di chiusura, immettere C prima della data, ad esempio C123101. Questo formato può essere utilizzato insieme a tutti i modelli per data.

### <a name="examples"></a>Esempi

Nella tabella seguente sono contenuti esempi di date utilizzando tutti i formati. Presuppone le impostazioni di paese con formato di data **anno.mese.giorno.**, una settimana che inizia il lunedì e la lingua inglese.

|**Immissione**      |**Interpretazione**      |
|---------------|------------------------|
|2022.12.31.|2022.12.31.|
|221231|2022.12.31.|
|22.12.31.|2022.12.31.|
|22.12.31.|2022.12.31.|
|20221231|2022.12.31.|
|22/12,31|2022.12.31.|
|11|anno data di lavoro.mese data di lavoro.11.|
|1112|anno data di lavoro.11.12.|
|o oppure oggi|data odierna|
|p4|intervallo di date che include il quarto periodo contabile, ad esempio 01/04/20..30/04/20|
|l o data di lavoro|la data di lavoro|
|lu o lunedì|Lunedì della settimana della data di lavoro|
|ma o martedì|Martedì della settimana della data di lavoro|
|sa o Sabato|Sabato della settimana della data di lavoro|
|d o Domenica|Domenica della settimana della data di lavoro|
|m23|Martedì della settimana 23 dell'anno della data di lavoro|
|m 23|Martedì della settimana 23 dell'anno della data di lavoro|
|m-1|Martedì della settimana 1 dell'anno della data di lavoro|

## <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> Impostazione di intervalli di date

In elenchi, totali e report, è possibile impostare filtri su date, orari e periodi di tempo contenenti un valore iniziale e facoltativamente un valore finale per visualizzare solo i dati contenuti in tale intervallo. All'impostazione di intervalli di date si applicano regole standard.

|**significato**|**Espressione di esempio (data)**|**Dati inclusi nel filtro**|
|-----------|---------------------|--------------------|
|intervallo|15 12 00..01 15 01<br /><br />..15 12 00<br /><br />p1..p4|Record la cui data di risposta è compresa tra il 15 12 00 e il 15 01 01 inclusi.<br /><br />Record con data 15 12 00 o precedente.<br /><br />Intervallo di date che include il secondo, il terzo e il quarto periodo contabile, ad esempio 01/01/20..30/04/20..|
|oppure|15 12 00\|16 12 00|Record con data 15 12 00 o 16 12 00. Se ci sono record con date in entrambi i giorni, saranno tutti visualizzati.|
|Combinazione|15 12 00\|01 12 00..10 12 00  <br /><br />..14 12 00\|30 12 00..|Record con data 15 12 00 o in date tra l'01 12 00 e il 10 12 00 compresi.  <br /><br />Record la cui data è il 12 14 00 o una data precedente oppure il 12 30 00 o una data successiva, ossia tutti i record esclusi quelli la cui data di risposta è compresa tra il 12 15 00 e il 12 29 00 inclusi.|

È possibile utilizzare uno qualsiasi dei formati validi nei filtri dell'intervallo di date. Ad esempio, lun14 3..o 4p applicato a un campo data/ora risulta un filtro dalle 3 AM di lunedì nella settimana 14 dell'anno della data di lavoro corrente, incluso, fino alle 4 PM, comprese.

## <a name="use-date-formulas"></a>Usare le formule data

Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date. È possibile immettere formule per le date in diversi campi o filtri per il calcolo della data.

> [!NOTE]
> In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo. Di conseguenza, se si immette, ad esempio, 1S, il periodo è effettivamente di otto giorni perché la data odierna è inclusa. Per specificare un periodo di sette giorni \(una settimana\) includendo la data di inizio del periodo, è necessario immettere 6G o 1S-1G.

Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:

- La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.

- La formula nel campo **Periodo di dilazione** per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza \(o dalla data del sollecito precedente\) alla creazione del sollecito.

- La formula nel campo **Calcolo data di scadenza** determina la modalità di calcolo della data di scadenza nel sollecito.

La formula per la data può contenere un massimo di 20 caratteri, sia numeri che lettere. È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di calendario.

|  Lettera  |  Significato  |
|----------|----------------------|
|C|Corrente|
|G|Giorno\(i\)|
|S|Settimana\(e\)|
|M|Mese\(i\)|
|T|Trimestre\(i\)|
|A|Anno\(i\)|

È possibile creare una formula per la data in tre modi diversi.

L'esempio seguente mostra come usare C, vale a dire corrente, e un'unità di tempo.

|  Espressione  |  Significato  |
|--------------|-----------|
|SC|Settimana corrente|
|MC|Mese corrente|

L'esempio seguente mostra come usare un numero e un'unità di tempo. Il numero non può essere maggiore di 9999.

|  Espressione  |  Significato  |
|--------------|-----------|
|10D|10 giorni a partire da oggi|
|2S|2 settimane a partire da oggi|

L'esempio seguente mostra come usare un'unità di tempo e un numero.

|  Espressione  |  Significato  |
|--------------|-----------|
|G10|Il successivo giorno 10 del mese|
|GS4|Il successivo quarto giorno della settimana \(Giovedì\)|

Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.

|  Espressione  |  Significato  |
|--------------|-----------|
|MC+10G|Mese corrente \+ 10 giorni|

Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.

|  Espressione  |  Significato  |
|--------------|-----------|
|-1A|1 anno fa da oggi|

> [!IMPORTANT]
> Se l'ubicazione utilizza un calendario di base, la formula per la data immessa, ad esempio, nel campo **Durata spedizione** verrà interpretata in base ai giorni lavorativi del calendario. Ad esempio la formula 1S significa sette giorni lavorativi.
<!--
# <a name="entering-date-ranges"></a>Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list.](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## <a name="use-date-formulas-1"></a>Use Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
> In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

- The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

- The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

- The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
> If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a>Immissione di ore

Quando immetti l'ora, puoi inserire qualsiasi separatore diverso da spazio tra le unità. Se usi due cifre per ogni unità fino a millisecondi, non è necessario.

È necessario immettere solo le unità di grandi dimensioni di richiedere; il resto sarà uguale a zero. È inoltre possibile omettere qualsiasi di contrassegno con l'indicazione AM/PM.

Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti. Presuppone le impostazioni del paese che formattano le ore in base a **Ore:Minuti:Secondi.Millisecondi.** e utilizzano gli indicatori AM e PM per "AM" e"PM" rispettivamente.

|**Immissione**      |**Interpretazione**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05.00.00|
|5AM|05.00.00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05.30.00|
|0530|05.30.00|
|5:30:5|05.30.05|
|053005|05.30.05|
|5:30:5.50|05:30:05,5|
|053005050|05.30.05,05|

> [!NOTE]
> I millisecondi vengono interpretati come notazione decimale. Così, ad esempio, 3, 30 e 300 significano tutti 300 millisecondi, mentre 03 significa 30 e 003 significa 3 millisecondi.

> [!IMPORTANT]
> Non è possibile utilizzare 24:00 per indicare la mezzanotte oppure utilizzare qualsiasi valore superiore a 24:00.

La parola per "ora" nella lingua usata da [!INCLUDE[prod_short](includes/prod_long.md)] verrà valutata per l'ora corrente del computer o dispositivo mobile in uso. È possibile immettere qualsiasi parte della parola, a partire dall'inizio, come o oppure ORA.

## <a name="entering-combined-dates-and-times"></a>Immissione di date e ore combinate

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration"></a>Immissione della durata

Alcuni campi dell'applicazione rappresentano una durata, o una quantità di tempo trascorso, anziché una data o un'ora specifica. È possibile immettere una durata in caratteri numerici seguiti dalla relativa unità di misura.

Di seguito vengono forniti alcuni esempi.

|**Durata**|**Unità di misura**|
|------------|-------------------|
|2h|2 ore|
|6h 30 m|6 ore 30 minuti|
|6.5h|6 ore 30 minuti|
|90m|1 ora 30 minuti|
|2d 6h 30m|2 giorni 6 ore 30 minuti|
|2d 6h 30m 56s 600ms|2 giorni 6 ore 30 minuti 56 secondi 600 millisecondi|

È inoltre possibile immettere un numero che verrà automaticamente convertito in una durata. Il numero immesso viene convertito in base all'unità di misura predefinita specificata nel campo relativo alla durata.

Per vedere quale unità di misura viene utilizzata in un campo di durata, immetti un numero. Quindi, puoi vedere in quale unità di misura è stato convertito.

Ad esempio, il numero 5 viene convertito in 5 h se l'unità di misura è l'ora.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/explore-modify-info-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Utilizzare [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)  
[Immissione di criteri di filtro](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
