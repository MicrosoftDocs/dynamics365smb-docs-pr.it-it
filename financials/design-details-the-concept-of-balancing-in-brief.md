---
title: 'Dettagli di progettazione: Il concetto di contropartita in breve | Microsoft Docs'
description: "La domanda è fornita dai clienti di una società. L'approvvigionamento è ciò che la società può creare e rimuovere per stabilire il saldo. Il sistema di pianificazione inizia con la domanda indipendente e successivamente risale a ritroso fino all'approvvigionamento."
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
ms.openlocfilehash: a87fb83e2fad2c99de9938f87ef6f83db9c64dc4
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-the-concept-of-balancing-in-brief"></a>Dettagli di progettazione: Il concetto di contropartita in breve
La domanda è fornita dai clienti di una società. L'approvvigionamento è ciò che la società può creare e rimuovere per stabilire il saldo. Il sistema di pianificazione inizia con la domanda indipendente e successivamente risale a ritroso fino all'approvvigionamento.  
  
 I profili di magazzino vengono utilizzati per contenere le informazioni sulle domande, gli approvvigionamenti, le quantità e l'intervallo. I profili essenzialmente compongono i due lati della bilancia.  
  
 L'obiettivo del meccanismo di pianificazione consiste nel controbilanciare la domanda e l'approvvigionamento di un articolo per garantire che l'approvvigionamento corrisponda alla domanda in modo fattibile così come definito dalle regole e dai parametri di pianificazione.  
  
 ![](media/nav_app_supply_planning_2_balancing.png "NAV_APP_supply_planning_2_balancing")  
  
## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
 [Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
