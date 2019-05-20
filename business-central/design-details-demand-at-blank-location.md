---
title: 'Dettagli di progettazione: Domanda e approvvigionamento | Microsoft Docs'
description: Questo argomento introduce il concetto di domanda, ovvero il termine comune utilizzato per tutti i tipi di domanda lorda, ad esempio un ordine di vendita e un componente necessario da un ordine di produzione.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 23e941b3ab6fc8e2176268f38647630419453d23
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242397"
---
# <a name="design-details-demand-and-supply"></a>Dettagli di progettazione: Domanda e approvvigionamento
La domanda è il termine comune utilizzato per tutti i tipi di domanda lorda, ad esempio un ordine di vendita e un componente necessario da un ordine di produzione. Inoltre, il programma consente i tipi di domanda più tecnici, ad esempio resi di acquisto e delle giacenze negative.  
  
Approvvigionamento è il termine comune utilizzato per indicare qualsiasi genere di quantità in entrata o positiva, quale il magazzino, gli acquisti, l'assemblaggio, la produzione o i trasferimenti in entrata. Inoltre, anche un reso di vendita può rappresentare un approvvigionamento.  
  
Per ordinare le numerose origini di approvvigionamento e di domanda, il sistema di pianificazione le organizza su due righe chiamate profili di magazzino. Un profilo conserva gli eventi di domanda e l'altro conserva i corrispondenti eventi di approvvigionamento. Ogni evento rappresenta un'entità di rete di ordini, ad esempio una riga ordine di vendita, un movimento contabile di magazzino o una riga di ordine di produzione.  
  
Quando vengono caricati i profili di magazzino, i differenti set di domanda-approvvigionamento vengono bilanciati in modo da fornire un piano di approvvigionamento che soddisfi gli obiettivi elencati.  
  
I parametri di pianificazione e i livelli di magazzino sono altri tipi rispettivamente di domanda e di approvvigionamento, che subiscono la contropartita integrata per rifornire gli articoli in stock. Per ulteriori informazioni, vedere [Dettagli di programmazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md).  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)