---
title: 'Dettagli di progettazione: Tracciabilità articolo nel magazzino | Microsoft Docs'
description: La gestione dei numeri seriali e di lotto è principalmente un'attività di warehouse, pertanto tutti i documenti di warehouse in uscita e in entrata hanno funzionalità standard per l'assegnazione e la selezione dei numeri di tracciabilità articolo. Tuttavia, poiché il sistema di impegni è basato sui movimenti contabili articoli, i documenti di attività di warehouse che registrano solo i movimenti warehouse non sono pienamente supportati.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a482e0fed80d5e9380b6c6e0ec03557abbc02953
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242102"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Dettagli di progettazione: Tracciabilità articolo nel magazzino
La gestione dei numeri seriali e di lotto è principalmente un'attività di warehouse, pertanto tutti i documenti di warehouse in uscita e in entrata hanno funzionalità standard per l'assegnazione e la selezione dei numeri di tracciabilità articolo.  

Tuttavia, poiché il sistema di impegni è basato sui movimenti contabili articoli, i documenti di attività di warehouse che registrano solo i movimenti warehouse non sono pienamente supportati. Poiché gli impegni e i numeri di tracciabilità articolo possono essere gestiti solo a livello dell'ubicazione, non a livello di zona e di collocazione, la pagina **Righe tracciabilità articolo** non può essere aperta dai documenti di attività di warehouse. Lo stesso vale per la pagina **Impegno**.  

Dopo aver aggiunto un numero seriale o di lotto a un articolo nell'ubicazione warehouse, questo può essere spostato e riclassificato liberamente nel warehouse tramite una struttura indipendente di tracciabilità articolo che sia indipendente dal sistema di impegno. È possibile accedere ai campi **Nr. seriale** e **Nr. lotto** direttamente nelle righe del documento di warehouse. Quando il numero seriale o di lotto viene successivamente incluso nella registrazione in uscita, viene sincronizzato con il sistema di impegno come parte della rettifica ordinaria della collocazione. Per ulteriori informazioni, vedere [Dettagli di progettazione: Integrazione con il magazzino](design-details-integration-with-inventory.md).  

Tuttavia, il sistema di impegno prende in considerazione le attività di warehouse quando calcola la disponibilità. Ad esempio, gli articoli che vengono allocati ai prelievi, o registrati come prelevati, non possono essere impegnati. Per ulteriori informazioni, vedere [Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)  
[Dettagli di progettazione: Integrazione con il magazzino](design-details-integration-with-inventory.md)  
[Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md)  
[Dettagli di progettazione: Progettazione tracciabilità articolo](design-details-item-tracking-design.md)