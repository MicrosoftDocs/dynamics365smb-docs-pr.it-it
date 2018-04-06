---
title: 'Procedura: Assegnare i numeri seriali e i numeri di lotto agli articoli per tenere traccia | Documenti Microsoft'
description: "È possibile aggiungere i numeri di serie e di lotto in qualsiasi documento in entrata o in uscita e visualizzare i relativi movimenti tracciabilità articolo registrati nei movimenti contabili articolo correlati."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f9672af6dc4f87f52773a91c587f60c6afe98b8f
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-serial-and-lot-numbers"></a>Utilizzo dei numeri di serie e di lotto
È possibile assegnare i numeri di serie e di lotto in qualsiasi documento in entrata o in uscita e visualizzare i relativi movimenti tracciabilità articolo registrati nei movimenti contabili articolo correlati. Eseguire l'operazione nella finestra **Righe tracciabilità articolo**.

La matrice dei campi della quantità nella parte superiore della finestra **Righe tracciabilità articolo** visualizza le quantità e le somme dei numeri di tracciabilità articolo che vengono definiti nelle righe. Le quantità devono corrispondere a quelle della riga documento, indicata da 0 nei campi **Indefinito**.

Per garantire prestazioni migliori, le informazioni sulla disponibilità vengono raccolte nella finestra **Righe tracciabilità articolo** una sola volta, all'apertura della finestra. Questo significa che tali informazioni non vengono più aggiornate fino a quando la finestra rimane aperta, anche se durante tale intervallo di tempo si verificano cambiamenti nel magazzino o in altri documenti.

