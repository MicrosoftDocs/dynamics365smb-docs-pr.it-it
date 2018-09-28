---
title: 'Dettagli di progettazione: Ordine | Microsoft Docs'
description: Questo argomento fornisce informazioni a collegamenti ordine-a-ordine in un ambiente di produzione su ordine.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 38272b0d777c276c372893082680d89fc33e060c
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-order"></a>Dettagli di progettazione: Ordine
In un ambiente di produzione su ordine, un articolo viene acquistato o prodotto esclusivamente per coprire una domanda specifica. In genere si riferisce ad articoli A e le motivazioni per scegliere il metodo di riordino Ordine può essere quello di una domanda poco frequente, un lead time insignificante o la variazione degli attributi necessari.  
  
Il programma crea un collegamento ordine su ordine, che funge da connessione preliminare tra l'approvvigionamento, un ordine di approvvigionamento o il magazzino e la domanda che deve soddisfare.  
  
Oltre all'utilizzo del metodo Ordine, il collegamento ordine-a-ordine può essere applicato durante la pianificazione nei seguenti modi:  
  
* Se si utilizza la politica di produzione Produzione su ordine per creare ordini di produzione di tipo progetto o multilivello (producendo i componenti necessari nello stesso ordine di produzione).  
* Se si utilizza la funzionalità Pianifica ordine vendita per creare un ordine di produzione da un ordine di vendita.  
  
Anche se un'azienda manifatturiera si considera come ambiente di produzione su ordine, potrebbe essere meglio utilizzare un metodo di riordino lotto-per-lotto se gli articoli sono standard puro senza variazione negli attributi. Di conseguenza, verrà utilizzato il magazzino non pianificato e si accumuleranno solo ordini di vendita con la stessa data di spedizione o all'interno di un intervallo di tempo definito.  
  
## <a name="order-to-order-links-and-past-due-dates"></a>Collegamenti ordine su ordine e date di scadenza arretrate  
A differenza della maggior parte dei set di approvvigionamento-domanda, gli ordini collegati con date di scadenza precedenti alla data di inizio della pianificazione sono completamente pianificati dal sistema. Il motivo economico di questa eccezione è che la domanda e l'approvvigionamento specifici devono essere sincronizzati attraverso l'esecuzione. Per ulteriori informazioni sulla zona bloccata che si applica alla maggior parte dei tipi di domanda-approvvigionamento, vedere [Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione](design-details-dealing-with-orders-before-the-planning-starting-date.md).  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md)   
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
