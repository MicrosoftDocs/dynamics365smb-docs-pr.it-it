---
title: Sintesi della riga di registrazione di contabilità generale | Microsoft Docs
description: In questo argomento vengono presentate le modifiche alla Codeunit 12, **Registrazioni Gen.-Riga di registrazione**, ovvero il principale oggetto applicazione per la registrazione di contabilità generale e la sola area per registrare contabilità generale, IVA e movimenti contabili di clienti e fornitori.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d778b29a5789d015b26b504ea8699ac64a92286c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911107"
---
# <a name="general-journal-post-line-overview"></a>Sintesi della riga di registrazione di contabilità generale
Codeunit 12, **Registrazioni Gen.-Riga di registrazione**, è il principale oggetto applicazione per la registrazione di contabilità generale ed è la sola area per registrare contabilità generale, IVA e movimenti contabili di clienti e fornitori. Questa codeunit viene inoltre utilizzata per tutte le operazioni Collega, Scollega e Storna.  
  
Mentre la codeunit è stata migliorata in ogni versione durante gli ultimi dieci anni, la relativa architettura è rimasta essenzialmente invariata. Codeunit è diventato molto grande, contiene circa 7.600 righe di codice. Con questa versione di [!INCLUDE[d365fin](includes/d365fin_md.md)], l'architettura viene modificata e la codeunit è stata resa più semplice e gestibile. La documentazione introduce le modifiche e fornisce informazioni necessarie per aggiornare.  
  
## <a name="old-architecture"></a>Architettura precedente  
L'architettura precedente aveva le seguenti funzionalità:  
  
* Era presente un utilizzo esteso delle variabili globali, il che aumentava la possibilità di errori nascosti causati dall'utilizzo di variabili con l'ambito errato.  
* Erano presenti numerose procedure lunghe (con più di 100 righe di codice) che avevano inoltre complessità ciclomatica elevata (ovvero molte istruzioni CASE, REPEAT, IF nidificate), il che ha reso il codice molto difficile da leggere e gestire.  
* Diverse procedure che erano utilizzate solo in locale e avevano lo scopo di essere utilizzate solo localmente non erano contrassegnate come locali.  
* La maggior parte delle procedure non avevano parametri e utilizzavano variabili globali. Alcuni parametri utilizzati e variabili globali sostituite con locali.  
* I modelli di codice per la ricerca dei conti di contabilità generale e la creazione di movimenti IVA e di contabilità generale non sono stati standardizzati e modificati a seconda delle aree. Inoltre, era presente molto codice duplicato e tra molti codici cliente e fornitore mancava simmetria.  
* Gran parte del codice nella codeunit 12, circa il 30%, relativo ai calcoli di tolleranza e di sconto sul pagamento, sebbene queste funzionalità non siano necessarie in molti paesi.  
* Registrazione, Collega, Scollega, Storna, Sconto e tolleranza pagamento e Rettifica tasso di cambio sono state unite nella codeunit 12 utilizzando un lungo elenco di variabili globali.  
  
### <a name="new-architecture"></a>Nuova Architettura  
In [!INCLUDE[d365fin](includes/d365fin_md.md)], sono stati apportati i seguenti miglioramenti alla codeunit 12:  
  
* Per Codeunit 12 è stato eseguito il refactoring in procedure più piccole (tutte minori di 100 righe di codice).  
* I modelli standardizzati per la ricerca dei conti di contabilità generale sono stati implementati utilizzando le funzioni di helper delle tabelle di Categoria registrazione.  
* Un Framework del motore di registrazione è stato implementato per gestire l'inizio e la fine delle transazioni e per isolare la creazione in contabilità generale, movimenti VAT, raccolta di rettifica VAT e calcolo di importi in valuta aggiuntivi.  
* La duplicazione di codice è stata eliminata.  
* Numerose funzioni di helper sono state trasferite alle corrispondenti tabelle dei movimenti contabili fornitore e cliente.  
* L'utilizzo delle variabili globali è stato minimizzato, in modo che ogni procedura utilizzi parametri e incapsuli la propria la logica di collegamento.  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: struttura dell'interfaccia di registrazione](design-details-posting-interface-structure.md)   
[Dettagli di progettazione: struttura del motore di registrazione](design-details-posting-engine-structure.md)
