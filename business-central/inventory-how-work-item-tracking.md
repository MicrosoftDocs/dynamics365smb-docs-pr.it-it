---
title: 'Tieni traccia degli articoli con numeri di serie, di lotto e di pacco'
description: 'È possibile aggiungere i numeri di serie, di lotto e di pacchetto in qualsiasi documento in entrata o in uscita e visualizzare i relativi movimenti tracciabilità articolo registrati nei movimenti contabili articolo correlati.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 08/31/2021
ms.author: edupont
---
# Tieni traccia degli articoli con numeri di serie, di lotto e di pacco

È possibile assegnare i numeri di serie, di lotto e di pacchetto in qualsiasi documento in entrata o in uscita e visualizzare i relativi movimenti tracciabilità articolo registrati nei movimenti contabili articolo correlati. Eseguire l'operazione nella pagina **Righe tracciabilità articolo**, accessibile da un documento in entrata o in uscita.

La matrice dei campi della quantità nella parte superiore della pagina **Righe tracciabilità articolo** visualizza le quantità e le somme dei numeri di tracciabilità articolo che vengono definiti nelle righe. Le quantità devono corrispondere a quelle della riga documento, indicata da 0 nei campi **Indefinito**.

Per garantire prestazioni migliori, le informazioni sulla disponibilità vengono raccolte nella pagina **Righe tracciabilità articolo** una sola volta, all'apertura della pagina. Questo significa che tali informazioni non vengono più aggiornate fino a quando la pagina rimane aperta, anche se durante tale intervallo di tempo si verificano cambiamenti nel magazzino o in altri documenti.

> [!NOTE]  
>  Affinché le funzionalità descritte in questo articolo funzionino, devi prima impostare la tracciabilità degli articoli. Per ulteriori informazioni, vedi [Configurare la tracciabilità di articoli con numeri di serie, di lotto e di pacco](inventory-how-setup-item-tracking.md).

## Disponibilità di tracciabilità articolo

Quando si utilizzano numeri di serie, lotto e pacchetto tramite [!INCLUDE[prod_short](includes/prod_short.md)] vengono calcolate le informazioni sulla disponibilità e tali informazioni vengono visualizzate nelle diverse pagine relative alla tracciabilità articolo. Ciò consente di verificare la quantità di numero di lotto, pacchetto o seriale attualmente in uso in altri documenti. Ciò riduce gli errori e le incertezze dovuti ad allocazioni doppie.

Nella pagina **Righe tracciabilità articolo** viene visualizzata un'icona di avviso nel campo **Disponibilità, nr. lotto** o **Disponibilità, nr. seriale** se la quantità selezionata o parte di essa è già in uso in altri documenti o se il numero di lotto o seriale non è disponibile.

Nelle pagine **Nr. lotto - Lista/Nr. seriale - Lista**, **Nr. lotto - Disponibilità/Nr. seriale - Disponibilità** e **Tracciabilità articolo - Seleziona movimenti** vengono visualizzate informazioni sulla quantità in uso di un articolo. Sono incluse le seguenti informazioni.

|Campo|Description|
|-----|-----------|  
|**Quantità totale**|La quantità totale dell'articolo attualmente in magazzino|
|**Qtà totale richiesta**|Il numero totale di articoli richiesti che sarà utilizzato nel documento corrente e in altri documenti|
|**Quantità corrente in sospeso**|Il numero di articoli richiesti nel documento corrente ma non ancora caricati nel database.|
|**Quantità corrente richiesta**|Il numero di articoli richiesti nel documento corrente|
|**Quantità totale disponibile**|numero totale di articoli in magazzino meno la quantità di articoli richiesti nel documento corrente e in altri documenti (quantità totale richiesta) e meno la quantità richiesta nel documento corrente ma non ancora caricata (quantità corrente in sospeso)|

Se si utilizza la pagina **Righe tracciabilità articolo** per un intervallo di tempo lungo o se avvengono numerose attività relative all'articolo con cui si sta lavorando, è possibile scegliere l'azione **Aggiorna disponibilità**. Inoltre, alla chiusura della pagina, la disponibilità dell'articolo verrà ricontrollata automaticamente per verificare che non vi siano problemi a riguardo.

## Per assegnare dei numeri seriali o di lotto nelle transazioni in entrata:

