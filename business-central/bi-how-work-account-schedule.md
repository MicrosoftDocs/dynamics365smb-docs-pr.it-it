---
title: Creare i report finanziari con i dati finanziari e le categorie di conti
description: Descrive come utilizzare i report finanziari per creare le visualizzazioni e i report per analizzare i dati finanziari.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a><a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Preparare i report finanziari con i dati finanziari e le categorie di conti

I report finanziari ti offrono informazioni dettagliate sui dati finanziari memorizzati nel piano dei conti. I report finanziari analizzano le cifre nei conti di contabilità generale (C/G) e confrontano i movimenti di contabilità generale con i movimenti di budget. La visualizzazione dei risultati nei grafici e nei report nella Gestione ruolo utente, quali il piano del flusso di cassa e i report Conto economico e Conto patrimoniale.

È possibile accedere a questi due report, ad esempio, con l'azione **Rendiconti finanziari** nella Gestione ruolo utente di Manager aziendale e Contabile.  

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce report finanziari di esempio che puoi utilizzare immediatamente. Puoi anche impostare righe e colonne personalizzate per specificare le cifre da confrontare. Puoi ad esempio creare report finanziari per calcolare i margini di profitto usando le dimensioni quali reparti o gruppi di clienti. Il numero di bilanci personalizzati che puoi creare è illimitato.  

L'impostazione dei report finanziari richiede una comprensione dei dati finanziari nel piano dei conti. Ad esempio, puoi visualizzare i movimenti di contabilità generale come percentuali dei movimenti di budget, ma ciò richiede la creazione di budget. Per ulteriori informazioni, vedi [Creare budget C/G](finance-how-create-budgets.md).

## <a name="financial-reports"></a><a name="financial-reports"></a>Report finanziari

I report finanziari organizzano i conti dal piano dei conti in modo da semplificare la presentazione dei dati. È possibile impostare vari layout per definire le informazioni che si desidera estrarre dal piano dei conti. I report finanziari forniscono uno spazio per i calcoli che non possono essere effettuati direttamente nel piano dei conti. Ad esempio, puoi creare subtotali per gruppi di conti e quindi includere quel totale in altri totali. Un altro esempio consiste nel calcolare i margini di profitto su dimensioni come reparti o gruppi di clienti. Inoltre puoi filtrare i movimenti di contabilità generale e i movimenti di budget in base, ad esempio, al saldo periodo o all'importo dare.

Puoi anche confrontare due o più report finanziari e definizioni di colonna utilizzando le formule, in modo da poter eseguire le seguenti operazioni:

* Creare report finanziari personalizzati.
* Creare tutti i report finanziari necessari, ognuno con un nome univoco.
* Impostare vari layout di report e stampare i report con le cifre correnti.

## <a name="gl-account-categories"></a><a name="gl-account-categories"></a>Categorie conto C/G

Le categorie di conto C/G consentono di modificare il layout dei rendiconti finanziari. Ad esempio, dopo aver impostato le categorie di conto nella pagina **Categorie conto C/G**, puoi scegliere l'azione **Genera report finanziari** e aggiornare i report finanziari sottostanti per i report finanziari principali. Alla successiva esecuzione di uno dei report, ad esempio il report **Conto patrimoniale**, nuovi totali e voci secondarie vengono aggiunte.

> [!NOTE]
> Le categorie di conto di livello superiore, come ad esempio il nodo **Passività**, sono fisse e non è possibile aggiungere. Tuttavia, è possibile eliminare e aggiungere categorie di conto ai livelli inferiori e definire la modalità di visualizzazione del report finanziario correlato nei report.
>
> Ti consigliamo di creare e strutturare da zero le proprie categorie di conto C/G di livello inferiore, se necessario in una gerarchia, anziché tentare di riorganizzare quelle esistenti. Ad esempio, è possibile ristrutturare il nodo **Passività** per contenere un nuovo nodo **Equità** seguito dai nodi **Passività correnti** e **Debiti a lungo termine**.

## <a name="create-a-new-financial-report"></a><a name="create-a-new-financial-report"></a>Creare un nuovo report finanziario

Usi i report finanziari per analizzare i conti di contabilità generale (C/G) o per confrontare i movimenti di contabilità generale con i movimenti di budget. Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.

I report finanziari nella versione standard di [!INCLUDE[prod_short](includes/prod_short.md)] possono non essere adatti alle tue esigenze aziendali. Per creare rapidamente i propri report finanziari, è possibile iniziare copiando un report finanziario esistente, come descritto al passaggio tre di seguito.

