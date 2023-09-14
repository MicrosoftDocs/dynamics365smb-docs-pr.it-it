---
title: 'Ricevimento, stoccaggio, movimentazione, prelievo e spedizione in configurazione avanzata di magazzino con prelievo e stoccaggio diretti'
description: 'In Business Central, i processi in entrata e in uscita possono essere eseguiti in modalità differenti a seconda del livello di complessità della warehouse.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# Procedura dettagliata del flusso in entrata e in uscita nella configurazione avanzata del magazzino con stoccaggio e prelievo diretti

Questa procedura dettagliata illustra come completare i flussi in entrata e in uscita nella configurazione avanzata per stoccaggio e prelievo diretti. Per ulteriori informazioni, vedi [Panoramica delle diverse opzioni di configurazione](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Prerequisiti  
Per completare questa procedura, devi diventare un dipendente warehouse presso l'ubicazione *BIANCA* effettuando i seguenti passaggi:  
1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2. Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.  
3. Nel campo **Codice ubicazione** immettere BIANCO:  
4. Attiva l'interruttore **Predefinito**.


## Scenario  
Ellen, la responsabile del magazzino, utilizza la funzionalità di cross-dock e di rifornimento delle collocazioni per velocizzare i tempi di ricezione e spedizione.  

## Passaggi

1. Crea spedizione warehouse.  

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 2.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
    2. Seleziona l'ordine per il cliente 10000 per l'ubicazione BIANCA. Il numero dell'ordine esterno è *W-1*. Utilizza gli strumenti di personalizzazione se il campo **Numero d'ordine esterno** non è visibile. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](../../ui-personalization-user.md).
    3. Scegli l'azione **Crea spedizione warehouse** per creare una spedizione warehouse per l'ordine di vendita selezionato.
    4.  Scegli l'azione **Rilascia** per comunicare alla warehouse che la spedizione ordine di vendita è pronta per la gestione warehouse.  

2. Definire le collocazioni per l'articolo per controllare dove viene stoccato 

    1.  Scegli l'icona ![lampadina che apre la funzione Dimmi 3.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli** e scegli il collegamento correlato.  
    2.  Seleziona *WRB-1000* e scegli l'azione **Contenuto delle collocazioni**.  
    3.  Scegli l'azione **Nuovo**. Aggiungi due righe. Utilizza gli strumenti di personalizzazione se un campo **Codice collocazione** non è visibile. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](../../ui-personalization-user.md). 
    
    |Articolo|Cod. ubicazione|Codice collocazione|Fisso|Unità di misura|
    |----------|----------|---------|---|------|  
    |WRB-1000|BIANCO|W-05-0001|Sì|BORSA|  
    |WRB-1000|BIANCO|W-05-0002|Sì|BORSA|

3. Crea il carico warehouse.  

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
    2. Seleziona l'ordine del fornitore 10000 per l'ubicazione BIANCA. Il numero dell'ordine fornitore è *W-2*. Utilizza gli strumenti di personalizzazione se il campo **Numero ordine fornitore** non è visibile. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](../../ui-personalization-user.md).
    3. Scegli l'azione **Crea carico warehouse** per creare un carico warehouse per l'ordine di acquisto selezionato.


4. Controlla se ci sono ordini in uscita che richiedono articoli ricevuti e invia la ricevuta
    1. Scegliere l'azione **Calcola cross-dock**. Questo popolerà una colonna **Qtà. al cross-dock**.
    2. Inserisci 0 nel campo **Qtà. al cross-dock** nella riga con l'articolo *WRB-1000* poiché non prevedi di reimballare l'articolo nell'area di carico.
    3. Scegli l'azione **Registra carico**.

5. Registrare lo stoccaggio warehouse
    1. Usa l'icona ![lampadina che apre la funzione Dimmi 5.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggio warehouse**, quindi seleziona il collegamento correlato.
    2. Individua il documento di stoccaggio warehouse creato dalla ricevuta warehouse e aprilo
    3. Nella pagina **Stoccaggio warehouse** esamina la sezione **Righe**

    In questa fase, viene rivelata la logica della capacità della collocazione. Le righe di stoccaggio warehouse avranno tre righe per l'articolo *WRB-1000*:
    - Una riga Prendere per spostare le quantità ricevute dalla collocazione di ricezione (W-08-0001)
    - Una riga Mettere che sposterà un contenitore in una delle collocazioni fisse configurate (W-05-0001)
    - Una riga Mettere che sposterà un altro contenitore in altre collocazioni fisse (W-05-0002). Ciò perché una singola collocazione fissa non può contenere l'intera quantità di carico.

    Poiché questo stoccaggio contiene righe di cross-dock, verranno visualizzate tre righe per l'articolo *WRB-1001*:
    -  Una riga Prendere per spostare le quantità ricevute dalla collocazione di ricezione (W-08-0001)
    -  Una riga Mettere per il 2 nella collocazione del cross-dock
    -  Una riga Mettere per la quantità rimanente nella collocazione di stoccaggio

    4. Seleziona l'azione **Registra stoccaggio**.


