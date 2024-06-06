---
title: Come stoccare gli articoli con gli stoccaggi magazzino
description: Informazioni su come utilizzare i documenti di stoccaggio di magazzino per registrare e contabilizzare le informazioni sullo stoccaggio e sul carico.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/19/2023
ms.custom: bap-template
ms.search.forms: '7375,'
---
# <a name="put-items-away-with-inventory-put-aways"></a>Eseguire lo stoccaggio con Stoccaggi Magazzino

In [!INCLUDE[prod_short](includes/prod_short.md)], la ricezione e lo stoccaggio degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in entrata|Richiesto carico|Richiesto stoccaggio|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino||Attivato|Di base: ordine per ordine.|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse|Attivato||Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni vedi [Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).

Questo articolo fa riferimento al metodo B nella tabella.

Quando l'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi, ma non l'elaborazione dei carichi, utilizza il documento **Stoccaggio magazzino** per registrare e contabilizzare le informazioni riguardanti lo stoccaggio e il carico per i documenti di origine. I documenti di origine in entrata includono ordini di acquisto, ordini di reso da vendita e trasferimenti in entrata.

> [!NOTE]
> Anche l'output di produzione e assemblaggio rappresenta documenti di origine in entrata. Per ulteriori informazioni sulla gestione dell'output di produzione e assemblaggio per i processi interni, vedi [Dettagli di progettazione: Flussi warehouse interni](design-details-internal-warehouse-flows.md).

È possibile creare uno stoccaggio in magazzino in tre modi:  

* Creare lo stoccaggio in magazzino direttamente dal documento di origine.  
* Crea gli stoccaggi in magazzino per più documenti di origine contemporaneamente utilizzando un processo batch.  
* Crea lo stoccaggio in due passaggi rilasciando prima il documento di origine per rendere gli articoli disponibili per lo stoccaggio. È possibile creare lo stoccaggio di magazzino in base al documento di origine utilizzando la pagina **Stoccaggio magazzino**.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Per creare uno stoccaggio magazzino dal documento origine

1. Nel documento di origine, che può essere un ordine di acquisto, un ordine di reso da vendita o un ordine di trasferimento in entrata, scegli l'azione **Crea stoccaggio / prelievo mag.**.  
2. Seleziona la casella di controllo **Crea stoccaggio mag.**.
3. Scegliere il pulsante **OK**. Verrà creato un nuovo stoccaggio di magazzino.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Per creare più stoccaggi in magazzino utilizzando un processo batch

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Crea stoccaggio/prelievo/movimento magazzino**, quindi seleziona il collegamento correlato. 
2. Nella Scheda dettaglio **Richiesta warehouse**, utilizzare i campi **Nr. origine** e **Documento origine** per filtrare determinati tipi di documenti oppure intervalli di numeri di documenti. Ad esempio, è possibile creare stoccaggi solo per gli ordini di acquisto.
3. Nella Scheda dettaglio **Opzioni** seleziona la casella di controllo **Crea stoccaggio mag.**.
4. Scegli il pulsante **OK**. Verranno creati gli stoccaggi magazzino specificati.

## <a name="to-create-the-put-away-in-two-steps"></a>Per creare lo stoccaggio in due passaggi

### <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Per richiedere uno stoccaggio magazzino emettendo il documento di origine

Quando si rilasciano ordini di acquisto, ordini di reso da vendita e ordini di trasferimento in entrata, gli articoli negli ordini diventano disponibili per lo stoccaggio. I passaggi seguenti descrivono come preparare gli articoli di un ordine di acquisto per essere stoccati.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.
2. Selezionare l'ordine di acquisto che si intende rilasciare, quindi scegliere l'azione **Rilascio**.  

### <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Per creare uno stoccaggio in magazzino in base al documento origine

Un addetto warehouse può creare un nuovo stoccaggio di magazzino in base al documento di origine rilasciato.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Stoccaggio in magazzino**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Documento origine**, selezionare il tipo di documento di origine per cui si esegue lo stoccaggio.  
4. Nel campo **Nr. origine** selezionare il documento di origine.  
5. In alternativa, scegliere l'azione **Prendi documento origine** per selezionare il documento da una lista di documenti di origine in entrata pronti per lo stoccaggio presso l'ubicazione.  
6. Selezionare il pulsante **OK** per compilare le righe di stoccaggio in base al documento di origine selezionato.  

## <a name="to-record-the-inventory-put-away"></a>Per registrare lo stoccaggio magazzino

1. Nella pagina **Stoccaggi magazzino** apri un documento di stoccaggio creato in precedenza.  
2. Nel campo **Codice collocazione** nelle righe di stoccaggio, le collocazioni in cui gli articoli devono essere stoccati sono suggerite sulla base della collocazione predefinita dell'articolo. Se necessario, puoi modificare la collocazione.  
3. Esegui lo stoccaggio e immetti la quantità effettiva stoccata nel campo **Qtà da Gestire**.

    Se è necessario inserire gli articoli relativi a una riga in più collocazioni, ad esempio perché la collocazione designata è piena, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.  
4. Dopo avere eseguito lo stoccaggio, scegli l'azione **Registra**.  

    * Registrare il carico delle righe del documento di origine che sono state stoccate
    * Se l'ubicazione prevede l'utilizzo di collocazioni, verranno inoltre creati movimenti warehouse per la registrazione delle modifiche delle quantità nelle collocazioni.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
