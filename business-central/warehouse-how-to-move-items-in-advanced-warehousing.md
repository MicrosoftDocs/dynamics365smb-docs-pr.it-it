---
title: Spostare gli articoli in warehouse che usano stoccaggio e prelievo diretti
description: Questo articolo spiega come spostare gli articoli nelle ubicazioni che utilizzano lo stoccaggio e il prelievo diretti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
---

# Spostare gli articoli nelle configurazioni warehouse avanzate che usano prelievo e stoccaggio diretti

È possibile spostare gli articoli tra le collocazioni senza una domanda da un documento di origine. Ad esempio, potresti volerlo fare come parte delle seguenti attività:

* Riorganizzare la warehouse.
* Portare gli articoli in un'area di ispezione.
* Prendere gli articoli temporaneamente dalle collocazioni di prelievo della warehouse per essere utilizzati, ad esempio, come modelli in contesti di vendita dimostrativi.
* Spostare gli articoli extra nell'area di produzione per i componenti configurati con alcuni metodi di consuntivazione.
* Spostare gli articoli prodotti o assemblati dall'area di produzione o assemblaggio alla warehouse.
* Spostare gli articoli dall'area di stoccaggio in blocco nelle collocazioni che utilizzi per il prelievo.

La modalità di spostamento degli articoli dipende dall'impostazione della warehouse come ubicazione. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).

Nelle configurazioni warehouse in cui l'interruttore **Prelievo e stoccaggio diretti** è attivato per le ubicazioni, è possibile registrare i movimenti non pianificati nelle seguenti pagine:  

* Movimento worksheet
* Prelievi interni warehouse
* Stoccaggi interni warehouse
* Registrazioni della riclassificazione warehouse

Le pagine **Prospetto movimenti**, **Prelievo interno warehouse** e **Stoccaggio interno warehouse** funzionano allo stesso modo. Utilizza le pagine per preparare le attività di warehouse per i dipendenti della warehouse. La differenza sta nelle funzionalità avanzate associate a ciascuna pagina e nei diversi tipi di attività di warehouse che sono probabilmente eseguite da diversi dipendenti:

* Il prospetto movimenti ti consente di riempire le collocazioni di prelievo con alta valutazione con articoli provenienti da altre collocazioni
* Gli stoccaggi utilizzano i modelli di stoccaggio
* Il prelievo utilizza la valutazione collocazione e la disponibilità

## Prospetto movimenti warehouse

### Per spostare gli articoli con il prospetto movimentazioni warehouse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto movimentazioni**, quindi scegli il collegamento correlato.  
2. Compila manualmente i campi nelle righe del prospetto o utilizza una delle seguenti azioni per compilare automaticamente le righe:

    * **Ottieni contenuto collocazione** compila le righe del prospetto con il contenuto della collocazione o delle collocazioni specificate.
    * **Calcola rifornimento collocazione** utilizza le valutazioni collocazioni per suggerire il rifornimento delle collocazioni con valutazione elevata spostando articoli dalle collocazioni con valutazione bassa.

    > [!NOTE]  
    > Se l'articolo soddisfa i criteri nell'elenco sottostante, i campi **Da zona** e **Da collocazione** saranno vuoti. [!INCLUDE [prod_short](includes/prod_short.md)] calcola da dove spostare gli articoli solo quando utilizzi l'azione **Crea movimento**.  
    >  
    > * L'articolo ha una data di scadenza.  
    > * L'interruttore **Prelievo in base a FEFO** è attivato per l'ubicazione.  
    > * Viene utilizzata la funzionalità **Calcola rifornimento collocazione**.  

3. Scegli l'azione **Crea movimento** per creare il movimento. Quando il movimento è completo, può essere registrato.  

### Per registrare la movimentazione warehouse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Movimentazioni**, quindi scegli il collegamento correlato.  
2. Apri il documento di movimento da registrare.  
3. Nelle righe **Posizione** specifica dove, quali e quando spostare l'articolo scegliendo i valori per i campi **Cod. zona**, **Cod. collocazione**, **Qtà da gestire** o **Data scadenza**.  
4. Nelle righe **Prendere** specifica nel campo **Qtà da gestire** la quantità del contenuto collocazione che vuoi spostare. Puoi modificare questo campo solo sulle righe **Prendere**. 

    > [!NOTE]
    > Se è necessario prelevare o inserire gli articoli relativi a una riga in più collocazioni, ad esempio perché la collocazione designata è piena, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.
 
5. Per registrare tutte le quantità suggerite specificate nel campo **Quantità**, scegli l'azione **Autocompil. qtà da gestire**.  
6. Scegliere l'azione **Registra**.  

> [!NOTE]  
> Per le ubicazioni che utilizzano lo stoccaggio e il prelievo diretti, non è possibile spostare manualmente gli articoli nelle collocazioni di tipo **RICEVI** perché non sono ancora considerati come scorte disponibili. Devi stoccare gli articoli in queste collocazioni prima che siano disponibili per i movimenti.

## Prelievo interno  

