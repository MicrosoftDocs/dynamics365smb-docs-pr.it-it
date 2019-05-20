---
title: Metodi di ammortamento| Documenti Microsoft
description: Informazioni sui diversi metodi di ammortamento o svalutazione dei cespiti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9c9d01e54aa43cbba722c459a2bf60be26433727
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240978"
---
# <a name="depreciation-methods"></a>Metodi ammortamento
Esistono otto metodi di ammortamento:  

* Quote Costanti  
* Decrescente 1  
* Decrescente 2  
* Decr. 1/Cost.  
* Decr. 2/Cost.  
* personalizzato  
* Manuale  

  > [!NOTE]  
  >   È possibile utilizzare questo metodo per i cespiti che non sono soggetti ad ammortamento, ad esempio i terreni. Immettere l'ammortamento nella Registrazioni Cespiti in C/G. Il processo batch **Calcolo ammortamento** non considera i cespiti che utilizzano questo metodo di ammortamento.  
* Convenzione semestrale  

  > [!NOTE]  
  >    Utilizzando questo metodo nei cespiti, ogni anno viene ammortizzato lo stesso importo.  

## <a name="straight-line-depreciation"></a>Ammortamento a quote costanti
Se si utilizza il metodo a quote costanti occorre indicare nel registro beni ammortizzabili cespiti una delle seguenti opzioni:  

* il periodo di ammortamento (anni o mesi) o una data di fine ammortamento  
* una percentuale annuale fissa  
* un importo annuale fisso  
* il periodo di ammortamento  

### <a name="depreciation-period"></a>Periodo di ammortamento
Se viene immesso il periodo di ammortamento (numero di anni di ammortamento, numero di mesi di ammortamento o data di fine ammortamento), viene utilizzata la formula seguente per calcolare l'importo dell'ammortamento:  

*importo di ammortamento = ((valore contabile – valore realizzo) x numero di giorni di ammortamento)/giorni di ammortamento restanti*  

I giorni restanti di ammortamento vengono calcolati sottraendo al numero di giorni di ammortamento il numero di giorni intercorsi tra la data di inizio ammortamento e l'ultima data di movimento cespite.  

Al valore contabile può essere sottratta la rivalutazione registrata, la svalutazione, l'ammortamento anticipato e l'ammortamento acc./ridotto, a seconda che il campo **Includi nel Calc. Ammortamento** sia disattivato e che il campo **Parte del Valore Netto** sia attivo nella pagina **Setup Tipo Reg. Cespiti**. Questo calcolo garantisce che il cespite venga completamente ammortizzato alla data di fine ammortamento.  

### <a name="fixed-yearly-percentage"></a>Percentuale annuale fissa
Se viene immessa una percentuale annuale fissa, l'importo di ammortamento viene calcolato in base alla seguente formula:  

importo di ammortamento = (% quota costante x base ammortizzabile x numero di giorni di ammortamento) / (100 x 360)  

### <a name="fixed-yearly-amount"></a>Importo annuale fisso
Se viene immesso un importo annuale fisso, il calcolo dell'importo di ammortamento viene effettuato in base alla seguente formula:  

importo di ammortamento = (importo fisso di ammortamento x numero di giorni di ammortamento) / 360  

### <a name="example---straight-line-depreciation"></a>Esempio: ammortamento a quote costanti
Il costo di acquisto di un cespite è VL 100.000. La vita utile prevista è di otto anni. Il processo batch **Calcola Ammortamento** viene eseguita semestralmente.  

Per questo esempio, il movimento contabile cespite viene visualizzato come segue:  

| Data | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/10 |Costo di acquisto |* |100,000.00 |100,000.00 |
| 30/06/10 |Deprezzamento |180 |-6.250,00 |93,750.00 |
| 31/12/10 |Deprezzamento |180 |-6.250,00 |87,500.00 |
| 30/06/11 |Deprezzamento |180 |-6.250,00 |81,250.00 |
| 31/12/11 |Deprezzamento |180 |-6.250,00 |75,000.00 |
| 30/06/17 |Deprezzamento |180 |-6.250,00 |6,250.00 |
| 31/12/17 |Deprezzamento |180 |-6.250,00 |0 |

