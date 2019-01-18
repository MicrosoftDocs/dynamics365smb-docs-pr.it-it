---
title: Elaborare gli annullamenti o i resi di vendita | Documenti Microsoft
description: "Descrive come creare una nota di credito vendita, direttamente o tramite un ordine di reso da vendita, per elaborare un reso, un annullamento o il rimborso per articoli o servizi per cui si è ricevuto il pagamento."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 1c1bcb570f06719cfbb8930667a2f2847003d93c
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="process-sales-returns-or-cancellations"></a>Elaborare i resi o gli annullamenti vendite
Se un cliente desidera restituire gli articoli o ottenere il rimborso degli articoli o dei servizi che gli sono stati venduti e che ha pagato, è necessario creare e registrare una nota di credito di vendita in cui viene specificata la modifica richiesta. Per includere le informazioni corrette in merito alle fatture di vendita, è possibile creare la nota di credito di vendita direttamente dalla fattura di vendita registrata oppure creare una nuova nota di credito di vendita con le informazioni copiate dalla fattura.

Se è necessario più controllo del processo di reso da vendita, ad esempio i documenti di warehouse per la gestione degli articoli o una sintesi migliorata quando si ricevono gli articoli da più documenti di vendita con un unico reso da vendita, è possibile creare gli ordini di reso da vendita. Un ordine di reso da vendita genera automaticamente la nota di credito di vendite e altri documenti correlati ai resi, ad esempio un ordine di vendita di sostituzione, se necessario. Per ulteriori informazioni, vedere la sezione "Per creare un ordine di reso da vendita sulla base di uno o più documenti di vendita registrati".

> [!NOTE]  
>   Se una fattura di vendita registrata non è stata ancora pagata, è possibile utilizzare la funzione **Rettifica** o **Annulla** nella fattura di vendita registrata per stornare le transazioni. Queste funzionano solo per le fatture non pagate e non supportano i resi o le cancellazioni parziali. Per ulteriori informazioni, vedere [Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md).

Un reso o un risarcimento può essere correlato solo ad alcuni degli articoli o dei servizi nella fattura di vendita originale. In questo caso, è necessario modificare le informazioni nelle righe della nota di credito di vendita o dell'ordine di reso da vendita. Quando si registra la nota di credito di vendita o l'ordine di reso da vendita, i documenti di vendita influenzati dalla variazione vengono stornati ed è possibile creare un pagamento di rimborso per il cliente. Per ulteriori informazioni, vedere [Effettuare i pagamenti](payables-make-payments.md).  

Oltre alla fattura di vendita registrata originale, è possibile collegare la nota di credito di vendita o l'ordine di reso da vendita ad altri documenti di vendita, ad esempio un'altra fattura di vendita registrata, in quanto il cliente restituisce anche gli articoli consegnati con la fattura.

È possibile inviare la nota di credito vendita registrata al cliente per confermare il reso o l'annullamento e comunicare che il valore correlato verrà rimborsato, ad esempio quando gli articoli vengono resi.

La registrazione della nota di credito annullerà anche tutti gli addebiti articolo assegnati al documento registrato, in modo che i movimenti valorizzazione articolo siano identici a prima dell'assegnazione dell'addebito articolo.

## <a name="inventory-costing"></a>Costing di magazzino
Per mantenere la corretta valutazione del magazzino, in genere si desidera sistemare gli articoli restituiti nuovamente in magazzino al costo unitario con cui sono stati venduti e non al costo unitario corrente. Questa operazione è detta storno esatto costo.

Sono disponibili due funzioni per assegnare lo storno esatto costo automaticamente.   

|Funzione|Description|  
|------------------|---------------------------------------|  
|La funzione **Ottieni righe documento registrato da stornare** nella pagina **Ordine di reso vendita**|Copia le righe di uno o più documenti registrati da stornare nell'ordine di reso da vendita. Per ulteriori informazioni, vedere la sezione "Per creare un ordine di reso da vendita e la relativa nota di credito di vendita per una o più fatture di vendita registrate".|  
|La funzione**Copia documento** nelle pagine **Nota credito vendita** e **Ordine di reso vendita**|Copia la testata e le righe di un documento registrato da stornare.<br /><br /> È necessario che la casella di controllo **Storno esatto costo obblig.** sia selezionata nella pagina **Setup contabilità clienti e vendite**.|

