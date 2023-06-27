---
title: Impostare impiegati warehouse
description: Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default e potenzialmente a più ubicazioni non di default.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# <a name="set-up-warehouse-employees" />Impostare impiegati warehouse

Ogni utente che può eseguire attività di warehouse deve essere impostato come impiegato warehouse assegnato a una ubicazione di default. [!INCLUDE [prod_short](includes/prod_short.md)] filtra le attività di magazzino in base all'ubicazione predefinita del dipendente. Può eseguire solo le attività di magazzino nell'ubicazione. Puoi anche assegnare un utente ad altre ubicazioni. Può accedere ma non eseguire attività in tali ubicazioni.

## <a name="to-set-up-warehouse-employees" />Per impostare impiegati warehouse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Selezionare il campo **ID utente** quindi selezionare l'utente da aggiungere come impiegato warehouse. Scegliere il pulsante **OK**.  
4. Nel campo **Cod. ubicazione**, immettere il codice dell'ubicazione in cui l'utente lavorerà.  
5. Attiva l'interruttore **Predefinito** per definire l'unica ubicazione in cui il dipendente può eseguire attività di warehouse.  
6. Ripeti i passaggi indicati per assegnare altri dipendenti a ubicazioni o per assegnare altre ubicazioni ai dipendenti warehouse esistenti.  

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/get-started-warehouse-management/)

## <a name="see-also" />Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definire un criterio di registrazione delle fatture per gli utenti](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
