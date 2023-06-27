---
title: Registrare gli acquisti con le fatture di acquisto (video)
description: Viene descritto come acquistare articoli di magazzino o non o risorse creando e registrando le fatture o gli ordini di acquisto.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="record-purchases-with-purchase-invoices-and-orders" />Registrare gli acquisti con le fatture e gli ordini di acquisto

È possibile creare una fattura o un ordine di acquisto per registrare il costo di acquisto e per tenere traccia del conto fornitori. Le fatture e gli ordini di acquisto vengono utilizzati per aggiornare in modo dinamico i livelli di magazzino in modo da ridurre i costi di magazzino al minimo e migliorare l'assistenza clienti. I costi di acquisto, incluse le spese di assistenza, e i valori di magazzino derivanti dalla registrazione delle fatture o degli ordini di acquisto contribuiscono alle cifre di profitto e altri indicatori KPI finanziari in Gestione ruolo utente.

## <a name="record-purchases-with-purchase-invoices" />Registrare gli acquisti con le fatture di acquisto

Quando si ricevono gli articoli di magazzino, o quando il servizio acquistato viene completato, si registra la fattura di acquisto per aggiornare il magazzino e i record finanziari e per attivare il pagamento al fornitore in base alle condizioni di pagamento. [Effettuare i pagamenti](payables-make-payments.md).

> [!CAUTION]  
> Non registrare gli articoli fisici per una fattura di acquisto fino a quando non si ricevono gli articoli e si conosce il costo finale dell'acquisto, incluse le spese aggiuntive. In caso contrario, il valore di magazzino e le cifre di margine possono risultare distorti.

### <a name="create-a-and-post-purchase-invoice" />Creare e registrare una fattura di acquisto

Di seguito viene descritto come creare una fattura di acquisto. I passaggi sono simili per un ordine di acquisto. La differenza principale è che gli ordini acquisto hanno campi e azioni aggiuntivi per la gestione fisica degli articoli.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.  
2. Nel campo **Fornitore** immettere il nome del fornitore esistente.

    Altri campi nella pagina **Fattura di vendita** ora vengono compilati con le informazioni standard del fornitore selezionato. Se il fornitore non è registrato, è necessario attenersi alla seguente procedura:

    1. Nel campo **Fornitore** immettere il nome del nuovo fornitore.
    2. Nella finestra di dialogo relativa alla registrazione del nuovo fornitore fare clic su **Sì**.
    3. Per ulteriori informazioni su come compilare la scheda fornitore, vai a [Registrare nuovi fornitori](purchasing-how-register-new-vendors.md).  
    4. Una volta completata la scheda fornitore, fai clic su **OK** per tornare alla pagina **Fattura di acquisto**.

3. Compilare i restanti campi della pagina **Fattura di acquisto** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    A questo punto si è pronti a compilare le righe della fattura di acquisto con gli articoli o le risorse acquistati presso il fornitore.

    > [!NOTE]  
    > Se sono state impostate righe di acquisto periodiche per il fornitore, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nella fattura scegliendo l'azione **Ottieni righe acquisto ricorrenti**.
4. Sulla FastTab **Righe**, nel campo **N. elemento**, inserisci il numero di un articolo d'inventario o di un servizio.
5. Nel campo **Quantità** immettere il numero di articoli da acquistare.

    Il campo **Importo riga** viene aggiornato al valore del campo **Costo unitario diretto** moltiplicato per il valore del campo **Quantità**.

    Il prezzo e l'importo riga vengono visualizzati con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda fornitore.

    I campi dei totali sotto le righe vengono automaticamente aggiornati quando si creano o si modificano le righe per visualizzare gli importi che verranno registrati nei libri contabili.

6. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.** nella parte inferiore della fattura.

    > [!NOTE]  
    > Se sono stati impostati gli sconti sulla fattura per il fornitore, allora la percentuale specificata verrà automaticamente inserita nel campo **Vendor Invoice Discount %** se vengono soddisfatti i criteri. Il relativo importo viene quindi inserito nel campo **Importo sconto fattura**.
7. Quando si ricevono l'assistenza o gli articoli acquistati, scegliere **Registra**.