* Data inizio ammortamento  

## <a name="declining-balance-1-depreciation"></a>Metodo di ammortamento a quote decrescenti 1
Questo metodo di ammortamento accelerato alloca la maggior parte dei costi di un cespite ai primi anni della sua vita utile. Se viene utilizzato questo metodo, occorre immettere una percentuale annua fissa.  

La formula seguente calcola l'importo di ammortamento:  

*importo di ammortamento = (quota decrescente % x numero di giorni di ammortamento x base ammortizzabile) / (100 x 360)*  

La base ammortizzabile viene calcolata sottraendo al valore contabile l'ammortamento registrato a partire dalla data di inizio dell'esercizio in corso.  

L'importo di ammortamento registrato può contenere movimenti con diversi tipi di registrazione (svalutazione, personalizzato 1 e personalizzato 2) contabilizzati a partire dalla data di inizio dell'anno fiscale corrente. Questi tipi registrazione sono inclusi nell'importo di ammortamento registrato nel caso in cui siano presenti segni di spunta nei campi **Tipo ammortamento** e **Parte del valore contabile** nella pagina **Setup tipo reg. cespiti**.  

### <a name="example---declining-balance-1-depreciation"></a>Esempio: metodo di ammortamento a quote decrescenti 1
Il costo di acquisto di un cespite è VL 100.000. Il campo **Perc. amm. quote decr. %** è 25. Il processo batch **Calcola Ammortamento** viene eseguita semestralmente.  

La tabella seguente mostra l'aspetto dei movimenti contabili cespiti.  

| Data | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/10 |Costi di acquisto |* |100,000.00 |100,000.00 |
| 30/06/10 |Deprezzamento |180 |-12.500,00 |87,500.00 |
| 31/12/10 |Deprezzamento |180 |-12.500,00 |75,000.00 |
| 30/06/11 |Deprezzamento |180 |-9.375,00 |65,625.00 |
| 31/12/11 |Deprezzamento |180 |-9.375,00 |56,250.00 |
| 30/06/12 |Deprezzamento |180 |-7.031,25 |49,218.75 |
| 31/12/12 |Deprezzamento |180 |-7.031,25 |42,187.50 |
| 30/06/13 |Deprezzamento |180 |-5.273,44 |36,914.06 |
| 31/12/13 |Deprezzamento |180 |-5.273,44 |31,640.62 |
| 30/06/14 |Deprezzamento |180 |-3.955,08 |27,685.54 |
| 31/12/14 |Deprezzamento |180 |-3.955,08 |23,730.46 |

* Data inizio ammortamento  

    Metodo di calcolo:  

    *1° anno: 25% di 100.000 = 25.000 = 12.500 + 12.500*

    *2° anno: 25% di 75.000 = 18.750 = 9.375 + 9.375*

    *3° anno: 25% di 56.250 = 14.062,50 = 7.031,25 + 7.031,25*

    Il calcolo continua fino a quando il valore contabile corrisponde all'importo finale di arrotondamento o al valore di realizzo immesso.   

## <a name="declining-balance-2-depreciation"></a>Metodo di ammortamento a quote decrescenti 2
Con i metodi a quote decrescenti 1 e 2 viene calcolato lo stesso importo totale di ammortamento per ogni anno. Tuttavia, se il processo batch **Calcola Ammortamento** viene eseguito più di una volta all'anno, il metodo Decrescente 1 produce importi di ammortamento uguali per ogni periodo di ammortamento. Il metodo Decrescente 2 invece produce importi di ammortamento decrescenti per ogni periodo.  

