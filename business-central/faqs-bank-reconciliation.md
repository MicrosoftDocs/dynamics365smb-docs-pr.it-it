---
title: Domande frequenti sull'assistenza per la riconciliazione dei conti correnti bancari con Copilot (anteprima)
description: 'Queste domande frequenti forniscono informazioni sulla tecnologia di IA utilizzata per riconciliare conti correnti bancari ed estratti conto in Business Central. Includono considerazioni e dettagli chiave su come viene utilizzata l''intelligenza artificiale, come è stata testata e valutata ed eventuali limitazioni specifiche.'
ms.date: 03/27/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# Domande frequenti sull'assistenza per la riconciliazione dei conti correnti bancari con Copilot (anteprima)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Queste domande frequenti descrivono l'impatto IA dell'assistenza di Microsoft Copilot sulla riconciliazione dei conti correnti bancari in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Che cos'è la funzionalità per l'assistenza per la riconciliazione dei conti correnti bancari?

La riconciliazione bancaria è un'attività contabile comune in cui le organizzazioni riesaminano i propri estratti conto per identificare le transazioni che devono essere registrate in [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, questa attività viene utilizzata per identificare commissioni bancarie periodiche o le piccole spese dei dipendenti.

La riconciliazione bancaria è in genere un processo con più passaggi. Innanzitutto gli estratti conto bancari vengono importati in [!INCLUDE[prod_short](includes/prod_short.md)]. Successivamente, le transazioni vengono associate a movimenti contabili. Infine, vengono registrate nuovi movimenti contabili per riflettere eventuali transazioni residue che non erano precedentemente note nei registri.

Copilot in [!INCLUDE[prod_short](includes/prod_short.md)] riduce lo sforzo manuale creando corrispondenze con più transazioni e suggerendo conti di contabilità generale (C/G) in cui puoi pubblicare.

## Quali sono le funzionalità dell'assistenza per la riconciliazione bancaria?

Copilot fornisce assistenza basata sull'intelligenza artificiale con due attività distinte:

- Creazione migliorata delle corrispondenze tra transazioni e movimenti contabili

    [!INCLUDE[prod_short](includes/prod_short.md)] offre regole automatizzate che creano automaticamente corrispondenze tra transazioni bancarie e movimenti contabili. Tuttavia, queste regole sono rigide e spesso danno luogo a molte transazioni senza corrispondenze, ognuna delle quali richiede un'ispezione e un confronto manuali. Copilot utilizza la tecnologia IA per ispezionare le transazioni senza corrispondenze e identificare più corrispondenze, in base a date, importi e descrizioni. Ad esempio, se un cliente ha pagato più fatture con un'unica somma forfettaria, Copilot riconcilia la singola riga dell'estratto conto con più movimenti contabili delle fatture.

- Conti C/G consigliati

    Per le transazioni bancarie residue per le quali non è stato possibile creare corrispondenze con alcun movimento contabile, Copilot utilizza la tecnologia IA per confrontare la descrizione della transazione con i nomi dei conti C/G e quindi suggerisce il conto C/G più probabile in cui effettuare la pubblicazione. Ad esempio, se le transazioni senza corrispondenze hanno la descrizione *Arresto carburante 24*, Copilot potrebbe suggerire di pubblicarle nel conto *Trasporti*.

Copilot non si connette alla tua banca per recuperare o inviare transazioni. Questa attività rimane completamente sotto il tuo controllo. Si tratta di un prerequisito per iniziare a utilizzare l'assistenza di Copilot, indipendentemente dal fatto che tali transazioni vengano aggiunte a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando una connessione bancaria digitale, importate da un file di estratto conto o inserite manualmente.

## Qual è lo scopo previsto dell'assistenza per la riconciliazione bancaria?

L'assistenza per la riconciliazione dei conti correnti bancari è progettata per migliorare l'accuratezza dei registri per aiutare i clienti a identificare le nuove transazioni di cui i clienti devono tenere conto in [!INCLUDE[prod_short](includes/prod_short.md)], . Ciò non è destinato al rilevamento di frodi o per identificare se i clienti hanno pagato in tempo.

## Come è stato valutata l'assistenza per la riconciliazione bancaria? Quali metriche vengono utilizzate per misurare le prestazioni?

L'assistenza per la riconciliazione dei conti correnti bancari è stata testata utilizzando combinazioni di dati sintetici sulle transazioni bancarie e conti C/G e movimenti contabili simili che coprono le variazioni tipiche e i limiti di dati per ciascun campo e in diverse lingue. I dati dei test rappresentano sia l'utilizzo tipico che l'utilizzo da parte di soggetti malintenzionati. Le prestazioni sono state misurate rispetto alla riconciliazione manuale degli stessi dati.