> [!TIP]
> Dopo aver creato un report finanziario, è possibile utilizzare la pagina **Report finanziario** per visualizzare in anteprima e convalidare il report finanziario appena definito. Per aprire la pagina scegli l'azione **Modifica report finanziario**.  

> [!NOTE]
> Quando si apre un report finanziario in modalità Visualizza o Modifica, è disponibile il riquadro Filtro. Tuttavia, non utilizzare il riquadro per impostare i filtri per i dati nel report. I filtri possono causare errori o potrebbero non filtrare effettivamente i dati. Utilizza invece i campi filtro nelle schede di dettaglio **Opzioni** e **Dimensioni**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.  
2. Sulla pagina **Report finanziari** scegli l'azione **Nuovo** per creare un nuovo nome per il report finanziario.
3. In alternativa, se desideri riutilizzare le impostazioni da un report finanziario esistente, scegli l'azione **Copia report finanziario**.
4. Compila i campi in base alle esigenze. Nel campo **Definizione colonna** seleziona una definizione esistente, che puoi modificare in seguito, se lo desideri.

    Le definizioni di colonna definiscono i parametri utilizzati per visualizzare i dati finanziari nelle righe. Ad esempio, una definizione di colonna può contenere quattro colonne che ti consentono di confrontare il saldo periodo e il saldo per lo stesso periodo di quest'anno e dell'anno scorso. Ulteriori informazioni nella sezione [Modificare una definizione di colonna](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Scegli l'azione **Modifica definizione di riga**.
6. Scegli le azioni **Inserisci conti C/G**, **Inserisci conti di cassa**, e **Inserisci tipi di costo** per creare una riga per ogni elemento finanziario che vuoi analizzare. Ad esempio, potresti avere una riga per i cespiti correnti e un'altra riga per i cespiti. Per avere un'idea, vedi i report finanziari nella società di esempio CRONUS.

    > [!NOTE]
    > Il campo **Nr. riga** mostra i primi 10 caratteri di un identificatore, ad esempio un numero di conto. Se aggiungi elementi con identificatori che iniziano con gli stessi 10 caratteri, avrai duplicati nel campo **Nr. riga** . Se necessario, puoi modificare manualmente gli identificatori dopo aver inserito gli elementi. Gli identificatori completi vengono visualizzati nel campo **Totale**.

7. Sulla pagina **Report finanziari** scegli l'azione **Modifica report finanziario** per accedere al report finanziario risultante.
8. Nella pagina **Report finanziario**, nel campo **Definizione colonna**, seleziona un'altra definizione di colonna per visualizzare i dati finanziari mediante altri parametri.
9. Selezionare **OK**.

A questo punto, hai definito la base del report finanziario, le righe dei dati finanziari da visualizzare e un layout esistente delle colonne per visualizzare i dati nelle righe usando parametri personalizzati. Se la definizione di colonna predefinita selezionata nel passaggio 4 non è adatta allo scopo, attieniti alla procedura in [Modificare una definizione di colonna](#edit-a-column-definition).

### <a name="edit-a-column-definition"></a><a name="edit-a-column-definition"></a>Modificare una definizione di colonna

Usa le definizioni di colonna per specificare le colonne da includere nel report. Ad esempio, è possibile creare un layout che metta a confronto saldo e saldo periodo per lo stesso periodo dell'anno in corso e di quello precedente. Puoi avere fino a 15 colonne, il che è utile, ad esempio, per visualizzare i budget per 12 mesi con una colonna che mostra il totale.

> [!NOTE]
> In una versione stampata/visualizzata in anteprima/salvata di un report finanziario è possibile visualizzare al massimo cinque colonne. Se il report finanziario invece è utilizzato solo per l'analisi nella pagina **Report finanziario**, è possibile creare tutte le colonne necessarie.

1. Sulla pagina **Report finanziari** seleziona il report finanziario pertinente, quindi scegli l'azione **Modifica definizione colonna**.
2. Nella pagina **Definizione colonna**, crea una riga per ogni colonna utilizzata per visualizzare i dati finanziari nel report finanziario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Selezionare **OK**.
4. Apri la pagina **Report finanziario** di tanto in tanto per verificare che la nuova definizione di colonna funzioni come previsto.

> [!NOTE]
> Le colonne definite in ciascuna riga rappresentano la colonna tre e le colonne successive nella pagina **Report finanziario**. Le prime due colonne, **Nr. riga** e **Descrizione**, sono fisse.  

### <a name="create-a-column-that-calculates-percentages"></a><a name="create-a-column-that-calculates-percentages"></a>Creare una colonna per il calcolo delle percentuali

A volte, potrebbe essere necessario includere in un report finanziario una colonna per il calcolo delle percentuali di un totale. Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, puoi inserire una colonna per indicare la percentuale delle vendite totale in ogni riga.

1. Scegli la ![lampadina che apre la funzione Dimmi 2.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.
2. Sulla pagina **Report finanziari** seleziona un report finanziario.  
3. Scegli l'azione **Modifica report finanziario** per impostare una riga del report finanziario per calcolare il totale su cui saranno basate le percentuali.  
4. Inserire una riga immediatamente sopra la prima riga per la quale si desidera visualizzare una percentuale.  
5. Compilare i campi della riga nel modo seguente: Nel campo **Tipo totale** immettere **Imposta base per percentuale**. Nel campo **Totale** immetti una formula del totale su cui sarà basata la percentuale. Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.  
6. Scegli l'azione **Modifica definizione colonna** per impostare una colonna.  
7. Compilare i campi della riga nel modo seguente: nel campo **Tipo colonna** selezionare **Formula**. Nel campo **Formula** immetti una formula per l'importo per il quale vuoi calcolare la percentuale, seguita dal segno di percentuale (%). Quindi, se il numero di colonna N contiene il saldo periodo, immetti **N%**.  
8. Ripeti i passaggi da 4 a 7 per ogni gruppo di righe che vuoi suddividere per percentuale.

## <a name="set-up-financial-reports-with-overviews"></a><a name="set-up-financial-reports-with-overviews"></a>Impostare report finanziari con panoramiche

È possibile utilizzare un report finanziario per creare un rendiconto in cui vengono confrontate le cifre della contabilità generale con le cifre del budget.

1. Scegli la ![lampadina che apre la funzione Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.
2. Sulla pagina **Report finanziari** seleziona un report finanziario.  
3. Scegli l'azione **Modifica definizione di riga**  
4. Nella pagina **Definizione riga** seleziona il nome del report finanziario predefinito nel campo **Nome**.
5. Scegli l'azione **Inserisci conti C/G**.  
6. Seleziona i conti che vuoi includere nella dichiarazione e scegli **OK**.

    I conti sono ora inseriti nel report finanziario. Inoltre puoi modificare la definizione di colonna.  
7. Sceglie l'azione **Modifica report finanziario**.  
8. Nella pagina **Report finanziario**, nella scheda dettaglio **Dimensioni**, imposta il filtro budget con il nome di filtro desiderato.  
9. Selezionare **OK**.  

Ora è possibile copiare e incollare la dichiarazione di budget in un foglio elettronico.  

## <a name="comparing-accounting-periods-using-period-formulas"></a><a name="comparing-accounting-periods-using-period-formulas"></a>Confronto dei periodi contabili con le formule periodo

Il report finanziario consente di confrontare i risultati di diversi periodi contabili, ad esempio mese precedente rispetto allo stesso mese dell'anno precedente. Per eseguire questa operazione, apri la pagina **Definizione colonna** e personalizzala aggiungendo il campo **Formula confronto periodo** come colonna. Per ulteriori informazioni vedi [Personalizzare l'area di lavoro](ui-personalization-user.md). È quindi possibile impostare quel campo su una formula del periodo.  

Un periodo contabile non deve necessariamente corrispondere al calendario. Tuttavia ogni anno fiscale deve avere lo stesso numero di periodi contabili, che possono avere una durata distinta.  

[!INCLUDE[prod_short](includes/prod_short.md)] usa la formula periodo per calcolare la durata del periodo di confronto in relazione al periodo rappresentato dal filtro data nel report. Il periodo di confronto si basa sul periodo indicato dalla data di inizio del filtro data. Le abbreviazioni per l'indicazione dei periodi sono:

| Abbreviazione | Descrizione                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periodo.                                                                                |
| UP           | Ultimo periodo di un trimestre, semestre o anno fiscale.                                   |
| CP           | Periodo corrente di un trimestre, semestre o anno fiscale. Usare CP nelle formule per impostare il periodo che inizia o finisce la formula. Ad esempio, FY\[1..CP\] indica il tempo dall'inizio dell'anno fiscale corrente al periodo corrente.|
| AF           | Anno fiscale. Ad esempio, FY\[1..3\] indica il primo trimestre dall'anno fiscale corrente. |

Esempi di formule

| Formula         | Descrizione                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Periodo corrente.                                                                                  |
| \-1P            | Periodo precedente.                                                                                 |
| \-1FY\[1..LP\]  | Intero anno fiscale precedente.                                                                     |
| \-1FY           | Periodo corrente nel precedente anno fiscale.                                                          |
| \-1FY\[1..3\]   | Primo trimestre dell'anno fiscale trascorso.                                                           |
| \-1FY\[1..CP\]  | Dall'inizio dell'anno fiscale trascorso al periodo corrente dell'anno fiscale trascorso, compresi entrambi i periodi. |
| \-1FY\[CP..LP\] | Dal periodo corrente dell'anno fiscale trascorso all'ultimo periodo dell'anno fiscale trascorso, compresi entrambi i periodi.   |

Se si desidera eseguire i calcoli in base a periodi di tempo regolari, è necessario invece immettere una formula nel campo **Formula confronto data**. Ad esempio, se il campo è impostato su -1A, in [!INCLUDE [prod_short](includes/prod_short.md)] viene effettuato il confronto con lo stesso periodo di un anno prima.

> [!NOTE]
> Non è sempre trasparente quali periodi si stanno confrontando perché è possibile impostare un filtro per data su un report che si estende su date diverse rispetto ai periodi contabili che si riflettono nel piano dei conti. Quindi, se crei un report finanziario in cui vuoi confrontare il periodo corrente con lo stesso periodo dell'anno precedente, imposti il campo **Formula confronto data** su *-1AF*. Quindi, si esegue il report il 28 febbraio e si imposta il filtro della data su gennaio e febbraio. Di conseguenza, il report finanziario confronta gennaio e febbraio di quest'anno con gennaio dell'anno scorso, che è l'unico periodo contabile completato dei due per l'anno prima.  

Per ulteriori informazioni, vedi [Utilizzare date e orari del calendario](ui-enter-date-ranges.md).

## <a name="print-and-save-financial-reports"></a><a name="print-and-save-financial-reports"></a>Stampare e salvare i report finanziari

Puoi stampare i report finanziari utilizzando i servizi di stampa del tuo dispositivo. [!INCLUDE[prod_short](includes/prod_short.md)] offre anche la possibilità di salvare i report come cartelle di lavoro di Microsoft Excel, documenti di Microsoft Word, file PDF e XML.

1. Scegli la ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
2. Sulla pagina **Report finanziari** seleziona il report da stampare, quindi scegli l'azione **Stampa**.
3. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nel campo **Stampante** seleziona il dispositivo a cui verrà inviato il report.
    1. L'opzione **(Gestito dal browser)** indica che non esiste una stampante designata per il report. In questo caso, il browser gestisce la stampa e visualizza i passaggi di stampa standard, in cui è possibile scegliere una stampante locale collegata al dispositivo. **(Gestito dal browser)** non è disponibile nell'app per dispositivi mobili [!INCLUDE[prod_short](includes/prod_short.md)] o nell'app per Microsoft Teams.
5. Scegliere l'azione **Stampa**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a><a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Pianificare un report finanziario o salvarlo come documento PDF, Word o Excel

Un report finanziario può essere salvato come file in diversi formati, come PDF, XML, Word o Excel. In alternativa, [!INCLUDE[prod_short](includes/prod_short.md)] può essere impostato per generare report finanziari ricorrenti:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
2. Nella pagina **Report finanziari** scegli l'azione **Stampa**.
3. Imposta il report di conseguenza, quindi scegli l'azione **Invia a**.
4. Seleziona il formato di file o l'azione **Programma** e scegli **OK**.
5. Per generare un report finanziario programmato o ricorrente, compila i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * Per i report finanziari ricorrenti, imposta i campi **Prima data/ora di inizio** e **Data/ora di scadenza** con la prima e l'ultima data, rispettivamente, per generare il report finanziario. Inoltre, seleziona in quali giorni viene generato il report impostando il campo **Formula della data di esecuzione successiva** seguendo il formato spiegato nella sezione [Usare le formule data](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports"></a><a name="importing-or-exporting-financial-reports"></a>Importazione o esportazione dei report finanziari

È possibile importare ed esportare i report finanziari come pacchetti di configurazione RapidStart, utili ad esempio per condividere le informazioni con altre aziende. Il pacchetto viene creato in un file .rapidstart, che comprime il contenuto.

### <a name="import-and-export-financial-reports"></a><a name="import-and-export-financial-reports"></a>Importare ed esportare report finanziari

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
2. Scegli il report finanziario, quindi scegli l'azione **Importa report finanziario** o **Esporta report finanziario**, a seconda di cosa vuoi fare.

> [!NOTE]
> Quando importi i report finanziari, i record esistenti con lo stesso nome di quelli che stai importando verranno eliminati.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Eseguire e stampare i report](ui-work-report.md)  
[Business Intelligence finanziario](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
