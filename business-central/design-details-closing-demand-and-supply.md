---
title: 'Dettagli di progettazione: Chiusura domanda e approvvigionamento | Microsoft Docs'
description: In questo argomento viene fornito un suggerimento sulle azioni da eseguire dopo l'esecuzione delle procedure di contropartita di approvvigionamento.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, planning, example, closing, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6cacf967295944ba720c20203700db30d9ec45c4
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-closing-demand-and-supply"></a>Dettagli di progettazione: Chiusura domanda e approvvigionamento
Una volta che sono state eseguite le procedure di contropartita di approvvigionamento, sono disponibili tre casi finali possibili:  
  
* La quantità e la data necessarie degli eventi di domanda sono state soddisfatte e la relativa pianificazione può essere chiusa. L'evento di approvvigionamento è ancora aperto e può essere in grado di soddisfare la domanda successiva, pertanto la procedura di contropartita può rincominciare con l'evento di approvvigionamento corrente e la domanda successiva.  
* L'ordine di approvvigionamento non può essere modificato per soddisfare tutta la domanda. Un evento di domanda è ancora aperto, con una quantità scoperta che può essere coperta dal successivo evento di approvvigionamento. L'evento di approvvigionamento corrente viene quindi chiuso, in modo che l'azione di bilanciamento posso riprendere dall'inizio con gli eventi domanda corrente e approvvigionamento successivo.  
* Tutta la domanda è stata coperta; non esiste alcuna domanda successiva (o non c'è stata alcuna domanda). Se esiste un surplus di approvvigionamento, può essere ridotto (o annullato) e quindi chiuso. È possibile che degli eventi di approvvigionamento aggiuntivi persistano nella catena, nel qual caso anch'essi devono essere annullati.  
  
Infine, il sistema di pianificazione creerà un collegamento di tracciabilità ordine tra approvvigionamento e domanda.  
  
## <a name="creating-the-planning-line-suggested-action"></a>Creazione della riga di pianificazione (azione suggerita)  
Se viene suggerita una qualsiasi azione, ad esempio nuovo, modifica della quantità, riprogrammazione e modifica della quantità o annullamento, per esaminare l'ordine di approvvigionamento, tramite il sistema di pianificazione viene creata una riga di pianificazione nel prospetto di pianificazione. A causa della tracciabilità dell'ordine, la riga di pianificazione viene creata non solo al momento della chiusura dell'evento di approvvigionamento, ma anche se l'evento della domanda è chiuso, anche se l'evento di approvvigionamento è ancora aperto e potrebbe essere soggetto a ulteriori modifiche quando viene elaborata la domanda successiva. Ciò significa che, una volta creata, la riga di pianificazione può essere modificata nuovamente.  
  
Per ridurre al minimo l'accesso al database durante la gestione degli ordini di produzione, la riga di pianificazione può essere gestita a tre livelli, mirando al contempo a eseguire il livello di manutenzione meno impegnativo:  
  
* Creare solo la riga di pianificazione con la data di scadenza e la quantità corrente ma senza il ciclo e i componenti.  
* Includere il ciclo: il ciclo di produzione pianificato viene steso includendo il calcolo delle date di inizio e di fine e dei periodi. Ciò risulta molto impegnativo in termini di accessi al database. Per determinare le date di scadenza e di fine, può essere necessario calcolare anche se l'evento di approvvigionamento non è stato chiuso (nel caso di programmazione in avanti).  
* Includere l'esplosione della distinta base: questa operazione può attendere fino a poco prima della chiusura dell'evento approvvigionamento.  
  
Ciò conclude le descrizioni delle modalità di caricamento, di assegnazione di priorità e di bilanciamento di domanda e approvvigionamento nel sistema di pianificazione. A integrazione di questa attività di pianificazione dell'approvvigionamento, il sistema deve garantire che il livello di magazzino richiesto di ciascun articolo pianificato sia mantenuto in base al relativo metodo di riordino.  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
