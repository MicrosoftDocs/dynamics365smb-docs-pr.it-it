---
title: Generare report finanziari con le situazioni contabili
description: Descrive come utilizzare le situazioni contabili per creare le visualizzazioni e i report per analizzare i dati finanziari.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8984d007f2082c6a21a3d2226a20f2ad585b131a
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129734"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Preparare i rendiconti finanziari con le situazioni contabili e le categorie di conti

Utilizzare le situazioni contabili per ottenere informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti. Le situazioni contabili analizzano le cifre nei conti di contabilità generale e confrontano i movimenti di contabilità generale con i movimenti budget di contabilità generale. La visualizzazione dei risultati nei grafici e nei report nella Gestione ruolo utente, quali il piano del flusso di cassa e i report Conto economico e Conto patrimoniale.

È possibile accedere a questi due report, ad esempio, con l'azione **Rendiconti finanziari** nella Gestione ruolo utente di Manager aziendale e Contabile.  

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce pianificazioni account di esempio che puoi utilizzare immediatamente. Puoi anche impostare righe e colonne personalizzate per specificare le cifre da confrontare. Puoi ad esempio creare piani dei conti per calcolare i margini di profitto in dimensioni quali reparti o gruppi di clienti. Il numero di bilanci personalizzati che puoi creare è illimitato.  

L'impostazione delle situazioni contabili richiede una comprensione dei dati finanziari nel piano dei conti. Ad esempio, puoi visualizzare i movimenti di contabilità generale come percentuali dei movimenti di budget, ma ciò richiede la creazione di budget. Per ulteriori informazioni, vedere [Creare budget C/G](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Situazioni contabili

Le situazioni contabili organizzano i conti dal piano dei conti in modo da semplificare la presentazione dei dati. È possibile impostare vari layout per definire le informazioni che si desidera estrarre dal piano dei conti. Le situazioni contabili forniscono uno spazio per i calcoli che non possono essere effettuati direttamente nel piano dei conti. Ad esempio, puoi creare subtotali per gruppi di conti e quindi includere quel totale in altri totali. Un altro esempio consiste nel calcolare i margini di profitto su dimensioni come reparti o gruppi di clienti. Inoltre puoi filtrare i movimenti di contabilità generale e i movimenti budget di contabilità generale in base, ad esempio, al saldo periodo o all'importo dare.

È inoltre possibile confrontare due o più situazioni contabili e layout di colonna utilizzando le formule che ti consente di effettuare le seguenti azioni:

* Creare report finanziari personalizzati.
* Creare tutte le situazioni contabili necessarie, ognuna con un nome univoco.
* Impostare vari layout di report e stampare i report con le cifre correnti.

## <a name="gl-account-categories"></a>Categorie conto C/G

Le categorie di conto C/G consentono di modificare il layout dei rendiconti finanziari. Dopo aver impostato le categorie di conto nella pagina **Categorie conto C/G** e aver scelto l'azione **Genera situazioni contabili**, le situazioni contabili sottostanti i report finanziari principali vengono aggiornate. Alla successiva esecuzione di uno dei report, ad esempio il report **Conto patrimoniale**, nuovi totali e voci secondarie vengono aggiunte, in base alle modifiche.

> [!NOTE]
> Le categorie di conto di livello superiore, come ad esempio il nodo **Passività** sono fisse e non è possibile aggiungere. Tuttavia, è possibile eliminare e aggiungere categorie di conto ai livelli inferiori e modificarne la struttura per definire la modalità di visualizzazione della situazione contabile correlata nei report.
>
> Si consiglia di creare e strutturare da zero le proprie categorie di conto C/G di livello inferiore, se necessario in una gerarchia, anziché tentare di riorganizzare quelle esistenti. Ad esempio, è possibile ristrutturare il nodo **Passività** per contenere un nuovo nodo **Equità** seguito dai nodi **Passività correnti** e **Debiti a lungo termine**.

