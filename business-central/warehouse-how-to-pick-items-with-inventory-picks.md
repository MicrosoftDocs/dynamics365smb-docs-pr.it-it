---
title: Come prelevare articoli con prelievi magazzino
description: Informazioni su come utilizzare i prelievi di magazzino per registrare e contabilizzare le informazioni di prelievo e spedizione per i documenti di origine.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# Prelevare articoli con prelievi magazzino

In [!INCLUDE[prod_short](includes/prod_short.md)], il prelievo e la spedizione degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in uscita|Richiesto prelievo|Richiesta spedizione|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registra il prelievo e la spedizione dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registra il prelievo e la spedizione da un documento di prelievo magazzino|Attivato||Di base: ordine per ordine.|  
|C|Registra il prelievo e la spedizione da un documento di spedizione warehouse||Attivato|Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni vedi [Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md).

Questo articolo fa riferimento al metodo B nella tabella.

Quando un'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, utilizza la pagina **Prelievi magazzino** per registrare e contabilizzare le informazioni riguardanti il prelievo e la spedizione per i documenti di origine. I documenti di origine in uscita includono ordini di vendita, ordini di reso da acquisto e trasferimenti in uscita.

> [!NOTE]
> Anche gli ordini di produzione e di assemblaggio con componenti rappresentano documenti di origine in uscita. Per ulteriori informazioni sulla gestione degli ordini di produzione e assemblaggio per i processi interni, vedi [Dettagli di progettazione: Flussi warehouse interni](design-details-internal-warehouse-flows.md).
>
> Sebbene gli ordini di assistenza siano anche documenti di origine in uscita, non supportano il livello di complessità di base ordine per ordine.
>
> Durante il prelievo e la spedizione di quantità righe di vendita assemblate sull'ordine, è necessario seguire determinate regole quando crei le righe di prelievo magazzino. Ulteriori informazioni in [Gestione di articoli da assemblare su ordine con prelievi magazzino](#handling-assemble-to-order-items-with-inventory-picks).  

È possibile creare un prelievo da magazzino in tre modi:

* Crea il prelievo da magazzino direttamente dal documento di origine.  
* Crea prelievi da magazzino per più documenti di origine contemporaneamente utilizzando un processo batch.
* Richiedi il prelievo in due passaggi rilasciando prima un documento di origine, per segnalare alla warehouse che il documento di origine è pronto per il prelievo.

Il prelievo in magazzino può quindi essere creato dalla pagina **Prelievo in magazzino** in base al documento di origine.  

## Per creare un prelievo magazzino dal documento di origine

1. Nel documento di origine, che può essere un ordine di vendita, un ordine di reso da acquisto o un ordine di trasferimento in uscita, scegli l'azione **Crea stoccaggio / prelievo mag.**.
2. Seleziona la casella di controllo **Crea prelievo mag.**.  
3. Scegliere il pulsante **OK**. Verrà creato un nuovo prelievo magazzino.

## Per creare più prelievi magazzino utilizzando un processo batch

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Crea stoccaggio/prelievo/movimento magazzino**, quindi seleziona il collegamento correlato.  
2. Nella Scheda dettaglio **Richiesta warehouse**, utilizzare i campi **Nr. origine** e **Documento origine** per filtrare determinati tipi di documenti oppure intervalli di numeri di documenti. Ad esempio, è possibile creare prelievi solo per gli ordini di vendita.  
3. Nella Scheda dettaglio **Opzioni**, seleziona la casella di controllo **Crea prelievo mag.**.
4. Scegli il pulsante **OK**.

## Per creare il prelievo in due passaggi

### Per richiedere un prelievo magazzino emettendo il documento di origine

Per gli ordini di vendita, gli ordini di reso acquisto e gli ordini di trasferimento in uscita, creare la richiesta warehouse emettendo l'ordine. Il rilascio dell'ordine rende gli articoli disponibili per il prelievo.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare l'ordine di vendita che si intende rilasciare, quindi scegliere l'azione **Rilascio**.

### Per creare un prelievo da magazzino basato sul documento di origine

Dopo aver rilasciato un ordine, l'addetto alla warehouse può creare un prelievo da magazzino.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prelievi magazzino**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  
3. Nel campo **Documento origine** seleziona il tipo di documento per cui esegui il prelievo.  
4. Nel campo **Nr. origine** selezionare il documento di origine.  
5. In alternativa, scegli l'azione **Prendi documento origine** per creare una lista di tutti i documenti di origine in uscita pronti per il prelievo presso l'ubicazione.  
6. Seleziona il pulsante **OK** per compilare le righe di prelievo in base ai documenti di origine selezionati.  

