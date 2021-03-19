---
title: Creare nuovi movimenti di valorizzazione per gli articoli in magazzino| Documenti Microsoft
description: Descrive come rivalutare o ammortizzare i movimenti di valorizzazione di uno o più articoli in magazzino registrandone il corrente valore calcolato.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5f4028a7c081bf73c23c57bcb4707d678b4e47d6
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393076"
---
# <a name="revalue-inventory"></a>Rivalutare il magazzino
Per rivalutare o ammortizzare un determinato articolo o movimento contabile articolo, è necessario utilizzare le registrazioni rivalutazioni.

## <a name="to-revalue-inventory"></a>Per rivalutare il magazzino
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni rivalutazioni** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Calcola valore magazzino**.
3. Nella pagina **Calcola valore magazzino** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere il pulsante **OK**.
5. In ciascuna riga nella pagina **Registrazioni rivalutazioni**, nel campo **Costo unitario (rivalutato)**, immettere il nuovo costo unitario. In alternativa, immettere il nuovo importo totale nel campo **Costo unitario (rivalutato)**.

    I dati pertinenti vengono automaticamente aggiornati. Si noti che il campo **Importo** mostra la modifica effettiva del valore di magazzino per il movimento contabile articolo selezionato. Calcola la differenza tra il campo **Valore Magazzino (Calcolato)** e il campo **Valore Magazzino (Rivalutato)**.
6. Una volta completate tutte le righe nelle registrazioni rivalutazioni, scegliere l'azione **Registra**.

Vengono a questo punto creati i nuovi movimenti di valorizzazione che riflettono le rivalutazioni registrate. È possibile visualizzare i nuovi valori nelle rispettive schede articolo.

## <a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Rivalutazione](design-details-revaluation.md)  
[Magazzino](inventory-manage-inventory.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]