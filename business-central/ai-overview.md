---
title: Panoramica del testo di marketing dell'articolo basato su intelligenza artificiale (anteprima) con Copilot
description: Ottieni una panoramica delle funzionalità di generazione di contenuti IA in Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 03/16/2023
ms.custom: bap-template
---
# <a name="overview-of-ai-powered-item-marketing-text-preview-with-copilot" />Panoramica del testo di marketing dell'articolo basato su intelligenza artificiale (anteprima) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Questo articolo fornisce una panoramica della funzionalità basata sull'intelligenza artificiale fornita da Copilot in Business Central.

## <a name="what-is-ai-powered-item-marketing-text-with-copilot" />Cos'è il testo di marketing dell'articolo basato su intelligenza artificiale con Copilot

Copilot fornisce assistenza alla scrittura basata sull'intelligenza artificiale per gli utenti di Business Central responsabili della creazione di testi di marketing (descrizioni di prodotti) su articoli venduti nei negozi online, come Shopify. Con il clic di un pulsante, Copilot genera un testo coinvolgente, creativo e mette in evidenza gli attributi chiave dell'articolo specifico. Con un po' di revisione e modifica, è pronto per la pubblicazione.

Copilot utilizza [il servizio Azure OpenAI di Microsoft](/azure/cognitive-services/openai/overview) per accedere a modelli di lingua che riconoscono, prevedono e generano il testo basato su set di dati addestrati.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Il video non riflette esattamente come la funzione attualmente funziona o appare nel prodotto. La funzione è leggermente cambiata da quando è stato prodotto il video. Ma ti dà un'idea generale della funzione e per cosa puoi usarla.*
  
## <a name="where-its-used" />Dove è utilizzato

Copilot è disponibile nelle schede articolo in Business Central. In Business Central, gli articoli sono come prodotti in altre applicazioni e negozi. Ogni articolo può essere gestito da una scheda in cui inserisci i dettagli sull'articolo, come le dimensioni, il costo o l'immagine. Questa scheda include anche una casella per l'inserimento del testo di marketing. Questo testo di marketing può essere pubblicato nel tuo negozio online per promuovere l'articolo. Ecco dove entra in gioco Copilot. Semplicemente selezionando l'azione **Crea con Copilot** sulla scheda articolo, Copilot genererà per te una bozza di testo intelligente. Una volta ottenuta la prima bozza, puoi eseguire Copilot ancora finché non ottieni una bozza che ti piace. Quando hai un suggerimento che ti piace, lo rivedi e lo modifichi per verificarne l'accuratezza, quindi lo salvi.

Se Business Central è configurato per connettersi al tuo negozio online su Shopify, puoi portare questo testo e pubblicarlo con l'articolo direttamente nel tuo negozio selezionando **Aggiungi a Shopify**.

## <a name="why-and-how-to-use-it" />Perché usarlo e come

Il testo generato dall'intelligenza artificiale può aiutarti ad accelerare il time-to-market dei prodotti nei negozi online, limitando il tempo impiegato per il copywriting. Alcuni vantaggi chiave sono:

- Aiuta gli utenti a superare il blocco dello scrittore facendoli iniziare con una bozza intelligente
- Sblocca la creatività per fornire descrizioni dei prodotti più accattivanti
- Migliora la coerenza del contenuto di marketing per le linee di prodotti

Dovresti considerare il testo generato dall'AI come un **semplice suggerimento**. I suggerimenti possono, in alcuni casi, contenere errori e persino testo inappropriato, pertanto sono necessarie la supervisione e la revisione umane. Prima di rendere il testo disponibile al pubblico, è necessario verificarne l'accuratezza e apportare le modifiche appropriate.

## <a name="current-limitations" />Quali sono le attuali limitazioni

Questa sezione spiega le attuali limitazioni della funzionalità di testo generato dall'intelligenza artificiale fornita da Copilot.

- I suggerimenti di testo generati dall'intelligenza artificiale sono solo in inglese.
- Suggerimenti scadenti possono risultare quando vengono utilizzati nomi di prodotti vaghi o generici e mancano specifiche su un articolo, come attributi chiave o una categoria.
- Copilot è supportato solo su Business Central online e non in ambienti cloud privati o ambienti locali di Business Central.
- Copilot non è supportato tramite connessioni alla propria risorsa del servizio Azure OpenAI nella sottoscrizione di Azure.
- L'estensibilità dei partner della funzionalità di intelligenza artificiale tramite il codice AL non è supportata.

## <a name="next-steps" />Passaggi successivi

Per iniziare, avrai bisogno di un ambiente con Business Central versione 22 abilitata con Copilot.

- Se sei già un cliente di Business Central, l'amministratore di Business Central dovrà configurare la versione 22 in un ambiente per te.
- Se non sei un cliente di Business Central, ma vuoi provare, puoi registrati per una versione di valutazione gratuita.

Per ulteriori informazioni, vai a [Ottenere la versione di anteprima di Business Central](ai-preview-getstarted.md).  

## <a name="see-also" />Vedere anche

[Configurare il testo del marketing articolo basato su intelligenza artificiale come amministratore](enable-ai.md)  
[Creare un testo di marketing con Copilot](item-marketing-text.md)  
[Domande frequenti sul testo di marketing per l'articolo basato sull'intelligenza artificiale con Copilot](ai-faq.md)  
[Iniziare a usare il connettore Shopify](shopify/get-started.md)  
