---
title: Come assegnare collocazioni di default ad articoli | Microsoft Docs
description: Quando si utilizzano le collocazioni di un'ubicazione, l'assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento. Quando si assegna una collocazione di default a un articolo, tale collocazione viene suggerita ogni volta che viene avviata una transazione per l'articolo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6777f71e35792b4bb4dfb44d1267b59b90109438
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771881"
---
# <a name="assign-default-bins-to-items"></a>Assegnare collocazioni di default ad articoli
Quando si utilizzano le collocazioni di un'ubicazione, l'assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento. Quando si assegna una collocazione di default a un articolo, tale collocazione viene suggerita ogni volta che viene avviata una transazione per l'articolo. Le collocazioni di default vengono definite nella pagina **Contenuto Collocazione**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Per assegnare una collocazione di default a un articolo
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto creazione contenuto collocazione** e scegliere il collegamento correlato.  
2.  Immettere le informazioni relative all'articolo e al codice collocazione per ogni collocazione da impostare come default per un articolo. Assicurarsi selezionare il campo **Default**.  
3.  Scegliere l'azione **Crea contenuto collocazione**. Le collocazioni di default vengono assegnate all'articolo.  

> [!NOTE]  
>  Quando si esegue lo stoccaggio di un articolo, se a quest'ultimo non è assegnata una collocazione di default, verrà assegnata quella di default come collocazione per lo stoccaggio dell'articolo.  

## <a name="to-change-the-default-bin-for-an-item"></a>Per modificare la collocazione di default per un articolo  
Potrebbe essere necessario modificare l'assegnazione della collocazione di default per un articolo o assegnare una collocazione di default a un nuovo articolo.    
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contenuto collocazioni** e quindi scegliere il collegamento correlato.  
2.  Selezionare il codice di ubicazione desiderato nel campo **Filtro ubicazione**.  
3.  Individuare il movimento del contenuto collocazione di default corrente per l'articolo e deselezionare la casella di controllo **Collocazione di default**.  
4.  Individuare la riga del contenuto della collocazione che si desidera utilizzare come nuova collocazione di default. Selezionare la casella di controllo **Collocazione di default**.  

> [!NOTE]  
>  Quando si esegue lo stoccaggio di un articolo per la prima volta, se a quest'ultimo non è assegnata una collocazione di default, il sistema assegnerà la collocazione di stoccaggio dell'articolo come collocazione di default.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]