## <a name="to-create-a-new-account-schedule"></a>Per creare una nuova situazione contabile

Utilizzare situazioni contabili per analizzare le cifre nei conti di contabilità generale o confrontare i movimenti di contabilità generale con i movimenti budget di contabilità generale. Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.

Le situazioni contabili nella versione standard di [!INCLUDE[prod_short](includes/prod_short.md)] sono la base dei report finanziari standard, che potrebbero non essere adatti alle esigenze dell'azienda. Per creare rapidamente i propri report finanziari, è possibile iniziare copiando una situazione contabile esistente, come descritto al passaggio 3.

> [!TIP]
> Dopo aver creato una situazione contabile, puoi utilizzare la pagina **Sintesi situaz. contabile** per visualizzare in anteprima e convalidare il report finanziario definito dalla situazione contabile. Per aprire la pagina, scegli l'azione **Panoramica**.  

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Situazioni contabili**, quindi scegli il collegamento correlato.  
2. Nella pagina **Situazioni contabili** scegliere l'azione **Nuovo** per creare una nuova situazione contabile.
3. In alternativa, se desideri riutilizzare le impostazioni da una situazione contabile esistente, scegli l'azione **Copia situazione contabile**.
4. Compilare i campi in base alle esigenze. Nel campo **Layout di colonna predefinito**, seleziona un layout esistente. Se necessario, è possibile modificarlo in seguito.

    I layout di colonna definiscono le colonne per i parametri utilizzati per visualizzare i dati finanziari nelle righe. Ad esempio, un layout di colonna può contenere quattro colonne che consentono di confrontare il saldo periodo e il saldo per lo stesso periodo di quest'anno e dell'anno scorso. Per ulteriori informazioni, vedere [Per modificare un layout di colonna](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Scegliere l'azione **Modifica situazione contabile**.
6. A seconda di cosa vuoi analizzare, scegli le azioni **Inserisci conti C/G**, **Inserisci conti di cassa**, e **Inserisci tipi di costo** per creare una riga per ogni elemento finanziario. Ad esempio, potresti avere una riga per i cespiti correnti e un'altra riga per i cespiti. Per avere un'idea, vedi le situazioni contabili nella società di esempio CRONUS.

    > [!NOTE]
    > Il campo **Nr. riga** mostrerà i primi 10 caratteri di un identificatore, ad esempio un numero di conto. Se aggiungi elementi con identificatori che iniziano con gli stessi 10 caratteri, avrai duplicati nel campo **Nr. riga** . Se necessario, puoi modificare manualmente gli identificatori dopo aver inserito gli elementi. Gli identificatori completi vengono visualizzati nel campo **Totale**.

7. Scegliere l'azione **Sintesi** per visualizzare il report finanziario risultante.
8. Nella pagina **Sintesi situaz. contabile**, nel campo **Nome Layout colonna**, selezionare un altro layout di colonna per visualizzare i dati finanziari mediante altri parametri.
9. Scegli il pulsante **OK**.

A questo punto, hai definito la base della situazione contabile, le righe dei dati finanziari da visualizzare e un layout esistente delle colonne per visualizzare i dati nelle righe per differenti parametri. Se il layout di colonna predefinito selezionato nel passaggio 4 non è adatto allo scopo, attieniti alla procedura seguente.

### <a name="to-edit-a-column-layout"></a>Per modificare un layout di colonna

I layout di colonna sono utilizzati per definire le colonne da includere nel report risultante. Ad esempio, è possibile creare un layout che metta a confronto saldo e saldo periodo per lo stesso periodo dell'anno in corso e di quello precedente. Puoi avere fino a 15 colonne, il che è utile, ad esempio, per visualizzare i budget per 12 mesi con una colonna che mostra il totale.

> [!NOTE]
> In una versione stampata/visualizzata in anteprima/salvata di una situazione contabile è possibile visualizzare al massimo cinque colonne. Se la situazione contabile è utilizzata solo per l'analisi nella pagina **Sintesi situaz. contabile**, è possibile creare tutte le colonne necessarie.

1. Nella pagina **Situazioni contabili**, selezionare la situazione contabile pertinente, quindi scegliere l'azione **Modifica setup layout colonna**.
2. Nella pagina **Layout colonne**, creare una riga per ogni colonna utilizzata per visualizzare i dati finanziari nel report finanziario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Scegliere il pulsante **OK**.
4. Aprire la pagina **Sintesi situaz. contabile** di tanto in tanto per verificare che il nuovo layout di colonna funzioni come previsto.

> [!NOTE]
> Le colonne definite in ciascuna riga rappresentano la colonna 3 e le colonne successive nella pagina **Sintesi situaz. contabile**. Le prime due colonne, **Nr. riga** e **Descrizione**, sono fisse.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Per creare una colonna per il calcolo delle percentuali

A volte, potrebbe essere necessario includere in una situazione contabile una colonna per il calcolo delle percentuali di un totale. Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, puoi inserire una colonna per indicare la percentuale delle vendite totale in ogni riga.

1. Scegli la ![lampadina che apre la funzione Dimmi 2.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Situazioni contabili**, quindi scegli il collegamento correlato.
2. Nella pagina **Descr. situazioni contabili** selezionare una situazione contabile.  
3. Selezionare l'azione **Modifica situazione contabile** per impostare una riga della situazione contabile per calcolare il totale su cui saranno basate le percentuali.  
4. Inserire una riga immediatamente sopra la prima riga per la quale si desidera visualizzare una percentuale.  
5. Compilare i campi della riga nel modo seguente: Nel campo **Tipo totale** immettere **Imposta base per percentuale**. Nel campo **Totale** immettere una formula del totale su cui sarà basata la percentuale. Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.  
6. Scegliere l'azione **Modifica setup layout colonna** per impostare una colonna.  
7. Compilare i campi della riga nel modo seguente: nel campo **Tipo colonna** selezionare **Formula**. Nel campo **Formula** immettere una formula per l'importo per il quale si desidera calcolare la percentuale, seguita dalla percentuale (%). Ad esempio, se il numero di colonna N contiene il saldo periodo, immettere **N%**.  
8. Ripetere i passaggi da 4 a 7 per ogni gruppo di righe che di desidera suddividere per percentuale.

## <a name="to-set-up-account-schedules-with-overviews"></a>Per impostare situazioni contabili con sintesi

È possibile utilizzare una situazione contabile per creare un rendiconto in cui vengono confrontate le cifre C/G con le cifre del budget C/G.

1. Scegli la ![lampadina che apre la funzione Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Situazioni contabili**, quindi scegli il collegamento correlato.
2. Nella pagina **Descr. situazioni contabili** selezionare una situazione contabile.  
3. Scegliere l'azione **Modifica situazione contabile**  
4. Nella pagina **Situazione contabile** selezionare il nome della situazione contabile di default nel campo **Nome**.
5. Scegli l'azione **Inserisci conti C/G**.  
6. Selezionare i conti che si intendono includere nella dichiarazione e selezionare il pulsante **OK**.

    I conti sono stati inseriti nella situazione contabile. Inoltre puoi modificare il layout di colonna.  
7. Scegliere l'azione **Sintesi**.  
8. Nella pagina **Sintesi situaz. contabile**, nella scheda dettaglio **Filtri dimensione**, imposta il filtro budget con il nome di filtro desiderato.  
9. Scegli il pulsante **OK**.  

Ora è possibile copiare e incollare la dichiarazione di budget in un foglio elettronico.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Confronto dei periodi contabili con le formule periodo

La situazione contabile consente di confrontare i risultati di diversi periodi contabili, ad esempio mese corrente rispetto allo stesso mese dell'anno precedente. Per eseguire questa operazione, aprire la pagina **Layout colonna** e personalizzala aggiungendo il campo **Formula confronto periodo** come colonna. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md). È quindi possibile impostare quel campo su una formula del periodo.  

Un periodo contabile non deve necessariamente corrispondere al calendario. Tuttavia ogni anno fiscale deve avere lo stesso numero di periodi contabili, che possono avere una durata distinta.  

[!INCLUDE[prod_short](includes/prod_short.md)] usa la formula periodo per calcolare l'importo dal periodo di confronto in relazione al periodo rappresentato dal filtro data nel report. Il periodo di confronto si basa sul periodo indicato dalla data di inizio del filtro data. Le abbreviazioni per l'indicazione dei periodi sono:

| Abbreviazione | Descrizione                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periodo                                                                                |
| UP           | Ultimo periodo di un trimestre, semestre o anno fiscale.                                   |
| CP           | Periodo corrente di un trimestre, semestre o anno fiscale. Usare CP nelle formule per impostare il periodo che inizia o finisce la formula. Ad esempio, FY\[1..CP\] indica il tempo dall'inizio dell'anno fiscale corrente al periodo corrente.|
| AF           | Anno fiscale. Ad esempio, FY\[1..3\] indica il primo trimestre dall'anno fiscale corrente |

Esempi di formule

| Formula         | Descrizione                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Periodo corrente                                                                                  |
| \-1P            | Periodo precedente                                                                                 |
| \-1FY\[1..LP\]  | Intero anno fiscale precedente                                                                     |
| \-1FY           | Periodo corrente nel precedente anno fiscale                                                          |
| \-1FY\[1..3\]   | Primo trimestre dell'anno fiscale trascorso                                                           |
| \-1FY\[1..CP\]  | Dall'inizio dell'anno fiscale trascorso al periodo corrente dell'anno fiscale trascorso, compresi entrambi i periodi |
| \-1FY\[CP..LP\] | Dal periodo corrente dell'anno fiscale trascorso all'ultimo periodo dell'anno fiscale trascorso, compresi entrambi i periodi   |

Se si desidera eseguire i calcoli in base a periodi di tempo regolari, è necessario invece immettere una formula nel campo **Formula confronto data**. Ad esempio, se il campo è impostato su -1A, in [!INCLUDE [prod_short](includes/prod_short.md)] viene effettuato il confronto con lo stesso periodo di un anno prima.

> [!NOTE]
> Non è sempre trasparente quali periodi si stanno confrontando perché è possibile impostare un filtro per data su un report che si estende su date diverse rispetto ai periodi contabili che si riflettono nei dati nel piano dei conti. Ad esempio, si crea una situazione contabile in cui si desidera confrontare il periodo corrente con lo stesso periodo dell'anno precedente, quindi si imposta il campo **Formula confronto data** su *-1AF*. Quindi, si esegue il report il 28 febbraio e si imposta il filtro della data su gennaio e febbraio. Di conseguenza, la situazione contabile confronta gennaio e febbraio di quest'anno con gennaio dell'anno scorso, che è l'unico periodo contabile completato dei due per l'anno prima.  

Per ulteriori informazioni sulle formule di data, vedere [Utilizzare date e orari del calendario](ui-enter-date-ranges.md).  

## <a name="import-or-export-account-schedules"></a>Importare o esportare situazioni contabili
Puoi importare ed esportare situazioni contabili come pacchetti di configurazione RapidStart. Ad esempio, i pacchetti di configurazione sono utili per condividerli con altre aziende. Il pacchetto viene creato in un file con estensione rapidstart, che offre il contenuto del pacchetto in un formato compresso.

### <a name="to-import-and-export-account-schedules"></a>Per importare ed esportare situazioni contabili
1. Scegli la ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Situazioni contabili**, quindi scegli il collegamento correlato.
2. Scegli la situazione contabile quindi scegli l'azione **Importa situazione contabile** o **Esporta situazione contabile** a seconda di cosa vuoi fare. 

> [!NOTE]
> Quando importi le situazioni contabili, i record esistenti con lo stesso nome di quelli che stai importando verranno eliminati.

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Intelligence](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]