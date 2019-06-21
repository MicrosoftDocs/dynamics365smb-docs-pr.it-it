---
title: Come immettere dati nei campi| Microsoft Docs
description: Ottenere informazioni su funzionalità generali che consentono di immettere dati nei campi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/03/2019
ms.author: jswymer
ms.openlocfilehash: d0fac96313b41a0e41ea96ab4fedd25565498f12
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621162"
---
# <a name="entering-data"></a>Immissione di dati

Sono disponibili numerose funzionalità generali che consentono di immettere dati più facilmente, più velocemente e in modo più preciso. In questo articolo sono descritte tutte le funzionalità generali per l'immissione di dati.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Tasti di scelta rapida

Esistono vari tasti di scelta rapida che consentono di lavorare “senza mouse" e velocizzare l'immissione di dati, in particolare con immissioni su larga scala e task di digitazione ripetitive.

Per ulteriori informazioni sui tasti di scelta rapida, vedere [Tasti di scelta rapida](keyboard-shortcuts.md). Alcuni dei tasti di scelta rapida vengono discussi in questo articolo.

## <a name="QuickEntry"></a>Accelerazione dell'immissione di dati utilizzando Accesso rapido

Accesso rapido è una funzionalità concepita per l'immissione di dati utilizzando la tastiera. La funzionalità di Accesso rapido viene utilizzata nei campi (come nelle pagine scheda) e negli elenchi (righe e colonne). È utile quando si eseguono task di digitazione ripetitive che richiedono la creazione di più record in sequenza, ad esempio un batch di ordini di vendita o la registrazione di nuovi articoli.

È possibile che si abbia già una certa familiarità nell'utilizzo del tasto TAB per spostarsi da un campo in una pagina al campo modificabile successivo. Uno svantaggio inerente all'utilizzo del tasto TAB è che sposta sempre lo stato attivo al campo seguente in modo sequenziale. <!-- even if the field is non-editable or seldom filled it in.-->Accesso rapido funziona in un altro modo. Con Accesso rapido, si utilizza il tasto INVIO per spostarsi solo nei campi a cui si è interessati, ignorando i campi non modificabili e i campi che in genere non vengono compilati. È possibile che questo comportamento sia già stato osservato in alcune pagine. Questo perché l'applicazione designa già i campi da includere quando si preme INVIO e quali ignorare. È possibile personalizzare Accesso rapido personalizzando l'area di lavoro e ottimizzando il modo di immissione dei dati in ogni pagina.

### <a name="how-quick-entry-works"></a>Funzionamento di Accesso rapido

Ogni campo può essere contrassegnato come *incluso in Accesso rapido* o *escluso da Accesso rapido*. I campi inclusi in Accesso rapido verranno inclusi nel percorso quando si preme INVIO; i campi che sono esclusi da Accesso rapido, non lo saranno.

Al termine dell'immissione dei dati in un campo, premere semplicemente INVIO per confermare le modifiche e accedere al campo seguente. Per invertire la direzione e accedere al campo precedente, premere MAIUSC+INVIO. Per ulteriori informazioni sui tasti di scelta rapida, vedere [Tasti di scelta rapida di Accesso rapido per campi](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Suggerimenti e consigli
Di seguito vengono fornite alcune informazioni utili sull'utilizzo di Accesso rapido.

- È disponibile per qualsiasi campo modificabile.
- Funziona anche con colonne e righe.
- Non impedisce l'accesso ad altri elementi di una pagina, ad esempio le azioni. Questi sono sempre accessibili utilizzando TAB e MAIUSC+TAB.  
- Le Schede dettaglio non devono essere espanse per utilizzare Accesso rapido. Se il campo Accesso rapido successivo si trova in una Scheda dettaglio compressa, quella scheda verrà espansa automaticamente e lo stato attivo sarà sul campo designato.
- Il funzionamento di Accesso rapido è indipendente dal fatto che i campi siano obbligatori o meno. È quindi opportuno assicurarsi che i campi obbligatori siano inclusi in Accesso rapido.
- Per impostazione predefinita, la maggior parte dei campi vengono automaticamente inclusi in Accesso rapido. Quindi inizialmente la task escluderà probabilmente i campi da Accesso rapido.

### <a name="how-to-change-quick-entry-fields"></a>Come modificare i campi Accesso rapido

Per modificare quali campi sono inclusi o esclusi da Accesso rapido in una pagina, si utilizza la personalizzazione.

1. Avviare la personalizzazione selezionando l'icona ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente") e quindi **Personalizza**.
2. Selezionare un campo che si desidera modificare, o negli elenchi, selezionare l'intestazione di colonna corrispondente, quindi scegliere **Includi in Accesso rapido** o **Escludi da Accesso rapido**.

Per ulteriori informazioni sulla personalizzazione, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Campi obbligatori

