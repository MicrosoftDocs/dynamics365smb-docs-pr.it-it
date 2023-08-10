---
title: Eseguire la consuntivazione dei componenti in base all'output dell'operazione
description: Questo argomento descrive come eseguire la consuntivazione dei componenti in base all'output dell'operazione e altri metodi di consuntivazione coinvolti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="flush-components-according-to-operation-output"></a>Eseguire la consuntivazione dei componenti in base all'output dell'operazione
È possibile definire diverse strategie di consuntivazione, per automatizzare la registrazione del consumo di componenti. 

Questa funzionalità si rivela particolarmente utile per i seguenti motivi:  

- **Valutazione magazzino**

    I movimenti di valorizzazione per output e consumo vengono creati in parallelo con lo stato di avanzamento dell'ordine di produzione. Senza codice legame tra ciclo e distinta base, il valore di magazzino aumenterà man mano che l'output viene registrato e diminuirà in un momento successivo quando il valore di consumo di componenti viene registrato insieme all'ordine di produzione chiuso.  
- **Disponibilità magazzino**

    Con la registrazione graduale del consumo, la disponibilità degli articoli componenti è più aggiornata, il che è importante per mantenere l'equilibrio interno tra offerta e domanda. Senza codice legame tra ciclo e distinta base, altre domande del componente potrebbero ritenere che sia disponibile finché è in sospeso una registrazione di consumo in ritardo.  
- **JIT (just-in-time)**

    Grazie alla possibilità di personalizzare i prodotti alle richieste del cliente, è possibile ridurre lo spreco assicurandosi che le modifiche di sistema e di lavoro si verifichino solo quando è necessario.  

- **Riduci l'immissione di dati**

    Grazie alla possibilità di eseguire la consuntivazione manuale di un'operazione, è possibile automatizzare l'intero processo di registrazione dei consumi e dell'output. Lo svantaggio dell'utilizzo della consuntivazione automatica consiste nel fatto che lo scarto potrebbe non essere registrato o persino individuato correttamente.

## <a name="automatic-consumption-posting-flushing-methods"></a>Metodi registrazione automatica del consumo (consuntivazione)

- Consuntivazione in avanti dell'intero ordine  
- Consuntivazione in avanti in base all'operazione  
- Consuntivazione a ritroso in base all'operazione  
- Consuntivazione a ritroso dell'intero ordine  

### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Reporting automatico - Consuntivazione in avanti dell'intero ordine
Se si esegue la consuntivazione in avanti dell'ordine di produzione all'inizio della commessa, il comportamento dell'applicazione è molto simile a un consumo manuale. La differenza principale consiste nel fatto che il consumo si verifica automaticamente.  

- L'intero contenuto della DB di produzione viene consumato e dedotto dal magazzino nel momento in cui viene aggiornato l'ordine di produzione rilasciato.  
- La quantità dei consumi è la quantità per assemblaggio indicata nella DB di produzione, moltiplicata per il numero di articoli principali creati.  
- Non è necessario registrare alcuna informazione nelle registrazioni dei consumi se tutti gli articoli devono essere sottoposti a consuntivazione.  
- Quando si consumano articoli dal magazzino, non è importante il momento in cui vengono creati i movimenti delle registrazioni di output, in quanto le registrazioni di output non hanno effetto su questa modalità di registrazione dei consumi.  
- Non è possibile impostare alcun codice di legame tra il ciclo e la distinta base.  

La consuntivazione in avanti di un intero ordine è adatta negli ambienti di produzione caratterizzati dai seguenti aspetti:  

-   Numero ridotto di difetti  
-   Numero ridotto di operazioni  
-   Elevato consumo di componenti nelle operazioni iniziali  

### <a name="automatic-reporting---forward-flushing-by-operation"></a>Registrazione automatica - Consuntivazione in avanti in base all'operazione
La consuntivazione in base all'operazione consente di dedurre materiale dal magazzino durante un'operazione specifica nel ciclo dell'articolo principale. Il materiale viene associato al ciclo tramite codici di legame tra ciclo e distinta base, un'attività che corrisponde all'applicazione di codici di legame tra ciclo e distinta base ai componenti nella DB di produzione.  

Il calcolo viene eseguito quando l'operazione associata allo stesso codice di legame tra ciclo e distinta base viene avviata. Iniziato indica che alcune attività vengono inserite nelle registrazioni di output per l'operazione. E l'attività può corrispondere all'immissione di un tempo di setup.  

L'importo della consuntivazione corrisponde alla quantità per assemblaggio indicata nella DB di produzione moltiplicata per il numero di articoli principali creati (quantità prevista).  

