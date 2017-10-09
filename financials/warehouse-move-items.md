---
title: Spostare articoli | Documenti Microsoft
description: "Quando gli articoli si trovano in magazzino, potrebbe essere necessario spostarli per supportare le attività di warehouse quotidiane necessarie per mantenere il flusso degli articoli nella warehouse. Alcuni movimenti avvengono in relazione diretta con le operazioni interne, ad esempio un ordine di produzione che richiede la consegna di componenti o lo stoccaggio di articoli finali. Altri movimenti vengono eseguiti come pura ottimizzazione dello spazio della warehouse oppure come movimenti ad-hoc da e verso tali operazioni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f52353ec74b10983b0acfd04169d6b146c70eb84
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="moving-items"></a>Spostamento di articoli
L'attività di warehouse di spostamento degli articoli all'interno della warehouse viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse. La complessità può andare dall'assenza delle funzionalità di warehouse, alle configurazioni di warehouse di base per la gestione ordine per ordine in una o più attività, fino alle configurazioni avanzate in cui tutte le attività di warehouse devono essere eseguite in un flusso di lavoro guidato. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

Quando in un'ubicazione warehouse potrebbe essere necessario spostare gli articoli per supportare le attività di warehouse quotidiane necessarie per mantenere il flusso degli articoli nella warehouse. Alcuni movimenti avvengono in relazione diretta con le operazioni interne, ad esempio un ordine di produzione che richiede la consegna di componenti o lo stoccaggio di articoli finali. Altri movimenti vengono eseguiti come pura ottimizzazione dello spazio della warehouse oppure come movimenti ad-hoc da e verso tali operazioni.

Lo spostamento degli articoli in altre ubicazioni influisce sui movimenti contabili articoli e deve pertanto essere effettuato tramite un ordine di trasferimento. Per ulteriori informazioni, vedere [Procedura: Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md).  

Le attività di spostamento aggiuntive consistono nel rifornimento periodico delle collocazioni di prelievo o di produzione e nella modifica delle informazioni sul contenuto delle collocazioni.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Spostare gli articoli tra le collocazioni nelle configurazioni di warehouse di base in qualsiasi momento e senza documenti di origine.|[Procedura: Spostare articoli in configurazioni di warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Utilizzare il prospetto movimentazione warehouse per spostare gli articoli in configurazioni di warehouse avanzate, sia per i documenti di origine che per i documenti ad hoc.|[Procedura: Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Inserire articoli componenti nelle operazioni interne delle configurazioni di warehouse di base, secondo quanto richiesto dai documenti di origine per tali operazioni.|[Procedura: Spostare componenti in un'area di operazione nelle configurazioni della warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Pianificare le collocazioni da riempire o svuotare per mantenere un flusso efficace, ad esempio svuotando un'area di immagazzinamento a massa prima di un carico di grandi dimensioni.|[Procedura: Pianificare movimentazioni warehouse nei prospetti](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Aggiornare la frequenza con cui le collocazioni, ad esempio le collocazioni di prelievo, devono essere rifornite in seguito alle fluttuazioni della domanda.|[Procedura: Calcolare il rifornimento della collocazione](warehouse-how-to-calculate-bin-replenishment.md)|
|Ristrutturare la warehouse con nuovi codici collocazione e nuove caratteristiche per le collocazioni e spostarli.|[Procedura: Ristrutturare warehouse](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

