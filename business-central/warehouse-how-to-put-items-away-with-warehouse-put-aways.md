---
title: Come stoccare articoli con gli stoccaggi warehouse
description: Informazioni sui diversi modi per utilizzare gli stoccaggi warehouse per stoccare gli articoli ricevuti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/19/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Eseguire lo stoccaggio con Stoccaggi warehouse:

In [!INCLUDE[prod_short](includes/prod_short.md)], la ricezione e lo stoccaggio degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in entrata|Richiesto carico|Richiesto stoccaggio|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino||Attivato|Di base: ordine per ordine.|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse|Attivato||Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni vedi [Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).

Questo articolo fa riferimento al metodo D nella tabella e presuppone che la ricezione sia già avvenuta. Per ulteriori informazioni vedi [Ricevere articoli](warehouse-how-receive-items.md).

Quando un'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi e dei carichi warehouse, utilizza la funzionalità relativa ai documenti di stoccaggio warehouse per controllare lo stoccaggio degli articoli. Quando registri un carico warehouse, i documenti di origine come ordini di acquisto, trasferimento in entrata o reso da vendita vengono aggiornati. La quantità ricevuta viene registrata nella contabilità articoli e le righe per gli articoli ricevuti vengono inviate alla funzione di stoccaggio nella warehouse.

A seconda del valore nel campo **Usa prospetto stoccaggi** nella **Scheda ubicazione**, le righe vengono rese disponibile per il prospetto stoccaggi o utilizzate per generare immediatamente i documenti di stoccaggio. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).  

Oltre ai metodi standard per creare stoccaggi warehouse descritti in questo argomento, puoi creare uno stoccaggio a partire dal carico warehouse registrato correlato. Questo è utile se sono state eliminate le righe di stoccaggio oppure se decidi di non utilizzare il prospetto stoccaggi, perché è possibile creare o ricreare istruzioni di stoccaggio dalle righe di carico registrate.

## <a name="zone-and-bin-codes"></a>Codici zona e collocazione

Nelle ubicazioni impostate per l'utilizzo di stoccaggi e prelievi diretti, le impostazioni che sono necessarie per determinare il miglior stoccaggio degli articoli:  

* Viene impostato un modello di stoccaggio. Per ulteriori informazioni, vedi [Impostare i modelli di stoccaggio](warehouse-how-to-set-up-put-away-templates.md).  
* Vengono definiti il peso, la cubatura e i requisiti di immagazzinamento speciali relativi all'articolo o all'unità di stockkeeping.
* La capacità, il tipo di collocazione e la valutazione sono definiti per le collocazioni.  

La valutazione collocazione viene usata quando più collocazioni soddisfano i criteri del modello di stoccaggio. Se i criteri del modello di stoccaggio e la valutazione della collocazione sono gli stessi per più di una collocazione, viene scelta la collocazione con il numero più alto.

## <a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet"></a>Per creare documenti di stoccaggio in blocco con i prospetti stoccaggi

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

È possibile creare documenti di stoccaggio per più carichi contemporaneamente nella pagina **Prospetto stoccaggi**.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetti stoccaggi**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Prendi documenti warehouse**. Verrà visualizzata la pagina **Selezione stoccaggio**.  

    L'elenco contiene tutti i carichi registrati pronti per essere stoccati, inclusi quelli per i quali sono già state create istruzioni di stoccaggio. I documenti contenenti righe di stoccaggio per le quali lo stoccaggio è stato eseguito per intero e registrato non vengono visualizzati in questa lista.  
3. Seleziona i documenti che vuoi utilizzare. È possibile gestire contemporaneamente righe appartenenti a più documenti.  

    > [!NOTE]  
    >  Se selezioni un documento di carico o stoccaggio interno per cui sono già state create istruzioni relative a tutte le righe, [!INCLUDE[prod_short](includes/prod_short.md)]] visualizza un messaggio per informare che non esiste alcun elemento da gestire.  

4. Compila il campo **Metodo di ordinamento** per ordinare le righe.  

    > [!NOTE]  
    >  Il modo in cui le righe vengono ordinate nel prospetto non si applica automaticamente all'istruzione di stoccaggio. Tuttavia, esistono le stesse opportunità per l'ordinamento e la valutazione collocazione. Puoi ricreare l'ordine delle righe pianificato nel prospetto durante la creazione delle istruzioni di stoccaggio o l'ordinamento nelle istruzioni di stoccaggio.

5. Compilare il campo **Qtà da gestire**. Scegliere l'azione **Autocompil. qtà da gestire** oppure compilare i campi manualmente.  
6. Le righe possono essere modificate manualmente, se necessario. È possibile eliminare righe nel caso in cui, ad esempio, sia necessario stoccare alcuni articoli in una collocazione distante dalle collocazioni per altri tipi di articoli.  

    > [!NOTE]  
    > Quando elimini le righe, vengono eliminate solo da questo prospetto. Non vengono eliminate dalla selezione di stoccaggio.  