## Per registrare i prelievi magazzino

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievo magazzino**, quindi scegli il collegamento correlato.  
2. Nel campo **Codice collocazione** sulle righe di prelievo, la collocazione da cui gli articoli devono essere prelevati suggerisce la collocazione di default dell'articolo. È possibile modificare la collocazione in questa pagina, se necessario.  
3. Esegui il prelievo e immetti la quantità nel campo **Qtà da gestire**.

    Se è necessario prelevare gli articoli relativi a una riga da più collocazioni, ad esempio perché la collocazione non include tutta la quantità, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.

4. Scegli l'azione **Registra**.  

    * Registra la spedizione delle righe del documento di origine prelevate.
    * Se l'ubicazione prevede l'utilizzo di collocazioni, verranno inoltre creati movimenti warehouse per la registrazione delle modifiche alla quantità nella collocazione.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Gestione di articoli da assemblare su ordine con prelievi magazzino

Puoi anche usare la pagina **Prelievi magazzino** per prelevare e spedire vendite in cui gli articoli devono essere assemblati prima che possano essere spediti. Per ulteriori informazioni vedi [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).

Gli articoli assemblaggio su ordine non sono presenti fisicamente in una collocazione finché non vengono assemblati e registrati come output in una collocazione. Il prelievo di articoli da assemblare su ordine da una collocazione per la spedizione segue un flusso speciale.

1. Da una collocazione gli addetti alla warehouse trasferiscono gli articoli di assemblaggio al dock di spedizione, quindi registrano il prelievo magazzino.
2. Tramite il prelievo magazzino registrato vengono registrati l'output di assemblaggio, il consumo di componenti e la spedizione di vendita.

È possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo che venga creato automaticamente un movimento di magazzino quando viene creato il prelievo magazzino per l'articolo di assemblaggio. Seleziona il campo **Crea movimenti automaticamente** nella pagina **Setup assemblaggio**. Per ulteriori informazioni vedi [Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Le righe di prelievo magazzino per articoli di vendita vengono create in modi diversi a seconda se nessuna, qualche o tutte le quantità della riga di vendita vengano assemblate su ordine. Negli scenari in cui una parte della quantità è assemblata e un'altra è prelevata dal magazzino, viene creato un minimo di due righe di prelievo.

Per le vendite in cui la quantità completa nella riga ordine di vendita è assemblata su ordine, viene creata una riga prelievo magazzino per la quantità. Il valore nel campo **Quantità da assemblare** è uguale al valore nel campo **Qtà. da spedire**. Il campo **Assemblaggio su ordine** viene selezionato nella riga.

Se un flusso di output dell'assemblaggio per l'ubicazione, il campo **Codice collocazione** sulla riga di prelievo magazzino contiene il valore dei seguenti campi, nel seguente ordine.

* ***Cod. coll. sp. ass. su ordine** <!-- not applicable for inv pick-->
* **Cod. coll. art. da assembl.**

Se un codice collocazione non è specificato sulla riga di ordine di vendita e non è impostato alcun flusso di output dell'assemblaggio per l'ubicazione, il campo **Codice collocazione** sulla riga di prelievo magazzino è vuoto. L'addetto alla warehouse deve aprire la pagina **Contenuto collocazioni** e selezionare la collocazione in cui sono assemblati gli articoli di assemblaggio.

Negli scenari in cui una parte della quantità è assemblata e un'altra deve essere prelevata, viene creato un minimo di due righe di prelievo.

* Una riga di prelievo è relativa alla quantità per l'assemblaggio su ordine. [!INCLUDE [prod_short](includes/prod_short.md)] utilizza i seguenti campi, in questo ordine, per determinare il codice collocazione: **Codice collocazione**, **Cod. coll. sp. ass. su ordine**, e **Cod. coll. art. da assembl.**. Se i campi sono vuoti, l'addetto alla warehouse deve aprire la pagina **Contenuto collocazioni** e selezionare la collocazione in cui sono assemblati gli articoli.  
* L'altra riga di prelievo dipende da quali collocazioni possono soddisfare la quantità restante. Se l'articolo è conservato in più collocazioni, verranno create più righe. La riga Prendere è basata sulla quantità nel campo **Qtà da spedire**.

> [!NOTE]  
> Se gli articoli vengono assemblati su ordinazione, il prelievo di magazzino per l'ordine di vendita collegato crea un movimento di magazzino per tutti i componenti di assemblaggio.  

## Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Procedura dettagliata: prelievo e spedizione nelle configurazioni di warehouse di base](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
