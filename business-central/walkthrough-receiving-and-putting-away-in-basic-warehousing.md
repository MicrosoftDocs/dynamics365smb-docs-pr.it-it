---
title: 'Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base'
description: Scopri i diversi modi di gestire i processi in entrata per la ricezione e lo stoccaggio.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
---
# Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base

In [!INCLUDE[prod_short](includes/prod_short.md)], la ricezione e lo stoccaggio degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in entrata|Richiesto carico|Richiesto stoccaggio|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino||Attivato|Di base: ordine per ordine.|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse|Attivato||Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni vedi [Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).

Nella seguente procedura dettagliata viene dimostrato il metodo B nella tabella precedente.  

## Informazioni sulla procedura dettagliata  

Nelle configurazioni di warehouse di base in cui un'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi ma non l'elaborazione dei carichi, utilizza la pagina **Stoccaggio in magazzino** per registrare le informazioni riguardanti lo stoccaggio e il carico per i documenti di origine in entrata. I seguenti sono i documenti di origine in entrata:

* Ordine di acquisto
* Ord. reso di vendita
* Ordine di trasferimento in ingresso
* Ordine di produzione con output pronto per essere stoccato

> [!NOTE]
> Anche se le impostazioni sono definite **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile registrare carichi e spedizioni direttamente dai documenti commerciali di origine nelle ubicazioni in cui selezioni queste caselle di controllo.  

In questa procedura dettagliata sono illustrati i task seguenti:  

* Imposta l'ubicazione ARGENTO per gli stoccaggi magazzino.  
* Imposta l'ubicazione ARGENTO per la gestione della collocazione.  
* Definisci una collocazione predefinita per l'articolo LS-81. (LS-75 è già impostato in CRONUS).  
* Crea un ordine di acquisto per il fornitore 10000 per 40 altoparlanti.  
* Verifica che le collocazioni di stoccaggio siano preimpostate in base all'impostazione.  
* Rilascia l'ordine di acquisto per la gestione warehouse.  
* Crea uno stoccaggio in magazzino in base al documento origine rilasciato.  
* Verifica che le collocazioni di stoccaggio siano ereditate dell'ordine di acquisto.  
* Registra la movimentazione warehouse nella warehouse e registra la ricezione acquisti per l'ordine di acquisto di origine.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Ruoli  

I seguenti ruoli utente eseguono le attività illustrate in questa procedura dettagliata:  

* Manager warehouse  
* Rivenditore  
* Lavoro warehouse  

## Prerequisiti  

Per completare questa procedura dettagliata, sarà necessario:  

* Dati CRONUS International Ltd.  
* Essere un dipendente warehouse presso l'ubicazione ARGENTO. Per impostare, esegui la procedura seguente:  

    1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
    2. Seleziona il campo **ID utente** e quindi il tuo account utente nella pagina **Utenti**.  
    3. Nel campo **Codice ubicazione** scegli **ARGENTO**.  
    4. Seleziona la casella di controllo **Predefinito**.  

## Scenario  

Ellen, responsabile warehouse presso CRONUS International Ltd., crea un ordine di acquisto per 10 unità dell'articolo LS-75 e 30 unità dell'articolo LS-81 per il fornitore 10000 che deve essere consegnato alla warehouse ARGENTO. Quando la consegna arriva alla warehouse, Gianni, il lavoratore warehouse, esegue lo stoccaggio degli articoli nelle collocazioni predefinite per gli articoli. Quando Gianni registra lo stoccaggio, gli articoli vengono registrati come ricevuti nel magazzino e disponibili alla vendita o a un'altra domanda.  

## Impostazione dell'ubicazione  

L'impostazione della pagina **Scheda ubicazione** definisce i flussi della warehouse della società.  

### Per impostare l'ubicazione  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2. Aprire la scheda ubicazione ARGENTO.  
3. Abilita l'interruttore **Richiesto stoccaggio**.  

    Imposta una collocazione predefinita per i due numeri articolo per controllare dove vengono stoccati.  

4. Scegliere l'azione **Collocazioni**.  
5. Seleziona la prima riga, per la collocazione **S-01-0001**, quindi scegli l'azione **Contenuti**.  

    Nota che nella pagina **Contenuto collocazione** l'articolo **LS-75** è già impostato come contenuto nella collocazione S-01-0001.  

6. Scegliere l'azione **Nuovo**.  
7. Selezionare i campi **Fisso** e **Default**.  
8. Nel campo **Nr. articolo** immetti **LS-81**.  

## Creare l'ordine di acquisto  

Gli ordini di acquisto sono il tipo più comune di documenti origine in entrata.  

### Per creare l'ordine di acquisto.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Creare un ordine di acquisto per il fornitore 10000 alla data di lavoro (23 gennaio) con le righe di ordine di acquisto seguenti.  

    |Articolo|Cod. ubicazione|Codice collocazione|Quantità|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|ARGENTO|S-01-0001|10|  
    |LS-81|ARGENTO|S-01-0001|30|  

    > [!NOTE]  
    > Il codice di collocazione viene immesso automaticamente in base al setup creato nella sezione [Impostazione dell'ubicazione](#setting-up-the-location).  

    Comunica alla warehouse che l'ordine di acquisto è pronto per la gestione warehouse al momento della consegna.  

4. Scegliere l'azione **Rilascia**.  

    La consegna degli altoparlanti dal fornitore 10000 è arrivata alla warehouse ARGENTO e Gianni continua lo stoccaggio.  

## Ricevere e stoccare gli articoli  

Usa la pagina **Stoccaggio in magazzino** per gestire tutte le attività di warehouse in entrata per un documento origine specifico, ad esempio un ordine di acquisto.  

### Per ricevere e stoccare gli articoli  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggi magazzino**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Selezionare il campo **Documento origine**, quindi selezionare **Ordine acquisto**.  
4. Selezionare il campo **Nr. origine**, selezionare la riga per gli acquisti dal fornitore 10000 e fare clic sul pulsante **OK**.  

    In alternativa, scegliere l'azione **Prendi documento origine**, quindi selezionare l'ordine di acquisto.  

5. Scegliere l'azione **Autocompil. qtà da gestire**.  

    In alternativa, nel campo **Qtà da gestire** immettere 10 e 30 rispettivamente nelle due righe di stoccaggio magazzino.  

6. Scegliere l'azione **Registra**, selezionare l'azione **Ricevi**, quindi il pulsante **OK**.  

    I 40 altoparlanti ora sono registrati come stoccati nella collocazione S-01-0001 e viene creato un movimento contabile articolo positivo che riflette la ricezione acquisti registrata.  

## Vedi anche  

[Eseguire lo stoccaggio con Stoccaggi Magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md)  
[Spostare articoli ad hoc nelle configurazioni della warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md)  
[Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]