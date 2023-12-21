---
title: 'Tieni traccia degli articoli con numeri di serie, di lotto e di pacco'
description: 'È possibile aggiungere i numeri di serie, di lotto e di pacchetto in qualsiasi documento in entrata o in uscita e visualizzare i relativi movimenti di tracciabilità articolo registrati nei movimenti contabili articolo correlati.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 12/19/2023
ms.custom: bap-template
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Tieni traccia degli articoli con numeri di serie, di lotto e di pacco

Puoi assegnare i numeri seriali, di lotto e di collo a qualsiasi documento in entrata o in uscita e visualizzare i relativi movimenti di tracciabilità articolo registrati nei movimenti contabili articolo correlati. Puoi tenere traccia degli articoli nella pagina **Righe tracciabilità articolo**, accessibile da documenti in entrata o in uscita.

I campi relativi alla quantità nella parte superiore della pagina **Righe tracciabilità articolo** visualizzano le quantità e le somme dei numeri di tracciabilità articolo che vengono definiti nelle righe. Le quantità devono corrispondere a quelle nelle righe documento, indicate da 0 nei campi **Indefinito**.

[!INCLUDE [prod_short](includes/prod_short.md)] aggiorna le informazioni sulla disponibilità nella pagina **Righe tracciabilità articolo** quando apri la pagina. Non aggiorna le informazioni quando la pagina è aperta, anche se durante tale periodo si verificano cambiamenti nel magazzino o in altri documenti.

