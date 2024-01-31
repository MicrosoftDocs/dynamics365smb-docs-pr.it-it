---
title: Come impostare le unità di stockkeeping
description: Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o una specifica variante.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/19/2023
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
ms.service: dynamics-365-business-central
---

# Configurare le unità di stockkeeping

Usa le unità di stockkeeping (SKUs) per registrare le informazioni relative agli articoli per una ubicazione o una variante specifiche. Consentono di aggiungere informazioni diverse su un articolo per una posizione specifica, ad esempio:

* Un magazzino o un centro di distribuzione
* Varianti, ad esempio numeri di scaffale diversi e informazioni di rifornimento diverse, per lo stesso articolo  

## Per impostare le unità di stockkeeping  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Unità di stockkeeping**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  
3. Compila i campi in base alle esigenze. I campi seguenti sono obbligatori: **Nr. articolo**, **Cod. ubicazione**e/o **Cod. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una volta impostata la prima unità di stockkeeping per un articolo, la casella di controllo **Unità di stockkeeping esisten.** nella scheda **Articolo** risulta selezionata.  

Per creare diverse unità di stockkeeping per un articolo, utilizzare il processo batch **Crea unità di stockkeeping**. Per ulteriori informazioni sui processi batch, vai a [Usare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> Le informazioni contenute nella scheda **Unità di stockkeeping** sono prioritarie rispetto a quelle della scheda **Articolo**.

> [!Warning]
> Se la USK viene fornita tramite produzione, il campo **Costo standard** non è utilizzato quando si fattura e si rettifica il costo effettivo dell'articolo prodotto. In alternativa, [!INCLUDE [prod_short](includes/prod_short.md)] usa il valore nel campo **Costo standard** nella scheda articolo sottostante e tutti gli scostamenti vengono calcolati rispetto al dettaglio costi di tale articolo.<br><br>
> Sebbene l'utente può assegnare le DB di produzione e i cicli assegnati alle SKU, anche il rollup del costo unitario e il calcolo correlato del dettaglio costi non sono disponibili nelle SKU. Per ulteriori informazioni sui costi standard, vai a [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md)

## Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Gestione assemblaggio](assembly-assemble-items.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
