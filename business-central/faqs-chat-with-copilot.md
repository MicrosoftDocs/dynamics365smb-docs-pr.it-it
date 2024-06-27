---
title: Domande frequenti sull'intelligenza artificiale responsabile per Chat con Copilot (anteprima)
description: 'Queste domande frequenti forniscono informazioni sulla tecnologia di IA utilizzata per chattare con Copilot in Business Central. Includono considerazioni e dettagli chiave su come viene utilizzata l''intelligenza artificiale, come è stata testata e valutata ed eventuali limitazioni specifiche.'
ms.date: 06/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# Domande frequenti sull'intelligenza artificiale responsabile per Chat con Copilot (anteprima)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

Queste domande frequenti descrivono l'impatto della funzionalità Chat con Copilot sull'intelligenza artificiale in [!INCLUDE[prod_short](includes/prod_short.md)]. Se sei interessato a domande generali sull'utilizzo della funzionalità, vedi [ Domande frequenti su Chat con Copilot](chat-with-copilot-faq.md).

## Che cosè Chat con Copilot?

Microsoft Copilot è un assistente basato sull'intelligenza artificiale che ti aiuta a essere più creativo, produttivo ed efficiente. Puoi chattare con Copilot in Business Central per ottenere risposte e informazioni dettagliate su [!INCLUDE[prod_short](includes/prod_short.md)] e dati aziendali digitando ciò che vuoi sapere in linguaggio naturale.

Chat con Copilot, denominata anche chat, è una funzionalità interattiva che risponde alle tue domande senza che tu debba navigare nell'interfaccia utente o nella documentazione del prodotto. Il riquadro Copilot è accessibile da qualsiasi area nel client di [!INCLUDE[prod_short](includes/prod_short.md)].

