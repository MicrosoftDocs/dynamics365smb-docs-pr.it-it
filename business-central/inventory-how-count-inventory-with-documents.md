---
title: Conteggio e adeguamento del magazzino
description: Descrive come contare l'inventario fisico e utilizzare i documenti di inventario per rettificare le scorte disponibili.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="count-and-adjust-inventory-using-documents"></a>Conteggio e rettifica dell'inventario utilizzando documenti

È possibile eseguire un inventario fisico degli articoli utilizzando documenti di ordine di inventario fisico e di registrazioni di inventario fisico. La pagina **Ordine inventario fisico** è utilizzata per organizzare il progetto di conteggio dell'inventario completo, ad esempio uno per posizione. Usa la pagina **Registrazione inventario fisico** per comunicare e acquisire il conteggio effettivo degli articoli. Puoi creare molteplici registrazioni per un ordine, ad esempio per distribuire gruppi di articoli a differenti dipendenti.

Il report **Registrazione inventario fisico** può essere stampato da ogni registrazione e contiene campi di quantità vuoti dove puoi immettere l'inventario conteggiato. Quando hai terminato il conteggio e le quantità sono state immesse nella pagina **Registrazione inventario fisico**, scegli l'azione **Fine**. Questa azione trasferisce le quantità alle righe pertinenti nella pagina **Ordine inventario fisico**. [!INCLUDE [prod_short](includes/prod_short.md)] garantisce l'impossibilità di registrare due volte il conteggio degli articoli.  

> [!NOTE]
> L'uso di documenti su come eseguire un conteggio di inventario fisico fornisce ulteriore controllo e supporta la distribuzione del conteggio a molteplici dipendenti. Puoi anche usare le registrazioni per eseguire lattività, come le pagine **Registrazioni inventario fisico** e **Registrazioni inventario fisico warehouse**. Per ulteriori informazioni, vedi [Conteggiare, rettificare e riclassificare l'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md). Questo articolo descrive come usare i documenti per eseguire un conteggio dell'inventario fisico.
>
> Se utilizzi le zone nella warehouse, non puoi utilizzare ordini di inventario fisico. Utilizza invece la pagina **Registrazioni inventario fisico warehouse** per conteggiare i movimenti warehouse prima di sincronizzarli con i movimenti contabili articoli.

Il conteggio dell'inventario mediante documenti consiste dei seguenti passaggi globali:

1. Creare un ordine di inventario fisico con le quantità di articoli previste precompilate.
2. Generare una o più registrazioni di inventario fisico a partire dall'ordine.
3. Immettere le quantità di articoli conteggiate nelle registrazioni, ad esempio come acquisite negli stampati, e impostarle su **Completato**.
4. Completare e registrate l'ordine di inventario fisico.

## <a name="to-create-a-physical-inventory-order"></a>Per creare un ordine di inventario fisico

Un ordine di inventario fisico è un documento completo che include un'intestazione di ordine di inventario fisico e righe di ordine. Le informazioni in un'intestazione di inventario fisico descrivono come eseguire l'inventario fisico. Le righe di ordine contengono informazioni sugli articoli e le relative ubicazioni.

Per creare le righe di ordine di inventario fisico, in genere utilizzi l'azione **Calcola righe** per aggiungere l'inventario corrente come righe nell'ordine. Puoi anche utilizzare l'azione **Copia da documento** per compilare le righe con il contenuto di un altro ordine di inventario fisico aperto o registrato. La procedura seguente descrive solo come utilizzare l'azione **Calcola righe**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini inventario fisico**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi necessari della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere l'azione **Calcola righe**.
5. Selezionare le opzioni come necessario.
6. Imposta i filtri, ad esempio, per includere solo un sottoinsieme di articoli da conteggiare con la prima registrazione.

    > [!TIP]
    > Per pianificare il conteggio dell'inventario da parte di più dipendenti, imposta filtri diversi ogni volta che utilizzi l'azione **Calcola righe** per compilare l'ordine solo con il sottoinsieme di articoli di inventario che un utente registrerà. Quindi, quando generi molteplici registrazioni di inventario fisico per più dipendenti, minimizzi il rischio di conteggiare gli articoli due volte. Per saperne di più, vedi [Per creare una registrazione di inventario fisico](#to-create-a-physical-inventory-recording).