> [!NOTE]  
> Affinché le funzionalità descritte in questo articolo funzionino, devi configurare la tracciabilità articolo. Per ulteriori informazioni, vedi [Configurare la tracciabilità articolo con numeri seriali, di lotto e di collo](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a>Disponibilità di tracciabilità articolo

Quando utilizzi numeri seriali, di lotto e di collo, [!INCLUDE[prod_short](includes/prod_short.md)] calcola le informazioni sulla disponibilità e le mostra in varie pagine relative alla tracciabilità articolo. Mostra quanto di un numero di lotto, di collo o seriale è in uso in altri documenti. Queste informazioni consentono di ridurre gli errori e le incertezze dovuti ad allocazioni doppie.

Nella pagina **Righe tracciabilità articolo**, potrebbe essere visualizzata un'icona di avviso nel campo **Disponibilità, Nr. lotto** o **Disponibilità, Nr. seriale** per i seguenti motivi:

* Se una parte o tutta la quantità selezionata è già utilizzata in altri documenti.
* Se il numero di lotto o seriale non è disponibile.

Le pagine **Nr. lotto - Lista/Nr. seriale - Lista**, **Nr. lotto - Disponibilità/Nr. seriale - Disponibilità** e **Tracciabilità articolo - Seleziona movimenti** mostrano la quantità di un articolo in uso. La tabella seguente elenca i campi pertinenti.

|Campo|Descrizione|
|-----|-----------|  
|**Quantità totale**|Il numero totale di un articolo attualmente in magazzino.|
|**Qtà totale richiesta**|Il numero totale di articoli richiesti nel documento corrente e in altri documenti.|
|**Quantità corrente in sospeso**|Il numero di articoli richiesti nel documento corrente ma non registrato.|
|**Quantità corrente richiesta**|Il numero di articoli richiesti nel documento corrente|
|**Quantità totale disponibile**|Il numero totale di articoli in magazzino meno la quantità dell'articolo richiesta nel documento corrente e in altri documenti (quantità totale richiesta) e meno la quantità richiesta ma non ancora registrata nel documento corrente (quantità corrente in sospeso)|

Se utilizzi la pagina **Righe tracciabilità articolo** per un lungo periodo di tempo o se vi sono numerose attività relative all'articolo con cui si sta lavorando, puoi scegliere l'azione **Aggiorna disponibilità**. Inoltre, la disponibilità dell'articolo viene ricontrollata automaticamente quando viene chiusa la pagina per verificare che non vi siano problemi a riguardo.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Per assegnare numeri seriali o di lotto nelle transazioni in entrata

È possibile che tu voglia tenere traccia degli articoli dal momento in cui arrivano. In tal caso, l’ordine di acquisto è spesso il documento centrale. Tuttavia, puoi eseguire la tracciabilità articolo da qualsiasi documento in entrata e i relativi movimenti registrati sono visualizzati nei movimenti contabili articolo correlati.

I numeri di tracciabilità vengono trasferiti automaticamente a tutte le attività di warehouse in uscita.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
2. Apri un ordine di acquisto esistente o creane uno.
3. Seleziona la riga documento e nella Scheda dettaglio **Righe**, scegli l'azione **Riga** e quindi l'azione **Righe tracciabilità articolo** per aprire la pagina **Modifica - Righe tracciabilità articolo**.  

   È possibile assegnare i numeri seriali o di lotto nei seguenti modi:  
   - Automaticamente, selezionando **Processo** quindi scegliendo **Assegna Nr. Seriale** o **Assegna Nr. di Lotto** per assegnare dei numeri seriali o di lotto in base alla numerazione predefinita.  
   - Automaticamente, selezionando **Processo** quindi scegliendo **Crea NS Personalizzato** in modo che il programma assegni dei numeri seriali o di lotto in base a numerazioni definite specificamente per gli articoli giunti in magazzino.  
   - Manualmente, immettendo direttamente i numeri seriali o di lotto, ad esempio i numeri dei fornitori.  
   - Manualmente, assegnando un numero specifico a ciascuna unità articolo.  

4. Per assegnare automaticamente, scegliere l'azione **Crea NS personalizzato**.  
5. Nel campo **NS personalizzato** immetti il numero iniziale di una numerazione di numeri seriali descrittiva. Ad esempio **S/N-Vend0001**.  
6. Nel campo **Incremento**, immettere 1 per specificare un incremento di 1 per ciascun numero della sequenza.  

    Il campo **Quantità da creare** contiene la quantità di righe di default, che tuttavia può essere modificata.  

7. Seleziona la casella di controllo **Crea nuovo nr. di lotto** per organizzare i nuovi numeri seriali in un lotto distinto.  
7. Scegli il pulsante **OK**.  

[!INCLUDE [prod_short](includes/prod_short.md)] crea un numero di lotto con singoli numeri seriali in base alla quantità degli articoli nella riga documento. Il numero è preceduto dal valore che hai immesso nel campo **NS personalizzato**. Ad esempio, a partire da **S/N-Vend0001**.  

I campi relativi alla quantità nell'intestazione visualizzano in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo che definisci nella pagina. Le quantità devono corrispondere a quelle nelle righe documento, indicate da **0** nel campo **Indefinito**.  

Quando registri il documento, i movimenti di tracciabilità articolo vengono trasferiti ai movimenti contabili articolo.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Per gestire i numeri seriali e di lotto quando si recuperano le righe di carico da una fattura di acquisto

Quando ottieni le righe di carico o di spedizione registrate dalle relative fatture o note di credito, le righe di tracciabilità articolo nei documenti warehouse vengono trasferite automaticamente. Tuttavia, vengono elaborate in un modo speciale.

La funzionalità supporta i seguenti processi in entrata:  

- **Ottieni righe di carico**, da una fattura di acquisto.  
- **Ottieni righe di spedizione reso**, da una nota di credito di acquisto.  

La funzionalità supporta i seguenti processi in uscita:  

- **Ottieni righe di spedizione**, da una fattura di vendita o da spedizioni combinate.  
- **Ottieni righe carico da reso**, da una nota credito vendita.  

In questi casi, le righe di tracciabilità articolo vengono trasferite alla fattura o alla nota di credito, ma la pagina **Righe tracciabilità articolo** non ti consente di apportare modifiche ai numeri seriali o di lotto. Puoi modificare solo le quantità.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto**, quindi seleziona il collegamento correlato.  
2. Aprire una fattura di acquisto di articoli acquistati con numero seriale o numero di lotto.  
3. Da una riga della fattura di acquisto, nella Scheda dettaglio **Righe** scegliere l'azione **Ottieni righe di carico**.  
4. Nella pagina **Ottieni righe di carico**, selezionare una riga di carico che contiene righe di tracciabilità articolo e fare clic sul pulsante **OK** .  

    Il documento di origine viene copiato nella fattura di acquisto come una nuova riga e le relative righe di tracciabilità articolo vengono copiate nella pagina **Righe tracciabilità articolo** sottostante.  

5. Nella fattura di acquisto seleziona la riga di carico trasferita.  
6. Per trovare le righe di tracciabilità articolo trasferite, scegli l'azione **Riga** nella Scheda dettaglio **Righe** e quindi scegli l'azione **Righe tracciabilità articolo**.  

Non puoi modificare i campi **Nr. seriale** e **Nr. lotto**. Tuttavia, puoi eliminare righe intere o modificare le quantità in modo da riflettere le modifiche nella riga di origine.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Per assegnare un numero seriale o di lotto durante una transazione in uscita

La gestione in uscita dei numeri seriali o di lotto è un'attività frequente in diversi processi di warehouse. Esistono due metodi per aggiungere numeri seriali e di lotto in transazioni in uscita:  

- Selezionando da numeri seriali o di lotto esistenti. Questo metodo viene utilizzato quando i numeri di tracciabilità articolo sono già stati assegnati in una transazione in entrata.
- Assegnando nuovi numeri seriali o di lotto per transazioni in uscita. Questo metodo viene utilizzato quando i numeri di tracciabilità articolo non sono assegnati ad articoli finché questi vengono venduti e sono pronti per la spedizione.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>Per effettuare una selezione da numeri seriali o di lotto esistenti

Quando lavori con articoli che richiedono la tracciabilità articolo e stai creando transazioni in uscita, dovrai in genere selezionare numeri di lotto o seriali tra quelli già esistenti.

1. In qualsiasi documento in uscita scegliere la riga per la quale si desidera selezionare numeri seriali o di lotto.  
2. Nella Scheda dettaglio **Righe**, scegliere l'azione **Riga**, quindi **Informazioni correlate** e infine **Righe tracciabilità articolo**.  
3. Nella pagina **Righe tracciabilità articolo** sono disponibili tre opzioni per specificare un numero di lotto o seriale:  

   - Seleziona il campo **Nr. seriale** e seleziona un numero nella pagina **Elenco nr. seriali**.
   - Seleziona il campo **Nr. lotto** e seleziona un numero nella pagina **Elenco nr. lotto**. Quindi seleziona il campo **Nr. seriale** e seleziona un numero nella pagina **Elenco nr. seriali**.
   - Seleziona l'azione **Elabora** e quindi scegli **Seleziona movimenti**. La pagina **Seleziona movimenti** mostra tutti i numeri di lotto e seriali con informazioni sulla disponibilità.

4. Nel campo **Quantità selezionata**, immetti la quantità di ogni numero di lotto o seriale da utilizzare.
5. Scegli il pulsante **OK**. Le informazioni sulla tracciabilità articolo vengono trasferite alla pagina **Righe tracciabilità articolo**.  

I campi relativi alla quantità nell'intestazione visualizzano in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo che definisci nella pagina. Le quantità devono corrispondere a quelle della riga documento, indicata da **0** nel campo **Indefinito**.  

Quando registri la riga documento, le informazioni sulla tracciabilità articolo vengono trasferite ai movimenti contabili articolo associati.

### <a name="to-assign-new-serial-or-lot-numbers"></a>Per assegnare nuovi numeri seriali o di lotto

Questo processo si applica quando gli articoli non hanno numeri seriali o di lotto mentre sono in magazzino. Puoi invece assegnare numeri di tracciabilità articolo quando gli articoli vengono venduti e sono pronti per la spedizione. In tal caso, assegni in genere i numeri di una numerazione predefinita.

1. Selezionare il documento pertinente, ad esempio una fattura di vendita o un ordine di vendita, e nella Scheda dettaglio **Righe**, scegli l'azione **Riga**, quindi **Informazioni correlate**, quindi scegli **Righe tracciabilità articolo**.  

    È possibile assegnare i numeri di tracciabilità articolo nei seguenti modi:  
    - Automaticamente, da una numerazione predefinita: scegli l'azione **Assegna nr. seriale** o **Assegna nr. di lotto**.  
    - Automaticamente, in base a parametri definiti specificamente per l'articolo in uscita: scegliere l'azione **Crea NS personalizzato**.  
    - Manualmente, immettendo numeri seriali o di lotto, senza utilizzare una numerazione.  

2. Per la procedura, assegnare un numero seriale automaticamente scegliendo **Assegna nr. seriale**.  

    Il campo **Quantità da creare** contiene la quantità di righe di default, che tuttavia può essere modificata.  
3. Selezionare il campo **Crea nuovo nr. di lotto** per organizzare i nuovi numeri seriali in un lotto distinto.  
4. Fare clic su **OK** per creare un numero di lotto e nuovi numeri seriali singoli in base alla quantità da gestire nella riga del documento correlata.  

I campi relativi alla quantità nella parte superiore visualizzano in modo dinamico le quantità e le somme dei numeri di tracciabilità articolo definiti nella pagina. Le quantità devono corrispondere a quelle della riga documento, indicata da **0** nel campo **Indefinito**.  

Quando il documento viene registrato, i movimenti di tracciabilità articolo vengono trasferiti ai movimenti contabili articolo.

### <a name="assign-tracking-numbers-on-source-documents"></a>Assegnare numeri di tracciabilità in documenti di origine

Alcune società definiscono numeri seriali o di lotto specifici nel documento di origine, ad esempio ordini di vendita. Ad esempio, se un cliente richiede un lotto specifico. Quando crei il documento di prelievo magazzino o di prelievo warehouse da un documento di origine in uscita in cui i numeri seriali o di lotto sono già definiti, non puoi modificare alcun campo nella pagina **Righe tracciabilità articolo** sotto il prelievo magazzino. L'unica eccezione è il campo **Qtà da gestire**. In tal caso, nelle righe di prelievi magazzino vengono specificati i numeri di tracciabilità articolo riportati nelle singole righe Prendere e Mettere. La quantità viene già suddivisa in base a combinazioni di numeri seriali o di lotto uniche, in quanto i numeri di tracciabilità articolo da spedire sono specificati nell'ordine di vendita.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Per gestire i numeri seriali e di lotto negli ordini di trasferimento

Le procedure per la gestione dei numeri seriali e di lotto che vengono trasferiti tra le diverse ubicazioni sono simili a quelle applicate agli articoli venduti e acquistati.  

Tuttavia, gli ordini di trasferimento sono univoci in quanto la spedizione e il carico sono entrambe eseguiti dalla stessa riga di trasferimento e utilizzano la stessa istanza della pagina **Righe tracciabilità articolo**. I numeri di tracciabilità articolo che vengono spediti da un'ubicazione devono essere ricevuti invariati nell'altra ubicazione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di trasferimento**, quindi scegli il collegamento correlato.  
2. Aprire l'ordine di trasferimento che si desidera elaborare. Nella Scheda dettaglio **Righe** scegliere l'azione **Riga**, l'azione **Righe tracciabilità articolo** e l'azione **Spedizione**.  
3. Nella pagina **Righe tracciabilità articolo** assegnare o selezionare dei numeri seriali o di lotto come per qualsiasi transazione di articoli in uscita.  

    Di solito, quando gestisci numeri seriali e di lotto per articoli trasferiti, i numeri sono in genere numeri già assegnati. Pertanto, sceglierai spesso tra numeri seriali o di lotto esistenti.  

4. Registra l'ordine di trasferimento, indicando prima la spedizione e poi la ricezione, in modo da registrare che gli articoli vengono trasferiti unitamente ai rispettivi movimenti di tracciabilità articolo.  

Durante il trasferimento, non puoi modificare i valori nella pagina **Righe tracciabilità articolo**.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>Per registrare ulteriori informazioni su numeri seriali o di lotto

Se devi collegare informazioni speciali a un determinato numero di tracciabilità articolo, ad esempio per un controllo qualità, puoi eseguire tale operazione nella scheda delle informazioni di un numero seriale o di lotto.

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

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Per modificare le informazioni esistenti sui numeri seriali o di lotto

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Selezionare un articolo con un codice di tracciabilità articolo e le informazioni sui numeri seriali o di lotto.
3. Nella pagina **Scheda articolo**, selezionare l'azione **Movimenti** e quindi scegliere **Movimenti contabili**.
4. Selezionare il campo **Nr. seriale** o **Nr. lotto** . Se per il numero di tracciabilità articolo sono disponibili informazioni, allora verrà visualizzata la pagina **Lista informazioni nr. lotto** o **Lista informazioni nr. seriale**.  
5. Selezionare una scheda quindi scegliere l'azione **Scheda informazioni nr. lotto/nr. seriale**.  
6. Modificare il breve testo descrittivo, il record di commento oppure il campo **Bloccato** .  

Non puoi modificare il numero seriale o di lotto o le quantità. A tale scopo, devi riclassificare il movimento contabile articolo. Per ulteriori informazioni sulla riclassificazione, vedi [Per riclassificare numeri di lotto o seriali](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Per riclassificare i numeri di serie o di lotto

Riclassificare la tracciabilità articolo significa modificare un numero di lotto o seriale in un nuovo numero o cambiare la data di scadenza impostando una nuova data. Se utilizzi i lotti, puoi anche unire più lotti in uno solo. Utilizza le registrazioni di riclassificazione articoli per eseguire queste attività.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Reg. riclass. articoli**, quindi scegli il collegamento correlato.  
2. Compilare la riga con le informazioni appropriate. Per ulteriori informazioni, vedere [Conteggiare l'inventario utilizzando documenti](inventory-how-count-inventory-with-documents.md) o [Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md).
3. Scegliere l'azione **Righe tracciabilità articolo**.  
4. Nel campo **Nr. seriale** o **Nr. lotto** selezionare il numero seriale o di lotto corrente.  
5. Se si desidera specificare un nuovo numero di tracciabilità articolo, immetterlo nel campo **Nuovo nr. seriale** o **Nuovo nr. lotto**. Se lo si desidera, è possibile unire uno o più lotti in un lotto nuovo o esistente.  

    > [!NOTE]  
    > Quando riclassifichi le date di scadenza, gli articoli con le date di scadenza più prossime per le transazioni in uscita vengono suggerite per prime. Per ulteriori informazioni, vedi [Prelievo in base al metodo FEFO](warehouse-picking-by-fefo.md).  

6. Per specificare una nuova data di scadenza per il numero seriale o di lotto, immettila nel campo **Nuova data scadenza**.  

    > [!IMPORTANT]  
    > * Se stai riclassificando un lotto per utilizzare lo stesso numero di lotto ma una data di scadenza diversa, devi riclassificare l'intero lotto, tramite una riga di registrazione di riclassificazione articoli. 
    > * Se stai riclassificando più di un lotto per utilizzare un nuovo numero di lotto, ovvero se stai unendo più lotti in un nuovo lotto, devi immettere la stessa nuova data di scadenza per tutti i lotti. 
    > * Se stai riclassificando un lotto esistente in un secondo lotto esistente con una data di scadenza diversa, devi utilizzare la data di scadenza del secondo lotto. 
    > * Se si lascia vuoto il campo **Nuova data scadenza**, il numero seriale o di lotto verrà riclassificato senza data di scadenza.  

7. Se sono disponibili informazioni sul numero seriale o di lotto precedente, è possibile copiarle nel nuovo numero.  

    1. Nella pagina **Righe tracciabilità articolo** scegliere l'azione **Nuove informazioni nr. seriale** o l'azione **Nuove informazioni nr. lotto**.  
    2. Per copiare le informazioni dal numero di lotto o seriale precedente, scegliere l'azione **Copia informazioni**.  
    3. Nella pagina in cui sono visualizzate le informazioni selezionare il numero seriale o di lotto da cui si desidera effettuare la copia, quindi fare clic su **OK**.  

8. Se si desidera modificare le informazioni esistenti per il numero di lotto o seriale, è possibile registrare informazioni sul numero di lotto o seriale.  
9. Effettuare la registrazione per collegare i nuovi numeri di tracciabilità articolo o le nuove date di scadenza ai movimenti contabili articoli associati

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Eseguire la scansione di codici a barre con l'app per dispositivi mobili Business Central

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Nella pagina **Righe tracciabilità articolo**, se vuoi eseguire la scansione di vari codici a barre di numeri seriali, di lotto o di collo, puoi usare l'azione **Scansione multipla**. Dopo la scansione di un codice a barre, il relativo valore viene immesso nel campo nella pagina e diventa disponibile il campo di immissione rapida successivo. Puoi anche utilizzare l'icona del lettore di codici a barre per popolare un campo specifico.

Le seguenti tabelle elencano le pagine che supportano la scansione di codici a barre per la tracciabilità articolo dall'app per dispositivi mobili [!INCLUDE [prod_short](includes/prod_short.md)].

|Pagina  |Valori dei campi che è possibile scansionare  |
|---------|---------|
|Righe tracciabilità articolo     |* Nr. seriale<br><br>* Nuovo nr. seriale<br><br>* Nr. lotto<br><br>* Nuovo nr. lotto<br><br>* Nr. collo<br><br>* Nuovo nr. collo|
|Registrazioni  Righe tracciabilità articolo     |* Nr. seriale<br><br>* Nuovo nr. seriale<br><br>* Nr. lotto<br><br>* Nuovo nr. lotto<br><br>* Nr. collo<br><br>* Nuovo nr. collo|
|Tracciabilità articolo     |* Filtro nr. seriale<br><br>* Filtro nr. lotto<br><br>* Nr. collo Filtra |
|Registrazioni articoli     |* Nr. seriale<br><br>* Nr. lotto<br><br>* Nr. collo     |
|Riga attività warehouse     |* Nr. seriale<br><br>* Nr. lotto<br><br>* Nr. collo<br><br>**Nota**: le seguenti pagine utilizzano la pagina Riga attività warehouse:<br><br>* pagina 5780 "Subform Prelievo warehouse"<br><br>* pagina 7378 "Subform Prelievo di magazzino"<br><br>* pagina 5771 "Subform Stoccaggio warehouse"<br><br>* pagina 7316 "Subform Movimento warehouse"<br><br>* pagina 7376 "Subform Stoccaggio magazzino"<br><br>* pagina 7383 "Subform Movimento di magazzino"        |
|Registrazioni  Registrazioni magazzino fisico     |* Nr. seriale<br><br>* Nr. lotto<br><br>* Nr. collo         |

## <a name="see-also"></a>Vedere anche

[Impostare la tracciabilità articolo con numeri di serie, di lotto e di collo](inventory-how-setup-item-tracking.md)  
[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)  
[Dettagli di progettazione: Tracciabilità articolo e impegni](design-details-item-tracking-and-reservations.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
