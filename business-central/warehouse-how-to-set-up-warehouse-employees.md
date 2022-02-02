---
title: Impostare impiegati warehouse
description: Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7328, 7348
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4d0c89b00c95c8da94e2b32c95b8a930b154b4e5
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971552"
---
# <a name="set-up-warehouse-employees"></a>Impostare impiegati warehouse

Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default. Mediante questa impostazione dell'utente vengono filtrate tutte le attività di warehouse del database in base all'ubicazione dell'impiegato in modo che l'impiegato possa eseguire esclusivamente le attività di warehouse nella posizione di default. Un utente può essere assegnato a ubicazioni aggiuntive non di default per le quali l'impiegato può visualizzare le righe delle attività ma non eseguire le attività.

## <a name="to-set-up-warehouse-employees"></a>Per impostare impiegati warehouse  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Selezionare il campo **ID utente** quindi selezionare l'utente da aggiungere come impiegato warehouse. Scegliere il pulsante **OK**.  
4. Nel campo **Cod. ubicazione**, immettere il codice dell'ubicazione in cui l'utente lavorerà.  
5. Selezionare la casella di controllo **Default** per definire l'unica ubicazione in cui l'impiegato può eseguire attività di warehouse.  
6. Ripetere i passaggi indicati per assegnare altri impiegati a ubicazioni o per assegnare ubicazioni non di default agli impiegati warehouse esistenti.  

## <a name="see-also"></a>Vedi anche

[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione di Gestione warehouse](warehouse-setup-warehouse.md) 
[Gestione assemblaggio](assembly-assemble-items.md)
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]