7. Selezionare l'azione **Crea stoccaggio**. Viene visualizzata la pagina **Crea documento** in cui è possibile aggiungere ulteriori informazioni relative allo stoccaggio che stai creando.  

    * È possibile assegnare lo stoccaggio a un addetto al magazzino specifico.  
    * È possibile ordinare le righe delle istruzioni di stoccaggio in base agli stessi criteri di ordinamento utilizzati nel prospetto o in base alla valutazione collocazione. Quando esegui l'ordinamento in base alla valutazione collocazione, le righe *Prendere* appaiono per prime, poiché la maggior parte delle collocazioni di carico ha una valutazione collocazione pari a 0. Le righe *Mettere* appaiono per ultime, a partire dalle collocazioni con la valutazione più bassa. Se la warehouse è stata strutturata in modo che le collocazioni con valutazione simile siano posizionate l'una accanto all'altra, questa modalità di ordinamento delle righe comporta una semplificazione delle operazioni che gli addetti warehouse dovranno eseguire.  
    * Puoi scegliere di non includere le righe create da [!INCLUDE [prod_short](includes/prod_short.md)] durante la conversione di un'unità di misura di grande dimensione in unità di misura più piccole selezionando il campo **Impostare filtro breakbulk**. Per ulteriori informazioni su breakbulk, vedi [Abilitare breakbulk automatico con stoccaggi e prelievi guidati](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * È possibile scegliere che il campo **Qtà da gestire** non venga compilato automaticamente nelle istruzioni di stoccaggio.  
    * È possibile scegliere di stampare il documento immediatamente.  

8. Seleziona **OK** per creare lo stoccaggio.  

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Per creare uno stoccaggio a partire dal carico registrato

Se un'ubicazione è impostata per l'elaborazione degli stoccaggi e dei carichi e sono state eliminate le righe di stoccaggio oppure utilizzi stoccaggi e prelievi diretti e hai deciso di non utilizzare il prospetto stoccaggi, puoi creare o ricreare istruzioni di stoccaggio per le righe di carico registrate.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Carichi warehouse registrati**, quindi scegli il collegamento correlato.  
2. Seleziona un carico registrato da stoccare.  
3. Scegliere l'azione **Scheda**.  

    Se il campo **Stato del documento** è vuoto, ciò indica che il carico non è stato assolutamente stoccato. In caso contrario, il campo indica se il carico è parzialmente o completamente stoccato.  

4. Se il carico non è stato stoccato o è stato stoccato solo parzialmente, scegliere l'azione **Crea stoccaggio**.  
5. Compila i campi in base alle esigenze, quindi scegli **OK**.  

## <a name="to-put-items-away"></a>Per stoccare gli articoli

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Stoccaggi warehouse**, quindi seleziona il collegamento correlato.

2. Apri lo stoccaggio warehouse pronto per la gestione.  
3. Se richiesto dalla warehouse, immetti il tuo ID utente quando inizi a lavorare su uno stoccaggio.  

    È possibile ordinare le righe stoccaggio in base a diversi criteri, ad esempio per articolo, numero di scaffale o data di scadenza. L'ordinamento può aiutare a ottimizzare il processo di stoccaggio, ad esempio:

    * Se le righe Prendere e Mettere per ciascuna riga di carico non sono consecutive, è possibile ordinarle selezionando **Articolo** nel campo **Metodo ordinamento**.  
    * Se le valutazioni collocazione riflettono il layout fisico della warehouse, utilizza il metodo di ordinamento **Valutazione collocazione** per organizzare la gestione delle ubicazioni della collocazione.

4. Esegui le azioni.

    Se un codice collocazione è obbligatorio per le ubicazioni, ogni riga di carico diventa almeno due righe nello stoccaggio warehouse, come segue.  

    * La prima riga, in cui il campo **Tipo azione** è impostato su **Prendere**, indica l'ubicazione degli articoli nell'area di carico. Non è possibile modificare la zona e la collocazione in questa riga.  
    * Nelle righe successive, in cui il campo **Tipo azione** è impostato su **Mettere**, viene indicata la posizione in cui inserire gli articoli nella warehouse. Se ricevi un numero elevato di articoli in una riga di carico, puoi stoccare tali articoli in diverse collocazioni, a ciascuna delle quali corrisponde una riga Mettere. 

    > [!NOTE]
    > Se è necessario inserire gli articoli relativi a una riga in più collocazioni, ad esempio perché la collocazione designata è piena, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.

5. Una volta posizionati tutti gli articoli nelle collocazioni, come indicato nelle istruzioni, scegliere l'azione **Registra stoccaggio**.  

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
