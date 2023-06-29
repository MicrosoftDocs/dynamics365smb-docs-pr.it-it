---
title: Elaborare i resi o gli annullamenti vendite
description: 'Descrive come creare una nota di credito di vendita per elaborare una restituzione, una cancellazione o un rimborso per articoli o servizi per i quali hai ricevuto il pagamento.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: edupont
---
# <a name="process-sales-returns-or-cancellations"></a><a name="process-sales-returns-or-cancellations"></a>Elaborare i resi o gli annullamenti vendite

Se un cliente desidera restituire gli articoli o ottenere il rimborso degli articoli o dei servizi che gli sono stati venduti e che ha pagato, è necessario creare e registrare una nota di credito di vendita in cui viene specificata la modifica richiesta. Per includere le informazioni corrette della fattura di vendita, potete fare quanto segue:  

- Creare la nota di credito di vendita direttamente dalla fattura di vendita registrata.
- Creare una nuova nota di credito di vendita con le informazioni della fattura copiate.

Se hai bisogno di un maggiore controllo del processo di ritorno delle vendite, come i documenti di magazzino per la gestione degli articoli, o una migliore visione d'insieme quando ricevi articoli da più documenti di vendita con un ritorno delle vendite, allora puoi creare ordini di ritorno delle vendite. Un ordine di restituzione delle vendite emette automaticamente la relativa nota di credito di vendita e altri documenti relativi alla restituzione, come un ordine di vendita sostitutivo, se necessario. Per maggiori informazioni, vedi [Elabora gli ordini di restituzione delle vendite](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Se una fattura di vendita registrata non è stata ancora pagata, è possibile utilizzare la funzione **Rettifica** o **Annulla** nella fattura di vendita registrata per stornare le transazioni. Queste funzionano solo per le fatture non pagate e non supportano i resi o le cancellazioni parziali. Per ulteriori informazioni, vedere [Correggere o annullare le fatture di vendita non pagate](sales-how-correct-cancel-sales-invoice.md).

Un reso o un risarcimento può essere correlato solo ad alcuni degli articoli o dei servizi nella fattura di vendita originale. In questo caso, è necessario modificare le informazioni nelle righe della nota di credito di vendita o dell'ordine di reso da vendita. Quando si registra la nota di credito di vendita o l'ordine di reso da vendita, i documenti di vendita influenzati dalla variazione vengono stornati ed è possibile creare un pagamento di rimborso per il cliente. Per ulteriori informazioni, vedere [Effettuare i pagamenti](payables-make-payments.md).  

La registrazione della nota di credito annullerà anche tutti gli addebiti articolo assegnati al documento registrato, in modo che i movimenti valorizzazione articolo siano identici a prima dell'assegnazione dell'addebito articolo.

