---
title: 'Dettagli di progettazione: Collegamento articoli | Microsoft Docs'
description: Questo argomento descrive dove vengono registrati la quantità e il valore di magazzino quando si registra una transazione di magazzino.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, items, ledger entries, posting, inventory'
ms.date: 06/08/2021
ms.author: bholtorf
---
# <a name="design-details-item-application"></a>Dettagli di progettazione: Collegamento articoli

Quando si registra una transazione di magazzino, la registrazione della quantità viene registrata nei movimenti contabili articoli, la registrazione del valore nei movimenti di valorizzazione. Per ulteriori informazioni, vedere [Dettagli di progettazione: Registrazione magazzino](design-details-inventory-posting.md).  

Inoltre, viene creato un collegamento articoli per collegare il destinatario di costo alla relativa origine di costo per fornire l'inoltro di costi secondo il metodo di costing. Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md).  

[!INCLUDE[prod_short](includes/prod_short.md)] esegue due tipi di collegamento articoli.  

|Tipo collegamento|Description|  
|----------------------|---------------------------------------|  
|Collegamento della quantità|Creato per tutte le transazioni di magazzino|  
|Collegamento costo|Creata per i movimenti in entrata insieme a un collegamento di quantità come risultato dell'interazione utente nei processi speciali.|  

I collegamenti articoli possono essere creati nei seguenti modi.  

|Metodo|Description|Tipo collegamento|  
|------------|---------------------------------------|----------------------|  
|Automatico|Viene eseguito come inoltro di costi generale in base al metodo di costing|Collegamento della quantità|  
|Fisso|Effettuato dall'utente quando:<br /><br /> - Elaborazione dei resi<br />- Registrazione di correzioni<br />- Annullamento delle registrazioni delle quantità<br />-   Creazione di spedizioni dirette **Nota:** il collegamento fisso può essere effettuato manualmente immettendo un numero di movimento nel campo **Collega-da mov. art.** o tramite una funzione, ad esempio **Ottieni righe documento registrato da stornare**.|Collegamento della quantità<br /><br /> Collegamento costo **Nota:** il collegamento dei costi si verifica solo nelle transazioni in entrata dove il campo **Collega da mov. art.** viene compilato per creare un collegamento fisso. Vedere la tabella seguente.|  

La scelta tra la creazione di collegamenti quantità o di collegamenti costi dipende dalla direzione della transazione di magazzino e dal fatto se il collegamento articoli viene eseguito automaticamente oppure è fisso, in relazione a processi speciali.  

Nella seguente tabella viene mostrato, in base ai campi di applicazione centrali nelle righe di transazione di magazzino, il flusso dei costi a seconda della direzione della transazione. Indica inoltre quando e perché il collegamento articoli è di tipo quantità o costo.  

|-|Campo Collega-a mov. art.|Campo Collega-da mov. art.|  
|-|--------------------------------|----------------------------------|  
|Collegamento per il movimento in uscita|Il movimento in uscita esegue il pull del costo dal movimento in entrata aperto.<br /><br /> **Collegamento della quantità**|Non supportato|  
|Collegamento per il movimento in entrata|Il movimento in entrata esegue il push del costo sul movimento in uscita aperto.<br /><br /> Il movimento in entrata è l'origine del costo.<br /><br /> **Collegamento della quantità**|Il movimento in entrata esegue il pull del costo dal movimento in uscita. **Nota:** nella creazione di questo collegamento fisso, la transazione in entrata viene gestita come un reso di vendita. Di conseguenza, il movimento in uscita collegato rimane aperto. <br /><br /> Il movimento in entrata NON è l'origine del costo.<br /><br /> **Collegamento costo**|  

> [!IMPORTANT]  
> Un reso di vendita NON viene considerato un'origine di costo quando viene collegato in modo fisso.  
>
> Il movimento di vendita rimane aperto fino alla registrazione dell'origine reale.  

In un movimento di collegamento articoli vengono registrate le seguenti informazioni.  

