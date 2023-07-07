---
title: Informazioni sugli ordini di produzione
description: Informazioni sugli ordini di produzione e su come vengono utilizzati per gestire la conversione dei materiali acquistati in articoli prodotti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="about-production-orders"></a>Informazioni sugli ordini di produzione

Gli ordini di produzione vengono utilizzati per gestire la conversione dei materiali acquistati in articoli prodotti. Gli ordini di produzione diramano il lavoro in diverse aree di produzione o centri di lavoro nella produzione.  

Prima di procedere con la produzione, la maggior parte delle società esegue, in genere una volta alla settimana, la pianificazione delle forniture, per calcolare il numero di ordini di produzione e di ordini di acquisto da eseguire per soddisfare la domanda di vendita della settimana. Gli ordini di acquisto forniscono i componenti richiesti in base alla DB di produzione per produrre gli articoli finali.

Gli ordini di produzione rappresentano i componenti centrali della funzionalità di produzione dell'applicazione e contengono le seguenti informazioni:  

- Prodotti pianificati per la produzione  
- Materiali necessari per gli ordini di produzione pianificati  
- Prodotti già lavorati  
- Materiali già selezionati  
- Prodotti lavorati in passato  
- Materiali utilizzati in operazioni di produzione precedenti  

Gli ordini di produzione costituiscono il punto iniziale per:  

- Pianificazione della produzione futura  
- Controllo della produzione corrente  
- Tracciabilità della produzione finita  

## <a name="production-order-creation"></a>Creazione di ordini di produzione
Gli ordini di produzione possono essere creati manualmente ordine per ordine nella pagina **Ordine di produzione** oppure possono essere generati nelle pagine **Ordine vendita** o **Pianificazione ordine**. È possibile creare più ordini nella pagina **Prospetto pianificazione**.  

Gli ordini di produzione vengono creati utilizzando le informazioni relative a:  

- Articoli  
- Dist.base di produz.
- Cicli  
- Centri di lavoro  
- Aree di produzione  

## <a name="limitations-on-production-order-creation"></a>Limiti sulla creazione degli ordini di produzione
Gli ordini di produzione vengono impegnati e tracciati automaticamente nella rispettiva origine quando:  

- Vengono creati da **[Prospetto pianificazione](production-how-to-run-mps-and-mrp.md)**.  
- Vengono creati dalla pagina **[Pianifica ordine vendita](production-how-to-create-production-orders-from-sales-orders.md)**  
- Vengono creati dalla pagina **[Pianificazione ordini](production-how-to-plan-for-new-demand.md)**  
- Si utilizza la funzione **[Ripianifica](production-how-to-replan-refresh-production-orders.md)** negli ordini di produzione  

Per ulteriori informazioni, vedere [Tenere traccia delle relazioni tra domanda e approvvigionamento](production-how-track-demand-supply.md)

Gli ordini di produzione creati tramite altri mezzi non vengono impegnati e tracciati automaticamente.   

## <a name="production-order-status"></a>Stato dell'ordine di produzione
Lo stato dell'ordine di produzione definisce il comportamento dell'ordine di produzione nell'applicazione. La forma e il contenuto della produzione sono determinati dallo stato dell'ordine. Gli ordini di produzione vengono visualizzati in pagine differenti in funzione del proprio stato. Non è possibile modificare manualmente lo stato di un ordine di produzione; è necessario utilizzare la funzione **Cambia stato** nel singolo ordine di produzione o nella finestra **Modifica stato ordine di produzione**.  

### <a name="simulated-production-order"></a>Ordine di produzione simulato
L'ordine di produzione simulato si distingue in base alle seguenti caratteristiche:  

- Come suggerito dal nome, rappresenta una simulazione il cui scopo principale sono l'esecuzione di offerte e il costing, ad esempio quando il reparto Ricerca e sviluppo desidera ottenere una valutazione dei costi su un articolo proposto. Un ordine di produzione simulato funge da esempio di un ordine di produzione.  
- Non influisce sulla pianificazione degli ordini. La pianificazione (MPS e MRP) non considera gli ordini di produzione simulati, né ne viene influenzata. Un ordine di produzione simulato, inoltre, non può essere utilizzato come modello, in quanto non è più disponibile quando se ne modifica lo stato.  