### Per creare un prelievo interno  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prelievo int. whse.**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Compilare il campo **Nr.** , il campo **Codice ubicazione** e il campo **A codice collocazione** nella Scheda dettaglio **Generale**. Il campo **A codice collocazione** indica la collocazione in cui si desidera inserire gli articoli prelevati. Ai fini della produzione, questa collocazione rappresenta la collocazione di produzione in entrata o la collocazione del reparto produttivo aperto. Viceversa, per altri scopi scegliere un codice collocazione per un tipo di collocazione che non viene utilizzata per il prelievo, in genere una collocazione di stazionamento, una collocazione di spedizione o un collocazione ad uso speciale.  
4. Selezionare un articolo nel campo **Nr. articolo**, quindi immettere le quantità che si desidera prelevare.  
5. Scegliere l'azione **Crea prelievo**. Verrà creata un'istruzione di prelievo indirizzata agli impiegati warehouse. In alternativa, scegli l'azione **Rilascia** e crea prelievi warehouse utilizzando la pagina **Prospetto prelievi**. Per saperne di più sui prospetti prelievi, vai a [Creare documenti di prelievo in blocco con i prospetti prelievi](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Quando il prelievo è completo, può essere registrato.  

### Per registrare il prelievo warehouse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi**, quindi scegli il collegamento correlato.  

    Per utilizzare un determinato prelievo, seleziona il prelievo dalla lista oppure filtra la lista per individuare i prelievi assegnati a te.  
2. Se il campo **ID utente assegnato** è vuoto, immetti il tuo ID per identificarti, se necessario.  
3. Preleva gli articoli.  

    Poiché la warehouse è impostata per utilizzare lo stoccaggio e il prelievo diretti, la valutazione collocazione determina le collocazioni da cui prelevare. Le collocazioni vengono quindi suggerite nelle righe prelievo. Le istruzioni contengono almeno due righe distinte, una per ogni azione Prendere e Mettere.  

4. Dopo avere prelevato e posizionato gli articoli nell'area di spedizione o nella collocazione di spedizione, scegli l'azione **Registra prelievo**.  

## Stoccaggio interno  

### Per creare uno stoccaggio interno  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggi interni warehouse**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**.
3. Compilare il campo **Nr.** e il campo **Cod. ubicazione**.
4. Compila una riga per ciascun articolo da spostare nella warehouse. I campi **Nr. articolo** e **Quantità** sono obbligatori.

    > [!NOTE]  
    > Quando scegli un articolo nel campo **Nr. articolo**, viene visualizzata la pagina **Contenuto collocazione** anziché la pagina **Articoli**. Questa pagina viene visualizzata perché stai eseguendo lo stoccaggio di un articolo assegnato una particolare collocazione, ovvero un *contenuto collocazione* e non semplicemente un articolo, e conosci già la collocazione da cui l'articolo deve essere prelevato. Se hai compilato il campo **Dal codice collocazione**, il contenuto collocazione verrà filtrato in base a tale valore.

5. Per compilare le righe con l'intero contenuto della collocazione o il contenuto di collocazioni specifiche nell'ubicazione, scegli l'azione **Ottieni contenuto collocazione**.  
6. Selezionare l'azione **Crea stoccaggio**. Verrà creata un'istruzione di stoccaggio indirizzata agli impiegati warehouse. In alternativa, scegli l'azione **Rilascia** e crea stoccaggi warehouse utilizzando la pagina **Prospetto stoccaggi**. Per saperne di più sui prospetti stoccaggi, vai a [Creare documenti di stoccaggio in blocco con i prospetti stoccaggi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Quando lo stoccaggio è completo, può essere registrato.  

### Per registrare lo stoccaggio warehouse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Stoccaggi**, quindi scegli il collegamento correlato.
2. Apri lo stoccaggio warehouse pronto per la gestione.  
3. Se richiesto, immetti il tuo ID utente quando inizi a lavorare su uno stoccaggio.  

    Per ottimizzare il processo di stoccaggio, è possibile ordinare le righe di stoccaggio in base a diversi criteri. Ad esempio, per articolo, numero di scaffale o data di scadenza.

    * Se le righe Prendere e Mettere per ciascuna riga di carico non sono consecutive, è possibile ordinarle selezionando **Articolo** nel campo **Metodo ordinamento**.  
    * Se le valutazioni collocazione riflettono il layout fisico della warehouse, utilizza il metodo di ordinamento **Valutazione collocazione** per organizzare la gestione delle ubicazioni della collocazione.  

4. Esegui lo stoccaggio.

    A ogni riga di stoccaggio interno corrispondono almeno due righe di stoccaggio warehouse.  

    * La prima riga, in cui il campo **Tipo azione** è impostato su **Prendere**, indica l'ubicazione degli articoli nell'area di carico. Non è possibile modificare la zona e la collocazione in questa riga.  
    * Nella riga successiva, in cui il campo **Tipo azione** è impostato su **Mettere**, viene indicata la posizione in cui inserire gli articoli nella warehouse. Se ricevi un numero elevato di articoli in una riga di carico, puoi stoccare tali articoli in diverse collocazioni, a ciascuna delle quali corrisponde una riga Mettere.  

5. Una volta posizionati tutti gli articoli nelle collocazioni, come indicato nelle istruzioni, scegliere l'azione **Registra stoccaggio**.  

## Per registrare un movimento che è già avvenuto

Se è necessario registrare il fatto che gli articoli sono già stati spostati in altre collocazioni senza uno stoccaggio, un prelievo o un movimento, è possibile utilizzare la pagina **Registr. riclassificaz. whse.** per registrare il movimento.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registr. riclassificaz. whse.**, quindi scegli il collegamento correlato.  
2. Compilare i campi **Nr. articolo**, **Codice Da zona**, **Dal codice collocazione**, **A codice zona** e **A codice collocazione**.  
3. Scegliere l'azione **Registra**.  

## Vedi il relativo [training Microsoft](/training/modules/manage-internal-warehouse-processes/)

## Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
