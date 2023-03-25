---
title: Ricezione e stoccaggio nella warehouse avanzata
description: I processi in entrata per la ricezione e lo stoccaggio possono essere eseguiti in quattro modalità utilizzando diverse funzionalità a seconda del livello di complessità della warehouse.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# Procedura dettagliata - Ricezione e stoccaggio nelle configurazioni di warehouse avanzate

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In [!INCLUDE[prod_short](includes/prod_short.md)], la ricezione e lo stoccaggio avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in entrata|Richiesto carico|Richiesto stoccaggio|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino||Attivato|Di base: ordine per ordine.|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse|Attivato||Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni vedi [Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).

Nella seguente procedura dettagliata viene dimostrato il metodo D nella tabella precedente.  

## Informazioni sulla procedura dettagliata

Nelle configurazioni di warehouse avanzate in cui un'ubicazione è impostata in modo da richiedere l'elaborazione di carichi oltre all'elaborazione di stoccaggi, utilizzare la pagina **Carico warehouse** per registrare e contabilizzare il carico di articoli su più ordini in entrata. Quando il carico warehouse è registrato, viene creato uno o più documenti di stoccaggio warehouse per istruire gli addetti warehouse sulla ricezione e lo stoccaggio degli articoli ricevuti nelle aree definite in base alla collocazione stabilita o in altre collocazioni. L'ubicazione specifica degli articoli viene registrata quando viene registrato lo stoccaggio warehouse. Il documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata, un assemblaggio o un ordine di produzione il cui output è pronto per lo stoccaggio. Se il carico viene creato per un ordine in entrata, più di un documento di origine in entrata può essere recuperato per il carico. Utilizzando questo metodo è possibile registrare più articoli in arrivo da ordini in entrata diversi con un carico.  

In questa procedura dettagliata sono illustrati i task seguenti:  

-   Impostazione dell'ubicazione BIANCA per la ricezione e lo stoccaggio.  
-   Creazione e rilascio di due ordini di acquisto per una gestione warehouse completa.  
-   Creazione e registrazione di un documento di carico warehouse per più righe di ordini di acquisto da fornitori specifici.  
-   Registrazione dello stoccaggio warehouse per gli articoli ricevuti.  

## Ruoli

Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

-   Manager warehouse  
-   Rivenditore  
-   Personale di ricezione  
-   Lavoro warehouse  

## Prerequisiti

Per completare questa procedura dettagliata, sarà necessario:  

-   Aver installato CRONUS.  
-   Per diventare un impiegato warehouse presso l'ubicazione BIANCA effettuando i seguenti passaggi:  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2.  Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.  
3.  Nel campo **Codice ubicazione** immettere BIANCO:  
4.  Selezionare il campo **Default**.  

## Scenario

Ellen, responsabile warehouse presso CRONUS, crea due ordini di acquisto per articoli relativi agli accessori dai fornitori 10000 e 20000 che devono essere consegnati al magazzino BIANCO. Quando le consegne giungono alla warehouse, Sammy, responsabile della ricezione degli articoli dai fornitori 10000 e 20000, utilizza un filtro per creare righe di carico per gli ordini di acquisto che arrivano dai due fornitori. Sammy registra gli articoli ricevuti nel magazzino in un carico warehouse e li mette a disposizione per la vendita o altre richieste. John, il lavoratore warehouse, prende gli articoli dalla collocazione di ricevimento e li stocca. Stocca tutte le unità nelle proprie collocazioni di default, eccetto 40 su 100 cerniere ricevute durante lo stoccaggio nel reparto di assemblaggio suddividendo la riga di stoccaggio. Quando John registra lo stoccaggio, il contenuto delle collocazioni viene aggiornato e gli articoli vengono resi disponibili per il prelievo dalla warehouse.  

## Verifica dell'impostazione dell'ubicazione BIANCA

L'impostazione della pagina **Scheda Ubicazione** definisce i flussi della warehouse della società.  

### Per rivedere l'impostazione dell'ubicazione  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2.  Aprire la scheda ubicazione BIANCA.  
3.  Notare che nella Scheda dettaglio **Warehouse** la casella di controllo **Stoccaggi e prelievi guidati** è selezionata.  

    Ciò significa che l'ubicazione è impostata per il livello massimo di complessità, riflesso dal fatto che tutte le caselle di controllo di gestione della warehouse nella Scheda dettaglio sono selezionate.  

4.  Notare che nella Scheda dettaglio **Collocazioni** le collocazioni sono specificate nei campi **Codice collocazione carichi** e **Codice collocazione spedizione**.  

Ciò significa che quando si crea un carico warehouse, il codice collocazione viene copiato nell'intestazione del documento di carico warehouse per impostazione di default e nelle righe degli stoccaggi warehouse risultanti.  

## Creazione degli ordini di acquisto

Gli ordini di acquisto sono il tipo più comune di documenti origine in entrata.  

### Per creare gli ordini di acquisto  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Creare un ordine di acquisto per il fornitore 10000 alla data di lavoro (23 gennaio) con le righe di ordine di acquisto seguenti.  

    |Articolo|Cod. ubicazione|Quantità|  
    |----------|-------------------|--------------|  
    |70200|BIANCO|100 PZ|  
    |70201|BIANCO|50 PZ|  

    Comunicare alla warehouse che l'ordine di acquisto è pronto per la gestione warehouse al momento della consegna.  

