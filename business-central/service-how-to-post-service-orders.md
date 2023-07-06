---
title: Come registrare gli ordini di assistenza
description: 'Dopo avere creato un ordine di assistenza, immesso tutte le informazioni necessarie e apportato le modifiche, è possibile registrarlo.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="post-service-orders-and-credit-memos"></a><a name="post-service-orders-and-credit-memos"></a><a name="post-service-orders-and-credit-memos"></a>Registrare note di credito e ordini di assistenza
Dopo avere creato un ordine di assistenza, immesso tutte le informazioni necessarie e apportato le modifiche, è possibile registrarlo. Per eseguire questa operazione, è necessario che l'ordine contenga almeno una riga di articolo in assistenza e una riga di assistenza. Se l'ordine contiene più di una riga di assistenza, tutte le righe verranno registrate contemporaneamente.  

Se si dispone di molti ordini di assistenza, è possibile risparmiare tempo utilizzando un processo batch per registrarli contemporaneamente. È possibile eseguire il processo batch da qualsiasi ordine di assistenza.

> [!Tip]
> Prima di registrare un documento di assistenza, è consigliabile utilizzare l'azione **Report test** per verificare se esistono errori o informazioni mancanti. Se sono presenti errori, è necessario risolvere il problema. È possibile stampare un nuovo report di test per verificare la correzione, quindi registrare il documento.

