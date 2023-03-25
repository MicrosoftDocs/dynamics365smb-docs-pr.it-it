---
title: Come impostare le unità di stockkeeping
description: Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '5704, 5700, 5702, 5701'
ms.date: 04/01/2021
ms.author: edupont
---
# Impostare le unità di stockkeeping

Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una ubicazione o un codice variante specifici.  

Le unità di stockkeeping rappresentano un'integrazione alle schede articolo. Non le sostituiscono, anche se sono correlate. Queste unità consentono di differenziare le informazioni relative ad un articolo per una specifica ubicazione, ad esempio una warehouse o un centro di distribuzione, o una specifica variante, ad esempio numeri scaffale e diverse informazioni relative al riapprovvigionamento, per lo stesso articolo.  

## Per impostare le unità di stockkeeping  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Unità di stockkeeping**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Compilare i campi della scheda. I campi seguenti sono obbligatori: **Nr. articolo**, **Cod. ubicazione**e/o **Cod. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una volta impostata la prima unità di stockkeeping per un articolo, la casella di controllo **Unità di stockkeeping esisten.** nella scheda **Articolo** risulta selezionata.  

Per creare diverse unità di stockkeeping per un articolo, utilizzare il processo batch **Crea unità di stockkeeping**.  

> [!NOTE]  
>  Le informazioni contenute nella scheda **Unità di stockkeeping** sono prioritarie rispetto a quelle della scheda **Articolo**.

> [!Warning]
> Se la USK viene fornita tramite produzione, il campo **Costo standard** non è utilizzato quando si fattura e si rettifica il costo effettivo dell'articolo prodotto. In alternativa, viene utilizzato il campo **Costo standard** nella scheda articolo sottostante e tutti gli scostamenti vengono calcolati rispetto al dettaglio costi di tale articolo.<br /><br />
> Poiché le distinte base e il ciclo di produzione non possono essere assegnati a USK, anche il rollup del costo unitario e il calcolo correlato del dettaglio costi non sono disponibili nelle USK. Per ulteriori informazioni, vedere [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md).

## Vedi il relativo [training Microsoft](/training/modules/control-inventory-multiple-locations/)

## Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Gestione assemblaggio](assembly-assemble-items.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
