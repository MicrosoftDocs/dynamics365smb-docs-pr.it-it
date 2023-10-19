---
title: Dettagli di progettazione - Rivalutazione
description: È possibile rivalutare il magazzino in base alla base di valutazione che riflette nel modo più preciso il valore di magazzino.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
---

# <a name="design-details-revaluation"></a>Dettagli di progettazione: Rivalutazione

È possibile rivalutare il magazzino in base alla base di valutazione che riflette nel modo più preciso il valore di magazzino. È inoltre possibile retrodatare una rivalutazione per aggiornare in modo corretto il costo delle merci vendute (COGS). Gli articoli che utilizzano il metodo di costing standard che non sono stati completamente fatturati possono essere rivalutati.  

In [!INCLUDE[prod_short](includes/prod_short.md)] la seguente flessibilità è supportata riguardo alla rivalutazione:  

- La quantità rivalutabile può essere calcolata per qualsiasi data, anche indietro nel tempo.  
- Per gli articoli che utilizzano il metodo di costing standard, i movimenti di costi previsti vengono inclusi nella rivalutazione.  
- Vengono rilevate le riduzioni di magazzino interessate dalla rivalutazione.  

## <a name="calculate-the-revaluable-quantity"></a>Calcola la quantità rivalutabile

La quantità rivalutabile è la quantità residua in magazzino disponibile in una data stabilita. La quantità è il totale dei movimenti contabili articoli completamente fatturati registrati alla data di rivalutazione o prima.  

> [!NOTE]  
>  Gli articoli che utilizzano il metodo di costing standard vengono considerati in modo diverso durante il calcolo della quantità rivalutabile per articolo, ubicazione e variante. Le quantità e i valori di movimenti contabili articoli che non sono completamente fatturati vengono inclusi nella quantità rivalutabile.  

Dopo aver registrato una rivalutazione, è possibile registrare un aumento o una riduzione di magazzino con una data di registrazione antecedente alla data di registrazione della rivalutazione. Tuttavia, questa quantità non verrà interessata dalla rivalutazione. Per pareggiare il magazzino, viene considerata solo la quantità rivalutabile originale.  

Poiché la rivalutazione può essere effettuata in qualsiasi data, è necessario che un articolo venga considerato parte del magazzino. Ad esempio, quando l'articolo è in magazzino e quando l'articolo è semilavorato (WIP).  

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
|02-15-20|Costo diretto|02-15-20|150.00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Costo previsto nella rivalutazione

La quantità rivalutabile viene calcolata come somma della quantità per i movimenti contabili articolo che hai registrato nella data della rivalutazione o prima. Quando alcuni articoli vengono ricevuti o spediti ma non fatturati, il loro valore di magazzino non può essere calcolato. Gli articoli che utilizzano il metodo di costing standard non sono limitati a tale riguardo.  

> [!NOTE]  
>  Un altro tipo di costo previsto che può essere rivalutato è magazzino WIP, all'interno di alcune regole. Per ulteriori informazioni, vedere [Rivalutazione del magazzino WIP](design-details-revaluation.md#wip-inventory-revaluation).  

Nel calcolo della quantità rivalutabile per gli articoli tramite il metodo di costing Standard vengono inclusi i movimenti contabili articoli che non sono stati completamente fatturati. Tali movimenti vengono rivalutati quando si registra la rivalutazione. Quando si fattura il movimento rivalutato, vengono creati i seguenti movimenti di valorizzazione:  

- Il solito movimento di valorizzazione fatturato con un tipo di movimento **Costo diretto**. L'importo del costo in questo movimento è il costo diretto derivante dalla riga di origine.  
- Un movimento valorizzazione con un tipo di movimento di **Scostamento**. Questo movimento registra la differenza tra il costo fatturato e il costo standard rivalutato.  
- Un movimento valorizzazione con un tipo di movimento di **Rivalutazione**. Questo movimento registra lo storno della rivalutazione del costo previsto.

### <a name="example-1"></a>Esempio

L'esempio seguente si basa sulla produzione della catena nell'esempio precedente. Questo esempio illustra come vengono creati i tre tipi di voci, in base al seguente scenario:  

1.  L'utente registra i collegamenti acquistati come ricevuti con un costo unitario di VL 2,00.  
2.  L'utente registra quindi una rivalutazione dei collegamenti con un nuovo costo unitario di VL 3,00, aggiornando il costo standard a VL 3,00.  
3.  L'utente registra l'acquisto originale dei collegamenti di una catena come fatturato; vengono creati i seguenti movimenti di valorizzazione:  

    1.  Un movimento di valorizzazione fatturato con un tipo di movimento **Costo diretto**.  
    2.  Un movimento di valorizzazione con un tipo di movimento di **Rivalutazione** per registrare lo storno della rivalutazione del costo previsto.  
    3.  Un movimento valorizzazione con un tipo di movimento Scostamento, che registra la differenza tra il costo fatturato e il costo standard rivalutato.  

Nella seguente tabella vengono illustrati i risultati.  

|Passaggio|Data di registrazione|Tipo movimento|Data di valutazione|Importo costo (previsto)|Importo costo (effettivo)|Nr. movimento cont. articolo|Nr. movimento|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Costo Diretto|01-15-20|300,00|0.00|1|1|  
|2.|01-20-20|Rivalutazione|01-20-20|150,00|0.00|1|2|  
|3.a.|01-15-20|Costo Diretto|01-15-20|-300,00|0.00|1|3|  
|3.b.|01-15-20|Rivalutazione|01-20-20|-150,00|0.00|1|4|  
|3.c.|01-15-20|Scostamenti|01-15-20|0.00|450.00|1|5|  

