---
title: Utilizzare i riferimenti dell'elemento
description: Impostare i riferimenti tra le descrizioni che voi e il vostro venditore usate per un articolo per inserire la descrizione dell'articolo del venditore sui documenti di acquisto.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588603"
---
# <a name="use-item-references"></a>Utilizzare i riferimenti dell'elemento
Se impostate un riferimento tra la descrizione dell'articolo che usate per un articolo e la descrizione che usa il venditore di quell'articolo, allora la descrizione dell'articolo del venditore viene automaticamente inserita nei documenti di acquisto per il venditore quando compilate il **Numero di riferimento dell'articolo**. . La stessa funzionalità è valida per i numeri di articolo cliente nei documenti di vendita.

Le seguenti procedure descrivono come utilizzare i riferimenti degli articoli dal lato dell'acquisto. I passaggi sono simili per gli acquisti.

> [!NOTE]
> Non tutte le aziende usano i riferimenti agli articoli, quindi per minimizzare il disordine nelle pagine abbiamo nascosto i campi e le azioni relative. Se decidi di usarli, puoi attivare il toggle **Utilizzare i riferimenti dell'elemento** nella pagina **Setup magazzino** . Dopo aver abilitato i riferimenti agli articoli, i campi e le azioni sono disponibili nelle pagine Scheda articolo, Scheda venditore e Scheda cliente, e dai documenti di vendita e acquisto.

## <a name="to-start-using-item-references"></a>Per iniziare a usare i riferimenti agli elementi
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup magazzino**, quindi scegli il collegamento correlato.
2. Attivare il toggle **Utilizzare i riferimenti dell’elemento**.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Per impostare un riferimento a una descrizione dell'articolo di un venditore

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci **Elemento** e scegli il link relativo.
2. Apri la scheda di un articolo per il quale vuoi creare un riferimento alla descrizione dell'articolo che il venditore usa per quell'articolo.
3. Scegli l'azione **Riferimenti elemento** .

     Se non riesci a trovare l'azione **Riferimenti dell'elemento**, scegli di visualizzare altre opzioni, e poi trovala sotto **Elemento** > **correlato**.
  
4. Su una nuova riga della pagina **Voci di riferimento dell’elemento**, compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Per immettere la descrizione articolo di un fornitore in un ordine di acquisto

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.
2. Create un ordine di acquisto per il fornitore per il quale avete impostato un riferimento di articolo nella procedura precedente.
3. Crea una linea di acquisto per l'articolo per il quale hai impostato un riferimento di articolo nella procedura precedente.
4. Nel **numero di riferimento della voce** seleziona il riferimento all'elemento che hai creato e poi scegli il pulsante **OK** .

Il campo **Descrizione** sulla riga viene sovrascritto con la descrizione dell'articolo del venditore, come impostato nella voce di riferimento dell'articolo.

## <a name="see-also"></a>Vedere anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]