---
title: Domande frequenti su suggerimenti di testo di marketing
description: 'Queste domande frequenti forniscono informazioni sulla tecnologia di intelligenza artificiale utilizzata nei suggerimenti di testo di marketing in Business Central, insieme a considerazioni e dettagli chiave su come viene utilizzata l''intelligenza artificiale, come è stata testata e valutata ed eventuali limitazioni specifiche.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---

# Domande frequenti sui suggerimenti di testo di marketing con Copilot

Queste domande frequenti (FAQ) descrivono l'impatto della funzionalità [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] sull'intelligenza artificiale in [!INCLUDE[prod_short](includes/prod_short.md)].

## Cos'è la funzionalità per i suggerimenti di testo di marketing?

Copilot fornisce assistenza alla scrittura agli utenti responsabili della creazione di testo di marketing (noto anche come copia) su articoli in [!INCLUDE[prod_short](includes/prod_short.md)]. Questa funzionalità è nota come [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. La funzionalità [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] fornisce assistenza alla scrittura agli utenti responsabili della creazione di testo di marketing (noto anche come *copia*) su articoli in [!INCLUDE[prod_short](includes/prod_short.md)].

La funzionalità è disponibile in qualsiasi scheda articolo di [!INCLUDE[prod_short](includes/prod_short.md)]. Per utilizzarla, basta aprire un articolo e quindi selezionare **Testo di marketing** > **Bozza con Copilot**. Questa azione genera automaticamente un suggerimento di testo coinvolgente, creativo e specifico per l'articolo mostrato. I suggerimenti si basano su vari input, tra cui:

- Gli attributi, la categoria e il nome dell'articolo.
- Le preferenze di stile di scrittura personali come tono della voce, qualità enfatizzata, formato e durata.

Puoi modificare il valore di queste opzioni di input per influenzare il risultato del testo generato dall'intelligenza artificiale. Prima di salvare un suggerimento, puoi facilmente esaminarlo e modificarlo per verificarne la precisione o provare un altro suggerimento.

Alcuni vantaggi chiave di questa funzionalità includono:

- Diminuisce il tempo impiegato per la scrittura di testi, che può accelerare il time-to-market per gli articoli venduti nei negozi online.
- Sblocca la creatività per fornire descrizioni dei prodotti più accattivanti.
- Migliora la coerenza del materiale di marketing per le linee di prodotti.

## Quali sono le funzionalità del sistema?

La funzionalità [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] utilizza il [servizio OpenAI di Microsoft Azure](/azure/cognitive-services/openai/overview) per accedere a potenti modelli linguistici che analizzano e generano linguaggio naturale. Questi modelli sono stati addestrati su un'ampia gamma di set di dati di testo. Di conseguenza, Copilot può generare risposte suggerite e personalizzate in inglese sulla base di una quantità minima di dati di input, come gli attributi, la categoria o la descrizione di un articolo. 

## Qual è lo scopo previsto del sistema?

Questa funzionalità ha lo scopo di assistere gli utenti nella creazione di testo di marketing per articoli in [!INCLUDE[prod_short](includes/prod_short.md)]. Gli scrittori utilizzano la funzionalità per ottenere rapidamente suggerimenti di testo accattivanti e coinvolgenti, che vengono poi riesaminati e modificati per garantirne la precisione. 

## Come è stato valutato il testo di marketing dell'articolo? Quali metriche vengono utilizzate per misurare le prestazioni?

- La funzionalità è stata sottoposta a test approfonditi in cui numerosi testi in diverse lingue sono stati valutati da esperti linguistici rispetto a vari criteri. I test si basavano sui dati dimostrativi di [!INCLUDE[prod_short](includes/prod_short.md)] e su altri cataloghi di prodotti fittizi.
- Questa funzionalità è stata creata in conformità con lo standard di intelligenza artificiale responsabile di Microsoft. [Scopri di più sull'intelligenza artificiale responsabile di Microsoft](https://aka.ms/RAI).

## In che modo Microsoft monitora la qualità del contenuto generato?

Microsoft dispone di vari sistemi per garantire che le funzionalità di Copilot rimangano operative e generino contenuti della massima qualità.

- Gli utenti hanno l'opportunità di fornire feedback per segnalare contenuti inappropriati e migliorare la funzionalità.

  - Se riscontri contenuto generato inappropriato, segnalalo a Microsoft utilizzando questo modulo di feedback: [Segnala abuso](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft potrebbe disattivare le funzionalità basate su Copilot per clienti selezionati se viene rilevato un abuso della funzionalità. 

  - Teniamo traccia del feedback degli utenti su [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] allo scopo di migliorare i suggerimenti. 

    Per fornire feedback, si utilizza l'icona Mi piace (pollice su) o Non mi piace (pollice giù) nella pagina **Copilot**in [!INCLUDE[prod_short](includes/prod_short.md)]. Raccogliamo la telemetria di questi gesti per ogni output di IA per cui invii feedback.

    ![Una scheda articolo con il riquadro Testo di marketing](media/create-with-copilot-window-feedback.svg)

- Il servizio OpenAI di Azure archivia le richieste e i completamenti del servizio per monitorare l'uso abusivo e per sviluppare e migliorare la qualità dei sistemi di gestione di contenuti del servizio OpenAI di Azure. [Scopri di più sulla nostra gestione e sul filtro dei contenuti](/azure/cognitive-services/openai/concepts/content-filter). I dati aziendali non vengono usati per addestrare modelli di intelligenza artificiale nel servizio OpenAI di Azure.

   I dipendenti Microsoft autorizzati possono accedere ai dati di richieste e completamenti che hanno attivato i nostri sistemi automatizzati allo scopo di indagare e verificare potenziali abusi. Per i clienti che utilizzano [!INCLUDE[prod_short](includes/prod_short.md)] nell'Unione Europea, i dipendenti Microsoft autorizzati si trovano nell'Unione Europea. Questi dati possono essere utilizzati per migliorare i nostri sistemi di gestione dei contenuti. In caso di violazione confermata delle norme, potremmo chiederti di intraprendere un'azione immediata per risolvere il problema e prevenire ulteriori abusi. La mancata risoluzione del problema può comportare la sospensione o l'interruzione dell'accesso alle risorse del servizio OpenAI di Azure.

   Per ulteriori informazioni, consulta [Dati, privacy e sicurezza per il servizio OpenAI di Azure](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## Il servizio OpenAI di Azure include un processo di registrazione e revisione umana e, in caso affermativo, posso rinunciarvi esplicitamente?  

Nell'ambito della fornitura del servizio OpenAI di Azure, Microsoft elaborerà e memorizzerà i dati dei clienti inviati al servizio, nonché il contenuto di output, allo scopo di monitorare e prevenire usi o output abusivi o dannosi del servizio e sviluppare, testare e migliorare le capacità progettate per prevenire l'uso abusivo e/o gli output dannosi del servizio. 

Il personale Microsoft autorizzato può esaminare i dati che hanno attivato i nostri sistemi automatizzati per indagare e verificare potenziali abusi e può impegnarsi in un campionamento casuale limitato di termini che non sono contrassegnati dai nostri sistemi automatizzati per garantire che i sistemi funzionino correttamente. Il personale Microsoft autorizzato può anche accedere e utilizzare questi dati per migliorare i nostri sistemi che monitorano e impediscono usi o output abusivi o dannosi del servizio. Leggi di più nelle [condizioni di anteprima](https://go.microsoft.com/fwlink/?linkid=2189520).

Affinché Microsoft possa salvaguardare il servizio e i relativi clienti, non è possibile rinunciare esplicitamente ai processi di registrazione e revisione umana.

## Quali dati vengono raccolti dalla funzionalità? Come vengono usati i dati?

La funzionalità per i suggerimenti di testo di marketing raccoglie i dati minimi richiesti da Business Central per offrire il servizio. Per ulteriori informazioni, vedi [Termini di Dynamics 365 per le funzionalità basate sul servizio OpenAI di Azure](https://go.microsoft.com/fwlink/?linkid=2236010).

La funzionalità raccoglie anche dati dal feedback che l'utente può fornire utilizzando le icone Mi piace (pollice su) o Non mi piace (pollice giù) nella parte superiore della pagina **Copilot**. I dati sono anonimi e includono la scelta Mi piace o Non mi piace, il motivo di Non mi piace, se fornito, e la funzionalità di Copilot a cui si applica il feedback. Usiamo questi dati per valutare e migliorare la qualità della funzionalità.

## Quali sono le limitazioni di [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]? In che modo gli utenti possono ridurre al minimo l'impatto delle limitazioni dei [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] durante l'utilizzo del sistema?

- Poiché la tecnologia alla base della funzionalità utilizza l'intelligenza artificiale che è stata addestrata su un'ampia gamma di origini, il contenuto generato non è sempre idoneo o adatto. Alcuni suggerimenti possono anche includere contenuti discutibili o inappropriati. È tua responsabilità rivedere e modificare i suggerimenti generati per assicurarti che siano accurati e appropriati.

- Lingue disponibili
  
   [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

## Quali fattori operativi e impostazioni consentono un uso efficace e responsabile del sistema?

Ci sono alcune cose che puoi fare per ottenere il massimo dalla funzionalità:

- Aggiungi più attributi a un articolo per promuovere le funzionalità e le caratteristiche specifiche che ti interessano.
- Modifica le opzioni per il tono della voce e l'enfasi della qualità in base alle tue preferenze personali.
- Migliora la descrizione dell'articolo.
- Assicurati che all'articolo sia assegnata la categoria più adatta.

Per saperne di più, vai a [Migliorare e personalizzare i suggerimenti di testo](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Esamina sempre l'accuratezza dei suggerimenti prima di salvarli e pubblicarli per il pubblico.


## Vedere anche

- [Suggerimenti di testo di marketing](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
