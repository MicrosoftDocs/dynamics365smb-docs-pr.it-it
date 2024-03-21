---
title: 'Dettagli di progettazione: Metodi di costing'
description: In questo argomento viene descritto come il metodo di costing determina se i valori effettivi e a budget vengono capitalizzati e utilizzati nel calcolo dei costi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/12/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-costing-methods"></a>Dettagli di progettazione: Metodi di costing

Il metodo di costing determina se un valore effettivo o a budget viene capitalizzato e utilizzato nel calcolo dei costi. Insieme alla data e alla sequenza di registrazione, il metodo di costing influisce anche sul modo in cui viene registrato il flusso dei costi.

> [!NOTE]
> Non è possibile modificare il metodo di costing dell'articolo se esiste un movimento contabile aperto per l'articolo. Per ulteriori informazioni, vedere [Dettagli di progettazione: modifica del metodo di determinazione dei costi per gli articoli](design-details-changing-costing-methods.md).

In [!INCLUDE[prod_short](includes/prod_short.md)] sono supportati i seguenti metodi:  

| Metodo di costing | Descrizione | Quando utilizzarlo |
|--|--|--|
| FIFO | Il costo unitario di un articolo è il valore effettivo di tutto il carico dell'articolo, selezionato secondo la regola FIFO.<br /><br /> Nella valutazione di magazzino si presuppone che il primo articolo posizionato nel magazzino venga venduto per primo. | Negli ambienti aziendali in cui il costo del prodotto è stabile.<br /><br /> (Quando i prezzi salgono, nei conti patrimoniali viene mostrato un valore maggiore). Ciò significa che la soggettività tributaria aumenta mentre il punteggio del credito e la capacità di prendere in prestito soldi migliora).<br /><br /> Per articoli con una durata a scaffale limitata, poiché le merci più vecchie devono essere vendute prima della data di scadenza. |
| LIFO | Il costo unitario di un articolo è il valore effettivo di tutto il carico dell'articolo, selezionato secondo la regola LIFO.<br /><br /> Nella valutazione di magazzino si presuppone che gli ultimi articoli posizionati nel magazzino vengano venduti per primo. | Operazione non consentita in molti paesi, perché può essere utilizzata per ridurre il profitto.<br /><br /> (Quando i prezzi salgono, il valore nel conto economico diminuisce). Ciò significa che la soggettività tributaria diminuisce mentre la capacità di prendere in prestito soldi peggiora). |
| Media | Il costo unitario di un articolo viene calcolato come il costo unitario medio in ogni momento dopo un acquisto.<br /><br /> Per la valutazione magazzino si presuppone che tutte le giacenze siano vendute simultaneamente. | Negli ambienti aziendali in cui il costo del prodotto non è stabile.<br /><br /> Quando gli inventari sono impilati o mischiati e non è possibile differenziarli, ad esempio con gli agenti chimici. |
| Specifico | Il costo unitario di un articolo è il costo esatto con la particolare unità è stata ricevuta. | Nella produzione o nel commercio di articoli facilmente identificabili a costi unitari abbastanza elevati.<br /><br /> Per gli articoli che sono soggetti a regolazione.<br /><br /> Per articoli con numeri di serie. |
| Standard | Il costo unitario di un articolo è prestabilito in base a una stima.<br /><br /> Quando il costo effettivo viene realizzato successivamente, il costo standard deve essere rettificato con il costo effettivo tramite i valori di scostamento. | Quando il controllo costi è fondamentale.<br /><br /> Nella produzione ripetitiva per stimare i costi di materiale diretto, di manodopera diretta e i costi generali di produzione.<br /><br /> Dove esiste una disciplina e del personale per gestire gli standard. |

Nell'immagine seguente viene mostrato il flusso dei costi attraverso il magazzino per ciascun metodo di costing.  

![Metodi di costing visualizzati.](media/design_details_inventory_costing_7_costing_methods.png "Metodi di costing visualizzati")  

