---
title: Creare e gestire gli articoli di catalogo
description: Descrive come trattare articoli che sono nell'elenco di fornitori degli articoli ma non nel proprio elenco di articoli trattati.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8f8d97f10904664dc68bec6ccb85823a765a58aa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8137889"
---
# <a name="work-with-catalog-items"></a>Utilizzare gli articoli di catalogo
È possibile offrire per loro comodità determinati articoli ai clienti che non si desidera gestire nel sistema fino a quando non si inizia a venderli. Se si desidera iniziare a gestire nel sistema tali articoli, è possibile convertirli in schede articolo normali in due modi.

* Dalla scheda articolo di catalogo, creare una nuova scheda articolo in base a un modello.
* Da una riga di ordine di vendita di tipo **Articolo** con un campo vuoto **No**, selezionare un articolo di catalogo. Una scheda articolo viene creata automaticamente per l'articolo di catalogo.

> [!NOTE]  
> Non è possibile selezionare un articolo di catalogo dalla pagina **Fattura di vendita**.<br /><br />
> È possibile selezionare un articolo di catalogo dalla pagina **Offerta di vendita**, ma l'articolo di catalogo non verrà convertito in articolo normale quando si utilizza la funzione **Crea ordine**.

Un articolo di catalogo ha in genere il numero di articolo del fornitore che lo fornisce. Per abilitare la conversione di una scheda articolo di catalogo in una scheda articolo normale, è necessario impostare come la numerazione articolo fornitore viene convertita nella numerazione articolo dell'utente.   

> [!Important]
> Gli articoli di catalogo non devono essere confusi con articoli non di magazzino, che sono articoli standard a cui è assegnato il tipo **Non in inventario** per tenerli fuori dalla disponibilità e dai calcoli dei costi, ad esempio perché sono utilizzati solo internamente e hanno un costo ridotto. Per ulteriori informazioni, vedere [Informazioni sui tipi di articolo](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Per creare un articolo di catalogo
Nelle schede articolo di catalogo sono presenti molte informazioni in meno rispetto alle schede articolo normale perché vengono utilizzate solo per offrirle in offerte e in altri modi. Per tale motivo, devono essere convertite in schede articolo normale prima di registrare le transazioni di vendita relative.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli di catalogo**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Per impostare come i numeri articolo di catalogo vengono convertiti nella numerazione dell'utente
Per abilitare la conversione di una scheda articolo di catalogo in una scheda articolo normale, è necessario impostare la modalità con cui la numerazione articolo fornitore viene convertita nel formato di numerazione articolo dell'utente.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup articolo di catalogo**, quindi scegli il collegamento correlato.
2. Compilare i campi come necessario.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Per convertire un articolo di catalogo in articolo normale
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli di catalogo**, quindi scegli il collegamento correlato.
2. Aprire la scheda dell'articolo di catalogo da convertire in articolo normale.
3. Nella pagina **Scheda articolo di catalogo** scegliere l'azione **Crea articolo**.

Viene creata una nuova scheda articolo precompilata con le informazioni dell'articolo del catalogo e un modello di articolo pertinente. È possibile immettere o modificare i campi della nuova scheda articolo secondo le necessità. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Per vendere un articolo di catalogo e convertirlo in articolo normale
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Scegliere l'azione **Nuovo**. Compilare i campi nella Scheda dettaglio **Generale** come per qualsiasi ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
3. In una nuova riga vendite, nel campo **Tipo**, selezionare **Articolo**, ma lasciare **Nr.** essere lasciato vuoto.
4. Scegliere l'azione **Riga**, quindi l'azione **Selezionare articoli di catalogo**.

    L'articolo di catalogo viene convertito in articolo normale. Verrà visualizzata una nuova scheda articolo precompilata con le informazioni dell'articolo di catalogo e viene creato un modello articolo relativo.
5. Nella pagina **Articoli di catalogo** selezionare l'articoli di catalogo che si desidera vendere, quindi scegliere **OK**.
6. Una volta completato l'ordine di vendita, scegliere l'azione **Registra**.

È possibile immettere o modificare i campi della nuova scheda articolo secondo le necessità. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

> [!NOTE]  
>   Un riferimento di articolo viene automaticamente inserito tra il numero di articolo del venditore e il tuo nuovo numero di articolo. Per maggiori informazioni, vedere [Use Elemento References](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Vedere anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Creare ordini speciali](sales-how-to-create-special-orders.md)|  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]