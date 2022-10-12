---
title: Prelevare per produzione, assemblaggio o commesse in warehouse di base
description: Quando l'ubicazione della warehouse richiede l'elaborazione dei prelievi ma non delle spedizioni, usa la pagina Prelievi magazzino per registrare il prelievo di componenti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617878"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Prelevare per produzione, assemblaggio o commesse in configurazioni di warehouse di base

La modalità di stoccaggio dei componenti di prelievo per gli ordini di produzione o assemblaggio dipende dall'impostazione della warehouse come ubicazione. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Prelevare per la produzione in configurazioni della warehouse di base

Se una ubicazione richiede l'elaborazione del prelievo ma non l'elaborazione della spedizione, puoi utilizzare la pagina **Prelievi magazzino**. La pagina **Prelievi magazzino** ti consente di organizzare e registrare il prelievo degli articoli per cui il metodo di consuntivazione è impostato su **Manuale**. Quando si registra un prelievo da magazzino, viene registrato il consumo dei componenti prelevati. Puoi anche usare **Movimento di magazzino** con riferimento a un documento di origine per assegnare i componenti con il metodo di consuntivazione impostato su **Manuale**, **Prelievo + Avanti**, **Prelievo + Indietro** per gli ordini di produzione.

Quando la produzione è integrata con i processi della warehouse, tramite collocazioni o stoccaggi e prelievi diretti, i componenti vengono consumati dalla collocazione nella riga dell'ordine di produzione. Tutti i componenti obbligatori devono essere disponibili in tale collocazione. In caso contrario, la registrazione del consumo manuale o automatico viene interrotta per tale componente.

> [!NOTE]  
> Tra i prelievi da magazzino, i movimenti di magazzino e i prelievi warehouse sono presenti le importanti differenze riportate di seguito:  
>
> - Quando si registra un prelievo da magazzino per un'operazione interna, come la produzione, il consumo dei componenti prelevati viene registrato contemporaneamente. Quando si inserisce un movimento di magazzino o un prelievo warehouse per un'operazione interna, si registra solo la movimentazione fisica dei componenti necessari a una collocazione nell'area di operazione senza registrare il consumo.  
> - Quando si utilizzano prelievi da magazzino, il campo **Cod. collocazione** nella riga di componente di un ordine di produzione definisce la collocazione *prendere* da dove vengono diminuiti i componenti quando viene registrato il consumo. Quando si utilizzano i movimenti di magazzino o un prelievo warehouse, il campo **Cod. collocazione** nelle righe di componenti dell'ordine di produzione definisce la collocazione *mettere* nell'area di operazione in cui l'addetto alla warehouse deve posizionare i componenti.  

Per prelevare o spostare componenti per i documenti di origine, una richiesta warehouse in uscita deve notificare all'area warehouse la necessità del componente. La richiesta warehouse in uscita viene creata quando esegui le seguenti azioni:

- Modifica dello stato di un ordine di produzione in Rilasciato.
- Creazione di un ordine di produzione rilasciato.  