## <a name="to-post-a-service-order"></a><a name="to-post-a-service-order"></a><a name="to-post-a-service-order"></a>Per registrare un ordine di assistenza
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Aprire l'ordine di assistenza desiderato.  
3. Nella pagina **Ordine assistenza** selezionare una delle seguenti azioni.  

    |**Azione**|**Risultato**|  
    |------------------|----------------|  
    |**Report Test** | Tutte le parti del documento saranno controllate e i risultati saranno inseriti in un report. Se il report segnala degli errori o la mancanza di alcune informazioni, è necessario risolvere il problema. Stampare quindi il nuovo report test.|  
    |**Registra** | Registrazione dell'ordine senza la stampa di una spedizione o di una fattura.|  
    |**Registra e Stampa** | Registrazione dell'ordine e stampa di una spedizione (l'ordine viene spedito senza essere fatturato) oppure di una fattura (se l'ordine viene fatturato).|  
    |**Registra Batch** | Registrare più ordini di assistenza in una volta contemporaneamente.|  

4. Quando si registra l'ordine, è necessario specificare una delle seguenti opzioni per la modalità di registrazione dell'ordine.  

    |**Opzione di registrazione**|**Operazione**|  
    |------------------------|----------------|  
    |**Spedizione** | Registra la spedizione degli articoli.|  
    |**Fattura** | Fatturazione degli articoli già spediti.|  
    |**Spedizione e Fattura** | Fatturazione e spedizione degli articoli.|  
    |**Spedizione e consumo** | Registra la spedizione e il consumo nell'ordine. Vengono aggiornate inoltre le quantità relative sulle righe di assistenza dell'ordine e sul documento di spedizione di assistenza registrato in precedenza.|  

È possibile registrare il consumo solo se la riga contiene una quantità spedita ma non fatturata o consumata.  

Durante la registrazione dell'ordine, verranno creati i movimenti contabili e i documenti registrati corrispondenti. Verranno aggiornati i campi appropriati nel documento relativo all'ordine di assistenza.  

## <a name="to-batch-post-service-orders"></a><a name="to-batch-post-service-orders"></a><a name="to-batch-post-service-orders"></a>Per registrare gli ordini di assistenza tramite processo batch
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Registra batch**.  
3.  È possibile impostare un filtro per selezionare numeri d'ordine d'assistenza specifici o un intervallo di numeri d'ordine per eseguire il processo batch.  
4.  Selezionare **OK** per avviare il processo batch.  

## <a name="to-post-a-service-credit-memo"></a><a name="to-post-a-service-credit-memo"></a><a name="to-post-a-service-credit-memo"></a>Per registrare una nota di credito di assistenza
Dopo avere creato e compilato una nota di credito di assistenza, è possibile registrare la nota di credito. Se durante la registrazione vengono rilevati errori o informazioni mancanti, il processo verrà interrotto e verrà visualizzato un messaggio di errore.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note credito assistenza**, quindi scegli il collegamento correlato.  
2. Creare una nuova nota di credito di assistenza. Scegliere l'azione **Nuovo**.  
3. Compilare i campi necessari.  
4. Scegliere l'azione **Registra**. Se si desidera stampare la nota di credito contemporaneamente alla registrazione, scegliere l'azione **Registra e stampa**.  
5. Per testare le note di credito prima di registrarle, scegliere **Report test**. Quando si esegue il report, vengono verificate le date di registrazione specificate nel documento.  
6. Per registrare più note di credito di assistenza contemporaneamente. eseguire il processo batch **Registra batch note cr. assistenza**. Ciò rappresenta un vantaggio se vi è un gran numero di note di credito da registrare.  

> [!NOTE]  
>  Prima di registrare le note di credito mediante il processo batch, è importante immettere tutte le informazioni necessarie. In caso contrario la registrazione potrebbe non avvenire correttamente. Al termine della registrazione da parte del processo batch, verrà visualizzato un messaggio con il numero delle note di credito di assistenza registrate.  

## <a name="to-post-consumption-from-a-service-order"></a><a name="to-post-consumption-from-a-service-order"></a><a name="to-post-consumption-from-a-service-order"></a>Per registrare il consumo da un ordine di assistenza
La procedura seguente indica le modalità di registrazione degli articoli, delle ore e/o dei costi relativi alle risorse utilizzati per un'operazione di assistenza specifica che non verrà addebitata al cliente. Si noti che è possibile registrare articoli consumati, ore o costi solo per una spedizione registrata a cui non sono associati fatture o consumi registrati.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Aprire l' ordine di assistenza per cui registrare il consumo.  
3. Scegliere l'articolo in assistenza. Scegliere l'azione **Righe assistenza**.  
4. Individuare i movimenti necessari e specificare le quantità di cui si desidera registrare il consumo nel campo **Qtà da consumare**. La quantità non può essere maggiore della quantità già spedita né di quella rimanente, ma non fatturata dopo la fatturazione parziale della spedizione.  

    > [!NOTE]  
    >  Per registrare il consumo relativamente a una commessa, compilare i campi **Nr. commessa**, **Nr. task commessa** e **Tipo riga commessa** della riga di assistenza.  

5. Scegliere le righe da registrare e scegliere l'azione **Registra**. Nella pagina visualizzata selezionare **Spedizione e consumo**.  

L'assistenza viene registrata come parzialmente o completamente consumata, a seconda del valore nel campo **Qtà da consumare** e vengono creati i movimenti contabili pertinenti. I documenti di spedizione assistenza registrati in precedenza vengono inoltre aggiornati cronologicamente con le quantità consumate. Le quantità pertinenti verranno aggiornate nelle righe di assistenza dell'ordine.  

## <a name="to-post-shipments-from-service-orders"></a><a name="to-post-shipments-from-service-orders"></a><a name="to-post-shipments-from-service-orders"></a>Per registrare spedizioni da ordini di assistenza
Dopo avere specificato i dettagli relativi a un servizio di assistenza, è possibile rettificare e registrare le quantità degli articoli utilizzati, il tempo impiegato e i costi sostenuti. In [!INCLUDE[prod_short](includes/prod_short.md)] verranno apportate le modifiche necessarie per riflettere il nuovo stato del magazzino e lo stato corrente del processo di gestione dell'ordine specifico.  

Nella seguente procedura viene illustrato come registrare la spedizione di articoli nelle righe di assistenza in ubicazioni non impostate per richiedere la gestione in warehouse.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordine assistenza**, quindi scegli il collegamento correlato. 2. Nella pagina relativa all'ordine di assistenza selezionato, scegliere **Azioni**, **Ordine**, **Righe assistenza**.  
3. Nella pagina **Righe assistenza** individuare i movimenti appropriati e specificare la quantità da registrare nel campo **Qtà da spedire**.  

   > [!NOTE]  
   >  Il valore della quantità da spedire viene stabilito in base alla registrazione parziale o completa della spedizione. Se la spedizione è completa, il valore del campo **Qtà da spedire** deve corrispondere a quello specificato nel campo **Quantità**. Se invece si registra una spedizione parziale, è necessario specificare la quantità da spedire inizialmente. Se una parte dei servizi di assistenza dell'ordine sono già stati spediti, è necessario tenerne nota nel campo **Quantità spedita**. La quantità massima che è possibile immettere nel campo **Qtà da spedire** è costituita dal numero di unità non ancora spedite.  

4. Scegliere l'azione **Registra**. Nella pagina visualizzata, selezionare il pulsante **Spedizione**.

In [!INCLUDE[prod_short](includes/prod_short.md)] vengono creati i movimenti contabili, ovvero i movimenti garanzia, articolo, assistenza o C/G, generati i documenti di spedizione di assistenza registrati e aggiornati i campi corrispondenti nelle righe di assistenza dell'ordine relativo.  

Se l'ubicazione è impostata in modo da richiedere la gestione warehouse, la spedizione e la movimentazione degli articoli nelle righe di assistenza funzionano allo stesso modo di altri documenti di origine. La sola differenza sta nel fatto che gli articoli nelle righe di assistenza possono essere consumati esternamente o internamente e pertanto richiedono in due diverse funzioni di rilascio.  

Per ulteriori informazioni sugli articoli delle righe del servizio di spedizione nelle configurazioni warehouse avanzate, vai a Selezionare gli articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

## <a name="to-undo-posted-consumption"></a><a name="to-undo-posted-consumption"></a><a name="to-undo-posted-consumption"></a>Per annullare un consumo registrato
È possibile annullare il consumo negli ordini di assistenza. Ad esempio, perché è stato registrato per errore.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizioni assistenza registrate**, quindi scegli il collegamento correlato.  
2. Aprire la spedizione di assistenza registrata per cui è stato registrato il consumo errato.  
3. Scegliere l'azione **Righe spedizioni assistenza**.  
4. Scegliere le righe contenenti il consumo non corretto, quindi scegliere l'azione **Annulla consumo**.  

 Nei campi relativi alla quantità delle righe selezionate verrà inserita una riga di spedizione di assistenza di contropartita con valori negativi.  
  
> [!NOTE]  
>  Non è possibile annullare un consumo di assistenza se:  

>    * L'ordine di assistenza è stato chiuso.  
>    * È stato registrato nell'area Commesse e i movimenti contabili delle commesse sono stati collegati ad esso.  

## <a name="to-post-service-lines"></a><a name="to-post-service-lines"></a><a name="to-post-service-lines"></a>Per registrare le righe di assistenza
Se in un ordine di assistenza è necessario eseguire operazioni per un elevato periodo di tempo prima della registrazione, potrebbe essere opportuno registrare alcune righe di assistenza collegate, ad esempio per mantenere aggiornato il magazzino. Per eseguire la registrazione, è possibile specificare le quantità relative sulle righe da registrare. La registrazione delle righe può essere eseguita singolarmente o selezionando diverse righe contemporaneamente.  

Nella procedura seguente viene descritta la registrazione della spedizione direttamente da un ordine di assistenza nelle ubicazioni senza setup di gestione warehouse. Se l'ubicazione è impostata per richiedere la gestione warehouse, la registrazione della spedizione avviene in un documento di warehouse diverso, a seconda del setup dell'ubicazione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Aprire l'ordine di assistenza, quindi scegliere l'azione **Righe assistenza**.  
4. Sulle righe da registrare, compilare i campi **Qtà da spedire**, **Qtà da fatturare** e **Qtà da consumare**, in base alle modalità di registrazione delle righe.  
5. Scegliere l'azione **Registra**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche
[Pubblicazione nella gestione assistenza](service-service-posting.md)  
[Creare un ordine di assistenza](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
