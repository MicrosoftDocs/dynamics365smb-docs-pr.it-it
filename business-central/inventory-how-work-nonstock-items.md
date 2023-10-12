---
title: Creare e gestire gli articoli di catalogo
description: Scopri come vendere gli articoli non presenti nell'elenco degli articoli.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# <a name="work-with-catalog-items"></a>Utilizzare gli articoli di catalogo

Gli articoli del catalogo sono articoli che non gestisci in [!INCLUDE[prod_short](includes/prod_short.md)] finché non li vendi. Quando usi l'azione **Seleziona l'articolo del catalogo** per aggiungere un articolo del catalogo a una riga di un ordine cliente, un'offerta o un ordine di vendita programmato, l'articolo del catalogo viene convertito in un articolo normale.

> [!NOTE]  
> Non è possibile selezionare un articolo di catalogo dalla pagina **Fattura di vendita**.

Un articolo di catalogo ha in genere il numero di articolo del fornitore che lo fornisce. Prima di poter convertire un articolo del catalogo in un articolo normale, è necessario specificare come convertire i numeri articolo fornitore nella numerazione dell'articolo. Per ulteriori informazioni sulla numerazione degli articoli, vedi [Specificare come i numeri articolo di catalogo vengono convertiti nella numerazione dell'utente](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Gli articoli di catalogo non devono essere confusi con articoli non di magazzino, che sono articoli standard a cui è assegnato il tipo **Non in inventario** per tenerli fuori dalla disponibilità e dai calcoli dei costi, ad esempio perché sono utilizzati solo internamente e hanno un costo ridotto. Per informazioni sugli articoli non in inventario, vai a [Informazioni sui tipi di articoli](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Creare un articolo di catalogo

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli di catalogo**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Specificare come i numeri articolo di catalogo vengono convertiti nella numerazione dell'utente

Prima di poter convertire un articolo del catalogo in un articolo regolare, è necessario specificare come convertire i numeri articolo fornitore nella struttura usata per i numeri dell'articolo.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup articolo di catalogo**, quindi scegli il collegamento correlato.
2. Nel campo **Nr. formato**, scegli l'opzione che preferisci.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Convertire un articolo di catalogo in articolo normale

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli di catalogo**, quindi scegli il collegamento correlato.
2. Aprire la scheda dell'articolo di catalogo da convertire in articolo normale.
3. Nella pagina **Scheda articolo di catalogo** scegliere l'azione **Crea articolo**.

Verrà visualizzata una nuova scheda articolo precompilata con le informazioni dell'articolo di catalogo e viene creato un modello articolo. È possibile modificare le informazioni sul nuovo articolo, se necessario. Per ulteriori informazioni sulla creazione degli articoli, vai a [Registrare nuovi articoli](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Per vendere un articolo di catalogo e convertirlo in articolo normale

Il seguente processo utilizza un ordine di vendita, ma i passaggi sono gli stessi per gli ordini di vendita programmati e le offerte.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Scegliere l'azione **Nuovo**. Compilare i campi nella Scheda dettaglio **Generale** come per qualsiasi ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
3. In una nuova riga vendite, nel campo **Tipo**, selezionare **Articolo**, ma lasciare **Nr.** essere lasciato vuoto.
4. Scegliere l'azione **Riga**, quindi l'azione **Selezionare articoli di catalogo**.
5. Nella pagina **Articoli di catalogo** selezionare l'articoli di catalogo che si desidera vendere, quindi scegliere **OK**.
6. Una volta completato l'ordine di vendita, scegliere l'azione **Registra**.

> [!NOTE]  
> Un riferimento di articolo viene automaticamente inserito tra il numero di articolo del venditore e il tuo nuovo numero di articolo. Per ulteriori informazioni sui riferimenti agli articoli, vai a [Usare i riferimenti agli articoli](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Creare ordini speciali](sales-how-to-create-special-orders.md)  
[Inventario](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
