---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2021
ms.author: bholtorf
---
Quando si immettono dati di tipo datetime che corrispondono a una data e un'ora combinate in un campo, è necessario inserire uno spazio tra la data e l'ora. La parte della data può contenere solo spazi nella forma del separatore della data ufficiale delle impostazioni del paese. L'ora può contenere spazi attorno all'indicatore AM/PM nelle impostazioni regionali rilevanti.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

Nella tabella seguente sono elencati i vari formati in cui è possibile immettere la data e l'ora e le interpretazioni corrispondenti.  

|Immissione|Interpretazione|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|11/mese corrente/anno corrente 12.00.00|
|1112 12|11/12/anno corrente 12.00.00|
|o oppure oggi|Data odierna 00.00.00|
|o ora|Ora corrente in data odierna|
|o 10:30|Data odierna 10.30.00|
|o 3:3:3|Data odierna 03.03.03|
|l o data di lavoro|Data del lavoro 00.00.00|
|lu o lunedì|Lunedì della settimana corrente 00.00.00|
|ma o martedì|Martedì della settimana corrente 00.00.00|
|me o mercoledì|Mercoledì della settimana corrente 00.00.00|
|gi o giovedì|Giovedì della settimana corrente 00.00.00|
|ve o venerdì|Venerdì della settimana corrente 00.00.00|
|sa o sabato|Sabato della settimana corrente 00.00.00|
|do o domenica|Domenica della settimana corrente 00.00.00|
|ma 10:30|Martedì della settimana corrente 10.30.00|
|ma 3:3:3|Martedì della settimana corrente 03.03.03|
|m23 o|Martedì della settimana 23 dell'anno della data di lavoro, ora corrente del giorno|
|m23|Martedì della settimana 23 dell'anno della data di lavoro|
|m 23|Oggi 23:00:00|
|m-1|Martedì della settimana 1 dell'anno della data di lavoro|