I metodi di costing differiscono in modo da valorizzare le riduzioni di magazzino e se utilizzano il costo effettivo o il costo standard come base di valutazione. Nella seguente tabella vengono illustrate le differenti caratteristiche. (Il metodo LIFO è escluso, in quanto è molto simile al metodo FIFO).  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Caratteristica generale|Collegamento o rettifica |Rivalutazione|Varie |
|-|---------|---------|---------|---------|
|**FIFO**     |Semplice da comprendere|Il collegamento tiene traccia della **quantità residua**.<br /><br /> La rettifica inoltra i costi in base al collegamento alla quantità. |Rivaluta solo la quantità fatturata.<br /><br /> Può essere eseguita per articolo oppure per movimento contabile articolo.<br /><br /> Può essere effettuata a ritroso.|Se una riduzione di magazzino viene retrodatata, i movimenti esistenti NON vengono collegati nuovamente per fornire il flusso di costi FIFO corretto.|
|**Media**     |In base alle opzioni del periodo: **Giorno**/**Settimana**/**Mese**/**Trimestre**/**Periodo contabile**.<br /><br /> Può essere calcolato per articolo oppure per articolo/ubicazione/variante.|Il collegamento tiene traccia della **quantità residua**.<br /><br /> I costi vengono calcolati e inviati per la **data di valutazione**. |Rivaluta solo la quantità fatturata.<br /><br /> Può essere effettuata solo per movimento.<br /><br /> Può essere effettuata a ritroso. |Se un aumento o una riduzione di magazzino viene retrodata, il costo medio viene ricalcolato e tutti i movimenti interessati vengono rettificati.<br /><br /> Se si modifica il periodo o tipo di calcolo, tutti i movimenti interessati devono essere rettificati.|
|**Standard**     |Semplice da utilizzare, ma richiede la manutenzione qualificata.|Il collegamento tiene traccia della **quantità residua**.<br /><br /> Il collegamento è basato su FIFO.|Rivaluta le quantità fatturate e non fatturate.<br /><br /> Può essere eseguita per articolo oppure per movimento contabile articolo.<br /><br /> Può essere effettuata a ritroso.|Utilizzare la pagina **Prospetto standard** per aggiornare e riepilogare periodicamente i costi standard.<br /><br /> NON è supportata per USK.<br /><br /> Nessun record storico esistente per i costi standard.|
|**Specifico**     |Richiede la tracciabilità articolo sia sulla transazione in entrata che sulla transazione in uscita.<br /><br /> Viene solitamente utilizzato per gli articoli serializzati.|Tutti i collegamenti sono fissi.|Rivaluta solo la quantità fatturata.<br /><br /> Può essere eseguita per articolo oppure per movimento contabile articolo.<br /><br /> Può essere effettuata a ritroso.|È possibile utilizzare la tracciabilità articolo specifico senza utilizzare il metodo di costing Specifico. Il costo quindi non seguirà il numero di lotto, ma l'ipotesi di costo del metodo di costing selezionato.|

## <a name="example"></a>Esempio

In questa sezione vengono forniti esempi di come i differenti metodi di costing influiscono sul valore di magazzino.  

Nella seguente tabella vengono mostrati gli aumenti e le riduzioni di magazzino su cui si basano gli esempi.  

|Data di registrazione:|Quantità|Nr. movimento|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|02-01-20|-1|4|  
|03-01-20|-1|5|  
|04-01-20|-1|6|  

> [!NOTE]  
> La quantità risultante in magazzino è pari a zero. Di conseguenza, il valore di magazzino deve essere zero, indipendentemente dal metodo di costing.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Effetto dei metodi di costing sulla valutazione degli aumenti di magazzino

Per gli articoli con i metodi di costing che utilizzano il costo effettivo come base di valutazione (**FIFO**, **LIFO**, **Medio** o **Specifico**), gli aumenti in magazzino sono stimati come costo di acquisto dell'articolo.  

- **Standard**  

    Per gli articoli che utilizzano il metodo di costing **Standard**, gli aumenti di magazzino vengono valutati in base al costo standard corrente dell'articolo.  

#### <a name="standard"></a>Standard

Per gli articoli che utilizzano il metodo di costing **Standard**, gli aumenti di magazzino vengono valutati in base al costo standard corrente dell'articolo.  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Effetto dei metodi di costing sulla valutazione delle riduzioni di magazzino

- **FIFO**  

    Per gli articoli che utilizzano il metodo di costing **FIFO**, gli articoli acquistati prima vengono venduti sempre per primi (numeri di movimento 3, 2 e 1 in questo esempio). Di conseguenza, le diminuzioni di magazzino vengono valutate prendendo il valore del primo aumento di magazzino.  

     COGS viene calcolato utilizzando il valore delle prime acquisizioni di magazzino.  

     La seguente tabella mostra come le diminuzioni di inventario vengono valutate per il metodo di costing **FIFO**.  

    |Data di registrazione:|Quantità|Importo costo (effettivo)|Nr. movimento|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-10,00|4|  
    |03-01-20|-1|-20,00|5|  
    |04-01-20|-1|-30,00|6|  