Per le società potrebbe essere necessario tenere traccia degli articoli dal momento in cui questi entrano nell'azienda. In questa situazione l'ordine di acquisto rappresenta spesso il documento di riferimento principale, sebbene sia possibile gestire la tracciabilità degli articoli utilizzando qualsiasi documento in entrata e visualizzare i relativi movimenti registrati nei movimenti contabili articolo correlati.

In questo modo i numeri vengono trasferiti automaticamente attraverso tutte le attività di magazzino in uscita senza interazione da parte degli addetti al magazzino.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
2. Apri un ordine di acquisto esistente o creane uno.
3. Seleziona la riga di documento pertinente e, nella Scheda dettaglio **Righe**, scegli l'azione **Riga** e quindi scegli l'azione **Righe tracciabilità articolo** per aprire la pagina **Righe tracciabilità articolo**.  

    È possibile assegnare i numeri seriali o di lotto nei seguenti modi:  
    -   Automaticamente, selezionando **Processo** quindi scegliendo **Assegna Nr. Seriale** o **Assegna Nr. di Lotto** per assegnare dei numeri seriali o di lotto in base alla numerazione predefinita.  
    -   Automaticamente, selezionando **Processo** quindi scegliendo **Crea NS Personalizzato** in modo che il programma assegni dei numeri seriali o di lotto in base a numerazioni definite specificamente per gli articoli giunti in magazzino.  
    -   Manualmente, immettendo direttamente i numeri seriali o di lotto, ad esempio i numeri dei fornitori.  
    -   Manualmente, assegnando un numero specifico a ciascuna unità articolo.  

4. Per assegnare automaticamente, scegliere l'azione **Crea NS personalizzato**.  
5. Nel campo **NS personalizzato** immettere il numero iniziale di una numerazione descrittiva, ad esempio **N/S-Forn0001**.  
6. Nel campo **Incremento**, immettere 1 per specificare un incremento di 1 per ciascun numero della sequenza.  

    Il campo **Quantità da creare** contiene la quantità di righe di default, che tuttavia può essere modificata.  

7. Selezionare la casella di controllo **Crea nuovo nr. di lotto** per organizzare i nuovi numeri seriali in un lotto distinto.  
7. Scegliere il pulsante **OK**.  

Viene creato un numero di lotto con singole numerazioni in base alla quantità degli articoli della riga del documento, iniziando da **S/N-Forn0001**.  

La matrice dei campi di quantità nella testata del form visualizza in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo definiti nella pagina. Le quantità devono corrispondere a quelle della riga documento, contraddistinta da 0 nei campi **Indefinito**.  

Quando il documento viene registrato, i movimenti di tracciabilità articolo vengono riportati nei movimenti contabili degli articoli ad essi associati.

### Per gestire i numeri seriali e di lotto quando si recuperano le righe di carico da una fattura di acquisto

Quando si utilizza la funzione per ottenere il carico registrato o le righe di spedizione dalle relative fatture o note di credito, le righe di tracciabilità articolo nei documenti warehouse vengono trasferite automaticamente; tuttavia, vengono elaborate in modo speciale.

La funzionalità supporta i seguenti processi in entrata:  
-   **Prendi Righe di Carico**, da una fattura di acquisto.  
-   **Prendi Righe Reso Spedizione**, da una nota di credito di acquisto.  

La funzionalità supporta i seguenti processi in uscita:  
-   **Prendi Righe di Spedizione**, da una fattura di vendita o da spedizioni combinate.  
-   **Prendi Righe Carico da Reso**, da una nota credito vendita.  

In queste situazioni le righe di tracciabilità articolo esistenti vengono copiate automaticamente nella fattura o nella nota di credito. La pagina **Righe Tracciabilità Articolo** non consente tuttavia di apportare modifiche ai numeri seriali o di lotto. Solo quantità possono essere modificate.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto**, quindi seleziona il collegamento correlato.  
2. Aprire una fattura di acquisto di articoli acquistati con numero seriale o numero di lotto.  
3. Da una riga della fattura di acquisto, nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di carico**.  
4. Nella pagina **Prendi righe di carico** , selezionare una riga di carico che contiene righe di tracciabilità articolo e fare clic sul pulsante **OK** .  

    Il documento di origine viene copiato nella fattura di acquisto come una nuova riga e le relative righe di tracciabilità articolo vengono copiate nella pagina **Righe tracciabilità articolo** sottostante.  

5. Nella fattura di acquisto selezionare la riga di carico trasferito.  
6. Per visualizzare le righe tracciabilità articolo trasferite, scegliere l'azione **Riga** dalla Scheda dettaglio **Righe** e quindi scegliere l'azione **Righe tracciabilità articolo**.  

