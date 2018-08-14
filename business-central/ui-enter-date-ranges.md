---
title: Impostare gli intervalli di date in Business Central | Documenti Microsoft
description: Informazioni su come ottenere un report per visualizzare i dati relativi a periodi di tempo specifici utilizzando gli intervalli di date in Business Central.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: it-it
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Immettere intervalli di date
È possibile impostare filtri contenenti una data di inizio e una data di fine per visualizzare solo la data inclusa in un intervallo di date o di ore specifico. All'impostazione di intervalli di date si applicano regole speciali. Si consideri come esempio la **Lista primi 10 clienti**:

![Impostare un intervallo di date nella pagina di richiesta per la Lista primi 10 clienti](./media/ui-enter-date-ranges/customer-top10-list.png)

In questo campo è possibile limitare il report a un intervallo di date, ad esempio, alle ultime 2 settimane o a un totale di 6 settimane o a qualsiasi intervallo che si desidera. Per impostare gli intervalli di date, immettere le date quindi utilizzare **..** o **|** per impostare l'intervallo. Nell'esempio, per visualizzare i 10 clienti principali per le prime 2 settimane di maggio, impostare il filtro data come *05 01 17..05 14 17*.
Di seguito vengono proposti altri esempi:

| Significato | Esempio | movimenti inclusi |
|---|---|---|
|uguale a| 12 15 16 |Solo i movimenti registrati il 15 dicembre 2016.|
|intervallo| 12 15 16..01 15 17<br /><br />..12 15 16|Movimenti registrati in date comprese tra il 15 dicembre 2016 e il 15 gennaio 2017, inclusi.<br /><br />Movimenti registrati prima del 15 dicembre 2016, incluso.|
|oppure|12 15 16&#124;12 16 16|Movimenti registrati il 15 dicembre o il 16 dicembre 2016. Se sono presenti movimenti registrati in entrambi i giorni, verranno visualizzati tutti.|

È inoltre possibile combinare i vari tipi di formato.

| Esempio | movimenti inclusi |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Movimenti registrati il 15 dicembre 2016 o in date comprese tra il 01° dicembre 2016 e il 31 maggio 2017 inclusi. |
|..12 14 16&#124;12 30 16.. | Movimenti registrati il 14 dicembre, o in giorni precedenti, o movimenti registrati il 30 dicembre, o successivamente, ossia tutti i movimenti esclusi quelli registrati in date comprese tra il 15 e il 29 dicembre, incluse. |

Si noti che negli esempi è stato utilizzato il formato data MMGGAA degli Stati Uniti. Quando [!INCLUDE[d365fin](includes/d365fin_md.md)] sarà disponibile in altri mercati, sarà possibile utilizzare i formati abituali per il proprio paese.

## <a name="using-date-formulas"></a>Utilizzo di formule per le date
Una formula di data è una breve combinazione di lettere e numeri che specifica il modo in cui calcolare le date. È possibile immettere formule per le date in diversi campi di calcolo e in campi relativi alla frequenza della ricorrenza in registrazioni periodiche.

> [!NOTE]
>  In tutti i campi di formula di dati, viene automaticamente incluso un giorno per coprire la data odierna come giorno di inizio del periodo. Di conseguenza, se si immette, ad esempio, **1W**, il periodo è effettivamente di otto giorni perché la data odierna è inclusa. Per specificare un periodo di sette giorni (una settimana vera) includendo la data di inizio del periodo, è necessario immettere **6D** o **1W\-1D**.

Di seguito vengono forniti alcuni esempi dell'utilizzo di formule per le date:

-   La formula della data nel campo per la ricorrenza della frequenza nelle registrazioni periodiche indica la frequenza con cui il movimento nella riga delle registrazioni verrà registrato.

-   La formula nel campo **Periodo di dilazione** per un livello di sollecito specifico determina il periodo di tempo che deve trascorrere dalla data di scadenza (o dalla data di scadenza del sollecito precedente) alla creazione del sollecito.

-   La formula nel campo **Calcolo data di scadenza** determina la modalità di calcolo della data di scadenza nel sollecito.

La formula per il calcolo della data può contenere un massimo di 20 caratteri, sia numeri che lettere. È possibile utilizzare le lettere seguenti, corrispondenti ad abbreviazioni di unità di tempo diverse.

|  Lettera  |  Specifica temporale  |
|----------|----------------------|
|C|Corrente|
|D|Giorno\(i\)|
|OVEST|Settimana\(e\)|
|M|Mese\(i\)|
|T|Trimestre\(i\)|
|A|Anno\(i\)|

È possibile creare una formula per la data in tre modi diversi.

L'esempio seguente mostra come usare **C**, vale a dire corrente, e un'unità di tempo.

|  Espressione  |  Significato  |
|--------------|-----------|
|CW|Settimana corrente|
|CM|Mese corrente|

L'esempio seguente mostra come usare un numero e un'unità di tempo. Il numero non può essere maggiore di 9999.

|  Espressione  |  Significato  |
|--------------|-----------|
|10D|10 giorni a partire da oggi|
|2W|2 settimane a partire da oggi|

L'esempio seguente mostra come usare un'unità di tempo e un numero.

|  Espressione  |  Significato  |
|--------------|-----------|
|D10|Il successivo giorno 10 del mese|
|WD4|Il successivo quarto giorno della settimana \(Giovedì\)|

Nell'esempio seguente viene mostrato come è possibile combinare i tre formati in base alle esigenze.

|  Espressione  |  Significato  |
|--------------|-----------|
|CM\+10D|Corrente mese \+ 10 giorni|

Nell'esempio seguente viene illustrato come utilizzare un segno meno per indicare una data nel passato.

|  Espressione  |  Significato  |
|--------------|-----------|
|-1A|1 anno fa da oggi|

> [!IMPORTANT]
>  Se l'ubicazione utilizza un calendario di base, la formula per la data immessa, ad esempio, nel campo **Durata spedizione** verrà interpretata in base ai giorni lavorativi del calendario. Ad esempio la formula **1W** significa sette giorni lavorativi.

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)  
[Immissione di criteri di filtro](ui-enter-criteria-filters.md)  

