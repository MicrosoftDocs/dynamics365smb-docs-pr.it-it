---
title: 'Carico, stoccaggio, prelievo e spedizione nella configurazione magazzino mista'
description: 'In Business Central, i processi in entrata e in uscita possono essere eseguiti in modalità differenti a seconda del livello di complessità della warehouse.'
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a>Procedura dettagliata del flusso in entrata e in uscita nelle configurazioni di warehouse miste

Questa procedura dettagliata illustra come completare i flussi in entrata e in uscita in una configurazione mista, in cui per il flusso in entrata il magazzino è configurato come Base: ordine per ordine e per il flusso in uscita viene utilizzata la configurazione Avanzata. Per ulteriori informazioni, vedi [Panoramica delle diverse opzioni di configurazione](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Prerequisiti
Per completare questa procedura, devi diventare un dipendente warehouse presso l'ubicazione *GIALLA* effettuando i seguenti passaggi:  
1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2. Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.  
3. Nel campo **Codice ubicazione** immetti *GIALLA*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Flusso in entrata: ricezione e stoccaggio nelle configurazioni di warehouse di base

In [!INCLUDE[prod_short](../../includes/prod_short.md)], i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Carichi|Stoccaggi|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|X|||2|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino|||X|3|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse||X||5/4/6|  
|D|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse||X|X|5/4/6|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in entrata](../../design-details-inbound-warehouse-flow.md).  

Nella seguente procedura dettagliata viene dimostrato il metodo C nella tabella precedente.  

### <a name="scenario"></a>Scenario
Alicia, l'agente di acquisto, crea un ordine di acquisto per diversi chicchi tostati della domanda. Quando la consegna combinata arriva alla warehouse, Gianni, il lavoratore warehouse, riceve ed esegue lo stoccaggio degli articoli. Quando Gianni registra la ricevuta, gli articoli vengono registrati come ricevuti nel magazzino e disponibili alla vendita o a un'altra domanda.  

### <a name="steps"></a>Passaggi
1. Imposta la pagina **Scheda ubicazione** per definire i flussi della warehouse in entrata della società.  

    1.  Scegli l'icona ![lampadina che apre la funzione Dimmi 2.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
    2.  Apri la scheda ubicazione *GIALLA*.  
    3.  Disabilita l'interruttore **Richiesto stoccaggio**.  

2. Rilascia gli ordini di acquisto alla warehouse.  

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 3.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
    2. Seleziona gli ordini del fornitore 10000 per l'ubicazione GIALLA. I numeri degli ordini fornitore sono *Y-1* e *Y-2*. Utilizza gli strumenti di personalizzazione se il campo **Numero ordine fornitore** non è visibile. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](../../ui-personalization-user.md).
    3. Scegli l'azione **Rilascia** per comunicare alla warehouse che gli ordini di acquisto selezionati sono pronti per la gestione warehouse al momento della consegna.  

3. Creare il carico warehouse per ricevere e stoccare gli articoli consegnati
    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Carichi warehouse**, e seleziona il collegamento correlato.
    2. Scegli l'azione **Nuovo**
    3. Nella pagina del carico warehouse premi Invio per selezionare automaticamente un numero di carico warehouse
    4. Nel campo **Codice ubicazione** immetti *GIALLA*.
    5. Scegli l'azione **Prendi documenti origine...**
    6. Seleziona gli ordini di acquisto rilasciati in precedenza dal fornitore 10000 e scegli il pulsante **OK**.
        Le righe conterranno una nuova voce per ogni riga dell'ordine di acquisto.

4. Rettificare la quantità nella ricevuta in base alla quantità ricevuta e al documento postale
    1. Seleziona la riga con l'articolo *WRB-1000*.
    2. Seleziona *OVERRCPT10* nel campo **Codice ricevuta in eccesso** e modifica il valore nel campo **Quantità da ricevere** da *100* a *110*.
    3. Seleziona la riga con l'articolo *WRB-1001* 
    4. Nella seconda riga cambia il valore del campo **Quantità da ricevere** da *200* a *190*.
    5. Scegli l'azione **Registra carico**.

### <a name="results"></a>Risultati
 - I chicchi tostati sono ora registrati come stoccati
 - Viene creato il **carico warehouse registrato**
 - Viene creato il **carico acquisto registrato**
 - Viene aggiornata la **Quantità ricevuta** dell'ordine di acquisto per le righe ricevute
 - Viene aumentato l'articolo **Inventario** della quantità scelta
    

## <a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a>Flusso in uscita: prelievo e spedizione nelle configurazioni di warehouse avanzate

In [!INCLUDE[prod_short](../../includes/prod_short.md)], i processi in uscita per il prelievo e la spedizione possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Prelievi|Spedizioni|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registra prelievo e spedizione dalla riga ordine|X|||2|  
|B|Registra prelievo e spedizione da un documento di prelievo magazzino||X||3|  
|C|Registra prelievo e spedizione da un documento di spedizione warehouse|||X|5/4/6|  
|D|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse||X|X|5/4/6|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in uscita](../../design-details-outbound-warehouse-flow.md).  

