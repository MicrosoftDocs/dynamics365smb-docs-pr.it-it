---
title: "Dettagli di progettazione: Assegnazione priorità ordini | Microsoft Docs"
description: "Informazioni su come assegnare le priorità per soddisfare domanda e approvvigionamento."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7af645f5a9dd7f34619d05cb2d4f0f7f8ad1921d
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-prioritizing-orders"></a>Dettagli di progettazione: Assegnazione priorità ordini
All'interno di una determinata USK, la data richiesta o disponibile rappresenta la priorità più alta; la domanda della data corrente deve essere gestita prima della domanda della settimana successiva. Ma oltre a questa priorità globale, il sistema di pianificazione suggerirà inoltre il tipo di domanda da soddisfare prima di soddisfarne un'altra. Analogamente, verrà suggerito quale origine di approvvigionamento deve essere collegata prima di collegare altre origini di approvvigionamento. Questa operazione viene eseguita in base alle priorità degli ordini.  
  
La domanda e l'approvvigionamento caricati contribuiscono a un profilo per la giacenza disponibile in base alle seguenti priorità:  
  
## <a name="priorities-on-the-demand-side"></a>Priorità sul lato della domanda  
1. Già spediti: Mov. contabili articolo  
2. Ordine di reso acquisto  
3. Ordini Vendita  
4. Ordine Assistenza  
5. Necessità componente di produzione  
6. Riga ordine di assemblaggio  
7. Ordine di trasferimento in uscita  
8. L'ordine programmato (non ancora utilizzato dagli ordini di vendita correlati)  
9. Previsione (non ancora utilizzata da altri ordini di vendita)  
  
> [!NOTE]  
>  I resi di acquisto non vengono in genere inclusi nella pianificazione dell'approvvigionamento; devono essere sempre impegnati dal lotto che sta per essere reso. Se non impegnati, i resi di acquisto svolgono un ruolo nella disponibilità e hanno un'elevata priorità per evitare che il sistema suggerisca un ordine di approvvigionamento solo per un ordine di reso.  
  
## <a name="priorities-on-the-supply-side"></a>Priorità sul lato dell'approvvigionamento  
1. Già in magazzino: Mov. contabili articoli (Flessibilità pianificazione = Nessuna)  
2. Ordine di reso vendita (flessibilità pianificazione = nessuna)  
3. Ordine di trasferimento in ingresso  
4. Ordine di produzione  
5. Ordine di assemblaggio  
6. Ordine acquisto  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Priorità correlata allo stato di domanda e approvvigionamento  
Oltre alle priorità specificate dal tipo di domanda e approvvigionamento, lo stato attuale degli ordini nel processo di esecuzione definisce anche una priorità. Ad esempio, le attività di magazzino hanno un l'impatto e lo stato degli ordini di vendita, di acquisto, di trasferimento, di assemblaggio e di produzione vengono presi in considerazione:  
  
1. Gestito parzialmente (flessibilità pianificazione = nessuna)  
2. Già nel processo nel warehouse (flessibilità pianificazione = Nessuna)  
3. Rilasciato - tutti i tipi di ordine (flessibilità pianificazione = illimitata)  
4. Ordine di produzione confermato (flessibilità pianificazione = illimitata)  
5. Pianificato/Aperto - tutti i tipi di ordine (flessibilità pianificazione = illimitata)  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
