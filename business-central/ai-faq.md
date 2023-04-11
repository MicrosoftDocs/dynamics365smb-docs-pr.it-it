---
title: Domande frequenti sul testo di marketing per l'articolo basato sull'intelligenza artificiale (anteprima) con Copilot
description: Ottieni risposta alle domande comuni sulle funzionalità di testo generate dall'intelligenza artificiale con Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# Domande frequenti sul testo di marketing per l'articolo basato sull'intelligenza artificiale (anteprima) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Questo articolo illustra domande e risposte per spiegare aspetti importanti della tecnologia IA alla base di Copilot e del testo che genera.

## [Generale](#tab/general)

### Che cos'è Copilot?

Copilot fornisce suggerimenti di testo generati dall'intelligenza artificiale per gli articoli in Business Central. È destinato agli utenti che scrivono testi di marketing per articoli per aiutarli a produrre contenuti accattivanti ed efficaci. Alcuni vantaggi chiave sono:

- Diminuisce il tempo impiegato per la scrittura di testi, che può accelerare il time-to-market per gli articoli venduti nei negozi online.
- Sblocca la creatività per fornire descrizioni dei prodotti più accattivanti.
- Migliora la coerenza del materiale di marketing per le linee di prodotti.

Gli utenti devono considerare il testo generato dall'intelligenza artificiale come un suggerimento che deve essere rivisto e modificato per verificarne l'accuratezza prima di renderlo disponibile pubblicamente.

### Perché Copilot non è disponibile per il testo di marketing sui miei articoli in Business Central?

Per disporre di Copilot, devono essere soddisfatti i seguenti requisiti:

- La lingua utilizzata in Business Central deve essere l'inglese. Qualsiasi lingua inglese disponibile funzionerà, come inglese (Stati Uniti), inglese (Regno Unito) o inglese (Sudafrica).

  Per cambiare la lingua, nell'angolo in alto a destra seleziona l'icona **Impostazioni** ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") > **Impostazioni personali** > **Lingua**. Per ulteriori informazioni, vai a [Modificare le impostazioni di base](ui-change-basic-settings.md#language).
- Devi utilizzare Business Central online versione 22 o successiva (se sei un cliente esistente) o una versione di prova.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->.

   Per verificare la versione, seleziona il punto interrogativo nell'angolo in alto a destra, quindi **Guida e supporto**. In **Risoluzione dei problemi**, cerca la versione dell'applicazione. Per informazioni su come ottenere la versione di anteprima corretta, vai a [Iniziare con una versione di anteprima di Business Central](ai-preview-getstarted.md).