|Campo|Description|  
|---------------------------------|---------------------------------------|  
|**Nr. movimento cont. articolo**|numero del movimento contabile articolo per la transazione per la quale è stato creato il movimento di collegamento.|  
|**Nr. movimento articolo in entrata**|Il numero del movimento contabile articolo dell'aumento di magazzino a cui deve essere collegata la transazione, se pertinente.|  
|**Nr. movimento articolo in uscita**|Il numero del movimento contabile articolo della riduzione di magazzino a cui deve essere collegata la transazione, se pertinente.|  
|**Quantità**|quantità collegata.|  
|**Data di Registrazione:**|data di registrazione della transazione.|  

## <a name="inventory-increase"></a>Aumento di magazzino
Quando si registra un aumento di magazzino, allora viene registrato un semplice movimento di collegamento articoli senza un collegamento a un movimento in uscita.  

### <a name="example"></a>Esempio
Nella seguente tabella viene illustrato il movimento di collegamento articoli che viene creato quando si registra una ricezione acquisti di 10 unità.  

|Data di registrazione|Nr. movimento articolo in entrata|Nr. movimento articolo in uscita|Quantità|Nr. movimento cont. articolo|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  

## <a name="inventory-decrease"></a>Riduzione di magazzino
Quando si registra una riduzione di magazzino, viene creato un movimento di collegamento articoli che collega la riduzione di magazzino a un aumento di magazzino. Questo collegamento viene creato utilizzando come linea guida il metodo di costing dell'articolo. Per gli articoli che utilizzano i metodi di costing FIFO, standard e medio, il collegamento è basato sul principio FIFO. La riduzione di magazzino viene applicata all'aumento di magazzino con la data di registrazione meno recente. Per gli articoli che utilizzano il metodo di costing LIFO, il collegamento è basato sul principio LIFO. La riduzione di magazzino viene applicata all'aumento di magazzino con la data di registrazione più recente.  

Nella tabella **Mov. contabili articoli**, il campo **Quantità residua** indica la quantità che non è ancora stata collegata. Se la quantità residua è superiore a 0, viene selezionata la casella di controllo **Apri**.  

### <a name="example-1"></a>Esempio
Nel seguente esempio viene illustrato un movimento di collegamento articoli creato quando si registra una spedizione di vendita di 5 unità degli articoli ricevuti nell'esempio precedente. Il primo movimento di collegamento articoli è la ricezione acquisti. Il secondo movimento di collegamento è la spedizione di vendita.  

Nella seguente tabella vengono mostrati i due movimenti di collegamento articoli derivanti rispettivamente dall'aumento di magazzino e dalla riduzione di magazzino.  

|Data di registrazione|Nr. movimento articolo in entrata|Nr. movimento articolo in uscita|Quantità|Nr. movimento cont. articolo|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|01-03-20|1|2|-5|2|  

## <a name="fixed-application"></a>Collegamento fisso
Viene impostato un collegamento fisso quando si specifica che il costo di un aumento di magazzino deve essere collegato a una determinata riduzione di magazzino o viceversa. Il collegamento fisso influisce sulle quantità residue dei movimenti, ma il collegamento fisso provoca anche lo storno del costo esatto del movimento originale a cui o da cui si sta effettuando il collegamento.  

Per impostare un collegamento fisso, è possibile utilizzare i campi **Collega a mov. art.** o **Collega da mov. art.** nelle righe del documento per specificare il movimento contabile articolo a cui o da cui si desidera collegare la riga della transazione. Viene ad esempio creato un collegamento fisso quando si desidera creare un collegamento costo che specifichi che un reso di vendita deve essere collegato a una determinata spedizione di vendita allo scopo di ottenere lo storno del costo della spedizione di vendita. In questo caso, il metodo di costing viene ignorato da [!INCLUDE[prod_short](includes/prod_short.md)] e viene eseguito un collegamento della riduzione di magazzino, o dell'aumento nel caso di un reso di vendita, al movimento contabile articolo specificato. Il vantaggio della creazione di un collegamento fisso consiste nel fatto che il costo della transazione originale viene passato alla nuova transazione.  

### <a name="example--fixed-application-in-purchase-return"></a>Esempio: collegamento fisso nel reso di acquisto
Il seguente esempio, che illustra l'effetto del collegamento fisso di un reso acquisto di un articolo che utilizza il metodo di costing FIFO, si basa sul seguente scenario:  

