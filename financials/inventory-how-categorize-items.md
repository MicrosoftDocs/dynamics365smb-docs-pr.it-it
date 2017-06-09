---
title: 'Procedura: Categorizzare gli articoli | Documenti Microsoft'
description: Viene descritto come organizzare gli articoli in categorie.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 06f50a356ddc3a501c28fe34891213b55a12e3fd
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-categorize-items"></a>Procedura: Classificare gli articoli
Per visualizzare una panoramica degli articoli e semplificare l'ordinamento e la ricerca degli articoli, risulta utile organizzare gli articoli in categorie.

Per trovare gli articoli in base alle caratteristiche, è possibile assegnare gli attributi ad articoli e a categorie articolo. Per ulteriori informazioni, vedere [Procedura: Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Per creare una categoria articolo
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Categorie articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Categorie articoli** scegliere l'azione **Nuovo**.
3. Nella finestra **Scheda categoria articolo**, nella Scheda dettaglio **Generale**, compilare i campi in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nella Scheda dettaglio **Attributi**, specificare tutti gli attributi per la categoria articolo. Per ulteriori informazioni, vedere la sezione "Per assegnare attributi a una categoria articolo" in [Procedura: Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).

**Nota**: se la categoria articolo è una categoria padre, come indicato dal campo **Categoria padre**, gli attributi articoli assegnati a tale categoria padre sono precompilati nella Scheda dettaglio **Attributi**.

**Nota**: gli attributi degli articoli assegnati a una categoria articolo vengono applicati automaticamente all'articolo a cui la categoria articolo è assegnata.

## <a name="to-assign-an-item-category-to-an-item"></a>Per assegnare una categoria articolo a un articolo
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Articoli**, quindi scegliere il collegamento correlato.
2. Aprire la scheda per l'articolo a cui si desidera assegnare una categoria articolo.
3. Nel campo **Codice categoria articolo** scegliere il pulsante di ricerca e selezionare una categoria articolo esistente. In alternativa, scegliere l'azione **Nuovo** per creare prima una nuova categoria articolo come descritto nella sezione "Per creare una categoria articolo".

## <a name="see-also"></a>Vedi anche
[Procedura: Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)  
[Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

