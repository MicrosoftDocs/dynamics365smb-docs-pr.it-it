---
title: 'Procedura: Impostare impiegati warehouse | Documenti Microsoft'
description: Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 624603a2610ca07388c0b84d13b0707e06e92a18
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881538"
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
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
