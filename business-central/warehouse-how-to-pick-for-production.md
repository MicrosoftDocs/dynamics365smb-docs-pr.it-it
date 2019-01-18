---
title: 'Procedura: Prelevare per la produzione in configurazioni di warehouse di base | Documenti Microsoft'
description: "Quando l'ubicazione della warehouse richiede l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, è possibile utilizzare la pagina **Prelievi Magazzino** per organizzare e registrare il prelievo di componenti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 33531bf23b8ae03a38ff176f31de3b7395ace052
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="pick-for-production-or-assembly"></a>Prelevare per la produzione o l'assemblaggio
La modalità di stoccaggio dei componenti di prelievo per gli ordini di produzione o assemblaggio dipende dall'impostazione della warehouse come ubicazione. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

Nelle configurazioni di warehouse di base, in cui l'ubicazione richiede l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, è possibile utilizzare la pagina **Prelievi magazzino** per organizzare e registrare il prelievo di componenti.  

Nelle configurazioni di wareahouse di base è necessario effettuare prelievi per ordini di assemblaggio tramite la pagina **Movimento di magazzino**. Per altre informazioni, vedere la sezione "Gestione di articoli da assemblare su ordine in prelievi magazzino" in [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md).  

Nelle configurazioni di warehouse avanzate in cui le ubicazioni richiedono sia prelievi che spedizioni, è possibile utilizzare la pagina **Prelievo warehouse** per immettere componenti negli ordini di produzione o di assemblaggio.

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

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Per prelevare componenti nelle configurazioni di warehouse avanzate
Nelle configurazioni di warehouse avanzate in cui l'ubicazione è impostata in modo da utilizzare sia il prelievo che la spedizione, è possibile prelevare componenti per le attività di assemblaggio e produzione tramite la pagina **Prelievo warehouse**. Per ulteriori informazioni, vedere [Prelevare articoli con prelievi warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md).

In alternativa, è possibile utilizzare la pagina **Prospetto movimentazioni** per spostare gli articoli tra le collocazioni ad hoc, ovvero senza riferimento a un documento di origine. Per ulteriori informazioni, vedere [Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Non è possibile creare un documento di prelievo warehouse da zero perché un'attività di prelievo fa sempre parte di un flusso di lavoro, in uno scenario di tipo push o pull.  

È possibile creare il documento di prelievo warehouse in modalità push selezionando l'azione **Crea prelievo whse.** nel documento di origine, ad esempio un ordine di assemblaggio rilasciato o una spedizione warehouse. Per ulteriori informazioni, vedere [Prelevare articoli con prelievi warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

In alternativa, è possibile creare il documento di prelievo warehouse in modalità pull mediante la pagina **Prospetto prelievi** per verificare le richieste di prelievo, sia per la spedizione che per le operazioni interne, quindi creare i documenti di prelievo warehouse necessari.  

La procedura seguente illustra uno scenario di tipo pull in cui si prelevano componenti per un ordine di produzione rilasciato tramite la pagina **Prospetto prelievi**. La procedura si applica anche agli ordini di assemblaggio.  

Per creare richieste di prelievo, sia per scenari pull e push, i documenti di origine in questione devono essere rilasciati. Rilasciare i documenti di origine per le operazioni interne nei seguenti modi.  

 |Documento origine|Metodo di rilascio|  
 |---------------------|--------------------|  
 |Ordine di produzione|Modificare il tipo di ordine in Ordine produzione rilasciato.|  
 |Ordine di assemblaggio|Modificare lo stato in Rilasciato.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Per prelevare componenti mediante i prospetti prelievi  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto prelievi** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Prendi documenti warehouse**, quindi selezionare le righe componenti dall'ordine di produzione rilasciato.  
3.  Controllare le righe, ordinarle in modo da ottenere un percorso di prelievo efficiente e combinarle con altre righe del prospetto, se necessario, in modo da ottimizzare i tempi di esecuzione delle attività da parte degli addetti al magazzino.  
4.  Scegliere l'azione **Crea prelievo**.  
5.  Definire come creare documenti di prelievo warehouse e come ordinare le righe prelievo compilando i campi nella pagina **Crea prelievo**.  
6.  Scegliere il pulsante **OK**.

I documenti di prelievo warehouse vengono adesso creati con le righe prelievo per ogni componente richiesto nell'operazione interno.

Se l'area dell'operazione interna, ad esempio il reparto di produzione, è impostata con una collocazione di default per il posizionamento dei componenti da utilizzare nell'operazione, il codice collocazione viene inserito nelle righe dell'area nel documento di prelievo warehouse per indicare agli addetti warehouse dove posizionare gli articoli. Per ulteriori informazioni, vedere [Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

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