Quando si immettono dati nelle pagine, alcuni campi sono contrassegnati con un asterisco rosso. L'asterisco rosso significa che il campo deve essere compilato per completare un determinato processo che utilizza il campo, ad esempio registrare una transazione che utilizza il valore nel campo.  

Anche se il campo contiene un asterisco rosso, non è obbligatorio compilarlo prima di continuare con altri campi o chiudere la pagina. L'asterisco rosso è solo un promemoria che segnala che l'utente sarà bloccato e non potrà completare un determinato processo.  

## <a name="finding-data-as-you-type"></a>Trovare dati durante la digitazione

 Quando si inizia a digitare dei caratteri in un campo, un elenco a discesa visualizza i valori di campo possibili. L'elenco cambia se si digitano ulteriori caratteri ed è possibile selezionare il valore corretto quando viene visualizzato.  

 In molti campi è disponibile un pulsante Freccia GIÙ che è possibile selezionare. Facendo clic sulla freccia, è possibile ottenere un elenco di tutti i dati disponibili in un quel campo. Il pulsante ha due funzioni, a seconda del tipo di campo:  

-   Lookup - Vengono visualizzate informazioni di un'altra tabella che possono essere immesse nel campo. È possibile selezionare soltanto un dato alla volta.  

-   DropDown - Vengono visualizzate le scelte possibili per il campo. È possibile selezionare soltanto una delle opzioni.  

## <a name="copying-and-pasting-fields-and-lines"></a>Copiare e incollare campi e righe

È possibile copiare una o più righe da un elenco o un singolo campo in una pagina e quindi incollare ciò che è stato copiato nella stessa pagina, in un'altra pagina o in un documento esterno (ad esempio di Microsoft Excel o Outlook). In breve, per copiare, premere CTRL + C (cmd + C in macOS) sulla tastiera. Per incollare, premere CTRL + V (cmd + V in macOS).

In un elenco, per copiare il campo nella stessa colonna della riga precedente e incollarlo nella riga corrente, premere F8.

Per ulteriori informazioni, vedere [Copiare e incollare in Business Central](ui-copy-paste.md).

## <a name="Focus"></a>Spostamento dello stato attivo sulle voci

Quando si lavora su documenti che includono la parte Voci, ad esempio un ordine di vendita o una fattura, è possibile passare a un'altra visualizzazione per spostare lo stato attivo solo sulle voci, essenzialmente espandendo la parte Voci affinché occupi l'intera area di lavoro, nascondendo altre parti della pagina ad eccezione dell'area Azioni nella parte superiore. In questo modo si ha una migliore panoramica delle voci e maggiore spazio per utilizzarle. Ciò è particolarmente utile quando si lavora con elenchi di voci di grandi dimensioni e si desidera un'immissione di dati rapida.

Un altro vantaggio è che fornisce una funzionalità di filtro avanzata, come in altre elenchi, e quindi la ricerca nelle voci diventa più semplice.

### <a name="switching-the-focus-on-and-off"></a>Attivare/disattivare lo stato attivo

Per spostare lo stato attivo sulle voci, selezionare un punto qualsiasi nella parte Voci, quindi scegliere l'![icona Modalità stato attivo](media/focus-mode.png "icona Modalità stato attivo") nell'angolo in alto a destra oppure premere CTRL+MAIUSC+F12.

Per passare di nuovo alla visualizzazione normale, scegliere l'![icona Modalità messa a fuoco](media/focus-mode.png "icona Modalità messa a fuoco") o premere di nuovo CTRL+MAIUSC+F12.

### <a name="filtering-the-line-items"></a>Filtri delle voci

