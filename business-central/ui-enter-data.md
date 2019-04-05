---
title: Come immettere dati nei campi| Microsoft Docs
description: Numerose funzioni generali consentono di immettere dati in modo semplice e veloce. In questo argomento sono descritte tutte le funzioni generali per l'immissione di dati.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: f1bd2fb92f787d52c5bbab8c2210b9d424c1ffd5
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2019
ms.locfileid: "852495"
---
# <a name="entering-data"></a>Immissione di dati
Numerose funzioni generali consentono di immettere dati in modo semplice e veloce. In questo articolo sono descritte tutte le funzioni generali per l'immissione di dati.  

Gli esempi in questo articolo utilizzano dati di esempio.

## <a name="mandatory-fields"></a>Campi obbligatori
Quando si immettono dati nelle pagine, alcuni campi sono contrassegnati con un asterisco rosso. L'asterisco rosso significa che il campo deve essere compilato per completare un determinato processo che utilizza il campo, ad esempio registrare una transazione che utilizza il valore nel campo.  

Anche se il campo contiene un asterisco rosso, non è obbligatorio compilarlo prima di continuare con altri campi o chiudere la pagina. L'asterisco rosso è solo un promemoria che segnala che l'utente sarà bloccato e non potrà completare un determinato processo.  


## <a name="finding-data-as-you-type"></a>Trovare dati durante la digitazione  
 Quando si inizia a digitare dei caratteri in un campo, un elenco a discesa visualizza i valori di campo possibili. L'elenco cambia se si digitano ulteriori caratteri ed è possibile selezionare il valore corretto quando viene visualizzato.  

 In molti campi è disponibile un pulsante Freccia GIÙ che è possibile selezionare. Facendo clic sulla freccia, è possibile ottenere un elenco di tutti i dati disponibili in un quel campo. Il pulsante ha due funzioni, a seconda del tipo di campo:  

-   Lookup - Vengono visualizzate informazioni di un'altra tabella che possono essere immesse nel campo. È possibile selezionare soltanto un dato alla volta.  

-   DropDown - Vengono visualizzate le scelte possibili per il campo. È possibile selezionare soltanto una delle opzioni.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards on the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Immettere quantità mediante calcolo  
 Quando si immettono numeri nei campi numerici come il campo **Quantità** in una riga di registrazione magazzino, è possibile immettere la formula invece della quantità della somma.  

## <a name="examples"></a>Esempi  

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
 In un campo di data è possibile immettere due, quattro, sei o otto cifre:  

-   Se si immettono solo due cifre, queste vengono considerate come indicanti il giorno e il programma aggiunge il mese e l'anno della data di lavoro.  

-   Se si immettono quattro cifre, queste vengono considerate come indicanti il giorno e il mese e il programma aggiunge l'anno della data di lavoro.  

-   Se la data che si desidera immettere è inclusa nell'intervallo compreso tra 01/01/1930 e 31/12/2029, è possibile immettere l'anno utilizzando due cifre. In caso contrario, immettere l'anno in quattro cifre.  

 È inoltre possibile immettere una data composta da un giorno della settimana seguito da un numero di settimana e, facoltativamente, dall'anno. Lu25 o lu25, ad esempio, indica lunedì nella settimana numero 25.  

 Anziché immettere una data specifica, è possibile immettere uno dei due codici seguenti.  

|Codice|Risultato|  
|--------------|----------------|  
|t|Si tratta della data odierna (la data di sistema del computer).|  
|w|La data di lavoro impostata nell'applicazione. Per modificare la data di lavoro, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md). Potrebbe essere necessario utilizzare una data di lavoro se sono presenti molte transazioni con una data diversa da quella odierna.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Utilizzo di formule per le date  
 Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date. È possibile immettere formule per le date in diversi campi di calcolo e in campi relativi alla frequenza della ricorrenza in registrazioni periodiche.  

> [!NOTE]  
>  In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo. Di conseguenza, se si immette, ad esempio, 1W, il periodo è effettivamente di otto giorni perché la data odierna è inclusa. Per specificare un periodo di sette giorni (una settimana) includendo la data di inizio del periodo, è necessario immettere 6D o 1W-1D.  

 Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:  

-   La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.  

-   La formula nel campo Periodo di dilazione per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza (o dalla data del sollecito precedente) alla creazione del sollecito.  

-   La formula nel campo Calcolo data di scadenza determina la modalità di calcolo della data di scadenza nel sollecito.  

 La formula per il calcolo della data può contenere un massimo di 20 caratteri, sia numeri che lettere. È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di tempo diverse.  

|||  
|-|-|  
|C|Corrente|  
|D|Giorno/i|  
|W|Settimana/e|  
|M|Mese/i|  
|Q|Trimestre/i|  
|Y|Anno/i|  

 È possibile creare una formula per la data in tre modi diversi.  

 Nell'esempio seguente viene illustrato come corrente più un'unità di tempo.  

|||  
|-|-|  
|CW|Settimana corrente|  
|CM|Mese corrente|  

 Nell'esempio seguente viene illustrato come un numero e un'unità di tempo. Il numero non può essere maggiore di 9999.  

|||  
|-|-|  
|10D|10 giorni a partire da oggi|  
|2W|2 settimane a partire da oggi|  

 Nell'esempio seguente viene illustrato come un'unità di tempo e un numero.  

|||  
|-|-|  
|D10|Il successivo giorno 10 del mese|  
|WD4|Il successivo quarto giorno della settimana (giovedì)|  

 Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.  

|||  
|-|-|  
|CM+10D|Mese corrente + 10 giorni|  

 Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.  

|||  
|-|-|  
|-1A|1 anno fa da oggi|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Vedi anche  
 [Ricerca, filtro e ordinamento di elenchi](ui-enter-criteria-filters.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
