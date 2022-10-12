---
title: Prelevare per le operazioni interne in configurazioni di warehouse avanzate
description: Se le ubicazioni utilizzano il prelievo e la spedizione, preleva i componenti per le attività di produzione, assemblaggio e commessa nella pagina Prelievo warehouse.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607555"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Prelevare per produzione, assemblaggio o commesse in configurazioni di warehouse avanzate

Nelle configurazioni di warehouse avanzate in cui l'ubicazione è impostata in modo da utilizzare sia il prelievo che la spedizione, è possibile prelevare componenti per le attività di assemblaggio e produzione tramite la pagina **Prelievo warehouse**.  

Puoi anche utilizzare la pagina **Prospetto movimentazioni** per spostare gli articoli tra le collocazioni, ovvero senza riferimento a un documento di origine. Per ulteriori informazioni, vedere [Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Per informazioni sugli articoli di prelievo nelle ubicazioni di warehouse impostate per prelevare solo, vedi [Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)..  

> [!NOTE]
> Non è possibile creare un documento di prelievo warehouse da zero perché un'attività di prelievo fa sempre parte di un flusso di lavoro, in uno scenario di tipo push o pull.  

È possibile creare il documento di prelievo warehouse in modalità push selezionando **Crea prelievo whse.** nel documento di origine, ad esempio un ordine di assemblaggio rilasciato o una spedizione warehouse. Per ulteriori informazioni, vedere [Prelevare articoli con prelievi warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

È inoltre possibile creare un documento di prelievo warehouse in modalità pull utilizzando la pagina **Prospetto prelievi** per rilevare le richieste di prelievo. Questo metodo è utile per la spedizione e le operazioni interne. Puoi quindi creare i documenti di prelievo warehouse richiesti.  

La procedura seguente illustra uno scenario di tipo pull in cui si prelevano componenti per un ordine di produzione rilasciato tramite la pagina **Prospetto prelievi**. La procedura si applica anche a un ordine di assemblaggio.  

Per creare richieste di prelievo, sia per scenari pull e push, i documenti di origine in questione devono essere rilasciati. Rilasciare i documenti di origine per le operazioni interne nei seguenti modi.  

|Documento origine|Metodo di rilascio|  
|---------------------|--------------------|  
|Ordine di produzione|Modificare il tipo di ordine in Ordine produzione rilasciato.|  
|Ordine di assemblaggio|Modificare lo stato in Rilasciato.|
|Commesse | Modifica lo stato in Aperto.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Per prelevare componenti mediante i prospetti prelievi

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto prelievi**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Prendi documenti warehouse**, quindi selezionare le righe componenti dall'ordine di produzione rilasciato.  
3. Ordina le righe per garantire un prelievo efficiente. Potresti voler combinare le righe per risparmiare tempo ai dipendenti.  
4. Scegliere l'azione **Crea prelievo**.  
5. Definire come creare documenti di prelievo warehouse e come ordinare le righe prelievo compilando i campi nella pagina **Crea prelievo**.  
6. Scegliere il pulsante **OK**. I documenti di prelievo warehouse vengono creati con le righe prelievo per ogni componente richiesto nell'operazione interno.  

Le aree operative come le officine di produzione potrebbero avere una collocazione predefinita per i componenti di cui hanno bisogno. In tal caso, il codice collocazione predefinito viene aggiunto al documento di prelievo warehouse per indicare dove inserire gli articoli. Per ulteriori informazioni, vedi i suggerimenti per i campi **Cod. coll. art. per produzione** o **Cod. coll. art. per assembl**.

## <a name="filling-the-consumption-bin"></a>Rifornimento della collocazione di consumo

Questo diagramma di flusso illustra in che modo il campo **Cod. collocazione** nelle righe del componente dell'ordine di produzione viene compilato in base al setup dell'ubicazione.

![Diagramma di flusso collocazione.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Vedere anche

[Warehouse Management](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
