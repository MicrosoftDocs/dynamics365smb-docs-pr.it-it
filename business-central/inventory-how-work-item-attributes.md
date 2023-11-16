---
title: Impostare attributi di articoli e assegnarli agli articoli
description: 'Descrive come impostare i valori di attributo articolo, ad esempio che possono essere utilizzati come parole di ricerca, e come assegnarli agli articoli e alle categorie di articoli.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'categories, search words, facets'
ms.search.forms: '7507, 7509, 7506, 7505, 7503, 7502, 7510, 7504, 7501, 7500, 9110, 5734, 7508'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="work-with-item-attributes"></a>Usare gli attributi articolo

Quando i clienti richiedono informazioni su un articolo, per corrispondenza o in un negozio Web integrato, possono chiedere o cercare in base alle caratteristiche, ad esempio l'altezza e l'anno del modello. Per fornire all'assistenza ai clienti, è possibile assegnare valori di attributo articolo di diversi tipi agli articoli e utilizzarli durante la ricerca degli articoli.

È inoltre possibile assegnare gli attributi degli articoli alle categorie di articoli, che quindi si applicano agli articoli che utilizzano le categorie di articoli. Per ulteriori informazioni, vedere [Classificare gli articoli](inventory-how-categorize-items.md).

> [!TIP]  
> Se all'articolo vengono allegate delle immagini, l'estensione per l'analisi delle immagini può individuare gli attributi nell'immagine e suggerire gli attributi in modo che sia possibile specificare se assegnarli. L'estensione è pronta. È solo necessario abilitarla. Per ulteriori informazioni, vedere [Estensione di analisi immagini](ui-extensions-image-analyzer.md).

## <a name="create-item-attributes"></a>Creare gli attributi articolo

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Attributi articolo**, quindi scegli il collegamento correlato.
2. Nella pagina **Attributi articolo** scegliere l'azione **Nuovo**.
3. Nella pagina **Attributi articolo** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Se selezioni **Opzione** nel campo **Tipo** puoi scegliere l'azione **Valori attributo articolo** per creare valori per l'attributo dell'articolo. Per ulteriori informazioni, vedere [Per creare i valori per gli attributi articolo di tipo Opzione](inventory-how-work-item-attributes.md#create-values-for-item-attributes-of-type-option).  

## <a name="create-values-for-item-attributes-of-type-option"></a>Creare i valori per gli attributi articolo di tipo Opzione

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Attributi articolo**, quindi scegli il collegamento correlato.
2. Nella pagina **Attributi articolo** selezionare l'attributo dell'articolo di tipo **Opzione** per cui si desidera creare i valori, quindi selezionare l'azione **Valori attributo articolo**.
3. Nella pagina **Valori attributo articolo** compilare i campi secondo le proprie necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="assign-item-attributes-to-items"></a>Assegnare attributi articolo agli articoli

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Nella pagina **Articoli**, selezionare l'articolo a cui si desidera assegnare gli attributi articoli quindi selezionare l'azione **Attributi**.
3. Nella pagina **Valori attributo articolo** scegliere l'azione **Nuovo**.
4. Nel campo **Attributo** scegliere il pulsante di ricerca e selezionare un attributo articolo esistente. In alternativa, scegliere l'azione **Nuovo** per creare prima un nuovo attributo articolo come descritto in [Per creare attributi articolo](inventory-how-work-item-attributes.md#create-item-attributes).
5. Nel campo **Valore** immettere il valore dell'attributo articolo, ad esempio "2010" per l'attributo **Anno modello**.
6. Per gli attributi articolo di tipo **Opzione**, scegliere il pulsante di ricerca nel campo **Valore**, quindi selezionare un valore di attributo articolo. In alternativa, scegliere l'azione **Nuovo** per creare prima un nuovo valore di attributo articolo come descritto in [Per creare i valori per gli attributi articolo di tipo Opzione](inventory-how-work-item-attributes.md#assign-item-attributes-to-items).
7. Ripetere i passaggi da 4 a 6 per tutti gli attributi articoli che si desidera assegnare all'articolo.

## <a name="assign-item-attributes-to-item-categories"></a>Assegnare attributi articolo alle categorie articoli

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie articoli**, quindi scegli il collegamento correlato.
2. Nella pagina **Categorie articoli**, selezionare la categoria dell'articolo a cui si desidera assegnare gli attributi articolo quindi selezionare l'azione **Modifica**.
3. Nella pagina **Scheda categoria articolo**, scegliere l'azione **Nuovo** nella Scheda dettaglio **Attributi**.
4. Nel campo **Attributo** scegliere il pulsante di ricerca e selezionare un attributo articolo esistente. In alternativa, scegliere l'azione **Nuovo** per creare prima un nuovo attributo articolo come descritto in [Per creare attributi articolo](inventory-how-work-item-attributes.md#create-item-attributes).
5. Nel campo **Valore predefinito** scegliere il pulsante di ricerca e selezionare un valore attributo articolo.
6. Ripetere i passaggi da 4 a 5 per tutti gli attributi articoli che si desidera assegnare alla categoria articolo.

> [!NOTE]  
> Gli attributi degli articoli per le categorie articolo padre verranno ereditati dalle categorie articolo figlio. Ciò è indicato dal campo **Ereditato da** nella Scheda dettaglio **Attributi**. Per ulteriori informazioni, vedere [Classificare gli articoli](inventory-how-categorize-items.md).

## <a name="filter-by-item-attributes"></a>Filtrare per attributi articolo

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Nella pagina **Articoli** scegliere l'azione **Filtra per attributi**.
3. Nella pagina **Filtra articoli per attributo**, fare clic sul pulsante di ricerca nel campo **Attributo** e selezionare un attributo dell'articolo.
4. Nel campo **Valore** scegliere il pulsante di ricerca e selezionare un valore attributo in base a cui filtrare gli articoli.

    > [!NOTE]  
    > È possibile selezionare solo i valori direttamente per gli attributi dell'articolo che hanno valori fissi, ad esempio il colore. Per gli attributi dell'articolo che hanno valori variabili, quali la larghezza, è necessario specificare il valore dell'attributo dell'articolo selezionando prima una condizione. Vedere il passaggio 5.
5. Nel campo **Valore** per un attributo articolo variabile, fare clic sul pulsante di ricerca.
6. Nella pagina **Specifica valore filtro** nel campo **Condizione**, fare clic sulla freccia rivolta verso il basso e selezionare una condizione.
7. Nel campo **Valore**, immettere un valore attributo in base a cui filtrare gli articoli.

    **Esempio**: per filtrare gli articoli in cui la descrizione materiale inizia con "blu", compilare i campi come segue: **Attributo** campo: Descrizione materiale, **Condizione** campo: Inizia con **Valore**, campo: blu.
8. Scegliere il pulsante **OK**.

Gli articoli nella pagina **Articoli** vengono filtrati in base ai valori dell'attributo articolo specificato.

## <a name="see-also"></a>Vedere anche

[Classificare gli articoli](inventory-how-categorize-items.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
