---
title: 'Dettagli di progettazione: Lotto-per-Lotto | Microsoft Docs'
description: "Informazioni su come utilizzare il metodo lotto-per lotto per stabilire la quantità dell'ordine in base alla domanda."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 712068b5fafb8c5334bf48ddfc9242d21c0995e9
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-lot-for-lot"></a>Dettagli di progettazione: Lotto-per-Lotto
I criteri lotto per lotto sono i più flessibili perché il sistema reagisce solo alla domanda effettiva, agiscono inoltre sulla domanda prevista dalla previsione e dagli ordini programmati e stabiliscono la quantità dell'ordine in base alla domanda. I criteri lotto per lotto sono destinati agli elementi A e B dove il magazzino può essere accettato ma dovrebbe essere evitato.  
  
Per certi aspetti, il metodo lotto per lotto è simile al metodo Ordine, ma presenta un approccio generico agli articoli; può accettare quantità in magazzino e aggrega la domanda e il corrispondente approvvigionamento in intervalli di tempo definiti dall'utente.  
  
L'intervallo di tempo è definito nel campo **Intervallo di tempo**. Il sistema utilizza l'intervallo di tempo minimo pari a un giorno, che è l'unità di misura più piccola per gli eventi di domanda e approvvigionamento offerta dal sistema (sebbene, nella pratica, gli ordini di produzione e le richieste di componenti possano essere misurate in secondi).  
  
L'intervallo di tempo fissa anche dei limiti sui tempi di riprogrammazione di un ordine di approvvigionamento esistente per soddisfare una domanda specificata. Se l'approvvigionamento rientra nell'intervallo di tempo, viene riprogrammato all'interno o all'esterno in modo da soddisfare la domanda. In caso contrario, se risiede in un periodo precedente, causerà un accumulo di magazzino inutile e dovrà essere annullato. Se risiede dopo, verrà invece creato un nuovo ordine di approvvigionamento.  
  
Con questo metodo, è possibile definire una scorta di sicurezza per compensare possibili fluttuazioni nell'approvvigionamento o per soddisfare una domanda improvvisa.  
  
Poiché la quantità dell'ordine di approvvigionamento è basato sulla domanda effettiva e può essere sensato utilizzare i modificatori di ordini: arrotondare la quantità di ordine fino a soddisfare un multiplo dell'ordine specificato (o unità di misura dell'acquisto), aumentare l'ordine a una quantità ordine minima specificata oppure diminuire la quantità alla quantità massima specificata (e creare quindi due o più approvvigionamenti per raggiungere la quantità necessaria totale).  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Metodi di riordino](design-details-reordering-policies.md)   
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