### <a name="planned-production-order"></a>Ordine di produzione pianificato
L'ordine di produzione pianificato si distingue per le seguenti caratteristiche:  

- È possibile creare automaticamente un ordine di produzione pianificato da un ordine di vendita.  
- Gli ordini di produzione pianificati sono analoghi agli ordini di produzione rilasciati e forniscono input per la pianificazione dei requisiti di capacità indicando i requisiti di capacità totale in base ad area di produzione o centro di lavoro.  
- Un ordine di produzione pianificato rappresenta la stima più realistica del carico futuro per l'area di produzione o il centro di lavoro in base alle informazioni disponibili. In genere tali ordini vengono generati dalla pianificazione, ma possono anche essere creati manualmente. Poiché questi ordini vengono cancellati durante le operazioni di pianificazione successive, la creazione manuale non rappresenta un metodo efficace.  
- La generazione di tali ordini nella produzione ha come risultato un "rilascio di ordini pianificati" suggerito, in cui sono inclusi quantità, data di rilascio e data di scadenza. La logica del sistema di pianificazione si basa sul sistema di rifornimento, i criteri di riordino e i modificatori di ordini rilevati nel processo di pianificazione dei fabbisogni.  
- Per esaminarne l'impatto, fare riferimento al carico di ogni area di produzione o centro di lavoro nel ciclo dell'ordine di produzione pianificato.  

### <a name="firm-planned-production-order"></a>Ordine di produzione confermato
L'ordine di produzione confermato si distingue per le seguenti caratteristiche:  

- È possibile creare automaticamente un ordine di produzione confermato da un ordine di vendita.  
- Un ordine di produzione confermato funge da segnaposto nella programmazione della pianificazione di alcune future commesse rilasciate.  
- Un ordine di produzione confermato può essere generato dalla pianificazione oppure può essere creato manualmente o dagli ordini di vendita. Non vengono cancellati durante la successiva pianificazione.  
- La generazione di tali ordini nella produzione ha come risultato un "rilascio di ordini pianificati" suggerito, in cui sono inclusi quantità, data di rilascio e data di scadenza. La logica del sistema di pianificazione si basa sul sistema di rifornimento, i metodi di riordino e i modificatori di ordini rilevati nel processo di pianificazione dei fabbisogni.  
- Per esaminarne l'impatto, fare riferimento al carico di ogni area di produzione o centro di lavoro nel ciclo dell'ordine di produzione pianificato.  

### <a name="released-production-order"></a>Ordine di produzione rilasciato
L'ordine di produzione rilasciato si distingue in base alle seguenti caratteristiche:  

- È possibile creare automaticamente un ordine di produzione rilasciato da un ordine di vendita.  
- Il fatto che un ordine di produzione sia stato rilasciato non significa necessariamente che i materiali siano stati prelevati o che la commessa sia fisicamente passata alla prima operazione.  
- In un ambiente di tipo produzione su ordine, non è insolito creare un ordine di produzione rilasciato immediatamente dopo l'immissione dell'ordine di vendita.  
- Il consumo dei materiali e l'output di prodotti effettivi possono essere registrati manualmente con un ordine di produzione rilasciato. La consuntivazione automatica del consumo e dell'output di prodotti, inoltre, viene eseguita solo per gli ordini di produzione rilasciati.  

### <a name="finished-production-order"></a>Ordine di produzione chiuso
L'ordine di produzione chiuso si distingue in base alle seguenti caratteristiche:  

- Un ordine di produzione chiuso è in genere un ordine già lavorato.  
- La chiusura di un ordine di produzione è un'attività importante nel completamento del ciclo di vita del costing dell'articolo prodotto. Tramite la chiusura di un ordine di produzione, è possibile rettificare e riconciliare il costing.  
- Gli ordini di produzione chiusi vengono utilizzati per il reporting statistico e per supportare la tracciabilità all'indietro ad altri ordini, ad esempio di vendita, di produzione e di acquisto. La possibilità di effettuare la tracciabilità all'indietro di un ordine di produzione chiuso consente di esaminare lo storico dettagliato.  
- Gli ordini di produzione chiusi non possono mai essere modificati.  

