---
title: Analizzare i dati nelle pagine elenco utilizzando la modalità di analisi dei dati
description: Informazioni su come utilizzare la modalità di analisi dei dati in Business Central per analizzare i dati.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/30/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-data-using-data-analysis-mode"></a><a name="analyze-list-data-using-data-analysis-mode"></a><a name="analyze-list-data-using-data-analysis-mode"></a>Analizzare i dati di elenco utilizzando la modalità di analisi dei dati

In questo articolo imparerai come analizzare i dati dalle pagine di elenco utilizzando la *modalità di analisi dei dati*. La modalità di analisi dei dati consente di analizzare i dati direttamente dalla pagina, senza dover eseguire un report o passare a un'altra applicazione come Excel. Fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri diversi, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Esempi potrebbero essere "I miei clienti", "Articoli di follow-up", "Fornitori aggiunti di recente", "Statistiche di vendita" o qualsiasi altra visualizzazione che puoi immaginare.

> [!TIP]
> Un aspetto positivo della modalità di analisi dei dati è che non modifica nessuno dei dati sottostanti della pagina elenco o il layout della pagina quando non è in modalità di analisi dei dati. Quindi il modo migliore per scoprire cosa puoi fare nella modalità di analisi dei dati è provare a usarla.

## <a name="prerequisite"></a><a name="prerequisite"></a><a name="prerequisite"></a>Prerequisiti

La modalità di analisi dei dati è attualmente in anteprima, il che significa che un amministratore deve attivarla prima che tu possa utilizzarla. Se sei un amministratore e desideri attivare la modalità di analisi dei dati, vai alla pagina **Gestione funzionalità** e abilita **Aggiornamento della funzionalità: modalità di analisi, analisi rapida dei dati direttamente in Business Central**. Per ulteriori informazioni sull'attivazione e sulla disattivazione delle funzionalità, vai a [Gestione delle funzionalità](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="get-started"></a><a name="get-started"></a><a name="get-started"></a>Introduzione

1. Apri la pagina elenco.

   Ad esempio, per lavorare con **Movimenti contabili clienti**, seleziona l'icona ![Lente di ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), immetti *movimenti contabili clienti*, quindi scegli il collegamento correlato.  