1. Nel movimento 1, l'utente registra un acquisto a un costo di VL 10,00.  
2. Nel movimento 2, l'utente registra un acquisto a un costo di VL 20,00.  
3. Nel movimento 3, l'utente registra un reso da acquisto. L'utente crea un collegamento fisso al secondo acquisto immettendo il numero del movimento contabile articolo nel campo **Collega a mov. art.** nella riga dell'ordine di reso di acquisto.  

Nella seguente tabella vengono mostrati i movimenti contabili articoli risultati dallo scenario.  

|**Data di registrazione**|**Tipo mov. articolo**|**Quantità**|**Importo costo (effettivo)**|**Nr. movimento cont. articolo**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|01-04-20|Acquisto|10|10.00|1|  
|01-05-20|Acquisto|10|20.00|2|  
|01-06-20|Acquisto (reso)|-10|-20,00|3|  

Poiché un collegamento fisso viene eseguita dal reso di acquisto al secondo movimento di acquisto, gli articoli vengono resi al costo corretto. Se l'utente non avesse eseguito il collegamento fisso, l'articolo reso sarebbe stato valutato in modo errato in VL 10,00 perché il reso sarebbe stato collegato al primo movimento di acquisto secondo il principio FIFO.  

Nella seguente tabella viene illustrato il movimento di collegamento articoli che deriva da un collegamento fisso.  

|Data di registrazione|Nr. movimento articolo in entrata|Nr. movimento articolo in uscita|Quantità|Nr. movimento cont. articolo|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-06-20|2|3|10|3|  

Il costo del secondo acquisto, VL 20,00 viene passato correttamente al reso di acquisto.  

### <a name="example--fixed-application-with-average-cost"></a>Esempio: collegamento fisso con costo medio
Il seguente esempio, che illustra l'effetto del collegamento fisso, si basa sul seguente scenario per un articolo che utilizza il metodo di costing medio:  

1. Nei movimenti numero 1 e 2, l'utente registra due fatture di acquisto. La seconda fattura ha costo unitario diretto errato di VL 1000,00.  
2. Nel movimento numero 3, l'utente registra una nota di credito di acquisto, con un collegamento fisso applicato al movimento di acquisto con il costo unitario diretto errato. La somma del campo **Importo costo (effettivo)** per i due movimenti di valorizzazione fissi diventa 0,00  
3. Nel movimento numero 4, l'utente registra un'altra fattura di acquisto con il costo unitario diretto corretto di VL 100,00  
4. Nel movimento numero 5, l'utente registra una fattura di vendita.  
5. La quantità di magazzino è 0 e anche il valore di magazzino è 0,00  

Nella seguente tabella viene illustrato il risultato dello scenario sui movimenti di valorizzazione dell'articolo.  

Nella seguente tabella viene illustrato il risultato dello scenario nei movimenti di valorizzazione dell'articolo dopo il completamento della registrazione e l'esecuzione della rettifica dei costi.

|Data di registrazione|Tipo mov. articolo|Quantità valorizzata|Importo costo (effettivo)|Collega-a mov. art.|Valutato per costo medio|Nr. movimento cont. articolo|Nr. movimento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Acquisto|1|200.00||No|1|1|  
|01-01-20|Acquisto|1|1000.00||No|2|2|  
|01-01-20|Acquisti|-1|-1000|2|No|3|3|  
|01-01-20|Acquisti|1|100.00||No|4|4|  
|01-01-20|Vendite|-2|-300,00||Sì|5|5|  

Se l'utente non avesse creato il collegamento fisso tra la nota di credito di acquisto e l'acquisto con il costo unitario diretto errato (passaggio 2 nello scenario precedente), il costo sarebbe stato rettificato in modo diverso.  

Nella seguente tabella viene illustrato il risultato sui movimenti di valorizzazione dell'articolo se il passaggio 2 dello scenario precedente viene eseguito senza un collegamento fisso.  

|Data di registrazione|Tipo mov. articolo|Quantità valorizzata|Importo costo (effettivo)|Collega-a mov. art.|Valutato per costo medio|Nr. movimento cont. articolo|Nr. movimento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Acquisto|1|200.00||No|1|1|  
|01-01-20|Acquisto|1|1000.00||No|2|2|  
|01-01-20|Acquisti|-1|433,33||Sì|3|3|  
|01-01-20|Acquisti|1|100.00||No|4|4|  
|01-01-20|Vendita|-2|866,67||Sì|5|5|  