Per assegnare manualmente lo storno esatto costo, è necessario utilizzare il campo **Collega-da mov. art.** per ogni tipo di riga di documento di reso e selezionare il numero del movimento di vendita originale. In questo modo, l'ordine di reso vendita o la nota di credito di vendita verrà collegato al movimento di vendita originale e l'articolo verrà valutato in base al costo unitario originale.

Per ulteriori informazioni, vedere [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Per creare una nuova nota di credito di vendita da una fattura di vendita registrata
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture di vendita registrate** e scegliere il collegamento correlato.  
2. Nella pagina **Fatture vendita registrate** selezionare la fattura di vendita registrata che si desidera stornare, quindi scegliere l'azione **Crea nota credito di rettifica**.

    Nell'intestazione della nota di credito di vendita sono incluse alcune informazioni contenute nella fattura di vendita registrata. Tali informazioni possono, ad esempio, essere sostituite da nuove informazioni che riflettono il contratto di reso.  
3. Modificare le informazioni nelle righe in base al contratto, quali il numero di articoli resi o l'importo da rimborsare.
4. Scegliere l'azione **Collega movimenti**.
5. Nella pagina **Collega movimenti clienti**, selezionare la riga con il documento di vendita registrato a cui si desidera collegare la nota di credito di vendita, quindi scegliere l'azione **Collega-a ID**.

    L'identificativo della nota di credito di vendita viene visualizzato nel campo **Collega-a ID**.
6. Nel campo **Importo da collegare** immettere l'importo che si desidera collegare se è inferiore all'importo originale.  

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo totale da collegare per stornare tutti i movimenti coinvolti, ad esempio quando il valore del campo **Saldo** è zero.
7. Scegliere il pulsante **OK**. Quando si registra la nota di credito di vendita, viene applicata ai documenti di vendita registrati.

    Dopo avere creato o modificato le righe della nota di credito di vendita e avere specificato le applicazioni singole o multiple, è possibile passare alla registrazione della nota di credito di vendita.   
8. Scegliere l'azione **Registra e invia**.  

Viene visualizzata la finestra di dialogo **Registra e invia conferma** contenente il metodo di invio preferito del cliente. È possibile modificare il metodo di invio scegliendo il pulsante di ricerca per il campo **Invia documento a**. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).  

I documenti di vendita registrati che sono stati collegati alla nota di credito sono ora stornati ed è possibile creare un pagamento del rimborso per il cliente. La nota di credito di vendita viene rimossa e sostituita con un nuovo documento nell'elenco delle note di credito di vendita registrate.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Per creare una nota di credito di vendita copiando una fattura di vendita registrata
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Note credito vendita** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo** per aprire una nuova nota di credito di vendita vuota.
3. Nel campo **Cliente** immettere il nome di un cliente esistente.
4. Scegliere l'azione **Copia documento**.
5. Nella pagina **Copia documento vendita**, nel campo **Tipo di documento**, selezionare **Fattura registrata**.
6. Selezionare il campo **Nr. documento** per aprire la pagina **Fatture vendita registrate** e selezionare la fattura di vendita registrata contenente le righe da stornare.
7. Selezionare la casella di controllo **Ricalcola righe** se si desidera che le righe copiate della fattura di vendita registrata vengano aggiornate con le modifiche al prezzo dell'articolo e al costo unitario poiché la fattura è stata registrata.
8. Scegliere il pulsante **OK**. Le righe della fattura copiate vengono inserite nella nota di credito vendite.
9. Completare la nota di credito di vendita come descritto nella sezione "Per creare una nota di credito di vendita da una fattura di vendita registrata" del presente argomento.

## <a name="to-create-a-sales-return-order-based-on-one-or-more-a-posted-sales-documents"></a>Per creare un ordine di reso da vendita sulla base di uno o più documenti di vendita registrati
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di reso vendita** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**.
4. Nella Scheda dettaglio **Righe**, compilare le righe manualmente oppure copiare le informazioni da altri documenti per compilare le righe automaticamente:

    - Utilizzare la funzione **Ottieni righe documento registrato da stornare** per copiare una o più righe da uno o più documenti registrati. Questa funzione consente di stornare sempre esattamente i costi dalle righe del documento registrato. Questa funzionalità è descritta nei passaggi seguenti.    
    - Utilizzare la funzione **Copia documento** per copiare un documento esistente nell'ordine di reso. Utilizzare questa funzione per copiare l'intero documento. Può essere un documento registrato o un documento non ancora registrato. Questa funzione consente lo storno esatto costo solo quando la casella di controllo **Storno esatto costo obblig.** è selezionata nella pagina **Setup contabilità clienti**.  

