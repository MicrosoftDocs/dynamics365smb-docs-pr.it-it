---
title: "Attività della warehouse | Documenti Microsoft"
description: "Dopo che le merci sono state ricevute e prima di venire spedite, viene eseguita una serie di attività di warehouse interne per garantire un flusso efficace nella warehouse e per organizzare e gestire l'inventario della società."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 604f7e55067efaebed412683ed51ce8717562688
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="warehouse-management"></a>Gestione warehouse
Dopo che le merci sono state ricevute e prima di venire spedite, viene eseguita una serie di attività di warehouse interne per garantire un flusso efficace nella warehouse e per organizzare e gestire l'inventario della società.

In genere, le attività di warehouse includono lo stoccaggio degli articoli, il loro spostamento all'interno della warehouse o tra warehouse e il loro prelievo per l'assemblaggio, la produzione o la spedizione. Gli articoli di assemblaggio da vendere o il magazzino possono inoltre essere considerati attività di warehouse ma vengono trattati altrove. Per ulteriori informazioni, vedere [Gestione assemblaggio](assembly-assemble-items.md).  

Nelle warehouse di grandi dimensioni, queste diverse attività di gestione possono essere separate in base ai reparti e l'integrazione può essere gestita da un flusso di lavoro guidato. Nelle installazioni più semplici, il flusso è meno formale e le attività di warehouse vengono eseguite tramite stoccaggi e prelievi di magazzino. Per ulteriori informazioni sulle configurazioni di warehouse di base rispetto alle configurazioni avanzate, vedere [Dettagli di progettazione: Panoramica warehouse](design-details-warehouse-overview.md).

Prima di eseguire attività di warehouse, è necessario impostare il sistema per la complessità della relativa elaborazione di warehouse. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Registrare il carico degli articoli nelle ubicazioni di warehouse, solo con un ordine di acquisto, nelle impostazioni semplici dell'ubicazione, o con un carico warehouse, in caso di processi warehouse parzialmente o completamente automatici nell'ubicazione.|[Ricevere articoli](warehouse-how-receive-items.md)|
|Ignorare i processi di stoccaggio e prelievo per velocizzare le operazioni dal carico o dalla produzione alla spedizione di un articolo.|[Sottoporre gli articoli a cross-dock](warehouse-how-to-cross-dock-items.md)|    
|Stoccare articoli ricevuti da acquisti, resi di vendita, trasferimenti o output di produzione, in base al processo warehouse configurato.|[Stoccaggio di articoli](warehouse-put-away-items.md)|
|Spostare gli articoli tra collocazioni nella warehouse.|[Spostamento di articoli](warehouse-move-items.md)|
|Prelevare articoli da spedire, trasferire o utilizzare in assemblaggio o produzione, in base al processo warehouse configurato.|[Prelievo di articoli](warehouse-pick-items.md)|
|Registrare la spedizione degli articoli dalle ubicazioni di warehouse, solo con un ordine di vendita, nelle impostazioni semplici dell'ubicazione, o con una spedizione warehouse, in caso di processi warehouse parzialmente o completamente automatici nell'ubicazione.|[Spedire articoli](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Vedi anche  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

