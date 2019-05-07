---
title: Utilizzare cross reference articolo | Microsoft Docs
description: "Se si imposta un cross-reference tra la descrizione articolo utilizzata per un articolo e la descrizione che il fornitore dell'articolo utilizza, la descrizione articolo del fornitore viene inserita automaticamente nei documenti di acquisto per il fornitore quando si compila il campo **Nr. cross-reference**  "
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "927104"
---
# <a name="use-item-cross-references"></a>Utilizzare Cross reference articolo
Se si imposta un cross-reference tra la descrizione articolo utilizzata per un articolo e la descrizione che il fornitore dell'articolo utilizza, la descrizione articolo del fornitore viene inserita automaticamente nei documenti di acquisto per il fornitore quando si compila il campo **Nr. cross-reference**   La stessa funzionalità è valida per i numeri di articolo cliente nei documenti di vendita.

Di seguito viene descritto come utilizzare i cross reference articolo per gli acquisti. I passaggi sono simili per gli acquisti.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Per impostare un cross reference articolo per una descrizione articolo di un fornitore
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Aprire la scheda di un articolo per il quale si desidera creare un cross reference per la descrizione articolo che il fornitore utilizza per l'articolo.
3. Scegliere l'azione **Cross reference**.
4. In una nuova riga nella pagina **Cross reference per l'articolo**, compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Per immettere la descrizione articolo di un fornitore in un ordine di acquisto
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e selezionare il collegamento correlato.
2. Creare un ordine di acquisto per il fornitore per il quale si è impostato un cross-reference articolo nella procedura precedente.
3. Creare una riga acquisto per l'articolo per il quale si è impostato un cross reference articolo nella procedura precedente.
4. Nel campo **Nr. cross-reference** selezionare il cross-reference articolo creato quindi scegliere il pulsante **OK**.

Il campo **Descrizione** della riga viene sovrascritto con la descrizione articolo del fornitore, come definito nel movimento cross-reference articolo.

## <a name="see-also"></a>Vedi anche
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
