---
title: Definizioni di colonna nel reporting finanziario
description: Descrive il funzionamento delle definizioni di colonna nel reporting finanziario.
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Definizioni di colonna nel reporting finanziario

Usa definizioni di colonna per specificare le colonne da includere in un report. Ad esempio, puoi creare un layout di report che metta a confronto saldo e saldo periodo per lo stesso periodo dell'anno in corso e di quello precedente. In una definizione di colonna possono essere presenti fino a 15 colonne. Ad esempio, più colonne sono utili per visualizzare i budget per 12 mesi con una colonna che mostra il totale.

## Creare o modificare una definizione di colonna

Segui questi passaggi per creare o modificare una definizione di colonna:

> [!NOTE]
> In una versione stampata, visualizzata in anteprima e salvata di un report finanziario è possibile visualizzare al massimo cinque colonne. Se il report finanziario invece è utilizzato solo per l'analisi nella pagina **Report finanziario**, è possibile creare tutte le colonne necessarie.

1. Nella pagina **Report finanziari** seleziona il report finanziario pertinente, quindi scegli l'azione **Modifica definizione colonna**.
1. Nella pagina **Definizione colonna**, crea una riga per ogni colonna utilizzata per visualizzare i dati finanziari nel report finanziario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Selezionare **OK**.
1. Apri la pagina **Report finanziario** di tanto in tanto per verificare che la nuova definizione di colonna funzioni come previsto.

## Definizioni di colonna integrate

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce definizioni di colonna di esempio che possono aiutarti a iniziare rapidamente a configurare report finanziari che soddisfano le tue esigenze.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## Esempio: Creare una definizione di colonna per calcolare le percentuali

Potrebbe essere necessario includere in un report finanziario una colonna per il calcolo delle percentuali di un totale. Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, potresti voler inserire una colonna per indicare la percentuale delle vendite totali in ogni riga.

1. Scegli la ![lampadina che apre la funzione Dimmi 2.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Sulla pagina **Report finanziari** seleziona un report finanziario.  
1. Scegli l'azione **Modifica report finanziario** per impostare una riga del report finanziario per calcolare il totale su cui sono basate le percentuali.  
1. Aggiungi una riga immediatamente sopra la prima riga per la quale vuoi visualizzare una percentuale.  
1. Compila i campi della riga come segue: 
    1. Nel campo **Tipo totale** immettere **Imposta base per percentuale**. 
    1. Nel campo **Totale** immettere una formula per il totale su cui è basata la percentuale. Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.  
1. Scegli l'azione **Modifica definizione colonna** per impostare una colonna.  
1. Compila i campi della riga come segue. 
    1. Nel campo **Tipo colonna** seleziona **Formula**. 
    1. Nel campo **Formula** immetti una formula per l'importo per il quale vuoi calcolare la percentuale, seguita dal segno di percentuale (%). Quindi, se il numero di colonna N contiene il saldo periodo, immetti **N%**.  
1. Ripeti i passaggi da 4 a 7 per ogni gruppo di righe che vuoi suddividere per percentuale.

## Confronto dei periodi contabili con le formule periodo

Il report finanziario consente di confrontare i risultati di diversi periodi contabili, ad esempio mese precedente rispetto allo stesso mese dell'anno precedente. Per eseguire questa operazione, apri la pagina **Definizione colonna** e personalizzala aggiungendo il campo **Formula confronto periodo** come colonna. Per ulteriori informazioni vedi [Personalizzare l'area di lavoro](ui-personalization-user.md). È quindi possibile impostare quel campo su una formula del periodo.  

Un periodo contabile non deve necessariamente corrispondere al calendario. Tuttavia ogni anno fiscale deve avere lo stesso numero di periodi contabili, sebbene ogni periodo possa avere una durata distinta.  