5. Scegliere l'azione **Ottieni righe documento registrato da stornare**.
6. Nella parte superiore della pagina **Righe documento vendita registrate** selezionare la casella di controllo **Mostra solo righe reversibili** se si desidera visualizzare solo le righe associate a quantità non ancora rese. Se, ad esempio, è già stata resa una quantità della fattura di vendita registrata, potrebbe essere preferibile non rendere tale quantità in un nuovo documento di reso vendita.

    > [!NOTE]  
    >  Questo campo è valido solo per righe di spedizioni registrate e di fatture registrate, ma non per righe di resi registrati o di note di credito registrate.

    Nella parte sinistra della pagina sono elencati i diversi tipi di documento, mentre il numero tra parentesi indica il numero di documenti disponibili per ogni tipo di documento.

7. Nel campo **Filtro tipo documento** selezionare il tipo di righe documento registrate che si intende utilizzare.  
8. Selezionare le righe che si desidera copiare nel nuovo documento.  

    > [!NOTE]  
    >  Se si utilizza CTRL+A per selezionare tutte le righe, vengono copiate tutte le righe incluse nel filtro impostato, ma viene ignorato il filtro **Mostra solo righe reversibili**. Si supponga, ad esempio, di avere filtrato le righe in base a un particolare numero di documento con due righe, una delle quali è già stata completamente resa. Anche se si seleziona il campo **Mostra solo righe reversibili**, se si preme CTRL+A per copiare tutte le righe, vengono copiate entrambe le righe anziché solo quella non ancora stornata.  

9. Scegliere **OK** per copiare le righe nel nuovo documento.  

    Si verificheranno i processi seguenti:  

    -   Per le righe del documento registrato di tipo **Articolo**, viene creata una nuova riga che rappresenta una copia della riga del documento registrato, con la quantità che non è ancora stata stornata. Il campo **Collega-da mov. art.** viene automaticamente compilato con il numero del movimento contabile articolo presente nella riga del documento registrata.  

    -   Per le righe del documento registrato non di tipo **Articolo**, ad esempio addebiti articoli, viene creata una nuova riga che rappresenta una copia della riga del documento registrato originale.  

    -   Viene calcolato il valore del campo **Costo unitario (VL)** nella nuova riga in base ai costi nei movimenti contabili articoli corrispondenti.  

    -   Se il documento copiato è una spedizione registrata, un carico registrato, un carico da reso registrato o una spedizione di reso registrata, il prezzo unitario viene calcolato automaticamente in base alla scheda articolo.  

    -   Se il documento copiato è una nota di credito o una fattura registrata, il prezzo unitario, gli sconti fattura e gli sconti riga vengono copiati dalla riga del documento registrato.  

    -   Se la riga del documento registrato include righe di tracciabilità articolo, il campo **Collega-da mov. art.** nelle righe di tracciabilità articolo viene compilato con i numeri dei movimenti contabili articoli appropriati indicati nelle righe di tracciabilità articolo registrate.  

     Quando si copia da una fattura o una nota di credito registrata, gli sconti fattura e gli sconti riga pertinenti vengono copiati come validi al momento della registrazione del documento dalla riga del documento registrato nella riga del nuovo documento. Si noti, tuttavia, che se l'opzione **Calcola sconto fatt.** è attivata nella pagina **Setup contabilità clienti e vendite** , lo sconto fattura verrà calcolato quando si registra la riga del nuovo documento. È possibile, pertanto, che l'importo riga per la nuova riga sia diverso da quello della riga del documento registrato, a seconda del nuovo calcolo dello sconto fattura.  

     > [!NOTE]  
     >  Se parte della quantità della riga del documento registrato è già stata stornata, venduta o consumata, viene creata una riga solo per la quantità rimanente in magazzino o non ancora resa. Se l'intera quantità della riga del documento registrato è già stata stornata, non viene creata una nuova riga.  
     >   
     >  Se il flusso delle merci nel documento registrato corrisponde a quello nel nuovo documento, viene creata una copia della riga del documento registrato originale nel nuovo documento. Il campo **Collega-da mov. art.** non viene compilato perché in questo caso, lo storno esatto costo non è possibile. Se, ad esempio, si utilizza la funzione **Ottieni righe documento registrato da stornare** per ottenere una riga di nota di credito vendita registrata per una nuova nota di credito vendita, nella nuova nota di credito viene copiata esclusivamente la riga di nota di credito registrata originale.  

