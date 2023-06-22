---
title: Panoramica dei processi della warehouse in uscita
description: Questo articolo descrive il flusso di lavoro della warehouse in uscita.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes" />Processi della warehouse in uscita

I processi in uscita nelle warehouse iniziano quando si rilascia un documento di origine per prelevare gli articoli da un'ubicazione warehouse. Ad esempio, per spedire gli articoli da qualche parte o per spostarli in un'altra sede della società. In linea di principio, il processo di spedizione degli ordini in uscita consiste in due attività:

* Prelevare gli articoli dagli scaffali.
* Spedire gli articoli fuori dalla warehouse.

I documenti di origine per il flusso di warehouse in uscita sono:  

* Ordine di vendita  
* Ordine di trasferimento in uscita  
* Ord. reso di acquisto  
* Ordine assistenza  

> [!NOTE]
> Anche gli ordini di produzione e di assemblaggio con componenti rappresentano documenti di origine in uscita. Gli ordini di produzione e di assemblaggio sono leggermente diversi perché sono in genere processi interni che non comportano la spedizione. Vengono invece utilizzati per stoccare articoli prodotti o spostare i componenti necessari per assemblare un articolo in un'area di assemblaggio. Per ulteriori informazioni su questi processi vedi [Dettagli di progettazione: Flussi warehouse interni](design-details-internal-warehouse-flows.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)], il prelievo e la spedizione degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in uscita|Richiesto prelievo|Richiesta spedizione|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registra il prelievo e la spedizione dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registra il prelievo e la spedizione da un documento di prelievo magazzino|Attivato||Di base: ordine per ordine.|  
|C|Registra il prelievo e la spedizione da un documento di spedizione warehouse||Attivato|Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse|Attivato|Attivato|Avanzate|  

L'approccio da scegliere dipende dalle procedure della warehouse e dal livello di complessità organizzativa. Di seguito sono riportati alcuni esempi che potrebbero aiutarti a decidere.

* In un ambiente di ordine per ordine con processi chiari e una struttura di collocazione semplice, il metodo A, il prelievo e la spedizione dalla riga ordine è appropriato.
* Se gli articoli per una riga ordine provengono da più di una collocazione o se gli addetti warehouse non possono lavorare con i documenti dell'ordine, è appropriato l'utilizzo di documenti di prelievo separati, metodo B.
* Se i processi di prelievo e spedizione coinvolgono più ordini e richiedono maggiore controllo e visione, è possibile scegliere di utilizzare un documento di spedizione warehouse e un documento di prelievo warehouse per separare le attività di prelievo e spedizione, metodi C e D.  

Nei metodi A, B e C, le attività di prelievo e di spedizione sono combinate in un unico passaggio quando si registra un documento come spedito. Nel metodo D, il prelievo viene registrato per primo e la spedizione viene registrata successivamente da un documento diverso.

> [!NOTE]
> Sebbene i prelievi warehouse e i prelievi di magazzino sembrino simili, i documenti sono diversi e vengono utilizzati in processi diversi.
> * Il prelievo di magazzino utilizzato nel metodo B, insieme alla registrazione delle informazioni di prelievo, registra anche la spedizione del documento di origine.
> * Il prelievo warehouse utilizzato nel metodo D non può essere registrato e registra solo il prelievo. La registrazione rende gli articoli disponibili per la spedizione warehouse ma non registra la spedizione. Nel flusso in uscita, il prelievo warehouse richiede una spedizione warehouse.

## <a name="no-dedicated-warehouse-activity" />Nessuna attività di warehouse dedicata

I seguenti articoli forniscono informazioni su come elaborare le ricevute per i documenti di origine se non sono disponibili attività di magazzino dedicate.

