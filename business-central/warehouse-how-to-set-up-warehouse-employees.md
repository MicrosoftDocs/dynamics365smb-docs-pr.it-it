---
title: 'Procedura: Impostare impiegati warehouse | Documenti Microsoft'
description: Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4a2ebf2d28833b9cb79c5711fd0314134dfc0915
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784169"
---
# <a name="set-up-warehouse-employees"></a>Impostare impiegati warehouse
Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default. Mediante questa impostazione dell'utente vengono filtrate tutte le attività di warehouse del database in base all'ubicazione dell'impiegato in modo che l'impiegato possa eseguire esclusivamente le attività di warehouse nella posizione di default. Un utente può essere assegnato a ubicazioni aggiuntive non di default per le quali l'impiegato può visualizzare le righe delle attività ma non eseguire le attività.

## <a name="to-set-up-warehouse-employees"></a>Per impostare impiegati warehouse  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impiegati warehouse** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Selezionare il campo **ID utente** quindi selezionare l'utente da aggiungere come impiegato warehouse. Scegliere il pulsante **OK**.  
6.  Nel campo **Cod. ubicazione**, immettere il codice dell'ubicazione in cui l'utente lavorerà.  
7.  Selezionare la casella di controllo **Default** per definire l'unica ubicazione in cui l'impiegato può eseguire attività di warehouse.  
8.  Ripetere i passaggi indicati per assegnare altri impiegati a ubicazioni o per assegnare ubicazioni non di default agli impiegati warehouse esistenti.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]