10. Nella pagina **Ordine reso di vendita**, nel campo **Cod. causa di reso** di ciascuna riga, selezionare il motivo del reso.
11. Scegliere l'azione **Registra**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Per creare un ordine di vendita sostitutivo da un reso dell'ordine di vendita
Si potrebbe decidere di compensare un cliente per un articolo venduto sostituendo l'articolo. La sostituzione può essere effettuata con lo stesso articolo o con un articolo differente. Questa situazione potrebbe presentarsi, ad esempio, se è stato erroneamente spedito l'articolo sbagliato.  

1. Nella pagina **Ordine reso di vendita** per un processo di reso attivo, su una riga vuota, creare un movimento negativo per l'articolo in sostituzione immettendo un importo negativo nel campo **Quantità**.  
2. Scegliere l'azione **Sposta righe negative**.
3. Nella pagina **Muovi righe vendite negative** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**. La riga negativa per l'articolo in sostituzione verrà eliminata dall'ordine di reso vendita e inserita in una nuova pagina **Ordine vendita**. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Per creare documenti relativi al reso da un ordine di reso vendita
È possibile creare automaticamente ordini di vendita di sostituzione, ordini di reso acquisto e ordini di acquisto di sostituzione durante il processo di reso da vendita. Ciò risulta utile, ad esempio, in situazioni in cui si desidera gestire articoli coperti da garanzia del fornitore.

1. Nella pagina **Ordine reso di vendita** per un processo di reso attivo, scegliere l'azione **Crea documenti collegati-resi**.
2. Nel campo **Nr. fornitore**, immettere il numero di un fornitore se si desidera creare automaticamente i documenti del fornitore.
3. Se è necessario rendere un articolo al fornitore, selezionare la casella di controllo **Crea ordini reso acquisto**.
4. Se è necessario ordinare un articolo dal fornitore, selezionare la casella di controllo **Crea ordini di acquisto**.
5. Se è necessario creare un ordine di vendita di sostituzione, selezionare la casella di controllo **Crea ordine di vendita**.

## <a name="to-create-a-restock-charge"></a>Per creare una spesa di ristoccaggio
Si potrebbe decidere di addebitare al cliente una commissione di ristoccaggio per coprire i costi di gestione fisica della resa dell'articolo. Ciò si potrebbe verificare, ad esempio, se il cliente ha per sbaglio ordinato un articolo errato oppure ha cambiato idea in seguito alla ricezione dell'articolo venduto.

È possibile registrare questo costo aumentato come addebito articolo in una nota di credito o in un ordine di reso e assegnarlo alla spedizione registrata. Di seguito sono descritte le procedure per un ordine di reso da vendita, ma gli stessi passaggi si applicano a una nota di credito di vendita.

1. Aprire la pagina **Ordine reso vendita** per un processo di reso attivo.
2. In una nuova riga selezionare **Addebito (Articolo)** nel campo **Tipo**.  
3. Compilare i campi relativi a qualsiasi riga di addebito dell'articolo. Per ulteriori informazioni, vedere [Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md).  

Durante la registrazione dell'ordine di reso da vendita, la spesa di ristoccaggio viene aggiunta all'importo del movimento di vendita corrispondente. In questo modo è possibile mantenere una valutazione precisa del magazzino.  