6. Definire le collocazioni di prelievo per l'articolo per controllare da dove viene prelevato 

    1.  Scegli l'icona ![lampadina che apre la funzione Dimmi 6.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
    2.  Aprire la scheda ubicazione *BIANCA*.  
    3.  Scegli l'azione **Collocazioni** nella **Scheda ubicazione**
    4.  Seleziona la collocazione *W-02-0001* e scegli l'azione **Contenuto**.  
    5.  Scegli l'azione **Nuovo**.  
    6.  Attiva l'interruttore **Fisso**.  
    7.  Nel campo **Nr. articolo** immetti *WRB-1000*. 
    8.  Nel campo **Quantità minima** immetti *2*. 
    9.  Nel campo **Quantità massima** immetti *10*. 

    Utilizza gli strumenti di personalizzazione se i campi **Quantità minima** e **Quantità massima** non sono visibili. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](../../ui-personalization-user.md). 

7. Riorganizza il magazzino spostando gli articoli dall'area di stoccaggio in blocco all'area di prelievo, per ottimizzare i tempi di prelievo.

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 7.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetti movimentazioni**, quindi scegli il collegamento correlato
    2. Sceliere l'azione **Calcola rifornimento collocazione**. 

    Viene creato il prospetto warehouse con la proposta sullo spostamento dell'articolo *WRB-1000* dall'area di stoccaggio in blocco all'area di prelievo.

    3. Scegli l'azione **Crea movimento** e conferma di voler creare il documento.
    4.  Scegli l'icona ![lampadina che apre la funzione Dimmi 8.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti warehouse**, quindi scegli il collegamento correlato
    5.  Apri il movimento warehouse che hai creato, esamina la sezione **Righe**

     In questa fase, viene rivelata la funzionalità di breakbulk. Ci saranno quattro righe:
    - Una riga per Prendere l'unico contenitore dalla collocazione di stoccaggio in blocco
    - Una riga per Mettere a magazzino i 48 PZ nella stessa collocazione. 
    - Una riga per Prendere i 10 PZ dalla collocazione di stoccaggio in blocco
    - Una riga per Mettere i 10 PZ nella collocazione di prelievo

    6.  Seleziona l'azione **Registra movimento**.

8. Creare i prelievi warehouse

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 9.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetti prelievi**, quindi scegli il collegamento correlato
    2. Scegli l'azione **Ottieni documenti magazzino** seleziona la riga per l'ordine di vendita per il cliente 10000, quindi scegli il pulsante **OK** per compilare le righe del prospetto in base al documento selezionato.

    3. Ispeziona il campo **Qtà in collocazione cross-dock**. 

    4. Scegliere l'azione **Crea prelievo**.
    5. Conferma una qualsiasi delle impostazioni di prelievo necessarie, ad esempio abilita l'interruttore **Per zona di partenza**. Scegli il pulsante **OK**.
    
    Riceverai un messaggio di conferma con i numeri di prelievo. Ci sono due prelievi in quanto alcuni articoli si trovano nella zona di cross-dock, vicino all'area di spedizione, e avrebbe senso elaborarli separatamente.

9.  Registrare i prelievi warehouse
    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 10.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi warehouse**, quindi scegli il collegamento correlato.
    2. Individua i prelievi che hai creato e aprili.
    3. Scegliere l'azione **Registra prelievo**.
    4. Ripeti per il secondo prelievo

10. Registrare la spedizione warehouse
    
    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 11.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizione warehouse**, quindi scegli il collegamento correlato.
    2. Nella pagina spedizione warehouse esamina la sezione **Righe**. Dopo che il prelievo in magazzino è stato registrato, la spedizione warehouse verrà aggiornata con la **Qtà. da spedire** compilata.
    3. Scegli l'azione **Registra spedizione**.
    4. Conferma l'opzione **Spedisci**.


## Risultati
- Viene creato il **carico warehouse registrato**
- Viene creato lo **stoccaggio warehouse registrato**    
- Viene creato il **carico acquisto registrato**    
- Viene aggiornata la **Quantità ricevuta** dell'**Ordine di acquisto** per le righe ricevute
- Viene creato il **movimento warehouse registrato**
- Viene creato il **prelievo warehouse registrato**
- Viene creata la **spedizione warehouse registrata**
- Viene creata la **spedizione vendita registrata**
- Viene aggiornata la **Quantità spedita** dell'**Ordine di vendita** per le righe spedite
- Viene aumentato l'articolo **Inventario** di eventuali rimanenze non spedite



## Vedere anche
[Ricevere articoli](../../warehouse-how-receive-items.md) 
[Dettagli di progettazione: flusso di magazzino in entrata](../../design-details-inbound-warehouse-flow.md) 
[Spedizione articoli](../../warehouse-how-ship-items.md) 
[Prelievo articoli per spedizione magazzino](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Dettagli di progettazione: flusso di magazzino in uscita](../../design-details-outbound-warehouse-flow.md) 
[Visualizzare la disponibilità degli articoli](../../inventory-how-availability-overview.md) 