Nel movimento numero 3, il valore nel campo **Importo costo (effettivo)** viene valutato in base alla media e pertanto include la registrazione erronea di 1000,00. Di conseguenza, diventa -433,33 ovvero un importo costo gonfiato. Verrà effettuato il seguente calcolo 1300 / 3 =.-433,33.  

Nel movimento numero 5, anche il valore del campo **Importo costo (effettivo)** per questo movimento risulta inaccurato per lo stesso motivo.  

> [!NOTE]  
>  Se si crea un collegamento fisso per una riduzione di magazzino per un articolo per il quale viene utilizzato il metodo di costing Medio, alla riduzione non viene assegnato il costo medio come avviene in genere, bensì il costo dell'aumento di magazzino specificato. Tale riduzione di magazzino non fa più pertanto parte del calcolo del costo medio.  

### <a name="example--fixed-application-in-sales-return"></a>Esempio: collegamento fisso nel reso di vendita
I collegamenti fissi sono anche uno strumento molto preciso di stornare esattamente i costi, ad esempio con resi di vendita.  

Il seguente esempio, che illustra in che modo un collegamento fisso garantisce lo storno esatto del costo, si basa sul seguente scenario:  

1.  L'utente registra una fattura di acquisto.  
2.  L'utente registra una fattura di vendita.  
3.  L'utente registra una nota di credito vendita per l'articolo reso, collegata al movimento di vendita, per stornare il costo correttamente.  
4.  Viene ricevuto il costo di spedizione collegato all'ordine di acquisto registrato in precedenza. L'utente lo registra come un addebito articolo.  

Nella seguente tabella vengono mostrati i risultati dei passaggi da 1 a 3 dello scenario sui movimenti di valorizzazione dell'articolo.  

|Data di registrazione|Tipo mov. articolo|Quantità valorizzata|Importo costo (effettivo)|Collega-da mov. art.|Nr. movimento cont. articolo|Nr. movimento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Acquisto|1|1000.00||1|1|  
|02-01-20|Vendita|-1|1000.00||2|2|  
|03-01-20|Vendita (Nota credito)|1|1000|2|3|3|  

Nella seguente tabella viene mostrato il movimento di valorizzazione risultante dal passaggio 4 dello scenario, quando si registra un addebito articolo.  

|Data di registrazione|Tipo mov. articolo|Quantità valorizzata|Importo costo (effettivo)|Collega-da mov. art.|Nr. movimento cont. articolo|Nr. movimento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|04-01-20|(Addebito articolo)|1|100.00||1|4|  

Nella seguente tabella viene illustrato l'effetto dello storno esatto del costo sui movimenti di valorizzazione dell'articolo.  

|Data di registrazione|Tipo mov. articolo|Quantità valorizzata|Importo costo (effettivo)|Collega-da mov. art.|Nr. movimento cont. articolo|Nr. movimento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Acquisto|1|1000.00||1|1|  
|02-01-20|Vendita|-1|1100.00||2|2|  
|03-01-20|Vendita (Nota credito)|1|1100.00|2|3|3|  
|04-01-20|(Addebito articolo)|1|100.00||1|4|  

Quando si esegue il processo batch **Rettifica costo - Movimenti articoli**, il costo aumentato del movimento di acquisto, dovuto all'addebito articolo, viene inoltrato al movimento di vendita (numero movimento 2). Il movimento di vendita inoltra quindi questo costo aumentato al movimento credito di vendita (movimento numero 3). Il risultato finale è che il costo viene stornato correttamente.  

> [!NOTE]  
>  Se si stanno utilizzando resi o note di credito ed è stato impostato il campo **Storno esatto costo obblig.** nella pagina **Setup contabilità fornitori e acquisti** o nella pagina **Setup contabilità clienti e vendite** in base alla propria situazione, [!INCLUDE[prod_short](includes/prod_short.md)] compilerà automaticamente i campi di movimento di collegamento quando si utilizza la funzione **Copia da documento**. Se si utilizza la funzione **Ottieni righe documento registrato da stornare**, allora i campi vengono sempre compilati automaticamente.  

> [!NOTE]  
>  Se si registra una transazione con un collegamento fisso e il movimento contabile articolo a cui si sta effettuando il collegamento è chiuso, ovvero la quantità residua è zero, allora il collegamento precedente viene automaticamente annullato e il movimento contabile articolo viene collegato di nuovo utilizzando il collegamento fisso specificato.  

