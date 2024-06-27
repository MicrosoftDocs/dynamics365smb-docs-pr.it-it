---
title: Aggiungere del testo di marketing agli articoli
description: Scrivere un testo di marketing per gli articoli in Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="add-marketing-text-to-items"></a>Aggiungere del testo di marketing agli articoli

Per qualsiasi articolo registrato in Business Central, puoi scrivere un *testo di marketing* sull'articolo. Sebbene il testo di marketing sia una sorta di descrizione, è diverso da quello del campo **Descrizione** dell'articolo. Il campo **Descrizione** viene in genere utilizzato come nome visualizzato conciso per identificare rapidamente il prodotto. Il testo di marketing, invece, è un testo più ricco e descrittivo. Il suo scopo è aggiungere contenuti di marketing e promozionali, noti anche come *copia*. Questo testo può quindi essere pubblicato con l'articolo se è pubblicato in un negozio Web, come Shopify, o incollato in un'e-mail o altre comunicazioni con i tuoi clienti.

Il testo di marketing può essere creato in due modi: Il modo più semplice per iniziare è utilizzare Copilot, che suggerisce il testo generato dall'intelligenza artificiale. L'altro modo è cominciare da zero. 

## <a name="get-marketing-text-suggestions-with-copilot"></a><a name=copilot></a>Ottenere suggerimenti di testo di marketing con Copilot

Con Copilot, ricevi rapidamente un suggerimento di testo che viene generato automaticamente per te. Il testo generato dall'intelligenza artificiale è adattato all'articolo e fornisce un buon punto di partenza. Il testo si basa in parte sulle seguenti informazioni:

- Attributi definiti per l'articolo, ad esempio, la descrizione, il colore, le dimensioni, il materiale e così via. [Ulteriori informazioni sugli attributi degli articoli](inventory-how-work-item-attributes.md).
- Il campo **Descrizione** dell'articolo.
- La categoria dell'articolo. [Ulteriori informazioni sulla classificazione degli articoli](inventory-how-categorize-items.md).
- Le preferenze di stile selezionabili come tono della voce, formato e durata.

Copilot è progettato per farti risparmiare tempo e aiutarti a scrivere testi creativi e accattivanti che riflettano il tuo marchio e siano coerenti in tutta la tua linea di prodotti. Inizia generando un suggerimento, quindi modifica il testo suggerito secondo le tue necessità.

### <a name="available-languages"></a>Lingue disponibili

