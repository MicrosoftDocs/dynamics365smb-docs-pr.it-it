---
title: Immissione di date e ore in Business Central | Documenti Microsoft
description: "Ottenere informazioni su come immettere le date e le ore inclusi suggerimenti relativi alla produttività quali abbreviazioni, espressioni e intervalli. Filtrare elenchi o report per una data o periodo specifici."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8717d60a8449ca300eaf9c1a5c4b137ea1a1a247
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---

# <a name="working-with-calendar-dates-and-times"></a>Utilizzo di date e orari del calendario
[!INCLUDE[d365fin](includes/d365fin_long_md.md)] offre diversi modi per immettere date e orari, incluse potenti funzionalità per accelerare l'immissione dei dati o scrivere espressioni di calendario complesse. È possibile immettere date e orari nei campi in diversi punti dell'applicazione. Ad esempio, in un ordine di vendita, è possibile impostare la data di spedizione. Quando si filtrano gli elenchi o i dati dei report, è possibile immettere date e orari per contrassegnare solo i dati a cui si è interessati.

## <a name="check-your-region-and-language-settings"></a>Verificare le impostazioni di lingua e paese
La pagina [**Impostazioni personali**](https://businesscentral.dynamics.com?page=9176 "Vai direttamente alla pagina delle impostazioni personali in Business Central") consente di specificare la **Regione** e la **Lingua** che si utilizzano nell'applicazione. Queste impostazioni influenzano le modalità di immissione delle date e ore. 

-   L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati.

-   Per gli schemi di date che coinvolgono le parole, la lingua delle parole utilizzate deve corrispondere all'impostazione della **Lingua**.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] utilizza il sistema di calendario gregoriano.

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->
## <a name="entering-dates"></a>Immissione di date
In un campo Data, è possibile immettere una data utilizzando il formato standard per le impostazioni di un paese. Diverse regioni possono utilizzare separatori diversi tra i giorni, i mesi e gli anni. Ad esempio, alcune regioni utilizzano i trattini (gg-mm-aaaa) e altri usano le barre (gg/mm/aaaa). Tuttavia, è possibile utilizzare qualsiasi separatore, anche uno spazio, e la data verrà automaticamente modificata per utilizzare separatori che corrispondono alla regione.

Si noti che il formato in cui le date vengono visualizzate sui report stampati o sui documenti inviati via e-mail non è influenzato dalla scelta personale di impostazione della regione.

Per lavorare in modo più produttivo con date e orari, è possibile utilizzare uno dei metodi o formati descritti nelle sezioni seguenti. 

### <a name="picking-dates-from-the-calendar"></a>Selezionare le date dal calendario
Qualsiasi campo che visualizza un'icona di calendario può essere impostato utilizzando il selettore di date del calendario. Per visualizzare il selettore di date del calendario, attivare l'icona del calendario o premere CTRL+tasto HOME nel campo.

![Campi Data](media/ui-date-field.png "Esempio di un campo data")

Vedere anche [Tasti di scelta rapida nel calendario (selezione data)](keyboard-shortcuts.md#calendarshortcuts)

### <a name="today"></a>Oggi
Immettere la parola corrispondente a `today`nella lingua impostata in **Lingua**, questo imposterà la data e sulla data corrente. Anziché immettere la parola intera, è possibile immettere una parte della parola, a partire dall'inizio, ad esempio `t` o `tod`, purché non sia anche l'inizio di un'altra parola.

### <a name="day-week-year-pattern"></a>Schema giorno\-settimana\-anno
È possibile immettere una data come giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno. Ad esempio, `Mon25` o `mon25` indica il lunedì della settimana 25. Se non si immette un anno, viene utilizzato l'anno della data di lavoro.

Anziché immettere l'intera parola per il giorno della settimana, è possibile immettere una parte della parola, a partire dall'inizio. Nel caso dei conflitti (come in inglese `s` che potrebbe essere Saturday o Sunday), i giorni vengono valutati in base all'impostazione di un paese. L'input viene prima valutato rispetto a `workdate` e `today`, ricordare questa informazione quando si utilizzano abbreviazioni. Ad esempio, in inglese, `t` indica già oggi (today) pertanto non può significare Tuesday o Thursday.

Lo schema del numero della settimana è sempre ISO 8601, dove la settimana 1 è la settimana che include il 4 gennaio o la settimana con il primo giovedì dell'anno.

### <a name="digit-patterns"></a>Schemi con cifre
In un campo di data è possibile immettere due, quattro, sei o otto cifre:

-   Se si immettono solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.

-   Se si immettono quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro. L'ordine giorno e il mese è determinato dalle impostazioni di un paese. Anche se le impostazioni del paese hanno l'anno prima del giorno e del mese, le quattro cifre vengono interpretate come giorno e mese.

-   Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1930 e 31/12/2029, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.

### <a name="current-work-date"></a>Data di lavoro corrente
La funzionalità della data di lavoro consente di registrare le transizioni utilizzando una data diversa dalla data corrente.

La parola "workdate", nella lingua impostata in **Lingua** imposterà la data sulla data di lavoro attualmente impostata e specificata nella pagina [**Impostazioni personali**](https://businesscentral.dynamics.com?page=9176 "\"Passare direttamente alla pagina impostazioni utente in Business Central"). Anziché immettere l'intera parola, è possibile immettere una parte della parola, ad esempio "l" o "lavoro".

Se non è stata definita una data di lavoro, per tale valore verrà automaticamente utilizzata la data corrente. Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.

Vedere anche [Modificare le impostazioni di base, quali l'ora di lavoro](ui-change-basic-settings.md#work-date).

### <a name="closing-date"></a>Data chiusura
Per chiudere un anno fiscale, è possibile utilizzare date di chiusura per indicare un movimento di chiusura. Una data di chiusura è tecnicamente compresa tra due date, ad esempio 31 dicembre e 1 gennaio.

Per specificare che si tratta di una data di chiusura, immettere `C` prima della data, ad esempio `C123101`. Questo metodo può essere utilizzato insieme a tutti i modelli per data.

### <a name="examples"></a>Esempi
Nella tabella seguente sono contenuti esempi di date utilizzando tutti i formati. Presuppone le impostazioni di paese con formato di data **anno.mese.giorno**, una settimana che inizia il lunedì e la lingua inglese.

|**Immissione**      |**Interpretazione**      |
|---------------|------------------------|
|`2018.12.31.`|2018.12.31.|
|`181231`|2018.12.31.|
|`18.12.31.`|2018.12.31.|
|`18.12.31.`|2018.12.31.|
|`20181231`|2018.12.31.|
|`18/12,31`|2018.12.31.|
|`11`|anno data di lavoro.mese data di lavoro.11.|
|`1112`|anno data di lavoro.11.12.|
|`t` o `today`|data odierna|
|`w` o `workdate`|la data di lavoro|
|`m` o `Monday`|Lunedì della settimana della data di lavoro|
|`tu` o `Tuesday`|Martedì della settimana della data di lavoro|
|`sa` o `Saturday`|Sabato della settimana della data di lavoro|
|`s` o `Sunday`|Domenica della settimana della data di lavoro|
|`t23`|Martedì della settimana 23 dell'anno della data di lavoro|
|`t 23`|Martedì della settimana 23 dell'anno della data di lavoro|
|`t-1`|Martedì della settimana 1 dell'anno della data di lavoro|

##  <a name="BKMK_SettingDateRanges"></a> Impostazione di intervalli di date
In elenchi, totali e report, è possibile impostare filtri su date, orari e periodi di tempo contenenti un valore iniziale e facoltativamente un valore finale per visualizzare solo i dati contenuti in tale intervallo. All'impostazione di intervalli di date si applicano regole standard.

|**significato**|**Espressione di esempio (data)**|**Dati inclusi nel filtro**|
|-----------|---------------------|--------------------|
|intervallo|`12 15 00..01 15 01`  \n`..12 15 00`|Record la cui data di risposta è compresa tra il 12 15 00 e il 01 15 01 inclusi.  \nRecord con data 12 15 00 o precedente.|
|oppure|`12 15 00|12 16 00`|Record con data 12 15 00 o 12 16 00. Se ci sono record con date in entrambi i giorni, saranno tutti visualizzati.|
|Combinazione|`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`|Record con data 12 15 00 o in date tra il 12 01 00 e il 12 10 00 compresi.  \nRecord la cui data è il 12 14 00 o una data precedente oppure il 12 30 00 o una data successiva, ossia tutti i record esclusi quelli la cui data di risposta è compresa tra il 12 15 00 e il 12 29 00 inclusi.|

È possibile utilizzare uno qualsiasi dei formati validi nei filtri dell'intervallo di date. Ad esempio, `mon14 3..t 4p` applicato a un campo data/ora risulta un filtro dalle 3 AM di lunedì nella settimana 14 dell'anno della data di lavoro corrente, incluso, fino alle 4 PM, comprese.


## <a name="using-date-formulas"></a>Utilizzo di formule per le date
Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date. È possibile immettere formule per le date in diversi campi o filtri per il calcolo della data.

> [!NOTE]
>  In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo. Di conseguenza, se si immette, ad esempio, `1W`, il periodo è effettivamente di otto giorni perché la data odierna è inclusa. Per specificare un periodo di sette giorni \(una settimana\) includendo la data di inizio del periodo, è necessario immettere `6D` o `1W-1D`.

Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:

-   La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.

-   La formula nel campo **Periodo di dilazione** per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza \(o dalla data del sollecito precedente\) alla creazione del sollecito.

-   La formula nel campo **Calcolo data di scadenza** determina la modalità di calcolo della data di scadenza nel sollecito.

La formula per la data può contenere un massimo di 20 caratteri, sia numeri che lettere. È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di calendario.

|  Lettera  |  Significato  |
|----------|----------------------|
|`C`|Corrente|
|`D`|Giorno\(i\)|
|`W`|Settimana\(e\)|
|`M`|Mese\(i\)|
|`Q`|Trimestre\(i\)|
|`Y`|Anno\(i\)|

È possibile creare una formula per la data in tre modi diversi.

L'esempio seguente mostra come usare `C`, vale a dire corrente, e un'unità di tempo.

|  Espressione  |  Significato  |
|--------------|-----------|
|`CW`|Settimana corrente|
|`CM`|Mese corrente|

L'esempio seguente mostra come usare un numero e un'unità di tempo. Il numero non può essere maggiore di 9999.

|  Espressione  |  Significato  |
|--------------|-----------|
|`10D`|10 giorni a partire da oggi|
|`2W`|2 settimane a partire da oggi|

L'esempio seguente mostra come usare un'unità di tempo e un numero.

|  Espressione  |  Significato  |
|--------------|-----------|
|`D10`|Il successivo giorno 10 del mese|
|`WD4`|Il successivo quarto giorno della settimana \(Giovedì\)|

Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.

|  Espressione  |  Significato  |
|--------------|-----------|
|`CM+10D`|Corrente mese \+ 10 giorni|

Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.

|  Espressione  |  Significato  |
|--------------|-----------|
|`-1Y`|1 anno fa da oggi|

> [!IMPORTANT]
>  Se l'ubicazione utilizza un calendario di base, la formula per la data immessa, ad esempio, nel campo **Durata spedizione** verrà interpretata in base ai giorni lavorativi del calendario. Ad esempio la formula `1W` significa sette giorni lavorativi.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

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
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a>Immissione di ore
Quando si immettono le ore, è possibile inserire qualsiasi separatore non spaziale desiderato tra le unità, ma se si utilizzano cifre doppie per ciascuna unità fino a millisecondi, non è necessario.

È necessario immettere solo le unità di grandi dimensioni di richiedere; il resto sarà uguale a zero. È inoltre possibile omettere qualsiasi di contrassegno con l'indicazione AM/PM.

Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti. Presuppone le impostazioni del paese che formattano le ore in base a **Ore:Minuti:Secondi.Millisecondi.** e utilizzano gli indicatori AM e PM per "AM" e"PM" rispettivamente.

|**Immissione**      |**Interpretazione**      |
|---------------|------------------------|
|`05:23:17`|05:23:17|
|`5`|05.00.00|
|`5AM`|05.00.00|
|`5P`|17:00:00|
|`12`|12:00:00|
|`12A`|00:00:00|
|`12P`|12:00:00|
|`17`|17:00:00|
|`5:30`|05.30.00|
|`0530`|05.30.00|
|`5:30:5`|05.30.05|
|`053005`|05.30.05|
|`5:30:5,50`|05:30:05,5|
|`053005050`|05.30.05,05|

È necessario tenere presente che i millisecondi vengono interpretati come notazione decimale. Così, ad esempio `3`, `30` e `300` tutti significano 300 millisecondi, mentre `03` significa `30` e `003` significa 3 millisecondi.

Non è possibile utilizzare `24:00` per indicare la mezzanotte, oppure utilizzare qualsiasi valore superiore a 24:00.

La parola per "ora" nella lingua usata da [!INCLUDE[d365fin](includes/d365fin_long_md.md)] verrà valutata per l'ora corrente del computer o dispositivo mobile in uso. È possibile immettere qualsiasi parte della parola, a partire dall'inizio, come `t` o `TIM`.

## <a name="entering-combined-dates-and-times"></a>Immissione di date e ore combinate
Quando si immettono dati di tipo datetime che corrispondono a una data e un'ora combinate in un campo, è necessario inserire uno spazio tra la data e l'ora. La parte della data può contenere solo spazi nella forma del separatore della data ufficiale delle impostazioni del paese. L'ora può contenere spazi attorno all'indicatore AM / PM.

È anche possibile inserire solo una data in un campo datetime, ma non è possibile inserire solo un'ora.

La seguente tabella elenca alcuni esempi di combinazioni di data/ora. Le impostazioni del paese negli esempi mostrano le date nel formato giorno\-mese\-anno, utilizzando i designatori AM / PM, la lingua inglese e la domenica come inizio della settimana.

|**Immissione**      |**Interpretazione**      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|08\-01\-2016 05:48:12 PM|
|`131202 132455`|13\-12\-2002 13:24:55|
|`1-12-02 10`|01\-12\-2002 10:00:00|
|`1.12.02 5`|01\-12\-2002 05:00:00|
|`1.12.02`|01\-12\-2002 00:00:00|
|`11 12`|11\-mese data di lavoro\-anno data di lavoro 12:00:00|
|`1112 12`|11\-12\-anno data di lavoro 12:00:00|
|`t` o `today`|Data odierna 00.00.00|
|`t 10:30`|Data odierna 10.30.00|
|`t 3:3:3`|Data odierna 03.03.03|
|`w` o `workdate`|Data del lavoro 00.00.00|
|`m` o `Monday`|Lunedì della settimana della data di lavoro 00:00:00|
|`tu` o `Tuesday`|Martedì della settimana della data di lavoro 00:00:00|
|`sa` o `Saturday`|Sabato della settimana della data di lavoro 00:00:00|
|`s` o `Sunday`|Domenica della settimana della data di lavoro 00:00:00|
|`tu 10:30`|Martedì della settimana della data di lavoro 10:30:00|
|`tu 3:3:3`|Martedì della settimana della data di lavoro 03:03:03|
|`t23 t`|Martedì della settimana 23 dell'anno della data di lavoro, ora corrente del giorno|
|`t23`|Martedì della settimana 23 dell'anno della data di lavoro|
|`t 23`|Oggi 23:00:00|
|`t-1`|Martedì della settimana 1 dell'anno della data di lavoro|

## <a name="entering-duration"></a>Immissione della durata
Alcuni campi dell'applicazione rappresentano una durata, o una quantità di tempo trascorso, anziché una data o un'ora specifica. È possibile immettere una durata in caratteri numerici seguiti dalla relativa unità di misura.

Di seguito vengono forniti alcuni esempi.

|**Durata**|**Unità di misura**|
|------------|-------------------|
|`2h`|2 ore|
|`6h 30 m`|6 ore 30 minuti|
|`6.5h`|6 ore 30 minuti|
|`90m`|1 ora 30 minuti|
|`2d 6h 30m`|2 giorni 6 ore 30 minuti|
|`2d 6h 30m 56s 600ms`|2 giorni 6 ore 30 minuti 56 secondi 600 millisecondi|

È inoltre possibile immettere un numero che verrà automaticamente convertito in una durata. Il numero immesso viene convertito in base all'unità di misura predefinita specificata nel campo relativo alla durata.

Per visualizzare l'unità di misura utilizzata in un campo di durata, immettere un numero e controllare l'unità di misura in cui viene convertito.

Ad esempio, il numero `5` viene convertito in 5 h se l'unità di misura è l'ora.


## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)  
[Immissione di criteri di filtro](ui-enter-criteria-filters.md)  