L'acquisto si riflette ora nel magazzino, nei movimenti contabili risorse e nei record finanziari e il pagamento fornitore viene attivato. La fattura di acquisto viene rimossa dall'elenco delle fatture di acquisto e sostituita con un nuovo documento nell'elenco delle fatture di acquisto registrate.  Per ulteriori informazioni su cosa accade quando si registrano i documenti di acquisto, vedi [Registrazione degli acquisti](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> In casi rari, gli importi registrati possono discostarsi da ciò che viene visualizzato nei campi dei totali. Ciò è in genere dovuto ai calcoli di arrotondamento in relazione all'IVA o all'imposta sulle vendite.
>
> Per verificare gli importi che verranno effettivamente registrati, vai alla pagina **Statistiche**, che tiene conto dei calcoli nel conto. Inoltre, se si sceglie l'azione **Rilascia**, i campi dei totali verranno aggiornati per includere i calcoli di arrotondamento.

## <a name="posted-invoices" />Fatture registrate

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

È possibile correggere o annullare in modo semplice una fattura di acquisto registrata prima che venga pagata al fornitore. Ciò risulta utile se si desidera correggere un errore di digitazione o se si desidera modificare l'acquisto in una fase iniziale dell'elaborazione dell'ordine. Ulteriori informazioni in [Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Se è già stato eseguito il pagamento degli articoli o dei servizi nella fattura di acquisto registrata, è necessario creare una nota di credito di acquisto per stornare l'acquisto. Ulteriori informazioni in [Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md).

[Apri l'elenco **Fatture acquisto registrate**](https://businesscentral.dynamics.com/?page=146) in [!INCLUDE [prod_short](includes/prod_short.md)].


## <a name="purchasing-non-inventory-items" />Acquisto di articoli non in magazzino

Le righe di una fattura di acquisto possono essere di tipo **Risorsa** o **Articolo**. Le schede articolo possono essere classificate come tipo **Inventario**, **Assistenza** o **Non inventario** per specificare se la scheda articolo rappresenta un'unità fisica di inventario, un'unità di misura del tempo (applicabile anche per le risorse) della manodopera o un'unità fisica non registrata in magazzino. Ulteriori informazioni in [Registrare nuovi articoli](inventory-how-register-new-items.md). Il processo della fattura di acquisto è lo stesso per tutti i tipi menzionati.

> [!NOTE]
> Con il tipo di riga acquisto **Risorsa**, è inoltre possibile acquistare risorse esterne, ad esempio, per fatturare a un fornitore per il lavoro eseguito. Ulteriori informazioni in [Impostare risorse](projects-how-setup-resources.md).
>
> Per utilizzare una risorsa acquistata, potrebbe essere necessario impostare la capacità della risorsa e assegnarla manualmente a un processo. L'acquisto di una risorsa crea un movimento contabile di risorsa, tuttavia, i movimenti contabili non vengono monitorati per quantità e valore come, ad esempio, per gli articoli. Se è richiesto il monitoraggio della quantità e del valore, considera l'utilizzo di altri tipi di voci.

## <a name="when-to-use-purchase-orders" />Quando utilizzare gli ordini di acquisto

Utilizzare gli ordini di acquisto se il processo di acquisto richiede la registrazione delle le ricevute parziali di una quantità di un ordine, ad esempio, perché la quantità completa non è disponibile presso il fornitore. Se si consegni articoli venduti direttamente dal fornitore al cliente, come una spedizione diretta, è necessario utilizzare anche gli ordini di acquisto. Ulteriori informazioni su [Effettuare spedizioni dirette](sales-how-drop-shipment.md).

In tutti gli altri aspetti, gli ordini di acquisto funzionano come le fatture di acquisto. La seguente procedura è basata su una fattura di acquisto. I passaggi sono simili per un ordine di acquisto.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order" />Ricevere gli articoli con un ordine di acquisto

Di seguito viene descritto come ricevere gli articoli con un ordine di acquisto. 

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.
2. Aprire un ordine di acquisto esistente o crearne uno.
3. Nel campo **Qtà da Ricevere** immettere la quantità ricevuta.

   > [!NOTE]
   > Se la quantità ricevuta è superiore a quella nell'ordine acquisto, e il fornitore è stato configurato per consentire le ricevute in eccesso, puoi utilizzare il campo **Ricezione eccessiva** per gestire la quantità in eccesso. Ulteriori informazioni nella sezione [Per ricevere più articoli di quelli ordinati](purchasing-how-record-purchases.md#receive-more-items-than-ordered).
4. Scegli l'azione **Registra**.

  Il valore nel campo **Qtà ricevuta** viene aggiornato. Se si tratta di una ricezione parziale, il valore è inferiore al valore nel campo **Quantità**.

> [!NOTE]
> Se usi la gestione warehouse, non puoi utilizzare l'azione **Registra** sull'ordine di acquisto per registrare la ricevuta. Questo perché un addetto warehouse ha già registrato la quantità dell'ordine di acquisto ricevuta. Per ulteriori informazioni vedi [Dettagli di progettazione - Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).

## <a name="receive-more-items-than-ordered" />Ricevere più articoli di quelli ordinati

Quando arrivano più merci di quelle ordinate, è possibile che vuoi mantenerle anziché annullare il carico. Ad esempio, potrebbe essere più economico mantenere l'eccesso di articoli nell'inventario anziché restituirli oppure il fornitore potrebbe offrire uno sconto per accettarlo.

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts" />Configurare le ricevute in eccesso

Crea i codici di ricevuta in eccesso per definire una percentuale in base alla quale una quantità ricevuta può superare la quantità ordinata. Specifica la percentuale nel campo **% tolleranza per ricezione eccessiva**. Quindi assegna il codice nelle pagine Scheda articolo o Scheda fornitore per articoli e fornitori.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Codici di ricezione eccessiva**, quindi scegli il collegamento correlato.
2. Compila i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item" />Assegnare il codice di ricezione eccessiva a un articolo

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , inserisci **Elemento** e scegli il link relativo.
2. Apri la pagina **Scheda articolo** per l'articolo.
3. Nel campo **Codice di ricezione eccessiva**, scegli il codice che contiene la percentuale che desideri consentire per le ricezioni in eccesso.

Il codice di ricezione eccessiva viene assegnato all'articolo. Gli ordini di acquisto o le ricevute warehouse per l'articolo ora consentono di ricevere più della quantità ordinata in base alla percentuale di tolleranza di ricezione eccessiva.

> [!NOTE]
> È possibile configurare un flusso di lavoro di approvazione per richiedere che le ricezioni eccessive debbano essere approvate prima di poter essere gestite. Seleziona la casella di conteollo **Approvazione richiesta** nella pagina **Codici di ricezione eccessiva**. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).