Gli articoli con numeri seriali o di lotto che possono essere analizzati sia in avanti che indietro nella rispettiva catena di catena di approvvigionamento. Ciò risulta utile per un controllo della qualità generale e per la restituzione dei prodotti. Per ulteriori informazioni, vedere [Analizzare articoli tracciati](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Informazioni sul prelievo dei numeri di serie o di lotto nella warehouse
La gestione in uscita dei numeri seriali o di lotto è un'attività frequente in diversi processi di warehouse.  

In alcuni processi, gli articoli in magazzino non sono dotati di numeri di serie o lotto e l'addetto warehouse deve assegnarne di nuovi durante la gestione in uscita, in genere una numerazione predefinita.

Nei processi semplici, gli articoli in magazzino sono già dotati di numeri di serie o lotto, ad esempio assegnati durante lo stoccaggio, e tali numeri vengono automaticamente trasferiti a tutte le attività di warehouse in uscita senza alcuna interazione da parte degli addetti warehouse.

In circostanze particolari per magazzini con numeri di serie o lotto, i numeri specifici sono definiti nel documento di origine, ad esempio un ordine di vendita, che l'addetto warehouse deve rispettare durante la gestione dell'uscita della warehouse. Ciò può essere dovuto al fatto che il cliente ha richiesto un lotto specifico durante l'elaborazione dell'ordine. Quando il documento di prelievo magazzino o di prelievo warehouse viene creato da un documento di origine in uscita in cui i numeri di serie o lotto sono già definiti, tutti i campi della finestra **Righe tracciabilità articolo** del prelievo magazzino non sono modificabili, tranne il campo **Qtà da gestire**. In tal caso, nelle righe di prelievi magazzino vengono specificati i numeri di tracciabilità articolo riportati nelle singole righe Prendere e Mettere. La quantità viene già suddivisa in base a combinazioni di numeri seriali o di lotto uniche, in quanto i numeri di tracciabilità degli articoli da spedire sono specificati nell'ordine di vendita.  

## <a name="item-tracking-availability"></a>Disponibilità di tracciabilità articolo
Quando si utilizzano numeri di lotto o serie, tramite [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono calcolate le informazioni sulla disponibilità per tali numeri e tali informazioni vengono visualizzate nelle diverse finestre relative alla tracciabilità articolo. Ciò consente di verificare la quantità di numero di lotto o seriale attualmente in uso in altri documenti. Ciò riduce gli errori e le incertezze dovuti ad allocazioni doppie.

Nella finestra **Righe tracciabilità articolo** viene visualizzata un'icona di avviso nel campo **Disponibilità, nr. lotto** o **Disponibilità, nr. seriale** se la quantità selezionata o parte di essa è già in uso in altri documenti o se il numero di lotto o seriale non è disponibile.

Nelle finestre **Nr. lotto - Lista/Nr. seriale - Lista**, **Nr. lotto - Disponibilità/Nr. seriale - Disponibilità** e **Tracciabilità articolo - Seleziona movimenti** vengono visualizzate informazioni sulla quantità in uso di un articolo. Sono incluse le seguenti informazioni.

|Campo|Description|
|-----|-----------|  
|**Quantità totale**|La quantità totale dell'articolo attualmente in magazzino|
|**Qtà totale richiesta**|Il numero totale di articoli richiesti che sarà utilizzato nel documento corrente e in altri documenti|
|**Quantità corrente in sospeso**|Il numero di articoli richiesti nel documento corrente ma non ancora caricati nel database.|
|**Quantità corrente richiesta**|Il numero di articoli richiesti nel documento corrente|
|**Quantità totale disponibile**|numero totale di articoli in magazzino meno la quantità di articoli richiesti nel documento corrente e in altri documenti (quantità totale richiesta) e meno la quantità richiesta nel documento corrente ma non ancora caricata (quantità corrente in sospeso)|

Se si utilizza la finestra **Righe tracciabilità articolo** per un intervallo di tempo lungo o se avvengono numerose attività relative all'articolo con cui si sta lavorando, è possibile scegliere l'azione **Aggiorna disponibilità**. Inoltre, alla chiusura della finestra, la disponibilità dell'articolo verrà ricontrollata automaticamente per verificare che non vi siano problemi a riguardo.

## <a name="to-set-up-item-tracking-codes"></a>Per impostare i codici di tracciabilità articolo
Un codice di tracciabilità articolo riflette i diversi criteri che una società può seguire nell'uso dei numeri seriali e di lotto degli articoli spostati all'interno di un magazzino.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici tracciabilità articolo**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Fare clic sulla Scheda dettaglio **Nr. seriale** e **Nr. lotto** per definire i criteri di tracciabilità degli articoli rispettivamente in base al numero seriale e al numero di lotto.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Per impostare le regole di scadenza per i numeri seriali e di lotto  
Per alcuni articoli potrebbe essere necessario impostare date e regole di scadenza specifiche nel codice di tracciabilità articolo. Questa funzionalità consente di tenere traccia della scadenza di determinati numeri seriali e di lotto.

1. Selezionare un codice di tracciabilità articolo esistente quindi scegliere l'azione **Modifica**.  
2.  Nella Scheda dettaglio **Varie** selezionare le seguenti caselle di controllo.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Registrazione scadenza vincolante**|Specifica che una data di scadenza assegnata al numero di tracciabilità articolo al momento dell'inserimento in magazzino deve essere rispettata all'uscita dal magazzino.|  
    |**Ins. manuale data scadenza**|Specifica che è necessario immettere manualmente una data di scadenza nella riga di tracciabilità articolo.|  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Per impostare le garanzie per i numeri seriali o di lotto  
Per alcuni articoli potrebbe essere necessario impostare garanzie specifiche nel codice di tracciabilità articolo. Questa funzionalità consente di tenere traccia della scadenza delle garanzie per determinati numeri seriali o di lotto presenti in magazzino.        
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici tracciabilità articolo**, quindi scegliere il collegamento correlato.  

1. Selezionare un codice di tracciabilità articolo esistente quindi scegliere l'azione **Modifica**.  
2.  Nella Scheda dettaglio **Varie** compilare il campo **Formula data garanzia** e selezionare la casella di controllo come indicato di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Formula data garanzia**|Specifica l'ultimo giorno di garanzia per l'articolo.|  
    |**Ins. manuale data garanzia**|Specifica che è necessario immettere manualmente una data di garanzia nella riga di tracciabilità articolo.|  

## <a name="to-record-serial-or-lot-number-information"></a>Per registrare informazioni sui numeri seriali o di lotto  
Nel caso in cui sia necessario collegare informazioni speciali a un determinato numero di tracciabilità articolo, ad esempio per un controllo qualità, è possibile eseguire tale operazione nella scheda di un numero seriale o di lotto.

1. Aprire un documento con i numeri di serie o di lotto assegnati.
2. Aprire la finestra **Righe tracciabilità articolo** per il documento.
3. Scegliere, ad esempio, l'azione **Scheda informazioni nr. seriale**.  

    I campi **Nr. lotto** e **Nr. seriale** sono precompilati dalla riga di tracciabilità articolo.  
4. Immettere brevi informazioni nel campo **Descrizione** , ad esempio sulla condizione dell'articolo.  
5. Scegliere l'azione **Commento** per creare un record di commento separato.  
6. Selezionare la casella di controllo **Bloccato** per escludere il numero seriale o di lotto da tutte le transazioni.  

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Per modificare le informazioni esistenti sui numeri seriali o di lotto  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.  
2. Selezionare un articolo con un codice di tracciabilità articolo e le informazioni sui numeri seriali o di lotto.
3. Nella finestra **Scheda articolo**, selezionare l'azione **Movimenti** e quindi scegliere **Movimenti contabili**.
4. Selezionare il campo **Nr. seriale** o **Nr. lotto** . Se per il numero di tracciabilità articolo sono disponibili informazioni, allora verrà visualizzata la finestra **Lista informazioni nr. lotto** o **Lista informazioni nr. seriale**.  
5. Selezionare una scheda quindi scegliere l'azione **Scheda informazioni nr. lotto/nr. seriale**.  
6. Modificare il breve testo descrittivo, il record di commento oppure il campo **Bloccato** .  

Non è possibile modificare il numero seriale o di lotto o le quantità. A tale scopo, è necessario riclassificare il movimento contabile articolo in questione. Per ulteriori informazioni, vedere la sezione "Per riclassificare i numeri di lotto o seriali".

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Per assegnare dei numeri seriali o di lotto nelle transazioni in entrata:  
Per le società potrebbe essere necessario tenere traccia degli articoli dal momento in cui questi entrano nell'azienda. In questa situazione l'ordine di acquisto rappresenta spesso il documento di riferimento principale, sebbene sia possibile gestire la tracciabilità degli articoli utilizzando qualsiasi documento in entrata e visualizzare i relativi movimenti registrati nei movimenti contabili articolo correlati.  

Le regole esatte per la gestione dei numeri di tracciabilità degli articoli in ambito aziendale dipendono dall'impostazione della finestra **Codice tracciabilità articolo**.  

> [!NOTE]  
>  Per utilizzare i numeri di tracciabilità articolo nelle attività di warehouse, è necessario selezionare i campi di setup **Tracciab. lotto in warehouse** e **Tracciab. NS in warehouse**, in quanto definiscono i principi speciali di gestione dei numeri di lotto e seriali nelle attività di warehouse.  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini acquisto**, quindi scegliere il collegamento correlato.  
2.  Selezionare la riga di documento pertinente e, nella Scheda dettaglio **Righe**, scegliere l'azione **Riga** e quindi scegliere l'azione **Righe tracciabilità articolo**.  

    È possibile assegnare i numeri seriali o di lotto nei seguenti modi:  

    -   Automaticamente, facendo clic su **Assegna Nr. Seriale** o **Assegna Nr. di Lotto** per assegnare dei numeri seriali o di lotto in base alla numerazione predefinita.  
    -   Automaticamente, facendo clic su **Crea NS Personalizzato** in modo che il programma assegni dei numeri seriali o di lotto in base a numerazioni definite specificamente per gli articoli giunti in magazzino.  
    -   Manualmente, immettendo direttamente i numeri seriali o di lotto, ad esempio i numeri dei fornitori.  
    -   Manualmente, assegnando un numero specifico a ciascuna unità articolo.  

3. Per assegnare automaticamente, scegliere l'azione **Crea NS personalizzato**.  
4. Nel campo **NS personalizzato** immettere il numero iniziale di una numerazione descrittiva, ad esempio **N/S-Forn0001**.  
5. Nel campo **Incremento**, immettere 1 per specificare un incremento di 1 per ciascun numero della sequenza.  

    Il campo **Quantità da creare** contiene la quantità di righe di default, che tuttavia può essere modificata.  

6. Selezionare la casella di controllo **Crea nuovo nr. di lotto** per organizzare i nuovi numeri seriali in un lotto distinto.  
7. Scegliere il pulsante **OK**.  

Viene creato un numero di lotto con singole numerazioni in base alla quantità degli articoli della riga del documento, iniziando da **S/N-Forn0001**.  

La matrice dei campi di quantità nella testata del form visualizza in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo definiti nella finestra. Le quantità devono corrispondere a quelle della riga documento, contraddistinta da 0 nei campi **Indefinito**.  

Quando il documento viene registrato, i movimenti di tracciabilità articolo vengono riportati nei movimenti contabili degli articoli ad essi associati.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Per assegnare un numero seriale o di lotto durante una transazione in uscita  
Esistono due modi per aggiungere i numeri seriali e di lotto nelle transazioni in uscita:  

-   Selezione da numeri seriali o di lotto esistenti. Questo scenario viene utilizzato quando i numeri di tracciabilità articolo sono già stati assegnati durante una transazione in entrata. Per ulteriori informazioni, vedere la sezione "Per selezionare da numeri seriali e di lotto esistenti".
-   Assegnazione nuovi numeri seriali o di lotto nelle transazioni in uscita. Questa procedura si applica quando i numeri di tracciabilità articolo non vengono assegnati agli articoli finché non siano venduti e pronti per la spedizione.  

Nella finestra **Scheda cod. tracciab. articolo** vengono configurate regole diverse per i numeri di tracciabilità articolo.  

> [!NOTE]  
>  Per assegnare i numeri di tracciabilità articolo nelle attività di warehouse, le caselle di controllo **Tracciab. NS in warehouse** e **Tracciab. lotto in warehouse** devono essere selezionate nella scheda del codice di tracciabilità articolo.    

1. Selezionare il documento pertinente e, nella Scheda dettaglio **Righe**, scegliere l'azione **Ordine** e quindi scegliere l'azione **Righe tracciabilità articolo**.  

    È possibile assegnare i numeri di tracciabilità articolo nei seguenti modi:  
    -   Automaticamente, dalla numerazione predefinita: scegliere l'azione **Assegna nr. seriale** o **Assegna nr. di lotto**.  
    -   Automaticamente, in base a parametri definiti specificamente per l'articolo in uscita: scegliere l'azione **Crea NS personalizzato**.  
    -   Manualmente, immettendo i numeri seriali o di lotto, senza utilizzare una numerazione.  

2.  Per la procedura, assegnare un numero seriale automaticamente scegliendo **Assegna nr. seriale**.  

    Il campo **Quantità da creare** contiene la quantità di righe di default, che tuttavia può essere modificata.  
3.  Selezionare il campo **Crea nuovo nr. di lotto** per organizzare i nuovi numeri seriali in un lotto distinto.  
4.  Fare clic su **OK** per creare un numero di lotto e nuovi numeri seriali singoli in base alla quantità da gestire nella riga del documento correlata.  

La matrice dei campi di quantità nella parte superiore visualizza in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo definiti nella finestra. Le quantità devono corrispondere a quelle della riga documento, contraddistinta da **0** nei campi **Indefinito**.  

Quando il documento viene registrato, i movimenti di tracciabilità articolo vengono riportati nei movimenti contabili degli articoli ad essi associati.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Per effettuare una selezione da numeri seriali o di lotto esistenti  
Quando si lavora con articoli che richiedono la tracciabilità articolo e si creano transazioni in uscita, ovvero transazioni che prevedono l'uscita degli articoli dal magazzino, è in genere necessario selezionare i numeri di lotto o seriali tra quelli già esistenti in magazzino.  

 Le regole esatte per la gestione dei numeri di tracciabilità degli articoli in ambito aziendale dipendono dall'impostazione della tabella **Codice Tracciabilità Articolo**.  

> [!NOTE]  
>  Per gestire i numeri di tracciabilità articolo nelle attività di warehouse, è necessario impostare l'attributo Tracciab. Lotto in Warehouse o Tracciab. NS in Warehouse per l'articolo, in quanto gestisce i principi speciali che regolano i numeri di lotto e seriali nella warehouse.

1.  In qualsiasi documento in uscita scegliere la riga per la quale si desidera selezionare numeri seriali o di lotto.  
2.  Nella Scheda dettaglio **Righe** scegliere l'azione **Azioni**, quindi l'azione **Riga** o **Articolo** e infine l'azione **Righe tracciabilità articolo**.  
3.  Nella finestra **Righe tracciabilità articolo** sono disponibili tre opzioni per specificare un numero di lotto o seriale:  

    -   Selezionare il campo **Nr. lotto** o **Nr. seriale** e selezionare un numero dalla finestra **Riepilogo tracciabilità articolo**.  
    -   Scegliere l'azione **Seleziona movimenti**. La finestra **Seleziona movimenti** mostra tutti i numeri di lotto o seriali con informazioni sulla disponibilità.

4. Nel campo **Quantità selezionata** , immettere la quantità di ogni numero di lotto o seriale che si desidera utilizzare.   
5. Selezionare il pulsante **OK** e le informazioni selezionate di tracciabilità articolo vengono trasferite alla finestra **Righe tracciabilità articolo** .  
6. Digitare o acquisire il numero di tracciabilità articolo.

La matrice dei campi di quantità nella testata visualizza in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo definiti nella finestra. Le quantità devono corrispondere a quelle della riga documento, contraddistinta da **0** nei campi **Indefinito**.  

 Quando si registra la riga del documento, le informazioni sulla tracciabilità articolo vengono trasferite ai movimenti contabili articoli associati.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Per gestire i numeri seriali e di lotto negli ordini di trasferimento  
Le procedure per la gestione dei numeri seriali e di lotto che vengono trasferiti tra le diverse ubicazioni sono simili a quelle applicate agli articoli venduti e acquistati.  

Tuttavia, l'ordine di trasferimento è unico in quanto la spedizione e la ricezione vengono entrambe eseguite dalla stessa riga di trasferimento e pertanto utilizzano la stessa istanza del form **Righe Tracciabilità Articolo**. Ciò significa che i numeri di tracciabilità articolo inviati da una determinata ubicazione dovranno essere ricevuti invariati nell'altra ubicazione.  

 Le regole esatte per la gestione dei numeri di tracciabilità degli articoli in ambito aziendale dipendono dall'impostazione della tabella  **Codice Tracciabilità Articolo**.    
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di trasferimento**, quindi scegliere il collegamento correlato.  
2.  Aprire l'ordine di trasferimento che si desidera elaborare. Nella Scheda dettaglio **Righe** scegliere l'azione **Riga**, l'azione **Righe tracciabilità articolo** e l'azione **Spedizione**.  
3.  Nel form **Righe Tracciabilità Articolo** assegnare o selezionare dei numeri seriali o di lotto come per qualsiasi transazione di articoli in uscita.  

    Di solito, quando si gestiscono i numeri seriali e di lotto per articoli trasferiti, a questi ultimi sono già stati assegnati dei numeri. Il processo pertanto consiste nell'effettuare una selezione da numeri seriali o di lotto già esistenti.  

4.  Registrare l'ordine di trasferimento, indicando prima la spedizione e poi la ricezione, in modo da registrare che gli articoli vengono trasferiti unitamente ai rispettivi movimenti di tracciabilità articolo.  

Durante il trasferimento, il form **Righe Tracciabilità Articolo** rimane bloccato per impedire operazioni di scrittura.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Per gestire i numeri seriali e di lotto quando si recuperano le righe di carico da una fattura di acquisto  
Quando si utilizza la funzione per ottenere il carico registrato o le righe di spedizione dalle relative fatture o note di credito, le righe di tracciabilità articolo nei documenti warehouse vengono trasferite automaticamente; tuttavia, vengono elaborate in modo speciale.

La funzionalità supporta i seguenti processi in entrata:  
-   **Prendi Righe di Carico**, da una fattura di acquisto.  
-   **Prendi Righe Reso Spedizione**, da una nota di credito di acquisto.  

La funzionalità supporta i seguenti processi in uscita:  
-   **Prendi Righe di Spedizione**, da una fattura di vendita o da spedizioni combinate.  
-   **Prendi Righe Carico da Reso**, da una nota credito vendita.  

In queste situazioni le righe di tracciabilità articolo esistenti vengono copiate automaticamente nella fattura o nella nota di credito. La finestra  **Righe Tracciabilità Articolo** non consente tuttavia di apportare modifiche ai numeri seriali o di lotto. Solo quantità possono essere modificate.  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture acquisto**, quindi scegliere il collegamento correlato.  
2.  Aprire una fattura di acquisto di articoli acquistati con numero seriale o numero di lotto.  
3.  Da una riga della fattura di acquisto, nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di carico**.  
4.  Nella finestra **Prendi righe di carico** , selezionare le righe di carico che contengono righe di tracciabilità articolo e fare clic sul pulsante **OK** .  

    Il documento di origine viene copiato nella fattura di acquisto come una nuova riga e le relative righe di tracciabilità articolo vengono copiate nella finestra **Righe tracciabilità articolo** sottostante.  

5.  Nella fattura di acquisto selezionare la riga di carico trasferito.  
6.  Per visualizzare le righe tracciabilità articolo trasferite, scegliere l'azione **Riga** dalla Scheda dettaglio **Righe** e quindi scegliere l'azione **Righe tracciabilità articolo**.  

Il contenuto dei campi **Nr. lotto** e **Nr. seriale** non è modificabile. Tuttavia, è possibile eliminare righe intere o modificare le quantità in modo da riflettere le modifiche apportate nella riga di origine.  

## <a name="to-reclassify-serial-or-lot-numbers"></a>Per riclassificare i numeri di serie o di lotto  
Riclassificare la tracciabilità di un articolo significa modificare un numero di lotto o seriale in un nuovo numero o cambiare la data di scadenza impostando una nuova data. Se si utilizzano i lotti, è anche possibile unire più lotti in uno solo. Queste attività possono essere eseguite utilizzando le registrazioni di riclassificazione articoli.

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riclassificazioni articoli**, quindi scegliere il collegamento correlato.  
2.  Compilare la riga con le informazioni appropriate. Per ulteriori informazioni, vedere [Conteggio, rettifica e riclassificazione dell'inventario](inventory-how-count-adjust-reclassify.md).
3.  Scegliere l'azione **Righe tracciabilità articolo**.  
4.  Nel campo **Nr. seriale** o **Nr. lotto** selezionare il numero seriale o di lotto corrente.  
5.  Se si desidera specificare un nuovo numero di tracciabilità articolo, immetterlo nel campo **Nuovo nr. seriale** o **Nuovo nr. lotto**. Se lo si desidera, è possibile unire uno o più lotti in un lotto nuovo o esistente.  

    > [!NOTE]  
    >  Si noti che quando si riclassificano le date di scadenza, gli articoli con le date di scadenza più prossime per le transazioni in uscita vengono suggerite per prime. Per ulteriori informazioni, vedere [Prelievo in base al metodo FEFO](warehouse-picking-by-fefo.md).  

5.  Se si desidera specificare una nuova data di scadenza per il numero seriale o di lotto, immetterla nel campo **Nuova data scadenza**.  

    > [!IMPORTANT]  
    >  Se si sta riclassificando un lotto per utilizzare lo stesso numero di lotto ma una data di scadenza diversa, è necessario riclassificare l'intero lotto, tramite una riga di registrazione di riclassificazione articoli. Se si sta riclassificando più di un lotto per utilizzare un nuovo numero di lotto, ovvero se si stanno unendo più lotti in un nuovo lotto, è necessario immettere la stessa nuova data di scadenza per tutti i lotti. Se si sta riclassificando un lotto esistente in un secondo lotto esistente con una data di scadenza diversa, è necessario utilizzare la data di scadenza del secondo lotto. Se si lascia vuoto il campo **Nuova data scadenza**, il numero seriale o di lotto verrà riclassificato senza data di scadenza.  

6.  Se sono disponibili informazioni sul numero seriale o di lotto precedente, è possibile copiarle nel nuovo numero.  

    1.  Nella finestra **Righe tracciabilità articolo** scegliere l'azione **Nuove informazioni nr. seriale** o l'azione **Nuove informazioni nr. lotto**.  
    2.  Per copiare le informazioni dal numero di lotto o seriale precedente, scegliere l'azione **Copia informazioni**.  
    3.  Nella finestra in cui sono visualizzate le informazioni selezionare il numero seriale o di lotto da cui si desidera effettuare la copia, quindi fare clic su **OK**.  

7.  Se si desidera modificare le informazioni esistenti per il numero di lotto o seriale, è possibile registrare informazioni sul numero di lotto o seriale.  
8.  Effettuare la registrazione per collegare i nuovi numeri di tracciabilità articolo o le nuove date di scadenza ai movimenti contabili articoli associati

## <a name="see-also"></a>Vedi anche
[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)   
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

