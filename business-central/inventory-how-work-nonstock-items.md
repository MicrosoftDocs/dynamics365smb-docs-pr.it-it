---
title: Creare e gestire gli articoli di catalogo
description: Descrive come vendere gli articoli non presenti nell'elenco degli articoli.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
ms.date: 06/20/2022
ms.author: bholtorf
---
# Utilizzare gli articoli di catalogo

Gli articoli del catalogo sono articoli che non gestisci in [!INCLUDE[prod_short](includes/prod_short.md)] finché non li vendi. Quando usi l'azione **Seleziona l'articolo del catalogo** per aggiungere un articolo del catalogo a una riga di un ordine cliente o di un'offerta, l'articolo del catalogo viene convertito in un articolo normale.

> [!NOTE]  
> Non è possibile selezionare un articolo di catalogo dalla pagina **Fattura di vendita**.

Un articolo di catalogo ha in genere il numero di articolo del fornitore che lo fornisce. Prima di poter convertire un articolo del catalogo in un articolo normale, è necessario specificare come convertire i numeri articolo fornitore nella numerazione dell'articolo. Per ulteriori informazioni, vedi [Specificare come i numeri articolo di catalogo vengono convertiti nella numerazione dell'utente](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Gli articoli di catalogo non devono essere confusi con articoli non di magazzino, che sono articoli standard a cui è assegnato il tipo **Non in inventario** per tenerli fuori dalla disponibilità e dai calcoli dei costi, ad esempio perché sono utilizzati solo internamente e hanno un costo ridotto. Per ulteriori informazioni, vedere [Informazioni sui tipi di articolo](inventory-about-item-types.md).

## Creare un articolo di catalogo

Nelle schede articolo di catalogo sono presenti molte informazioni in meno rispetto alle schede articolo normale perché vengono utilizzate solo per offrirle in offerte e in altri modi. Per tale motivo, devono essere convertite in schede articolo normale prima di registrare le transazioni di vendita relative.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli di catalogo**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Specificare come i numeri articolo di catalogo vengono convertiti nella numerazione dell'utente

Prima di poter convertire un articolo del catalogo in un articolo normale, è necessario specificare come convertire i numeri articolo fornitore nella numerazione dell'articolo.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup articolo di catalogo**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze.

## Convertire un articolo di catalogo in articolo normale

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli di catalogo**, quindi scegli il collegamento correlato.
2. Aprire la scheda dell'articolo di catalogo da convertire in articolo normale.
3. Nella pagina **Scheda articolo di catalogo** scegliere l'azione **Crea articolo**.

Viene creata una nuova scheda articolo precompilata con le informazioni dell'articolo del catalogo e un modello di articolo pertinente. È possibile immettere o modificare i campi della nuova scheda articolo secondo le necessità. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

## Per vendere un articolo di catalogo e convertirlo in articolo normale

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Scegliere l'azione **Nuovo**. Compilare i campi nella Scheda dettaglio **Generale** come per qualsiasi ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
3. In una nuova riga vendite, nel campo **Tipo**, selezionare **Articolo**, ma lasciare **Nr.** essere lasciato vuoto.
4. Scegliere l'azione **Riga**, quindi l'azione **Selezionare articoli di catalogo**.

    L'articolo di catalogo viene convertito in articolo normale. Verrà visualizzata una nuova scheda articolo precompilata con le informazioni dell'articolo di catalogo e viene creato un modello articolo relativo.
5. Nella pagina **Articoli di catalogo** selezionare l'articoli di catalogo che si desidera vendere, quindi scegliere **OK**.
6. Una volta completato l'ordine di vendita, scegliere l'azione **Registra**.

È possibile immettere o modificare i campi della nuova scheda articolo secondo le necessità. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

> [!NOTE]  
> Un riferimento di articolo viene automaticamente inserito tra il numero di articolo del venditore e il tuo nuovo numero di articolo. Per maggiori informazioni, vedere [Use Elemento References](inventory-how-use-item-cross-refs.md).

## Vedi il relativo [training Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/)

## Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Creare ordini speciali](sales-how-to-create-special-orders.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
