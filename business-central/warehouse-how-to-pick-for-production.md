---
title: 'Procedura: Prelevare per la produzione in configurazioni di warehouse di base | Documenti Microsoft'
description: Quando l'ubicazione della warehouse richiede l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, è possibile utilizzare la pagina **Prelievi Magazzino** per organizzare e registrare il prelievo di componenti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e58299e7edecc35c7757ebc91d1e444df299ee13
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310302"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Prelevare per produzione o assemblaggio in configurazioni di warehouse di base
La modalità di stoccaggio dei componenti di prelievo per gli ordini di produzione o assemblaggio dipende dall'impostazione della warehouse come ubicazione. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

Nelle configurazioni di warehouse di base, in cui l'ubicazione richiede l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, è possibile utilizzare la pagina **Prelievi magazzino** per organizzare e registrare il prelievo di componenti.  

Nelle configurazioni di wareahouse di base è necessario effettuare prelievi per ordini di assemblaggio tramite la pagina **Movimento di magazzino**. Per ulteriori informazioni, vedere la sezione [Gestione di un articolo da assemblare su ordine con prelievi magazzino](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Nelle configurazioni di warehouse avanzate in cui le ubicazioni richiedono sia prelievi che spedizioni, è possibile utilizzare la pagina **Prelievo warehouse** per immettere componenti negli ordini di produzione o di assemblaggio. Per ulteriori informazioni, vedere [Prelevare per produzione o assemblaggio in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

> [!NOTE]  
>  Tra i prelievi da magazzino e i movimenti di magazzino sono presenti le importanti differenze riportate di seguito:  
>   
>  -   Quando si registra un prelievo da magazzino per un'operazione interna, come la produzione, il consumo dei componenti prelevati viene registrato contemporaneamente. Quando si inserisce un movimento di magazzino per un'operazione interna, si registra solo la movimentazione fisica dei componenti necessari a una collocazione nell'area di operazione senza registrare il consumo.  
> -   Quando si utilizzano prelievi da magazzino, il campo **Cod. collocazione** nella riga di componente di un ordine di produzione definisce la collocazione *prendere* da dove vengono diminuiti i componenti quando viene registrato il consumo. Quando si utilizzano i movimenti di magazzino, il campo **Cod. collocazione** nelle righe di componenti dell'ordine di produzione definisce la collocazione *mettere* nell'area di operazione in cui l'addetto alla warehouse deve posizionare i componenti.  

Una condizione preliminare di sistema per il prelievo o la movimentazione di componenti per i documenti di origine è l'esistenza di una richiesta warehouse in uscita per comunicare i componenti necessari all'area di warehouse. La richiesta warehouse in uscita viene creata ogni volta che lo stato dell'ordine di produzione viene modificato e impostato su Rilasciato o quando viene creato un ordine di produzione rilasciato.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Per prelevare componenti nelle configurazioni di warehouse di base
Nelle configurazioni di warehouse di base in cui l'ubicazione è impostata in modo da utilizzare solo il prelievo, è possibile prelevare componenti per le attività di produzione tramite la pagina **Prelievo magazzino**. Per ulteriori informazioni, vedere [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prelievi magazzino** e quindi scegliere il collegamento correlato.  
2.  Per accedere ai componenti dell'ordine di produzione, scegliere l'azione **Prendi documenti origine** e selezionare l'ordine di produzione rilasciato.  
3.  Eseguire il prelievo e registrare le informazioni di prelievo effettive nel campo **Qtà prelevata**.  
4.  Quando le righe sono pronte per la registrazione, scegliere l'azione **Registra**. Verranno creati i movimenti di warehouse necessari e verrà registrato il consumo degli articoli.  

È inoltre possibile creare **Prelievi magazzino** direttamente dall'ordine produzione rilasciato. Scegliere l'azione **Crea stoccaggio / prelievo mag.**, selezionare la casella di controllo **Crea prelievo mag.**, quindi scegliere il pulsante **OK**.

In alternativa, è possibile utilizzare la pagina **Movimento di magazzino** per spostare gli articoli tra le collocazioni ad hoc, ovvero senza riferimento a un documento di origine.
Per ulteriori informazioni, vedere ad esempio [Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Gestione di articoli da assemblare su ordine con prelievi magazzino
La pagina **Prelievi magazzino** è inoltre utilizzata per prelevare e spedire vendite in cui gli articoli devono essere assemblati prima che possano essere spediti. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).

Gli articoli da spedire non sono presenti fisicamente in una collocazione finché non vengono assemblati e registrati come output in una collocazione nell'area di assemblaggio. Ciò significa che il prelievo di articoli da assemblare su ordine per la spedizione seguono un flusso speciale. Da una collocazione gli addetti alla warehouse trasferiscono gli articoli di assemblaggio al dock di spedizione, quindi registrano il prelievo magazzino. Tramite il prelievo magazzino registrato vengono quindi registrati l'output di assemblaggio, il consumo di componenti e la spedizione di vendita.

È possibile impostare [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo che venga creato automaticamente un movimento di magazzino quando viene creato il prelievo magazzino per l'articolo di assemblaggio. Per eseguire questa operazione, è necessario selezionare il campo **Crea movimenti automaticamente** nella pagina **Setup assemblaggio**. Per ulteriori informazioni, vedere [Spostare componenti in un'area di operazione nella gestione warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Le righe di prelievo magazzino per articoli di vendita vengono create in modi diversi a seconda se nessuna, qualche o tutte le quantità della riga di vendita vengano assemblate su ordine.

Nelle vendite normali in cui si utilizzano prelievi magazzino per registrare la spedizione delle quantità di magazzino, per ogni riga di ordine di vendita vengono create una o più righe di prelievo magazzino se l'articolo è posizionato in collocazioni diverse. La riga di prelievo è basata sulla quantità nel campo **Qtà da spedire**.

Nelle vendite di assemblaggio su ordine in cui la quantità completa nella riga ordine di vendita è assemblata su ordine, viene creata una riga prelievo magazzino per la quantità. Ciò significa che il valore nel campo Quantità da assemblare è simile al valore nel campo **Qtà. da spedire**. Il campo **Assemblaggio su ordine** viene selezionato nella riga.

Se un flusso di output assemblaggio è impostato per l'ubicazione, il valore nel campo **Cod. coll. sp. ass. su ordine** o il valore nel campo **Cod. coll. art. da assembl.**, in tale ordine, viene immesso nel campo **Codice collocazione** sulla riga di prelievo magazzino.

Se nessun codice collocazione è specificato sulla riga di ordine di vendita e non è impostato alcun flusso di output dell'assemblaggio per l'ubicazione, il campo **Codice collocazione** sulla riga di prelievo magazzino è vuoto. L'addetto alla warehouse deve aprire la pagina **Contenuto collocazioni** e selezionare la collocazione in cui sono assemblati gli articoli di assemblaggio.

Negli scenari di combinazione, in cui una parte della quantità deve essere assemblata e un'altra deve essere prelevata dal magazzino, viene creato un minimo di due righe di prelievo magazzino. Una riga di prelievo è relativa alla quantità per l'assemblaggio su ordine. L'altra riga di prelievo dipende da quali collocazioni possono soddisfare la quantità restante dal magazzino. I codici di collocazione nelle due righe vengono compilati in modi diversi come descritto rispettivamente per i due tipi diversi di vendita. Per altre informazioni, vedere la sezione "Scenari di combinazione" in [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Rifornimento della collocazione di consumo
Questo diagramma di flusso illustra in che modo il campo **Cod. collocazione** nelle righe del componente dell'ordine di produzione viene compilato in base al setup dell'ubicazione.

![Diagramma di flusso collocazione](media/binflow.png "BinFlow")

## <a name="see-also"></a>Vedi anche
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
