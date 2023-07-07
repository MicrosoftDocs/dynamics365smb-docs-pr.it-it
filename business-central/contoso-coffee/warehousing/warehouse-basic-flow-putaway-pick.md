---
title: 'Carico, stoccaggio, prelievo e spedizione nella configurazione magazzino di base'
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

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a>Procedura dettagliata del flusso in entrata e in uscita nelle configurazioni di warehouse di base

Questa procedura dettagliata illustra come completare i flussi in entrata e in uscita nella configurazione di base per ordine per ordine. Per ulteriori informazioni, vedi [Panoramica delle diverse opzioni di configurazione](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Prerequisiti
Per completare questa procedura, devi diventare un dipendente warehouse presso l'ubicazione *ARGENTO* effettuando i seguenti passaggi:  
1. Scegli l'icona ![lampadina che apre la funzione Dimmi 1.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2. Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.  
3. Nel campo **Codice ubicazione** immetti *ARGENTO*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Flusso in entrata: ricezione e stoccaggio nelle configurazioni di warehouse di base

In [!INCLUDE[prod_short](../../includes/prod_short.md)], i processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Carichi|Stoccaggi|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|X|||2|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino|||X|3|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse||X||5/4/6|  
|D|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse||X|X|5/4/6|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in entrata](../../design-details-inbound-warehouse-flow.md).  

Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.  

### <a name="scenario"></a>Scenario
Alicia, l'agente di acquisto, crea un ordine di acquisto per diversi chicchi tostati. Quando la consegna arriva al magazzino, John, il magazziniere, ripone gli articoli in collocazioni adatte. Quando John registra lo stoccaggio, gli articoli vengono registrati come ricevuti in magazzino e disponibili per la vendita o altra domanda.  

### <a name="steps"></a>Passaggi
1. Imposta la pagina **Scheda ubicazione** per definire i flussi della warehouse in entrata della società.  

    1.  Scegli l'icona ![lampadina che apre la funzione Dimmi 2.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
    2.  Apri la scheda ubicazione *ARGENTO*.  
    3.  Selezionare la casella di controllo **Richiesto stoccaggio**.  

2. Definisci una collocazione predefinita per l'articolo per controllare dove viene stoccato

    1.  Scegli l'azione **Collocazioni** nella **Scheda ubicazione**
    2.  Seleziona la prima riga, per la collocazione *S-1-01*, quindi scegli l'azione **Contenuti**.  
    3.  Scegli l'azione **Nuovo**.  
    4.  Selezionare i campi **Fisso** e **Default**.  
    5.  Nel campo **Nr. articolo** immetti *WRB-1000*.  

3. Crea l'ordine di acquisto, che è il tipo più comune di documenti origine in entrata.  

    1.  Scegli l'icona ![lampadina che apre la funzione Dimmi 3.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
    2.  Scegli l'azione **Nuovo**.  
    3.  Crea un ordine di acquisto per il fornitore 10000 con le righe di ordine di acquisto seguenti. Utilizza gli strumenti di personalizzazione se un campo **Codice collocazione** non è visibile. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](../../ui-personalization-user.md). 

    |Articolo|Cod. ubicazione|Codice collocazione|Quantità|  
    |----------|----------|---------|--------------|  
    |WRB-1000|ARGENTO|S-1-01|20|  
    |WRB-1001|ARGENTO||30|

    Il codice collocazione nel primo viene compilato di conseguenza per l'impostazione. Il codice collocazione per il secondo articolo è vuoto in quanto non ha valori predefiniti. Tienilo così.  

    4.  Scegli l'azione **Rilascia** per comunicare alla warehouse che l'ordine di acquisto è pronto per la gestione warehouse al momento della consegna.  

4. Crea lo **Stoccaggio in magazzino** per ricevere e stoccare gli articoli consegnati  

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 4.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggi magazzino**, quindi seleziona il collegamento correlato.  
    2. Scegli l'azione **Nuovo**. 
    3. Nel campo *Codice ubicazione* seleziona **ARGENTO**.
    4. Selezionare il campo **Documento origine**, quindi selezionare **Ordine acquisto**.  
    5. Seleziona il campo **Nr. origine**, seleziona la riga per l'acquisto dal fornitore 10000, quindi scegli il pulsante **OK** per riempire le righe di stoccaggio in base al documento di origine selezionato.

        In alternativa, scegliere l'azione **Prendi documento origine**, quindi selezionare l'ordine di acquisto.  

5. Modificare lo stoccaggio in magazzino in base al posizionamento effettivo degli articoli e al documento di registrazione

    Quando ha inserito gli articoli nelle collocazioni, John ha notato che la collocazione predefinita contiene già alcuni articoli, quindi ha deciso di utilizzare un'altra collocazione. John colloca anche altri articoli nelle collocazioni successive, poiché la quantità ricevuta non è adatta alla capacità.

    1. Nella prima riga modifica **Codice collocazione** da *S-1-01*, che è stato copiato dall'ordine di acquisto, a *S-1-02*. 
    2.  Immetti 20 nel campo **Qtà. da gestire** nella riga di stoccaggio magazzino con l'articolo WBR-1000.  
    3. Nella seconda riga, inserisci 20 nel campo **Qtà da gestire** e scegli l'azione **Dividi riga**. Verrà visualizzata una nuova riga, costituita da una copia di quella originale tranne per il fatto che il campo **Qtà da gestire** contiene il valore sottratto dalla riga originale. 
    4. Compila i codici collocazione per l'articolo WBR-1001:

    |Articolo|Codice collocazione|Quantità|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Scegliere l'azione **Registra**, selezionare l'azione **Ricevi**, quindi il pulsante **OK**.  

