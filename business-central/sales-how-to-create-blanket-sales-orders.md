---
title: Utilizzare gli ordini di vendita programmati o gli ordini di acquisto
description: Gli ordini programmati vengono utilizzati quando un cliente si impegna ad acquistare grandi quantità che verranno consegnate con diverse spedizioni più piccole effettuate in un determinato periodo di tempo. Lo stesso vale per l'acquisto.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '507, 509, 6620, 6622, 6623, 9303, 9310'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="work-with-blanket-sales-orders-or-blanket-purchase-orders"></a>Utilizzare gli ordini di vendita programmati o gli ordini di acquisto programmati

Un ordine di vendita programmato rappresenta la struttura di un accordo a lungo termine fra la società e un cliente. Allo stesso modo, utilizzare gli ordini di acquisto programmati per gestire contratti a lungo termine tra l'utente e il fornitore.

Un ordine programmato viene in genere creato quando un cliente si impegna ad acquistare grandi quantità che verranno consegnate con diverse spedizioni più piccole effettuate in un determinato periodo di tempo. Gli ordini programmati riguardano spesso un solo articolo con date di consegna predefinite. Il motivo principale dell'utilizzo di un ordine programmato anziché di un ordine di vendita consiste nel fatto che le quantità immesse in un ordine programmato non hanno influenza sulla disponibilità dell'articolo e pertanto tali ordini possono essere utilizzati come prospetto per il monitoraggio, le previsioni e le pianificazioni.

Nell'ordine programmato ogni singola spedizione può essere impostata come riga di ordine, che è quindi possibile convertire in ordine di vendita al momento della spedizione.

È ad esempio possibile utilizzare un ordine di vendita programmato se un cliente ordina 1000 unità di un articolo ma richiede che vengano consegnate 250 unità ogni settimana per tutto il mese seguente.

> [!NOTE]
> Gli ordini di acquisto programmati sono simili agli ordini di vendita programmati. In questa documentazione vengono descritti solo gli ordini di vendita programmati.

## <a name="to-create-a-blanket-sales-order"></a>Per creare un ordine di vendita programmato

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita programmati**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Lasciare vuoto il campo **Data ordine**. Quando vengono creati i diversi ordini di vendita dall'ordine programmato, la data dell'ordine di vendita viene impostata sulla data del lavoro effettiva.
5. Nella Scheda dettaglio **Righe** creare righe separate per ogni spedizione. Se, ad esempio, un cliente desidera che 1000 unità vengano divise equamente per quattro settimane, immettere quattro righe separate, ognuna per 250 unità.  

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Per creare un ordine di vendita da un ordine di vendita programmato

1. Per creare un ordine per una delle righe nell'ordine di vendita programmato, rimuovere la quantità dal campo **Qtà da spedire** di tutte le righe che al momento non si desidera spedire.  
2. Per creare gli ordini, scegliere l'azione **Crea ordine** e quindi **Sì**. Verrà visualizzato un messaggio che informa che all'ordine programmato è stato assegnato un numero di ordine. Si osservi che l'ordine programmato non è stato eliminato.  
3. Scegliere il pulsante **OK**.  
4. Per visualizzare i risultati dei passaggi precedenti, scegliere l'azione **Riga**, l'azione **Righe non registrate** e l'azione **Ordini**.  
5. Nella pagina **Righe vendita** selezionare l'ordine di vendita appropriato e scegliere l'azione **Riga** e l'azione **Mostra documento**.  

Quanto segue si applica agli ordini di vendita creati da ordini di vendita programmati:  

