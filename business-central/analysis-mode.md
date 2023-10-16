---
title: Analizzare i dati nelle pagine elenco e nelle query utilizzando la modalità di analisi dei dati
description: Informazioni su come utilizzare la modalità di analisi dei dati in Business Central per analizzare i dati.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/05/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Analizzare la pagina elenco e dati di query utilizzando la modalità di analisi dei dati

> **SI APPLICA A:** Anteprima pubblica nel primo ciclo di rilascio di Business Central 2023 e successive per l'analisi delle pagine elenco; Disponibile a livello generale nel secondo ciclo di rilascio di Business Central 2023 per l'analisi dei dati dalle pagine elenco e dalle query.

In questo articolo apprenderai come analizzare i dati delle pagine elenco e delle query utilizzando la *modalità di analisi dei dati*. La modalità di analisi dei dati consente di analizzare i dati direttamente dalla pagina, senza dover eseguire un report o passare a un'altra applicazione come Excel. Fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Invece di eseguire i report utilizzando opzioni e filtri diversi, puoi aggiungere più schede che rappresentano attività o viste diverse sui dati. Esempi potrebbero essere "I miei clienti", "Articoli di follow-up", "Fornitori aggiunti di recente", "Statistiche di vendita" o qualsiasi altra visualizzazione che puoi immaginare.

> [!TIP]
> Un aspetto positivo della modalità di analisi dei dati è che non modifica nessuno dei dati sottostanti della pagina elenco o della query o il layout della pagina o della query quando non è in modalità di analisi dei dati. Quindi il modo migliore per scoprire cosa puoi fare nella modalità di analisi dei dati è provare a usarla.

## Prerequisiti 

- Se utilizzi Business Central versione 22, la modalità di analisi dei dati è in anteprima. Pertanto, un amministratore deve abilitarlo per poterlo utilizzare. Per abilitarla, vai alla pagina **Gestione funzionalità** e abilita **Aggiornamento della funzionalità: modalità di analisi, analisi rapida dei dati direttamente in Business Central**. [Ulteriori informazioni su Gestione funzionalità](/dynamics365/business-central/dev-itpro/administration/feature-management).
- Nella versione 23 e successive, al tuo account deve essere assegnato il set di autorizzazioni **DATA ANALYSIS - EXEC** o includere l'autorizzazione di esecuzione sull'oggetto di sistema **9640 Consenti modalità di analisi dati**. In qualità di amministratore, puoi escludere queste autorizzazioni per gli utenti a cui non desideri concedere l'accesso alla modalità di analisi.

> [!NOTE]
> Potresti notare che alcune pagine elenco non includono l'interruttore **Analizza** per passare alla modalità di analisi. Il motivo è che gli sviluppatori possono disabilitare la modalità di analisi in pagine specifiche utilizzando la [proprietà AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) in AL.

## Introduzione

1. Apri la pagina elenco o la query.

   Ad esempio, per utilizzare la pagina **Movimenti contabili clienti**, seleziona l'icona ![Lente di ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), immetti *movimenti contabili clienti*, quindi scegli il collegamento correlato. 

