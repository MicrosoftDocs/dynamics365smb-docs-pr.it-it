---
title: Come prelevare articoli con prelievi magazzino
description: Se un'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non la spedizione, utilizzare i documenti di prelievo da magazzino per registrare e contabilizzare le informazioni riguardanti il prelievo e la spedizione per i documenti di origine.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 79b373ec522d2cd8f99c6b0a98db0df7f9d1793f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533699"
---
# <a name="pick-items-with-inventory-picks"></a>Prelevare articoli con prelievi magazzino

Quando un'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, utilizzare la pagina **Prelievi magazzino** per registrare e contabilizzare le informazioni riguardanti il prelievo e la spedizione per i documenti di origine. Il documento di origine in uscita può essere un ordine di vendita, un ordine di reso da acquisto, un ordine di trasferimento in uscita o un ordine di produzione i cui componenti sono pronti per il prelievo.

> [!NOTE]  
> I componenti per gli ordini di assemblaggio non possono essere prelevati o registrati con i prelievi da magazzino. Pertanto, utilizzare la pagina **Movimento di magazzino**. Per ulteriori informazioni, vedere [Spostare componenti in un'area di operazione nella gestione warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).
>
> Durante il prelievo e la spedizione di quantità righe di vendita assemblate sull'ordine, è necessario seguire determinate regole per la creazione di righe di prelievo magazzino. Per ulteriori informazioni, vedere la sezione [Gestione di articoli da assemblare su ordine in prelievi magazzino](#handling-assemble-to-order-items-with-inventory-picks).  

È possibile creare un prelievo da magazzino in tre modi:  

- Creare il prelievo in due passaggi innanzitutto richiedendo un prelievo magazzino emettendo il documento di origine. Ciò segnala alla warehouse che il documento di origine è pronto per il prelievo. Il prelievo in magazzino può quindi essere creato utilizzando la pagina **Prelievo in magazzino** in base al documento di origine.  
- Creare il prelievo da magazzino direttamente dal documento di origine.  
- Creare prelievi da magazzino per più documenti di origine contemporaneamente utilizzando l'apposito processo batch.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Per richiedere un prelievo magazzino emettendo il documento di origine

Per gli ordini di vendita, gli ordini di reso acquisto e gli ordini di trasferimento in uscita, creare la richiesta warehouse emettendo l'ordine. Di seguito viene descritto come eseguire l'operazione da un ordine di vendita.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare l'ordine di vendita che si intende rilasciare, quindi scegliere l'azione **Rilascio**.

Per gli ordini di produzione, creare automaticamente la richiesta warehouse per il prelievo di componenti, chiamata *consuntivazione*, quando lo stato dell'ordine di produzione viene modificato in **Rilasciato** oppure quando viene creato l'ordine di produzione rilasciato. Per ulteriori informazioni, vedere [Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md).

Dopo aver creato la richiesta warehouse, un dipendente della warehouse addetto al prelievo di articoli può vedere che il documento di origine è pronto per il prelievo e potrà creare un nuovo documento di prelievo basato sulla richiesta warehouse.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Per creare un prelievo da magazzino basato sul documento di origine

Ora che la richiesta è stata creata, l'impiegato della warehouse può creare un nuovo prelievo da magazzino basato sul documento di origine rilasciato.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prelievi magazzino**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
    Assicurarsi che il campo **Nr.** della Scheda dettaglio **Generale** sia compilato.
3. Nel campo **Documento origine** selezionare il tipo di documento di origine per cui si esegue il prelievo.  
4. Nel campo **Nr. origine** selezionare il documento di origine.  
5. In alternativa, scegliere l'azione **Prendi documento origine** per selezionare il documento da una lista di documenti di origine in uscita pronti per il prelievo presso l'ubicazione.  
6. Selezionare il pulsante **OK** per compilare le righe di prelievo in base al documento di origine selezionato.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Per creare un prelievo magazzino dal documento di origine

1. Nel documento di origine, che può essere un ordine di vendita, un ordine di reso da acquisto, un ordine di trasferimento in uscita o un ordine di produzione, scegliere l'azione **Crea stoccaggio / prelievo mag.**.
2. Selezionare la casella di controllo **Crea prelievo mag.**.  
3. Scegliere il pulsante **OK**. Verrà creato un nuovo prelievo magazzino.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Per creare più prelievi magazzino utilizzando un processo batch

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Crea stoccaggio/Prelievo mag.**, quindi seleziona il collegamento correlato.  
2. Nella Scheda dettaglio **Richiesta warehouse**, utilizzare i campi **Nr. origine** e **Documento origine** per filtrare determinati tipi di documenti oppure intervalli di numeri di documenti. Ad esempio, è possibile creare prelievi solo per gli ordini di vendita.  
3. Nella Scheda dettaglio **Opzioni**, selezionare la casella di controllo **Crea prelievo mag.**.
4. Scegliere il pulsante **OK**. Verranno creati i prelievi magazzino specificati.

> [!NOTE]  
> In caso di prelievo e spedizione di quantità righe di vendita assemblate su ordine, è opportuno seguire determinate regole per la creazione di righe di prelievo magazzino. Per ulteriori informazioni, vedere la sezione [Gestione di articoli da assemblare su ordine in prelievi magazzino](#handling-assemble-to-order-items-with-inventory-picks).  
>
> Nelle configurazioni di warehouse di base, gli articoli assemblati per gli ordini di vendita vengono prelevati dall'ordine di vendita collegato, come descritto in questo argomento. Per ulteriori informazioni, vedere la sezione [Gestione di articoli da assemblare su ordine in prelievi magazzino](#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="to-record-the-inventory-picks"></a>Per registrare i prelievi magazzino

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievo magazzino**, quindi scegli il collegamento correlato.  
2. Nel campo **Codice collocazione** sulle righe di prelievo, la collocazione da cui gli articoli devono essere prelevati suggerisce la collocazione di default dell'articolo. È possibile modificare la collocazione in questa pagina, se necessario.  
3. Eseguire il prelievo e immettere le informazioni riguardanti la quantità effettiva stoccata nel campo **Qtà da gestire**.

    Se è necessario prelevare gli articoli relativi a una riga da più collocazioni, ad esempio perché non sono disponibili nella collocazione designata, utilizzare la funzione **Dividi riga** della Scheda dettaglio **Righe**. Per ulteriori informazioni sulla divisione delle righe, vedere [Suddividere le righe attività warehouse](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Dopo avere eseguito il prelievo, scegliere l'azione **Registra**.  

Il processo di registrazione contabilizzerà la spedizione delle righe del documento di origine prelevate oppure, nel caso di ordini di produzione, il consumo. Se l'ubicazione prevede l'utilizzo di collocazioni, verranno inoltre creati movimenti warehouse per la registrazione delle modifiche delle quantità nelle collocazioni.  

## <a name="to-delete-inventory-pick-lines"></a>Per eliminare le righe prelievi magazzino

Se gli articoli nel prelievo magazzino non sono disponibili, è generalmente possibile eliminare tali righe di prelievo magazzino dopo averle registrate ed eliminare quindi il documento di prelievo magazzino. Il documento di origine, ad esempio un ordine di vendita o un ordine di produzione, conterrà gli articoli restanti da prelevare, che possono essere ottenuti in un momento successivo mediante un nuovo prelievo magazzino quando gli articoli diventano disponibili.  

> [!WARNING]  
> Questo processo non è possibile se i numeri di serie/lotto sono specificati nel documento di origine. Ad esempio, se una riga ordine di vendita contiene un numero di lotto o di serie, tale specifica di tracciabilità articolo verrà eliminata se una riga di prelievo magazzino per il numero di lotto o di serie viene eliminata.  
>
> Se le righe di prelievo magazzino hanno numeri di serie/lotto che non sono disponibili, non eliminare le righe in questione. In alternativa, è necessario modificare il campo **Qtà da gestire** in zero, registrare i prelievi effettivi, quindi eliminare il documento di prelievo magazzino. Ciò dà la certezza che le righe di prelievo magazzino per tali numeri di serie/lotto possono essere ricreate successivamente dall'ordine vendita.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Gestione di articoli da assemblare su ordine con prelievi magazzino

La pagina **Prelievi magazzino** è inoltre utilizzata per prelevare e spedire vendite in cui gli articoli devono essere assemblati prima che possano essere spediti. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).

Gli articoli da spedire non sono presenti fisicamente in una collocazione finché non vengono assemblati e registrati come output in una collocazione nell'area di assemblaggio. Ciò significa che il prelievo di articoli da assemblare su ordine per la spedizione seguono un flusso speciale. Da una collocazione gli addetti alla warehouse trasferiscono gli articoli di assemblaggio al dock di spedizione, quindi registrano il prelievo magazzino. Tramite il prelievo magazzino registrato vengono quindi registrati l'output di assemblaggio, il consumo di componenti e la spedizione di vendita.

È possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo che venga creato automaticamente un movimento di magazzino quando viene creato il prelievo magazzino per l'articolo di assemblaggio. Per eseguire questa operazione, è necessario selezionare il campo **Crea movimenti automaticamente** nella pagina **Setup assemblaggio**. Per ulteriori informazioni, vedere [Spostare componenti in un'area di operazione nella gestione warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Le righe di prelievo magazzino per articoli di vendita vengono create in modi diversi a seconda se nessuna, qualche o tutte le quantità della riga di vendita vengano assemblate su ordine.

Nelle vendite normali in cui si utilizzano prelievi magazzino per registrare la spedizione delle quantità di magazzino, per ogni riga di ordine di vendita vengono create una o più righe di prelievo magazzino se l'articolo è posizionato in collocazioni diverse. La riga di prelievo è basata sulla quantità nel campo **Qtà da spedire**.

Nelle vendite di assemblaggio su ordine in cui la quantità completa nella riga ordine di vendita è assemblata su ordine, viene creata una riga prelievo magazzino per la quantità. Ciò significa che il valore nel campo Quantità da assemblare è simile al valore nel campo **Qtà. da spedire**. Il campo **Assemblaggio su ordine** viene selezionato nella riga.

Se un flusso di output assemblaggio è impostato per l'ubicazione, il valore nel campo **Cod. coll. sp. ass. su ordine** o il valore nel campo **Cod. coll. art. da assembl.**, in tale ordine, viene immesso nel campo **Codice collocazione** sulla riga di prelievo magazzino.

Se nessun codice collocazione è specificato sulla riga di ordine di vendita e non è impostato alcun flusso di output dell'assemblaggio per l'ubicazione, il campo **Codice collocazione** sulla riga di prelievo magazzino è vuoto. L'addetto alla warehouse deve aprire la pagina **Contenuto collocazioni** e selezionare la collocazione in cui sono assemblati gli articoli di assemblaggio.

Negli scenari di combinazione, in cui una parte della quantità deve essere assemblata e un'altra deve essere prelevata dal magazzino, viene creato un minimo di due righe di prelievo magazzino. Una riga di prelievo è relativa alla quantità per l'assemblaggio su ordine. L'altra riga di prelievo dipende da quali collocazioni possono soddisfare la quantità restante dal magazzino. I codici di collocazione nelle due righe vengono compilati in modi diversi come descritto rispettivamente per i due tipi diversi di vendita. Per altre informazioni, vedere la sezione "Scenari di combinazione" in [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Vedere anche

[Warehouse Management](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Procedura dettagliata: prelievo e spedizione nelle configurazioni di warehouse di base](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
