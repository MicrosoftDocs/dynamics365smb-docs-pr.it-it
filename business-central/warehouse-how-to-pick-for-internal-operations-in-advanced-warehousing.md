---
title: Prelevare per le operazioni interne in configurazioni di warehouse avanzate
description: Se le ubicazioni utilizzano sia il prelievo che la spedizione, prelevare i componenti per le attività di produzione e assemblaggio nella pagina Prelievo warehouse.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a0704d35debbe8cdd7c2be240c6a02759a919795
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531244"
---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Prelevare per produzione o assemblaggio in configurazioni di warehouse avanzate

Nelle configurazioni di warehouse avanzate in cui l'ubicazione è impostata in modo da utilizzare sia il prelievo che la spedizione, è possibile prelevare componenti per le attività di assemblaggio e produzione tramite la pagina **Prelievo warehouse**.  

In alternativa, è possibile utilizzare la pagina **Prospetto movimentazioni** per spostare gli articoli tra le collocazioni ad hoc, ovvero senza riferimento a un documento di origine. Per ulteriori informazioni, vedere [Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Per informazioni sugli articoli di prelievo per le operazioni interne nelle ubicazioni di warehouse impostate per prelevare solo, vedere [Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)..  

Non è possibile creare un documento di prelievo warehouse da zero perché un'attività di prelievo fa sempre parte di un flusso di lavoro, in uno scenario di tipo push o pull.  

È possibile creare il documento di prelievo warehouse in modalità push selezionando **Crea prelievo whse.** nel documento di origine, ad esempio un ordine di assemblaggio rilasciato o una spedizione warehouse. Per ulteriori informazioni, vedere [Prelevare articoli con prelievi warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

In alternativa, è possibile creare il documento di prelievo warehouse in modalità pull mediante la pagina **Prospetto prelievi** per verificare le richieste di prelievo, sia per la spedizione che per le operazioni interne, quindi creare i documenti di prelievo warehouse necessari.  

La procedura seguente illustra uno scenario di tipo pull in cui si prelevano componenti per un ordine di produzione rilasciato tramite la pagina **Prospetto prelievi**. La procedura si applica anche a un ordine di assemblaggio.  

Per creare richieste di prelievo, sia per scenari pull e push, i documenti di origine in questione devono essere rilasciati. Rilasciare i documenti di origine per le operazioni interne nei seguenti modi.  

|Documento origine|Metodo di rilascio|  
|---------------------|--------------------|  
|Ordine di produzione|Modificare il tipo di ordine in Ordine produzione rilasciato.|  
|Ordine di assemblaggio|Modificare lo stato in Rilasciato.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Per prelevare componenti mediante i prospetti prelievi

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto prelievi**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Prendi documenti warehouse**, quindi selezionare le righe componenti dall'ordine di produzione rilasciato.  
3.  Controllare le righe, ordinarle in modo da ottenere un percorso di prelievo efficiente e combinarle con altre righe del prospetto, se necessario, in modo da ottimizzare i tempi di esecuzione delle attività da parte degli addetti al magazzino.  
4.  Scegliere l'azione **Crea prelievo**.  
5.  Definire come creare documenti di prelievo warehouse e come ordinare le righe prelievo compilando i campi nella pagina **Crea prelievo**.  
6.  Scegliere il pulsante **OK**. I documenti di prelievo warehouse vengono creati con le righe prelievo per ogni componente richiesto nell'operazione interno.  

Se l'area dell'operazione interna, ad esempio il reparto di produzione, è impostata con una collocazione di default per il posizionamento dei componenti da utilizzare nell'operazione, il codice collocazione viene inserito nelle righe dell'area nel documento di prelievo warehouse per indicare agli addetti warehouse dove posizionare gli articoli. Per ulteriori informazioni, vedere il campo **Cod. coll. art. per produzione** o **Cod. coll. art. per assembl**.

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
