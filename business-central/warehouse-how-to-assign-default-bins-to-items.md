---
title: Assegnare collocazioni di default ad articoli
description: 'Quando si utilizzano le collocazioni di un''ubicazione, l''assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '7371, 7374, 7379'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Assegnare collocazioni di default ad articoli
Quando si utilizzano le collocazioni di un'ubicazione, l'assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento. Quando si assegna una collocazione di default a un articolo, tale collocazione viene suggerita ogni volta che viene avviata una transazione per l'articolo. Le collocazioni di default vengono definite nella pagina **Contenuto Collocazione**.  

## Per assegnare una collocazione di default a un articolo
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto creaz. cont. colloc.**, e quindi seleziona il collegamento correlato.  
2.  Immettere le informazioni relative all'articolo e al codice collocazione per ogni collocazione da impostare come default per un articolo. Assicurarsi selezionare il campo **Default**.  
3.  Scegliere l'azione **Crea contenuto collocazione**. Le collocazioni di default vengono assegnate all'articolo.  

> [!NOTE]  
>  Quando si esegue lo stoccaggio di un articolo, se a quest'ultimo non è assegnata una collocazione di default, verrà assegnata quella di default come collocazione per lo stoccaggio dell'articolo.  

## Per modificare la collocazione di default per un articolo  
Potrebbe essere necessario modificare l'assegnazione della collocazione di default per un articolo o assegnare una collocazione di default a un nuovo articolo.
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Contenuto collocazioni**, quindi scegli il collegamento correlato.  
2.  Selezionare il codice di ubicazione desiderato nel campo **Filtro ubicazione**.  
3.  Individuare il movimento del contenuto collocazione di default corrente per l'articolo e deselezionare la casella di controllo **Collocazione di default**.  
4.  Individuare la riga del contenuto della collocazione che si desidera utilizzare come nuova collocazione di default. Selezionare la casella di controllo **Collocazione di default**.  

> [!NOTE]  
>  Quando si esegue lo stoccaggio di un articolo per la prima volta, se a quest'ultimo non è assegnata una collocazione di default, il sistema assegnerà la collocazione di stoccaggio dell'articolo come collocazione di default.  

## Vedere anche  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md) 
[Gestione assemblaggio](assembly-assemble-items.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]