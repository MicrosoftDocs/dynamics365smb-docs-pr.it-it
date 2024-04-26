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

Le categorie di conti C/G semplificano le definizioni dei report finanziari e li rendono più resistenti ai cambiamenti nella struttura del piano dei conti. Per ulteriori informazioni, vedi [Utilizzare categorie di conto C/G per modificare il layout dei rendiconti finanziari](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

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

- Nome (codice)
- Descrizione
- Definizione riga
- Definizione colonna

:::image type="content" source="media/financial-reports.png" alt-text="Mostra come vengono costruiti tutti i report finanziari da una definizione di riga e una definizione di colonna." lightbox="media/financial-reports.png":::

> [!NOTE]
> I report finanziari di esempio in [!INCLUDE[prod_short](includes/prod_short.md)] non sono pronti per essere utilizzati immediatamente. A seconda del modo in cui imposti i conti C/G, le dimensioni, le categorie di conti C/G e i budget, devi modificare le definizioni di riga e di colonna di esempio e i report finanziari in cui vengono utilizzate in base alla tua configurazione.

Puoi anche usare delle formule per confrontare due o più report finanziari e definizioni di colonna. Le comparazioni consentono di eseguire le seguenti operazioni:

- Creare report finanziari personalizzati.
- Creare tutti i report finanziari necessari, ognuno con un nome univoco.
- Impostare vari layout di report e stampare i report con le cifre correnti.

## Percorso di apprendimento: Creare report finanziari in Microsoft Dynamics 365 Business Central

Vuoi imparare a creare budget e quindi utilizzare report finanziari, dimensioni e definizioni di riga e di colonna per generare i report finanziari necessari per la maggior parte delle aziende?

Comincia mediante il percorso di apprendimento [Creare report finanziari in Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central).

## Creare un nuovo report finanziario

Usi i report finanziari per analizzare i conti di contabilità generale (C/G) o per confrontare i movimenti di contabilità generale con i movimenti di budget. Per esempio, è possibile visualizzare i movimenti C/G come percentuali dei movimenti budget.

I report finanziari nella versione standard di [!INCLUDE[prod_short](includes/prod_short.md)] possono non essere adatti alle tue esigenze aziendali. Per creare rapidamente i propri report finanziari, è possibile iniziare copiando un report finanziario esistente, come descritto al passaggio 3 di seguito.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.  
1. Sulla pagina **Report finanziari** scegli l'azione **Nuovo** per creare un nuovo nome per il report finanziario. In alternativa, per riutilizzare le impostazioni da un report finanziario esistente, scegli l'azione **Copia report finanziario**.
1. Immetti il nome breve del report (non puoi modificarlo in seguito) e la descrizione.
1. Scegli una definizione di riga e una definizione di colonna.
1. Eventualmente, scegli le visualizzazioni analisi per le definizioni di riga e di colonna.
1. Scegli l'azione **Modifica report finanziario** per accedere più proprietà nel report finanziario.
1. Nella Scheda dettaglio **Opzioni** puoi modificare la descrizione del report, modificare le definizioni di riga e di colonna e definire come visualizzare le date. Le date possono essere una gerarchia Giorno/Settimana/Mese/Trimestre/Anno oppure utilizzare periodi contabili. Per saperne di più, vedi [Confronto dei periodi contabili con le formule periodo](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas)
1. Nella Scheda dettaglio **Dimensioni** puoi definire i filtri dimensioni per il report.
1. Puoi visualizzare l'anteprima del report nell'area sotto la Scheda dettaglio **Dimensioni**.

> [!TIP]
> Dopo aver creato un report finanziario, puoi utilizzare la pagina **Report finanziario** per visualizzarlo in anteprima e convalidarlo. Per aprire la pagina scegli l'azione **Visualizza report finanziario**.  

> [!NOTE]
> Quando si apre un report finanziario in modalità Visualizza o Modifica, è disponibile il riquadro Filtro. Non utilizzare il riquadro filtri per impostare i filtri per i dati nel report. Tali filtri possono causare errori o potrebbero non filtrare effettivamente i dati. Utilizza invece i campi nelle Schede dettaglio **Opzioni** e **Dimensioni** per impostare i filtri per il report.

### Creare o modificare una definizione di riga

Le definizioni di riga nei report finanziari forniscono un'area per i calcoli che non possono essere effettuati direttamente nel piano dei conti. Ad esempio, puoi creare subtotali per gruppi di conti e quindi includere quel totale in altri totali. Puoi anche calcolare passaggi intermedi che non vengono visualizzati nel report finale.

Per saperne di più, vedi [Definizioni di riga nel reporting finanziario](bi-row-definitions.md).

### Creare o modificare una definizione di colonna

Usa le definizioni di colonna per specificare le colonne da includere nel report. Ad esempio, puoi creare un layout di report che metta a confronto saldo e saldo periodo per lo stesso periodo dell'anno in corso e di quello precedente. In una definizione di colonna possono essere presenti fino a 15 colonne. Ad esempio, più colonne sono utili per visualizzare i budget per 12 mesi con una colonna che mostra il totale.

Per saperne di più, vedi [Definizioni di colonna nel reporting finanziario](bi-column-definitions.md).

## Utilizzo delle dimensioni nei report finanziari

Nelle analisi finanziarie, una dimensione corrisponde ai dati che aggiungi a un movimento come una specie di contrassegno. Tali dati vengono utilizzati per raggruppare movimenti con caratteristiche simili, ad esempio clienti, aree, prodotti e agenti, quindi recuperare facilmente questi gruppi per l'analisi. Puoi usare le dimensioni per i movimenti in registrazioni, documenti e budget.

Ogni dimensione descrive lo stato attivo dell'analisi. Quindi, un'analisi bidimensionale, ad esempio, corrisponde a vendite per area. Utilizzando più di due dimensioni quando crei un movimento, puoi eseguire un'analisi più complessa. Un esempio di analisi complessa è l'esplorazione delle vendite per campagna di vendita, per gruppo di clienti e per area. Ciò ti offre una visione più approfondita della tua attività, ad esempio quanto bene sta operando, dove sta prosperando e dove non lo sta facendo e dove dovresti allocare più risorse. Queste informazioni ti consentono di prendere decisioni più informate. Per ulteriori informazioni, vedi [Usare le dimensioni](finance-dimensions.md).

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

## Integra i report finanziari con Excel

Puoi integrare un report finanziario con un modello di cartella di lavoro Excel, adattare il layout alle tue esigenze e quindi aggiornare il modello Excel con i dati da [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, questa integrazione semplifica la generazione dei rendiconti finanziari mensili e annuali in un formato adatto alle tue esigenze.

### Configurare l'integrazione di Excel per un report finanziario (creare un modello Excel)

Per impostare l'integrazione di Excel per un report finanziario, attieniti alla seguente procedura per creare un modello Excel per un report.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Nella pagina **Report finanziari** seleziona il report finanziario da abilitare con Excel e quindi scegli l'azione **Esporta in Excel**.
1. Selezionare l'azione **Crea nuovo documento**. Questa azione scarica un modello di cartella di lavoro Excel con un singolo foglio di lavoro denominato in base al nome del report.
1. Copia il foglio di lavoro e rinominalo in **Dati**.
1. Rinomina il foglio di lavoro del report a tuo piacimento.
1. Nel foglio di lavoro del report, contrassegna tutte le celle che mostrano i dati del report finanziario (comprese le intestazioni di colonna e riga). Nella barra multifunzione **Home**, trova il menu **Numero** e seleziona **Generale** come formato.
1. Scegli la cella più a sinistra dell'area con i dati del report finanziario e imposta un riferimento alla cella equivalente nel foglio di lavoro Dati. Trascina la formula verso destra per estenderla a tutte le celle della prima riga, quindi trascina la riga verso il basso per coprire tutte le righe del report finanziario.
1. Nascondi il foglio di lavoro **Dati**.
1. Formatta il foglio di lavoro del report in base alle tue esigenze.
1. Salva la cartella di lavoro in OneDrive o in una posizione simile in cui viene eseguito il backup e la versione del file.
1. Chiudi la cartella di lavoro.

### Esegui un report finanziario con un modello Excel

Per eseguire un report finanziario con un modello Excel, attieniti alla seguente procedura:

1. Scegli la ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Nella pagina **Report finanziari** seleziona il report finanziario da abilitare con Excel e quindi scegli l'azione **Esporta in Excel**.
1. Scegli l'azione **Aggiorna copia del documento esistente**.
1. Carica il tuo modello Excel (chiudi la cartella di lavoro Excel prima di caricarla).
1. Nella pagina **Ricerca nome/valore**, scegli il foglio di lavoro Dati.
1. [!INCLUDE[prod_short](includes/prod_short.md)] esegue il report finanziario e unisce i dati risultanti con il modello Excel.

## Stampare e salvare i report finanziari

Puoi stampare i report finanziari utilizzando i servizi di stampa del tuo dispositivo. [!INCLUDE[prod_short](includes/prod_short.md)] offre anche opzioni di salvare i report come cartelle di lavoro di Excel, documenti di Word, file PDF e XML.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Sulla pagina **Report finanziari** seleziona il report da stampare, quindi scegli l'azione **Stampa**.
1. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Nel campo **Stampante** seleziona il dispositivo a cui viene inviato il report.
    1. L'opzione **(Gestito dal browser)** indica che non esiste una stampante designata per il report. In questo caso, il browser gestisce la stampa e visualizza i passaggi di stampa standard, in cui è possibile scegliere una stampante locale collegata al dispositivo. **(Gestito dal browser)** non è disponibile nell'app per dispositivi mobili [!INCLUDE[prod_short](includes/prod_short.md)] o nell'app per Teams.
1. Scegliere l'azione **Stampa**.

### Pianificare un report finanziario o salvarlo come documento PDF, Word o Excel

Puoi salvare un report finanziario in formti di file come PDF, XML, Word o Excel. [!INCLUDE[prod_short](includes/prod_short.md)] può anche generare report finanziari ricorrenti.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Nella pagina **Report finanziari** scegli l'azione **Stampa**.
1. Imposta il report di conseguenza, quindi scegli l'azione **Invia a**.
1. Seleziona il formato di file o l'azione **Programma** e scegli **OK**.
1. Per generare un report finanziario programmato o ricorrente, compila i campi. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Per i report finanziari ricorrenti, imposta i campi **Prima data/ora di inizio** e **Data/ora di scadenza** con la prima e l'ultima data, rispettivamente, per generare il report finanziario. Inoltre, seleziona in quali giorni viene generato il report impostando il campo **Formula della data di esecuzione successiva** seguendo il formato spiegato nella sezione [Usare le formule data](ui-enter-date-ranges.md#use-date-formulas).


## Procedure consigliate per utilizzare definizioni di report finanziari

Le definizioni di report finanziari non hanno una versione. Quando modifichi una definizione di report, la versione precedente viene sostituita quando la modifica viene salvata nel database. L'elenco seguente contiene alcune procedure consigliate per l'utilizzo delle definizioni di report finanziari:

- Se aggiungi definizioni di report, scegli un buon codice e compila il campo della descrizione con un testo significativo mentre sai ancora per quale motivo usi il report. Queste informazioni aiutano i tuoi colleghi (e te stesso in futuro) a lavorare con il report e magari a modificare la definizione di report.
- Prima di modificare una definizione di report, prendine una copia come backup, nel caso in cui la modifica non funzioni come previsto. Puoi semplicemente copiare la definizione (dargli un nome appropriato) o esportarla. Per saperne di più, vedi [Importare o esportare definizioni di report finanziari](#import-or-export-financial-report-definitions).
- Se hai bisogno di una nuova copia di una definizione che [!INCLUDE[prod_short](includes/prod_short.md)] fornisce, un modo semplice di ottenerne una è creare una nuova società che contenga solo i dati di setup. Quindi, esporta la definizione e importala nella società in cui la definizione necessita di un aggiornamento.

## Importare o esportare definizioni di report finanziari

Puoi importare ed esportare definizioni di report finanziari come pacchetti di configurazione RapidStart. Ad esempio, i pacchetti di configurazione sono utili per condividere le informazioni con altre società. Il pacchetto viene creato in un file .rapidstart, che comprime il contenuto.

> [!NOTE]
> Quando importi le definizioni di report finanziari, i record esistenti con gli stessi nomi di quelli che stai importando vengono eliminati. Il pacchetto di configurazione per una definizione di report non sovrascriverà alcuna definizione di riga o di colonna esistente utilizzata nella definizione di report.

Per importare o esportare definizioni di report finanziari, procedi come segue:

1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Scegli il report finanziario, quindi scegli l'azione **Importa report finanziario** o **Esporta report finanziario**, a seconda di cosa vuoi fare.

Per ulteriori informazioni su come importare o esportare le definizioni di righe o colonne del report finanziario, consulta i seguenti articoli: 

- [Importare o esportare definizioni di riga di reporting finanziario](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions) o
- [Importare o esportare definizioni di colonna di reporting finanziario](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## Vedere anche

[Definizioni di riga nel reporting finanziario](bi-row-definitions.md)  
[Definizioni di colonna nel reporting finanziario](bi-column-definitions.md)  
[Eseguire e stampare i report](ui-work-report.md)  
[Business Intelligence finanziario](bi.md)  
[Dati finanziari](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