Per avviare il filtro, selezionare l'![icona riquadro Filtro](media/open-filter-pane-icon.png "Icona riquadro Filtro") nella parte superiore dell'elenco o premere **MAIUSC+F3** per aprire il riquadro Filtro. il riquadro Filtro viene utilizzato come qualsiasi altro elenco. Per ulteriori informazioni, vedere [Filtri](ui-enter-criteria-filters.md#Filtering).

I filtri sono particolarmente utili quando si visualizzano e analizzano i documenti più lunghi. Ad esempio, si supponga di aprire una fattura di vendita registrata e di filtrare le voci per visualizzare tutte quelle che hanno un singolo sconto maggiore del 5% oppure per visualizzare solo accessori per biciclette con la parola “pro" nel nome.

## <a name="entering-quantities-by-calculation"></a>Immettere quantità mediante calcolo

Quando si immettono numeri nei campi numerici come il campo **Quantità** in una riga di registrazione magazzino, è possibile immettere la formula invece della quantità della somma.  

### <a name="examples"></a>Esempi  

-   Se si immette 19+19, il valore del campo viene calcolato in 38.  

-   Se si immette 41-9, il valore del campo viene calcolato in 32.  

-   Se si immette 12*4, il valore del campo viene calcolato in 48.  

-   Se si immette 12/4, il valore del campo viene calcolato in 3.  

## <a name="entering-negative-numbers"></a>Immettere numeri negativi

È possibile immettere numeri negativi in due modi. Il numero -20,5 può essere immesso come:  

-   -20,5  

    oppure
-   20,5-  

 In entrambi i casi, l'importo verrà registrato come -20,5.  

 Se l'ultimo carattere dell'espressione è un **+** o un **-**, l'intera espressione verrà registrata con tale segno. Ad esempio **10-20+** restituirà 10 e non -10.  

## <a name="entering-dates-and-times"></a>Immissione di date e ore

È possibile immettere date e ore in tutti i campi riservati alle date (campi di data). È possibile immettere date con o senza separatori.

> [!NOTE]  
> La modalità di immissione di date e ore dipende dalle impostazioni di **Area geografica**. Per ulteriori informazioni, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Immissione di date

Per i campi di date, è possibile utilizzare Selezione dati, che consente di selezionare una data da un calendario, oppure immettere manualmente le date. Questa sezione fornisce una breve panoramica della modalità di immissione di date. Per ulteriori informazioni, vedere [Utilizzo di date e orari del calendario](ui-enter-date-ranges.md).

Per l'immissione manuale di date, è possibile due, quattro, sei o otto cifre:  

-   Se si immettono solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.  

-   Se si immettono quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro.  

-   Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1930 e 31/12/2029, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.  

È inoltre possibile immettere una data composta da un giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno. Lu25 o lu25, ad esempio, indica lunedì nella settimana numero 25.  

Anziché immettere una data specifica, è possibile immettere uno di questi codici.  

|Code|Risultato|  
|--------------|----------------|  
|t|Specifica la data odierna (la data di sistema del computer).|  
|P|Specifica un periodo contabile, dove `p` indica il primo periodo contabile, `p2` indica il secondo periodo contabile e così via. |
|w|Specifica la data di lavoro impostata nell'applicazione. Per modificare la data di lavoro, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md). Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.|
|c|Indica che la data dopo `c`è una data di chiusura, ad esempio `C123101`.|  

## <a name="entering-times"></a>Immissione di ore

Quando si immette l'ora, è possibile inserire qualsiasi separatore tra le unità. L'immissione di un separatore è tuttavia facoltativa. Non è necessario immettere i minuti, i secondi o l'indicazione AM/PM.  

Nella tabella seguente sono indicati i diversi formati in cui è possibile immettere l'ora e le interpretazioni corrispondenti.  

|Movimento|Interpretazione|  
|---------------|------------------------|  
|5|05.00.00|  
|5:30|05.30.00|  
|0530|05.30.00|  
|5:30:5|05.30.05|  
|053005|05.30.05|  
|5:30:5.50|05:30:05,5|  
|053005050|05.30.05,05|  

 Se non si utilizza un separatore, è necessario immettere due cifre per ciascuna unità di tempo.  

## <a name="entering-datetimes"></a>Immissione di date e ore

Quando si immettono date e ore, è necessario inserire uno spazio tra la data e l'ora.  

Nella tabella seguente sono elencati i vari formati in cui è possibile immettere la data e l'ora e le interpretazioni corrispondenti.  

|Movimento|Interpretazione|  
|---------------|------------------------|  
|131202 132455|13/12/02 13.24.55|  
|1-12-02 10|01/12/02 10.00.00|  
|1.12.02 5|01/12/02 05.00.00|  
|1.12.02|01/12/02 00.00.00|  
|11 12|11-mese corrente-anno corrente 12.00.00|  
|1112 12|11-12-anno corrente 12.00.00|  
|t o today|Data odierna 00.00.00|  
|t time|Ora corrente in data odierna|  
|t 10:30|Data odierna 10.30.00|  
|t 3:3:3|Data odierna 03.03.03|  
|w o workdate|Data del lavoro 00.00.00|  
|lu o lunedì|Lunedì della settimana corrente 00.00.00|  
|ma o martedì|Martedì della settimana corrente 00.00.00|  
|me o mercoledì|Mercoledì della settimana corrente 00.00.00|  
|gi o giovedì|Giovedì della settimana corrente 00.00.00|  
|ve o venerdì|Venerdì della settimana corrente 00.00.00|  
|sa o sabato|Sabato della settimana corrente 00.00.00|  
|do o domenica|Domenica della settimana corrente 00.00.00|  
|ma 10:30|Martedì della settimana corrente 10.30.00|  
|ma 3:3:3|Martedì della settimana corrente 03.03.03|  

## <a name="entering-duration"></a>Immissione della durata

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

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Vedere anche  
 [Ricerca, filtro e ordinamento di elenchi](ui-enter-criteria-filters.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
