---
title: 'Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione | Microsoft Docs'
description: In questo argomento vengono descritte le regole che la pianificazione applica agli ordini nella zona bloccata.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4fc4afa14f9f2a989fae0b1ca8ee0e61fe24fd21
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione
Per evitare che un piano di approvvigionamento mostri suggerimenti impossibili e pertanto inutili, il sistema di pianificazione considera il periodo fino alla data di inizio pianificazione come una zona bloccata nella quale nulla viene pianificato. La seguente regola si applica alla zona bloccata:  
  
Tutta le domande e l'approvvigionamento prima della data di inizio del periodo di pianificazione verranno considerati come parte del magazzino o saranno spediti.  
  
Di conseguenza, il sistema di pianificazione non suggerisce, con poche eccezioni, modifiche agli ordini di approvvigionamento nella zona bloccata e nessun collegamento di tracciabilità viene creato o gestito per quel periodo.  
  
Le eccezioni a questa regola sono:  
  
* Se le scorte disponibili previste, inclusa la somma di domanda e approvvigionamento nella zona bloccata, è inferiore a zero.  
* Se i numeri seriali o di lotto sono obbligatori negli ordini retrodatati.  
* Se il set di approvvigionamento-domanda è collegato da un metodo ordine su ordine.  
  
Se la giacenza disponibile iniziale è minore di zero, il sistema di pianificazione suggerisce un ordine di approvvigionamento di emergenza datato il giorno precedente al periodo di pianificazione per coprire la quantità mancante. Di conseguenza, il magazzino previsto e disponibile sarà sempre almeno uguale a zero quando inizia la pianificazione per il periodo futuro. Nella riga di pianificazione per questo ordine di approvvigionamento verrà visualizzata un'icona di avviso di emergenza. Verranno inoltre fornite informazioni aggiuntive su ricerca.  
  
## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>I numeri seriali o di lotto e i collegamenti ordine su ordine sono esenti dalla zona bloccata  
Se i numeri seriali o di lotto sono obbligatori o è presente un collegamento ordine su ordine, il sistema di pianificazione ignorerà la zona bloccata e includerà tali quantità che sono retrodatate dalla data iniziale e potenzialmente suggerirà delle azioni correttive se la domanda e l'approvvigionamento non sono sincronizzati. Il motivo economico di questo principio è che questo specifico set di domanda e approvvigionamento deve corrispondere per garantire che la domanda specifica sia soddisfatta completamente.  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
