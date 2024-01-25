---
title: Spostamento degli articoli
description: Scopri come spostare gli articoli tra le collocazioni nella warehouse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: Conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7315, 7349, 7351, 7382, 7384, 7386, 7387, 7399, 7400, 9314, 9330, 9345'
---
# <a name="moving-items"></a>Spostamento di articoli

Puoi spostare gli articoli nella warehouse in diversi modi, a seconda di come hai configurato la warehouse. La complessità può variare:

* Le warehouse di piccole dimensioni potrebbero utilizzare configurazioni warehouse di base per gestire gli ordini singolarmente, in uno o più passaggi.
* Le warehouse di grandi dimensioni potrebbero utilizzare configurazioni avanzate in cui tutte le attività di warehouse sono coordinate da un flusso di lavoro diretto. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).

Potrebbe essere necessario spostare gli articoli tra collocazioni, ad esempio, a causa di operazioni interne:

* Un ordine di produzione richiede la consegna dei componenti o lo stoccaggio degli articoli finiti.
* Un responsabile della warehouse vuole ottimizzare lo spazio.
* Movimenti non pianificati da e verso le operazioni.
* Rifornimento delle collocazioni di prelievo o di produzione.
* Aggiornamento del contenuto delle collocazioni.

Le attività di conteggio, rettifica e riclassificazione degli articoli possono comportare attività di warehouse che devono essere eseguite in movimenti warehouse prima di poter essere sincronizzate con i relativi movimenti contabili articoli. Per ulteriori informazioni vedi [Conteggio, rettifica e riclassificazione dell'inventario](inventory-how-count-adjust-reclassify.md).  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|  
|Spostamento articoli tra ubicazioni|[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)|
|Spostare gli articoli tra le collocazioni nelle configurazioni di warehouse di base in qualsiasi momento e senza documenti di origine.|[Spostare articoli nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Utilizza il prospetto movimentazione warehouse, prelievo e stoccaggio interni, per spostare gli articoli in configurazioni di warehouse avanzate con prelievo e stoccaggio diretti.|[Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Ristrutturare la warehouse con nuovi codici collocazione e nuove caratteristiche per le collocazioni e spostarli.|[Ristrutturare warehouse](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Vedere anche

[Panoramica della gestione warehouse](design-details-warehouse-management.md)  
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
