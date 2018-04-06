---
title: Come assegnare collocazioni di default ad articoli | Microsoft Docs
description: "Quando si utilizzano le collocazioni di un'ubicazione, l'assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento. Quando si assegna una collocazione di default a un articolo, tale collocazione viene suggerita ogni volta che viene avviata una transazione per l'articolo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 826e1392143b166566619c5aef8c28ac2b09bc22
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="assign-default-bins-to-items"></a>Assegnare collocazioni di default ad articoli
Quando si utilizzano le collocazioni di un'ubicazione, l'assegnazione di collocazioni di default agli articoli può semplificarne il processo di spedizione, ricezione e spostamento. Quando si assegna una collocazione di default a un articolo, tale collocazione viene suggerita ogni volta che viene avviata una transazione per l'articolo. Le collocazioni di default vengono definite nella finestra **Contenuto Collocazione**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Per assegnare una collocazione di default a un articolo
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Prospetto creaz. cont. colloc.**, quindi scegliere il collegamento correlato.  
2.  Immettere le informazioni relative all'articolo e al codice collocazione per ogni collocazione da impostare come default per un articolo. Assicurarsi selezionare il campo **Default**.  
3.  Scegliere l'azione **Crea contenuto collocazione**. Le collocazioni di default vengono assegnate all'articolo.  

> [!NOTE]  
>  Quando si esegue lo stoccaggio di un articolo, se a quest'ultimo non è assegnata una collocazione di default, verrà assegnata quella di default come collocazione per lo stoccaggio dell'articolo.  

## <a name="to-change-the-default-bin-for-an-item"></a>Per modificare la collocazione di default per un articolo  
Potrebbe essere necessario modificare l'assegnazione della collocazione di default per un articolo o assegnare una collocazione di default a un nuovo articolo.    
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Contenuto collocazioni**, quindi scegliere il collegamento correlato.  
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
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

