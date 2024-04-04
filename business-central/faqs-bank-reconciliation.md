---
title: Domande frequenti sull'assistenza per la riconciliazione dei conti correnti bancari (anteprima) con Copilot
description: 'Queste domande frequenti forniscono informazioni sulla tecnologia di IA utilizzata per riconciliare conti correnti bancari ed estratti conto in Business Central. Includono considerazioni e dettagli chiave su come viene utilizzata l''intelligenza artificiale, come è stata testata e valutata ed eventuali limitazioni specifiche.'
ms.date: 11/07/2023
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

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Domande frequenti sull'assistenza per la riconciliazione dei conti correnti bancari (anteprima) con Copilot

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Queste domande frequenti descrivono l'impatto IA dell'assistenza di Copilot sulla riconciliazione dei conti correnti bancari in [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="what-is-bank-reconciliation-assist"></a>Che cos'è la funzionalità per l'assistenza per la riconciliazione dei conti correnti bancari?

La riconciliazione bancaria è un'attività contabile comune in cui le organizzazioni riesaminano i propri estratti conto per identificare le transazioni che devono essere registrate in [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, questa attività verrebbe utilizzata per identificare commissioni bancarie periodiche o le piccole spese dei dipendenti. Questa attività è in genere un processo in più fasi, che inizia con l'importazione degli estratti conto in [!INCLUDE[prod_short](includes/prod_short.md)], seguito dalla creazione di corrispondenze tra le transazioni e i movimenti contabili e dalla pubblicazione di nuovi movimenti contabili per riflettere eventuali transazioni residue che non erano precedentemente note nei registri. Copilot in [!INCLUDE[prod_short](includes/prod_short.md)] riduce lo sforzo manuale creando corrispondenze con più transazioni e suggerendo conti di contabilità generale in cui puoi pubblicare. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Quali sono le funzionalità dell'assistenza per la riconciliazione bancaria?

Copilot fornisce assistenza basata sull'intelligenza artificiale con due attività distinte: 

- Creazione migliorata delle corrispondenze tra transazioni e movimenti contabili 

   [!INCLUDE[prod_short](includes/prod_short.md)] offre regole automatizzate che creano automaticamente corrispondenze tra transazioni bancarie e movimenti contabili. Tuttavia, queste regole sono rigide e spesso danno luogo a molte transazioni senza corrispondenze, ognuna delle quali richiede un'ispezione e un confronto manuali. Copilot utilizza la tecnologia IA per ispezionare le transazioni rimanenti e identificare più corrispondenze, in base a date, importi e descrizioni. Ad esempio, se più fatture sono state pagate come un'unica somma forfettaria da un cliente, Copilot riconcilia la singola riga dell'estratto conto con più movimenti contabili delle fatture. 
 
- Conti di contabilità generale suggeriti 

   Per le transazioni bancarie residue per le quali non è stato possibile creare corrispondenze con alcun movimento contabile, Copilot utilizza la tecnologia IA per confrontare la descrizione della transazione con i nomi dei conti C/G, suggerendo il conto C/G più probabile in cui effettuare la pubblicazione. Ad esempio, Copilot potrebbe suggerire che la transazione con la descrizione "Arresto carburante 24" venga pubblicata nel conto "Trasporti". 

Copilot non si connette alla tua banca per recuperare o inviare transazioni. Questa attività rimane completamente sotto il tuo controllo ed è un prerequisito per iniziare a utilizzare l'assistenza di Copilot, indipendentemente dal fatto che tali transazioni vengano aggiunte a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando una connessione bancaria digitale, importate da un file di estratto conto o inserite manualmente. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Qual è lo scopo previsto dell'assistenza per la riconciliazione bancaria?

L'assistenza per la riconciliazione dei conti correnti bancari è progettata per aiutare a identificare le nuove transazioni di cui i clienti devono tenere conto in [!INCLUDE[prod_short](includes/prod_short.md)], per migliorare l'accuratezza dei loro registri. Questa attività non è destinata al rilevamento o all'identificazione di frodi se i clienti hanno pagato in tempo.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Come è stato valutata l'assistenza per la riconciliazione bancaria? Quali metriche vengono utilizzate per misurare le prestazioni?

Questa funzionalità è stata testata utilizzando combinazioni di dati sintetici sulle transazioni bancarie e conti C/G e movimenti contabili simili che coprono le variazioni tipiche e i limiti di dati per ciascun campo e in diverse lingue. I dati dei test rappresentano sia l'utilizzo tipico che l'utilizzo da parte di soggetti malintenzionati. Le prestazioni sono state misurate rispetto alla riconciliazione manuale degli stessi dati. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Quali sono le limitazioni dell'assistenza per la riconciliazione bancaria? In che modo gli utenti possono ridurre al minimo l'impatto delle limitazioni della riconciliazione bancaria durante l'utilizzo del sistema?

L'assistenza per la riconciliazione dei conti correnti bancari offre prestazioni migliori quando i nomi dei conti C/G, le descrizioni dei movimenti contabili e le descrizioni delle transazioni bancarie sono tutti nella stessa lingua. Le lingue miste delle descrizioni delle transazioni spesso danno luogo a meno corrispondenze e suggerimenti. 

I conti CoGe suggeriti offrono migliori prestazioni in lingua inglese. Sebbene questa funzionalità possa essere utilizzata in una qualsiasi delle lingue [!INCLUDE[prod_short](includes/prod_short.md)] disponibili, gli utenti potrebbero riscontrare meno corrispondenze delle transazioni e meno conti CoGe suggeriti in altre lingue. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>In quali aree geografiche e lingue è disponibile l'assistenza per la riconciliazione bancaria?

Questa funzionalità è disponibile per la localizzazione di qualsiasi paese/regione dell'ambiente e in qualsiasi lingua dell'utente. Per gli ambienti dei clienti situati in paesi/aree geografiche in cui il servizio OpenAI di Azure non è distribuito, gli amministratori devono prima consentire lo spostamento dei dati oltre i confini affinché [!INCLUDE[prod_short](includes/prod_short.md)] si connetta al servizio OpenAI di Azure e questa funzionalità sia disponibile. 

Per ulteriori informazioni sulla lingua, vedi la domanda precedente sulle limitazioni.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Cosa ci si aspetta dagli utenti finali quando si utilizza l'assistenza per la riconciliazione dei conti correnti bancari?

### <a name="while-using-bank-account-reconciliation"></a>Durante l'uso della riconciliazione dei conti correnti bancari

È possibile che a volte le corrispondenze e i suggerimenti basati sull'intelligenza artificiale siano errati o incompleti. Gli utenti dell'assistenza per la riconciliazione dei conti correnti bancari devono verificare l'accuratezza delle corrispondenze e dei suggerimenti forniti da Copilot prima di scegliere di conservarli. Le corrispondenze e i suggerimenti di Copilot non vengono salvati nel database di [!INCLUDE[prod_short](includes/prod_short.md)] fino a che non scegli il pulsante Conservalo ed esci dalla finestra Copilot. Puoi anche modificare e correggere eventuali corrispondenze o suggerimenti prima di scegliere di conservarlo. 

### <a name="after-completing-bank-account-reconciliation"></a>Dopo aver completato la riconciliazione dei conti correnti bancari

Si consiglia agli utenti di verificare anche l'accuratezza e di correggere eventuali discrepanze dopo aver chiuso la finestra Copilot, comprese le seguenti attività: 

- Esamina il report sui test della riconciliazione. 
- Assicurati che la tua organizzazione disponga dei processi di revisione e audit appropriati. 
- Riapri eventuali riconciliazioni pubblicate utilizzando la funzione Annulla. 
- Correggi eventuali movimenti contabili errati mediante lo storno dei movimenti. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Cosa ci si aspetta dagli amministratori e dagli utenti finali quando si utilizza l'assistenza per la riconciliazione dei conti correnti bancari?

Gli utenti finali, come contabili, tesorieri o altri che lavorano sulla contabilità aziendale, devono sempre verificare l'accuratezza delle corrispondenze e dei suggerimenti forniti da Copilot prima di scegliere di conservarli. Dopo la riconciliazione con Copilot, consigliamo di riesaminare il report sui test della riconciliazione per verificarne l'accuratezza e identificare eventuali discrepanze. 

Gli amministratori devono garantire che agli utenti contabili appropriati sia stato concesso l'accesso a questa funzionalità. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Copilot è l'unico mezzo per completare la riconciliazione dei conti correnti bancari?

No. L'uso di Copilot è facoltativo. [!INCLUDE[prod_short](includes/prod_short.md)] offre mezzi tradizionali, non basati sull'intelligenza artificiale, per importare estratti conto, eseguire regole di corrispondenza predefinite e applicare manualmente corrispondenze e pubblicare nei conti CoGe appropriati. Sia l'approccio tradizionale che Copilot possono essere utilizzati contemporaneamente in un'organizzazione. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Come posso fornire feedback sui contenuti generati dall'intelligenza artificiale?

Ogni volta che Copilot fornisce corrispondenze o suggerimenti, puoi fornire feedback a Microsoft direttamente dalla finestra di Copilot, utilizzando i controlli Mi piace e Non mi piace. Il tuo feedback rimane anonimo e usiamo questi dati per migliorare la qualità del servizio.


## <a name="see-also"></a>Vedere anche

[Riconciliare conti correnti bancari utilizzando l'assistenza per la riconciliazione di conti correnti bancari (anteprima)](bank-reconciliation-with-copilot.md)
