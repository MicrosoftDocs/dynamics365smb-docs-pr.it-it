---
title: 'Procedura: Rivalutare il magazzino | Documenti Microsoft'
description: "Descrive come rivalutare o ammortizzare il valore di uno o più articoli in magazzino registrandone il corrente valore calcolato."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0f7137b3ac4e2c68c1c9a9b94b3ba73e0438a4a9
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-revalue-inventory"></a>Procedura: Rivalutare il magazzino
Per rivalutare o ammortizzare un determinato articolo o movimento contabile articolo, è necessario utilizzare le registrazioni rivalutazioni.

## <a name="to-revalue-inventory"></a>Per rivalutare il magazzino
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Registrazioni rivalutazioni**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Calcola valore magazzino**.
3. Nella finestra **Calcola valore magazzino** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere il pulsante **OK**.
5. In ciascuna riga nella finestra **Registrazioni rivalutazioni**, nel campo **Costo unitario (rivalutato)**, immettere il nuovo costo unitario. In alternativa, immettere il nuovo importo totale nel campo **Costo unitario (rivalutato)**.

    I dati pertinenti vengono automaticamente aggiornati. Si noti che il campo **Importo** mostra la modifica effettiva del valore di magazzino per il movimento contabile articolo selezionato. Calcola la differenza tra il campo **Valore Magazzino (Calcolato)** e il campo **Valore Magazzino (Rivalutato)**.
6. Una volta completate tutte le righe nelle registrazioni rivalutazioni, scegliere l'azione **Registra**.

Vengono a questo punto creati i nuovi movimenti di valorizzazione che riflettono le rivalutazioni registrate. È possibile visualizzare i nuovi valori nelle rispettive schede articolo.

## <a name="see-also"></a>Vedi anche
[Magazzino](inventory-manage-inventory.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