## <a name="determine-whether-revaluation-affects-an-inventory-decrease"></a>Determinare se la rivalutazione influisce su una riduzione di magazzino

Usare la data della registrazione o della rivalutazione per determinare se una riduzione di magazzino è interessata dalla rivalutazione.  

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

Il seguente esempio, che illustra la rivalutazione di un articolo che utilizza il metodo di costing FIFO. L'esempio si basa sullo scenario seguente:  

1.  In data 20-01-01 l'utente registra un acquisto di 6 unità.  
2.  In data 20-02-01 l'utente registra una vendita di 1 unità.  
3.  In data 20-03-01 l'utente registra una vendita di 1 unità.  
4.  In data 20-04-01 l'utente registra una vendita di 1 unità.  
5.  In data 20-01-03 l'utente calcola il valore di magazzino per l'articolo e registra una rivalutazione del costo unitario dell'articolo da VL 10,00 a VL 8,00.  
6.  In data 20-02-01 l'utente registra una vendita di 1 unità.  
7.  In data 20-03-01 l'utente registra una vendita di 1 unità.  
8.  In data 20-04-01 l'utente registra una vendita di 1 unità.  
9. Eseguire il processo batch **Rettifica costo - Movimenti articoli**.  

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
||04-01-20|Vendita|04-01-20|-1|2.00|7|12|  

## <a name="wip-inventory-revaluation"></a>Rivalutazione del magazzino WIP

La rivalutazione delle scorte WIP implica la rivalutazione dei componenti registrati come scorte WIP.  

È importante disporre di convenzioni che controllino quando un articolo è inventario WIP da un punto di vista finanziario. In [!INCLUDE[prod_short](includes/prod_short.md)] sono presenti le convenzioni seguenti:  

- Un componente acquistato diventa parte delle giacenze di materie prime quando registri un acquisto come fatturato.  
- Un componente acquistato o subassemblato diventerà parte del magazzino WIP quando se ne registra il consumo in relazione a un ordine di produzione.  
- Un componente acquistato o subassemblato resta parte del magazzino WIP fino al momento in cui un ordine di produzione (articolo lavorato) viene fatturato.  

La modalità con cui viene impostata la data di valutazione del movimento di valorizzazione di consumo segue le stesse regole impostate per il magazzino non WIP. Per ulteriori informazioni, vai a [Determinare se la rivalutazione influisce su una riduzione di magazzino](#determine-whether-revaluation-affects-an-inventory-decrease).  

È possibile rivalutare il magazzino WIP nelle seguenti condizioni:

- La data di rivalutazione è precedente alle date di registrazione dei corrispondenti movimenti contabili articoli di tipo Consumo.
- Non hai fatturato l'ordine di produzione.  

> [!CAUTION]  
> Il report **Valutazione magazzino - WIP** visualizza il valore dei movimenti di ordini di produzione registrati e potrebbe quindi risultare un poco confusionario per gli articoli WIP che sono stati rivalutati.  

## <a name="revaluate-items-with-the-average-costing-method"></a>Rivalutare gli articoli con il metodo di costing medio

È possibile rivalutare solo gli articoli che utilizzano il metodo di costing medio se **Calcola per** è *Articolo*.

Puoi eseguire la rivalutazione solo alla fine del periodo selezionato nel campo **Periodo costo medio** della pagina **Impostazione inventario**.

La rivalutazione non influirà sulle transazioni negative nel mese corrente, motivo per cui non sono inclusi nemmeno i movimenti in entrata completamente applicati.

### <a name="example-3"></a>Esempio

Questo esempio mostra cosa succede quando si calcola il valore dell'inventario nella pagina **Giornale di rivalutazione articolo**. Nella pagina **Impostazione inventario**, **Articolo** viene scelto nel campo **Tipo calcolo costo medio** e **Mese** viene scelto nel campo **Periodo costo medio**.

Nella seguente tabella vengono mostrati i movimenti contabili articoli su cui si basa l'esempio del costo medio per articolo, ITEM1.

|Data di registrazione|Tipo mov. articolo|Quantità|Importo costo (effettivo)|Nr. movimento|
|----|----|----|----|----|
25-04-23|Acquisti|5|5.00|1
26-04-23|Acquisti|3|3.00|2
27-04-23|Vendita|-5|-5,00|3
28-04-23|Vendita|-1|-1,00|4
13-05-23|Acquisti|2|20.00|5
17-06-23|Vendita|-6|-22,00|6

La seguente tabella mostra il risultato dell'esecuzione del report **Calcola valore inventario** con date di registrazione diverse.

|Data di registrazione|Quantità|Commento|
|---|---|-------------|
30-04-23|2|Include solo la quantità rimanente dal movimento 2. Il movimento 1 è completamente applicato prima della data di registrazione e il movimento 5 è successivo alla data di registrazione.
31-05-23|4|Include solo le quantità rimanenti dai movimenti 2 e 13.
30-06-23|0|Nessuna quantità rimanente alla data di registrazione.

Il risultato dei seguenti movimenti sarà 0, indipendentemente dalla data di registrazione.

|Data di registrazione|Tipo mov. articolo|Quantità|Importo costo (effettivo)|Nr. movimento|
|----|----|----|----|----|
13-05-23|Acquisti|5|5.00|1
26-04-23|Vendita|-5|5.00|2

## <a name="see-also"></a>Vedi anche

[Dettagli di progettazione: determinazione dei costi di magazzino](design-details-inventory-costing.md)   
[Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)   
[Dettagli di progettazione: Valutazione di magazzino](design-details-inventory-valuation.md)
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