Nella seguente procedura dettagliata viene dimostrato il metodo D nella tabella precedente.

### <a name="scenario-1"></a>Scenario
Elisabetta, la responsabile degli ordini, crea gli ordini di vendita per vari chicchi tostati e li passa al magazzino. Poiché tutti gli ordini provengono dallo stesso cliente, Ellen, la responsabile del magazzino, decide di spedirli insieme. Gianni, il lavoratore warehouse deve assicurarsi che la spedizione sia preparata e consegnata al cliente.

### <a name="steps-1"></a>Passaggi
Questa è la continuazione di [Flusso in entrata: ricezione e stoccaggio nelle configurazioni di warehouse di base](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Rilascia gli ordini di vendita alla warehouse.  

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 5.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
    2. Seleziona gli ordini per il cliente 10000 per l'ubicazione GIALLA. I numeri degli ordini esterni sono *Y-3*, *Y-4*, e *Y-5*. Utilizza gli strumenti di personalizzazione se il campo **Numero d'ordine esterno** non è visibile. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](../../ui-personalization-user.md).
    3. Scegli l'azione **Rilascia** per comunicare alla warehouse che gli ordini di vendita selezionati sono pronti per la gestione warehouse.  

2. Per spedire gli articoli  
    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 6.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizioni warehouse**, quindi scegli il collegamento correlato.  
    2. Scegli l'azione **Nuovo**.  
    3. Nel campo **Codice ubicazione** immetti *GIALLA*.  
    4. Scegliere l'azione **Usa filtri per richiamare doc. orig.**.  
    5. Nel campo **Codice** immetti **CUST10000**.  
    6. Nel campo **Descrizione** immetti **Cliente 10000**.  
    7. Scegliere l'azione **Modifica**.  
    8. Nella Scheda dettaglio **Vendite**, nel campo **Filtro Vendere a - Nr. cliente**, immetti *10000*.  
    9. Scegliere l'azione **Esegui**. 
    
    La spedizione warehouse viene compilato con quattro righe che rappresentano le righe ordine di vendita per il cliente specificato. Il campo **Qtà. da spedire** è vuoto perché gli articoli devono essere prelevati prima.

3. Creare il prelievo warehouse dalla spedizione warehouse
    1. Nella pagina spedizione warehouse scegli l'azione **Crea prelievo**.
    2. Conferma una qualsiasi delle impostazioni di prelievo necessarie, ad esempio, seleziona *Articolo* nel campo **Metodo di ordinamento per riga attività** per raggruppare gli stessi articoli insieme. Scegli il pulsante **OK**.
    3. Riceverai un messaggio di conferma con il numero di prelievo. 

4. Aprire il prelievo warehouse
    1. Usa l'icona ![lampadina che apre la funzione Dimmi 7.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi warehouse**, quindi scegli il collegamento correlato.
    2. Individua il prelievo che hai creato e aprilo.
    3. Aggiorna la **Qtà. da gestire** se necessario.
    4. Scegliere l'azione **Registra prelievo**.
    5. Il prelievo warehouse verrà chiuso e rimosso se tutte le quantità vengono gestite.

5. Registrare la spedizione warehouse
   1. Scegli l'icona ![lampadina che apre la funzione Dimmi 8.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizioni warehouse**, quindi scegli il collegamento correlato.  
   2. Individua la spedizione che hai creato e aprila.
    Nota che **Qtà. da spedire** è compilata.
    3. È possibile aggiornare **Data di registrazione**, **Numero documento esterno**, **Codice spedizioniere**, **Metodo di spedizione**, se necessario. I valori non vuoti verranno propagati ai documenti di origine.
    4. Scegli l'azione **Registra spedizione**.
    5. Conferma l'opzione **Spedisci**.

### <a name="results-1"></a>Risultati
 - I chicchi tostati sono ora registrati come prelevati 
 - Viene creato il **prelievo warehouse registrato**
 - Viene creata la **spedizione warehouse registrata**
 - Vengono create le tre **spedizioni vendita registrate**
 - Viene aggiornata la **Quantità spedita** dell'ordine di vendita per le righe spedite
 - Viene diminuito l'articolo **Inventario** della quantità scelta


## <a name="see-also"></a>Vedere anche
[Ricevere articoli](../../warehouse-how-receive-items.md)
[Impostare le warehouse di base con aree di operazioni](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Dettagli di progettazione: flusso di magazzino in entrata](../../design-details-inbound-warehouse-flow.md)
[Spedizione articoli](../../warehouse-how-ship-items.md)
[Prelievo articoli per spedizione magazzino](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Dettagli di progettazione: flusso di magazzino in uscita](../../design-details-outbound-warehouse-flow.md)
[Visualizzare la disponibilità degli articoli](../../inventory-how-availability-overview.md)
