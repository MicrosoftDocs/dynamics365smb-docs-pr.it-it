---
title: Organizzare gli articoli in categorie| Documenti Microsoft
description: Per semplificare la ricerca e trovare gli articoli, è possibile assegnare gli attributi degli articoli e organizzare gli articoli in categorie.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3959392048f4c130e6564160f9b2c6f5956ece8c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746243"
---
# <a name="categorize-items"></a>Classificare gli articoli

Per visualizzare una panoramica degli articoli e semplificare l'ordinamento e la ricerca degli articoli, risulta utile organizzare gli articoli in categorie.

Per trovare gli articoli in base alle caratteristiche, è possibile assegnare gli attributi ad articoli e a categorie articolo. Per ulteriori informazioni, vedere [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Per creare una categoria articolo
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Categorie articoli** e quindi scegliere il collegamento correlato.
2. Nella pagina **Categorie articoli** scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda categoria articolo**, nella Scheda dettaglio **Generale**, compilare i campi in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nella Scheda dettaglio **Attributi**, specificare tutti gli attributi per la categoria articolo. Per ulteriori informazioni, vedere [Per assegnare attributi articolo alle categorie articoli](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Se la categoria articolo è una categoria padre, come indicato dal campo **Categoria padre**, gli attributi articoli assegnati a tale categoria padre sono precompilati nella Scheda dettaglio **Attributi**.

> [!NOTE]  
> Gli attributi degli articoli assegnati a una categoria articolo vengono applicati automaticamente all'articolo a cui la categoria articolo è assegnata.

Se si cambia idea su una categoria di articoli, è possibile eliminarla. Tuttavia, se è già stato assegnato a un articolo, è necessario rimuovere l'assegnazione prima di poter eliminare la categoria dell'articolo.

## <a name="to-assign-an-item-category-to-an-item"></a>Per assegnare una categoria articolo a un articolo

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Aprire la scheda per l'articolo a cui si desidera assegnare una categoria articolo.
3. Nel campo **Codice categoria articolo** scegliere il pulsante di ricerca e selezionare una categoria articolo esistente. In alternativa, scegliere l'azione **Nuovo** per creare prima una nuova categoria articolo come descritto in [Per creare una categoria articolo](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Categorie, attributi e varianti

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Vedere anche

[Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]