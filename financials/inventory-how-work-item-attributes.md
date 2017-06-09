---
title: 'Procedura: Utilizzare gli attributi degli articoli| Documenti Microsoft'
description: Descrive come impostare gli attributi degli articoli e assegnarli agli articoli e alle categorie di articoli.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 82fee2e5b1ae3e87e607cd930973a8be32045e71
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-item-attributes"></a>Procedura: Utilizzare gli attributi degli articoli
Quando i clienti richiedono informazioni su un articolo, per corrispondenza o in un negozio Web integrato, possono chiedere o cercare in base alle caratteristiche, ad esempio l'altezza e l'anno del modello. Per fornire all'assistenza ai clienti, è possibile assegnare valori di attributo articolo di diversi tipi agli articoli e utilizzarli durante la ricerca degli articoli.

È inoltre possibile assegnare gli attributi degli articoli alle categorie di articoli, che quindi si applicano agli articoli che utilizzano le categorie di articoli. Per ulteriori informazioni, vedere [Procedura: Classificare gli articoli](inventory-how-categorize-items.md).

## <a name="to-create-item-attributes"></a>Per creare attributi articolo
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Attributi articolo**, quindi scegliere il collegamento correlato.
2. Nella finestra **Attributi articolo** scegliere l'azione **Nuovo**.
3. Nella finestra **Attributi articolo** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Nota**: se si seleziona **Opzione** nel campo **Tipo** è possibile scegliere l'azione **Valori attributo articolo** per creare valori per l'attributo dell'articolo. Per ulteriori informazioni, vedere la sezione "Per creare i valori per gli attributi articolo di tipo Opzione".  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Per creare i valori per gli attributi articolo di tipo Opzione
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Attributi articolo**, quindi scegliere il collegamento correlato.
2. Nella finestra **Attributi articolo** selezionare l'attributo dell'articolo di tipo **Opzione** per cui si desidera creare i valori, quindi selezionare l'azione **Valori attributo articolo**.
3. Nella finestra **Valori attributo articolo** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Per assegnare attributi articolo agli articoli
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Articoli**, selezionare l'articolo a cui si desidera assegnare gli attributi articoli quindi selezionare l'azione **Attributi**.
3. Nella finestra **Valori attributo articolo** scegliere l'azione **Nuovo**.
4. Nel campo **Attributo** scegliere il pulsante di ricerca e selezionare un attributo articolo esistente. In alternativa, scegliere l'azione **Nuovo** per creare prima un nuovo attributo articolo come descritto nella sezione "Per creare attributi articolo".
5. Nel campo **Valore** immettere il valore dell'attributo articolo, ad esempio "2010" per l'attributo **Anno modello**.
6. Per gli attributi articolo di tipo **Opzione**, scegliere il pulsante di ricerca nel campo **Valore**, quindi selezionare un valore di attributo articolo. In alternativa, scegliere l'azione **Nuovo** per creare prima un nuovo valore di attributo articolo come descritto nella sezione "Per creare i valori per gli attributi articolo di tipo Opzione".
7. Ripetere i passaggi da 4 a 6 per tutti gli attributi articoli che si desidera assegnare all'articolo.

## <a name="to-assign-item-attributes-to-item-categories"></a>Per assegnare attributi articolo alle categorie articoli
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Categorie articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Categorie articoli**, selezionare la categoria dell'articolo a cui si desidera assegnare gli attributi articolo quindi selezionare l'azione **Modifica**.
3. Nella finestra **Scheda categoria articolo**, scegliere l'azione **Nuovo** nella Scheda dettaglio **Attributi**.
4. Nel campo **Attributo** scegliere il pulsante di ricerca e selezionare un attributo articolo esistente. In alternativa, scegliere l'azione **Nuovo** per creare prima un nuovo attributo articolo come descritto nella sezione "Per creare un attributo articolo".
5. Nel campo **Valore predefinito** scegliere il pulsante di ricerca e selezionare un valore attributo articolo.
6. Ripetere i passaggi da 4 a 5 per tutti gli attributi articoli che si desidera assegnare alla categoria articolo.

**Nota**: gli attributi degli articoli per le categorie articolo padre verranno ereditati dalle categorie articolo figlio. Ciò è indicato dal campo **Ereditato da** nella Scheda dettaglio **Attributi**. Per ulteriori informazioni, vedere [Procedura: Classificare gli articoli](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Per filtrare per attributi articolo
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Articoli** scegliere l'azione **Filtra per attributi**.
3. Nella finestra **Filtra articoli per attributo**, fare clic sul pulsante di ricerca nel campo **Attributo** e selezionare un attributo dell'articolo.
4. Nel campo **Valore** scegliere il pulsante di ricerca e selezionare un valore attributo in base a cui filtrare gli articoli.

    **Nota**: è possibile selezionare solo i valori direttamente per gli attributi dell'articolo che hanno valori fissi, ad esempio il colore. Per gli attributi dell'articolo che hanno valori variabili, quali la larghezza, è necessario specificare il valore dell'attributo dell'articolo selezionando prima una condizione. Vedere il passaggio 5.
5. Nel campo **Valore** per un attributo articolo variabile, fare clic sul pulsante di ricerca.
6. Nella finestra **Specifica valore filtro** nel campo **Condizione**, fare clic sulla freccia rivolta verso il basso e selezionare una condizione.
7. Nel campo **Valore**, immettere un valore attributo in base a cui filtrare gli articoli.

    **Esempio**: per filtrare gli articoli in cui la descrizione materiale inizia con "blu", compilare i campi come segue: **Attributo** campo: Descrizione materiale, **Condizione** campo: Inizia con **Valore**, campo: blu.
8. Scegliere il pulsante **OK**.   

Gli articoli nella finestra **Articoli** vengono filtrati in base ai valori dell'attributo articolo specificato.

## <a name="see-also"></a>Vedi anche
[Procedura: Classificare gli articoli](inventory-how-categorize-items.md)    
[Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

