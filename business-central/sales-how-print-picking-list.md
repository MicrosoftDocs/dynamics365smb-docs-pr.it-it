---
title: Stampare una lista prelievi magazzino da un ordine di vendita
description: 'È possibile stampare una lista prelievo magazzino direttamente da un ordine di vendita, vendite, fattura e altri documenti di vendita in uscita.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
---
# Stampare la lista prelievo

È possibile stampare una lista prelievo magazzino direttamente da un ordine di vendita e altri documenti che avviano la spedizione di articoli.

Questo report viene in genere utilizzato in società senza funzionalità dedicata per la gestione del magazzino, in modo che un addetto all'inventario possa visualizzare o stampare la lista prelievo dal relativo documento di vendita. In società con volumi più elevati o processi più complessi, la spedizione e il prelievo vengono pianificati ed eseguiti in documenti di magazzino dedicati. Per ulteriori informazioni vedi [Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md).

## Per stampare una lista prelievo da un ordine di vendita

La seguente procedura è basata su un ordine di vendita. I passaggi sono simili per tutti i documenti di vendita che possono essere utilizzati per avviare la spedizione degli articoli, come l'ordine di trasferimento.

1. Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di vendita per cui si desidera prelevare gli articoli.  
3. Scegliere l'azione **Report**, quindi scegliere l'azione **Lista prelievo per ordine**.  
4. Scegliere il pulsante **Stampa** per stampare la lista prelievo oppure scegliere il pulsante **Anteprima** per visualizzarla sullo schermo.

È inoltre possibile salvare la lista prelievo come documento, ad esempio da inviare a qualcuno o da aggiungere come allegato all'ordine di vendita. Per ulteriori informazioni vedi [Gestire allegati, collegamenti e note in schede e documenti](ui-how-add-link-to-record.md).

> [!NOTE]
> Se si è utilizzata la funzione **Esplodi DB** nell'ordine di vendita, nel report vengono visualizzati solo i componenti dell'articolo di assemblaggio correlato. Per ulteriori informazioni vedi [Utilizzare le distinte base](inventory-how-work-BOMs.md).

## Vedere anche

[Magazzino](inventory-manage-inventory.md)  
[Flusso di warehouse in uscita](design-details-outbound-warehouse-flow.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