- **LIFO**  

    Per gli articoli che utilizzano il metodo di costing **LIFO**, gli articoli acquistati più recentemente vengono venduti sempre per primi (numeri di movimento 3, 2 e 1 in questo esempio). Di conseguenza, le diminuzioni di magazzino vengono valutate prendendo il valore dell'ultimo aumento di magazzino.  

     COGS viene calcolato utilizzando il valore delle acquisizioni di magazzino più recenti.  

     La seguente tabella mostra come le diminuzioni di inventario vengono valutate per il metodo di costing **LIFO**.  

    |Data di registrazione:|Quantità|Importo costo (effettivo)|Nr. movimento|  
    |------------|--------|--------------------|---------|  
    |02-01-20|-1|-30,00|4|  
    |03-01-20|-1|-20,00|5|  
    |04-01-20|-1|-10,00|6|  

- **Media**  

    Per gli articoli che utilizzano il metodo di costing **Medio**, le riduzioni di magazzino vengono valutate calcolando una media ponderata del magazzino rimanente all'ultimo giorno del costo medio del periodo in cui la riduzione di magazzino è stata registrata. Per ulteriori informazioni, vedere [Dettagli di progettazione: Costo medio](design-details-average-cost.md).  

     Nella seguente tabella viene mostrato in che modo vengono valutate le diminuzioni di magazzino per il metodo di costing **Media**.  

    | Data di registrazione: | Quantità | Importo costo (effettivo) | Nr. movimento |
    |--|--|--|--|
    | 02-01-20 | -1 | -20,00 | 4 |
    | 03-01-20 | -1 | -20,00 | 5 |
    | 04-01-20 | -1 | -20,00 | 6 |

- **Standard**  

    Per gli articoli che utilizzano il metodo di costing **Standard**, le riduzioni di magazzino sono simili al metodo di costing **FIFO** fatta eccezione per la valutazione basata su un costo standard, non sul costo effettivo.  

    Nella seguente tabella viene mostrato in che modo vengono valutate le diminuzioni di magazzino per il metodo di costing **Standard**.  

    |Data di registrazione:|Quantità|Importo costo (effettivo)|Nr. movimento|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-15,00|4|  
    |03-01-20|-1|-15,00|5|  
    |04-01-20|-1|-15,00|6|  

- **Specifico**  

    I metodi di costing si basano su un presupposto di come il flusso del costo vada dall'aumento di magazzino a una riduzione di magazzino. Tuttavia, se esistono informazioni più precise relative al flusso di costo, è possibile sostituire questa supposizione creando un collegamento fisso tra i movimenti. Un collegamento fisso crea un collegamento tra una riduzione di magazzino e un aumento di magazzino specifico e dirige il flusso di costo di conseguenza.  

    Per gli articoli che utilizzano il metodo di costing **Specifico**, le riduzioni di magazzino vengono stimate in base all'aumento di magazzino collegato dal collegamento fisso.  

    Nella seguente tabella viene mostrato in che modo vengono valutate le diminuzioni di magazzino per il metodo di costing **Specifico**.  

    |Data di registrazione:|Quantità|Importo costo (effettivo)|Movimento Collegato|Nr. movimento|
    |------------|--------|--------------------|----------------|---------|  
    |02-01-20|-1|-20,00|**2**|4|  
    |03-01-20|-1|-10,00|**1**|5|  
    |04-01-20|-1|-30,00|**3**|6|  

## <a name="see-also"></a>Vedi anche

[Dettagli di progettazione: determinazione dei costi di magazzino](design-details-inventory-costing.md)  
[Dettagli di progettazione: scostamento](design-details-variance.md)  
[Dettagli di progettazione: costo medio](design-details-average-cost.md)  
[Dettagli di progettazione: collegamento articoli](design-details-item-application.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Dati finanziari](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glossario dei termini nei processi aziendali di Dynamics 365](/dynamics365/guidance/business-processes/glossary)  
[Definire la panoramica dei costi di prodotti e servizi](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