Questa tecnica è particolarmente efficace in presenza di molte operazioni e nel caso in cui certi componenti non sono necessari fino alle fasi successive della sequenza di assemblaggio. In un setup JIT (Just-In-Time), infatti, gli articoli potrebbero persino non essere disponibili in magazzino quando viene avviato l'ordine di produzione rilasciato.  

Il materiale può essere consumato durante le operazioni tramite codici di legame tra ciclo e distinta base. Alcuni componenti potrebbero non essere utilizzati fino alle operazioni di assemblaggio finale e non devono essere prelevati dallo stock fino a quel momento.  

### <a name="automatic-reporting---back-flushing-by-operation"></a>Registrazione automatica - Consuntivazione a ritroso in base all'operazione
La consuntivazione a ritroso in base all'operazione consente di registrare il consumo in seguito alla registrazione dell'operazione nelle registrazioni di output.  

Il vantaggio di questo metodo consiste nel fatto che è noto il numero di parti principali completate nell'operazione.  

Il materiale incluso nella DB di produzione è collegato ai record del ciclo tramite codici di legame tra ciclo e distinta base. La consuntivazione a ritroso viene eseguita quando un'operazione associata a un determinato codice di legame tra ciclo e distinta base viene registrata con una quantità finita.  

L'importo della consuntivazione corrisponde alla quantità per assemblaggio indicata nella DB di produzione moltiplicata per il numero di articoli principali registrati come quantità di output nell'operazione. Tale valore può differire dalla quantità prevista.  

### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Reporting automatico - Consuntivazione a ritroso dell'intero ordine
In questo metodo di reporting non vengono considerati i codici di legame tra ciclo e distinta base.  

Non viene prelevato alcun componente fino a quando lo stato dell'ordine di produzione rilasciato non viene modificato in *Completato*. L'importo della consuntivazione corrisponde alla quantità per assemblaggio indicata nella DB di produzione moltiplicata per il numero di articoli principali finiti e inseriti in magazzino.  

La consuntivazione a ritroso dell'intero ordine di produzione richiede lo stesso setup della consuntivazione in avanti: il metodo di reporting deve essere impostato alla fine in ogni scheda articolo per tutti gli articoli all'interno della DB principale di cui eseguire il reporting. Tutti i codici di legame tra ciclo e distinta base devono essere rimossi dalla DB di produzione. 



Ad esempio, se un ordine di produzione per produrre 800 metri richiede 8 chilogrammi di un componente, quando si registrano 200 metri come output, 2 chilogrammi vengono automaticamente registrati come consumo. Puoi eseguirlo combinando il metodo di consuntivazione a ritroso e i codici di legame tra ciclo e distinta base in modo che la quantità di cui è stata effettuata la consuntivazione per operazione sia proporzionale all'effettivo output dell'operazione completata. Per gli articoli impostati con il metodo di consuntivazione a ritroso, il comportamento di default prevede di calcolare e registrare il consumo di componenti quando si modifica lo stato di un ordine di produzione rilasciato in **Completato**. Se inoltre si definiscono i codici legame tra ciclo e distinta base, il calcolo e la registrazione si verificano una volta completata ogni operazione e la quantità effettivamente consumata nell'operazione viene registrata. Per ulteriori informazioni, vedere [Creare cicli](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Per eseguire la consuntivazione dei componenti in base all'output dell'operazione

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Modifica**.  
3.  Nella Scheda dettaglio **Rifornimento**, nel campo **Metodo consuntivazione**, selezionare **Indietro**.  

    > [!NOTE]  
    >  Selezionare **Prelievo+ Indietro** se il componente è utilizzato in un'ubicazione impostata per l'utilizzo di stoccaggi e prelievi guidati.  