Il contenuto dei campi **Nr. lotto** e **Nr. seriale** non è modificabile. Tuttavia, è possibile eliminare righe intere o modificare le quantità in modo da riflettere le modifiche apportate nella riga di origine.  

## Per assegnare un numero seriale o di lotto durante una transazione in uscita

La gestione in uscita dei numeri seriali o di lotto è un'attività frequente in diversi processi di warehouse. Esistono due modi per aggiungere i numeri seriali e di lotto nelle transazioni in uscita:  

-   Selezione da numeri seriali o di lotto esistenti. Questo scenario viene utilizzato quando i numeri di tracciabilità articolo sono già stati assegnati durante una transazione in entrata.
-   Assegnazione nuovi numeri seriali o di lotto nelle transazioni in uscita. Questa procedura si applica quando i numeri di tracciabilità articolo non vengono assegnati agli articoli finché non siano venduti e pronti per la spedizione.

### Per effettuare una selezione da numeri seriali o di lotto esistenti  

Quando si lavora con articoli che richiedono la tracciabilità articolo e si creano transazioni in uscita, ovvero transazioni che prevedono l'uscita degli articoli dal magazzino, è in genere necessario selezionare i numeri di lotto o seriali tra quelli già esistenti in magazzino.

1. In qualsiasi documento in uscita scegliere la riga per la quale si desidera selezionare numeri seriali o di lotto.  
2. Nella Scheda dettaglio **Righe**, scegliere l'azione **Riga**, quindi **Informazioni correlate** e infine **Righe tracciabilità articolo**.  
3. Nella pagina **Righe tracciabilità articolo** sono disponibili tre opzioni per specificare un numero di lotto o seriale:  

    - Selezionare il campo **Nr. seriale** e selezionare un numero nella pagina **Elenco nr. seriali**.
    - Selezionare il campo **Nr. lotto** e selezionare un numero nella pagina **Elenco nr. lotto**. Quindi, selezionare il campo **Nr. seriale** e selezionare un numero nella pagina **Elenco nr. seriali**.
    - Selezionare l'azione **Processo** e quindi **Seleziona movimenti**. La pagina **Seleziona movimenti** mostra tutti i numeri di lotto e seriali con informazioni sulla disponibilità.

4. Nel campo **Quantità selezionata** , immettere la quantità di ogni numero di lotto o seriale che si desidera utilizzare.
5. Selezionare il pulsante **OK** e le informazioni selezionate di tracciabilità articolo vengono trasferite alla pagina **Righe tracciabilità articolo** .  

La matrice dei campi di quantità nella testata del form visualizza in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo definiti nella pagina. Le quantità devono corrispondere a quelle della riga documento, contraddistinta da **0** nei campi **Indefinito**.  

Quando si registra la riga del documento, le informazioni sulla tracciabilità articolo vengono trasferite ai movimenti contabili articoli associati.

### Per assegnare nuovi numeri seriali o di lotto  

Questa alternativa si applica quando gli articoli di magazzino non hanno numeri di serie o di lotto ma numeri di tracciabilità articolo quando gli articoli sono venduti e pronti per essere spediti. In questo scenario i numeri vengono in genere assegnati da una serie di numeri predefiniti.

1. Selezionare il documento pertinente, ad esempio una fattura di vendita o un ordine di vendita, e nella Scheda dettaglio **Righe**, scegli l'azione **Riga**, quindi **Informazioni correlate**, quindi scegli **Righe tracciabilità articolo**.  

    È possibile assegnare i numeri di tracciabilità articolo nei seguenti modi:  
    -   Automaticamente, dalla numerazione predefinita: scegliere l'azione **Assegna nr. seriale** o **Assegna nr. di lotto**.  
    -   Automaticamente, in base a parametri definiti specificamente per l'articolo in uscita: scegliere l'azione **Crea NS personalizzato**.  
    -   Manualmente, immettendo i numeri seriali o di lotto, senza utilizzare una numerazione.  

2. Per la procedura, assegnare un numero seriale automaticamente scegliendo **Assegna nr. seriale**.  

    Il campo **Quantità da creare** contiene la quantità di righe di default, che tuttavia può essere modificata.  
3. Selezionare il campo **Crea nuovo nr. di lotto** per organizzare i nuovi numeri seriali in un lotto distinto.  
4. Fare clic su **OK** per creare un numero di lotto e nuovi numeri seriali singoli in base alla quantità da gestire nella riga del documento correlata.  

