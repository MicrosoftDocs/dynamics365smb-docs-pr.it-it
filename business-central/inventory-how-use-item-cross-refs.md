---
title: Utilizzare Cross reference articoli
description: Impostare i riferimenti tra le descrizioni che l'utente e il fornitore utilizzano per un articolo in modo da poter inserire la descrizione dell'articolo del fornitore nei documenti di acquisto.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 7d670f6553a1bd70dcc3d97f90436f36c6627c56
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013794"
---
# <a name="use-item-cross-references"></a>Utilizzare Cross reference articolo
Se si imposta un cross-reference tra la descrizione articolo utilizzata per un articolo e la descrizione che il fornitore dell'articolo utilizza, la descrizione articolo del fornitore viene inserita automaticamente nei documenti di acquisto per il fornitore quando si compila il campo **Nr. cross-reference**   La stessa funzionalità è valida per i numeri di articolo cliente nei documenti di vendita.

Di seguito viene descritto come utilizzare i cross reference articolo per gli acquisti. I passaggi sono simili per gli acquisti.

> [!NOTE]
> Sta diventando sempre più comune che gli identificatori degli articoli come GTIN o GUID contengano 30 o più caratteri, che è più di quanto la funzionalità corrente per i riferimenti incrociati degli articoli possa gestire. Se è necessario utilizzare riferimenti che contengono più di 30 caratteri, l'amministratore può attivare la funzionalità **scrittura di riferimenti articolo più lunghi** nella pagina [Gestione delle funzionalità](https://businesscentral.dynamics.com/?page=2610) (il collegamento richiede un tenant [!INCLUDE[prod_short](includes/prod_short.md)]). Il modo in cui si usano i riferimenti non cambia, ma i nomi di cose come pagine e pulsanti cambia. Ad esempio, la pagina **Cross reference per l'articolo** diventerà la pagina **Movimenti riferimento per l'articolo**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Per impostare un cross reference articolo per una descrizione articolo di un fornitore

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Aprire la scheda di un articolo per il quale si desidera creare un cross reference per la descrizione articolo che il fornitore utilizza per l'articolo.
3. Scegliere l'azione **Cross reference**.

     Se non si riesce a trovare l'azione **Cross reference**, scegliere di visualizzare più opzioni, quindi trovarla in **Correlato** > **Articolo**.
  
4. In una nuova riga nella pagina **Cross reference per l'articolo**, compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Per immettere la descrizione articolo di un fornitore in un ordine di acquisto

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.
2. Creare un ordine di acquisto per il fornitore per il quale si è impostato un cross-reference articolo nella procedura precedente.
3. Creare una riga acquisto per l'articolo per il quale si è impostato un cross reference articolo nella procedura precedente.
4. Nel campo **Nr. cross-reference** selezionare il cross-reference articolo creato quindi scegliere il pulsante **OK**.

Il campo **Descrizione** della riga viene sovrascritto con la descrizione articolo del fornitore, come definito nel movimento cross-reference articolo.

## <a name="see-also"></a>Vedere anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]