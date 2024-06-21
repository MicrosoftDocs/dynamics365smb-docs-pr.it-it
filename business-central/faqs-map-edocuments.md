---
title: Domande frequenti sul mapping di documenti elettronici a ordini di acquisto
description: 'Queste domande frequenti forniscono informazioni sulla tecnologia di intelligenza artificiale utilizzata in Business Central, insieme a considerazioni e dettagli chiave su come viene utilizzata l''intelligenza artificiale, come è stata testata e valutata ed eventuali limitazioni specifiche.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# Domande frequenti sul mapping di documenti elettronici a ordini di acquisto utilizzando Copilot (anteprima)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Queste domande frequenti descrivono l'impatto della funzionalità **Assistenza per la corrispondenza dei documenti elettronici** sull'intelligenza artificiale in [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Che cos'è l'assistenza per la corrispondenza dei documenti elettronici?

I documenti elettronici fungono da spina dorsale delle moderne transazioni commerciali. Rappresentano documenti critici come fatture e ricevute che fluiscono in entrambe le direzioni attraverso la consegna e il ricevimento. Puoi generare e trasmettere fatture elettroniche digitalmente in un formato strutturato che facilita l'elaborazione automatizzata delle fatture. Tuttavia, la gestione delle fatture digitali in entrata può essere più complessa per i team addetti alla contabilità fornitori.  

Nelle piccole e medie imprese (PMI), il team della contabilità fornitori svolge un ruolo fondamentale nel monitorare accuratamente gli obblighi dei fornitori. La loro responsabilità principale è registrare accuratamente le fatture in entrata. Raggiungere la precisione può richiedere un certo impegno, in particolare quando si riconciliano le fatture esterne dei fornitori con gli ordini di acquisto esistenti. Le discrepanze in codici, descrizioni e unità di misura spesso comportano delle sfide perché questi elementi potrebbero non corrispondere in sistemi e società diversi. Inoltre, i costi imprevisti, come le spese di trasporto, potrebbero essere visualizzati come voci separate che richiedono una rettifica manuale. I contabili devono includere nei documenti anche i numeri e le date delle fatture. È importante sottolineare che la relazione tra ordini di acquisto e fatture esterne non è sempre uno a uno. Potresti ricevere più fatture esterne per lo stesso ordine di acquisto.

Storicamente, [!INCLUDE [prod_short](includes/prod_short.md)]  potrebbe generare nuove fatture di acquisto sulla base delle fatture elettroniche ricevute. Tuttavia, abbinare manualmente le fatture agli ordini di acquisto esistenti era un processo lungo e soggetto a errori.

La funzionalità **Assistenza per la corrispondenza dei documenti elettronici** utilizza l'intelligenza artificiale generativa per semplificare questo processo automatizzando l'analisi delle fatture elettroniche esterne. Consente ai contabili di chiedere a Copilot di trovare una corrispondenza tra le righe nelle fatture elettroniche in entrata e le righe negli ordini di acquisto in [!INCLUDE [prod_short](includes/prod_short.md)].

## Quali sono le funzionalità dell'assistenza per la corrispondenza dei documenti elettronici?

Copilot fornisce assistenza basata sull'intelligenza artificiale per trovare una corrispondenza tra la fattura digitale ricevuta e gli ordini di acquisto esistenti in [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot trova la corrispondenza con le righe in base a quanto segue:

- Somiglianza delle descrizioni
- Unità di misura
- Quantità disponibili per la fatturazione
- Importi

Copilot identifica le descrizioni simili se hanno unità di misura e prezzi adeguati, ma può anche trovare corrispondenze in casi più complessi. Ad esempio, può identificare se una fattura elettronica ha due righe con una variante dello stesso articolo e una sola riga nell'ordine di acquisto; [!INCLUDE [prod_short](includes/prod_short.md)] cerca la corrispondenza con queste righe purché le descrizioni siano simili e i prezzi siano gli stessi.