4.  Scegliere l'azione **Rilascia**. Lo stato cambia da Aperto a Rilasciato.

    Procedere alla creazione del secondo ordine di acquisto.  

5.  Scegliere l'azione **Nuovo**.  
6.  Creare un ordine di acquisto per il fornitore 20000 alla data di lavoro (23 gennaio) con le righe di ordine di acquisto seguenti.  

    |Articolo|Cod. ubicazione|Quantità|  
    |----------|-------------------|--------------|  
    |70100|BIANCO|10 CAN|  
    |70101|BIANCO|12 CAN|  

    Scegliere l'azione **Rilascia**. Lo stato cambia da Aperto a Rilasciato.

    Le consegne degli articoli dai fornitori 10000 e 20000 sono arrivate alla warehouse BIANCO e Sammy inizia per elaborare le ricezioni di acquisto.  

## Ricezione degli articoli

Nella pagina **Carico warehouse** è possibile gestire più ordini in entrata per i documenti di origine, ad esempio un ordine di acquisto.  

### Per ricevere gli articoli  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Carichi warehouse**, quindi seleziona il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Nel campo **Codice ubicazione** immettere BIANCO:  
4.  Seleziona **Azioni** e **Funzioni**, quindi scegli l'azione **Usa filtri per richiamare doc. orig.**  
5.  Nel campo **Codice** immettere **ACCESSORIO**.  
6.  Nel campo **Descrizione** immettere **Fornitori 10000 e 20000**.  
7.  Scegliere l'azione **Modifica**.  
8.  Nella Scheda dettaglio **Acquisto**, nel campo **Filtro Acquistare-da Nr. forn.**, immettere **10000&#124;20000**.  
9. Scegliere l'azione **Esegui**. Il carico warehouse viene compilato con quattro righe che rappresentano le righe ordine di acquisto per i fornitori specificati. Il campo **Qtà da ricevere** è compilato in quanto non è stata selezionata la casella di controllo **Non compilare Qtà da gestire** nella pagina **Filtri per ottenere documenti origine**.  
10. In alternativa, se si desidera utilizzare un filtro come descritto in precedenza in questa sezione, scegliere l'azione **Prendi documento origine**, quindi selezionare gli ordini di acquisto dai fornitori in questione.  
11. Scegli **Registrazione** e quindi l'azione **Registra carico**, quindi scegli il pulsante **Sì**.  

    I movimenti contabili articoli positivi vengono creati sulla base delle ricezioni acquisti registrate di accessori da fornitori 10000 e 20000 e gli articoli sono pronti per lo stoccaggio nella warehouse dalla collocazione di carico.  

## Stoccaggio di articoli

Nella pagina **Stoccaggio warehouse** è possibile gestire gli stoccaggi per uno specifico documento warehouse di carico che copre più documenti di origine. Come in tutti i documenti di attività di warehouse, ogni articolo nello stoccaggio nella warehouse è rappresentato da una riga Prendere e da una riga Mettere. Nella procedura riportata di seguito, il codice di collocazione nelle righe Prendere è la collocazione di ricevimento di default presso l'ubicazione BIANCA, W-08-0001.  


### Per stoccare gli articoli  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggi**, quindi scegli il collegamento correlato.  
2.  Selezionare l'unico documento di stoccaggio warehouse nell'elenco e scegliere l'azione **Modifica**.  

    Il documento di stoccaggio warehouse verrà visualizzato con un totale di otto righe Prendere o Mettere per le quattro righe ordine di acquisto.

    Al lavoratore warehouse viene detto che il reparto di assemblaggio necessita di 40 cerniere. Inizia così a dividere la singola riga Mettere per specificare una seconda riga Mettere per la collocazione W-02-0001 nel reparto di assemblaggio in cui il lavoratore warehouse colloca quella parte di cerniere ricevute.  

3.  Selezionare la seconda riga nella pagina **Stoccaggio warehouse**, la riga Mettere per l'articolo 70200.  
4.  Nel campo **Qtà da gestire** modificare il valore da 100 a 60.  
5.  Nella Scheda dettaglio **Righe** scegliere **Funzioni**, quindi **Dividi riga**. Una nuova riga viene inserita per l'articolo 70200 con 40 nel campo **Qtà da gestire**.  
6.  Nel campo **Codice collocazione** immettere W-02-0001. Il campo **Codice zona** viene compilato automaticamente.  

    Per impostazione predefinita, il campo **Codice zona** nelle righe vendite è nascosto, quindi occorre visualizzarlo. Per fare ciò è necessario personalizzare la pagina. Per ulteriori informazioni, vedere [Per avviare la personalizzazione di una pagina tramite il banner Personalizzazione](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

    Procedere con la registrazione dello stoccaggio.  

7.  Scegliere l'azione **Registra stoccaggio**, quindi scegliere il pulsante **Sì**.  

    Gli accessori ricevuti vengono a questo punto stoccati nelle collocazioni di default degli articoli e 40 cerniere vengono collocate nel reparto di assemblaggio. Gli articoli ricevuti sono ora disponibili per essere prelevati a seconda delle richieste interne, ad esempio gli ordini di assemblaggio, o delle richieste esterne, ad esempio le spedizioni vendite.  

## Vedi anche  
 [Eseguire lo stoccaggio con Stoccaggi warehouse:](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Spostare articoli in configurazioni di warehouse avanzate](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]