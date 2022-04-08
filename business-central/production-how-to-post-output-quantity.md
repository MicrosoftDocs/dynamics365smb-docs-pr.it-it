---
title: Registrare l'output e i tempi di lavorazione tramite processo batch
description: La quantità di output rappresenta l'avanzamento del lavoro sotto forma di quantità finita e capacità utilizzata del centro lavoro o della macchina.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000773, 99000778, 99000823, 99000827
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7a1c30340efabed66e4ce359fc7680945e0db1de
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522748"
---
# <a name="batch-post-output-and-run-times"></a>Registrare l'output e i tempi di lavorazione tramite processo batch
La quantità di output rappresenta l'avanzamento del lavoro sotto forma di quantità finita e capacità utilizzata del centro lavoro o della macchina.

È possibile usare le registrazioni output su:

* Rettifica il magazzino in relazione all'output degli articoli finiti da produzione.
* Registrare le quantità e gli scarti per ciascuna operazione nel ciclo di produzione.
* Registrare la configurazione e il tempo di esecuzione per il lavoro e i centri lavoro.

> [!NOTE]
> Se viene utilizzato un instradamento della produzione, il magazzino viene aggiornato solo quando registri la quantità di output nell'ultima operazione.

Tramite la finestra **Registrazioni di produzione**, è possibile eseguire le stesse attività della finestra **Registrazioni output** e allo stesso tempo le relative attività di registrazione del consumo. Per ulteriori informazioni, vedi [Registrare i consumi e l'output relativi a una singola riga dell'ordine di produzione rilasciato](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Per registrare quantità di output e/o registrare tempi di lavorazione per una o più righe dell'ordine di produzione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni output**, quindi scegli il collegamento correlato.  
2. Compilare i campi inserendo i dati relativi agli ordini di produzione e/o ai tempi di lavorazione. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Puoi usare la funzione **Esplodi ciclo** per generare righe di registrazione dagli ordini di produzione.
  
3. Se l'operazione è stata completata, selezionare il campo **Completato** .  
4. Per registrare le operazioni scegliere l'azione **Registra**. 

I movimenti contabili capacità vengono aggiornati per il lavoro utilizzato o per i centri lavoro con informazioni su tempo e quantità di produzione e scarto.  

Se hai registrato l'ultima operazione, l'articolo verrà aggiunto al magazzino.  

## <a name="see-also"></a>Vedere anche

[Registrare lo scarto manualmente](production-how-to-post-scrap.md)
[Stornare la registrazione dell'output](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
