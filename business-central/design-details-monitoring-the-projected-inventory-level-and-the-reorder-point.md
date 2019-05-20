---
title: 'Dettagli di progettazione: Monitoraggio del livello di giacenza disponibile e del punto di riordino | Microsoft Docs'
description: Informazioni sulla distinzione tra il livello di scorte disponibili previste e il livello di giacenza disponibile per la pianificazione del magazzino.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3ab1fbc381638a31b601f872e7280d7dc5200fdb
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246337"
---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Dettagli di progettazione: Monitoraggio del livello di giacenza disponibile e del punto di riordino
Il magazzino è un tipo di approvvigionamento, ma per la pianificazione del magazzino, il sistema di pianificazione distingue tra due livelli di magazzino:  

* Quantità scorte previste  
* Scorte disponibili previste  

## <a name="projected-inventory"></a>Quantità scorte previste  
Inizialmente, la giacenza disponibile corrisponde alla quantità di giacenza lorda, inclusi approvvigionamento e domanda passati anche se non registrati, all'avvio del processo di pianificazione. In futuro, diventa un livello di giacenza disponibile mobile che viene mantenuto dalle quantità lorde di approvvigionamenti e domande futuri perché sono introdotte seguendo la linea del tempo (se impegnate o allocate in altri modi).  

La giacenza disponibile viene utilizzata dal sistema di pianificazione per monitorare il punto di riordino e per determinare la quantità di riordino quando viene utilizzato il metodo di riordino Qtà Massima.  

## <a name="projected-available-inventory"></a>Scorte disponibili previste  
Le scorte disponibili previste sono la parte della giacenza disponibile che in un dato momento è disponibile per soddisfare la domanda. Le scorte disponibili previste vengono utilizzate dal motore di pianificazione durante il monitoraggio del livello della scorta di sicurezza.  

Le scorte disponibili previste vengono utilizzate dal sistema di pianificazione per monitorare il livello di scorta di sicurezza, dal momento che la scorta di sicurezza deve essere sempre disponibile per servire la domanda imprevista.  

## <a name="time-buckets"></a>Intervalli di tempo  
È importante disporre di un controllo stretto delle scorte previste per rilevare quando viene raggiunto il punto di riordino e per calcolare le giuste quantità dell'ordine quando si utilizza il metodo di riordino Qtà massima.  

Come dichiarato in precedenza, il livello di magazzino previsto viene calcolato all'inizio del periodo di pianificazione. È un livello lordo che non considera gli impegni e le allocazioni simili. Per monitorare il livello di magazzino durante la sequenza di pianificazione, le modifiche aggregate vengono monitorate dal sistema nell'arco di un intervallo di tempo. Il sistema garantisce che l'intervallo di tempo sia almeno di un giorno perché è l'unità di tempo più precisa in caso di un evento di approvvigionamento o di domanda.  

## <a name="determining-the-projected-inventory-level"></a>Determinazione del livello di magazzino previsto  
Nella seguente sequenza viene descritto in che modo viene determinato il livello di giacenza disponibile:  

* Quando un evento di approvvigionamento, ad esempio un ordine di acquisto, è stato completamente pianificato, la giacenza disponibile verrà aumentata alla data di scadenza.  
* Una volta che un evento di domanda è stato completamente soddisfatto, la giacenza disponibile non diminuirà immediatamente. In alternativa, registra un sollecito di diminuzione, ovvero un record interno che contiene la data e la quantità di contributo alla giacenza disponibile.  
* Quando un evento di approvvigionamento successivo viene pianificato e collocato nella sequenza temporale, i solleciti di riduzione registrati vengono analizzati singolarmente fino alla data di approvvigionamento pianificata durante l'aggiornamento della giacenza disponibile. Durante il processo, potrebbe essere raggiunto o superato il livello del punto di riordino del sollecito di incremento interno.  
* Se viene immesso un nuovo ordine di approvvigionamento, nel sistema viene controllato se tale ordine viene immesso prima dell'approvvigionamento corrente. In questo caso, il nuovo approvvigionamento diventa l'approvvigionamento corrente e la procedura di contropartita rincomincia.  

Di seguito viene illustrato questo principio:  

![Determinazione del livello di magazzino previsto](media/nav_app_supply_planning_2_projected_inventory.png "Determinazione del livello di magazzino previsto")  

1. L'approvvigionamento **Sa** di 4 (fisso) chiude la domanda **Da** di -3.  
2. CloseDemand: Creare un sollecito di riduzione di -3 (non visualizzato).  
3. L'approvvigionamento **Sa** viene chiuso con un surplus di 1 (non esiste più domanda).  

     Ciò aumenta il livello di scorte previste a +4, mentre la giacenza **disponibile** diventa -1.  

4. Il successivo approvvigionamento **Sb** di 2 (un altro ordine) è già stato immesso nella sequenza temporale.  
5. Il sistema controlla se esiste un sollecito di riduzione precedente a **Sb**; in caso negativo, non viene intrapresa alcuna azione.  
6. Il sistema chiude l'approvvigionamento **Sb** (non esiste più domanda) riducendolo a 0 (annullamento) o lasciandolo invariato.  

     Ciò aumenta il livello del magazzino previsto (A: +0 => +4 o B: +2 = +6).  

7. Il sistema esegue un controllo finale: è presente un sollecito di riduzione? Sì, ne esiste uno alla data di **Da**.  
8. Viene aggiunto un sollecito di diminuzione dal sistema di -3 al livello di giacenza disponibile, A: +4 -3 = 1 o B: +6 -3 = +3.  
9. Nel caso di A, il sistema crea un ordine programmato in avanti che inizia alla data indicata di **Da**.  

     Nel caso di B, viene raggiunto il punto di riordino e viene creato un nuovo ordine.  

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md)   
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
