---
title: Creare i report finanziari con i dati finanziari e le categorie di conti
description: Descrive come utilizzare i report finanziari per creare le visualizzazioni e i report per analizzare i dati finanziari.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# Preparare il reporting finanziario con i dati finanziari e le categorie di conti

La funzionalità **Report finanziari** ti offre informazioni sui dati finanziari mostrati nel piano dei conti. Puoi configurare i report finanziari per analizzare le cifre nei conti di contabilità generale (C/G) e confrontare i movimenti di contabilità generale con i movimenti di budget. La visualizzazione dei risultati nei grafici e nei report nella Gestione ruolo utente, quali il piano del flusso di cassa e i report Conto economico e Conto patrimoniale. Puoi accedere a questi due report, ad esempio, con l'azione **Rendiconti finanziari** nelle home page Manager aziendale e Contabile.  

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce report finanziari di esempio che puoi utilizzare immediatamente come modelli. Puoi anche impostare report personalizzati per specificare le cifre da confrontare. Puoi ad esempio creare report finanziari per calcolare i margini di profitto usando le dimensioni quali reparti o gruppi di clienti. Il numero di report finanziari che puoi creare è illimitato e non richiede il coinvolgimento di uno sviluppatore.  

## Prerequisiti per il reporting finanziario

L'impostazione dei report finanziari richiede una comprensione della struttura del piano dei conti. Esistono tre concetti chiave a cui probabilmente devi prestare attenzione prima di progettare i tuoi report finanziari:

- Mappare i conti registrazione C/G alle categorie di conti C/G.
- Progettare il modo in cui utilizzi le dimensioni.
- Impostare i budget budget C/G.

