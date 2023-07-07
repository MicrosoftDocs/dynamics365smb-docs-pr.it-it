---
title: Dettagli di progettazione - Rivalutazione
description: È possibile rivalutare il magazzino in base alla base di valutazione che riflette nel modo più preciso il valore di magazzino.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-revaluation"></a>Dettagli di progettazione: Rivalutazione
È possibile rivalutare il magazzino in base alla base di valutazione che riflette nel modo più preciso il valore di magazzino. È inoltre possibile retrodatare una rivalutazione, in modo che il costo delle merci vendute (COGS) venga aggiornato correttamente per gli articoli che sono già stati venduti. Gli articoli che utilizzano il metodo di costing standard che non sono stati completamente fatturati possono essere rivalutati.  

In [!INCLUDE[prod_short](includes/prod_short.md)] la seguente flessibilità è supportata riguardo alla rivalutazione:  

-   La quantità rivalutabile può essere calcolata per qualsiasi data, anche indietro nel tempo.  
-   Per gli articoli che utilizzano il metodo di costing standard, i movimenti di costi previsti vengono inclusi nella rivalutazione.  
-   Vengono rilevate le riduzioni di magazzino interessate dalla rivalutazione.  

## <a name="calculating-the-revaluable-quantity"></a>Calcolo della quantità rivalutabile
 La quantità rivalutabile è la quantità residua in magazzino disponibile per la rivalutazione in una data stabilita. Viene calcolata come totale complessivo delle quantità di movimenti contabili articolo completamente fatturati che hanno una data di registrazione uguale o precedente alla data di registrazione di rivalutazione.  

> [!NOTE]  
>  Gli articoli che utilizzano il metodo di costing standard vengono considerati in modo diverso durante il calcolo della quantità rivalutabile per articolo, ubicazione e variante. Le quantità e i valori di movimenti contabili articoli che non sono completamente fatturati vengono inclusi nella quantità rivalutabile.  

Dopo aver registrato una rivalutazione, è possibile registrare un aumento o una riduzione di magazzino con una data di registrazione antecedente alla data di registrazione della rivalutazione. Tuttavia, questa quantità non verrà interessata dalla rivalutazione. Per pareggiare il magazzino, viene considerata solo la quantità rivalutabile originale.  

Poiché la rivalutazione può essere effettuata in qualsiasi data, è necessario disporre di convenzioni per quando un articolo viene considerato parte del magazzino da un punto di vista finanziario. Ad esempio, quando l'articolo è in magazzino e quando l'articolo è semilavorato (WIP).  

### <a name="example"></a>Esempio
Nel seguente esempio viene illustrato quando un articolo WIP diventa parte del magazzino. L'esempio si basa sulla produzione di una catena con 150 collegamenti.  

![Magazzino WIP e rivalorizzazione.](media/design_details_inventory_costing_10_revaluation_wip.png "Magazzino WIP e rivalorizzazione")  

**1Q**: L'utente registra i collegamenti acquistati come ricevuti. Nella tabella seguente viene mostrato il movimento di valorizzazione articolo risultante.  

|Data di registrazione:|Articolo|Tipo movimento|Quantità|Nr. movimento|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|COLLEGAMENTO|Acquisti|150|1|  

> [!NOTE]  
>  Ora è disponibile per la rivalutazione un articolo che utilizza il metodo di costing standard.  

**1V**: L'utente registra i collegamenti acquistati come fatturati e i collegamenti diventano parte del magazzino, da un punto di vista finanziario. Nella tabella seguente sono riportati i movimenti di valorizzazione risultanti.  

|Data di registrazione:|Tipo movimento|Data di valutazione|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Costo Diretto|01-01-20|150,00|1|1|  

 **2Q + 2V**: L'utente registra i collegamenti acquistati come utilizzati per la produzione della catena di ferro. Dal punto di vista finanziario, i collegamenti diventano parte del magazzino WIP.  Nella tabella seguente viene mostrato il movimento di valorizzazione articolo risultante.  

|Data di registrazione:|Articolo|Tipo movimento|Quantità|Nr. movimento|  
|------------------|----------|----------------|--------------|---------------|  
|02-01-20|COLLEGAMENTO|Consumo|-150|1|  

Nella tabella seguente viene mostrato il movimento di valorizzazione risultante.  

|Data di registrazione:|Tipo movimento|Data di valutazione|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|02-01-20|Costo Diretto|02-01-20|-150,00|2|2|  

La data di valutazione viene impostata alla data di registrazione del consumo (20-01-02), come una normale riduzione di magazzino.  

**3Q**: L'utente registra la catena come output e completa l'ordine di produzione. Nella tabella seguente viene mostrato il movimento di valorizzazione articolo risultante.  