### <a name="results"></a>Risultati
 - I chicchi tostati sono ora registrati come stoccati in collocazioni specifiche
 - Viene creato lo **stoccaggio magazzino registrato**
 - Viene creato il **carico acquisto registrato**
 - Viene aggiornata la **Quantità ricevuta** dell'ordine di acquisto per le righe ricevute
 - Viene aumentato l'articolo **Inventario** della quantità scelta
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a>Flusso in uscita: prelievo e spedizione nelle configurazioni di warehouse di base

In [!INCLUDE[prod_short](../../includes/prod_short.md)], i processi in uscita per il prelievo e la spedizione possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.  

|Metodo|Processo in entrata|Collocazioni|Prelievi|Spedizioni|Livello di complessità (vedere [Dettagli di progettazione: Setup warehouse](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registra prelievo e spedizione dalla riga ordine|X|||2|  
|B|Registra prelievo e spedizione da un documento di prelievo magazzino||X||3|  
|C|Registra prelievo e spedizione da un documento di spedizione warehouse|||X|5/4/6|  
|D|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse||X|X|5/4/6|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in uscita](../../design-details-outbound-warehouse-flow.md).  

Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.

### <a name="scenario-1"></a>Scenario
Susan, la responsabile degli ordini, crea un ordine di vendita per vari chicchi tostati e lo passa al magazzino. Gianni, il lavoratore warehouse deve assicurarsi che la spedizione sia preparata e consegnata al cliente. Gianni gestisce tutte le attività interessate nella pagina **Prelievo magazzino** che automaticamente punta alle collocazioni in cui vengono archiviati i chicchi tostati.

### <a name="steps-1"></a>Passaggi
Questa è la continuazione di [Flusso in entrata: ricezione e stoccaggio nelle configurazioni di warehouse di base](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Imposta la pagina **Scheda ubicazione** per definire i flussi della warehouse in entrata della società.  

    1.  Scegli l'icona ![lampadina che apre la funzione Dimmi 5.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
    2.  Apri la scheda ubicazione *ARGENTO*.  
    3.  Selezionare la casella di controllo **Richiesto prelievo**.  

2. Crea l'ordine di vendita, che è il tipo più comune di documenti origine in uscita.  

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 6.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
    2. Scegli l'azione **Nuovo**.  
    3. Crea un ordine di vendita per il cliente 10000 con la seguente riga ordine di vendita.  

    |Articolo|Cod. ubicazione|Quantità|  
    |----|-------------|--------|  
    |WRB-1000|ARGENTO|20|  
    |WRB-1001|ARGENTO|30|  

    I codici collocazione vengono popolati automaticamente con le collocazioni predefinite.

    4. Scegli l'azione **Crea stoccaggio/prelievo di magazzino**.
    5. Selezionare la casella di controllo **Crea prelievo mag.**.  
    6. Scegli il pulsante **OK**. Verrà creato un nuovo prelievo magazzino.

3. Prelevare e spedire gli articoli

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi 7.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi magazzino**, quindi scegli il collegamento correlato.  
    2. Seleziona il prelievo da magazzino per le vendite al cliente 10000
    
    Il prelievo da magazzino creato ha ignorato la collocazione definita per l'articolo *WRB-1000*, in quanto non contiene scorte e ha utilizzato un'altra collocazione. La seconda riga, con l'articolo *WRB-1001* è stata automaticamente suddivisa per prelevare da più collocazioni.
    
4. Scegliere l'azione **Autocompil. qtà da gestire**.  

5. Scegliere l'azione **Registra**, selezionare **Spedizione**, quindi scegliere il pulsante **OK**.  

### <a name="results-1"></a>Risultati
 - I chicchi tostati sono ora registrati come prelevati da collocazioni specifiche
 - Viene creato il **prelievo magazzino registrato**
 - Viene creata la **spedizione vendita registrata**
 - Viene aggiornata la **Quantità spedita** dell'ordine di vendita per le righe spedite
 - Viene diminuito l'articolo **Inventario** della quantità scelta


## <a name="see-also"></a>Vedere anche
[Articoli stoccati con stoccaggi magazzino](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Impostare magazzini di base con aree operative](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Dettagli di progettazione: flusso di magazzino in entrata](../../design-details-inbound-warehouse-flow.md) 
[Prelevare articoli con prelievi inventario](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Dettagli di progettazione: flusso di magazzino in uscita](../../design-details-outbound-warehouse-flow.md) 
[Visualizzare la disponibilità degli articoli](../../inventory-how-availability-overview.md) 