- Dopo la conversione dell'ordine programmato in un ordine di vendita, l'ordine di vendita contiene tutte le righe dell'ordine programmato. Le righe in cui la quantità indicata nel campo **Qtà da spedire** è stata eliminata vengono visualizzate, ma il relativo campo **Quantità** è vuoto. È possibile mantenere queste righe, modificarle o eliminarle.  
- È importante ricordare che la quantità della riga dell'ordine di vendita non deve essere superiore alla quantità associata alla riga dell'ordine programmato. In caso contrario, non sarà possibile registrare l'ordine di vendita.  
- Quando l'ordine di vendita viene registrato come spedito e/o fatturato, i campi **Quantità spedita** e **Quantità fatturata** vengono aggiornati nell'ordine programmato correlato.  
- Quando l'ordine viene creato da un ordine programmato, il numero dell'ordine programmato e il numero di riga vengono registrati come proprietà delle righe di vendita.  
- Quando gli ordini di vendita non vengono creati direttamente dall'ordine programmato, ma sono comunque correlati a esso, è possibile creare un collegamento tra un ordine di vendita e un ordine programmato immettendo il numero dell'ordine programmato associato nel campo **Nr. ordine programmato** nella riga dell'ordine di vendita.  
- Dopo avere creato un ordine di vendita per la quantità totale di una riga di ordine programmato, non è possibile creare altri ordini di vendita per la stessa riga. Agli utenti non è consentito immettere una quantità nel campo **Qtà da spedire**. Se, tuttavia, è necessario aggiungere ulteriori quantità a un ordine programmato, è possibile aumentare il valore del campo **Quantità**, quindi creare ulteriori ordini.  
- L'ordine di vendita programmato fatturato rimane nel sistema fino a quando non viene eliminato, eliminando i singoli ordini programmati o eseguendo il processo batch **Elimina ord. ven. progr. fatt.**.  
- Se un cliente è anche registrato come contatto nell'area di applicazione Marketing ed è stato specificato un codice modello di interazione per l'ordine di vendita programmato nella pagina **Setup marketing**, viene registrata un'interazione nella tabella Mov. log interazione quando si seleziona **Stampa** per stampare l'ordine di vendita programmato.

## <a name="to-view-the-status-of-a-blanket-sales-order"></a>Per visualizzare lo stato di un ordine di vendita programmato

È possibile visualizzare lo stato di un ordine di vendita programmato nella pagina **Statistiche ordini vendita programmati**. Ciò può risultare utile quando si avvia la fatturazione dell'ordine creato dall'ordine di vendita programmato.  

1.  Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita programmati**, quindi scegli il collegamento correlato.  
2.  Selezionare un ordine di vendita programmato quindi scegliere l'azione **Statistiche**.  
3.  Nella pagina **Statistiche ordini vendita programmati**, nella Scheda dettaglio **Generale**, è possibile visualizzare le informazioni di riepilogo relative all'intero ordine in base alla quantità totale riportata nei vari **campi Quantità** delle righe dell'ordine di vendita programmato.  

- Nella Scheda dettaglio **Fatturazione** è possibile visualizzare le informazioni di riepilogo in base alla quantità totale riportata nei campi **Qtà da fatturare** delle righe dell'ordine di vendita programmato.  
- Nella Scheda dettaglio **Spedizione** è possibile visualizzare le informazioni di riepilogo in base alla quantità totale riportata nei campi **Qtà da ricevere** delle righe dell'ordine di vendita programmato.  
- Nella Scheda dettaglio **Pagamento anticipato** è possibile visualizzare informazioni di riepilogo relative agli importi prepagati.  
- Nella Scheda dettaglio **Fornitore** è possibile visualizzare le informazioni principali relative al fornitore.

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Per visualizzare le righe degli ordini di vendita programmati registrate e non registrate

Il collegamento tra l'ordine di vendita programmato e l'ordine di vendita di origine ed eventuali altri documenti di vendita, viene mantenuto dopo la registrazione come lista delle righe della fattura di vendita registrate e non registrate.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita programmati**, quindi scegli il collegamento correlato.
2. Aprire l'ordine di vendita programmato che si desidera visualizzare.
3. Per visualizzare i movimenti non registrati, selezionare la riga in questione, quindi scegliere l'azione **Riga** e l'azione **Righe non registrate**. Selezionare una delle seguenti opzioni.  

|Opzione|Description|
|--|--|
|**Ordini**|Specifica ordini aperti associati alla riga selezionata.|
|**Fatture**|Specifica fatture aperte associate alla riga selezionata. È possibile associare manualmente le fatture aperte a un ordine programmato immettendo il numero dell'ordine programmato nella riga della fattura di vendita.|
|**Ordini di reso**|Specifica ordini di reso aperti associati alla riga selezionata.|
|**Note di credito**|Specifica note di credito aperte associate alla riga selezionata.|

4. Per visualizzare i movimenti registrati, selezionare la riga in questione, quindi scegliere l'azione **Riga** e l'azione **Righe registrate**. Selezionare una delle seguenti opzioni.  

|Opzione|Description|
|---|----|
|**Spedizioni**|spedizioni registrate associate alla riga selezionata.|
|**Fatture**|fatture registrate associate alla riga selezionata.|
|**Carichi da reso**|carichi da reso registrati associati alla riga selezionata.|
|**Note di credito**|note di credito registrate associate alla riga selezionata.|

5. Nella pagina **Righe acquisto** scegliere l'azione **Mostra documento** per visualizzare il movimento.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Vendite](sales-manage-sales.md)  
[Creare ordini di assemblaggio programmati](assembly-how-to-create-blanket-assembly-orders.md)  
[Setup Vendite](sales-setup-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