[!INCLUDE[prod_short](includes/prod_short.md)] usa la formula periodo per calcolare la durata del periodo di confronto in relazione al periodo rappresentato dal filtro data nel report. Il periodo di confronto si basa sul periodo indicato dalla data di inizio del filtro data. La tabella seguente mostra le abbreviazioni per le specifiche del periodo.

| Abbreviazione | Descrizione                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periodo.                                                                                |
| UP           | Ultimo periodo di un trimestre, semestre o anno fiscale.                                   |
| CP           | Periodo corrente di un trimestre, semestre o anno fiscale. Usare CP nelle formule per impostare il periodo che inizia o finisce la formula. Ad esempio, FY\[1..CP\] indica il tempo dall'inizio dell'anno fiscale corrente al periodo corrente.|
| AF           | Anno fiscale. Ad esempio, FY\[1..3\] indica il primo trimestre dall'anno fiscale corrente. |

Esempi di formule

| Formula | Descrizione |
|-----|-----|
| \<Blank\>       | Periodo corrente. |
| \-1P            | Periodo precedente.            |
| \-1FY\[1..LP\]  | Intero anno fiscale precedente.                  |
| \-1FY           | Periodo corrente nel precedente anno fiscale.       |
| \-1FY\[1..3\]   | Primo trimestre dell'anno fiscale trascorso.        |
| \-1FY\[1..CP\]  | Dall'inizio dell'anno fiscale trascorso al periodo corrente dell'anno fiscale trascorso, compresi entrambi i periodi. |
| \-1FY\[CP..LP\] | Dal periodo corrente dell'anno fiscale trascorso all'ultimo periodo dell'anno fiscale trascorso, compresi entrambi i periodi.   |

Per calcolare in base a periodi di tempo regolari, immettere invece una formula nel campo **Formula confronto data**. Ad esempio, se il campo è impostato su -1A, in [!INCLUDE [prod_short](includes/prod_short.md)] viene effettuato il confronto con lo stesso periodo di un anno prima.

> [!NOTE]
> Non è sempre ovvio quali periodi si stanno confrontando perché è possibile impostare un filtro per data su un report che si estende su date diverse rispetto ai periodi contabili nel piano dei conti. Quindi, se crei un report finanziario in cui vuoi confrontare il periodo corrente con lo stesso periodo dell'anno precedente, imposti il campo **Formula confronto data** su **-1AF**. Quindi, si esegue il report il **28 febbraio** e si imposta il filtro della data su **gennaio e febbraio**. Di conseguenza, il report finanziario confronta gennaio e febbraio di quest'anno con gennaio dell'anno scorso, che è l'unico periodo contabile completato dei due per l'anno prima.  

Per ulteriori informazioni, vedi [Utilizzare date e orari del calendario](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## Importare o esportare definizioni di colonna di report finanziari

A partire dal primo ciclo di rilascio del 2024 (versione 24.1), puoi importare ed esportare le definizioni di colonna di report finanziari come pacchetti di configurazione RapidStart. Ad esempio, i pacchetti di configurazione sono utili per condividere le informazioni con altre società. Il pacchetto viene creato in un file .rapidstart, che comprime il contenuto.

> [!NOTE]
> Quando importi le definizioni di colonna di report finanziari, i record esistenti con lo stesso nome di quelli che stai importando verranno sostituiti con nuove definizioni. Il pacchetto di configurazione per una definizione di report non sovrascriverà alcuna definizione di riga o di colonna esistente utilizzata nella definizione di report.

Per importare o esportare definizioni di colonna di report finanziari, procedi come segue:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Definizioni di colonne**, quindi scegli il collegamento correlato.
1. Scegli la definizione di riga, quindi scegli l'azione **Importa definizione di colonna** o **Esporta definizione di colonna**, a seconda di cosa vuoi fare.

## Vedere anche

[Definizioni di riga nel reporting finanziario](bi-row-definitions.md)  
[Preparare il reporting finanziario](bi-how-work-account-schedule.md)  
[Business Intelligence finanziario](bi.md)  
[Dati finanziari](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