2. Nella barra delle azioni nella parte superiore della pagina, attiva l'interruttore **Analizza**.

    La modalità di analisi dei dati apre i dati in un'esperienza ottimizzata per l'analisi dei dati.  In modalità di analisi dei dati, la normale barra delle azioni viene sostituita da una speciale barra della modalità di analisi dei dati. La figura seguente illustra le diverse aree di una pagina nella modalità di analisi dei dati.

   [![Mostra una panoramica di una pagina nella modalità di analisi dei dati](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Ogni area è spiegata nelle sezioni che seguono.

3. Usa le diverse aree per manipolare, riassumere e analizzare i dati. Per i dettagli vedi le sezioni seguenti.

4. Quando vuoi uscire dalla modalità di analisi, disattiva l'interruttore **Analizza**.

   Le schede di analisi che hai aggiunto rimangono fino a quando non le elimini. Quindi, se torni di nuovo alla modalità di analisi dei dati, le vedi esattamente come le avevi lasciate.

> [!NOTE]
> I dati mostrati in modalità di analisi sono controllati dai filtri o dalle viste impostati nella pagina elenco. Ciò ti consente di prefiltrare i dati prima di accedere alla modalità di analisi.

## Lavorare con la modalità di analisi dei dati

Nella modalità di analisi dei dati, la pagina è divisa in due aree:

- L'area principale, costituita dall'area dati (1), dalla barra di riepilogo (2) e dalla barra delle schede (5)
- L'area di manipolazione dei dati, composta da due riquadri: colonne (3) e filtri di analisi (4).

### Area dati (1)

L'area dati è il punto in cui vengono visualizzate le righe e le colonne della pagina elenco o della query e i dati vengono riepilogati. L'area dati fornisce un modo versatile per controllare il layout delle colonne e un modo rapido per ottenere un riepilogo dei dati. Per le colonne che contengono valori numerici, la somma di tutti i valori della colonna viene visualizzata nell'ultima riga, a meno che non siano stati definiti gruppi di righe. In questo caso, le somme vengono visualizzate come subtotale per i gruppi.  

![Mostra una panoramica di un'area dati in una pagina nella modalità di analisi dei dati](media/analysis-mode-data-area.png)

- Per spostare una colonna, selezionala e trascinala dove ha più senso nella tua analisi.
- Fai clic con il pulsante destro del mouse sulla colonna o passaci sopra con il mouse e seleziona l'icona del menu ![Mostra l'icona su una colonna in modalità di analisi dei dati che apre un menu di azioni](media/analysis-mode-column-menu-icon.png) per accedere a diverse azioni che puoi eseguire sulle colonne. Ad esempio:

  - Per aggiungere una colonna a sinistra o a destra dell'area dati in modo che non sia fuori dallo schermo durante lo scorrimento, seleziona ![Mostra l'icona su una colonna in modalità analisi dati che apre un menu di azioni](media/analysis-mode-column-menu-icon.png) > **Aggiungi colonna** > **Aggiungi a sinistra** la parte della colonna.
  - Definisci i filtri di dati direttamente nella definizione della colonna invece di accedere ai riquadri **Filtri di analisi**. Puoi ancora esaminare i dettagli sui dati correlati e per ogni riga e aprire la scheda per altre informazioni su una determinata entità.
- Utilizza l'area dati per interagire con i dati. Per le colonne che contengono valori numerici sommabili, puoi ottenere statistiche descrittive su un set di campi contrassegnandoli. Le statistiche vengono visualizzate nella barra di stato (2) nella parte inferiore della pagina.
- Esporta i dati in formato Excel o csv. Fai clic con il pulsante destro del mouse sull'area dati o su una selezione di celle da esportare.

### Barra di riepilogo (2)

La barra di riepilogo si trova nella parte inferiore della pagina e visualizza le statistiche sui dati nella pagina elenco o nella query. Man mano che interagisci con le colonne i cui valori possono essere sommati, ad esempio selezionando più righe in una colonna che visualizza gli importi, i dati si aggiornano.

![Mostra una panoramica di una barra di riepilogo nella modalità di analisi dei dati](media/analysis-mode-totals-row.png)

La tabella seguente descrive i diversi numeri visualizzati nell'area dei totali:

|Numero|Descrizione|
|-|-|
|Righe|Il numero di righe selezionate come parte del numero totale di righe disponibili. |
|Righe totali|Il numero di righe nella query o nell'elenco non filtrato.|
|Filtrato|Il numero di righe visualizzate come risultato dei filtri applicati all'elenco o alla query.|
|Media|Il valore medio in tutti i campi sommabili selezionati.|
|Conteggio|Il numero di righe selezionate.|
|Minimo|Il valore minimo in tutti i campi sommabili selezionati.|
|Massimo|Il valore massimo in tutti i campi sommabili selezionati.|
|Somma|La somma totale di tutti i valori nei campi sommabili selezionati.|

### Colonne (3)

L'area **Colonne** è uno dei due riquadri che usi per definire la tua analisi. L'altra area è il riquadro **Filtri di analisi**. Il riquadro **Colonne** viene utilizzato per riepilogare i dati. Utilizza il riquadro **Colonne** per definire quali colonne devono essere incluse nell'analisi.

![Mostra una panoramica del riquadro colonne nella modalità di analisi dei dati](media/analysis-mode-columns-2.png)

|Aree|Descrizione|
|-|-|
|Cerca/seleziona o deseleziona tutte le caselle|Ricerca di colonne. Seleziona la casella di controllo per selezionare/deselezionare tutte le colonne.|
|Caselle di controllo|Quest'area include una casella di controllo per ogni campo nella tabella di origine dell'elenco o della query. Utilizza quest'area per modificare le colonne visualizzate. Seleziona una casella di controllo per mostrare la colonna per il campo sulla pagina; deseleziona la casella di controllo per nascondere la colonna. |
|Gruppi di righe|Utilizza quest'area per raggruppare e sommare i dati in base a uno o più campi. Puoi includere solo campi non numerici, come campi di testo, data e ora. I gruppi di righe vengono utilizzati spesso in modalità pivot.|
|Valori|Utilizza quest'area per specificare i campi per i quali vuoi una somma totale. Puoi includere solo campi che contengono numeri che possono essere sommati; ad esempio, non campi di testo, data o ora.|

Per spostare un campo da un'area all'altra, seleziona l'icona per afferrare ![Mostra una panoramica di una pagina nella modalità di analisi](media/column-grab-icon.png) accanto alla colonna nell'elenco e trascina nell'area di destinazione. Ti viene impedito di spostare un campo in un'area in cui non è consentito.

### Filtri analisi (4)

Il riquadro **Filtri analisi** consente di impostare ulteriori filtri di dati sulle colonne per limitare le voci nell'elenco. Imposta i filtri sulle colonne per limitare le voci nell'elenco e le successive somme solo per le voci che ti interessano in base a criteri da te definiti. Ad esempio, supponi di essere interessato solo ai dati per un cliente specifico o agli ordini di vendita che superano un importo specifico. Per impostare un filtro, seleziona la colonna, scegli l'operazione di confronto dall'elenco (come **Uguale a** o **Inizia con**), quindi inserisci il valore.

![Mostra una panoramica del riquadro filtri nella modalità di analisi](media/analysis-mode-filters.png)

> [!NOTE]
> I filtri aggiuntivi si applicano solo alla scheda di analisi corrente. Ciò consente di definire esattamente i filtri di dati aggiuntivi necessari per un'analisi specifica.

### Schede (5)

L'area delle schede in alto ti consente di creare diverse configurazioni (colonne e filtri di analisi) su schede separate, dove puoi manipolare i dati nelle schede indipendentemente l'una dall'altra. C'è sempre almeno una scheda, chiamata **Analisi 1** per impostazione predefinita. L'aggiunta di più schede è utile per salvare le configurazioni di analisi utilizzate di frequente su un set di dati. Ad esempio, potresti avere schede per l'analisi dei dati in modalità pivot e altre schede che filtrano un sottoinsieme di righe. Alcune schede possono mostrare una visualizzazione dettagliata con molte colonne, mentre altre mostrano solo alcune colonne chiave.

Ecco alcuni suggerimenti su come lavorare con più schede di analisi:

- Per aggiungere una nuova scheda, seleziona il segno **+** grande accanto all'ultima scheda di analisi.
- Seleziona la freccia rivolta verso il basso su una scheda per accedere a un elenco di azioni che puoi eseguire su una scheda, come rinominare, duplicare, eliminare e spostare.

   - **Elimina** elimina la scheda attualmente aperta. **Elimina tutto** elimina tutte le schede che hai aggiunto, tranne la scheda predefinita **Analisi 1**.
- Non puoi rimuovere completamente la scheda **Analisi 1**, ma puoi rinominarla utilizzando l'azione **Rinomina** e cancellare le modifiche apportate utilizzando **Elimina** o **Elimina tutto**.  

- Le schede di analisi che hai aggiunto e configurato rimangono fino a quando non le elimini. Quindi, se torni di nuovo alla modalità di analisi dei dati, le vedi esattamente come le avevi lasciate.

   > [!TIP]
   > Le schede che hai impostato sono visibili solo a te. Gli altri utenti vedranno solo le schede che hanno configurato.
- Puoi copiare le schede di analisi. La copia può essere utile se vuoi sperimentare la modifica di una scheda senza modificare l'originale o per creare diverse varianti della stessa analisi.


## Gerarchie di date

In modalità analisi, i campi data del set di dati vengono generati in una gerarchia anno-trimestre-mese di tre campi separati. Questa gerarchia si basa sul calendario normale e non sui calendari fiscali definiti in Business Central.

I campi aggiuntivi sono denominati _\<field name\> Anno_, _\<field name\> Trimestre_ e _\<field name\> Mese_. Ad esempio, se il set di dati include un campo denominato _Data di registrazione_, la gerarchia di date corrispondente è composta da campi chiamati _Anno data di registrazione_, _Trimestre data di registrazione_ e _Mese data di registrazione_.

> [!NOTE]
> La gerarchia delle date attualmente si applica solo ai campi di tipo data, non ai campi di tipo datetime.

## Modalità pivot

È possibile utilizzare la modalità pivot per analizzare grandi quantità di dati numerici, e fare un subtotale dei dati per categorie e sottocategorie. La modalità pivot è equivalente alle [tabelle pivot in Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Per attivare e disattivare la modalità pivot, fai scorrere l'interruttore **Modalità pivot** nel riquadro **Colonne** (3). Quando attivi la modalità pivot, nel riquadro viene visualizzata l'area **Etichette colonna**. Utilizza l'area **Etichette colonna** per raggruppare i totali della somma per le righe in categorie. I campi che aggiungi all'area **Etichette colonna** sono visualizzati come colonne nell'area dati (1).

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


## Analizzare grandi quantità di dati

Se il set di dati che desideri analizzare supera le 100.000 righe, ti consigliamo di accedere a una modalità di analisi ottimizzata per set di dati di grandi dimensioni. Attualmente vi sono due limitazioni se passi a questa modalità: 

- La formattazione dei campi dei seguenti quattro tipi di dati potrebbe cambiare: 

   - valuta 
   - decimali (mostrati sempre con due decimali) 
   - date (visualizzate sempre nel formato AAAA-MM-GG)
   - fusi orari
- I campi utilizzati in modalità pivot e aggiunti alle etichette delle colonne devono avere un numero basso di valori distinti.

   Se abiliti la modalità pivot e trascini un campo nell'area **Etichette colonna**, dove i dati sottostanti per quel campo hanno troppi valori distinti, la scheda del browser potrebbe non rispondere e alla fine si chiude, richiedendo di ricominciare da capo in una nuova sessione. In questo caso, non abilitare la modalità pivot per quel campo o applica un filtro al campo prima di aggiungerlo all'area **Etichette colonna**.

## Condividere l'analisi dei dati

Dopo aver preparato un'analisi in una scheda, puoi condividerla come collegamento con colleghi e altri utenti della tua organizzazione direttamente dal client. Solo i destinatari che sono autorizzati ad accedere alla società e ai dati possono utilizzare il collegamento.

1. Nella scheda dell'analisi, seleziona la freccia rivolta verso il basso, quindi seleziona **Copia collegamento**.

   ![Azione per copiare un'analisi](media/copy-analysis.svg)

   Si apre la finestra di dialogo **Collega a \<tab name\>**.

1. Per impostazione predefinita, l'analisi che condividi si collegherà alla pagina o alla query della società in cui lavori attualmente, indicata da `company=<company_name>` nel campo URL accanto al pulsante **Copia**. Se desideri inviare un collegamento a un'analisi non associata a una società specifica, imposta il campo **Società:** su **Non collegare a una società specifica**.

   ![Finestra di dialogo per la copia di un collegamento per una scheda di analisi](media/analysis-link-copied.svg)

1. Seleziona **Copia**.

1. Incolla il collegamento nel supporto di comunicazione di tua scelta, come Word, Outlook, Teams, OneNote e così via. 

2. Una volta ricevuto, i destinatari possono selezionare il collegamento e aprire l'analisi per la pagina o la query in Business Central. Ai destinatari viene richiesto di specificare un nome per la nuova scheda di analisi che verrà creata.  

## Limitazioni nel primo ciclo di rilascio del 2023 (anteprima)

L'anteprima pubblica di questa funzionalità presenta le seguenti limitazioni:

- La visualizzazione in modalità di analisi ha un limite di 100.000 righe. Se superi questo limite, riceverai un messaggio di avviso. Per aggirare questa limitazione, imposta i filtri sulla pagina prima di passare alla modalità di analisi, se possibile. Ad esempio, potresti voler analizzare un determinato gruppo di clienti o solo i dati dell'anno in corso. Puoi anche scegliere una vista predefinita se funziona per la tua analisi.
- La funzionalità di condivisione dell'analisi dei dati non è disponibile.
- La possibilità di salvare le scelte preferite per l'analisi dei dati nelle pagine elenco e di salvare i menu di analisi per scheda di analisi non è attualmente disponibile.

## Vedere anche

[Analisi dei dati ad hoc](reports-adhoc-analysis.md)  
[Visualizzare e modificare in Excel](across-work-with-excel.md)  
