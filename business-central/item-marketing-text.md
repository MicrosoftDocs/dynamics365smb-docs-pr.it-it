---
title: Aggiungere del testo di marketing agli articoli
description: Scrivere un testo di marketing per gli articoli in Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="add-marketing-text-to-items"></a>Aggiungere del testo di marketing agli articoli

Per qualsiasi articolo registrato in Business Central, puoi scrivere un *testo di marketing* sull'articolo. Sebbene il testo di marketing sia una sorta di descrizione, è diverso da quello del campo **Descrizione** dell'articolo. Il campo **Descrizione** viene in genere utilizzato come nome visualizzato conciso per identificare rapidamente il prodotto. Il testo di marketing, invece, è un testo più ricco e descrittivo. Il suo scopo è aggiungere contenuti di marketing e promozionali, noti anche come *copia*. Questo testo può quindi essere pubblicato con l'articolo se è pubblicato su un negozio online, come Shopify.

Il testo di marketing può essere creato in due modi: Il modo più semplice per iniziare è utilizzare Copilot, che suggerisce il testo generato dall'intelligenza artificiale. L'altro modo è cominciare da zero. 

## <a name="get-marketing-text-suggestions-with-copilot"></a><a name=copilot></a>Creare un testo di marketing generato dall'intelligenza artificiale (anteprima) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Con Copilot, ricevi rapidamente un suggerimento di testo che viene generato automaticamente per te. Il testo generato dall'intelligenza artificiale è adattato all'articolo e fornisce un buon punto di partenza. Il testo si basa in parte sulle seguenti informazioni:

- Attributi definiti per l'articolo, ad esempio, come la descrizione, il colore, le dimensioni, il materiale e così via.
- Le preferenze di stile selezionabili come tono della voce, formato e durata.

Copilot è progettato per farti risparmiare tempo e aiutarti a scrivere testi creativi e accattivanti che riflettano il tuo marchio e siano coerenti in tutta la tua linea di prodotti. Inizia generando un suggerimento, quindi modifica il testo suggerito secondo le tue necessità.

> [!NOTE]
> Nella versione di anteprima di Business Central, il testo generato dall'IA è solo in inglese.

### <a name="prerequisites"></a>Prerequisiti

- Stai utilizzando una [versione di anteprima](ai-preview-getstarted.md) di Business Central abilitata per Copilot. L'abilitazione di Copilot viene eseguita da un amministratore. Per ulteriori informazioni, vai a [Configurare il testo di marketing degli articoli basato sull'intelligenza artificiale con Copilot](enable-ai.md).
- La lingua utilizzata in Business Central deve essere l'inglese. Qualsiasi lingua inglese disponibile funzionerà, come inglese (Stati Uniti), inglese (Regno Unito) o inglese (Sudafrica).

   Per cambiare la lingua, nell'angolo in alto a destra seleziona l'icona **Impostazioni** ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") > **Impostazioni personali** > **Lingua**. Per ulteriori informazioni, vai a [Modificare le impostazioni di base](ui-change-basic-settings.md#language).
- Rivedi le [Domande frequenti su Copilot](ai-faq.md) per saperne di più sui suggerimenti di testo generati dall'intelligenza artificiale da Copilot e su come utilizzarli.

### <a name="create-first-draft-with-copilot"></a>Creare la prima bozza con Copilot

