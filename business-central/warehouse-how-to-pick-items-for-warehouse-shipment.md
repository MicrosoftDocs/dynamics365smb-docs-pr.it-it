---
title: Prelevare articoli per la spedizione warehouse
description: Informazioni sull'utilizzo dei documenti di prelievo warehouse per creare ed elaborare le informazioni di prelievo prima di registrare una spedizione warehouse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/11/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# Prelevare articoli per la spedizione warehouse

In [!INCLUDE[prod_short](includes/prod_short.md)], il prelievo e la spedizione degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in uscita|Richiesto prelievo|Richiesta spedizione|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registra il prelievo e la spedizione dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registra il prelievo e la spedizione da un documento di prelievo magazzino|Attivato||Di base: ordine per ordine.|  
|C|Registra il prelievo e la spedizione da un documento di spedizione warehouse||Attivato|Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni vedi [Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md).

Questo articolo fa riferimento al metodo D nella tabella. Per ulteriori informazioni sugli articoli di spedizione, vai a [Articoli di spedizione](warehouse-how-ship-items.md).

Quando l'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi e delle spedizioni warehouse, è possibile utilizzare i documenti di prelievo warehouse per creare ed elaborare le informazioni di prelievo prima di registrare la spedizione warehouse.  

Puoi creare i documenti di prelievo warehouse da zero. I prelievi fanno parte di un flusso di lavoro in cui la persona che sta elaborando un ordine li crea in modalità push o l'addetto alla warehouse li crea in modalità pull:

- In modalità push, dove utilizzi l'azione **Crea prelievo** nella pagina **Spedizione warehouse** . Seleziona le righe da prelevare e prepara i prelievi specificando, ad esempio, le collocazioni da cui prelevare, quelle in cui inserire e il numero di unità da gestire. Le collocazioni possono essere predefinite per l'ubicazione o la risorsa warehouse.
- In modalità pull, dove utilizzi l'azione **Rilascia** nella pagina **Spedizione warehouse** per rendere gli articoli disponibili per il prelievo. Quindi, nella pagina **Prospetto prelievi**, i dipendenti della warehouse possono utilizzare l'azione **Prendi documenti warehouse** per prendere i prelievi assegnati.

> [!NOTE]  
> Il prelievo per una spedizione warehouse di articoli assemblati per un ordine di vendita segue gli stessi passaggi dei normali prelievi warehouse per la spedizione, come descritto in questo articolo. Tuttavia, il numero delle righe prelievo per la quantità da spedire può essere molti a uno perché vengono selezionati i componenti, non l'articolo assemblato.  
>
> Le righe prelievo warehouse vengono create per il valore nel campo **Quantità residua** sulle righe dell'ordine di assemblaggio collegato alla riga dell'ordine di vendita spedito. Tutti i componenti vengono prelevati con una sola azione. Per ulteriori informazioni vedi [Gestione di articoli di assemblaggio su ordine in spedizioni warehouse](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Per informazioni sul prelievo di componenti per gli ordini di assemblaggio, incluse le situazioni in cui l'articolo di assemblaggio è correlato a una spedizione vendita, vedi [Prelevare per produzione, assemblaggio o commesse in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## Controllare se gli articoli sono disponibili per il prelievo

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## Per creare documenti di prelievo in blocco con i prospetti prelievi

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto prelievi**, quindi scegli il collegamento correlato.  

2. Scegliere l'azione **Prendi documenti warehouse**.  

    L'elenco includerà tutte le spedizioni che sono state rilasciate per il prelievo, comprese quelle per le quali sono già state create istruzioni di prelievo. I documenti contenenti righe di prelievo per le quali il prelievo è stato eseguito per intero e registrato non vengono visualizzati in questa lista.  
3. Selezionare le spedizioni per cui preparare un prelievo.

    > [!NOTE]  
    >  Se tenti di selezionare un documento di spedizione o stoccaggio interno per cui sono già state create istruzioni relative a tutte le righe, viene visualizzato un messaggio per informare che non esiste alcun elemento da gestire. Per combinare le istruzioni di prelievo warehouse già create in un'unica istruzione di prelievo, è necessario eliminare prima i singoli prelievi warehouse.

4. Compila il campo **Metodo di ordinamento** per ordinare le righe.  

    > [!NOTE]  
    >  Il modo in cui le righe vengono ordinate nel prospetto non si applica automaticamente all'istruzione di prelievo. Tuttavia, esistono le stesse opportunità per l'ordinamento e la valutazione collocazione. È possibile ricreare facilmente l'ordine delle righe pianificate nel prospetto quando crei le istruzioni di prelievo o le ordini nelle istruzioni di prelievo.

5. Compila il campo **Qtà. gestire** manualmente o utilizzando l'azione **Autocompil. qtà da gestire**.  

    La pagina mostra le quantità disponibili nelle collocazioni cross-dock. Queste informazioni sono utili per pianificare le assegnazioni del lavoro in situazioni di cross-dock. [!INCLUDE[prod_short](includes/prod_short.md)] proporrà sempre prima un prelievo da una collocazione cross-dock.
6. Le righe possono essere modificate, se necessario. È inoltre possibile eliminare le righe per creare un prelievo più efficiente. Se ad esempio vi sono più righe con articoli nelle collocazioni di cross-dock, puoi creare un prelievo per tutte le righe. Gli articoli sottoposti a cross-dock verranno spediti con agli altri articoli e nelle collocazioni di cross-dock sarà disponibile una maggiore quantità di spazio per ulteriori articoli in entrata.  

    > [!NOTE]  
    >  Quando elimini le righe, vengono eliminate solo dal prospetto. Non vengono eliminate dalla lista di selezione di prelievo.  

7. Scegliere l'azione **Crea prelievo**. Si apre la pagina **Crea prelievo**, dove puoi aggiungere ulteriori informazioni sul prelievo che stai creando. Specifica in che modo combinare le righe di prelievo nei documenti di prelievo selezionando una delle opzioni seguenti.  

    |Opzione|Descrizione|
    |-|-|
    |Per documento whse. Documento|Crea documenti di prelievo distinti per le righe del prospetto con lo stesso documento warehouse di origine.|
    |Per cliente/forn./ubicazione|Crea documenti di prelievo separati per ogni cliente (ordini di vendita), fornitore (ordini di reso acquisto) e ubicazione (ordini di trasferimento).|
    |Per articolo|Crea documenti di prelievo separati per ogni articolo nel prospetto prelievi.|
    |Per Da zona|Crea documenti di prelievo separati per ogni zona da cui verranno prelevati articoli.|
    |Per collocazione|Crea documenti di prelievo separati per ogni collocazione da cui verranno prelevati articoli.|
    |Per scadenza|Crea documenti di prelievo separati per i documenti di origine che hanno la stessa data di scadenza.|

    Specifica in che modo vengono creati i documenti di prelievo selezionando una delle opzioni seguenti.

    |Opzione|Descrizione|
    |-|-|
    |Importo massimo No. di righe prelievo|Crea documenti di prelievo con un numero di righe in ogni documento non superiore a quello specificato.|
    |Importo massimo No. di doc. origine prelievo|Crea documenti di prelievo che si riferiscono a un numero di documenti origine non superiore a quello specificato.|
    |ID utente assegnato|Crea documenti di prelievo solo per le righe del prospetto assegnate all'impiegato warehouse selezionato.|
    |Metodo di ordinamento per righe di prelievo|Scegli una delle opzioni disponibili per ordinare le righe nel documento di prelievo creato.|
    |Impostare filtro breakbulk|Nasconde le righe prelievo di breakbulk intermedie quando un'unità di misura più grande viene convertita in un'unità di misura più piccola e completamente prelevata.|
    |Qtà da gestire non compilata|Lascia il campo Qtà. da gestire vuoto nelle righe di prelievo create.|
    |Stampa prelievo|Stampa i documenti di prelievo al momento della creazione. È inoltre possibile stampare dai documenti di prelievo creati.|

8. Selezionare **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] creerà il prelievo in base alle tue selezioni.  