2. Nella barra delle azioni nella parte superiore della pagina, attiva l'interruttore **Analizza**.

    La modalità di analisi dei dati apre i dati in un'esperienza ottimizzata per l'analisi dei dati.  In modalità di analisi dei dati, la normale barra delle azioni viene sostituita da una speciale barra della modalità di analisi dei dati. La figura seguente illustra le diverse aree di una pagina nella modalità di analisi dei dati.

   [![Mostra una panoramica di una pagina nella modalità di analisi dei dati](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Ogni area è spiegata nelle sezioni che seguono.

3. Usa le diverse aree per manipolare, riassumere e analizzare i dati. Per i dettagli vedi le sezioni seguenti.

4. Quando vuoi uscire dalla modalità di analisi, disattiva l'interruttore **Analizza**.

   Le schede di analisi che hai aggiunto rimangono fino a quando non le elimini. Quindi, se torni di nuovo alla modalità di analisi dei dati, le vedrai esattamente come le avevi lasciate.

> [!NOTE]
> I dati mostrati in modalità di analisi sono controllati dai filtri o dalle viste impostati nella pagina elenco. Ciò ti consente di prefiltrare i dati prima di accedere alla modalità di analisi.

## <a name="work-with-data-analysis-mode"></a><a name="work-with-data-analysis-mode"></a><a name="work-with-data-analysis-mode"></a>Lavorare con la modalità di analisi dei dati

Nella modalità di analisi dei dati, la pagina è divisa in due aree:

- L'area principale, costituita dall'area dati (1), dalla barra di riepilogo (2) e dalla barra delle schede (5)
- L'area di manipolazione dei dati, composta da due riquadri: colonne (3) e filtri di analisi (4).

### <a name="data-area-1"></a><a name="data-area-1"></a><a name="data-area-1"></a>Area dati (1)

L'area dati è il punto in cui vengono visualizzate le righe e le colonne della pagina elenco e i dati vengono riepilogati. L'area dati fornisce un modo versatile per controllare il layout delle colonne e un modo rapido per ottenere un riepilogo dei dati. Per le colonne che contengono valori numerici, la somma di tutti i valori della colonna viene visualizzata nell'ultima riga, a meno che non siano stati definiti gruppi di righe. In questo caso, le somme vengono visualizzate come subtotale per i gruppi.  

![Mostra una panoramica di un'area dati in una pagina nella modalità di analisi dei dati](media/analysis-mode-data-area.png)

- Per spostare una colonna, selezionala e trascinala dove ha più senso nella tua analisi.
- Fai clic con il pulsante destro del mouse sulla colonna o passaci sopra con il mouse e seleziona l'icona del menu ![Mostra l'icona su una colonna in modalità di analisi dei dati che apre un menu di azioni](media/analysis-mode-column-menu-icon.png) per accedere a diverse azioni che puoi eseguire sulle colonne. Ad esempio:

  - Per aggiungere una colonna a sinistra o a destra dell'area dati in modo che non sia fuori dallo schermo durante lo scorrimento, seleziona ![Mostra l'icona su una colonna in modalità analisi dati che apre un menu di azioni](media/analysis-mode-column-menu-icon.png) > **Aggiungi colonna** > **Aggiungi a sinistra** la parte della colonna.
  - Definisci i filtri di dati direttamente nella definizione della colonna invece di accedere ai riquadri **Filtri di analisi**. Puoi ancora esaminare i dettagli sui dati correlati e per ogni riga e aprire la scheda per altre informazioni su una determinata entità.
- Utilizza l'area dati per interagire con i dati. Per le colonne che contengono valori numerici sommabili, puoi ottenere statistiche descrittive su un set di campi contrassegnandoli. Le statistiche vengono visualizzate nella barra di stato (2) nella parte inferiore della pagina.
- Esporta i dati in formato Excel o csv. È sufficiente fare clic con il pulsante destro del mouse sull'area dati o su una selezione di celle da esportare.

### <a name="summary-bar-2"></a><a name="summary-bar-2"></a><a name="summary-bar-2"></a>Barra di riepilogo (2)

La barra di riepilogo si trova nella parte inferiore della pagina e visualizza le statistiche sui dati nell'elenco. Man mano che interagisci con le colonne i cui valori possono essere sommati, ad esempio selezionando più righe in una colonna che visualizza gli importi, i dati verranno aggiornati.

![Mostra una panoramica di una barra di riepilogo nella modalità di analisi dei dati](media/analysis-mode-totals-row.png)

La tabella seguente descrive i diversi numeri visualizzati nell'area dei totali:

|Numero|Descrizione|
|-|-|
|Righe|Il numero di righe selezionate come parte del numero totale di righe disponibili. |
|Righe totali|Il numero di righe nell'elenco non filtrato.|
|Filtrato|Il numero di righe visualizzate come risultato dei filtri applicati all'elenco.|
|Media|Il valore medio in tutti i campi sommabili selezionati.|
|Conteggio|Il numero di righe selezionate.|
|Minimo|Il valore minimo in tutti i campi sommabili selezionati.|
|Massimo|Il valore massimo in tutti i campi sommabili selezionati.|
|Somma|La somma totale di tutti i valori nei campi sommabili selezionati.|

### <a name="columns-3"></a><a name="columns-3"></a><a name="columns-3"></a>Colonne (3)

L'area **Colonne** è uno dei due riquadri che usi per definire la tua analisi. L'altra area è il riquadro **Filtri di analisi**. Il riquadro **Colonne** viene utilizzato per riepilogare i dati. Utilizza il riquadro **Colonne** per definire quali colonne devono essere incluse nell'analisi.

![Mostra una panoramica del riquadro colonne nella modalità di analisi dei dati](media/analysis-mode-columns-2.png)

|Aree|Descrizione|
|-|-|
|Cerca/seleziona o deseleziona tutte le caselle|Ricerca di colonne. Seleziona la casella di controllo per selezionare/deselezionare tutte le colonne.|
|Caselle di controllo|Quest'area include una casella di controllo per ogni campo nella tabella di origine dell'elenco. Utilizza quest'area per modificare le colonne visualizzate nell'elenco. Seleziona una casella di controllo per mostrare la colonna per il campo sulla pagina; deseleziona la casella di controllo per nascondere la colonna. |
|Gruppi di righe|Utilizza quest'area per raggruppare e sommare i dati in base a uno o più campi. Puoi includere solo campi non numerici, come campi di testo, data e ora. I gruppi di righe vengono utilizzati spesso in modalità pivot.|
|Valori|Utilizza quest'area per specificare i campi per i quali vuoi una somma totale. Puoi includere solo campi che contengono numeri che possono essere sommati; ad esempio, non campi di testo, data o ora.|

Per spostare un campo da un'area all'altra, seleziona l'icona per afferrare ![Mostra una panoramica di una pagina nella modalità di analisi](media/column-grab-icon.png) accanto alla colonna nell'elenco precedente e trascina nell'area di destinazione. Ti viene impedito di spostare un campo in un'area in cui non è consentito.

### <a name="analysis-filters-4"></a><a name="analysis-filters-4"></a><a name="analysis-filters-4"></a>Filtri analisi (4)

Il riquadro **Filtri analisi** consente di impostare ulteriori filtri di dati sulle colonne per limitare le voci nell'elenco. Imposta i filtri sulle colonne per limitare le voci nell'elenco e le successive somme solo per le voci che ti interessano in base a criteri da te definiti. Ad esempio, supponi di essere interessato solo ai dati per un cliente specifico o agli ordini di vendita che superano un importo specifico. Per impostare un filtro, seleziona la colonna, scegli l'operazione di confronto dall'elenco (come **Uguale a** o **Inizia con**), quindi inserisci il valore.

![Mostra una panoramica del riquadro filtri nella modalità di analisi](media/analysis-mode-filters.png)

> [!NOTE]
> I filtri aggiuntivi si applicano solo alla scheda di analisi corrente. Ciò consente di definire esattamente i filtri di dati aggiuntivi necessari per un'analisi specifica.

### <a name="tabs-5"></a><a name="tabs-5"></a><a name="tabs-5"></a>Schede (5)

L'area delle schede in alto ti consente di creare diverse configurazioni (colonne e filtri di analisi) su schede separate, dove puoi manipolare i dati nelle schede indipendentemente l'una dall'altra. C'è sempre almeno una scheda, chiamata **Analisi 1** per impostazione predefinita. L'aggiunta di più schede è utile per salvare le configurazioni di analisi utilizzate di frequente su un set di dati. Ad esempio, potresti avere schede per l'analisi dei dati in modalità pivot e altre schede che filtrano un sottoinsieme di righe. Alcune schede possono mostrare una visualizzazione dettagliata con molte colonne, mentre altre mostrano solo alcune colonne chiave.

Ecco alcuni suggerimenti su come lavorare con più schede di analisi:

- Per aggiungere una nuova scheda, seleziona il segno **+** grande accanto all'ultima scheda di analisi.
- Seleziona la freccia rivolta verso il basso su una scheda per accedere a un elenco di azioni che puoi eseguire su una scheda, come rinominare, duplicare, eliminare e spostare.

   - **Elimina** elimina la scheda attualmente aperta. **Elimina tutto** elimina tutte le schede che hai aggiunto, tranne la scheda predefinita **Analisi 1**.
- Non puoi rimuovere completamente la scheda **Analisi 1**, ma puoi rinominarla utilizzando l'azione **Rinomina** e cancellare le modifiche apportate utilizzando **Elimina** o **Elimina tutto**.  

- Le schede di analisi che hai aggiunto e configurato rimangono fino a quando non le elimini. Quindi, se torni di nuovo alla modalità di analisi dei dati, le vedrai esattamente come le avevi lasciate.

   > [!TIP]
   > Le schede che hai impostato sono visibili solo a te. Gli altri utenti vedranno solo le schede che hanno configurato.
- Puoi copiare le schede di analisi. La copia può essere utile se vuoi sperimentare la modifica di una scheda senza modificare l'originale o per creare diverse varianti della stessa analisi.

## <a name="pivot-mode"></a><a name="pivot-mode"></a><a name="pivot-mode"></a>Modalità pivot

È possibile utilizzare la modalità pivot per analizzare grandi quantità di dati numerici, e fare un subtotale dei dati per categorie e sottocategorie. La modalità pivot è equivalente alle [tabelle pivot in Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Per attivare e disattivare la modalità pivot, fai scorrere l'interruttore **Modalità pivot** nel riquadro **Colonne** (3). Quando attivi la modalità pivot, nel riquadro viene visualizzata l'area **Etichette colonna**. Utilizza l'area **Etichette colonna** per raggruppare i totali della somma per le righe in categorie. I campi che aggiungi all'area **Etichette colonna** verranno visualizzati come colonne nell'area dati (1).

La creazione dell'analisi dei dati in modalità pivot comporta lo spostamento dei campi nelle tre aree: **Gruppi di righe**, **Etichette colonne**, e **Valori**. La figura seguente illustra dove i campi vengono mappati all'area dati (1), dove `sum` sono i dati calcolati e, facoltativamente, **Valori**.

<table>
<tr><th></th><th>Etichetta colonna</th><th></th><th>Etichetta colonna</th><th></th></tr>
<tr><th>Gruppo di righe</th><th>Valore</th><th>Valore</th><th>Valore</th><th>Valore</th></tr>
<tr><td>riga</td><td>somma</td><td>somma</td><td>somma</td><td>somma</td></tr>
<tr><td>riga</td><td>somma</td><td>somma</td><td>somma</td><td>somma</td></tr>
<tr><td>riga</td><td>somma</td><td>somma</td><td>somma</td><td>somma</td></tr>
<tr><td>riga</td><td>somma</td><td>somma</td><td>somma</td><td>somma</td></tr>
</table>

> [!TIP]
> Le colonne che hanno solo pochi valori possibili sono i migliori candidati per l'utilizzo nella colonna **Valori**.

## <a name="limitations"></a><a name="limitations"></a><a name="limitations"></a>Limiti

La vista analisi ha attualmente un limite di 100.000 righe. Se superi questo limite, riceverai un messaggio di avviso. Per aggirare questa limitazione, imposta i filtri sulla pagina prima di passare alla modalità di analisi dei dati, se possibile.  Potresti analizzare un determinato gruppo di clienti o solo i dati dell'anno in corso. Puoi anche scegliere una vista predefinita se funziona per la tua analisi.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Analisi dei dati ad hoc](reports-adhoc-analysis.md)  
[Visualizza e modifica in Excel](across-work-with-excel.md)  
