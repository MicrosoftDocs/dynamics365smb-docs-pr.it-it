---
title: "Dettagli di progettazione: Qtà massima | Microsoft Docs"
description: "Il criterio Quantità massima è un modo per mantenere il magazzino utilizzando un punto di riordino."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 26bed0b8832d5b12ce5d697df8ec6194ac7ae9b2
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-maximum-qty"></a>Dettagli di progettazione: Qtà Massima
Il criterio Quantità massima è un modo per mantenere il magazzino utilizzando un punto di riordino.  
  
 Tutto ciò che riguarda il metodo Qtà Riordino Fissa si applica anche a questi criteri. L'unica differenza è la quantità dell'approvvigionamento suggerito. Se si utilizza il metodo della quantità massima, la quantità di riordino verrà definita in modo dinamico in base al livello delle giacenze disponibili e quindi in genere differirà da ordine a ordine.  
  
## <a name="calculated-per-time-bucket"></a>Calcolato per intervallo di tempo  
 La quantità di riordino viene determinata in un punto del tempo (alla fine di un intervallo di tempo) quando il sistema di pianificazione rileva che il punto di riordino è stato superato. A questo punto, il sistema misura l'interruzione dal livello di magazzino previsto corrente fino al magazzino massimo specificato. Ciò costituisce la quantità che deve essere riordinata. Il sistema controlla quindi se l'approvvigionamento è già stato ordinato altrove in modo che possa essere caricato entro il lead time e, in caso affermativo, riduce la quantità del nuovo ordine di approvvigionamento della quantità già ordinata.  
  
 Il sistema assicurerà che la giacenza disponibile raggiunga almeno il livello del punto di riordino, nel caso l'utente abbia dimenticato di specificare una quantità di magazzino massima.  
  
## <a name="combines-with-order-modifiers"></a>Combina con i modificatori di ordine  
 In base all'impostazione, è consigliabile combinare i criteri Quantità massima con i modificatori di ordini per garantire una quantità minima dell'ordine o per arrotondarla a un numero intero di unità di misura di acquisto, o suddividerla in più lotti come definito dalla quantità massima ordine.  
  
## <a name="combines-with-calendars"></a>Associazioni con i calendari  
 Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione verifica che l'ordine sia programmato per un giorno non lavorativo, in base ai calendari definiti nel campo **Codice calendario base** delle finestre **Informazioni società** e **Scheda Ubicazione**.  
  
 Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. In questo modo, potrebbe verificarsi che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.  
  
## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md)   
 [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
 [Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