## Per prelevare articoli per una spedizione warehouse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prelievi warehouse**, quindi scegli il collegamento correlato.  

    Se è necessario utilizzare un determinato prelievo, selezionare il prelievo dalla lista oppure filtrare la lista per individuare i prelievi specificatamente assegnati a se stessi. Aprire la scheda prelievo.  
2. Se il campo **ID utente assegnato** è vuoto, immetti il tuo ID per identificarti, se necessario.  
3. Preleva gli articoli.  

    Se la warehouse prevede l'utilizzo di collocazioni, vengono utilizzate le collocazioni predefinite degli articoli per suggerire la posizione da cui prelevare gli articoli. Le istruzioni contengono almeno due righe distinte, una per ogni azione Prendere e Mettere.  

    Se la warehouse prevede l'utilizzo di stoccaggi e prelievi guidati, viene utilizzata la valutazione collocazione per calcolare le migliori collocazioni da cui effettuare il prelievo. Tali collocazioni vengono quindi suggerite nelle righe prelievo. Le istruzioni contengono almeno due righe distinte, una per ogni azione Prendere e Mettere.  

    * La prima riga, in cui il campo **Tipo azione** è impostato su **Prendere**, indica l'ubicazione degli articoli nell'area di prelievo. Se si spedisce un numero elevato di articoli in una riga di spedizione, potrebbe essere necessario prelevare gli articoli in diverse collocazioni, pertanto è presente una riga Prendere per ogni collocazione.
    * Nelle righe successive, in cui il campo **Tipo azione** è impostato su **Mettere**, viene indicata la posizione in cui inserire gli articoli nella warehouse. Non è possibile modificare la zona e la collocazione in questa riga.

    > [!NOTE]
    > Se è necessario prelevare o inserire gli articoli relativi a una riga in più collocazioni, ad esempio perché la collocazione designata è piena, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.

4. Dopo avere prelevato e posizionato gli articoli nell'area di spedizione o nella collocazione di spedizione, scegli l'azione **Registra prelievo**.  

Ora puoi immettere gli articoli al dock di spedizione e registrare la spedizione, incluso il documento di origine correlato, nella pagina **Spedizione warehouse**. Per ulteriori informazioni vedi [Spedire articoli](warehouse-how-ship-items.md).

## Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
