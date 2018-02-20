---
title: Organizzare gli articoli in categorie| Documenti Microsoft
description: "Per semplificare la ricerca e trovare gli articoli, è possibile assegnare gli attributi degli articoli e organizzare gli articoli in categorie."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 64511e0979671d13740bd18d95d53e8e37564583
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="categorize-items"></a>Classificare gli articoli
Per visualizzare una panoramica degli articoli e semplificare l'ordinamento e la ricerca degli articoli, risulta utile organizzare gli articoli in categorie.

Per trovare gli articoli in base alle caratteristiche, è possibile assegnare gli attributi ad articoli e a categorie articolo. Per ulteriori informazioni, vedere [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Per creare una categoria articolo
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Categorie articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Categorie articoli** scegliere l'azione **Nuovo**.
3. Nella finestra **Scheda categoria articolo**, nella Scheda dettaglio **Generale**, compilare i campi in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nella Scheda dettaglio **Attributi**, specificare tutti gli attributi per la categoria articolo. Per ulteriori informazioni, vedere la sezione "Per assegnare attributi a una categoria articolo" in [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).

> [!NOTE]  
>   Se la categoria articolo è una categoria padre, come indicato dal campo **Categoria padre**, gli attributi articoli assegnati a tale categoria padre sono precompilati nella Scheda dettaglio **Attributi**.

> [!NOTE]  
>   Gli attributi degli articoli assegnati a una categoria articolo vengono applicati automaticamente all'articolo a cui la categoria articolo è assegnata.

## <a name="to-assign-an-item-category-to-an-item"></a>Per assegnare una categoria articolo a un articolo
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.
2. Aprire la scheda per l'articolo a cui si desidera assegnare una categoria articolo.
3. Nel campo **Codice categoria articolo** scegliere il pulsante di ricerca e selezionare una categoria articolo esistente. In alternativa, scegliere l'azione **Nuovo** per creare prima una nuova categoria articolo come descritto nella sezione "Per creare una categoria articolo".

## <a name="see-also"></a>Vedi anche
[Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

