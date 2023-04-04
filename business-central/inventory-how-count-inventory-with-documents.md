---
title: Conteggio e adeguamento del magazzino
description: Descrive come contare l'inventario fisico e utilizzare i documenti di inventario per rettificare le scorte disponibili.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/01/2021
ms.author: edupont
---
# Conteggio e regolazione del magazzino utilizzando documenti

È possibile eseguire un inventario fisico degli articoli utilizzando documenti di ordine di inventario fisico e di registrazioni di inventario fisico. La pagina **Ordine inventario fisico** è utilizzata per organizzare il progetto di conteggio dell'inventario completo, ad esempio uno per posizione. La pagina **Registrazione magazzino fisico** è utilizzata per comunicare e acquisire il conteggio effettivo degli articoli. È possibile creare molteplici registrazioni per un ordine, ad esempio per distribuire gruppi di articoli a dipendenti differenti.

Il report **Registrazione inventario fisico** può essere stampato da ogni registrazione e contiene campi di quantità vuoti per l'immissione dell'inventario conteggiato. Quando un utente termina il conteggio e le quantità vengono immesse nella pagina **Registrazione inventario fisico**, si sceglie l'azione **Fine**. Ciò trasferisce le quantità alle righe pertinenti alla pagina **Ordine inventario fisico**. La funzionalità garantisce che nessun conteggio di articoli può essere registrato due volte.  

> [!NOTE]
> L'uso di documenti su come eseguire un magazzino fisico fornisce ulteriore controllo e supporta la distribuzione del conteggio a molteplici impiegati. È inoltre possibile eseguire la task utilizzando registrazioni, come le pagine **Registrazioni inventario fisico** e **Registrazioni dell'inventario fisico warehouse**. Per ulteriori informazioni, vedere [Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni ](inventory-how-count-adjust-reclassify.md). Questo articolo descrive come eseguire un magazzino fisico utilizzando i documenti.
>
> Se utilizzi le zone, non puoi utilizzare gli ordini di magazzino fisico. Utilizza invece la pagina **Registrazioni del magazzino fisico warehouse** per conteggiare i movimenti warehouse prima di sincronizzarli con i movimenti contabili articoli.

Il conteggio dell'inventario utilizzando documenti consiste dei seguenti passaggi globali:

1. Creare un ordine di inventario fisico con le quantità di articoli previste precompilate.
2. Generare una o più registrazioni di inventario fisico a partire dall'ordine.
3. Immettere le quantità di articoli conteggiate nelle registrazioni, ad esempio come acquisite negli stampati, e impostarle su **Completato**.
4. Completare e registrate l'ordine di inventario fisico.

## Per creare un ordine di inventario fisico

Un ordine di inventario fisico è un documento è completo che consiste di un'intestazione di ordine di inventario fisico e alcune righe di ordine di inventario fisico. Le informazioni in un'intestazione di inventario fisico descrivono come eseguire l'inventario fisico. Le righe dell'ordine di inventario fisico contengono informazioni sugli articoli e le relative ubicazioni.