La matrice dei campi di quantità nella parte superiore visualizza in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo definiti nella pagina. Le quantità devono corrispondere a quelle della riga documento, contraddistinta da **0** nei campi **Indefinito**.  

Quando il documento viene registrato, i movimenti di tracciabilità articolo vengono riportati nei movimenti contabili degli articoli ad essi associati.

### Assegnare numeri di tracciabilità in documenti di origine

In circostanze particolari per magazzini con numeri di serie o lotto, i numeri specifici sono definiti nel documento di origine, ad esempio un ordine di vendita, che l'addetto warehouse deve rispettare durante la gestione dell'uscita della warehouse. Ciò può essere dovuto al fatto che il cliente ha richiesto un lotto specifico durante l'elaborazione dell'ordine. Quando il documento di prelievo magazzino o di prelievo warehouse viene creato da un documento di origine in uscita in cui i numeri di serie o lotto sono già definiti, tutti i campi della pagina **Righe tracciabilità articolo** del prelievo magazzino non sono modificabili, tranne il campo **Qtà da gestire**. In tal caso, nelle righe di prelievi magazzino vengono specificati i numeri di tracciabilità articolo riportati nelle singole righe Prendere e Mettere. La quantità viene già suddivisa in base a combinazioni di numeri seriali o di lotto uniche, in quanto i numeri di tracciabilità degli articoli da spedire sono specificati nell'ordine di vendita.

## Per gestire i numeri seriali e di lotto negli ordini di trasferimento

Le procedure per la gestione dei numeri seriali e di lotto che vengono trasferiti tra le diverse ubicazioni sono simili a quelle applicate agli articoli venduti e acquistati.  

Tuttavia, l'ordine di trasferimento è unico in quanto la spedizione e la ricezione vengono entrambe eseguite dalla stessa riga di trasferimento e pertanto utilizzano la stessa istanza della pagina **Righe tracciabilità articolo**. Ciò significa che i numeri di tracciabilità articolo inviati da una determinata ubicazione dovranno essere ricevuti invariati nell'altra ubicazione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di trasferimento**, quindi scegli il collegamento correlato.  
2. Aprire l'ordine di trasferimento che si desidera elaborare. Nella Scheda dettaglio **Righe** scegliere l'azione **Riga**, l'azione **Righe tracciabilità articolo** e l'azione **Spedizione**.  
3. Nella pagina **Righe tracciabilità articolo** assegnare o selezionare dei numeri seriali o di lotto come per qualsiasi transazione di articoli in uscita.  

    Di solito, quando si gestiscono i numeri seriali e di lotto per articoli trasferiti, a questi ultimi sono già stati assegnati dei numeri. Il processo pertanto consiste nell'effettuare una selezione da numeri seriali o di lotto già esistenti.  

4. Registrare l'ordine di trasferimento, indicando prima la spedizione e poi la ricezione, in modo da registrare che gli articoli vengono trasferiti unitamente ai rispettivi movimenti di tracciabilità articolo.  

Durante il trasferimento, la pagina **Righe tracciabilità articolo** rimane bloccato per impedire operazioni di scrittura.  

## Per registrare ulteriori informazioni su numeri seriali o di lotto

Nel caso in cui sia necessario collegare informazioni speciali a un determinato numero di tracciabilità articolo, ad esempio per un controllo qualità, è possibile eseguire tale operazione nella scheda di un numero seriale o di lotto.

1. Aprire un documento con i numeri di serie o di lotto assegnati.
2. Aprire la pagina **Righe tracciabilità articolo** per l'articolo per cui si desidera inserire le informazioni.
3. Scegliere l'azione **Riga** e poi, ad esempio, l'azione **Scheda informaz. nr. seriale**.  
4. Scegliere il segno più **(+)** in cima all'elenco per creare una nuova voce. I campi **Nr. lotto** e **Nr. seriale** sono precompilati dalla riga di tracciabilità articolo.
5. Immettere brevi informazioni nel campo **Descrizione** , ad esempio sulla condizione dell'articolo.  
6. Scegliere l'azione **Correlato**, scegliere l'azione **Nr. seriale**, quindi scegliere l'azione **Commento** per creare un record di commento separato.  
7. Selezionare il campo **Bloccato** per escludere il numero seriale o di lotto da tutte le transazioni.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

È possibile modificare le schede informative seriali o sui lotti create in un secondo momento.

