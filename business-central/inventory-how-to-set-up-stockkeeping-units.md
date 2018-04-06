---
title: "Procedura: Impostare le unità di stockkeeping | Documenti Microsoft"
description: "Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4870e82d4390e0a96a137579d035fee0e54b19eb
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-stockkeeping-units"></a>Impostare le unità di stockkeeping
Le unità di stockkeeping possono essere utilizzate per registrare le informazioni relative agli articoli per una specifica ubicazione o uno specifico codice variante.  

 Le unità di stockkeeping rappresentano un'integrazione alle schede articolo. Non le sostituiscono, anche se sono correlate. Queste unità consentono di differenziare le informazioni relative ad un articolo per una specifica ubicazione, ad esempio una warehouse o un centro di distribuzione, o una specifica variante, ad esempio numeri scaffale e diverse informazioni relative al riapprovvigionamento, per lo stesso articolo.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Per impostare le unità di stockkeeping  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Unità di stockkeeping**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Compilare i campi della scheda. I campi seguenti sono obbligatori: **Nr. articolo**, **Cod. ubicazione**e/o **Cod. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una volta impostata la prima unità di stockkeeping per un articolo, la casella di controllo **Unità di stockkeeping esisten.** nella scheda **Articolo** risulta selezionata.  

Per creare diverse unità di stockkeeping per un articolo, utilizzare il processo batch **Crea unità di stockkeeping**.  

> [!NOTE]  
>  Le informazioni contenute nella scheda **Unità di stockkeeping** sono prioritarie rispetto a quelle della scheda **Articolo**.  

## <a name="see-also"></a>Vedi anche  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