## <a name="to-create-a-sales-allowance"></a>Per creare un abbuono di vendita
È possibile inviare a un cliente una nota di credito con una riduzione di prezzo nel caso in cui il cliente abbia ricevuto articoli leggermente danneggiati oppure in ritardo.  
È possibile registrare questo prezzo ridotto come addebito articolo in una nota di credito o in un ordine di reso e assegnarlo alla spedizione registrata. Di seguito sono descritte le procedure per una nota di credito di vendita, ma gli stessi passaggi si applicano a un ordine di reso da vendita.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Note credito vendita** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo** per aprire una nuova nota di credito di vendita vuota.
3. Compilare la testata della nota di credito con le informazioni relative al cliente cui si intende riconoscere l'abbuono.  
4. Nel campo **Tipo** della Scheda dettaglio **Righe** selezionare **Addebito (Articolo)**.  
5.  Nel campo **Nr.** selezionare il valore di addebito articolo appropriato.  
     È possibile creare un numero di addebito articolo particolare in cui includere gli abbuoni.  
6.  Nel campo **Quantità** immettere **1**.  
7.  Nel campo **Prezzo Unitario** immettere l'importo dell'abbuono.  
8.  Assegnare l'abbuono di vendita come addebito articolo agli articoli nella spedizione registrata. Per ulteriori informazioni, vedere [Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md). Dopo avere assegnato l'abbuono, tornare alla pagina **Nota credito**.  

Durante la registrazione dell'ordine di reso da vendita, l'abbuono viene aggiunto all'importo del movimento di vendita corrispondente. In questo modo è possibile mantenere una valutazione precisa del magazzino.

## <a name="to-combine-return-receipts"></a>Per combinare carichi da reso
È possibile cumulare carichi da reso se il cliente restituisce più articoli che rientrano in più ordini di reso da vendita.  

Al momento del carico degli articoli nella warehouse, i relativi ordini di reso da vendita vengono registrati come ricevuti. In tal modo vengono creati i carichi da reso registrati.  

Al momento della fatturazione al cliente, invece di fatturare ciascun ordine di reso separatamente, è possibile creare una nota di credito di vendita e copiare automaticamente in questo documento le righe di carico da reso registrate. Sarà quindi possibile registrare la nota di credito di vendita e fatturare tutti gli ordini di reso da vendita aperti in una volta sola.  

Per cumulare carichi da reso, è necessario selezionare la casella di controllo **Fatt. cumulative** nella pagina **Scheda cliente**.  

### <a name="to-manually-combine-return-receipts"></a>Per cumulare manualmente i carichi da reso  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Nota credito vendita** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**.  
4. Scegliere l'azione **Prendi righe carico da reso**.  
5. Selezionare le righe di carico da reso che si desidera includere nella nota di credito:  

    -   Per inserire tutte le righe, selezionare tutte le righe, quindi fare clic su **OK**.  

    -   Per inserire righe specifiche, selezionare le righe, quindi fare clic su **OK**.  

6.  Se viene selezionata una riga di spedizione errata o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella nota di credito ed eseguire nuovamente la funzione **Prendi righe carico da reso**.  
7.  Contabilizzare la fattura.  

### <a name="to-automatically-combine-return-receipts"></a>Per combinare automaticamente carichi da reso  
È possibile cumulare automaticamente i carichi da reso, nonché registrare automaticamente le note di credito utilizzando la funzione **Cumula carichi da reso**.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cumula carichi da reso** e quindi scegliere il collegamento correlato.
2. Nella pagina **Cumula carichi da reso**, compilare i campi per selezionare i carichi da reso corrispondenti.
3. Selezionare la casella di controllo **Registra note di credito**. In caso contrario, è necessario registrare manualmente le note di credito di acquisto risultanti.
4.  Scegliere il pulsante **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Per rimuovere un ordine di reso ricevuto e fatturato  
Quando si fatturano carichi da reso in questo modo, gli ordini di reso da cui sono stati registrati i carichi da reso vengono mantenuti, anche se sono già stati completamente ricevuti e fatturati.  

Quando i carichi da reso vengono cumulati in una nota di credito e registrati, per le righe accreditate viene creata una nota di credito vendita registrata. Il campo **Quantità fatturata** dell'ordine di reso vendita di origine viene aggiornato in base alla quantità fatturata.   
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina ordini di reso vend. fatturati** e quindi selezionare il collegamento correlato.  
2.  Specificare nel campo del filtro **Nr.** quali ordini di reso eliminare.  
3.  Scegliere il pulsante **OK**.  

In alternativa, eliminare i singoli ordini di reso vendita manualmente.   

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