## Per modificare le informazioni esistenti sui numeri seriali o di lotto

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Selezionare un articolo con un codice di tracciabilità articolo e le informazioni sui numeri seriali o di lotto.
3. Nella pagina **Scheda articolo**, selezionare l'azione **Movimenti** e quindi scegliere **Movimenti contabili**.
4. Selezionare il campo **Nr. seriale** o **Nr. lotto** . Se per il numero di tracciabilità articolo sono disponibili informazioni, allora verrà visualizzata la pagina **Lista informazioni nr. lotto** o **Lista informazioni nr. seriale**.  
5. Selezionare una scheda quindi scegliere l'azione **Scheda informazioni nr. lotto/nr. seriale**.  
6. Modificare il breve testo descrittivo, il record di commento oppure il campo **Bloccato** .  

Non è possibile modificare il numero seriale o di lotto o le quantità. A tale scopo, è necessario riclassificare il movimento contabile articolo in questione. Per ulteriori informazioni su questa operazione, vedere [Per riclassificare numeri di lotto o seriali](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## Per riclassificare i numeri di serie o di lotto

Riclassificare la tracciabilità di un articolo significa modificare un numero di lotto o seriale in un nuovo numero o cambiare la data di scadenza impostando una nuova data. Se si utilizzano i lotti, è anche possibile unire più lotti in uno solo. Queste attività possono essere eseguite utilizzando le registrazioni di riclassificazione articoli.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Reg. riclass. articoli**, quindi scegli il collegamento correlato.  
2. Compilare la riga con le informazioni appropriate. Per ulteriori informazioni, vedere [Conteggiare l'inventario utilizzando documenti](inventory-how-count-inventory-with-documents.md) o [Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md).
3. Scegliere l'azione **Righe tracciabilità articolo**.  
4. Nel campo **Nr. seriale** o **Nr. lotto** selezionare il numero seriale o di lotto corrente.  
5. Se si desidera specificare un nuovo numero di tracciabilità articolo, immetterlo nel campo **Nuovo nr. seriale** o **Nuovo nr. lotto**. Se lo si desidera, è possibile unire uno o più lotti in un lotto nuovo o esistente.  

    > [!NOTE]  
    >  Si noti che quando si riclassificano le date di scadenza, gli articoli con le date di scadenza più prossime per le transazioni in uscita vengono suggerite per prime. Per ulteriori informazioni, vedere [Prelievo in base al metodo FEFO](warehouse-picking-by-fefo.md).  

6. Se si desidera specificare una nuova data di scadenza per il numero seriale o di lotto, immetterla nel campo **Nuova data scadenza**.  

    > [!IMPORTANT]  
    >  Se si sta riclassificando un lotto per utilizzare lo stesso numero di lotto ma una data di scadenza diversa, è necessario riclassificare l'intero lotto, tramite una riga di registrazione di riclassificazione articoli. Se si sta riclassificando più di un lotto per utilizzare un nuovo numero di lotto, ovvero se si stanno unendo più lotti in un nuovo lotto, è necessario immettere la stessa nuova data di scadenza per tutti i lotti. Se si sta riclassificando un lotto esistente in un secondo lotto esistente con una data di scadenza diversa, è necessario utilizzare la data di scadenza del secondo lotto. Se si lascia vuoto il campo **Nuova data scadenza**, il numero seriale o di lotto verrà riclassificato senza data di scadenza.  

7. Se sono disponibili informazioni sul numero seriale o di lotto precedente, è possibile copiarle nel nuovo numero.  

    1. Nella pagina **Righe tracciabilità articolo** scegliere l'azione **Nuove informazioni nr. seriale** o l'azione **Nuove informazioni nr. lotto**.  
    2. Per copiare le informazioni dal numero di lotto o seriale precedente, scegliere l'azione **Copia informazioni**.  
    3. Nella pagina in cui sono visualizzate le informazioni selezionare il numero seriale o di lotto da cui si desidera effettuare la copia, quindi fare clic su **OK**.  

8. Se si desidera modificare le informazioni esistenti per il numero di lotto o seriale, è possibile registrare informazioni sul numero di lotto o seriale.  
9. Effettuare la registrazione per collegare i nuovi numeri di tracciabilità articolo o le nuove date di scadenza ai movimenti contabili articoli associati

## Vedi il relativo [training Microsoft](/training/modules/prepare-item-tracking/)

## Vedere anche

[Configurare la tracciabilità di articoli con numeri di serie, di lotto e di pacco](inventory-how-setup-item-tracking.md)  
[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)  
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