4.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cicli**, quindi scegli il collegamento correlato.  
5.  Definire codici di legame tra ciclo e distinta base per ogni operazione che consuma il componente. Per ulteriori informazioni, vedere [Creare cicli](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Non utilizzare lo stesso collegamento di instradamento per operazioni diverse nell'instradamento, poiché porterà alla registrazione del consumo del componente per ciascuna operazione collegata.  
6.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **DB produzione**, quindi seleziona il collegamento correlato.  
7.  Definire codici di legame tra ciclo e distinta base da ogni istanza del componente all'operazione in cui viene consumato.

Il consumo verrà registrato automaticamente al momento della registrazione dell'output. Per ulteriori informazioni, vedere [Registrare l'output e i tempi di lavorazione tramite processo batch](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Metodi di consuntivazione

La tabella seguente descrive le opzioni del metodo di consuntivazione disponibili che è possibile specificare sulle schede **Articolo** e **Unità di stockkeeping**.

|Opzione|Descrizione|
|------------|-------------|  
|Manuale|Richiede di inserire manualmente e registrare il consumo nella registrazione di consumo.|
|Aut. inizio|Inserisce automaticamente il consumo in base alle righe nelle righe del componente dell'ordine di produzione. <br><br>Per impostazione predefinita, la registrazione del consumo di componenti si verifica quando si modifica lo stato di un ordine di produzione in **Rilasciato**. Tuttavia, se si utilizza il campo Cod. **coll. ciclo e dist. base** nelle righe del componente dell'ordine di produzione, le registrazioni si verificano per operazione quando inizia l'operazione. Per ulteriori informazioni, vedi [Procedura: Creare collegamenti ciclo](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Nota**<br>Per la consuntivazione in avanti, la registrazione specifica per l'operazione che è possibile ottenere con i codici di legame tra ciclo e DB si basa sulla quantità prevista definita nella riga del componente. Per informazioni sulla consuntivazione specifica per l'operazione basata sull'output effettivo, vedere la descrizione di **Aut. fine** in questo argomento.<br><br>Se l'ubicazione o le risorse in cui il componente è consumato sono impostate con una struttura di collocazione di default, l'articolo viene consumato dal **Codice coll. produzione aperta**. Per ulteriori informazioni, vedi [Procedura: Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Importante** <br>La consuntivazione in avanti si verifica inoltre quando si fa sceglie **Aggiorna** in un ordine di produzione rilasciato creato da zero. In questi ordini di produzione rilasciati creati direttamente non è possibile modificare le informazioni di collocazione perché le righe del componente ordine produzione vengono generate quando si aggiorna l'ordine, che esegue contemporaneamente la consuntivazione in avanti dei componenti. Di conseguenza, se si desidera modificare le informazioni di collocazione nelle righe del componente dell'ordine di produzione prima della consuntivazione in avanti, tale ordine dovrà essere creato con lo stato *Pianificato* o *Confermato*.|
|Aut. fine|Calcola automaticamente e registra il consumo in base alle righe nelle righe del componente dell'ordine di produzione.<br><br> Per impostazione predefinita, il calcolo e la registrazione del consumo di componenti si verifica quando si modifica lo stato di un ordine di produzione rilasciato in **Completato**. Tuttavia, se si utilizza il campo **Cod. legame ciclo-DB** nelle righe del componente dell'ordine di produzione, il calcolo e la registrazione si verificano una volta completata ogni operazione.<br><br> **Nota** <br>La consuntivazione a ritroso e i codici di legame tra ciclo e distinta base possono combinarsi in modo che la quantità di cui è stata effettuata la consuntivazione per operazione sia proporzionale all'effettivo output di tale operazione. Per ulteriori informazioni, vedi [Procedura: Componenti ordine produzione a livello in base all'output dell'operazione](#to-flush-components-according-to-operation-output).<br><br> Se l'ubicazione o il centro lavoro in cui il componente è consumato sono impostate con una struttura di collocazione di default, l'articolo viene consumato dal **Codice coll. produzione aperta**.|
|Prelievo + Avanti|Uguale al metodo di consuntivazione in avanti, tranne per il fatto che funziona solo per le ubicazioni che utilizzano la configurazione warehouse avanzata o la configurazione warehouse di base con collocazioni obbligatorie.<br><br> Il consumo viene calcolato e registrato dalla collocazione definita nel campo **Cod. coll. art. per produzione** nell'ubicazione o nel centro di lavoro dopo che il componente è stato prelevato dalla warehouse.<br><br> **Nota** <br>Se un componente è impostato con il metodo Prelievo + Consuntivazione in avanti, non potrà disporre di un codice legame ciclo-DB per un'operazione impostata con il metodo di consuntivazione in avanti. Il componente viene quindi consuntivato automaticamente quando comincia l'operazione, che rende impossibile richiedere l'attività di prelievo.|
|Prelievo + Indietro|Uguale al metodo di consuntivazione indietro, tranne per il fatto che funziona solo per le ubicazioni che utilizzano la configurazione warehouse avanzata o la configurazione warehouse di base con collocazioni obbligatorie.<br><br> Il consumo viene calcolato e registrato dalla collocazione definita nel campo **Cod. coll. art. per produzione** nell'ubicazione o nel centro di lavoro dopo che il componente è stato prelevato dalla warehouse.|

## <a name="see-also"></a>Vedere anche

[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