## <a name="production-order-execution"></a>Esecuzione degli ordini di produzione
Dopo che un ordine di produzione è stato creato e pianificato, deve essere rilasciato alla produzione per essere eseguito. Durante l'esecuzione dell'ordine vengono registrati i seguenti dati:  

- Materiali prelevati o consumati  
- Quantità di tempo spesa lavorando sull'ordine  
- Quantità dell'articolo padre prodotta  

Queste informazioni possono essere registrate manualmente o tramite reporting automatico, in base al setup nel campo Metodo consuntivazione dell'articolo e l'area di produzione.  

### <a name="material-consumption"></a>Consumo dei materiali
L'applicazione offre un'ampia gamma di opzioni per la registrazione del consumo dei materiali a un'azienda manifatturiera. Il consumo dei materiali, ad esempio, può essere registrato manualmente, opzione preferibile nel caso di frequenti sostituzioni di componenti o di uno scarto maggiore del previsto.  

Il consumo dei materiali può essere elaborato tramite le [registrazioni consumi](production-how-to-post-consumption.md) oppure registrato automaticamente dall'applicazione mediante la funzione di reporting automatico (consuntivazione). Di seguito vengono indicati i metodi di reporting:  

- Manuale  
- Aut. inizio  
- Aut. fine  

Il reporting dei consumi manuale utilizza le registrazioni consumi per specificare il prelievo dei materiali.  

Il reporting dei consumi aut. avanti presuppone che la quantità prevista di tutti i materiali per l'intero ordine venga consumata al rilascio dell'ordine di produzione, a meno che non si utilizzino codici di legame tra ciclo-DB. In questo secondo caso, il materiale consumato in seguito all'inizio del passaggio operativo viene registrato nelle registrazioni di output. Per la consuntivazione in avanti dell'intero ordine di produzione, è necessario effettuare due operazioni:  

- Nella scheda articolo di ciascun articolo incluso nella DB di produzione di livello principale deve essere selezionata la consuntivazione in avanti.  
- Tutti i codici di legame tra ciclo e distinta base nella DB di produzione devono essere rimossi.  

Il reporting dei consumi aut. fine registra l'effettiva quantità di tutto il materiale prelevato o consumato quando lo stato di un ordine di produzione viene modificato in *Completato*, a meno che non si utilizzino codici di legame tra ciclo e distinta base. In questo secondo caso, il materiale viene consumato in seguito alla registrazione dell'articolo principale per il passaggio operativo nelle registrazioni di output.  

Quando l'ordine di produzione viene aggiornato, il metodo di consuntivazione viene copiato dalla scheda articolo. Poiché il metodo di consuntivazione per ogni componente dell'ordine di produzione determina la modalità e il momento di registrazione del consumo, è importante notare che è possibile modificare tale metodo per articoli specifici direttamente nell'ordine di produzione. 

Per ulteriori informazioni vedere [Componenti ordine produzione a livello in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md)

### <a name="production-output"></a>Output di produzione
L'applicazione offre la possibilità di tenere traccia del tempo speso per lavorare su un ordine di produzione, nonché di registrare la quantità prodotta. Queste informazioni possono essere utili per determinare in modo più accurato i costi di produzione. I produttori che utilizzano un sistema di costing standard, inoltre, possono registrare le informazioni effettive per sviluppare standard migliori.  

L'output può essere elaborato tramite le [registrazioni di output](production-how-to-post-output-quantity.md) oppure può essere registrato automaticamente dall'applicazione. Il metodo di consuntivazione viene copiato dall'applicazione dalla scheda centro di lavoro o area di produzione al ciclo dell'ordine di produzione durante l'aggiornamento. Come per il consumo dei materiali, sono disponibili tre metodi di reporting dell'output:  

- Manuale  
- Aut. inizio  
- Aut. fine  

Nel metodo manuale vengono utilizzate le registrazioni output per specificare il tempo consumato e la quantità prodotta.  