### <a name="over-receive-an-order" />Ricezione eccessiva di un ordine

Sulle righe di acquisto e sulle righe di ricevuta del magazzino, il campo **Quantità di ricezione eccessiva** viene utilizzato per registrare le quantità ricevute in eccesso, ovvero le quantità che superano il valore nel campo **Quantità**, la quantità ordinata.

Quando si gestisce una ricezione in eccesso, puoi aumentare il valore nel campo **Qtà da Ricevere** per la quantità effettivamente ricevuta. Il campo **Quantità di ricezione in eccesso** viene aggiornato per mostrare la quantità in eccesso. In alternativa, è possibile inserire la quantità in eccesso nel campo **Quantità di ricezione in eccesso**. Il campo **Qtà da Ricevere** viene aggiornato per mostrare la quantità ordinata più quella in eccesso. La seguente procedura ha descritto come compilare il campo **Qtà da Ricevere**.  

1. In un ordine di acquisto o in un documento di ricevuta di magazzino in cui la quantità ricevuta è superiore a quella ordinata, immettere la quantità effettivamente ricevuta nel campo **Qtà da Ricevere**.

    Se l'aumento rientra nella tolleranza specificata dal codice di ricezione eccessiva assegnato, il campo **Quantità di ricezione eccessiva** viene aggiornato per mostrare la quantità che il valore nel campo **Quantità** ha superato.

    Se l'aumento è superiore alla tolleranza, la ricezione eccessiva non è consentita. Verifica se un altro codice di ricevuta in eccesso la consene. In caso contrario, è possibile ricevere solo la quantità ordinata e la quantità in eccesso deve essere gestita altrimenti, ad esempio, restituendola al fornitore.

2. Registra la ricevuta come faresti per qualsiasi altra ricevuta.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] non gestisce automaticamente gli aspetti finanziari delle ricevute in eccesso. È necessario gestirle manualmente in accordo con il fornitore, ad esempio, chiedendo al fornitore di inoltrare una fattura nuova o aggiornata.

## <a name="external-document-number" />Numero di documento esterni

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases" />Registrazione di acquisti