[!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

### <a name="prerequisites"></a>Prerequisiti

La funzionalità dei suggerimenti di testo di marketing è attivata nel tuo ambiente. Questa attività viene in genere eseguita da un amministratore. Per ulteriori informazioni, vai a [Configurare le funzionalità di Copilot e IA](enable-ai.md).

### <a name="create-first-draft-with-copilot"></a>Creare la prima bozza con Copilot

Completa i seguenti passaggi per aggiungere testo di marketing a un articolo esistente. Per informazioni su come creare un nuovo articolo, vedi [Registrare nuovi articoli](inventory-how-register-new-items.md).

1. In Business Central, apri l'articolo che vuoi modificare completando i seguenti passaggi:

   - Nell'angolo in alto a destra seleziona l'icona ![lampadina che apre la funzione Dimmi 22.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato per visualizzare l'elenco degli articoli disponibili.

   - Fai doppio clic sull'articolo o selezionane il valore nella colonna **Nr.** .

1. Dalla scheda articolo, ci sono due modi per iniziare a scrivere testo di marketing con Copilot: dal riquadro Dettaglio informazioni **Testo di marketing** o utilizzando l'azione **Testo di marketing**. Questi metodi sono indicati nella seguente figura di una scheda articolo.  

   [![Una scheda articolo con il riquadro Testo di marketing](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

   Per creare la prima bozza di un articolo, effettua una delle seguenti operazioni:

   - Nel riquadro **Testo di marketing** del riquadro Dettaglio informazioni sul lato destro della pagina seleziona **Bozza con Copilot**. 

     Copilot inizia a redigere una bozza del testo di marketing.

   - Nella parte superiore della pagina, seleziona l'azione **Testo di marketing**, quindi seleziona **Bozza con Copilot** nella finestra **Modifica testo marketing**.  Appare la finestra **Bozza di testo di marketing con Copilot**, che elenca tutti gli attributi disponibili per l'articolo.
1. Seleziona gli attributi su cui Copilot deve basare i suggerimenti, quindi seleziona **Genera**. Puoi modificare gli attributi selezionati e altre opzioni in un secondo momento. Copilot inizia a redigere una bozza del testo di marketing. 

   ![Finestra Modifica testo marketing](media/marketing-text-copilot-attributes.svg)

1. Quando Copilot completa la bozza, il testo appare nella finestra dell'editor di Copilot per la revisione e la modifica.

   [![Finestre Crea con Copilot](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Ora puoi ottenere più suggerimenti, provare a migliorare i suggerimenti ottenuti, modificare il testo e altro ancora. Vai a [Rivedere, modificare e salvare](#review-edit-and-save-text) per i dettagli.

### <a name="review-edit-and-save-text"></a>Rivedere, modificare e salvare il testo

Una volta che hai la prima bozza, devi rivederla e apportare le modifiche al testo per prepararla alla pubblicazione. Questo lavoro viene svolto dall'editor di Copilot, che ti consente di ottenere più suggerimenti, modificare le preferenze per influenzare i suggerimenti e apportare modifiche manuali al testo e allo stile del stesso.

> [!IMPORTANT]
> Il testo generato dall'intelligenza artificiale da Copilot è solo un suggerimento e può contenere errori. Richiede la supervisione e la revisione umana per garantire che sia accurato e appropriato. Esamina il testo suggerito e modifica se necessario prima di salvarlo e pubblicarlo per il consumo pubblico.

Utilizza le seguenti linee guida per finalizzare e salvare il testo di marketing.

1. Apporta le modifiche al testo direttamente nella casella di testo. Usa la barra degli strumenti lungo la parte inferiore della casella per formattare e definire lo stile del testo, aggiungere collegamenti e altro ancora.
2. Per ottenere un nuovo suggerimento, seleziona **Rigenera**.
3. Se non sei soddisfatto dei suggerimenti, migliorali utilizzando le opzioni **Tono**, **Formato** ed **Enfasi**.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Per le linee guida su come migliorare i suggerimenti, vai a [Migliorare e personalizzare i suggerimenti di testo](#improve-and-tailor-text-suggestions).

4. Per passare da un suggerimento all'altro, utilizza i collegamenti Precedente e Successivo nella parte superiore della pagina (*x* **di** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Esamina attentamente il testo per verificarne l'accuratezza e l'adeguatezza:

   - Se vuoi salvare il testo, seleziona **Conservalo**. 
   - Se non vuoi salvarlo, seleziona il pulsante Elimina (cestino) ![L'icona cestino per eliminare tutte le proposte di Copilot per la riconciliazione dei conti correnti bancari](media/copilot-delete-trash-can.png).

### <a name="improve-and-tailor-text-suggestions"></a>Migliorare e personalizzare i suggerimenti di testo

Ci sono alcuni passaggi che puoi fare per migliorare i suggerimenti di testo e modificarli in base alle tue preferenze personali o aziendali.

1. Modifica gli attributi dell'articolo utilizzati da Copilot.

   I suggerimenti di Copilot sono in parte basati sugli attributi assegnati all'articolo. Per visualizzare gli attributi disponibili e le impostazioni correnti, selezionare l'icona di modifica ![ Icona di modifica nella finestra di Copilot per modificare gli attributi](media/edit-pencil.png) nell'angolo in alto a sinistra. Nella pagina **Attributi articolo**, scegli gli attributi più appropriati per le caratteristiche che intendi promuovere. Più attributi pertinenti includi, migliore sarà il risultato. Se ritieni che ti manchino alcuni attributi chiave, aggiungine altri. Per ulteriori informazioni sugli attributi, vedi [Utilizzare gli attributi articolo](inventory-how-work-item-attributes.md)
1. Modifica le impostazioni per le opzioni **Tono**, **Formato** ed **Enfasi**.

   |Opzione|Descrizione|
   |-|-|
   |Tono |Utilizza questa opzione per influenzare il tipo di parole, frasi e punteggiatura utilizzate per coinvolgere il pubblico di destinazione. Puoi scegliere tra diversi toni di voce predefiniti, che vanno da **Formale** (che si traduce in un tono più professionale delle scelte) a **Creativo** (che si traduce in un tono più informale). |
   |Formato e lunghezza|Usa questa opzione per controllare la struttura generale del testo, che si compone di tre parti, coperte da quattro diverse opzioni: <ul><li>**Tagline** - Una frase accattivante o una breve frase che identifica l'articolo o il marchio.</li><li>**Paragrafo** - Un singolo paragrafo di testo scorrevole e dettagliato, composto da diverse frasi complete.</li><li>**Tagline + Paragrafo**- Una tagline seguita da un paragrafo</li><li>**Informativa** - Una frase introduttiva, simile a uno slogan, seguita da un elenco puntato di punti di interesse chiave.</li></ul> |
   |Enfasi|Utilizza questa opzione per scegliere da un elenco di qualità predefinite che vuoi enfatizzare nel testo. Scegli una qualità che si allinei al meglio con il tipo di articolo di cui stai scrivendo. Le qualità non corrispondono direttamente agli attributi, alla descrizione o alla categoria dell'articolo. Ad esempio, **Qualità** potrebbe essere una buona scelta sia per una bicicletta che per una scrivania, mentre **Velocità** sarebbe adatta a una bicicletta, ma non una scrivania.|

1. Migliora il campo **Descrizione** nella scheda articolo.

   Il testo nel campo **Descrizione** è utilizzato così com'è in molti punti del testo suggerito, quindi è importante che la descrizione ritragga al meglio il modo in cui desideri fare riferimento all'articolo nel testo di marketing. 

1. Assicurati che il campo **Codice categoria articolo** sulla scheda articolo sia impostato su una categoria corretta.

   Copilot trova parole e frasi correlate alla categoria e le inserisce nel testo suggerito.

### <a name="working-with-multiple-languages"></a>Utilizzare più lingue

Il testo viene sempre generato nella lingua definita dalle [impostazioni](ui-change-basic-settings.md#language) dell'utente. Se l'organizzazione opera e inserisce dati in Business Central utilizzando una lingua diversa o se Business Central è connesso al tuo punto vendita online, ad esempio con Shopify, ciò potrebbe comportare la pubblicazione di contenuti che non corrispondono a contenuti di marketing simili.

## <a name="create-text-from-scratch"></a>Creare un testo da zero

1. In Business Central, apri l'articolo che vuoi modificare come segue:

    1. Nell'angolo in alto a destra seleziona l'icona ![lampadina che apre la funzione Dimmi 22.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato per visualizzare l'elenco degli articoli disponibili.
    2. Per aprire l'articolo, fai doppio clic sul nome o selezionane il numero nella colonna **Nr.** .

2. Completa uno dei seguenti passaggi:

   - Nel riquadro **Testo di marketing** del riquadro Dettaglio informazioni sul lato destro della pagina seleziona **Modifica**.
   - Seleziona l'azione **Testo di marketing**.
3. Apporta le modifiche al testo direttamente nella casella **Testo di marketing**. Usa la barra degli strumenti lungo la parte inferiore della casella per formattare e definire lo stile del testo, aggiungere collegamenti e altro ancora.
4. Al termine seleziona **OK** per salvare il testo.

## <a name="see-also"></a>Vedere anche

[Panoramica dei suggerimenti di testo di marketing](ai-overview.md)  
[Risoluzione dei problemi relativi alle funzionalità di Copilot e IA](ai-copilot-troubleshooting.md)  
[Domande frequenti sui suggerimenti di testo di marketing](faqs-marketing-text.md)  
[Configurare le funzionalità di Copilot e IA](enable-ai.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
