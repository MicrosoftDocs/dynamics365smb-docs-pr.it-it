---
title: 'Dettagli di progettazione: Il ruolo dell''intervallo di tempo | Microsoft Docs'
description: "Lo scopo dell'intervallo di tempo è di raccogliere gli eventi di domanda nell'intervallo di tempo in modo da creare un ordine di approvvigionamento congiunto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: ff748a192d8d1650a708ab70ec33ccc7bfd53c48
ms.contentlocale: it-it
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a>Dettagli di progettazione: Il ruolo dell'intervallo di tempo
Lo scopo dell'intervallo di tempo è di raccogliere gli eventi di domanda nell'intervallo di tempo in modo da creare un ordine di approvvigionamento congiunto.  

 Per i metodi di riordino che utilizzano un punto di riordino, è possibile definire un intervallo di tempo. In questo modo si garantisce che la domanda nello stesso periodo di tempo venga accumulata prima di controllare l'impatto sulla giacenza disponibile e se il punto di riordino sia stato superato. Se il punto di riordino è passato, viene programmato un nuovo ordine di approvvigionamento in una data successiva dalla fine del periodo definito dall'intervallo di tempo. Gli intervalli di tempo iniziano con la data di inizio pianificazione.  

 Il concetto di attività in un intervallo di tempo riflette il processo manuale di controllo del livello di magazzino su base frequente anziché ad ogni transazione. L'utente deve definire la frequenza (intervallo di tempo). Ad esempio, l'utente raccoglie tutte le esigenze dell'articolo da un fornitore per inserire un ordine settimanale.  

 ![Esempio di pianificazione basata su intervallo di tempo](media/nav_app_supply_planning_2_reorder_cycle.png "Esempio di pianificazione basata su intervallo di tempo")  

 L'intervallo di tempo viene in genere utilizzato per evitare un effetto di sovrapposizione. Ad esempio, una riga equilibrata di approvvigionamento e domanda dove una domanda iniziale viene annullata o ne viene creata una nuova. Il risultato sarebbe che ogni ordine di approvvigionamento (eccetto l'ultimo) viene riprogrammato.  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md)   
 [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
 [Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)

