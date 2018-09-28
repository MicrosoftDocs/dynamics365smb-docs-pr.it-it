---
title: 'Dettagli di progettazione: Gestione dei metodi di riordino | Microsoft Docs'
description: Panoramica dei task per la definizione di un metodo di riordino nella pianificazione dell'approvvigionamento.
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
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b273dedd269d8b86ba4fa7a9d9540c44b701a97e
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-reordering-policies"></a>Dettagli di progettazione: Gestione dei metodi di riordino
Affinché un articolo partecipi alla pianificazione dell'approvvigionamento, i metodi di riordino devono essere definiti. Sono disponibili i seguenti quattro metodi di riordino:  
  
* Qtà Riordino Fissa  
* Qtà Massima  
* Ordine  
* Lotto-per-Lotto  
  
I motivi Qtà Riordino Fissa e Qtà massima sono relativi alla pianificazione del magazzino. Sebbene la pianificazione del magazzino sia tecnicamente più semplice della procedura di contropartita, questi criteri devono coesistere con la contropartita dettagliata della tracciabilità di approvvigionamento e ordine. Per controllare l'integrazione tra i due e fornire visibilità nella logica di pianificazione, rigidi principi controllano la gestione dei metodi di riordino.  
  
## <a name="in-this-section"></a>In questa sezione  
[Dettagli di progettazione: Il ruolo del punto di riordino](design-details-the-role-of-the-reorder-point.md)  
[Dettagli di progettazione: Monitoraggio del livello di giacenza disponibile e del punto di riordino](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Dettagli di progettazione: Il ruolo dell'intervallo di tempo](design-details-the-role-of-the-time-bucket.md)  
[Dettagli di progettazione: Al di sotto del livello di overflow](design-details-staying-under-the-overflow-level.md)  
[Dettagli di progettazione: Gestione giacenze negative previste](design-details-handling-projected-negative-inventory.md)  
[Dettagli di progettazione: Metodi di riordino](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