Copilot non si connette al servizio endpoint dei documenti elettronici per recuperare o inviare giustificativi digitali. Questa attività rimane completamente sotto il tuo controllo ed è un prerequisito per utilizzare l'assistenza di Copilot. Ciò è vero indipendentemente dal fatto che i documenti digitali vengano aggiunti a [!INCLUDE [prod_short](includes/prod_short.md)] utilizzando una connessione con un servizio endpoint o immessi manualmente.  

## Qual è l'uso previsto dell'assistenza per la corrispondenza dei documenti elettronici?  

L'obiettivo della funzionalità **Assistenza per la corrispondenza dei documenti elettronici** è assistere il team della contabilità fornitori a trovare una corrispondenza tra gli ordini di acquisto esistenti e le fatture elettroniche in entrata. Gran parte di questa attività ruota attorno alla corrispondenza delle stringhe. [!INCLUDE [prod_short](includes/prod_short.md)] offre una funzionalità che automatizza parte di questa attività e i LLM sono stati identificati come un'opportunità per integrare tale funzionalità e ridurre ulteriormente lo sforzo manuale.  

## Come è stata valutata l'assistenza per la corrispondenza dei documenti elettronici? Quali metriche vengono utilizzate per misurare le prestazioni?

Questa funzionalità è stata testata utilizzando combinazioni delle seguenti informazioni:

- Descrizioni di articoli esterni
- Unità di misura
- Quantità e importi
- Descrizioni di articoli standard
- Lingue differenti
- Altri parametri che coprono le variazioni tipiche e i limiti dei dati per ciascun campo 

I dati dei test rappresentano sia l'utilizzo tipico che l'utilizzo da parte di soggetti malintenzionati. Le prestazioni sono state misurate rispetto alla corrispondenza manuale degli stessi dati nelle fatture elettroniche e negli ordini di acquisto.

## Quali sono le limitazioni dell'assistenza per la corrispondenza dei documenti elettronici? In che modo gli utenti possono ridurre al minimo l'impatto delle limitazioni dell'assistenza per la corrispondenza dei documenti elettronici quando utilizzano il sistema?

L'**assistenza per la corrispondenza dei documenti elettronici** offre prestazioni migliori quando le descrizioni degli articoli esterni (fattura elettronica) e interni ([!INCLUDE [prod_short](includes/prod_short.md)]) e le unità di misura sono tutte nella stessa lingua. Le lingue miste o la lingua mista delle descrizioni degli articoli spesso danno luogo a meno corrispondenze e suggerimenti.  

La corrispondenza suggerita degli articoli delle fatture elettroniche con gli articoli degli ordini di acquisto funziona meglio in lingua inglese. Anche se puoi utilizzare questa funzionalità in qualsiasi lingua che [!INCLUDE [prod_short](includes/prod_short.md)] supporta, potresti riscontrare meno corrispondenze di articoli in altre lingue.

## In quali aree geografiche e lingue è disponibile l'assistenza per la corrispondenza dei documenti elettronici? 

Questa funzionalità è disponibile per la localizzazione di qualsiasi paese/area geografica dell'ambiente e in qualsiasi lingua dell'utente ad eccezione del Canada. A causa del supporto linguistico limitato, la funzionalità non è inizialmente disponibile per i clienti canadesi non soddisfa la conformità linguistica normativa. 

Per gli ambienti dei clienti situati in paesi/aree geografiche in cui il servizio OpenAI di Azure non è distribuito, questa funzionalità è disponibile se gli amministratori dapprima consentono lo spostamento dei dati oltre i confini affinché [!INCLUDE [prod_short](includes/prod_short.md)] si connetta al servizio OpenAI di Azure.  

