---
title: Analizzare i dati negli elenchi con Copilot (anteprima)
description: Scopri come utilizzare Copilot in Business Central per analizzare i dati.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-data-in-lists-with-help-from-copilot-preview"></a>Analizzare i dati negli elenchi con Copilot (anteprima)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Questo articolo spiega come utilizzare l'*assistenza all'analisi* per analizzare i dati nelle pagine di elenco.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-analysis-assist"></a>Informazioni sull'assistenza all'analisi

L'assistenza all'analisi è un copilota per la [modalità di analisi](analysis-mode.md) nelle pagine di elenco in Business Central. La modalità di analisi fornisce un modo interattivo e versatile per calcolare, riassumere ed esaminare i dati. Per analizzare i dati nella modalità di analisi, crei una scheda *analisi* in cui trasformi i dati per visualizzare le aggregazioni e i riepiloghi desiderati. Ad esempio, puoi organizzare i campi in righe e colonne, specificare filtri, ordinare colonne ed eseguire il pivot nei campi. Con l'assistenza all'analisi, invece di svolgere questa attività manualmente, ottieni più o meno lo stesso, o almeno inizialmente, utilizzando parole. Esprimendo la struttura desiderata in linguaggio naturale, ad esempio "ordina in base alla quantità dal più piccolo al più grande" o "mostra il costo medio per categoria", l'assistenza all'analisi utilizza l'intelligenza artificiale per generare un layout suggerito in una scheda di analisi.

## <a name="available-languages"></a>Lingue disponibili

[!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

## <a name="prerequisites"></a>Prerequisiti

- La funzionalità di assistenza all'analisi è attivata e ti vengono concesse le autorizzazioni per utilizzarla. Questa attività viene in genere eseguita da un amministratore. [Vedi qui per ulteriori informazioni sulla configurazione delle funzionalità di Copilot e IA](enable-ai.md).
<!-- - The display language in Business Central is set to one the following English locales: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Learn how to change the language](ui-change-basic-settings.md#language)-->
<!-- - Your Business Central environment is in any country/region except Canada (this feature isn't yet available in Canada).-->

## <a name="get-started"></a>Introduzione

1. Apri la pagina di elenco da analizzare.

   Ad esempio, per utilizzare la pagina **Articoli**, seleziona l'icona ![Lente di ingrandimento che apre la funzionalità Dimmi.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), immetti *Articoli*, quindi scegli il collegamento correlato.

1. Puoi iniziare ad analizzare i dati con Copilot direttamente dalla pagina di elenco o accedendo prima alla modalità di analisi. Per iniziare, esegui uno dei passaggi seguenti:

    - Nella barra delle azioni nella parte superiore della pagina, seleziona ![Mostra l'icona del copilota](media/copilot-icon.png) **Copilot** > **Analizza lista**.
    - Nella barra delle azioni nella parte superiore della pagina, seleziona ![Mostra l'icona di accesso alla modalità di analisi](media/analysis-mode-icon.png) **Entra in modalità analisi**, quindi seleziona ![Mostra l'icona del copilota](media/copilot-icon.png) **Copilot** > **Crea nuova analisi**.

1. Nella finestra **Analizza articoli** con Copilot, immetti una descrizione del layout che desideri. Questa descrizione è nota come *prompt*.

    ![Mostra l'assistenza all'analisi Copilot](media/analysis-assist.png)

    > [!TIP]
    > Per assistenza nella scrittura di un prompt, seleziona ![Mostra l'icona del prompt di visualizzazione](media/prompt-guide-icon.png) **Guida rapida** e scegli una delle opzioni per iniziare. Il testo tra parentesi `[ ]` viene mostrato solo come esempio e non è incluso nella finestra Copilot.

1. Seleziona **Genera** quindi attendi che Copilot generi il layout nella nuova scheda di analisi.
1. Esamina i risultati nella nuova scheda di analisi.

   > [!NOTE]
   > Se esci dalla nuova scheda di analisi (ad esempio passi a un'altra scheda o pagina di analisi) o se apporti modifiche al layout nella scheda (ad esempio l'ordinamento delle colonne o la modifica delle impostazioni nelle schede **Colonne** e **Filtri analisi**), la nuova scheda di analisi viene salvata automaticamente e Copilot si chiude.

1. Se desideri modificare l'analisi generata, puoi eseguire uno di questi passaggi:

   - Per basarti sulle istruzioni precedenti, inserisci le informazioni nella casella **Aggiungi ulteriori dettagli sull'analisi**, quindi seleziona la freccia ![Mostra la freccia di regolazione](media/analysis-assist-adjust-button.png) **Regola**. Copilot ricorda le istruzioni precedenti e le utilizza per effettuare modifiche.

   - Per iniziare da zero aggiungendo nuove istruzioni, seleziona l'icona ![Mostra l'icona matita di modifica del prompt](media/edit-pencil.png) **Modifica prompt:**, aggiungi i dettagli al prompt e quindi seleziona **Genera**.

1. Se vuoi salvare la scheda di analisi, seleziona **Mantieni**. Se non la vuoi salvare, seleziona **Elimina**.

## <a name="prompt-tips-and-examples"></a>Suggerimenti ed esempi di prompt

La creazione di prompt efficaci per Copilot è essenziale per ottenere suggerimenti di analisi accurati e pertinenti. Esistono anche modi per ridurre al minimo il testo che aggiungi nei prompt per rendere più veloce la digitazione. Ecco alcuni suggerimenti e linee guida seguiti da alcuni esempi:

- Sii conciso ed evita frasi lunghe o multiple.
- Assicurati che i nomi dei campi utilizzati nei prompt siano in qualche modo vicini ai nomi dei campi effettivi nella pagina.
- Utilizza il linguaggio naturale, esprimendo la struttura dei dati che desideri in modo amichevole e colloquiale.
- Utilizza parole chiave, frasi e termini comuni utilizzati nell'analisi dei dati, come `group by`, `sum`, `sort by` e così via.
- Se la risposta iniziale non è quella desiderata, aggiungi istruzioni successive o riformula l'ultima istruzione.
- Sono consentite abbreviazioni comuni.
- L'uso di maiuscolo e/o minuscolo non è importante.

### <a name="examples"></a>Esempi

I seguenti esempi di prompt utilizzano l'assistenza all'analisi nell'elenco **Articoli**. La pagina degli articoli include tre campi sommabili per l'analisi: **Giacenza**, **Costo unitario**, **Prezzo unitario**.

Prompt: `Show items by brand and unit of measure`

Questo prompt tenta di mostrare i totali per tutti i campi sommabili, raggruppati per marca e campo **Unità di misura base**. Ma in questo caso, "marca" non corrisponde ad alcun nome di campo, quindi Copilot probabilmente non riesce a trovare un campo corrispondente. Quindi chiede di riformulare il prompt e riprovare.

Prompt: `Show items by type and uom`

Questo prompt tenta mostra i totali per tutti i campi sommabili, raggruppati per campo **Tipo** e **Unità di misura base**. Ma invece di scrivere "unità di misura", viene utilizzata l'abbreviazione `uom`.

Prompt: `Show total quantity per type per UoM`

Questo prompt crea una tabella pivot nel campo **Giacenza** per **Unità di misura base** per **Tipo**.

## <a name="see-also"></a>Vedere anche

[Domande frequenti sull'intelligenza artificiale responsabile per l'assistenza all'analisi](faqs-analysis-assist.md)  
[Analisi dei dati ad hoc](reports-adhoc-analysis.md)  