- La funzionalità **Crea descrizioni del prodotto basate sull'intelligenza artificiale con Copilot** deve essere abilitata.

   Per ulteriori informazioni, vai a [Abilitare o disabilitare la funzione "Crea descrizioni del prodotto basate sull'intelligenza artificiale con Copilot"](enable-ai.md#enable-or-disable-the-create-ai-powered-product-descriptions-with-copilot-feature).
- Un amministratore ha accettato le condizioni.

   Per ulteriori informazioni, vai a [Accettare o rifiutare l'anteprima e le condizioni sulla privacy per tutti gli utenti](enable-ai.md#consent-to-or-reject-the-preview-and-privacy-terms-and-conditions-for-all-users).

### Copilot è disponibile per l'anteprima in Business Central locale?

No, attualmente non è supportato in Business Central locale.

### Come funziona Copilot, da dove viene il testo suggerito?

Copilot utilizza [il servizio Azure OpenAI di Microsoft](/azure/cognitive-services/openai/overview) per accedere a potenti modelli linguistici che analizzano e generano il linguaggio naturale. Questi modelli sono stati addestrati su un'ampia gamma di set di dati di testo. Di conseguenza, Copilot può generare risposte suggerite e personalizzate in inglese sulla base di una quantità minima di dati di input, come gli attributi, la categoria o la descrizione di un articolo. 

### Qual è la qualità del testo suggerito da Copilot?

Poiché la tecnologia alla base di Copilot utilizza l'intelligenza artificiale che è stata addestrata su un'ampia gamma di origini, il contenuto generato non è sempre idoneo o adatto. Alcuni suggerimenti possono anche includere contenuti discutibili o inappropriati. È tua responsabilità rivedere e modificare i suggerimenti generati per assicurarti che siano accurati e appropriati.

Per informazioni sui suggerimenti inappropriati, vai a [Che cosa è stato fatto per i suggerimenti di testo offensivi e dannosi?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### Come posso migliorare i suggerimenti che ricevo da Copilot?

Ci sono alcune cose che puoi fare per ottenere il massimo dai suggerimenti di Copilot:

- Aggiungi più attributi a un articolo per promuovere le funzionalità e le caratteristiche specifiche che ti interessano
- Modifica le opzioni per il tono della voce e l'enfasi della qualità in base alle tue preferenze personali.
- Migliora la descrizione dell'articolo
- Assicurati che all'articolo sia assegnata la categoria più adatta.

Per saperne di più, vai a [Migliorare e personalizzare i suggerimenti di testo](item-marketing-text.md#improve-and-tailor-text-suggestions).

### Cosa succede se non sono soddisfatto del testo generato?

Per aiutarci a migliorare il testo, seleziona **È un buon suggerimento?** nella pagina **Crea con Copilot** , che puoi rispondere con il pollice in su (mi piace) o il pollice in giù (necessita di miglioramenti).

![Mostra e scheda articolo con il riquadro Testo di marketing](media/create-with-copilot-window-feedback.png)

### Gli amministratori possono disabilitare Copilot? Se sì, come?

Business Central offre agli amministratori due modi per disabilitare Copilot nell'anteprima:

- Non accettare l'informativa sulla privacy di Azure OpenAI per tutti gli utenti.

  oppure

- Disattivare la funzione **Crea descrizioni del prodotto basate sull'intelligenza artificiale con Copilot** nella pagina **Gestione funzionalità** .

Per saperne di più, vai a [Configurare il testo di marketing degli articoli basato sull'intelligenza artificiale (anteprima) con Copilot come amministratore](enable-ai.md).

## [Equità](#tab/fairness)

### Copilot funziona con lingue diverse dall'inglese?

Attualmente, Copilot supporta solo l'inglese. È possibile che vengano restituite risposte imprecise quando gli utenti conversano con il sistema in lingue diverse dall'inglese.

## [Supervisione umana](#tab/oversight)

### Che cosa è stato fatto per i suggerimenti di testo offensivi e dannosi?

Il servizio Azure OpenAI archivia le richieste e i completamenti del servizio per monitorare l'uso abusivo e per sviluppare e migliorare la qualità dei sistemi di gestione dei contenuti di Azure OpenAI. [Scopri di più sulla nostra gestione e sul filtro dei contenuti](/azure/cognitive-services/openai/concepts/content-filter).

I dipendenti Microsoft autorizzati possono accedere ai dati di richiesta e completamento che hanno attivato i nostri sistemi automatizzati allo scopo di indagare e verificare potenziali abusi. Per i clienti che hanno distribuito il servizio Azure OpenAI nell'Unione Europea, i dipendenti Microsoft autorizzati si troveranno nell'Unione Europea. Questi dati possono essere utilizzati per migliorare i nostri sistemi di gestione dei contenuti. In caso di violazione confermata delle norme, potremmo chiederti di intraprendere un'azione immediata per risolvere il problema e prevenire ulteriori abusi. La mancata risoluzione del problema può comportare la sospensione o l'interruzione dell'accesso alle risorse di Azure OpenAI.

Per ulteriori informazioni, vedi [Dati, privacy e sicurezza per il servizio Azure OpenAI](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### Posso rinunciare al processo di registrazione e revisione umana?  

Nell'ambito dell'offerta delle anteprime di Azure Open AI, Microsoft elaborerà e memorizzerà i Dati del cliente inviati al servizio, nonché il Contenuto di output, allo scopo di (1) monitorare e prevenire usi o output abusivi o dannosi del servizio e (2) sviluppare, testare e migliorare le capacità progettate per prevenire l'uso abusivo e/o gli output dannosi del servizio. Il personale Microsoft autorizzato può esaminare i dati che hanno attivato i nostri sistemi automatizzati per indagare e verificare potenziali abusi e può impegnarsi in un campionamento casuale limitato di termini che non sono contrassegnati dai nostri sistemi automatizzati per garantire che i sistemi funzionino correttamente. Il personale Microsoft autorizzato può anche accedere e utilizzare questi dati per migliorare i nostri sistemi che monitorano e impediscono usi o output abusivi o dannosi del servizio. Leggi di più nelle [condizioni di anteprima](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/)

## [Privacy](#tab/privacy)

### Quali dati vengono raccolti dalla funzionalità? Come vengono usati i dati?

La funzionalità raccoglie la tua risposta alla domanda **È un buon suggerimento?** nella pagina **Crea con Copilot** , che puoi essere il pollice in su (mi piace) o il pollice in giù (necessita di miglioramenti).

Usiamo questi dati per valutare e migliorare la qualità della funzionalità. Maggiori informazioni su quali dati vengono raccolti sono disponibili nei [termini di anteprima](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Mostra e scheda articolo con il riquadro Testo di marketing](media/create-with-copilot-window-feedback.png)

---

## Vedere anche

[Panoramica del testo di marketing dell'articolo basato su intelligenza artificiale con Copilot](ai-overview.md)  
[Configurare testo del marketing articolo basato su intelligenza artificiale con Copilot come amministratore](enable-ai.md)  
[Creare un testo di marketing per gli articoli utilizzando Copilot](item-marketing-text.md)  
[Domande frequenti sul testo di marketing per l'articolo basato sull'intelligenza artificiale con Copilot](ai-faq.md)  