7. Scegli il pulsante **OK**.

Una riga per ogni articolo esistente nell'ubicazione scelta e per i filtri e le opzioni impostati viene aggiunta all'ordine. Per gli articoli che vengono impostati per la tracciabilità degli articoli, viene selezionata la casella di controllo **Usa tracciabilità articolo** e le informazioni sulla quantità prevista di numeri seriali e di lotto sono disponibili scegliendo l'azione **Righe** e quindi **Righe tracciabilità articolo**. Per saperne di più, vedi [Gestire la tracciabilità degli articoli durante il conteggio dell'inventario](#handle-item-tracking-when-counting-inventory).

Ora puoi creare una o più registrazioni, che sono le istruzioni per i dipendenti che eseguono il conteggio.  

> [!NOTE]
> Se utilizzi la tracciabilità specifica del collo, puoi anche utilizzare i documenti per conteggiare e rettificare l'inventario con i numeri dei colli. Per iniziare a utilizzare questa funzionalità, devi attivare **Aggiornamento delle funzionalità: consente l'uso del monitoraggio dei colli negli ordini di inventario fisico** nella pagina **Gestione funzionalità**. Gli ordini di inventario fisico esistenti vengono aggiornati, tuttavia, [!INCLUDE [prod_short](includes/prod_short.md)] non può popolare il campo **Nr. collo** . Devi ricreare queste righe utilizzando l'azione **Calcola righe** nella pagina **Ordine inventario fisico**.
>
> Puoi immettere il numero di collo per gli articoli per cui è necessaria la tracciabilità del collo nella pagina **Righe registrazione inventario**. Scegli **Fine** per finalizzare la registrazione.
>
> Dopo aver scelto **Fine** nella pagina **Ordine inventario fisico**, [!INCLUDE [prod_short](includes/prod_short.md)] calcola le differenze rispetto al collo e ad altri dettagli di tracciabilità articolo ed effettua rettifiche positive o negative.

## <a name="to-create-a-physical-inventory-recording"></a>Per creare una registrazione di inventario fisico

Per ciascun ordine di inventario fisico puoi creare uno o più documenti di registrazione dell'inventario fisico in cui i dipendenti immettono le quantità conteggiate. I dipendenti possono immettere le quantità manualmente o con un dispositivo di scansione.

Per impostazione predefinita, una registrazione viene creata per tutte le righe nel relativo ordine di inventario fisico. Per evitare che due dipendenti conteggino gli stessi articoli se distribuisci il conteggio, compila gradualmente l'ordine di inventario fisico impostando i filtri nel processo batch **Calcola righe**. Quindi crea la registrazione dell'inventario fisico con la casella di controllo **Solo righe non nelle registrazioni** selezionata. Questa impostazione garantisce che ogni nuova registrazione contenga articoli differenti da quelli in altre registrazioni.

Per il conteggio manuale, puoi stampare il report **Registrazione inventario fisico**, che presenta una colonna vuota in cui gli impiegati del warehouse possono inserire le quantità conteggiate. Al termine del conteggio, immetti le quantità registrate nelle righe pertinenti della pagina **Registrazione inventario fisico**. Infine, si trasferiscono le quantità registrate al relativo ordine di inventario fisico impostando lo stato su **Completato**.

1. Nella pagina **Ordine inventario fisico** contenente le righe per gli articoli da conteggiare in una registrazione, scegliere l'azione **Crea nuova registrazione**.
2. Selezionare le opzioni e impostare i filtri come necessario.
3. Scegli il pulsante **OK**.
4. Carica ogni set di articoli da conteggiare nell'ordine di inventario fisico correlato e ripeti i passaggi da 1 a 3 con la casella di controllo **Solo righe non nelle registrazioni** selezionata.
5. Scegliere l'azione **Registrazioni** per aprire la pagina **Elenco registrazione magazzino fisico**.
6. Aprire la registrazione pertinente.
7. Compilare i campi appropriati nella Scheda dettaglio **Generale**.
8. Per gli articoli che utilizzano la tracciabilità degli articoli, creare una riga supplementare per ogni codice di numero di lotto o numero seriale scegliendo l'azione **Funzioni** e quindi l'azione **Copia riga**. Per saperne di più, vedi [Gestire la tracciabilità degli articoli durante il conteggio dell'inventario](#handle-item-tracking-when-counting-inventory).  
9. Scegli l'azione **Stampa** per preparare il documento fisico che i dipendenti possono utilizzare per annotare le quantità che conteggiano.

## <a name="to-finish-a-physical-inventory-recording"></a>Terminare una registrazione di inventario fisico

Dopo che i dipendenti hanno contato le quantità, registrale in [!INCLUDE [prod_short](includes/prod_short.md)].

1. Nella pagina **Elenco registrazione magazzino fisico**, selezionare la registrazione di inventario fisico che si desidera terminare e scegliere l'azione **Modifica**.
2. Nella Scheda dettaglio **Righe**, immettere la quantità conteggiata effettiva nel campo **Quantità** per ogni riga.
3. Per gli articoli con numeri di serie o di lotto (la casella di controllo **Usa tracciabilità articolo** è selezionata), immetti le quantità conteggiate nelle righe rispettivamente per i numeri di serie e i numeri di lotto dell'articolo. Per saperne di più, vedi [Gestire la tracciabilità degli articoli durante il conteggio dell'inventario](#handle-item-tracking-when-counting-inventory).
4. Seleziona la casella di controllo **Registrato** in ogni riga.
5. Dopo aver immesso tutti i dati per una registrazione di inventario fisico, scegliere l'azione **Fine**. Da notare che la casella di controllo **Registrato** deve essere selezionata per tutte le righe.

    > [!NOTE]
    > Quando si termina una registrazione di inventario fisico, ogni riga viene trasferita alla riga esattamente corrispondente nell'ordine di inventario fisico correlato. Per trovare una corrispondenza, i campi **Nr. articolo**, **Codice variante**, **Codice ubicazione** e **Codice collocazione** devono essere gli stessi nella registrazione e nelle righe dell'ordine.>
    > 
    > Se non vi è una riga di ordine di inventario fisico corrispondente e se la casella di controllo **Consenti registrazione senza ordine** è selezionata, una nuova riga viene aggiunta e viene selezionata la casella di controllo **Registrato senza ordine** nella riga dell'ordine di inventario fisico correlato. In caso contrario, viene visualizzato un messaggio di errore e il processo viene annullato.> Se più righe della registrazione di inventario fisico corrispondono a una riga dell'ordine di inventario fisico, viene visualizzato un messaggio e il processo viene annullato. Se, per qualche ragione, nell'ordine di inventario fisico vi sono due righe di inventario fisico identiche, puoi utilizzare un'azione per risolvere il problema. Per ulteriori informazioni, vedi [Per trovare righe di ordine di inventario fisico duplicate](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>Per completare un ordine di inventario fisico

Al termine di una registrazione di inventario fisico, il campo **Quantità registrata (base)** nell'ordine di inventario fisico correlato viene aggiornato con i valori conteggiati (registrati) e la casella di controllo **In righe registrazione** viene selezionata. Se una quantità conteggiato è differente da quella previsto, tale differenza è indicata nei campi **Quantità positiva (base)** e **Quantità negativa (base)**.

Per accedere alle quantità previste e le eventuali differenze registrate per gli articoli con la tracciabilità articolo, scegli l'azione **Righe** e quindi scegli l'azione **Righe tracciabilità articolo** per selezionare varie visualizzazioni per numeri seriali e di lotto nel conteggio dell'inventario fisico.

È inoltre possibile scegliere l'azione **Differenza ordini magazzino fisico** per visualizzare le eventuali differenze tra la quantità prevista e la quantità conteggiata.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Per trovare righe di ordine di inventario fisico duplicate

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini inventario fisico**, quindi scegli il collegamento correlato.
2. Apri l'ordine di inventario fisico per il quale vuoi visualizzare le righe duplicate.
3. Scegliere l'azione **Visualizza righe duplicate**.

Le righe di ordine di inventario fisico duplicate vengono visualizzate affinché sia possibile eliminarle e mantenere solo una riga con un set di valori univoco nei campi **Nr. articolo**, **Codice variante**, **Codice ubicazione** e **Codice collocazione**.

### <a name="to-post-a-physical-inventory-order"></a>Per registrare un ordine di inventario fisico

Dopo il completamento di un ordine di inventario fisico e la modifica del relativo stato a **Completato**, puoi registrarlo. Puoi impostare lo stato di un ordine di inventario fisico solo su **Completato** nelle seguenti condizioni:

- Lo stato di tutte le registrazioni di inventario fisico correlate è **Completato**.
- Ogni riga di ordine di inventario fisico viene conteggiata da almeno una riga di registrazione inventario.
- Le caselle di controllo **In righe registrazione** e **Quantità prevista calcolata** sono selezionate per tutte le righe di ordine di inventario fisico.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini inventario fisico**, quindi scegli il collegamento correlato.
2. Selezionare l'ordine di inventario fisico che si intende completare, quindi scegliere l'azione **Modifica**.

    Nella pagina **Ordine inventario fisico**, la quantità registrata è visualizzata nel campo **Quantità registrata (base)**.
3. Scegliere l'azione **Fine**.

    Il valore nel campo **Stato** è **Completato**. Ora puoi modificare l'ordine solo scegliendo l'azione **Riapri**.
4. Per registrare l'ordine, scegliere l'azione **Registra**, quindi scegliere il pulsante **OK**.

    I movimenti contabili articoli vengono aggiornati insieme ai movimenti di tracciabilità ordine correlati.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### <a name="to-view-posted-physical-inventory-orders"></a>Per visualizzare ordini di inventario fisico registrati

Dopo la registrazione, l'ordine di inventario fisico viene eliminato ed è possibile visualizzare e valutare il documento come ordine di inventario fisico registrato incluse le relative registrazioni di inventario fisico e gli eventuali commenti. L'ordine registrato include le registrazioni dell'inventario fisico e gli eventuali commenti immessi.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini magazzino fisico registrati**, quindi scegli il collegamento correlato.
2. Nella pagina **Ordini magazzino fisico registrati**, seleziona l'ordine di inventario registrato, quindi scegli l'azione **Visualizza**.
3. Per visualizzare un elenco di registrazioni di inventario fisico correlate, scegliere l'azione **Registrazioni**.

## <a name="handle-item-tracking-when-counting-inventory"></a>Gestire la tracciabilità degli articoli durante il conteggio dell'inventario

La tracciabilità degli articoli è relativa ai numeri di serie o di lotto assegnati agli articoli. Quando conteggi un articolo che è immagazzinato nell'inventario come, ad esempio, 10 numeri di lotto diversi, il dipendente deve essere in grado di registrare quali e quante unità di ogni numero di lotto sono nell'inventario. Per ulteriori informazioni, vedi [Utilizzare numeri di serie e di lotto](inventory-how-work-item-tracking.md).

La casella di controllo **Usa tracciabilità articolo** nelle righe di ordine di inventario fisico viene selezionata automaticamente se un codice di tracciabilità articolo è impostato per l'articolo. Puoi selezionare o deselezionare manualmente la casella di controllo.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Esempio - Preparare una registrazione di inventario fisico per un articolo tracciato

Considerare un inventario fisico per l'articolo A, che è immagazzinato nell'inventario come dieci numeri seriali differenti.

1. Nella riga di registrazione per l'articolo, seleziona la casella di controllo **Usa tracciabilità articolo**.
2. Scegliere il campo **Nr. seriale**, selezionare il primo numero seriale presente nell'inventario per l'articolo, quindi scegliere il pulsante **OK**.

    Copia la riga del primo articolo tracciato per inserire righe aggiuntive che corrispondono al numero di numeri seriali immagazzinati nell'inventario.

3. Scegli l'azione **Funzioni** e quindi **Copia riga**.
4. Nella pagina **Copia riga record magazzino fisico**, immetti **9** nel campo **Nr. di copie** quindi scegli il pulsante **OK**.
5. Nella prima riga, nel campo **Nr. seriale** seleziona il numero seriale successivo per l'articolo.
6. Ripeti il passaggio 5 per i restanti otto numeri di serie. Assicurati di non selezionare lo stesso numero due volte.
7. Scegli l'azione **Stampa** per preparare lo stampato che i dipendenti utilizzano per annotare gli articoli conteggiati e i numeri seriali/di lotto.

Da notare che il report **Registrazione inventario fisico** contiene dieci righe per l'articolo A, uno per ogni numero seriale.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Esempio - Registrare le differenze nei numeri di lotto conteggiati

Un articolo tracciato viene archiviato nell'inventario con la numerazione "LOT“.

**Giacenze previste**:

|Nr. lotto|Quantità|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Totale|120|

**Quantità registrate**:

|Nr. lotto|Quantità|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Totale|112|

**Quantità da convalidare**:

|Nr. lotto|Quantità prevista|Quantità registrata|Quantità da convalidare|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Totale|120|112|-8|

Nella pagina **Ordine inventario fisico**, il campo **Quantità negativa (base)** contiene **8**. Per la riga di ordine, la pagina **Elenco tracciabilità articoli magazzino fisico** mostra le quantità positive o negative per ogni numero di lotto.

## <a name="inventory-documents"></a>Documenti di inventario

I seguenti tipi di documenti sono utili per la gestione del tuo warehouse:

* Usa **Carichi magazzino** per registrare rettifiche positive di articoli in base a qualità, quantità e costo.
* Usa **Spedizioni magazzino** per cancellare merci mancanti o danneggiate.

Puoi stampare questi documenti in qualsiasi fase, rilasciarli e riaprirli e assegnare valori comuni, come le dimensioni, nell'intestazione. Per ristampare i documenti dopo la registrazione, utilizza le pagine **Ricevuta magazzino registrata** e **Spedizione magazzino registrata**.

> [!NOTE]
> Prima di poter utilizzare questi documenti devi specificare una serie di numeri per creare i loro identificatori. Per saperne di più, vedi [Per impostare la numerazione dei documenti di inventario](#to-set-up-numbering-for-inventory-documents).

### <a name="to-set-up-numbering-for-inventory-documents"></a>Per impostare la numerazione per i documenti di magazzino

La seguente procedura illustra come impostare una numerazione per i documenti del magazzino.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup magazzino**, quindi scegli il collegamento correlato.
2. Nella Scheda dettaglio **Numerazione**, specifica nei seguenti campi la serie di numeri per i documenti:

   - **N. ricevuta magazzino**  
   - **N. ricevute magazzino registrate**  
   - **N. spedizione magazzino**  
   - **N. spedizione magazzino registrata**  

### <a name="to-create-and-post-an-inventory-document"></a>Per creare e registrare un documento di magazzino

La procedura seguente mostra come creare, stampare e registrare una ricevuta di magazzino. I passaggi sono simili a quelli per le spedizioni del magazzino.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Carichi magazzino**, quindi scegli il collegamento correlato.  
2. Nell'intestazione della pagina **Ricevuta di magazzino**, scegli la posizione nel campo **Codice posizione**, quindi compila i campi rimanenti secondo necessità.
3. Nella Scheda dettaglio **Linee**, nel campo **Articolo**, scegli l'articolo di magazzino. Nel campo **Quantità** immettere il numero di articoli da aggiungere.
4. Per stampare un report **Ricevuta magazzino** dalla pagina **Ricevuta di magazzino**, scegli l'azione **Stampa**.

Le seguenti funzioni sono disponibili nella pagina **Ricevuta di magazzino**:

- Scegli le azioni **Rilascio** o **Riapri** per impostare lo stato per la fase di elaborazione successiva.  
- Scegli l'azione **Registra** per registrare il carico di magazzino o scegli **Registra e stampa** per registrare il carico e stampare il report di prova.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="printing-inventory-documents"></a>Stampa di documenti di magazzino

Puoi specificare i report che devono essere stampati in fasi diverse scegliendo una delle seguenti opzioni nel campo **Uso** della pagina **Selezione report - Magazzino**:

* Ricevuta magazzino
* Spedizione magazzino
* Ricevuta magazzino registrata
* Spedizione magazzino registrata

> [!NOTE]
> I report disponibili potrebbero variare in base alla localizzazione per il tuo paese/area geografica. L'applicazione di base non include alcun layout.

## <a name="see-also"></a>Vedere anche

[Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md)  
[Utilizzare i numeri di serie e di lotto](inventory-how-work-item-tracking.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica gestione del magazzino](design-details-warehouse-management.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