Per creare le righe dell'ordine di inventario fisico, in genere si utilizza la funzione **Calcola righe** per riflettere la giacenza corrente come righe nell'ordine. In alternativa, è possibile utilizzare la funzione **Copia da documento** per compilare le righe con il contenuto di un altro ordine di inventario fisico aperto o registrato. La procedura seguente descrive solo come utilizzare la funzione **Calcola righe**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini inventario fisico**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi necessari della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Scegliere l'azione **Calcola righe**.
5. Selezionare le opzioni come necessario.
6. Impostare i filtri, ad esempio, per includere solo un sottoinsieme di articoli da conteggiare con la prima registrazione.

    > [!TIP]
    > Per pianificare il conteggio dell'inventario da parte di più dipendenti , è consigliabile impostare filtri diversi ogni volta che si utilizza l'azione **Calcola righe** per compilare l'ordine solo con il sottoinsieme di articoli dell'inventario che un utente registrerà. In questo modo, quando si generano molteplici registrazioni di inventario fisico per più dipendenti, si minimizza il rischio di conteggiare gli articoli due volte. Per ulteriori informazioni, vedere la sezione [Per creare una registrazione di inventario fisico](#to-create-a-physical-inventory-recording).

7. Scegliere il pulsante **OK**.

Una riga per ogni articolo esistente nell'ubicazione scelta e per i filtri e le opzioni impostati viene inserita nell'ordine. Per gli articoli che vengono impostati per la tracciabilità degli articoli, viene selezionata la casella di controllo **Usa tracciabilità articolo** e le informazioni sulla quantità prevista di numeri seriali e di lotto sono disponibile scegliendo l'azione **Righe** e quindi **Righe tracciabilità articolo**. Per ulteriori informazioni, vedere la sezione [Gestione della tracciabilità degli articoli durante il conteggio dell'inventario](#handling-item-tracking-when-counting-inventory).

Ora è possibile procedere alla creazione di una o più registrazioni, che sono le istruzioni per i dipendenti che eseguono il conteggio effettivo.  

## Per creare una registrazione di inventario fisico

Per ogni ordine di inventario fisico, è possibile creare uno o più documenti di registrazione di inventario fisico nei quali i dipendenti immettono le quantità conteggiate, manualmente o mediante un con dispositivo di scansione integrato.

Per impostazione predefinita, una registrazione viene creata per tutte le righe nel relativo ordine di inventario fisico. Per evitare che due dipendenti contino gli stessi articoli nel caso di un conteggio distribuito, è consigliabile compilare gradualmente l'ordine di inventario fisico impostando i filtri sul processo batch **Calcola righe** (vedere la sezione “Per creare un ordine di inventario fisico") e quindi creare la registrazione di inventario fisico durante la selezione della casella di controllo **Solo righe non nelle registrazioni**. Questo impostazioni garantiscono che ogni nuova registrazione creata contenga solo articoli differenti da quelli in altre registrazioni.

Nel caso di conteggio manuale, è possibile stampare un elenco, il report **Registrazione magazzino fisico**, che presenta una colonna vuota in cui inserire le quantità conteggiate. Al termine del conteggio, si immettono le quantità registrate nelle righe pertinenti della pagina **Registrazione magazzino fisico**. Infine, si trasferiscono le quantità registrate al relativo ordine di inventario fisico impostando lo stato su **Completato**.

1. Nella pagina **Ordine inventario fisico** contenente le righe per gli articoli da conteggiare in una registrazione, scegliere l'azione **Crea nuova registrazione**.
2. Selezionare le opzioni e impostare i filtri come necessario.
3. Scegliere il pulsante **OK**.

    Viene creato un documento di registrazione di inventario fisico

4. Caricare ogni set di articoli da conteggiare nell'ordine di inventario fisico correlato e ripetere i passaggi da 1 a 3 con la casella di controllo **Solo righe non nelle registrazioni** selezionata.

5. Scegliere l'azione **Registrazioni** per aprire la pagina **Elenco registrazione magazzino fisico**.
6. Aprire la registrazione pertinente.
7. Compilare i campi appropriati nella Scheda dettaglio **Generale**.
8. Per gli articoli che utilizzano la tracciabilità degli articoli, creare una riga supplementare per ogni codice di numero di lotto o numero seriale scegliendo l'azione **Funzioni** e quindi l'azione **Copia riga**. Per ulteriori informazioni, vedere la sezione [Gestione della tracciabilità degli articoli durante il conteggio dell'inventario](#handling-item-tracking-when-counting-inventory).  
9. Scegliere l'azione **Stampa** per produrre il documento fisico che i dipendenti utilizzeranno per annotare le quantità conteggiate.

## Terminare una registrazione di inventario fisico

Quando i dipendenti hanno conteggiato le quantità di inventario, è necessario registrarle nel sistema.

1. Nella pagina **Elenco registrazione magazzino fisico**, selezionare la registrazione di inventario fisico che si desidera terminare e scegliere l'azione **Modifica**.
2. Nella Scheda dettaglio **Righe**, immettere la quantità conteggiata effettiva nel campo **Quantità** per ogni riga.
3. Per gli articoli con numeri di serie o di lotto (la casella di controllo **Usa tracciabilità articolo** è selezionata), immettere le quantità conteggiate nelle righe dedicate rispettivamente ai numeri di serie e ai numeri di lotto degli articoli. Per ulteriori informazioni, vedere la sezione [Gestione della tracciabilità degli articoli durante il conteggio dell'inventario](#handling-item-tracking-when-counting-inventory).
4. Selezionare la casella di controllo **Registrato** in ogni riga.
5. Dopo aver immesso tutti i dati per una registrazione di inventario fisico, scegliere l'azione **Fine**. Da notare che la casella di controllo **Registrato** deve essere selezionata per tutte le righe.

> [!NOTE]
> Quando si termina una registrazione di inventario fisico, ogni riga viene trasferita alla riga esattamente corrispondente nell'ordine di inventario fisico correlato. Per un'esatta corrispondenza, i campi **Nr. articolo**, **Codice variante**, **Codice ubicazione** e **Codice collocazione** devono essere gli stessi nella registrazione e nelle righe dell'ordine.<br /><br />
> Se non vi è una riga di ordine di inventario fisico corrispondente e se la casella di controllo **Consenti registrazione senza ordine** è selezionata, una nuova riga viene inserita automaticamente e viene selezionata la casella di controllo **Registrato senza ordine** nella riga dell'ordine di inventario fisico correlato. In caso contrario, viene visualizzato un messaggio di errore e il processo viene annullato.<br /><br />
> Se più righe della registrazione di inventario fisico corrispondono a una riga dell'ordine di inventario fisico, viene visualizzato un messaggio e il processo viene annullato. Se, per qualche ragione, nell'ordine di inventario fisico vi sono due righe di inventario fisico identiche, è possibile utilizzare una funzione per risolvere il problema. Per ulteriori informazioni, vedere [Per trovare righe di ordine di inventario fisico duplicate](#to-find-duplicate-physical-inventory-order-lines).

## Per completare un ordine di inventario fisico

Al termine di una registrazione di inventario fisico, il campo **Quantità registrata (base)** nell'ordine di inventario fisico correlato viene aggiornato con i valori conteggiati (registrati) e la casella di controllo **In righe registrazione** viene selezionata. Se un valore conteggiato è differente da quello previsto, tale differenza è indicata rispettivamente nel campo **Quantità positiva (base)** e **Quantità negativa (base)**.

Per visualizzare le quantità previste e le eventuali differenze registrate per gli articoli con la tracciabilità degli articoli, scegliere l'azione **Righe** e quindi scegliere l'azione **Righe tracciabilità articolo** per selezionare varie visualizzazioni per numeri seriali e di lotto coinvolti nel conteggio dell'inventario fisico.

È inoltre possibile scegliere l'azione **Differenza ordini magazzino fisico** per visualizzare le eventuali differenze tra la quantità prevista e la quantità conteggiata.

### Per trovare righe di ordine di inventario fisico duplicate

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini inventario fisico**, quindi scegli il collegamento correlato.
2. Aprire l'ordine di inventario fisico per il quale si desidera visualizzare le righe duplicate.
3. Scegliere l'azione **Visualizza righe duplicate**.

Eventuali righe di ordine di inventario fisico duplicate vengono visualizzate affinché sia possibile eliminarle e mantenere solo una riga con un set di valori univoco nei campi **Nr. articolo**, **Codice variante**, **Codice ubicazione** e **Codice collocazione**.

### Per registrare un ordine di inventario fisico

Dopo il completamento di un ordine di inventario fisico e la modifica del relativo stato a **Completato**, è possibile registrarlo. È possibile impostare lo stato di un ordine di inventario fisico su **Completato** se le seguenti condizioni sono vere:

- Lo stato di tutte le registrazioni di inventario fisico correlate è **Completato**.
- Ogni riga di ordine di inventario fisico è stata conteggiata da almeno una riga di registrazione inventario.
- Le caselle di controllo **In righe registrazione** e **Quantità prevista calcolata** sono state selezionate per tutte le righe di ordine di inventario fisico.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini inventario fisico**, quindi scegli il collegamento correlato.
2. Selezionare l'ordine di inventario fisico che si intende completare, quindi scegliere l'azione **Modifica**.

    Nella pagina **Ordine inventario fisico**, si visualizza la quantità registrata nel campo **Quantità registrata (base)**.
3. Scegliere l'azione **Fine**.

    Il valore nel campo **Stato** diventa **Completato** ed è ora possibile modificare l'ordine soltanto scegliendo dapprima l'azione **Riapri**.
4. Per registrare l'ordine, scegliere l'azione **Registra**, quindi scegliere il pulsante **OK**.

I movimenti contabili articoli interessati vengono aggiornati insieme ai movimenti di tracciabilità ordine correlati.

### Per visualizzare ordini di inventario fisico registrati

Dopo la registrazione, l'ordine di inventario fisico verrà eliminato ed è possibile visualizzare e valutare il documento come ordine di inventario fisico registrato incluse le relative registrazioni di inventario fisico e gli eventuali commenti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini magazzino fisico registrati**, quindi scegli il collegamento correlato.
2. Nella pagina **Ordini magazzino fisico registrati**, selezionare l'ordine di inventario registrato che si desidera visualizzare, quindi scegliere l'azione **Visualizza**.
3. Per visualizzare un elenco di registrazioni di inventario fisico correlate, scegliere l'azione **Registrazioni**.

## Gestione della tracciabilità degli articoli durante il conteggio dell'inventario

La tracciabilità degli articoli è relativa ai numeri di serie o di lotto assegnati agli articoli. Quando si conteggia un articolo che è immagazzinato nell'inventario come, ad esempio, 10 numeri di lotto diversi, il dipendente deve essere in grado di registrare quali e quante unità di ogni numero di lotto sono nell'inventario. Per ulteriori informazioni sulla funzionalità di tracciabilità di articoli, vedere [Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md).

La casella di controllo **Usa tracciabilità articolo** nelle righe di ordine di inventario fisico viene selezionata automaticamente se un codice di tracciabilità articolo è impostato per l'articolo, ma è anche possibile selezionarla o deselezionarla manualmente.

### Esempio - Preparare una registrazione di inventario fisico per un articolo tracciato

Considerare un inventario fisico per l'articolo A, che è immagazzinato nell'inventario come dieci numeri seriali differenti.
1. Nella riga di registrazione per l'articolo, selezionare la casella di controllo **Usa tracciabilità articolo**.
2.  Scegliere il campo **Nr. seriale**, selezionare il primo numero seriale presente nell'inventario per l'articolo, quindi scegliere il pulsante **OK**.

    Procedere con la copia della riga del primo articolo tracciato per inserire righe aggiuntive corrispondenti al numero di numeri seriali immagazzinati nell'invetario.

3. Scegliere l'azione **Funzioni** e quindi l'azione **Copia riga**.
4. Nella pagina **Copia riga record magazzino fisico**, immettere 9 nel campo **Nr. di copie** quindi scegliere il pulsante **OK**.
5. Nella prima delle righe della copia, selezionare il campo **Nr. seriale** e selezionare il numero seriale successivo per l'articolo.
6. Ripetere il passaggio 5 per gli otto numeri seriali rimanenti, facendo attenzione a non selezionarne uno due volte.
7. Scegliere l'azione **Stampa** per preparare lo stampato che i dipendenti utilizzeranno per annotare gli articoli conteggiati e i numeri seriali/di lotto.

Da notare che il report **Registrazione inventario fisico** contiene dieci righe per l'articolo A, uno per ogni numero seriale.

### Esempio - Registrare e inserire le differenze nei numeri di lotto conteggiati

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

Nella pagina **Ordine inventario fisico**, il campo **Quantità negativa (base)** conterrà *8*. Per la riga in questione, la pagina **Elenco tracciabilità articoli magazzino fisico** conterrà le quantità positive o negative per i singoli numeri di lotto.

## Documenti di magazzino

I seguenti tipi di documenti sono utili per la gestione del tuo warehouse:

- Usa **Ricevute di magazzino** per registrare rettifiche positive di articoli in base a qualità, quantità e costo.
- Usa **Spedizioni di magazzino** per cancellare merci mancanti o danneggiate.

Puoi stampare questi documenti in qualsiasi fase, rilasciarli e riaprirli e assegnare valori comuni, comprese le dimensioni, nell'intestazione. Se desideri ristampare i documenti dopo che sono stati pubblicati, puoi farlo nelle pagine **Ricevuta scorte registrata** e **Spedizione magazzino registrata**.

> [!NOTE]
> Prima di poter utilizzare questi documenti è necessario specificare una serie di numeri per creare i loro identificatori. Per ulteriori informazioni, vedere la sezione seguente.

### Per impostare la numerazione per i documenti di magazzino

La seguente procedura illustra come impostare una numerazione per i documenti del magazzino.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup magazzino**, quindi scegli il collegamento correlato.
2. Nella Scheda dettaglio **Numerazione**, specifica nei seguenti campi la serie di numeri per i documenti:
   - **N. ricevuta magazzino**  
   - **N. ricevute magazzino registrate**  
   - **N. spedizione magazzino**  
   - **N. spedizione magazzino registrata**  

### Per creare e registrare un documento di magazzino

La procedura seguente mostra come creare, stampare e registrare una ricevuta di magazzino. I passaggi sono simili a quelli per le spedizioni del magazzino.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Carichi magazzino**, quindi scegli il collegamento correlato.  
2. Nell'intestazione della pagina **Ricevuta di magazzino**, scegli la posizione nel campo **Codice posizione**, quindi compila i campi rimanenti secondo necessità.
3. Nella Scheda dettaglio **Linee**, nel campo **Articolo**, scegli l'articolo di magazzino. Nel campo **Quantità** immettere il numero di articoli da aggiungere. 
4. Per stampare un report **Ricevuta magazzino** dalla pagina **Ricevuta di magazzino**, scegli l'azione **Stampa**.

Le seguenti funzioni sono disponibili nella pagina **Ricevuta di magazzino**:

- Scegli le azioni **Rilascio** o **Riapri** per impostare lo stato per la fase di elaborazione successiva  
- Scegli l'azione **Registra** per registrare la ricevuta di magazzino o scegli **Registra e stampa** per registrare la ricevuta e stampare il report di prova  

## Stampa dei documenti di magazzino

Puoi specificare i report che devono essere stampati in fasi diverse scegliendo una delle seguenti opzioni nel campo **Uso** nella pagina **Selezione report - Magazzino**:

- Ricevuta magazzino
- Spedizione magazzino
- Ricevuta magazzino registrata
- Spedizione magazzino registrata

> [!NOTE]
> I report disponibili possono variare in base alla localizzazione del tuo paese. L'applicazione di base non include alcun layout.

## Vedi il relativo [training Microsoft](/training/modules/adjust-inventory/)

## Vedere anche

[Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md)  
[Utilizzare i numeri di serie e di lotto](inventory-how-work-item-tracking.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica gestione del magazzino](design-details-warehouse-management.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
