---
title: Stampare una lista prelievi magazzino da un ordine di vendita
description: È possibile stampare una lista prelievo magazzino direttamente da un ordine di vendita, vendite, fattura e altri documenti di vendita in uscita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4cddce48df3be0a3fadaa74ed751b274ccce7f31
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115463"
---
# <a name="print-the-picking-list"></a>Stampare la lista prelievo

È possibile stampare una lista prelievo magazzino direttamente da un ordine di vendita e altri documenti che avviano la spedizione di articoli.

Questo report viene in genere utilizzato in società senza funzionalità dedicata per la gestione del magazzino, in modo che un addetto all'inventario possa semplicemente visualizzare o stampare la lista prelievo dal relativo documento di vendita. In società con volumi più elevati o processi più complessi, il prelievo viene pianificato ed eseguito in documenti di magazzino dedicati. Per ulteriori informazioni, vedere [Prelevare articoli](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Per stampare una lista prelievo da un ordine di vendita

La seguente procedura è basata su un ordine di vendita. I passaggi sono simili per tutti i documenti di vendita che possono essere utilizzati per avviare la spedizione degli articoli, come l'ordine di trasferimento.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.  
2. Aprire l'ordine di vendita per cui si desidera prelevare gli articoli.  
3. Scegliere l'azione **Report**, quindi scegliere l'azione **Lista prelievo per ordine**.  
4. Scegliere il pulsante **Stampa** per stampare la lista prelievo oppure scegliere il pulsante **Anteprima** per visualizzarla sullo schermo.

È inoltre possibile salvare la lista prelievo come documento, ad esempio da inviare a qualcuno o da aggiungere come allegato all'ordine di vendita. Per ulteriori informazioni, vedere [Gestire allegati, collegamenti e note in schede e documenti](ui-how-add-link-to-record.md).

> [!NOTE]
> Se si è utilizzata la funzione **Esplodi DB** nell'ordine di vendita, nel report vengono visualizzati solo i componenti dell'articolo di assemblaggio correlato. Per altre informazioni, vedere [Utilizzare le distinte base](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Vedere anche

[Magazzino](inventory-manage-inventory.md)  
[Prelievo degli articoli](warehouse-pick-items.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]