1. In Business Central, apri l'articolo che vuoi modificare. Per aprire un articolo, segui i passaggi seguenti:

   1. Nell'angolo in alto a destra seleziona l'icona ![lampadina che apre la funzione Dimmi 22.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato per visualizzare l'elenco degli articoli disponibili.
   2. Per aprire l'articolo, fai doppio clic sul nome o selezionane il valore nella colonna **Nr.** .

   Per informazioni su come creare un articolo, vai a [Registrare nuovi articoli](inventory-how-register-new-items.md).

   [![Mostra e scheda articolo con il riquadro Testo di marketing](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. Dalla scheda dell'articolo, ci sono due modi per iniziare a scrivere un testo di marketing con Copilot:

   - Utilizza il riquadro **Testo di marketing** nel riquadro Dettaglio informazioni sul lato destro della pagina. Attenersi alla seguente procedura:

     1. Nel riquadro **Testo di marketing** , seleziona **Crea con Copilot**.

        Il testo suggerito viene visualizzato nel riquadro.
     2. Se desideri un altro suggerimento, seleziona **Crea con Copilot** di nuovo. Se non ti piace un suggerimento, seleziona **Ignora** per cancellare il riquadro.

        Puoi ripetere questo passaggio più e più volte finché non ricevi un suggerimento che ritieni sia un buon punto di partenza. Ma tieni presente che il suggerimento corrente verrà sovrascritto e non potrai recuperarlo. Quindi, se ti piace il suggerimento attuale, vai al passaggio successivo. Avrai comunque l'opportunità di ottenere più suggerimenti e persino di migliorarli, se lo desideri in seguito.
      3. Seleziona **Rivedi e salva il suggerimento** o **Modifica** per rivedere, modificare e salvare il testo.

         Questo passaggio ti porta alla pagina **Crea con Copilot**. Vai alla sezione successiva.

         > [!NOTE]
         > Il testo non verrà salvato fino a quando non eseguirai questo passaggio.

   - Seleziona l'azione **Testo di marketing** nella parte superiore della pagina della scheda articolo per andare direttamente alla pagina **Crea con Copilot**.

     Dalla pagina **Crea con Copilot** , seleziona **Crea con Copilot** per ottenere il primo suggerimento. Puoi quindi ottenere più suggerimenti, provare a migliorare i suggerimenti che ricevi, modificare il testo e altro ancora. Vai a [Rivedere, modificare e salvare](#review-edit-and-save-text) per i dettagli.

   > [!TIP]
   > [Da dove provengono i suggerimenti?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### <a name="review-edit-and-save-text"></a>Rivedere, modificare e salvare il testo

Una volta che hai la prima bozza, devi rivederla e apportare le modifiche al testo per prepararla alla pubblicazione. Questo lavoro viene svolto dalla pagina **Crea con Copilot**. Il testo corrente è mostrato nella casella **Testo di marketing**. La pagina ti consente di ottenere più suggerimenti, modificare le preferenze per influenzare i suggerimenti e apportare manualmente modifiche e modellare il testo.

[![Mostra le finestre Crea con Copilot](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> Il testo generato dall'intelligenza artificiale da Copilot è solo un suggerimento e può contenere errori. Richiede la supervisione e la revisione umana per garantire che sia accurato e appropriato. Esamina il testo suggerito e modifica se necessario prima di salvarlo e pubblicarlo per il consumo pubblico.

Utilizza le seguenti linee guida per finalizzare e salvare il testo di marketing.

1. Apporta le modifiche al testo direttamente nella casella **Testo di marketing**. Usa la barra degli strumenti lungo la parte inferiore della casella per formattare e definire lo stile del testo, aggiungere collegamenti e altro ancora.
2. Per ricevere un nuovo suggerimento, seleziona **Crea bozza**.
3. Se non sei soddisfatto dei suggerimenti, migliora i suggerimenti di testo in base alle tue preferenze.

   Seleziona **Altre impostazioni**, modifica le opzioni visualizzate in **Scegli come Copilot crea suggerimenti**, quindi seleziona **Crea bozza** per ottenere un nuovo suggerimento.

   Per le linee guida su come migliorare i suggerimenti, vai a [Migliorare e personalizzare i suggerimenti di testo](#improve-and-tailor-text-suggestions).

4. Se vuoi tornare al suggerimento precedente, seleziona **Annulla**.
5. Esamina attentamente il testo per verificarne l'accuratezza e l'adeguatezza, quindi seleziona **OK** per salvarlo.

### <a name="improve-and-tailor-text-suggestions"></a>Migliorare e personalizzare i suggerimenti di testo

Ci sono alcuni passaggi che puoi fare per migliorare i suggerimenti di testo e modificarli in base alle tue preferenze personali o aziendali.

1. Utilizza le opzioni nella parte superiore della pagina **Crea con Copilot** per influenzare il risultato del testo generato dall'intelligenza artificiale: 

   |Opzione|Descrizione|
   |-|-|
   |Attributi da includere|Utilizza questa opzione per basare i suggerimenti, in parte, sugli attributi assegnati all'articolo. Scegli gli attributi che meglio si allineano alle caratteristiche che desideri promuovere. Più attributi pertinenti includi, più ricco sarà il risultato. Se ritieni che ti manchino alcuni attributi chiave, aggiungine altri. Per ulteriori informazioni sugli attributi, vedi [Utilizzare gli attributi articolo](inventory-how-work-item-attributes.md) |
   |Enfatizza una qualità|Utilizza questa opzione per scegliere da un elenco di qualità predefinite che vuoi enfatizzare nel testo. Scegli una qualità che si allinei al meglio con il tipo di articolo di cui stai scrivendo. Le qualità non corrispondono direttamente agli attributi, alla descrizione o alla categoria dell'articolo. Ad esempio, **Qualità** potrebbe essere una buona scelta sia per una bicicletta che per una scrivania, mentre **Velocità** sarebbe adatta a una bicicletta, ma non una scrivania.|
   |Tono della voce|Utilizza questa opzione per influenzare il tipo di parole, frasi e punteggiatura utilizzate per coinvolgere il pubblico di destinazione. Puoi scegliere tra diversi toni di voce predefiniti, che vanno da **Formale** (che si traduce in un tono più professionale delle scelte) a **Creativo** (che si traduce in un tono più informale). |
   |Formato e lunghezza|Usa questa opzione per controllare la struttura generale del testo, che si compone di tre parti, coperte da quattro diverse opzioni: <ul><li>**Tagline** - Una frase accattivante o una breve frase che identifica l'articolo o il marchio.</li><li>**Paragrafo** - Un singolo paragrafo di testo scorrevole e dettagliato, composto da diverse frasi complete.</li><li>**Tagline + Paragrafo**- Una tagline seguita da un paragrafo</li><li>**Informativa** - Una frase introduttiva, simile a uno slogan, seguita da un elenco puntato di punti di interesse chiave.</li></ul> |

2. Migliora il campo **Descrizione** nella scheda articolo.

   Il testo nel campo **Descrizione** sarà utilizzato così com'è in molti punti del testo suggerito, quindi è importante che la descrizione ritragga al meglio il modo in cui desideri fare riferimento all'articolo nel testo di marketing. 

3. Assicurati che il campo **Codice categoria articolo** sulla scheda articolo sia impostato su una categoria corretta.

   Copilot troverà parole e frasi correlate alla categoria e le inserirà nel testo suggerito.

## <a name="create-text-from-scratch"></a>Creare un testo di marketing da zero

1. In Business Central, apri l'articolo che vuoi modificare come segue:

    1. Nell'angolo in alto a destra seleziona l'icona ![lampadina che apre la funzione Dimmi 22.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato per visualizzare l'elenco degli articoli disponibili.
    2. Per aprire l'articolo, fai doppio clic sul nome o selezionane il numero nella colonna **Nr.** .

2. Effettuare una delle seguenti operazioni:

   - Nel riquadro **Testo di marketing** del riquadro Dettaglio informazioni sul lato destro della pagina seleziona **Modifica**.
   - Seleziona l'azione **Testo di marketing**.
3. Apporta le modifiche al testo direttamente nella casella **Testo di marketing**. Usa la barra degli strumenti lungo la parte inferiore della casella per formattare e definire lo stile del testo, aggiungere collegamenti e altro ancora.
4. Al termine seleziona **OK** per salvare il testo.

## <a name="see-also"></a>Vedere anche

[Panoramica del testo di marketing dell'articolo basato su intelligenza artificiale con Copilot](ai-overview.md)  
[Configurare testo del marketing articolo basato su intelligenza artificiale con Copilot](enable-ai.md)  
[Domande frequenti sul testo di marketing per l'articolo basato sull'intelligenza artificiale con Copilot](ai-faq.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