Il metodo aut. inizio consente di registrare automaticamente l'output e il tempo previsti al momento del rilascio di un ordine di produzione. I codici di legame tra ciclo e distinta base non costituiscono un fattore interessato dalla consuntivazione in avanti dell'output.  

Il metodo aut.fine consente di registrare automaticamente l'output e il tempo previsti al momento della chiusura di un ordine di produzione. I codici di legame tra ciclo e distinta base non costituiscono un fattore interessato dalla consuntivazione a ritroso dell'output.  

### <a name="posting-consumption-and-output"></a>Registrazione di consumo e output
È possibile utilizzare qualsiasi combinazione di consuntivazione automatica e registrazione manuale delle informazioni sia per il consumo che per l'output. È possibile, ad esempio, eseguire la consuntivazione in avanti automatica dei componenti, ma utilizzare le registrazioni dei consumi per registrare lo scarto. Analogamente, è possibile registrare automaticamente l'output, ma utilizzare le registrazioni di output per registrare lo scarto dell'articolo principale o il tempo aggiuntivo speso sull'ordine.  

Se infine si immettono il consumo e l'output manualmente, è necessario determinare la sequenza in cui verranno registrate tali informazioni. È possibile registrare prima il consumo e quindi utilizzare un metodo rapido per immettere le informazioni in base alla quantità di output prevista. In alternativa, è possibile immettere prima l'output utilizzando la funzione **Esplodi ciclo**. Si registrerà quindi il consumo in base all'effettiva quantità di output.  

### <a name="production-journal"></a>Registrazioni di produzione
La funzionalità [Registrazioni di produzione](production-how-to-register-consumption-and-output.md) combina le funzioni Registrazioni consumi e Registrazioni output in una singola registrazione, cui è possibile accedere direttamente dall'ordine di produzione rilasciato.  

Lo scopo della funzionalità Registrazioni di produzione consiste nel fornire un'unica interfaccia per registrare il consumo e l'output da un ordine di produzione.  

La funzionalità Registrazioni di produzione fornisce un'interfaccia semplice e consente di effettuare le seguenti operazioni:  

- Registrare in modo facile l'output e il consumo correlati a un ordine di produzione  
- Correlare i componenti alle operazioni  
- Correlare i dati delle operazioni effettive alle stime standard nelle righe cicli e componenti dell'ordine di produzione  
- Registrare e stampare una panoramica dei dati operativi registrati per l'ordine di produzione  

Le registrazioni di produzione consentono di eseguire molte delle funzioni disponibili nelle registrazioni dei consumi e dell'output. Le dimensioni, la tracciabilità degli articoli e il contenuto collocazioni vengono gestiti allo stesso modo che nelle registrazioni dei consumi e dell'output.  

Le registrazioni di produzione, tuttavia, differiscono dalle altre due registrazioni per le seguenti caratteristiche:  

- Vengono chiamate direttamente da una riga di ordine di produzione rilasciato e impostate con i dati pertinenti.  
- Consentono di definire i tipi di componenti da gestire in base al filtro del metodo di consuntivazione nelle registrazioni.  
- Le quantità e i tempi già registrati per l'ordine vengono visualizzati nella parte inferiore delle registrazioni come movimenti effettivi.  
- I campi in cui l'immissione di dati è irrilevante sono vuoti o non modificabili.  
- L'utente può specificare la modalità di preimpostazione delle quantità di output nelle registrazioni. È possibile specificare, ad esempio, che l'ultima operazione deve essere impostata su zero come quantità di output.  
- Se si esce dalle registrazioni senza registrare le modifiche, viene visualizzato un messaggio di richiesta che consente di tornare alle registrazioni.  
- Consentono di visualizzare operazioni e componenti in una struttura logica che fornisce una panoramica del processo di produzione.  

Nelle registrazioni di produzione le quantità dei consumi vengono registrate come movimenti contabili negativi per gli articoli, le quantità di output vengono registrate come movimenti contabili positivi e il tempo speso viene registrato come movimenti contabili capacità.  

## <a name="see-also"></a>Vedi anche
[Manufacturing](production-manage-manufacturing.md)
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
