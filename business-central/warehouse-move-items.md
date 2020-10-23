---
title: Spostare articoli | Documenti Microsoft
description: Quando gli articoli si trovano in magazzino, potrebbe essere necessario spostarli per supportare le attività di warehouse quotidiane necessarie per mantenere il flusso degli articoli nella warehouse. Alcuni movimenti avvengono in relazione diretta con le operazioni interne, ad esempio un ordine di produzione che richiede la consegna di componenti o lo stoccaggio di articoli finali. Altri movimenti vengono eseguiti come pura ottimizzazione dello spazio della warehouse oppure come movimenti ad-hoc da e verso tali operazioni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d0decb06f9ea7c8dd85aba8cb9aea2ac02cac824
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920274"
---
# <a name="moving-items"></a>Spostamento di articoli
L'attività di warehouse di spostamento degli articoli all'interno della warehouse viene eseguita in modi diversi a seconda della configurazione delle funzionalità di gestione warehouse. La complessità può andare dall'assenza delle funzionalità di warehouse, alle configurazioni di warehouse di base per la gestione ordine per ordine in una o più attività, fino alle configurazioni avanzate in cui tutte le attività di warehouse devono essere eseguite in un flusso di lavoro guidato. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

Quando in un'ubicazione warehouse potrebbe essere necessario spostare gli articoli per supportare le attività di warehouse quotidiane necessarie per mantenere il flusso degli articoli nella warehouse. Alcuni movimenti avvengono in relazione diretta con le operazioni interne, ad esempio un ordine di produzione che richiede la consegna di componenti o lo stoccaggio di articoli finali. Altri movimenti vengono eseguiti come pura ottimizzazione dello spazio della warehouse oppure come movimenti ad-hoc da e verso tali operazioni.

Le attività di spostamento aggiuntive consistono nel rifornimento periodico delle collocazioni di prelievo o di produzione e nella modifica delle informazioni sul contenuto delle collocazioni.

Lo spostamento degli articoli in altre ubicazioni influisce sui movimenti contabili articoli e deve pertanto essere effettuato tramite un ordine di trasferimento. Per ulteriori informazioni, vedere [Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md).  

Le attività di conteggio, rettifica e riclassificazione degli articoli correlate al magazzino possono comportare attività di warehouse che devono essere eseguite in movimenti warehouse prima di poter essere sincronizzate con i relativi movimenti contabili articoli. Per ulteriori informazioni, vedere [Conteggio, rettifica e riclassificazione dell'inventario](inventory-how-count-adjust-reclassify.md)  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Spostare gli articoli tra le collocazioni nelle configurazioni di warehouse di base in qualsiasi momento e senza documenti di origine.|[Spostare articoli nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Utilizzare il prospetto movimentazione warehouse per spostare gli articoli in configurazioni di warehouse avanzate, sia per i documenti di origine che per i documenti ad hoc.|[Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Inserire articoli componenti nelle operazioni interne delle configurazioni di warehouse di base, secondo quanto richiesto dai documenti di origine per tali operazioni.|[Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Pianificare le collocazioni da riempire o svuotare per mantenere un flusso efficace, ad esempio svuotando un'area di immagazzinamento a massa prima di un carico di grandi dimensioni.|[Pianificare movimentazioni warehouse nei prospetti](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Aggiornare la frequenza con cui le collocazioni, ad esempio le collocazioni di prelievo, devono essere rifornite in seguito alle fluttuazioni della domanda.|[Calcola rifornimento collocazione](warehouse-how-to-calculate-bin-replenishment.md)|
|Ristrutturare la warehouse con nuovi codici collocazione e nuove caratteristiche per le collocazioni e spostarli.|[Ristrutturare warehouse](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
