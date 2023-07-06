---
title: Sintesi della riga di registrazione di contabilità generale
description: 'Questo argomento introduce le modifiche a Codeunit 12, Gen. Jnl.-Post Line ed è la sola area in cui inserire i movimenti di contabilità generale, IVA e clienti e fornitori.'
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, general ledger, post'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="general-journal-post-line-overview"></a><a name="general-journal-post-line-overview"></a><a name="general-journal-post-line-overview"></a>Sintesi della riga di registrazione di contabilità generale

Codeunit 12, **Registrazioni Gen.-Riga di registrazione**, è il principale oggetto applicazione per la registrazione di contabilità generale ed è la sola area per registrare contabilità generale, IVA e movimenti contabili di clienti e fornitori. Questa codeunit viene inoltre utilizzata per tutte le operazioni Collega, Scollega e Storna.  
  
In Microsoft Dynamics NAV 2013 R2, la codeunit è stata ridisegnata perché era diventata molto grande, con circa 7.600 righe di codice. Questa architettura è stato modificata e la codeunit è stata resa più semplice e gestibile. La documentazione descrive le modifiche e fornisce informazioni necessarie per aggiornare.  
  
## <a name="old-architecture"></a><a name="old-architecture"></a><a name="old-architecture"></a>Architettura precedente
L'architettura precedente aveva le seguenti funzionalità:  
  
* Era presente un utilizzo esteso delle variabili globali, il che aumentava la possibilità di errori nascosti causati dall'utilizzo di variabili con l'ambito errato.  
* Erano presenti numerose procedure lunghe (con più di 100 righe di codice) che avevano inoltre complessità ciclomatica elevata (ovvero molte istruzioni CASE, REPEAT, IF nidificate), il che ha reso il codice molto difficile da leggere e gestire.  
* Diverse procedure che erano utilizzate solo in locale e avevano lo scopo di essere utilizzate solo localmente non erano contrassegnate come locali.  
* La maggior parte delle procedure non avevano parametri e utilizzavano variabili globali. Alcuni parametri utilizzati e variabili globali sostituite con locali.  
* I modelli di codice per la ricerca dei conti di contabilità generale e la creazione di movimenti IVA e di contabilità generale non sono stati standardizzati e modificati a seconda delle aree. Inoltre, era presente molto codice duplicato e tra molti codici cliente e fornitore mancava simmetria.  
* Gran parte del codice nella codeunit 12, circa il 30%, relativo ai calcoli di tolleranza e di sconto sul pagamento, sebbene queste funzionalità non siano necessarie in molti paesi.  
* Registrazione, Collega, Scollega, Storna, Sconto e tolleranza pagamento e Rettifica tasso di cambio sono state unite nella codeunit 12 utilizzando un lungo elenco di variabili globali.  
  
### <a name="new-architecture"></a><a name="new-architecture"></a><a name="new-architecture"></a>Nuova Architettura
In [!INCLUDE[prod_short](includes/prod_short.md)], sono stati apportati i seguenti miglioramenti alla codeunit 12:  
  
* Per Codeunit 12 è stato eseguito il refactoring in procedure più piccole (tutte minori di 100 righe di codice).  
* I modelli standardizzati per la ricerca dei conti di contabilità generale sono stati implementati utilizzando le funzioni di helper delle tabelle di Categoria registrazione.  
* Un Framework del motore di registrazione è stato implementato per gestire l'inizio e la fine delle transazioni e per isolare la creazione in contabilità generale, movimenti VAT, raccolta di rettifica VAT e calcolo di importi in valuta aggiuntivi.  
* La duplicazione di codice è stata eliminata.  
* Numerose funzioni di helper sono state trasferite alle corrispondenti tabelle dei movimenti contabili fornitore e cliente.  
* L'utilizzo delle variabili globali è stato minimizzato, in modo che ogni procedura utilizzi parametri e incapsuli la propria la logica di collegamento.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedi anche

[Dettagli di progettazione: Struttura dell'interfaccia di registrazione](design-details-posting-interface-structure.md)  
[Dettagli di progettazione: struttura del motore di registrazione](design-details-posting-engine-structure.md)  
[Dettagli di progettazione: Riga di registrazione di contabilità generale (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