## <a name="transfer-application"></a>Applicazione trasferimento
Quando un articolo viene trasferito da un'ubicazione a un'altra, all'interno del magazzino della società, viene creato un collegamento tra i due movimenti di trasferimento. La valutazione di un movimento di trasferimento dipende dal metodo di costing. Per gli articoli che utilizzano il metodo di costing medio, la valutazione viene effettuata utilizzando il costo medio nel costo medio del periodo in cui si verifica la data di valutazione di trasferimento. Per gli articoli che utilizzano altri metodi di costing, la valutazione viene effettuata ritracciando al costo dell'aumento di magazzino originale.  

### <a name="example--average-costing-method"></a>Esempio: metodo di costing medio
Il seguente esempio, che illustra la modalità di applicazione dei movimenti di trasferimento, si basa sul seguente scenario di un articolo che utilizza il metodo di costing medio e il costo medio del periodo Giorno.  

1. L'utente acquista l'articolo a un costo di VL 10,00.  
2. L'utente acquista nuovamente l'articolo a un costo di VL 20,00.  
3. L'utente trasferisce l'articolo dall'ubicazione EST all'ubicazione OVEST.  

Nella seguente tabella viene illustrato l'effetto del trasferimento sui movimenti di valorizzazione dell'articolo.  

|Data di registrazione|Tipo mov. articolo|Cod. ubicazione|Quantità valorizzata|Importo costo (effettivo)|Nr. movimento|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Acquisti|EST|1|10,00|1|  
|01-01-20|Acquisti|EST|1|20,00|2|  
|02-01-20|Trasferimento|EST|-1|15.00|3|  
|02-01-20|Trasferimento|OVEST|1|15.00|4|  

### <a name="example--standard-costing-method"></a>Esempio: Metodo di costing standard
Il seguente esempio, che illustra la modalità di applicazione dei movimenti di trasferimento, si basa sul seguente scenario di un articolo che utilizza il metodo di costing standard e il costo medio del periodo Giorno.  

1. L'utente acquista l'articolo a un costo standard di VL 10,00.  
2. L'utente trasferisce l'articolo dall'ubicazione EST all'ubicazione OVEST a un costo standard di VL 12,00.  

Nella seguente tabella viene illustrato l'effetto del trasferimento sui movimenti di valorizzazione dell'articolo.  

|Data di registrazione|Tipo mov. articolo|Cod. ubicazione|Quantità valorizzata|Importo costo (effettivo)|Nr. movimento|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Acquisti|EST|1|10,00|1|  
|02-01-20|Trasferimento|EST|-1|10,00|2|  
|02-01-20|Trasferimento|OVEST|1|10,00|3|  

Poiché il valore dell'aumento di magazzino originale è VL 10,00, il trasferimento viene valutato a quel costo, non a VL 12,00.  

## <a name="reapplication"></a>Nuovo collegamento
A causa della modalità di calcolo del costo unitario di un articolo, un collegamento articoli non corretto potrebbe portare a un costo medio o a un costo unitario non attendibile. Gli scenari seguenti possono determinare dei collegamenti articoli errati. Potrebbero richiedere l'annullamento dei collegamenti articoli e la creazione di un nuovo collegamento dei movimenti contabili articoli:  

* Ci si è dimenticati di creare un collegamento fisso.  
* È stato creato un collegamento fisso non corretto.  
* Si desidera oltrepassare il collegamento creato automaticamente durante la registrazione, in base al metodo di costing dell'articolo.  
* È necessario restituire un articolo a cui è stata stata collegata manualmente una vendita, senza utilizzare la funzione **Ottieni righe documento registrato da stornare**, ed è di conseguenza necessario annullare il collegamento.  

[!INCLUDE[prod_short](includes/prod_short.md)] offre una funzionalità per l'analisi e la correzione dei collegamenti articoli. Questa operazione può essere effettuata nella pagina **Prospetto collegamento**.  

## <a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Problema noto di collegamento articoli](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)  
[Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)  
[Dettagli di progettazione: Costo medio](design-details-average-cost.md)   
[Dettagli di progettazione: Rettifica costo](design-details-cost-adjustment.md)  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