## Quali sono le limitazioni dell'assistenza per la riconciliazione bancaria? In che modo gli utenti possono ridurre al minimo l'impatto di queste limitazioni quando utilizzano il sistema?

L'assistenza per la riconciliazione dei conti correnti bancari offre prestazioni migliori quando i nomi dei conti C/G, le descrizioni dei movimenti contabili e le descrizioni delle transazioni bancarie sono tutti nella stessa lingua. Le lingue miste delle descrizioni delle transazioni spesso danno luogo a meno corrispondenze e suggerimenti.

I conti CoGe suggeriti funzionano meglio in una delle lingue supportate (vedi la sezione successiva per un elenco delle lingue). Gli utenti potrebbero riscontrare meno corrispondenze delle transazioni e meno conti CoGe suggeriti in altre lingue.

## In quali aree geografiche e lingue è disponibile l'assistenza per la riconciliazione bancaria? 

- Aree disponibili

  L'assistenza per la riconciliazione dei conti correnti bancari è disponibile in tutte le [aree geografiche/paesi di Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) supportati. Per gli ambienti dei clienti situati in paesi/aree geografiche in cui il servizio OpenAI di Azure non è distribuito, gli amministratori devono consentire lo spostamento dei dati oltre i confini per permettere la connessione di [!INCLUDE [prod_short](includes/prod_short.md)] al servizio OpenAI di Azure. Ulteriori informazioni sullo [spostamento di dati di Copilot tra aree geografiche](ai-copilot-data-movement.md).

- Lingue disponibili

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Per ulteriori informazioni sulle lingue, vedi la domanda precedente sulle limitazioni.

## Cosa ci si aspetta dagli utenti di sistema quando utilizzano l'assistenza per la riconciliazione dei conti correnti bancari?

### Durante la riconciliazione di un C/C bancario

È possibile che a volte le corrispondenze e i suggerimenti basati sull'intelligenza artificiale siano errati o incompleti. Gli utenti dell'assistenza per la riconciliazione dei conti correnti bancari devono verificare l'accuratezza delle corrispondenze e dei suggerimenti forniti da Copilot prima di scegliere di conservarli. Le corrispondenze e i suggerimenti di Copilot non vengono salvati nel database di [!INCLUDE[prod_short](includes/prod_short.md)] fino a che non selezioni il pulsante **Conservalo** e chiudi la finestra Copilot. Puoi modificare e correggere eventuali corrispondenze o suggerimenti prima di scegliere di mantenerli.

### Dopo aver completato la riconciliazione dei conti correnti bancari

Si consiglia agli utenti di verificare anche l'accuratezza e di correggere eventuali discrepanze dopo aver chiuso la finestra Copilot. Questo processo dovrebbe includere le seguenti attività:

- Esamina il report sui test della riconciliazione.
- Assicurati che la tua organizzazione disponga dei processi di revisione e audit appropriati.
- Riapri eventuali riconciliazioni pubblicate utilizzando la funzione **Annulla**.
- Correggi eventuali movimenti contabili errati mediante lo storno dei movimenti.

## Cosa ci si aspetta dagli amministratori e dagli utenti di sistema quando utilizzano l'assistenza per la riconciliazione dei conti correnti bancari?

Gli utenti di sistema, come contabili, tesorieri o altri che lavorano sulla contabilità aziendale, devono sempre verificare l'accuratezza delle corrispondenze e dei suggerimenti forniti da Copilot prima di scegliere di conservarli. Dopo la riconciliazione con Copilot, consigliamo agli utenti di riesaminare il report sui test della riconciliazione per verificarne l'accuratezza e identificare eventuali discrepanze.

Gli amministratori devono garantire che agli utenti contabili appropriati sia concesso l'accesso a questa funzionalità.

## Copilot è l'unico mezzo per completare la riconciliazione dei conti correnti bancari?

Nr. L'uso di Copilot è facoltativo. [!INCLUDE[prod_short](includes/prod_short.md)] offre mezzi tradizionali, non basati sull'intelligenza artificiale, per importare estratti conto, eseguire regole di corrispondenza predefinite e applicare manualmente corrispondenze e pubblicare nei conti CoGe appropriati. Sia l'approccio tradizionale che Copilot possono essere utilizzati contemporaneamente in un'organizzazione.

## Come posso fornire feedback sui contenuti generati dall'intelligenza artificiale?

Ogni volta che Copilot fornisce corrispondenze o suggerimenti, puoi fornire feedback a Microsoft direttamente dalla finestra di Copilot, utilizzando i controlli Mi piace e Non mi piace. Il tuo feedback rimane anonimo e usiamo questi dati per migliorare la qualità del servizio.

## Vedere anche

[Riconciliare i conti correnti bancari con Copilot (anteprima)](bank-reconciliation-with-copilot.md)