Le categorie di conti C/G semplificano le definizioni dei report finanziari e li rendono più resistenti ai cambiamenti nella struttura del piano dei conti. Per ulteriori informazioni, vedi [Utilizzare categorie di conto C/G per modificare il layout dei rendiconti finanziari](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

L'impostazione delle dimensioni ti consente di suddividere e analizzare i tuoi dati finanziari in modi sensati per la tua organizzazione. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md). 

Se vuoi visualizzare i movimenti di contabilità generale come percentuali dei movimenti di budget, devi creare budget C/G. Per ulteriori informazioni, vedi [Creare budget C/G](finance-how-create-budgets.md).

## Report finanziari

I report finanziari organizzano i conti dal piano dei conti in modo da semplificare la presentazione dei dati. È possibile impostare vari layout per definire le informazioni che si desidera estrarre dal piano dei conti. I report finanziari inoltre forniscono uno spazio per i calcoli che non possono essere effettuati direttamente nel piano dei conti. Ad esempio, puoi creare subtotali per gruppi di conti e quindi includere quel totale in altri totali. Un altro esempio consiste nel calcolare i margini di profitto su dimensioni come reparti o gruppi di clienti. Inoltre puoi filtrare i movimenti di contabilità generale e i movimenti di budget in base, ad esempio, al saldo periodo o all'importo dare.

> [!NOTE] 
> Matematicamente, pensa a un report finanziario come definito da due cose:
>
> - Un vettore di definizioni di riga che definiscono cosa deve essere calcolato.
> - Un vettore di definizioni di colonna che definisce i dati per il calcolo.
>
> Il report finanziario è quindi il prodotto esterno di questi due vettori, dove ogni valore di cella viene calcolato in base alla formula nella riga applicata alla definizione dei dati dalla colonna.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Mostra come viene costruito un report finanziario da una definizione di riga e una definizione di colonna." lightbox="media/financial-report-definition.svg":::

La pagina **Report finanziari** mostra come tutti i report finanziari seguono uno schema costituito dai seguenti attributi:

* Nome (codice)
* Descrizione
* Definizione riga
* Definizione colonna

:::image type="content" source="media/financial-reports.png" alt-text="Mostra come vengono costruiti tutti i report finanziari da una definizione di riga e una definizione di colonna." lightbox="media/financial-reports.png":::

> [!NOTE]
> I report finanziari di esempio in [!INCLUDE[prod_short](includes/prod_short.md)] non sono pronti per essere utilizzati immediatamente. A seconda del modo in cui imposti i conti C/G, le dimensioni, le categorie di conti C/G e i budget, devi modificare le definizioni di riga e di colonna di esempio e i report finanziari in cui vengono utilizzate in base alla tua configurazione.

Puoi anche usare delle formule per confrontare due o più report finanziari e definizioni di colonna. Le comparazioni consentono di eseguire le seguenti operazioni:

* Creare report finanziari personalizzati.
* Creare tutti i report finanziari necessari, ognuno con un nome univoco.
* Impostare vari layout di report e stampare i report con le cifre correnti.

## Percorso di apprendimento: Creare report finanziari in Microsoft Dynamics 365 Business Central

Vuoi imparare a creare budget e quindi utilizzare report finanziari, dimensioni e definizioni di riga e di colonna per generare i report finanziari generalmente necessari per la maggior parte delle aziende?

Comincia ad apprendere mediante il percorso di apprendentimento [Creare report finanziari in Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central)

## Creare un nuovo report finanziario

Usi i report finanziari per analizzare i conti di contabilità generale (C/G) o per confrontare i movimenti di contabilità generale con i movimenti di budget. Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.

I report finanziari nella versione standard di [!INCLUDE[prod_short](includes/prod_short.md)] possono non essere adatti alle tue esigenze aziendali. Per creare rapidamente i propri report finanziari, è possibile iniziare copiando un report finanziario esistente, come descritto al passaggio tre di seguito.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.  
1. Sulla pagina **Report finanziari** scegli l'azione **Nuovo** per creare un nuovo nome per il report finanziario. In alternativa, per riutilizzare le impostazioni da un report finanziario esistente, scegli l'azione **Copia report finanziario**.
1. Immetti il nome breve del report (non può essere modificato) e la descrizione.
1. Scegli una definizione di riga e una definizione di colonna.
1. Eventualmente, scegli le visualizzazioni analisi per le definizioni di riga e di colonna.
1. Scegli l'azione **Modifica report finanziario** per accedere più proprietà nel report finanziario.
1. Nella Scheda dettaglio **Opzioni** puoi modificare la descrizione del report, modificare le definizioni di riga e di colonna e definire come visualizzare le date. Le date possono essere una gerarchia Giorno/Settimana/Mese/Trimestre/Anno oppure utilizzare periodi contabili. Per saperne di più, vedi [Confronto dei periodi contabili con le formule periodo](#comparing-accounting-periods-using-period-formulas)
1. Nella Scheda dettaglio **Dimensioni** puoi definire i filtri dimensioni per il report.
1. Puoi visualizzare l'anteprima del report nell'area sotto la Scheda dettaglio **Dimensioni**.

> [!TIP]
> Dopo aver creato un report finanziario, puoi utilizzare la pagina **Report finanziario** per visualizzarlo in anteprima e convalidarlo. Per aprire la pagina scegli l'azione **Visualizza report finanziario**.  

> [!NOTE]
> Quando si apre un report finanziario in modalità Visualizza o Modifica, è disponibile il riquadro Filtro. Non utilizzare il riquadro filtri per impostare i filtri per i dati nel report. Tali filtri possono causare errori o potrebbero non filtrare effettivamente i dati. Utilizza invece i campi nelle Schede dettaglio **Opzioni** e **Dimensioni** per impostare i filtri per il report.

### Creare o modificare una definizione di riga

Le definizioni di riga nei report finanziari forniscono un'area per i calcoli che non possono essere effettuati direttamente nel piano dei conti. Ad esempio, puoi creare subtotali per gruppi di conti e quindi includere quel totale in altri totali. Puoi anche calcolare passaggi intermedi che non vengono visualizzati nel report finale.

1. Nella pagina **Report finanziari** seleziona il report finanziario pertinente e quindi scegli l'azione **Modifica definizione riga**.
1. Scegli le azioni **Inserisci conti C/G**, **Inserisci conti di cassa**, e **Inserisci tipi di costo** per creare una riga per ogni elemento finanziario che vuoi analizzare. Ad esempio, potresti avere una riga per i cespiti correnti e un'altra riga per i cespiti. Per avere un'idea, esplora i report finanziari nella società demo CRONUS.

    > [!NOTE]
    > Il campo **Nr. riga** mostra i primi 10 caratteri di un identificatore, ad esempio un numero di conto. Se aggiungi elementi con identificatori che iniziano con gli stessi 10 caratteri, avrai duplicati nel campo **Nr. riga** . Se necessario, puoi modificare manualmente gli identificatori dopo aver inserito gli elementi. Gli identificatori completi vengono visualizzati nel campo **Totale**.

> [!NOTE]
> Le colonne definite in ciascuna riga nella definizione di riga rappresentano la colonna tre e le colonne successive nella pagina **Report finanziario**. Le prime due colonne, **Nr. riga** e **Descrizione**, sono fisse.  

### Creare o modificare una definizione di colonna

Usa le definizioni di colonna per specificare le colonne da includere nel report. Ad esempio, puoi creare un layout di report che metta a confronto saldo e saldo periodo per lo stesso periodo dell'anno in corso e di quello precedente. In una definizione di colonna possono essere presenti fino a 15 colonne. Ad esempio, più colonne sono utili per visualizzare i budget per 12 mesi con una colonna che mostra il totale.

> [!NOTE]
> In una versione stampata/visualizzata in anteprima/salvata di un report finanziario è possibile visualizzare al massimo cinque colonne. Se il report finanziario invece è utilizzato solo per l'analisi nella pagina **Report finanziario**, è possibile creare tutte le colonne necessarie.

1. Sulla pagina **Report finanziari** seleziona il report finanziario pertinente, quindi scegli l'azione **Modifica definizione colonna**.
1. Nella pagina **Definizione colonna**, crea una riga per ogni colonna utilizzata per visualizzare i dati finanziari nel report finanziario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Selezionare **OK**.
1. Apri la pagina **Report finanziario** di tanto in tanto per verificare che la nuova definizione di colonna funzioni come previsto.

### Creare una definizione di colonna per il calcolo delle percentuali

Potrebbe essere necessario includere in un report finanziario una colonna per il calcolo delle percentuali di un totale. Se, ad esempio, vi sono alcune righe in cui è prevista la suddivisione delle vendite per dimensioni, puoi inserire una colonna per indicare la percentuale delle vendite totale in ogni riga.

1. Scegli la ![lampadina che apre la funzione Dimmi 2.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Sulla pagina **Report finanziari** seleziona un report finanziario.  
1. Scegli l'azione **Modifica report finanziario** per impostare una riga del report finanziario per calcolare il totale su cui sono basate le percentuali.  
1. Aggiungi una riga immediatamente sopra la prima riga per la quale vuoi visualizzare una percentuale.  
1. Compilare i campi della riga nel modo seguente: Nel campo **Tipo totale** immettere **Imposta base per percentuale**. Nel campo **Totale** immetti una formula del totale su cui sarà basata la percentuale. Ad esempio, se il totale vendite è incluso nella riga 11 immettere **11**.  
1. Scegli l'azione **Modifica definizione colonna** per impostare una colonna.  
1. Compila i campi della riga come segue. Nel campo **Tipo colonna** seleziona **Formula**. Nel campo **Formula** immetti una formula per l'importo per il quale vuoi calcolare la percentuale, seguita dal segno di percentuale (%). Quindi, se il numero di colonna N contiene il saldo periodo, immetti **N%**.  
1. Ripeti i passaggi da 4 a 7 per ogni gruppo di righe che vuoi suddividere per percentuale.

## Usare le categorie di conto C/G per modificare il layout dei rendiconti finanziari

Le categorie di conto C/G consentono di modificare il layout dei rendiconti finanziari. Ad esempio, dopo aver impostato le categorie di conto nella pagina **Categorie conto C/G**, puoi scegliere l'azione **Genera report finanziari** e aggiornare i report finanziari sottostanti per i report finanziari principali. Alla successiva esecuzione di uno di questi report, ad esempio il report **Conto patrimoniale**, nuovi totali e voci secondarie vengono aggiunte.

Un altro vantaggio derivante dall'utilizzo di categorie di conto C/G rispetto ai conti C/G nelle definizioni di riga è che una modifica nella struttura del piano dei conti non influisce sui report finanziari.

> [!NOTE]
> Le categorie di conto di livello superiore, come ad esempio il nodo **Passività**, sono fisse e non è possibile aggiungerne altre. Tuttavia, è possibile eliminare e aggiungere categorie di conto ai livelli inferiori e definire la modalità di visualizzazione del report finanziario correlato nei report.
>
> Ti consigliamo di creare e strutturare da zero le proprie categorie di conto C/G di livello inferiore, se necessario in una gerarchia, anziché tentare di riorganizzare quelle esistenti. Ad esempio, è possibile ristrutturare il nodo **Passività** per contenere un nuovo nodo **Equità** seguito dai nodi **Passività correnti** e **Debiti a lungo termine**. Per saperne di più, vedi [Mapping dei conti di contabilità generale alle categorie di conti](finance-general-ledger.md#account-categories).

## Utilizzo delle dimensioni nei report finanziari

Nelle analisi finanziarie, una dimensione corrisponde ai dati che aggiungi a un movimento come una specie di contrassegno. Tali dati vengono utilizzati per raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Puoi usare le dimensioni per i movimenti in registrazioni, documenti e budget.

Ogni dimensione descrive lo stato attivo dell'analisi. Quindi, un'analisi bidimensionale, ad esempio, corrisponde a vendite per area. Utilizzando più di due dimensioni quando crei un movimento, puoi eseguire un'analisi più complessa. Un esempio di analisi complessa è l'esplorazione delle vendite per campagna di vendita, per gruppo di clienti e per area. Ciò ti offre una visione più approfondita della tua attività, ad esempio quanto bene sta operando, dove sta prosperando e dove non lo sta facendo e dove dovresti allocare più risorse. Queste informazioni ti consentono di prendere decisioni più informate. Per ulteriori informazioni, vedi [Utilizzare le dimensioni](finance-dimensions.md).

## Impostare report finanziari con panoramiche

Puoi utilizzare un report finanziario per creare un rendiconto che confronti le cifre della contabilità generale con le cifre del budget.

1. Scegli la ![lampadina che apre la funzione Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Sulla pagina **Report finanziari** seleziona un report finanziario.  
1. Scegli l'azione **Modifica definizione di riga**  
1. Nella pagina **Definizione riga** seleziona il nome del report finanziario predefinito nel campo **Nome**.
1. Scegli l'azione **Inserisci conti C/G**.  
1. Seleziona i conti che vuoi includere nella dichiarazione e scegli **OK**.

    I conti sono inseriti nel report finanziario. Inoltre puoi modificare la definizione di colonna.  
1. Sceglie l'azione **Modifica report finanziario**.  
1. Nella pagina **Report finanziario**, nella scheda dettaglio **Dimensioni**, imposta il filtro budget con il nome di filtro desiderato.  
1. Selezionare **OK**.  

Ora è possibile copiare e incollare la dichiarazione di budget in un foglio elettronico.  

## Confronto dei periodi contabili con le formule periodo

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

## Stampare e salvare i report finanziari

Puoi stampare i report finanziari utilizzando i servizi di stampa del tuo dispositivo. [!INCLUDE[prod_short](includes/prod_short.md)] offre anche la possibilità di salvare i report come cartelle di lavoro di Excel, documenti di Word, file PDF e XML.

1. Scegli la ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Sulla pagina **Report finanziari** seleziona il report da stampare, quindi scegli l'azione **Stampa**.
1. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Nel campo **Stampante** seleziona il dispositivo a cui verrà inviato il report.
    1. L'opzione **(Gestito dal browser)** indica che non esiste una stampante designata per il report. In questo caso, il browser gestisce la stampa e visualizza i passaggi di stampa standard, in cui è possibile scegliere una stampante locale collegata al dispositivo. **(Gestito dal browser)** non è disponibile nell'app per dispositivi mobili [!INCLUDE[prod_short](includes/prod_short.md)] o nell'app per Teams.
1. Scegliere l'azione **Stampa**.

### Pianificare un report finanziario o salvarlo come documento PDF, Word o Excel

Un report finanziario può essere salvato come file in diversi formati, come PDF, XML, Word o Excel. In alternativa, [!INCLUDE[prod_short](includes/prod_short.md)] può generare report finanziari ricorrenti:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Nella pagina **Report finanziari** scegli l'azione **Stampa**.
1. Imposta il report di conseguenza, quindi scegli l'azione **Invia a**.
1. Seleziona il formato di file o l'azione **Programma** e scegli **OK**.
1. Per generare un report finanziario programmato o ricorrente, compila i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Per i report finanziari ricorrenti, imposta i campi **Prima data/ora di inizio** e **Data/ora di scadenza** con la prima e l'ultima data, rispettivamente, per generare il report finanziario. Inoltre, seleziona in quali giorni viene generato il report impostando il campo **Formula della data di esecuzione successiva** seguendo il formato spiegato nella sezione [Usare le formule data](ui-enter-date-ranges.md#use-date-formulas).

## Importazione o esportazione di definizioni di report finanziari

Puoi importare ed esportare definizioni di report finanziari come pacchetti di configurazione RapidStart, utili ad esempio per condividere le informazioni con altre società. Il pacchetto viene creato in un file .rapidstart, che comprime il contenuto.

> [!NOTE]
> Quando importi le definzioni di riga/report finanziari, i record esistenti con lo stesso nome di quelli che stai importando verranno eliminati. Tieni presente che il pacchetto di configurazione per una definizione di report non sovrascriverà alcuna definizione di riga o di colonna esistente utilizzata nella definizione di report.

Per importare o esportare definizioni di report finanziari, procedi come segue:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Scegli il report finanziario, quindi scegli l'azione **Importa report finanziario** o **Esporta report finanziario**, a seconda di cosa vuoi fare.

Per importare o esportare definizioni di riga di report finanziari, procedi come segue:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Definizioni di riga** e scegli il collegamento correlato.
1. Scegli la definizione di riga, quindi scegli l'azione **Importa definizione di riga** o **Esporta definizione di riga**, a seconda di cosa vuoi fare.

## Vedere anche

[Eseguire e stampare i report](ui-work-report.md)  
[Business Intelligence finanziario](bi.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
