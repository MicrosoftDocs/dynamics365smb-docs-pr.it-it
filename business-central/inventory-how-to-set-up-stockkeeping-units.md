---
title: 'Procedura: Impostare le unità di stockkeeping | Documenti Microsoft'
description: Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 610939cb61c917d5319fc758e582c0d169d7f11b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182014"
---
# <a name="set-up-stockkeeping-units"></a>Impostare le unità di stockkeeping
Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.  

 Le unità di stockkeeping rappresentano un'integrazione alle schede articolo. Non le sostituiscono, anche se sono correlate. Queste unità consentono di differenziare le informazioni relative ad un articolo per una specifica ubicazione, ad esempio una warehouse o un centro di distribuzione, o una specifica variante, ad esempio numeri scaffale e diverse informazioni relative al riapprovvigionamento, per lo stesso articolo.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Per impostare le unità di stockkeeping  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Unità di stockkeeping** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Compilare i campi della scheda. I campi seguenti sono obbligatori: **Nr. articolo**, **Cod. ubicazione** e/o **Cod. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una volta impostata la prima unità di stockkeeping per un articolo, la casella di controllo **Unità di stockkeeping esisten.** nella scheda **Articolo** risulta selezionata.  

Per creare diverse unità di stockkeeping per un articolo, utilizzare il processo batch **Crea unità di stockkeeping**.  

> [!NOTE]  
>  Le informazioni contenute nella scheda **Unità di stockkeeping** sono prioritarie rispetto a quelle della scheda **Articolo**.

> [!Warning]
> Se la USK viene fornita tramite produzione, il campo **Costo standard** non è utilizzato quando si fattura e si rettifica il costo effettivo dell'articolo prodotto. In alternativa, viene utilizzato il campo **Costo standard** nella scheda articolo sottostante e tutti gli scostamenti vengono calcolati rispetto al dettaglio costi di tale articolo.<br /><br />
> Poiché le distinte base e il ciclo di produzione non possono essere assegnati a USK, anche il rollup del costo unitario e il calcolo correlato del dettaglio costi non sono disponibili nelle USK. Per ulteriori informazioni, vedere [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md).

## <a name="see-also"></a>Vedi anche  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