In un documento di acquisto, è possibile scegliere tra le seguenti azioni di registrazione:

* **Registra**
* **Anteprima registrazione**
* **Registra e stampa**
<!--* **Test Report**-->
* **Registra batch**

Quando un documento di acquisto viene registrato, il conto del fornitore, la contabilità generale e i movimenti contabili risorse vengono aggiornati.

Per ciascun documento di acquisto viene creato un movimento di acquisto nella tabella **Movimenti C/G**. Vengono inoltre creati un movimento nel conto del fornitore nella tabella **Mov. contabili fornitori** e un movimento C/G nel relativo conto passività verso il fornitore. Infine, la registrazione dell'acquisto potrebbe generare un movimento IVA e un movimento C/G relativi all'importo dello sconto. La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione Sconti** nella pagina **Setup contabilità fornitori**.

Per ogni riga di acquisto, se applicabile, verranno create le seguenti voci:

* Tabella **Mov. Contabile Articoli** se la riga di acquisto è di tipo **Articolo**.
* Tabella **Movimento C/G** se le righe di acquisto sono di tipo **Conto G/C**.
* Tabella **Movimento contabile risorsa** se la riga di acquisto è di tipo **Risorsa**.

Inoltre, i documenti di acquisto vengono sempre registrati nelle tabelle **Testata carico acq.** e **Testate fatt. acq**.

È sempre possibile rivedere i vari movimenti contabili che verranno creati in seguito alle registrazioni. Scegli **Anteprima registrazione** per convalidare il documento e ispezionare i movimenti contabili previsti.


> [!IMPORTANT]  
> Quando si registra un ordine acquisto per gli articoli, è possibile creare sia un carico che una fattura. Ciò può avvenire in modo simultaneo oppure indipendente. Prima di effettuare la registrazione, è inoltre possibile creare una ricevuta parziale e una fattura parziale immettendo le necessarie informazioni nei campi **Qtà da ricevere** e **Qtà da fatturare** delle singole righe dell'ordine di acquisto. Tieni presente che non puoi creare una fattura di acquisto da un ordine di acquisto per prodotti o servizi che non sono stati ricevuti. Questo significa che è necessario registrare una ricezione prima di emettere una fattura oppure la ricezione e la fattura devono essere contemporanee.

È possibile effettuare la registrazione oppure effettuare la registrazione e stampare. Quando si seleziona Registra e stampa, viene stampato un report al momento della registrazione dell'ordine. È inoltre possibile scegliere l'azione **Registra batch** per registrare più ordini contemporaneamente. Ulteriori informazioni in [Registrare più documenti contemporaneamente](ui-batch-posting.md).

## <a name="viewing-ledger-entries" />Visualizzazione di movimenti contabili

Una volta completata la registrazione, le righe di acquisto registrate vengono rimosse dall'ordine. Un messaggio avviserà l'utente che la registrazione è completata. Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie pagine, come ad esempio le pagine **Movimenti contabili fornitori**, **Movimenti C/G**, **Mov. contabili articoli**, **Movimenti contabili risorse**, **Ricezioni acquisti** e **Fatture acquisto registrate**.

Nella maggior parte dei casi, è possibile aprire i movimenti contabili dalla scheda o dal documento interessato. Ad esempio, nella pagina **Scheda fornitore** scegliere l'azione **Movimenti**.

## <a name="editing-ledger-entries" />Modifica di movimenti contabili

È possibile modificare determinati campi nei documenti di acquisto registrati, come ad esempio **Riferimento pagamento**. Ulteriori informazioni in [Modificare i documenti registrati](across-edit-posted-document.md). Per i campi più critici che influiscono sulla traccia di controllo, è necessario stornare o annullare la registrazione. Ulteriori informazioni in [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-related-microsoft-training-1" />Vedi il relativo [training Microsoft](/training/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also" />Vedere anche

[Richiedere le offerte](purchasing-how-request-quotes.md)  
[Acquistare articoli per una vendita](purchasing-how-purchase-products-sale.md)  
[Preparare le spedizioni dirette](sales-how-drop-shipment.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Impostare risorse](projects-how-setup-resources.md)  
[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Modificare i documenti registrati](across-edit-posted-document.md)  
[Registrare più documenti contemporaneamente](ui-batch-posting.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md)  
[Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