Puoi porre domande in linguaggio naturale, ad esempio "Come posso consegnare le merci ai miei clienti direttamente dai miei fornitori?" oppure "Abbiamo sedie da ufficio in stock per meno di 600 $?" In risposta, Copilot fornisce risposte in linguaggio naturale. A seconda delle domande, le risposte possono includere testo semplice, collegamenti a record o pagine in [!INCLUDE[prod_short](includes/prod_short.md)] e collegamenti ad articoli della guida di [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Learn.

## Quali sono le funzionalità di Chat con Copilot?

Puoi chattare con Copilot per ottenere risposte alle seguenti categorie di domande:

### Spiegazione e guida

Puoi chiedere a Copilot di spiegare un concetto specifico correlato a [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio cosa sono le dimensioni o fornire indicazioni su come completare un'attività, ad esempio come registrare un ordine cliente. Copilot esegue una ricerca nella documentazione ufficiale di [!INCLUDE[prod_short](includes/prod_short.md)] pubblicata da Microsoft e fornisce una risposta in base alla documentazione.

- Copilot utilizza le conoscenze in Microsoft Learn (non una ricerca Web ampia) per eseguire una ricerca semantica solo nella documentazione di Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Learn.

- Copilot non intraprende azioni, non crea nuovi dati né modifica alcuna configurazione. Riassume semplicemente tutti i paragrafi che trova in Microsoft Learn che corrispondono alla domanda o al prompt nella chat.

### Ricerca di dati aziendali e pagine correlate

Puoi chiedere a Copilot di trovare le pagine per nome oppure record in base ai relativi campi e vincoli. Se Copilot trova una corrispondenza, risponde con un collegamento al record o alla pagina pertinente, che puoi quindi selezionare.

- Copilot converte l'input in linguaggio naturale in una query composta da criteri di ricerca, ordinamento e filtro delle tabelle.

  La funzionalità utilizza le funzionalità native di ricerca dei dati di [!INCLUDE[prod_short](includes/prod_short.md)] per trovare i dati corrispondenti nelle tabelle all'interno del database della società. La ricerca viene eseguita con la tua identità per motivi di sicurezza e conformità. Non esegue la ricerca al di fuori del database di [!INCLUDE[prod_short](includes/prod_short.md)].

- Copilot non intraprende azioni, non crea nuovi dati né modifica alcuna configurazione. Riepiloga solo i record ricevuti dalla ricerca di dati nativa di [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Qual è l'uso previsto di Chat con Copilot?

Chat è progettato per l'uso aziendale e per rispondere a domande relative a [!INCLUDE[prod_short](includes/prod_short.md)] e ai dati aziendali in esso contenuti. La funzionalità ti aiuta a risolvere attività comuni come trovare documenti o ottenere indicazioni. Puoi esprimerti con parole tue, rendendo il tuo lavoro più semplice e più accessibile quando utilizzi [!INCLUDE[prod_short](includes/prod_short.md)].

## Come è stata valutata la funzionalità Chat con Copilot? Quali metriche vengono utilizzate per misurare le prestazioni?

- La funzionalità è stata sottoposta a test approfonditi durante i quali a Copilot sono stati forniti numerosi testi in lingua inglese che coprivano un'ampia gamma di argomenti e stili di intenti di espressione. I risultati sono stati valutati rispetto a accuratezza, pertinenza e sicurezza.
  
- La funzionalità è stata creata in conformità con lo standard di intelligenza artificiale responsabile di Microsoft. [Scopri di più sull'intelligenza artificiale responsabile di Microsoft](https://aka.ms/RAI).

## In che modo Microsoft monitora la qualità del contenuto generato?

Microsoft dispone di vari sistemi per garantire che i contenuti generati da Copilot siano della massima qualità, per rilevare abusi e garantire la sicurezza dei nostri clienti e dei loro dati.

Puoi fornire feedback a ogni risposta di Copilot e segnalare contenuti imprecisi o inappropriati per aiutare Microsoft a migliorare questa funzionalità. 

- Puoi fornire feedback utilizzando l'icona Mi piace (pollice su) o Non mi piace (pollice giù) nel riquadro **Copilot**in [!INCLUDE[prod_short](includes/prod_short.md)].
  
- Analizziamo e utilizziamo il tuo feedback sulla funzionalità per migliorare le risposte.
  
- Se riscontri contenuto generato inappropriato, segnalalo a Microsoft utilizzando questo modulo di feedback: [Segnala abuso](https://go.microsoft.com/fwlink/?linkid=2249810).
  
- Microsoft potrebbe disattivare le funzionalità basate su Copilot per clienti selezionati se viene rilevato un abuso della funzionalità.

## Quali sono le limitazioni di Chat con Copilot? In che modo gli utenti possono ridurre al minimo l'impatto delle limitazioni di Chat con Copilot durante l'utilizzo del sistema?

- Limitazioni generali dell'IA

  I sistemi di intelligenza artificiale sono strumenti preziosi, ma non deterministici. Il contenuto che generano potrebbe non essere accurato. Pertanto, è importante utilizzare il proprio giudizio per esaminare e verificare le risposte di Copilot prima di prendere decisioni che potrebbero influenzare le parti interessate come clienti e partner. Per la maggior parte delle risposte, Copilot include anche citazioni o collegamenti di riferimento che puoi utilizzare per verificare rapidamente se Copilot è arrivato alla risposta corretta. Ad esempio, quando viene chiesto come eseguire un'attività, Copilot include collegamenti all'articolo di origine. Quando viene chiesto di trovare un record in base a criteri specifici, Copilot include collegamenti che descrivono la pagina elenco identificata come argomento di conversazione. Fornisce inoltre informazioni su eventuali filtri o ordinamenti applicati per ottenere una risposta.

- Limitazioni linguistiche

  - La chat è supportata solo in inglese per le seguenti impostazioni locali inglesi: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Se la lingua di visualizzazione in [!INCLUDE[prod_short](includes/prod_short.md)] non è una di queste impostazioni locali, la chat non è disponibile.

  - La qualità delle risposte può risultare inferiore nelle seguenti condizioni:
    - L'impostazione locale relativa alla lingua è diversa da en-US.
    - L'impostazione della lingua per l'utente in [!INCLUDE[prod_short](includes/prod_short.md)] è diversa dalla lingua principale dei dati nel database di [!INCLUDE[prod_short](includes/prod_short.md)].

- Limitazioni di settore, prodotto e argomento specifiche

   La chat include meccanismi di sicurezza integrati che impediscono la generazione indesiderata di contenuti dannosi, come contenuti sessualmente espliciti o incitamento alla violenza. A volte, i clienti operano in settori, vendono prodotti e servizi o utilizzano processi che naturalmente si sovrappongono a ciò che potrebbe essere considerato inappropriato in altri contesti, oppure utilizzano dati che potrebbero far scattare queste tutele. La chat potrebbe non funzionare bene in questi casi.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## Dati che vengono raccolti da Chat con Copilot e come vengono utilizzati

Microsoft non utilizza i dati della tua società, incluso il testo che invii a Copilot, per addestrare i modelli di intelligenza artificiale fondamentali a vantaggio di altri. Gli amministratori aziendali hanno il pieno controllo sulla gestione di questi dati che fanno parte della loro sottoscrizione di Azure. Poiché gli amministratori o altre persone nella tua società potrebbero avere accesso a questi dati come stabilito dal tuo datore di lavoro, ti consigliamo di non inserire dati sensibili come password o altri segreti.

## Cosa offre Chat with Copilot a livello di sicurezza

La chat è progettata per essere sicura e viene eseguita sotto l'identità dell'utente, ereditando tutte le autorizzazioni di sicurezza e altre restrizioni e non operando mai al di fuori della sicurezza della piattaforma di [!INCLUDE[prod_short](includes/prod_short.md)]. Ciò significa che Copilot può accedere solo ai dati a cui hai accesso.

Per gli utenti con autorizzazione SUPER, la chat può individuare più facilmente i dati non protetti che in genere sono più difficili da ottenere per gli altri utenti. Le organizzazioni che non applicano il modello di sicurezza di [!INCLUDE[prod_short](includes/prod_short.md)] per limitare le tabelle e gli oggetti a cui ciascun utente o ruolo utente ha accesso, potrebbero correre un rischio elevato quando utilizzano la chat. Pertanto, consigliamo alla tua organizzazione di implementare il modello di sicurezza di [!INCLUDE[prod_short](includes/prod_short.md)] o di disattivare la chat.

## Vedere anche

- [Chat con Copilot (anteprima)](chat-with-copilot.md)