Per ulteriori informazioni sulla lingua, vedi [Quali sono le limitazioni dell'assistenza per la corrispondenza dei documenti elettronici? In che modo gli utenti possono ridurre al minimo l'impatto delle limitazioni dell'assistenza per la corrispondenza dei documenti elettronici quando utilizzano il sistema?](#what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system).   

## Quali fattori operativi e impostazioni consentono un uso efficace e responsabile della funzionalità?

Copilot integra l'algoritmo di mapping che [!INCLUDE [prod_short](includes/prod_short.md)] già fornisce e mappa le righe che l'algoritmo non ha fornito.

### Cosa ci si aspetta dagli utenti finali durante l'utilizzo dell'assistenza per la corrispondenza dei documenti elettronici?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Dopo aver mappato le fatture elettroniche in entrata agli ordini di acquisto, devi mappare le righe nei documenti.

La pagina **Mapping ordini di acquisto** mostra tutte le righe di entrambi i documenti. Qui puoi eseguire il mapping manualmente, il che può essere difficile se ci sono molte righe.

Puoi utilizzare l'**assistenza per la corrispondenza dei documenti elettronici** per mappare le righe in base ai seguenti criteri:

- Somiglianza nelle descrizioni
- Unità di misura
- Quantità disponibili per la fatturazione
- Importi

Le corrispondenze di Copilot potrebbero essere errate o incomplete. Devi sempre verificarne l'accuratezza prima di scegliere di mantenerle. Le corrispondenze e i suggerimenti di Copilot vengono salvati in [!INCLUDE [prod_short](includes/prod_short.md)] quando scegli **Mantieni** ed esci da Copilot. Puoi modificare e correggere eventuali corrispondenze o suggerimenti prima di scegliere di mantenerli. 

### Cosa ci si aspetta dagli amministratori e dagli utenti finali quando si utilizza l'assistenza per la corrispondenza dei documenti elettronici?

Gli utenti finali, come i contabili, o altre persone che ricevono fatture elettroniche devono sempre verificare l'accuratezza delle corrispondenze e dei suggerimenti forniti da Copilot prima di scegliere di mantenerli. Ti consigliamo di esaminare le righe degli ordini di acquisto per verificarne l'accuratezza e individuare eventuali discrepanze. Sei tu a decidere se utilizzare o meno l'**assistenza per la corrispondenza dei documenti elettronici**. Anche quando la funzionalità **assistenza per la corrispondenza dei documenti elettronici** è abilitata dagli amministratori e disponibile, puoi sempre scegliere di utilizzarla sempre, a volte o mai.  

Gli amministratori decidono se utilizzare Copilot in [!INCLUDE [prod_short](includes/prod_short.md)]. Se abilitano Copilot, gli amministratori devono assicurarsi di concedere l'accesso agli utenti appropriati.

> [NOTE!]
> - Non supportiamo questa funzionalità per [!INCLUDE [prod_short](includes/prod_short.md)] locale o in cloud privati.
> - I partner non possono estendere questa funzionalità. Gli sviluppatori partner non possono modificare, sostituire o estendere questa funzionalità. 

## Copilot è l'unico modo per trovare corrispondenze tra documenti elettronici e ordini di acquisto?  

No, sei tu a decidere se utilizzare o meno Copilot. [!INCLUDE [prod_short](includes/prod_short.md)] offre modalità non basate sull'intelligenza artificiale per trovare corrispondenze tra articoli della fattura elettronica ricevuta ad articoli in ordini di acquisto in [!INCLUDE [prod_short](includes/prod_short.md)]. Le organizzazioni possono anche utilizzare entrambi gli approcci contemporaneamente.  

## Come posso fornire feedback sui contenuti generati dall'intelligenza artificiale?  

Ogni volta che Copilot fornisce corrispondenze o suggerimenti, puoi fornire feedback a Microsoft direttamente dalla finestra di Copilot, utilizzando i controlli Mi piace e Non mi piace. Il tuo feedback rimane anonimo e usiamo questi dati per migliorare la qualità del servizio.  

## Vedere anche

[Panoramica dei documenti elettronici](finance-edocuments-overview.md)
[Mappare documenti elettronici per acquistare righe di ordini di acquisto con Copilot](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