* [Vendere prodotti](sales-how-sell-products.md)
* [Ordini di trasferimento](inventory-how-transfer-between-locations.md)
* [Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md)
* [Creare ordini di assistenza](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations" />Configurazioni warehouse di base

Nel diagramma seguente vengono illustrati i processi warehouse in uscita per diversi tipi di documenti nelle configurazioni warehouse di base. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Mostra i passaggi in un flusso in uscita di base in una warehouse.":::

### <a name="-release-a-source-document" />1: Rilasciare un documento di origine

Quando usi l'azione **Rilascia** su un documento di origine, ad esempio un ordine di vendita o di trasferimento, gli articoli nel documento sono pronti per essere movimentati nella warehouse. Ad esempio, prelevati e stoccati nella collocazione specificata nel documento. In alternativa, puoi creare documenti di prelievo magazzino per le singole righe di ordini, in modalità push, in base alle collocazioni specificate e le quantità da gestire.  

### <a name="-create-an-inventory-pick" />2: Creare un prelievo di magazzino

Nella pagina **Prelievo magazzino** l'addetto al magazzino recupera, in modalità pull, le righe del documento di origine. In alternativa, le righe di prelievo magazzino sono già create, in modalità push, dall'utente responsabile del documento di origine.  

### <a name="-post-an-inventory-pick" />3: Registrare un prelievo di magazzino

In ogni riga per gli articoli che sono stati prelevati o spostati, in parte o completamente, compila il campo **Quantità**, quindi registra il prelievo di magazzino. I documenti di origine correlati al prelievo magazzino vengono registrati come spediti o consumati.  

Per i prelievi di magazzino vengono creati i movimenti contabili articoli negativi e i movimenti warehouse e viene eliminata la richiesta di prelievo, se completamente gestita. Ad esempio, il campo **Quantità spedita** nella riga del documento di origine in entrata viene aggiornato. Viene creato un documento di spedizione registrato che corrisponde all'ordine di vendita, ad esempio, e agli articoli spediti.  

## <a name="advanced-warehouse-configurations" />Configurazioni avanzate della warehouse

Nel diagramma seguente vengono illustrati i processi warehouse in uscita per diversi tipi di documenti nelle configurazioni warehouse avanzata. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Mostra i passaggi in un flusso in uscita in una warehouse avanzata.":::

### <a name="-release-a-source-document" />1: Rilasciare un documento di origine

Il rilascio di un documento di origine nelle configurazioni avanzate è uguale a quello delle configurazioni di base. Gli articoli diventano disponibili per la movimentazione nella warehouse. Ad esempio, possono essere inclusi in una spedizione.  

### <a name="-create-a-warehouse-shipment" />2: Creare una spedizione warehouse

Nella pagina **Spedizione warehouse** ottieni le righe dal documento di origine rilasciato. Puoi combinare le righe di più documenti di origine in un'unica spedizione warehouse.  

### <a name="-create-a-warehouse-pick" />3: Creare un prelievo warehouse

Nella pagina **Spedizione warehouse** crea le attività di prelievo warehouse per le spedizioni warehouse in uno dei due seguenti modi:

- In modalità push, dove utilizzi l'azione **Crea prelievo**. Seleziona le righe da prelevare e prepara i prelievi specificando, ad esempio, le collocazioni da cui prelevare, quelle in cui inserire e il numero di unità da gestire. Le collocazioni possono essere predefinite per l'ubicazione o la risorsa warehouse.
- In modalità pull, dove utilizzi l'azione **Rilascia**. Nella pagina **Prospetto prelievi**, i dipendenti della warehouse possono utilizzare l'azione **Prendi documenti warehouse** per ottenere i prelievi assegnati. Una volta registrati i prelievi della warehouse, le righe nel **Prospetto prelievi** vengono eliminate.

### <a name="-register-a-warehouse-pick" />4: Registrare un prelievo warehouse

Nella pagina **Prelievo warehouse** l'addetto alla warehouse compila il campo **Quantità** per ogni riga che ha prelevato in tutto o in parte, quindi registra il prelievo.

I movimenti warehouse vengono creati e le righe di prelievo warehouse vengono eliminate, se la quantità è stata completamente prelevata. Il documento di prelievo warehouse rimane aperto fino a quando la quantità completa della spedizione warehouse non viene registrata. Il campo **Qtà prelevata** nelle righe di spedizione warehouse viene aggiornato di conseguenza.  

### <a name="-post-the-warehouse-shipment" />5: Registrare la spedizione warehouse

Una volta che tutti gli articoli nel documento di spedizione warehouse sono registrati come prelevati, l'addetto alla warehouse registra la spedizione. La registrazione aggiorna i movimenti contabili articolo per riflettere la riduzione delle scorte. Ad esempio, il campo **Quantità spedita** nella riga del documento di origine in entrata viene aggiornato.  

## <a name="see-also" />Vedere anche

[Warehouse Management](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
