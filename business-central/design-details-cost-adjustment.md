---
title: Dettagli di progettazione - Rettifica costo
description: 'La rettifica dei costi inoltra le modifiche dei costi dalle origini di costo ai destinatari di costo, in base al metodo di costing di un articolo, per fornire una valutazione di magazzino corretta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="design-details-cost-adjustment"></a>Dettagli di progettazione: Rettifica costo

Il principale scopo della rettifica dei costi è di inoltrare le modifiche dei costi dalle origini di costo ai destinatari di costo, in base al metodo di costing di un articolo, per fornire una valutazione di magazzino corretta.  

Un articolo può essere fatturato come venduto prima di essere fatturato come acquistato, in modo che il valore di magazzino registrato della vendita non corrisponde al costo di acquisto effettivo. La rettifica dei costi aggiorna il costo di COGS per i movimenti di vendita storici per verificarne la corrispondenza tra i costi delle transazioni in entrata a cui si applicano. Per ulteriori informazioni, vedere [Dettagli di progettazione: Collegamento articoli](design-details-item-application.md).  

Di seguito vengono indicati gli scopi secondari, o funzioni, della rettifica costo:  

* Fatturare ordini di produzione terminati:  

  * Modificare lo stato dei movimenti di valorizzazione da **Previsto** a **Effettivo**.  
  * Rimuovere i conti WIP. Per ulteriori informazioni, vedere [Dettagli di progettazione: Registrazione dell'ordine di produzione](design-details-production-order-posting.md).  
  * Registrare variazione. Per ulteriori informazioni, vedere [Dettagli progettazione: Scostamento](design-details-variance.md).  
  * Aggiornare il costo unitario nella scheda articolo.  

I costi di magazzino devono essere rettificati prima che i movimenti di valorizzazione correlati possano essere riconciliati con la contabilità generale. Per ulteriori informazioni, vedere [Dettagli di progettazione: Riconciliazione con la contabilità generale](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Rilevazione della rettifica

L'attività di rilevamento di eventuali necessità di rettifiche dei costi viene svolta principalmente dalla routine Item Jnl.-Post Line, mentre l'attività di calcolo e di generazione dei movimenti di rettifica viene eseguita dal processo batch **Rettifica costo - Mov. art.**.  

Per poter inoltrare i costi, il meccanismo di rilevamento determina quali origini hanno modificato i costi e a quali destinazioni devono essere inoltrati questi costi. In [!INCLUDE[prod_short](includes/prod_short.md)] sono disponibili le seguenti tre funzioni di rilevamento:  

* Mov. collegamento articoli  
* Rettifica costo medio cod. spedizioni Intrastat  
* Livello di ordine  

### <a name="item-application-entry"></a>Mov. collegamento articoli

La funzione di tracciabilità viene utilizzata per gli articoli che utilizzano i metodi di costing FIFO, LIFO, Standard e Specifico e per gli scenari di collegamenti fissi. Le funzioni della funzione sono le seguenti:  

* La rettifica dei costi è rilevata contrassegnando i movimenti contabili articoli di origine come *Mov. colleg. da rettif.* ogni volta che si registra un movimento contabile articoli o un movimento valorizzazione.  
* Il costo viene inoltrato in base alle catene di costi registrati nella tabella **Mov. collegamento articoli**.  

### <a name="average-cost-adjustment-entry-point"></a>Rettifica costo medio cod. spedizioni Intrastat

La funzione di rilevamento viene utilizzata per gli articoli che utilizzano il metodo di costing medio. Le funzioni della funzione sono le seguenti:  

* La rettifica dei costi viene rilevata contrassegnando un record nella tabella **Rettifica costo medio cod. spedizioni Intrastat** ogni volta che viene registrato un movimento valorizzazione.  
* Il costo viene inoltrato applicando i costi ai movimenti valorizzazione con una data di valutazione successiva.  

### <a name="order-level"></a>Livello di ordine

Questa funzione di rilevamento viene utilizzata in scenari di conversione, produzione e assemblaggio. Le funzioni della funzione sono le seguenti:  

* La rettifica dei costi viene rilevata contrassegnando l'ordine ogni volta che una risorsa o un materiale viene registrato come utilizzato o consumato.  
* Il costo viene inoltrato applicando i costi dalla risorsa o dal materiale ai movimenti di output associati allo stesso ordine.  

La funzione di livello di ordine viene utilizzata per rilevare le rettifiche nella registrazione di assemblaggi. Nel seguente grafico viene visualizzata la struttura dei movimenti di rettifica:  

![Flusso di voci nella rettifica dei costi.](media/design_details_assembly_posting_3.png "Flusso di voci nella rettifica dei costi")  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Rettifica costo automatica e rettifica costo manuale

La rettifica dei costi può essere effettuata in due modi:  

* Manualmente, tramite l'esecuzione del processo batch **Rettifica costo - Movimenti articoli**. È possibile eseguire questo processo batch per tutti gli articoli o solo per determinati articoli o categorie articolo. Questo processo batch effettua una rettifica dei costi per gli articoli in magazzino per i quali è stata effettuata una transazione in entrata, ad esempio un acquisto. Per gli articoli che utilizzano il metodo di costing medio, anche il processo batch esegue una rettifica se vengono create le transazioni in uscita.  
* Automaticamente, regolando i costi ogni volta che si registra una transazione di magazzino e quando termina un ordine di produzione. La rettifica dei costi viene eseguita solo per uno o più articoli specifici interessati dalla registrazione. Viene impostata quando si seleziona la casella di controllo **Rettifica costo automatica** nella pagina **Setup magazzino**.  

Si consiglia di eseguire la rettifica dei costi automaticamente al momento della registrazione perché i costi unitari vengono aggiornati con più frequenza e pertanto sono più precisi. Lo svantaggio consiste nel fatto che una frequente rettifica costo può influire negativamente sulle prestazioni del database.  

Poiché è importante mantenere aggiornato il costo unitario di un articolo, è consigliabile eseguire il processo batch **Rettifica costo - Movimenti articoli** il più spesso possibile, durante le ore non lavorative. In alternativa, utilizzare la rettifica costi automatica. In questo modo, il costo unitario degli articoli viene aggiornato giornalmente.  

A prescindere dall'esecuzione manuale o automatica della rettifica dei costi, il processo di rettifica e le relative conseguenze non cambiano. [!INCLUDE[prod_short](includes/prod_short.md)] calcola il valore della transazione in entrata e inoltra tale costo a tutte le transazioni in uscita, come le vendite o i consumi, collegati alla transazione in entrata. La rettifica dei costi crea movimenti di valorizzazione che contengono importi di rettifica e importi che si compensano per arrotondamento.  

I nuovi movimenti di valorizzazione dell'arrotondamento e della rettifica contengono la data di registrazione della fattura correlata. Le eccezioni si verificano se i movimenti di valorizzazione rientrano in un periodo contabile o in un periodo di magazzino chiuso o se la data di registrazione è antecedente alla data nel campo **Consenti registraz. da** della pagina **Setup contabilità generale**. In questo caso, il processo batch assegna la data di registrazione come la prima data del successivo periodo aperto.  

## <a name="adjust-cost---item-entries-batch-job"></a>Processo batch Rettifica costo - Mov. art.

Quando si esegue il processo batch **Rettifica costo - Movimenti articoli**, è possibile scegliere se eseguire tale processo per tutti gli articoli o solo per determinati articoli o categorie.  

> [!NOTE]  
> Si consiglia di eseguire sempre il processo batch per tutti gli articoli e utilizzare l'opzione filtro solo per ridurre il runtime del processo batch o per rettificare il costo di un determinato articolo.  

### <a name="example"></a>Esempio

Nell'esempio seguente viene mostrato che cosa accade se si registra un acquistato come ricevuto e fatturato in data 20-01-01. In secondo momento l'articolo venduto viene registrato come spedito e fatturato in data 01-15-20. Si eseguono quini di processi batch **Rettifica costo - Movimenti articoli** e **Registra costo magazzino in C/G**. Vengono creati i seguenti movimenti.  

#### <a name="value-entries-1"></a>Movimenti di valorizzazione (1)

|Data di registrazione|Tipo mov. articolo|Importo costo (effettivo)|Costo registrato in C/G|Quantità fatturata|Nr. movimento|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01-01-20|Acquisti|10,00|10,00|1|1|  
|01-15-20|Vendite|-10,00|-10,00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Movimenti di relazione nella C/G – Relazione Movimento Articolo (1)

|Nr. movimento C/G|Nr. movimento valorizzazione|Nr. registro C/G|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Movimenti C/G (1)

|Data di registrazione|Conti C/G|Numero di conto (demo en-US)|Importo|Nr. movimento|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Conto giac. magazzino]|2130|10,00|1|  
|01-01-20|[Conto costi diretti coll.]|7291|-10,00|2|  
|01-15-20|[Conto giac. magazzino]|2130|-10,00|3|  
|01-15-20|[Conto COGS]|7290|10,00|4|  

Successivamente, si registra un addebito articolo di acquisto correlato per VL 2,00 fatturato il 20-10-02. Si esegue il processo batch **Rettifica costo - Movimenti articoli** e successivamente il processo batch **Registra costo magazzino in C/G**. Il processo batch di rettifica costi modifica il costo della vendita di VL -2,00 e il processo batch **Registra costo magazzino in C/G** registra i nuovi movimenti di valorizzazione nella contabilità generale. Il risultato è il seguente.  

#### <a name="value-entries-2"></a>Movimenti di valorizzazione (2)

|Data di registrazione|Tipo mov. articolo|Importo costo (effettivo)|Costo registrato in C/G|Quantità fatturata|Rettifica|Nr. movimento|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|02-10-20|Acquisti|2.00|2.00|0|No|3|  
|01-15-20|Vendite|-2,00|-2,00|0|Sì|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Movimenti di relazione nella C/G – Relazione Movimento Articolo (2)

|Nr. movimento C/G|Nr. movimento valorizzazione|Nr. registro C/G|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Movimenti C/G (2)

|Data di registrazione|Conti C/G|Numero di conto (demo en-US)|Importo|Nr. movimento|  
|------------|-----------|------------------------|------|---------|  
|02-10-20|[Conto giac. magazzino]|2130|2.00|5|  
|02-10-20|[Conto costi diretti coll.]|7291|-2,00|6|  
|01-15-20|[Conto giac. magazzino]|2130|-2,00|7|  
|01-15-20|[Conto COGS]|7290|2.00|8|  

## <a name="automatic-cost-adjustment"></a>Rettifica costo automatica

Per impostare l'esecuzione automatica della rettifica dei costi quando si registra una transazione di magazzino, utilizzare il campo **Rettifica costo automatica** della pagina **Setup magazzino**. Questo campo consente di selezionare una data antecedente a quella di lavoro corrente nella quale si desidera che venga eseguita una rettifica automatica dei costi. Sono disponibili le seguenti opzioni:  

|Opzione|Description|
|------|-----------|
|Mai|I costi non vengono rettificati al momento della registrazione.|  
|Giorno|I costi vengono rettificati se la registrazione avviene entro un giorno dalla data del lavoro.|  
|Settimana|I costi vengono rettificati se la registrazione avviene entro una settimana dalla data del lavoro.|  
|Mese|I costi vengono rettificati se la registrazione avviene entro un mese dalla data del lavoro.|  
|Trimestre|I costi vengono rettificati se la registrazione avviene entro un trimestre dalla data del lavoro.|  
|Anno|I costi vengono rettificati se la registrazione avviene entro un anno dalla data del lavoro.|  
|Sempre|I costi vengono sempre rettificati durante la registrazione, indipendentemente dalla data di esecuzione dell'operazione.|  

La selezione che si effettua nel campo **Rettifica costo automatica** è importante per le prestazioni e per la precisione dei costi. Periodi di tempo più brevi, ad esempio **Giorno** o **Settimana**, influiscono meno sulle prestazioni del sistema, in quanto fissano un requisito più rigoroso per cui solo i costi registrati nell'ultimo giorno o nell'ultima settimana possono essere rettificati automaticamente. Ciò significa che la rettifica dei costi automatica non viene eseguita frequentemente e quindi influisce meno sulle prestazioni del sistema. Tuttavia, ciò significa anche che i costi unitari possono essere meno precisi.  

### <a name="example-1"></a>Esempio

Nel seguente esempio viene illustrato uno scenario di rettifica costo automatica:  

* Il 10 gennaio si registra un articolo acquistato come ricevuto e fatturato.  
* Il 15 gennaio si registra un ordine di vendita per l'articolo come spedito e fatturato.
* Il 5 febbraio si riceve una fattura per una spesa di trasporto sull'acquisto originale. Si registrano queste spese di spedizione, applicandole alla fattura di acquisto originale, e incrementando così il costo di acquisto originale.  

Se è stata impostata la rettifica dei costi automatica da applicare alle registrazioni che si verificano in un mese o un trimestre dalla data di lavoro corrente, la rettifica dei costi automatica verrà eseguita e il costo dell'acquisto verrà inoltrato alla vendita.  

Se è stata impostata la rettifica dei costi automatica da applicare alle registrazioni che si verificano in un giorno o una settimana dalla data di lavoro corrente, la rettifica dei costi automatica non verrà eseguita e il costo dell'acquisto non verrà inoltrato alla vendita fintanto che non si esegue il processo batch **Rettifica costo - Movimenti articoli**.  

## <a name="see-also"></a>Vedi anche

[Rettifica costi articolo](inventory-how-adjust-item-costs.md)  
[Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)  
[Dettagli di progettazione: Riconciliazione con la contabilità generale](design-details-reconciliation-with-the-general-ledger.md)  
[Dettagli di progettazione: Registrazione di magazzino](design-details-inventory-posting.md)  
[Dettagli di progettazione: Scostamento](design-details-variance.md)  
[Dettagli di progettazione: Registrazione dell'ordine di assemblaggio](design-details-assembly-order-posting.md)  
[Dettagli di progettazione: Registrazione dell'ordine di produzione](design-details-production-order-posting.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