> [!NOTE]
> Gli aspetti contabili dei resi di vendita, come i pagamenti ai clienti come rimborso, sono considerati lavori contabili e non sono descritti qui. Per ulteriori informazioni, vedere [Gestione della contabilità fornitori](payables-manage-payables.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Per creare una nuova nota di credito di vendita da una fattura di vendita registrata

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , immetti **Fatture di vendita registrate**, quindi scegli il collegamento correlato.  
2. Nella pagina **Fatture di vendita registrate**, seleziona la fattura di vendita registrata che vuoi annullare, scegli l'azione **Annulla** e poi scegli l'azione **Crea nota di credito correttiva** .

    Nell'intestazione della nota di credito di vendita sono incluse alcune informazioni contenute nella fattura di vendita registrata. Tali informazioni possono, ad esempio, essere sostituite da nuove informazioni che riflettono il contratto di reso.  
3. Modificare le informazioni nelle righe in base al contratto, quali il numero di articoli resi o l'importo da rimborsare.
4. Scegli l'azione **Prepara** e poi scegli l'azione **Applica voci** .
5. Nella pagina **Collega movimenti clienti**, selezionare la riga con il documento di vendita registrato a cui si desidera collegare la nota di credito di vendita, quindi scegliere l'azione **Collega-a ID**.

    L'identificativo della nota di credito di vendita viene visualizzato nel campo **Collega-a ID**.
6. Nel campo **Importo da collegare** immettere l'importo che si desidera collegare se è inferiore all'importo originale.  

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo totale da collegare per stornare tutti i movimenti coinvolti, ad esempio quando il valore del campo **Saldo** è zero.
7. Scegliere il pulsante **OK**. Quando si registra la nota di credito di vendita, viene applicata ai documenti di vendita registrati.

    Dopo avere creato o modificato le righe della nota di credito di vendita e avere specificato le applicazioni singole o multiple, è possibile passare alla registrazione della nota di credito di vendita.  
8. Scegli l'azione **Registrazione**, poi scegli l'azione **Registra e invia**.  

Viene visualizzata la finestra di dialogo **Registra e invia conferma** contenente il metodo di invio preferito del cliente. È possibile modificare il metodo di invio scegliendo il pulsante di ricerca per il campo **Invia documento a**. Per ulteriori informazioni, vedere [Impostare profili di invio documenti](sales-how-setup-document-send-profiles.md).  

I documenti di vendita registrati che sono stati collegati alla nota di credito sono ora stornati ed è possibile creare un pagamento del rimborso per il cliente. La nota di credito di vendita viene rimossa e sostituita con un nuovo documento nell'elenco delle note di credito di vendita registrate.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Per creare una nota di credito di vendita copiando una fattura di vendita registrata

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Note credito vendita**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo** per aprire una nuova nota di credito di vendita vuota.
3. Nel campo **Nome del cliente**, inserite il nome di un cliente esistente.
4. Scegli l'azione **Prepara**, poi scegli l'azione **Copia documento** .
5. Nella pagina **Copia documento vendita**, nel campo **Tipo di documento**, selezionare **Fattura registrata**.
6. Scegli il campo **N. documento** per aprire la pagina **Fatture di vendita registrate** e poi seleziona il record della fattura di vendita registrata che contiene le righe che vuoi invertire.
7. Selezionare la casella di controllo **Ricalcola righe** se si desidera che le righe copiate della fattura di vendita registrata vengano aggiornate con le modifiche al prezzo dell'articolo e al costo unitario poiché la fattura è stata registrata.
8. Scegliere il pulsante **OK**. Le righe della fattura copiate vengono inserite nella nota di credito vendite.
9. Completare la nota di credito di vendita come descritto in [Per creare una nota di credito di vendita da una fattura di vendita registrata](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-allowance"></a><a name="to-create-a-sales-allowance"></a>Per creare un abbuono di vendita
È possibile inviare a un cliente una nota di credito con una riduzione di prezzo nel caso in cui il cliente abbia ricevuto articoli leggermente danneggiati oppure in ritardo.  
È possibile registrare questo prezzo ridotto come addebito articolo in una nota di credito o in un ordine di reso e assegnarlo alla spedizione registrata. Di seguito sono descritte le procedure per una nota di credito di vendita, ma gli stessi passaggi si applicano a un ordine di reso da vendita.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Note credito vendita**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo** per aprire una nuova nota di credito di vendita vuota.
3. Compilare la testata della nota di credito con le informazioni relative al cliente cui si intende riconoscere l'abbuono.  
4. Nel campo **Tipo** della Scheda dettaglio **Righe** selezionare **Addebito (Articolo)**.  
5. Nel campo **Nr.** selezionare il valore di addebito articolo appropriato.  
     È possibile creare un numero di addebito articolo particolare in cui includere gli abbuoni.  
6. Nel campo **Quantità** immettere **1**.  
7. Nel campo **Prezzo unitario tasse escluse**, immetti l'importo dell'indennità di vendita.  
8. Assegnare l'abbuono di vendita come addebito articolo agli articoli nella spedizione registrata. Per ulteriori informazioni, vedere [Utilizzare gli addebiti articolo al conto per i costi aggiuntivi commerciali](payables-how-assign-item-charges.md). Dopo avere assegnato l'abbuono, tornare alla pagina **Nota credito**.  

Durante la registrazione dell'ordine di reso da vendita, l'abbuono viene aggiunto all'importo del movimento di vendita corrispondente. In questo modo è possibile mantenere una valutazione precisa del magazzino.

## <a name="to-combine-return-receipts"></a><a name="to-combine-return-receipts"></a>Per combinare carichi da reso
È possibile cumulare carichi da reso se il cliente restituisce più articoli che rientrano in più ordini di reso da vendita.  

Al momento del carico degli articoli nella warehouse, i relativi ordini di reso da vendita vengono registrati come ricevuti. In tal modo vengono creati i carichi da reso registrati.  

Al momento della fatturazione al cliente, invece di fatturare ciascun ordine di reso separatamente, è possibile creare una nota di credito di vendita e copiare automaticamente in questo documento le righe di carico da reso registrate. Sarà quindi possibile registrare la nota di credito di vendita e fatturare tutti gli ordini di reso da vendita aperti in una volta sola.  

Per cumulare carichi da reso, è necessario selezionare la casella di controllo **Fatt. cumulative** nella pagina **Scheda cliente**.  

### <a name="to-manually-combine-return-receipts"></a><a name="to-manually-combine-return-receipts"></a>Per cumulare manualmente i carichi da reso

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note credito vendita**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi appropriati nella Scheda dettaglio **Generale**.  
4. Scegliere l'azione **Prendi righe carico da reso**.  
5. Selezionare le righe di carico da reso che si desidera includere nella nota di credito:  

    - Per inserire tutte le righe, selezionare tutte le righe, quindi fare clic su **OK**.  

    - Per inserire righe specifiche, selezionare le righe, quindi fare clic su **OK**.  
6.  Se viene selezionata una riga di spedizione errata o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella nota di credito ed eseguire nuovamente la funzione **Prendi righe carico da reso**.  
7.  Contabilizzare la fattura.  

### <a name="to-automatically-combine-return-receipts"></a><a name="to-automatically-combine-return-receipts"></a>Per combinare automaticamente carichi da reso

È possibile cumulare automaticamente i carichi da reso, nonché registrare automaticamente le note di credito utilizzando la funzione **Cumula carichi da reso**.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cumula carichi da reso**, quindi scegli il collegamento correlato.
2. Nella pagina **Cumula carichi da reso**, compilare i campi per selezionare i carichi da reso corrispondenti.
3. Selezionare la casella di controllo **Registra note di credito**. In caso contrario, è necessario registrare manualmente le note di credito di acquisto risultanti.
4. Scegliere il pulsante **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a><a name="to-remove-a-received-and-invoiced-return-order"></a>Per rimuovere un ordine di reso ricevuto e fatturato

Quando si fatturano carichi da reso in questo modo, gli ordini di reso da cui sono stati registrati i carichi da reso vengono mantenuti, anche se sono già stati completamente ricevuti e fatturati.  

Quando i carichi da reso vengono cumulati in una nota di credito e registrati, per le righe accreditate viene creata una nota di credito vendita registrata. Il campo **Quantità fatturata** dell'ordine di reso vendita di origine viene aggiornato in base alla quantità fatturata.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") icona, inserisci **Cancella ordini di ritorno delle vendite fatturate**, e poi scegli il link relativo.  
2. Specificare nel campo del filtro **Nr.** quali ordini di reso eliminare.  
3. Scegliere il pulsante **OK**.  

In alternativa, eliminare i singoli ordini di reso vendita manualmente.  

## <a name="inventory-costing"></a><a name="inventory-costing"></a>Costing di magazzino

Per mantenere la corretta valutazione del magazzino, in genere si desidera sistemare gli articoli restituiti nuovamente in magazzino al costo unitario con cui sono stati venduti e non al costo unitario corrente. Questa operazione è detta storno esatto costo.

Esistono due funzioni per assegnare automaticamente l'inversione esatta dei costi:  

|Funzione|Descrizione|  
|------------------|---------------------------------------|  
|La funzione **Ottieni righe documento registrato da stornare** nella pagina **Ordine di reso vendita**|Copia le righe di uno o più documenti registrati da stornare nell'ordine di reso da vendita. Per maggiori informazioni, vedere [Creare un ordine di restituzione delle vendite basato su uno o più documenti di vendita inviati](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|La funzione**Copia documento** nelle pagine **Nota credito vendita** e **Ordine di reso vendita**|Copia la testata e le righe di un documento registrato da stornare.<br /><br /> È necessario che la casella di controllo **Storno esatto costo obblig.** sia selezionata nella pagina **Setup contabilità clienti e vendite**.|

Per assegnare manualmente lo storno esatto costo, è necessario utilizzare il campo **Collega-da mov. art.** per ogni tipo di riga di documento di reso e selezionare il numero del movimento di vendita originale. In questo modo, l'ordine di reso vendita o la nota di credito di vendita verrà collegato al movimento di vendita originale e l'articolo verrà valutato in base al costo unitario originale.

Per ulteriori informazioni, vedere [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Vedi anche

[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Elaborare i resi o gli annullamenti acquisti](purchasing-how-process-purchase-returns-cancellations.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
