---
title: Organizzare gli articoli in categorie| Documenti Microsoft
description: Per semplificare la ricerca e trovare gli articoli, è possibile assegnare gli attributi degli articoli e organizzare gli articoli in categorie.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b831443bd9e068b4c20f583cc8e0e7132d75ac5e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441145"
---
# <a name="categorize-items"></a>Classificare gli articoli

Per visualizzare una panoramica degli articoli e semplificare l'ordinamento e la ricerca degli articoli, risulta utile organizzare gli articoli in categorie.

Per trovare gli articoli in base alle caratteristiche, è possibile assegnare gli attributi ad articoli e a categorie articolo. Per ulteriori informazioni, vedere [Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Per creare una categoria articolo
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie articoli**, quindi scegli il collegamento correlato.
2. Nella pagina **Categorie articoli** scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda categoria articolo**, nella Scheda dettaglio **Generale**, compilare i campi in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nella Scheda dettaglio **Attributi**, specificare tutti gli attributi per la categoria articolo. Per ulteriori informazioni, vedere [Per assegnare attributi articolo alle categorie articoli](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Se la categoria articolo è una categoria padre, come indicato dal campo **Categoria padre**, gli attributi articoli assegnati a tale categoria padre sono precompilati nella Scheda dettaglio **Attributi**.

> [!NOTE]  
> Gli attributi degli articoli assegnati a una categoria articolo vengono applicati automaticamente all'articolo a cui la categoria articolo è assegnata.

Se si cambia idea su una categoria di articoli, è possibile eliminarla. Tuttavia, se è già stato assegnato a un articolo, è necessario rimuovere l'assegnazione prima di poter eliminare la categoria dell'articolo.

## <a name="to-assign-an-item-category-to-an-item"></a>Per assegnare una categoria articolo a un articolo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.
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