I metodi di consuntivazione influiscono anche sul flusso dei componenti in produzione. Per ulteriori informazioni vedere [Componenti ordine produzione a livello in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md). **Movimento di magazzino** con riferimenti al documento di origine e **Prelievo warehouse** non può essere utilizzato per selezionare componenti con metodi di consuntivazione *Avanti* e *Indietro*. **Prelievi magazzino** non può essere utilizzato per selezionare componenti con qualsiasi metodo di consuntivazione diverso da *Manuale*. Per gestire i componenti rimanenti, usa **Movimento di magazzino** senza riferimento a un documento di origine. Per ulteriori informazioni, vedere ad esempio [Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Nelle configurazioni di magazzino avanzate in cui le ubicazioni richiedono sia prelievi che spedizioni, è necessario utilizzare la pagina **Prelievo warehouse** per portare i componenti con il metodo di consuntivazione impostato su *Manuale*, *Prelievo + Avanti*, *Prelievo + Indietro* agli ordini di produzione. Per ulteriori informazioni, vedere [Prelevare per produzione o assemblaggio in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Per prelevare i componenti per la produzione e le commesse in configurazioni di base della warehouse

Nelle configurazioni di warehouse di base in cui l'ubicazione è impostata in modo da utilizzare solo il prelievo, è possibile prelevare componenti per le attività di produzione e le righe di pianificazione commesse tramite la pagina **Prelievo magazzino**. Per ulteriori informazioni, vedere [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> È stata aggiunta la possibilità di selezionare i componenti per le righe di pianificazione commesse in [!INCLUDE[d365fin](includes/d365fin_md.md)] nel secondo ciclo di rilascio del 2022. Per iniziare a utilizzare la funzionalità, un amministratore deve attivare **Aggiornamento funzionalità: abilitazione del prelievo magazzino e warehouse da commesse** nella pagina **Gestione funzionalità**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] utilizza il valore del campo **Quantità rimanente** nella riga di pianificazione commessa quando crea prelievi magazzino. Per utilizzare i prelievi di magazzino per le commesse, è necessario attivare l'interruttore **Applica collegamento utilizzo** nella pagina **scheda commessa** per la commessa. Ciò ti consente di monitorare l'utilizzo rispetto al tuo piano. Se non si attiva l'interruttore, la quantità rimanente rimarrà a **0** e il prelievo magazzino non verrà creato. Per ulteriori informazioni, vedi [Per impostare la tracciabilità dell'utilizzo in una commessa](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prelievi magazzino**, quindi scegli il collegamento correlato.  
2. Per accedere ai componenti dell'ordine di produzione, scegliere l'azione **Prendi documenti origine** e selezionare l'ordine di produzione rilasciato.  
3. Esegui il prelievo del componente e registra le informazioni di prelievo effettive nel campo **Qtà da gestire**.  
4. Quando le righe sono pronte per la registrazione, scegliere l'azione **Registra**. Verranno creati i movimenti di warehouse necessari e verrà registrato il consumo degli articoli.  

È inoltre possibile creare **Prelievi magazzino** direttamente dall'ordine produzione rilasciato. Scegli l'azione **Crea stoccaggio/prelievo/movimento magazzino**, seleziona la casella di controllo **Crea prelievo mag.**, quindi scegli il pulsante **OK**.

In alternativa, usa **Movimento di magazzino** con riferimento al documento di origine per spostare gli articoli tra i contenitori. Sarà necessario registrare il consumo separatamente. Per ulteriori informazioni, vedi [Registrare il consumo produzione tramite processo batch](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Prelievo per l'assemblaggio in configurazioni della warehouse di base

Utilizza le seguenti pagine per prelevare gli ordini di assemblaggio:

- La pagina **Movimento di magazzino**.
- Se l'ubicazione richiede prelievi ma non spedizioni, utilizza la pagina **Prelievi magazzino** per prelevare, assemblare e spedire ordini di vendita in cui gli articoli devono essere assemblati prima che possano essere spediti. Per ulteriori informazioni, vedere la sezione [Gestione di un articolo da assemblare su ordine con prelievi magazzino](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Nelle configurazioni di warehouse avanzate in cui le ubicazioni richiedono sia prelievi che spedizioni, è necessario utilizzare la pagina **Prelievo warehouse** per immettere componenti negli ordini di assemblaggio. Per ulteriori informazioni, vedere [Prelevare per produzione o assemblaggio in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Gestione di articoli da assemblare su ordine con prelievi magazzino

La pagina **Prelievi magazzino** è inoltre utilizzata per prelevare e spedire vendite in cui gli articoli devono essere assemblati prima che possano essere spediti. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).

Gli articoli da assemblare su ordine da spedire non sono considerati presenti in una collocazione finché non vengono assemblati e registrati come output in una collocazione nell'area di assemblaggio. Pertanto, il prelievo di questi articoli per la spedizione segue un flusso speciale. Da una collocazione gli addetti alla warehouse trasferiscono gli articoli di assemblaggio al dock di spedizione, quindi registrano il prelievo magazzino. Tramite il prelievo magazzino registrato vengono quindi registrati l'output di assemblaggio, il consumo di componenti e la spedizione di vendita.

È possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo che venga creato automaticamente un movimento di magazzino quando viene creato il prelievo magazzino per l'articolo di assemblaggio. Per creare movimenti automaticamente, scegli il campo **Crea movimenti automaticamente** nella pagina **Setup assemblaggio**. Per ulteriori informazioni, vedere [Spostare componenti in un'area di operazione nella gestione warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

[!INCLUDE[prod_short](includes/prod_short.md)] crea le righe di prelievo magazzino per articoli di vendita in modi diversi a seconda se nessuna, qualche o tutte le quantità della riga di vendita vengano assemblate su ordine.

- Nelle vendite in cui utilizzi i prelievi magazzino per registrare la spedizione magazzino, [!INCLUDE[prod_short](includes/prod_short.md)] crea una riga di prelievo magazzino per ciascuna riga dell'ordine di vendita. Se l'articolo viene posizionato in collocazioni diverse, verrà creata più di una riga. Le righe di prelievo si basano sulla quantità nel campo **Qtà da spedire**.
- Nelle vendite in cui la quantità completa nella riga ordine di vendita è assemblata su ordine, viene creata una riga prelievo magazzino per la quantità. Il valore nel campo Quantità da assemblare è uguale al valore nel campo **Qtà. da spedire**. Il campo **Assemblaggio su ordine** viene selezionato nella riga.

Se un flusso di output assemblaggio è impostato per l'ubicazione, il valore nei campi **Cod. coll. sp. ass. su ordine** o **Cod. coll. art. da assembl.**, in tale ordine, viene immesso nel campo **Codice collocazione** sulla riga di prelievo magazzino.

Se nessun codice collocazione è specificato sulla riga di ordine di vendita e non è impostato alcun flusso di output dell'assemblaggio per l'ubicazione, il campo **Codice collocazione** sulla riga di prelievo magazzino è vuoto. L'addetto alla warehouse deve aprire la pagina **Contenuto collocazioni** e selezionare la collocazione in cui sono assemblati gli articoli di assemblaggio.

Quando una parte della quantità deve essere prima assemblata e un'altra deve essere prelevata dal magazzino, [!INCLUDE[prod_short](includes/prod_short.md)] crea almeno due righe di prelievo magazzino. Una riga di prelievo è relativa alla quantità per l'assemblaggio su ordine. L'altra riga di prelievo dipende da quali collocazioni possono soddisfare la quantità restante dal magazzino. I codici di collocazione nelle due righe vengono compilati in modi diversi come descritto rispettivamente per i due tipi diversi di vendita. Per altre informazioni, vedere la sezione "Scenari di combinazione" in [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).

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