|Data di registrazione:|Articolo|Tipo movimento|Quantità|Nr. movimento|  
|------------------|----------|----------------|--------------|---------------|  
|02-15-20|CATENA|Output|1|3|  

**3V**: l'utente esegue il processo batch **(Rettifica costo - Movimenti articoli)** che registra la catena come fatturata per indicare che tutto il consumo dei materiali è stato completamente fatturato. Dal punto di vista finanziario, i collegamenti non fanno più parte del magazzino WIP quando l'output è completamente fatturato e rettificato. Nella tabella seguente sono riportati i movimenti di valorizzazione risultanti.  

|Data di registrazione:|Tipo movimento|Data di valutazione|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Costo Diretto|01-01-20|150,00|2|2|  
|02-01-20|Costo Diretto|02-01-20|-150,00|2|2|  
|02-15-20|Costo Diretto|02-15-20|150,00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Costo previsto nella Rivalutazione
La quantità rivalutabile viene calcolata come somma della quantità per i movimenti contabili articolo completamente fatturati con una data di registrazione uguale o precedente alla data di rivalutazione. Ciò significa che quando alcuni articoli vengono caricati o spediti ma non fatturati, il loro valore di magazzino non può essere calcolato. Gli articoli che utilizzano il metodo di costing standard non sono limitati a tale riguardo.  

> [!NOTE]  
>  Un altro tipo di costo previsto che può essere rivalutato è magazzino WIP, all'interno di alcune regole. Per ulteriori informazioni, vedere [Rivalutazione del magazzino WIP](design-details-revaluation.md#wip-inventory-revaluation).  

Nel calcolo della quantità rivalutabile per gli articoli tramite il metodo di costing Standard vengono inclusi i movimenti contabili articoli che non sono stati completamente fatturati. Tali movimenti vengono poi rivalutati quando si registra la rivalutazione. Quando si fattura il movimento rivalutato, vengono creati i seguenti movimenti di valorizzazione:  

-   Il solito movimento di valorizzazione fatturato con un tipo di movimento **Costo diretto**. L'importo del costo in questo movimento è il costo diretto derivante dalla riga di origine.  
-   Un movimento valorizzazione con un tipo di movimento di **Scostamento**. Questo movimento registra la differenza tra il costo fatturato e il costo standard rivalutato.  
-   Un movimento valorizzazione con un tipo di movimento di **Rivalutazione**. Questo movimento registra lo storno della rivalutazione del costo previsto.  

### <a name="example-1"></a>Esempio
Nel seguente esempio, basato sulla produzione della catena nell'esempio precedente, viene illustrato in che modo vengono creati i tre tipi di movimenti. Si basa sullo scenario seguente:  

1.  L'utente registra i collegamenti acquistati come ricevuti con un costo unitario di VL 2,00.  
2.  L'utente registra quindi una rivalutazione dei collegamenti con un nuovo costo unitario di VL 3,00, aggiornando il costo standard a VL 3,00.  
3.  L'utente registra l'acquisto originale dei collegamenti come fatturato; viene così creato quanto segue:  

    1.  Un movimento di valorizzazione fatturato con un tipo di movimento **Costo diretto**.  
    2.  Un movimento di valorizzazione con un tipo di movimento di **Rivalutazione** per registrare lo storno della rivalutazione del costo previsto.  
    3.  Un movimento valorizzazione con un tipo di movimento Scostamento, che registra la differenza tra il costo fatturato e il costo standard rivalutato.  
Nella tabella seguente sono riportati i movimenti di valorizzazione risultanti.  

|Passaggio|Data di registrazione:|Tipo movimento|Data di valutazione|Importo costo (previsto)|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Costo Diretto|01-15-20|300,00|0.00|1|1|  
|2.|01-20-20|Rivalutazione|01-20-20|150,00|0.00|1|2|  
|3.a.|01-15-20|Costo Diretto|01-15-20|-300,00|0.00|1|3|  
|3.b.|01-15-20|Rivalutazione|01-20-20|-150,00|0.00|1|4|  
|3.c.|01-15-20|Scostamento|01-15-20|0.00|450,00|1|5|  

## <a name="determining-whether-an-inventory-decrease-is-affected-by-revaluation"></a>Determinare se una riduzione di magazzino è interessata dalla rivalutazione
La data della registrazione o della rivalutazione viene utilizzata per determinare se una riduzione di magazzino è interessata dalla rivalutazione.  

Nella seguente tabella vengono mostrati i criteri utilizzati per un articolo che non utilizza il metodo di costing medio.  

