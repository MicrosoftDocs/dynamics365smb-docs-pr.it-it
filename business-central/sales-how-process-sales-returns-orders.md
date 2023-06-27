---
title: Elaborare gli ordini di restituzione delle vendite
description: 'Descrive come creare un ordine di restituzione delle vendite per elaborare una restituzione, una cancellazione o un rimborso per articoli o servizi per i quali si è ricevuto il pagamento.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/08/2021
ms.author: edupont
---
# <a name="process-sales-return-orders" />Elaborare gli ordini di restituzione delle vendite

Se hai bisogno di un maggiore controllo del processo di ritorno delle vendite, come i documenti di magazzino per la gestione degli articoli, o una migliore visione d'insieme quando ricevi articoli da più documenti di vendita con un ritorno delle vendite, allora puoi creare ordini di ritorno delle vendite. Un ordine di reso da vendita genera automaticamente la nota di credito di vendite e altri documenti correlati ai resi, ad esempio un ordine di vendita di sostituzione, se necessario.

Oltre alla fattura di vendita registrata originale, è possibile collegare la nota di credito di vendita o l'ordine di reso da vendita ad altri documenti di vendita, ad esempio un'altra fattura di vendita registrata, in quanto il cliente restituisce anche gli articoli consegnati con la fattura.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents" />Creare un ordine di ritorno delle vendite basato su uno o più documenti di vendita inviati

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini reso vendita**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**.
4. Nella Scheda dettaglio **Righe**, compilare le righe manualmente oppure copiare le informazioni da altri documenti per compilare le righe automaticamente:

    - Utilizzare la funzione **Ottieni righe documento registrato da stornare** per copiare una o più righe da uno o più documenti registrati. Questa funzione consente di stornare sempre esattamente i costi dalle righe del documento registrato. Questa funzionalità è descritta nei passaggi seguenti.    
    - Utilizzare la funzione **Copia da documento** per copiare un documento esistente nell'ordine di reso. Utilizzare questa funzione per copiare l'intero documento. Può essere un documento registrato o un documento non ancora registrato. Questa funzione consente lo storno esatto costo solo quando la casella di controllo **Storno esatto costo obblig.** è selezionata nella pagina **Setup contabilità clienti**.  

5. Scegli l'azione **Elabora**, poi scegli l'azione **Ottieni linee di documenti pubblicati per invertire** .
6. Nella parte superiore della pagina **Righe documento vendita registrate** selezionare la casella di controllo **Mostra solo righe reversibili** se si desidera visualizzare solo le righe associate a quantità non ancora rese. Se, ad esempio, è già stata resa una quantità della fattura di vendita registrata, potrebbe essere preferibile non rendere tale quantità in un nuovo documento di reso vendita.

    > [!NOTE]  
    >  Questo campo è valido solo per righe di spedizioni registrate e di fatture registrate, ma non per righe di resi registrati o di note di credito registrate.

    Nella parte sinistra della pagina sono elencati i diversi tipi di documento, mentre il numero tra parentesi indica il numero di documenti disponibili per ogni tipo di documento.

7. Nel campo **Filtro tipo documento** selezionare il tipo di righe documento registrate che si intende utilizzare.  
8. Selezionare le righe che si desidera copiare nel nuovo documento.  

    > [!NOTE]  
    >  Se usi <kbd>CTRL</kbd>+<kbd>A</kbd> per selezionare tutte le righe, vengono copiate tutte le righe incluse nel filtro impostato, ma viene ignorato il filtro **Mostra solo righe reversibili**. Si supponga, ad esempio, di avere filtrato le righe in base a un particolare numero di documento con due righe, una delle quali è già stata completamente resa. Anche se selezioni il campo **Mostra solo righe reversibili**, se selezioni <kbd>CTRL</kbd>+<kbd>A</kbd> per copiare tutte le righe, vengono copiate entrambe le righe anziché solo quella non ancora stornata.  

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

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order" />Per creare un ordine di vendita sostitutivo da un reso dell'ordine di vendita
Si potrebbe decidere di compensare un cliente per un articolo venduto sostituendo l'articolo. La sostituzione può essere effettuata con lo stesso articolo o con un articolo differente. Questa situazione potrebbe presentarsi, ad esempio, se è stato erroneamente spedito l'articolo sbagliato.  

1. Nella pagina **Ordine reso di vendita** per un processo di reso attivo, su una riga vuota, creare un movimento negativo per l'articolo in sostituzione immettendo un importo negativo nel campo **Quantità**.  
2. Scegliere l'azione **Sposta righe negative**.
3. Nella pagina **Muovi righe vendite negative** compilare i campi secondo le necessità.
4. Scegliere il pulsante **OK**. La riga negativa per l'articolo in sostituzione verrà eliminata dall'ordine di reso vendita e inserita in una nuova pagina **Ordine vendita**. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order" />Per creare documenti relativi al reso da un ordine di reso vendita
È possibile creare automaticamente ordini di vendita di sostituzione, ordini di reso acquisto e ordini di acquisto di sostituzione durante il processo di reso da vendita. Ciò risulta utile, ad esempio, in situazioni in cui si desidera gestire articoli coperti da garanzia del fornitore.

1. Nella pagina **Ordine reso di vendita** per un processo di reso attivo, scegliere l'azione **Crea documenti collegati-resi**.
2. Nel campo **Nr. fornitore**, immettere il numero di un fornitore se si desidera creare automaticamente i documenti del fornitore.
3. Se è necessario rendere un articolo al fornitore, selezionare la casella di controllo **Crea ordini reso acquisto**.
4. Se è necessario ordinare un articolo dal fornitore, selezionare la casella di controllo **Crea ordini di acquisto**.
5. Se è necessario creare un ordine di vendita di sostituzione, selezionare la casella di controllo **Crea ordine di vendita**.

## <a name="to-create-a-restock-charge" />Per creare una spesa di ristoccaggio
Si potrebbe decidere di addebitare al cliente una commissione di ristoccaggio per coprire i costi di gestione fisica della resa dell'articolo. Ciò si potrebbe verificare, ad esempio, se il cliente ha per sbaglio ordinato un articolo errato oppure ha cambiato idea in seguito alla ricezione dell'articolo venduto.

È possibile registrare questo costo aumentato come addebito articolo in una nota di credito o in un ordine di reso e assegnarlo alla spedizione registrata. Quanto segue descrive questo per un ordine di restituzione delle vendite, ma gli stessi passi si applicano a un promemoria di credito di vendita.

1. Aprire la pagina **Ordine reso vendita** per un processo di reso attivo.
2. In una nuova riga selezionare **Addebito (Articolo)** nel campo **Tipo**.  
3. Compilare i campi relativi a qualsiasi riga di addebito dell'articolo. Per ulteriori informazioni, vedere [Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md).  

Durante la registrazione dell'ordine di reso da vendita, la spesa di ristoccaggio viene aggiunta all'importo del movimento di vendita corrispondente. In questo modo è possibile mantenere una valutazione precisa del magazzino.  

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also" />Vedi anche

[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
