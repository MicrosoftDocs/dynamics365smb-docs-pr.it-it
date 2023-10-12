---
title: Prelievo e spedizione nelle configurazioni della warehouse di base
description: Questo articolo descrive vari livelli di complessità nei processi di prelievo e spedizione.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---
# Procedura dettagliata: prelievo e spedizione nelle configurazioni della warehouse di base

In [!INCLUDE[prod_short](includes/prod_short.md)], il prelievo e la spedizione degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in uscita|Richiesto prelievo|Richiesta spedizione|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Registra il prelievo e la spedizione dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registra il prelievo e la spedizione da un documento di prelievo magazzino|Attivato||Di base: ordine per ordine.|  
|C|Registra il prelievo e la spedizione da un documento di spedizione warehouse||Attivato|Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registra il prelievo da un documento di prelievo warehouse e la spedizione da un documento di spedizione warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni vedi [Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md).

Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.  

## Informazioni sulla procedura dettagliata

Nelle configurazioni della warehouse di base in cui un'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, utilizzare la pagina **Prelievi magazzino** per registrare le informazioni riguardanti il prelievo e la spedizione per i documenti di origine in uscita. Il documento di origine in uscita può essere un ordine di vendita, un ordine di reso da acquisto, un ordine di trasferimento in uscita o un ordine di produzione i cui componenti sono necessari.  

In questa procedura dettagliata sono illustrati i task seguenti:  

- Impostazione ubicazione SUD per i prelievi magazzino.  
- Creazione di un ordine di vendita per il cliente 10000 per 30 Lampade Amsterdam.  
- Rilascio dell'ordine di vendita per la gestione warehouse.  
- Creazione di un prelievo di magazzino in base al documento origine rilasciato.  
- Registrazione della movimentazione warehouse dalla warehouse e registrazione contemporanea della spedizione vendita per l'ordine di vendita di origine.  

## Ruoli

Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

- Manager warehouse  
- Gestore ordini  
- Lavoro warehouse  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## Scenario

Ellen, responsabile warehouse presso CRONUS, imposta la warehouse SUD per la gestione dei prelievi di base in cui gli addetti alla warehouse elaborano ordini in uscita singoli. Elisabetta, il gestore ordini, crea un ordine di vendita per 30 unità dell'articolo 1928-S da spedire al cliente 10000 dalla warehouse SUD. Gianni, il lavoratore warehouse deve assicurarsi che la spedizione sia preparata e consegnata al cliente. Gianni gestisce tutte le attività interessate nella pagina **Prelievo magazzino** che automaticamente punta alle collocazioni in cui viene archiviato 1928-S.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### Impostazione dei codici collocazione

Una volta impostata la posizione, è necessario aggiungere due contenitori.

#### Per impostare i codici collocazione

1. Scegliere l'azione **Collocazioni**.
2. Crea due contenitori, con i codici *S-01-0001* e *S-01-0002*.

### Diventare un impiegato warehouse presso l'ubicazione SUD

Per utilizzare questa funzionalità, devi aggiungerti all'ubicazione come lavoratore warehouse. 

#### Per diventare un impiegato warehouse

  1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni 1.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
  2. Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Impiegati warehouse**.
  3. Nel campo **Codice ubicazione** selezionare SUD.  
  4. Selezionare il campo **Impostazione predefinita**, quindi selezionare il pulsante **Sì**.  

### Rendere disponibile l'articolo 1928-S

Per rendere l'articolo 1928-S disponibile nell'ubicazione SUD seguire i passaggi di seguito riportati:  

  1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni 2.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni articoli**, quindi scegli il collegamento correlato.  
  2. Aprire il giornale di default e quindi creare due righe registrazioni magazzino con le informazioni seguenti sulla data di lavoro (23 gennaio).  

        |Tipo movimento|Numero di articolo|Cod. ubicazione|Codice collocazione|Quantità|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Rettifica positiva|1928-S|SUD|S-01-0001|20|  
        |Rettifica positiva|1928-S|SUD|S-01-0002|20|  

        Per impostazione predefinita, il campo **Codice collocazione** nelle righe vendite sono nascosti, quindi occorre visualizzarlo. Per fare ciò è necessario personalizzare la pagina. Per ulteriori informazioni, vedere [Per avviare la personalizzazione di una pagina tramite il banner Personalizzazione](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

  3. Selezionare **Azioni**, quindi **Registrazione** e infine scegliere **Registra**.  
  4. Selezionare il pulsante **Sì**.  

## Creazione dell'ordine di vendita

Gli ordini di vendita sono il tipo più comune di documenti origine in uscita.  

### Per creare l'ordine di vendita

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Creare un ordine di vendita per il fornitore 10000 alla data di lavoro (23 gennaio) con la riga di ordine di vendita seguente.  

    |Articolo|Cod. ubicazione|Quantità|  
    |----|-------------|--------|  
    |1928-S|SUD|30|  

     Comunicare alla warehouse che l'ordine di vendita è pronto per la gestione warehouse.  

4. Scegliere l'azione **Rilascia**.  

    Gianni procede al prelievo e alla spedizione degli articoli venduti.  

## Prelievo e spedizione articoli

Nella pagina **Prelievo magazzino** è possibile gestire tutte le attività di warehouse in uscita per un documento origine specifico, ad esempio un ordine di vendita. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### Per prelevare gli articoli e procedere alla spedizione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi magazzino**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  

    Assicurarsi che il campo **Nr.** della Scheda dettaglio **Generale** sia compilato.
3. Selezionare il campo **Documento origine**, quindi selezionare **Ordine vendita**.  
4. Selezionare il campo **Nr. origine**, selezionare la riga per la vendita al cliente 10000 e fare clic sul pulsante **OK**.  

    In alternativa, scegliere l'azione **Prendi documento origine**, quindi selezionare l'ordine di vendita.  
5. Scegliere l'azione **Autocompil. qtà da gestire**.  

    In alternativa, nel campo **Qtà da gestire** immettere 10 e 20 rispettivamente nelle due righe di prelievo magazzino.  
6. Scegliere l'azione **Registra**, selezionare **Spedizione**, quindi scegliere il pulsante **OK**.  

    Le 30 Lampade Amsterdam ora sono registrate come prelevati dalle collocazioni S-01-0001 e S-01-0002 e viene creato un movimento contabile articolo negativo che riflette la spedizione di vendita registrata.  

## Vedere anche

[Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md)  
[Spostare articoli ad hoc nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Dettagli di progettazione: Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md)  
[Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