### <a name="example---declining-balance-2-depreciation"></a>Esempio: metodo di ammortamento a quote decrescenti 2
Il costo di acquisto di un cespite è VL 100.000. Il campo **Perc. amm. quote decr. %** è 25. Il processo batch **Calcola Ammortamento** viene eseguita semestralmente. I movimenti contabili cespiti vengono visualizzati come segue:  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/10 |Costi di acquisto |* |100,000.00 |100,000.00 |
| 30/06/10 |Deprezzamento |180 |-13.397,46 |86,602.54 |
| 31/12/10 |Deprezzamento |180 |-11.602,54 |75,000.00 |
| 30/06/11 |Deprezzamento |180 |-10.048,09 |64,951.91 |
| 31/12/11 |Deprezzamento |180 |-8.701,91 |56,250.00 |

* Data inizio ammortamento  

Metodo di calcolo:  

* VC = Valore contabile  
* GA = numero di giorni di ammortamento  
* PQD = percentuale di ammortamento quote decrescenti  
* P = PQD/100  
* G = GA/360  

La formula per il calcolo dell'importo di ammortamento è la seguente:  

*IA = VC x (1-(1-P)<sup>D<sup>*  

I valori di ammortamento sono:  

| Date | Calcolo |
| --- | --- |
| 30/06/10 |IA = 100.000,00 x (1 -(1 - 0,25)<sup>0,5<sup>) = 13.397,46 |
| 31/12/10 |IA = 86.602,54 x (1 - (1 - 0,25)<sup>0,5<sup>) = 11.602,54 |
| 30/06/11 |IA = 75.000,00 x (1 - (1 - 0,25)<sup>0,5<sup>) = 10.048,09 |
| 31/12/11 |IA = 64.951,91 x (1 - (1 - 0,25)<sup>0,5<sup>) = 8.701,91 |

## <a name="db1sl-depreciation"></a>Ammortamento Decr. 1/Cost.
Decr. 1/Cost. è un abbreviazione che indica una combinazione del metodo a quote decrescenti 1 e del metodo a quote costanti. Il calcolo continua fino a quando il valore contabile corrisponde all'importo finale di arrotondamento o al valore di realizzo immesso.  

Con il processo batch **Calcola Ammortamento** viene calcolato un importo a quote costanti ed uno a quote decrescenti, ma soltanto l'importo maggiore viene trasferito nelle registrazioni.  

È possibile utilizzare le diverse percentuali per calcolare le quote decrescenti.  

Se viene utilizzato questo metodo, occorre immettere la vita utile prevista ed una percentuale di quota decrescente nella pagina **Registro Beni Amm. Cespiti**.  

### <a name="example---db1-sl-depreciation"></a>Esempio: ammortamento Decrescente 1-Quote Costanti
Il costo di acquisto di un cespite è VL 100.000. Nella pagina **Registro beni amm. cespiti** il campo **Perc. amm. quote decr. %** contiene 25 e il campo **Nr. anni di ammortamento** contiene 8. Il processo batch **Calcola Ammortamento** viene eseguita semestralmente.  

I movimenti contabili cespiti vengono visualizzati come segue:  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/10 |Costi di acquisto |* |100,000.00 |100,000.00 |
| 30/06/10 |Deprezzamento |180 |-12.500,00 |87,500.00 |
| 31/12/10 |Deprezzamento |180 |-12.500,00 |75,000.00 |
| 30/06/11 |Deprezzamento |180 |-9.375,00 |65,625.00 |
| 31/12/11 |Deprezzamento |180 |-9.375,00 |56,250.00 |
| 30/06/12 |Deprezzamento |180 |-7.031,25 |49,218.75 |
| 31/12/12 |Deprezzamento |180 |-7.031,25 |42,187.50 |
| 30/06/13 |Deprezzamento |180 |-5.273,44 |36,914.06 |
| 31/12/13 |Deprezzamento |180 |-5.273,44 |31,640.62 |
| 30/06/14 |Deprezzamento |180 |-3.955,08 |27,685.54 |
| 31/12/14 |Deprezzamento |180 |-3.955,08 |23,730.46 |
| 30/06/15 |Deprezzamento |180 |-3.955,08 |19.775,38 quote cost. |
| 31/12/15 |Deprezzamento |180 |-3.955,08 |15.820,30 quote cost. |
| 30/06/16 |Deprezzamento |180 |-3.955,08 |11.865,22 quote cost. |
| 31/12/16 |Deprezzamento |180 |-3.955,07 |7.910,15 quote cost. |
| 30/06/17 |Deprezzamento |180 |-3.955,08 |3.955,07 quote cost. |
| 31/12/17 |Deprezzamento |180 |-3.955,07 |0,00 quote cost. |

* Data inizio ammortamento  

L'indicazione "quote cost." dopo il valore contabile indica che è stato utilizzato il metodo a quote costanti.  

Metodo di calcolo:  

1° anno:  

*importo di ammortamento a quote decrescenti: 25% di 100.000 = 25.000=12.500+12.500*  

*importo di ammortamento a quote costanti = 100.000/8=12.500=6.250+6.250*  

L'importo di ammortamento a quote decrescenti viene utilizzato in quanto costituisce l'importo maggiore.  

6° anno (2015):  

*importo di ammortamento a quote decrescenti: 25% di 23,730.46 = 4,943.85=2,471.92+2,471.92*  

*importo di ammortamento a quote costanti = 23.730,46/3 = 7.910,15=3.995,07+3.995,08*  

L'importo di ammortamento a quote costanti viene utilizzato in quanto costituisce l'importo maggiore.  

## <a name="user-defined-depreciation"></a>Ammortamento definito dall'utente
Il programma dispone di una funzionalità che consente di impostare metodi di ammortamento personalizzati.  

Se si utilizza un metodo personalizzato, occorre inserire nella pagina **Tabelle Ammortamento** una percentuale di ammortamento per ogni periodo (mese, trimestre, anno o periodo contabile).  

La formula per il calcolo dell'importo di ammortamento è la seguente:  

Importo di ammortamento = (% ammortamento x numero di giorni di ammortamento x base ammortizzabile) / (100 x 360)  

### <a name="depreciation-based-on-number-of-units"></a>Ammortamento in base al numero di unità
Il metodo personalizzato può essere utilizzato anche per effettuare l'ammortamento in base al numero di unità, ad esempio nel caso di produzione di macchinari con una determinata durata totale di funzionamento. Nella pagina **Tabelle Ammortamento** è possibile immettere il numero di unità che possono essere prodotte in ogni periodo (mese, trimestre, anno o periodo contabile).  

### <a name="to-set-up-user-defined-depreciation-methods"></a>Per impostare i metodi di ammortamento personalizzati
La pagina **Tabella ammortamento** consente di impostare metodi di ammortamento personalizzati. Ad esempio, è possibile impostare l'ammortamento in base al numero di unità.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Tabelle ammortamento** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Lista tabelle ammortamento** scegliere l'azione **Nuovo**.  
3. Nella pagina **Scheda tabella ammortamento** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="example---user-defined-depreciation"></a>Esempio - ammortamento definito dall'utente
Ai fini del calcolo dell'imposta sul reddito, l'utilizzo di un determinato metodo di ammortamento consente di ammortizzare i cespiti più velocemente.  

A fini fiscali, per un cespite della durata utile di tre anni si utilizzerebbero i seguenti tassi di ammortamento:  

* 1° anno: 25%  
* 2° anno: 38%  
* 3° anno: 37%  

Il costo di acquisto è VL 100.000 e la durata dell'ammortamento è di 5 anni. L'ammortamento viene calcolato annualmente.  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/10 |Costo di acquisto |* |100,000.00 |100,000.00 |
| 31/12/10 |Deprezzamento |360 |-25.000,00 |75,000.00 |
| 31/12/11 |Deprezzamento |360 |-38.000,00 |37,000.00 |
| 31/12/12 |Deprezzamento |360 |-37.000,00 |0 |
| 31/12/13 |Deprezzamento |Nessuno |Nessuno |0 |
| 31/12/14 |Deprezzamento |Nessuno |Nessuno |0 |

* Data inizio ammortamento  

Se si utilizza un metodo personalizzato, occorre compilare i campi **Data iniz. amm. personalizzato** e **Data inizio ammortamento** nella pagina **Registro beni amm. cespiti**. Il campo **Data iniz. amm. personalizzato** e il contenuto del campo **Durata periodo** nella pagina **Tabelle ammortamento** consentono di determinare gli intervalli di tempo da utilizzare per i calcoli di ammortamento. In questo modo, viene garantito che la percentuale indicata sarà utilizzata per la prima volta lo stesso giorno per tutti i cespiti. Il campo **Data inizio ammortamento** consente di calcolare il numero di giorni di ammortamento.  

Nell'esempio precedente, i campi **Data iniz. amm. personalizzato** e **Data inizio ammortamento** contengono 01/01/01. Se invece nel campo **Data iniz. amm. personalizzato** fosse indicata la data 01/01/10 e nel campo **Data inizio ammortamento** la data riportata fosse 01/04/11, il risultato sarebbe:  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/01/10 |Costo di acquisto |* |100,000.00 |100,000.00 |
| 31/12/10 |Deprezzamento |270 |-18.750,00 |81,250.00 |
| 31/12/11 |Deprezzamento |360 |-38.000,00 |42,250.00 |
| 31/12/12 |Deprezzamento |360 |-37.000,00 |6,250.00 |
| 31/12/13 |Deprezzamento |90 |-6.250,00 |0 |
| 31/12/14 |Deprezzamento |Nessuno |Nessuno |0 |

* Data inizio ammortamento  

## <a name="half-year-convention-depreciation"></a>Ammortamento di convenzione semestrale
Il metodo di ammortamento di convenzione semestrale viene applicato se nel campo **Usa convenzione semestrale** della pagina **Registro beni amm. cespiti** è stato impostato un segno di spunta.  

Questo metodo può essere utilizzato insieme ai seguenti metodi di ammortamento:  

* Quote Costanti  
* Decrescente 1  
* Decr. 1/Cost.  

Applicando il metodo di convenzione semestrale, i cespiti avranno sei mesi di ammortamento durante il primo anno a prescindere dal contenuto del campo **Data inizio Ammortamento**.  

> [!NOTE]  
>   La vita utile residua del cespite dopo il primo anno finanziario conterrà sempre un semestre in cui viene utilizzato il metodo di convenzione semestrale. Affinché il metodo di convenzione semestrale venga applicato correttamente, nel campo **Data Finale Ammortamento** nel **Registro Beni Ammortizzabili Cespite** deve sempre essere riportata una data che sia esattamente di sei mesi anteriore alla data di fine esercizio in cui il cespite viene ammortizzato completamente.  

### <a name="example---half-year-convention-depreciation"></a>Esempio: ammortamento di convenzione semestrale
Il costo di acquisto di un cespite è VL 100.000. La **Data Inizio Ammortamento** è il 01/03/10. La vita utile prevista è di cinque anni, per cui la **Data Finale Ammortamento** deve essere il 30/06/15. Il processo batch **Calcola Ammortamento** viene eseguita annualmente. Questo esempio si basa su un anno finanziario di calendario.  

I movimenti contabili cespiti vengono visualizzati come segue:  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/03/10 |Costo di acquisto |* |100,000.00 |100,000.00 |
| 31/12/10 |Deprezzamento |270 |-10.000,00 |90,000.00 |
| 31/12/11 |Deprezzamento |360 |-20.000,00 |70,000.00 |
| 31/12/12 |Deprezzamento |360 |-20.000,00 |50,000.00 |
| 31/12/13 |Deprezzamento |360 |-20.000,00 |30,000.00 |
| 31/12/14 |Deprezzamento |360 |-20.000,00 |10,000.00 |
| 31/12/15 |Deprezzamento |180 |-10.000,00 |0.00 |

* Data inizio ammortamento  

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Esempio: ammortamento Decrescente 1/Quote Costanti utilizzando il metodo di convenzione semestrale
Il costo di acquisto di un cespite è VL 100.000. La **Data Inizio Ammortamento** è il 01/11/10. La vita utile prevista è di cinque anni, per cui la **Data Finale Ammortamento** deve essere il 30/06/15. Nella pagina **Registro beni amm. cespiti** il campo **Perc. amm. quote decr. %** contiene 40. Il processo batch **Calcola Ammortamento** viene eseguita annualmente. Questo esempio si basa su un anno finanziario di calendario.  

I movimenti contabili cespiti vengono visualizzati come segue:  

| Date | Tipo reg. cespite | Giorni | Importo | Valore contabile |
| --- | --- | --- | --- | --- |
| 01/11/10 |Costo di acquisto |* |100,000.00 |100,000.00 |
| 31/12/10 |Deprezzamento |60 |-20.000,00 |80,000.00 |
| 31/12/11 |Deprezzamento |360 |-32.000,00 |48,000.00 |
| 31/12/12 |Deprezzamento |360 |-19.200,00 |28,800.00 |
| 31/12/13 |Deprezzamento |360 |-11.520,00 |17,280.00 |
| 31/12/14 |Deprezzamento |360 |-11.520,00 |5.760,00 quote cost. |
| 31/12/15 |Deprezzamento |180 |-5.760,00 |0,00 quote cost. |

* Data inizio ammortamento  

L'indicazione "quote cost." dopo il valore contabile indica che è stato utilizzato il metodo a quote costanti.  

Metodo di calcolo:  

1° anno:  

*importo di ammortamento a quote decrescenti = importo dell'intero anno = 40% di 100.000 = 40.000. Ne consegue che l'importo semestrale è 40.000 / 2 = 20.000*  

*importo di ammortamento a quote costanti = importo dell'intero anno = 100.000 / 5 = 20.000. Ne consegue che l'importo semestrale è 20.000 / 2 = 10.000*  

L'importo di ammortamento a quote decrescenti viene utilizzato in quanto costituisce l'importo maggiore.  

5° anno (2004):  

*importo di ammortamento a quote decrescenti = 40% di 17.280,00 = 6.912,00*  

*importo di ammortamento a quote costanti = 28.800 / 1,5 = 11.520,00*  

L'importo di ammortamento a quote costanti viene utilizzato in quanto costituisce l'importo maggiore.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Duplicazione di movimenti in più registri beni ammortizzabili
In presenza di tre registri di beni ammortizzabili, B1, B2 e B3, per duplicare i movimenti da B1 a B2 e B3 occorre inserire un segno di spunta nel campo **Parte della Lista Duplicazione** nelle schede Registro Beni Ammortizzabili per B2 e B3. Si consiglia questa operazione nel caso in cui il registro dei beni ammortizzabili B1 sia integrato in contabilità generale ed utilizzi le registrazioni cespiti in contabilità generale ed i registri dei beni ammortizzabili B2 e B3 non siano integrati in contabilità generale ed utilizzino la registrazione cespiti.  

Immettendo un movimento in B1 nella registrazione C/G cespiti ed inserendo un segno di spunta nel campo **Usa Lista Duplicazione**, il movimento verrà duplicato nei registri B2 e B3 in Registrazioni Cespiti durante la registrazione.  

> [!NOTE]  
>   La registrazione e il batch di registrazione di partenza e di arrivo della duplicazione non possono coincidere. I movimenti possono essere duplicati nelle registrazioni cespiti o nelle registrazioni C/G cespiti quando vengono annotati nelle registrazioni C/G cespiti, a condizione che si utilizzi un batch diverso.  

> [!NOTE]  
>   Non è consentito utilizzare la stessa numerazione nelle registrazioni cespiti e nelle registrazioni cespiti. Quando si annotano movimenti nelle registrazioni cespiti o C/G, il campo **Nr. documento** deve essere lasciato vuoto. Se si immette un numero nel campo, il numero viene duplicato nelle registrazioni del cespite. Sarà necessario modificare manualmente il numero di documento prima di poter contabilizzare le registrazioni.  

## <a name="see-also"></a>Vedi anche
[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Introduzione](product-get-started.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