|Scenario|Nr. movimento|Tempo|Influenzato dalla rivalutazione|  
|--------------|---------------|------------|-----------------------------|  
|A|Precedentemente al numero movimento di rivalutazione|Precedentemente alla data di registrazione di rivalutazione|No|  
|B|Precedentemente al numero movimento di rivalutazione.|Uguale alla data di registrazione di rivalutazione|No|  
|C|Precedentemente al numero movimento di rivalutazione.|Successivo alla data di registrazione di rivalutazione|Sì|  
|D|Successivamente al numero movimento di rivalutazione.|Precedentemente alla data di registrazione di rivalutazione|Sì|  
|E|Successivamente al numero movimento di rivalutazione.|Uguale alla data di registrazione di rivalutazione|Sì|  
|D|Successivamente al numero movimento di rivalutazione.|Successivo alla data di registrazione di rivalutazione|Sì|  

### <a name="example-2"></a>Esempio
Il seguente esempio, che illustra la rivalutazione di un articolo che utilizza il metodo di costing FIFO, si basa sul seguente scenario:  

1.  In data 20-01-01 l'utente registra un acquisto di 6 unità.  
2.  In data 20-01-02 l'utente registra la vendita di 1 unità.  
3.  In data 03-01-20 l'utente registra la vendita di 1 unità.  
4.  In data 04-01-20 l'utente registra la vendita di 1 unità.  
5.  In data 20-01-03 l'utente calcola il valore di magazzino per l'articolo e registra una rivalutazione del costo unitario dell'articolo da VL 10,00 a VL 8,00.  
6.  In data 20-01-02 l'utente registra la vendita di 1 unità.  
7.  In data 03-01-20 l'utente registra la vendita di 1 unità.  
8.  In data 04-01-20 l'utente registra la vendita di 1 unità.  
9. L'utente esegue il processo batch **Rettifica costo - Movimenti articoli**.  

Nella tabella seguente sono riportati i movimenti di valorizzazione risultanti.  

|Scenario|Data di registrazione:|Tipo movimento|Data di valutazione|Quantità valorizzata|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Acquisti|01-01-20|6|60.00|1|1|  
||03-01-20|Rivalutazione|03-01-20|4|-8,00|1|5|  
|A|02-01-20|Vendite|02-01-20|-1|-10,00|2|2|  
|B|03-01-20|Vendite|03-01-20|-1|-10,00|3|3|  
|C|04-01-20|Vendite|04-01-20|-1|-10,00|4|4|  
||04-01-20|Vendite|04-01-20|-1|2.00|4|9|  
|D|02-01-20|Vendite|03-01-20|-1|-10,00|5|6|  
||02-01-20|Vendite|03-01-20|-1|2.00|5|10|  
|E|03-01-20|Vendite|03-01-20|-1|-10,00|6|7|  
||03-01-20|Vendite|03-01-20|-1|2.00|6|11|  
|D|04-01-20|Vendite|04-01-20|-1|-10,00|7|8|  
||04-01-20|Vendite|04-01-20|-1|2.00|7|12|  

## <a name="wip-inventory-revaluation"></a>Rivalutazione del magazzino WIP
La rivalutazione del magazzino WIP implica la rivalutazione dei componenti registrati come parte del magazzino WIP al momento della rivalutazione.  

Tenendo ciò a mente, è più importante stabilire convenzioni come quando un articolo viene considerato parte del magazzino WIP da un punto di vista finanziario. In [!INCLUDE[prod_short](includes/prod_short.md)] sono presenti le convenzioni seguenti:  

-   Un componente acquistato diventa parte delle giacenze di materie prime a partire del momento della registrazione di un acquisto come fatturato.  
-   Un componente acquistato o subassemblato diventerà parte del magazzino WIP a partire dalla registrazione del consumo in relazione a un ordine di produzione.  
-   Un componente acquistato o subassemblato resta parte del magazzino WIP fino al momento in cui un ordine di produzione (articolo lavorato) viene fatturato.  

La modalità con cui viene impostata la data di valutazione del movimento di valorizzazione di consumo segue le stesse regole impostate per il magazzino non WIP. Per ulteriori informazioni, vedere [Determinare se una riduzione di magazzino è interessata dalla rivalutazione](design-details-revaluation.md#determining-whether-an-inventory-decrease-is-affected-by-revaluation).  

Il magazzino WIP può essere rivalutato finché la data di rivalutazione non è successiva alla data di registrazione dei corrispondenti movimenti contabili articoli di tipo Consumo e purché l'ordine di produzione corrispondente non sia stato ancora fatturato.  

> [!CAUTION]  
>  Il report **Valutazione magazzino - WIP** visualizza il valore dei movimenti di ordini di produzione registrati e può quindi risultare un poco confusionario per gli articoli WIP che sono stati rivalutati.  

## <a name="see-also"></a>Vedi anche
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)   
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)   
 [Dettagli di progettazione: Valutazione di magazzino](design-details-inventory-valuation.md) [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
 [Finanze](finance.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
