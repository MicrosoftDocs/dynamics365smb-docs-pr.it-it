---
title: Informazioni sugli ordini di produzione
description: Scopri gli ordini di produzione e come vengono utilizzati per gestire la conversione dei materiali acquistati in articoli lavorati.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-production-orders"></a>Informazioni sugli ordini di produzione

Gli ordini di produzione vengono utilizzati per gestire la conversione dei materiali acquistati in articoli prodotti. Gli ordini di produzione diramano il lavoro in diverse aree di produzione o centri di lavoro nella produzione.  

Prima di procedere con la produzione, la maggior parte delle società esegue, in genere una volta alla settimana, la pianificazione delle forniture, per calcolare il numero di ordini di produzione e di ordini di acquisto da eseguire per soddisfare la domanda di vendita della settimana. Gli ordini di acquisto forniscono i componenti richiesti in base alla DB di produzione per produrre gli articoli finali.

Gli ordini di produzione sono i componenti centrali della funzionalità di produzione e contengono le seguenti informazioni:  

- Prodotti pianificati per la produzione  
- Materiali necessari per gli ordini di produzione pianificati  
- Prodotti lavorati  
- Materiali già selezionati  
- Prodotti lavorati in passato  
- Materiali utilizzati in operazioni di produzione precedenti  

Gli ordini di produzione costituiscono il punto iniziale per:  

- Pianificazione della produzione futura  
- Controllo della produzione corrente  
- Tracciabilità della produzione finita  

## <a name="production-order-creation"></a>Creazione di ordini di produzione

Puoi creare un ordine di produzione alla volta manualmente nella pagina **Ordine di produzione** oppure generarli nelle pagine **Ordine vendita** o **Pianificazione ordine**. Puoi anche creare più ordini nella pagina **Prospetto pianificazione**.  

Gli ordini di produzione vengono creati utilizzando le informazioni in:  

- Articoli  
- Dist.base di produz.
- Cicli  
- Centri di lavoro  
- Aree di produzione  

## <a name="limitations-on-creating-production-orders"></a>Limiti sulla creazione di ordini di produzione

Gli ordini di produzione vengono impegnati e tracciati automaticamente nella rispettiva origine quando:  

- Vengono creati nella finestra [Prospetto pianificazione](production-how-to-run-mps-and-mrp.md)  
- Vengono creati dalla pagina [Pianifica ordine vendita](production-how-to-create-production-orders-from-sales-orders.md)  
- Vengono creati nella pagina [Pianificazione ordini](production-how-to-plan-for-new-demand.md)  
- Si utilizza la funzione [Ripianifica](production-how-to-replan-refresh-production-orders.md) negli ordini di produzione  

Per ulteriori informazioni, vedere [Tenere traccia delle relazioni tra domanda e approvvigionamento](production-how-track-demand-supply.md)

Gli ordini di produzione creati tramite altri mezzi non vengono impegnati e tracciati automaticamente.

## <a name="production-order-status"></a>Stato dell'ordine di produzione

Lo stato dell'ordine di produzione definisce il comportamento dell'ordine di produzione nell'applicazione. Lo stato dell'ordine determina la forma e il contenuto della produzione. Gli ordini di produzione vengono visualizzati in pagine differenti in funzione del proprio stato. Lo stato di un ordine di produzione non può essere modificato manualmente. Devi utilizzare la funzione **Cambia stato** nel singolo ordine di produzione o nella pagina **Modifica stato ordine di produzione**.  

### <a name="simulated-production-order"></a>Ordine di produzione simulato

Un ordine di produzione simulato è univoco e si basa sulle seguenti caratteristiche:  

- Come suggerisce il nome, è una simulazione che puoi utilizzare per offerte e costing. Ad esempio, quando il reparto Ricerca e Sviluppo desidera ottenere una stima dei costi su un articolo proposto. Un ordine di produzione simulato funge da esempio di un ordine di produzione.  
- Non influisce sulla pianificazione degli ordini. La pianificazione (MPS e MRP) non prende in considerazione gli ordini di produzione simulati e non ne viene influenzata. Un ordine di produzione simulato, inoltre, non può essere utilizzato come modello, in quanto non è più disponibile quando se ne modifica lo stato.  

### <a name="planned-production-order"></a>Ordine di produzione pianificato

Un ordine di produzione pianificato è univoco per via delle seguenti caratteristiche:  

- È possibile creare automaticamente un ordine di produzione pianificato da un ordine di vendita.  
- Gli ordini di produzione pianificati sono analoghi agli ordini di produzione rilasciati e forniscono input per la pianificazione dei requisiti di capacità indicando i requisiti di capacità totale in base ad area di produzione o centro di lavoro.  
- Un ordine di produzione pianificato rappresenta la stima più realistica del carico futuro per l'area di produzione o il centro di lavoro in base alle informazioni disponibili. In genere tali ordini vengono generati dalla pianificazione, ma possono anche essere creati manualmente. Poiché vengono cancellati durante le operazioni di pianificazione successive, la creazione manuale non rappresenta un metodo efficace.  
- La generazione di tali ordini nella produzione ha come risultato un "rilascio di ordini pianificati" suggerito, in cui sono inclusi quantità, data di rilascio e data di scadenza. La logica del sistema di pianificazione si basa sul sistema di rifornimento, i criteri di riordino e i modificatori di ordini rilevati nel processo di pianificazione dei fabbisogni.  
- Per esaminarne l'impatto, fai riferimento al carico di ogni area di produzione o centro di lavoro nel ciclo dell'ordine di produzione pianificato.  

### <a name="firm-planned-production-order"></a>Ordine di produzione pianificato confermato

Un ordine di produzione pianificato confermato è univoco per via delle seguenti caratteristiche:  

- È possibile creare automaticamente un ordine di produzione confermato da un ordine di vendita.  
- Un ordine di produzione confermato agisce da segnaposto nella programmazione della pianificazione di alcuni futuri progetti rilasciati.  
- Un ordine di produzione confermato può essere generato dalla pianificazione oppure può essere creato manualmente o dagli ordini di vendita. Non vengono cancellati durante la successiva pianificazione.  
- La generazione di tali ordini nella produzione ha come risultato un "rilascio di ordini pianificati" suggerito, in cui sono inclusi quantità, data di rilascio e data di scadenza. La logica del sistema di pianificazione si basa sul sistema di rifornimento, i criteri di riordino e i modificatori di ordini rilevati nel processo di pianificazione dei fabbisogni.  
- Per esaminarne l'effetto, fai riferimento al carico di ogni area di produzione o centro di lavoro nel ciclo dell'ordine di produzione pianificato.  

### <a name="released-production-order"></a>Ordine di produzione rilasciato

L'ordine di produzione rilasciato è univoco per via delle seguenti caratteristiche:  

- È possibile creare automaticamente un ordine di produzione rilasciato da un ordine di vendita.  
- Il fatto che un ordine di produzione venga rilasciato non significa necessariamente che i materiali vengano prelevati o che il progetto sia fisicamente passato alla prima operazione.  
- In un ambiente di produzione su ordine, non è insolito creare un ordine di produzione rilasciato immediatamente dopo l'immissione dell'ordine di vendita.  
- Il consumo dei materiali e l'output di prodotti effettivi possono essere registrati manualmente con un ordine di produzione rilasciato. La consuntivazione automatica del consumo e dell'output di prodotti, inoltre, viene eseguita solo per gli ordini di produzione rilasciati.  

### <a name="finished-production-order"></a>Ordine di produzione chiuso

Un ordine di produzione chiuso è univoco per via delle seguenti caratteristiche:  

- Un ordine di produzione chiuso è in genere un ordine lavorato.  
- La chiusura di un ordine di produzione è un'attività importante nel completamento del ciclo di vita del costing dell'articolo prodotto. Alla chiusura di un ordine di produzione, è possibile rettificare e riconciliare il costing.  
- Gli ordini di produzione chiusi vengono utilizzati per il reporting statistico e per supportare la tracciabilità all'indietro ad altri ordini, ad esempio di vendita, di produzione e di acquisto. La possibilità di effettuare la tracciabilità all'indietro di un ordine di produzione chiuso consente di esaminare lo storico dettagliato.  
- Gli ordini di produzione chiusi non possono mai essere modificati.  

## <a name="production-order-execution"></a>Esecuzione di ordini di produzione

Dopo che un ordine di produzione è stato creato e pianificato, deve essere rilasciato alla produzione per essere eseguito. Durante l'esecuzione dell'ordine vengono registrati i seguenti dati:  

- I materiali prelevati o consumati  
- Quantità di tempo spesa lavorando sull'ordine  
- La quantità dell'articolo padre prodotta  

Puoi registrate queste informazioni manualmente o tramite reporting automatico. Il metodo dipende dall'impostazione nel campo Metodo consuntivazione dell'articolo e dell'area di produzione.  

### <a name="material-consumption"></a>Consumo materiale

[!INCLUDE [prod_short](includes/prod_short.md)] offre varie opzioni su come registrare il consumo dei materiali. Il consumo dei materiali, ad esempio, può essere registrato manualmente, opzione preferibile nel caso di frequenti sostituzioni di componenti o di scarti maggiori del previsto.  

Il consumo dei materiali può essere elaborato tramite la [registrazione consumi](production-how-to-post-consumption.md) ma può anche essere registrato automaticamente da [!INCLUDE [prod_short](includes/prod_short.md)], noto come reporting automatico (consuntivazione). Sono disponibili i metodi di reporting Manuale, In avanti e A ritroso.

Il reporting dei consumi manuale utilizza le registrazioni consumi per specificare il prelievo dei materiali.  

Il reporting dei consumi In avanti presuppone che la quantità prevista di tutti i materiali per l'intero ordine venga consumata al rilascio dell'ordine di produzione, a meno che non si utilizzino codici di legame tra ciclo-DB. In questo secondo caso, il materiale consumato dopo l'inizio del passaggio operativo viene registrato nelle registrazioni output. Per la consuntivazione in avanti dell'intero ordine di produzione, è necessario effettuare due operazioni:  

- Nella scheda articolo di ciascun articolo incluso nella DB di produzione di livello principale deve essere selezionata la consuntivazione in avanti.  
- Tutti i codici di legame tra ciclo e distinta base nella DB di produzione devono essere rimossi.  

Il reporting dei consumi A ritroso registra l'effettiva quantità di tutto il materiale prelevato o consumato quando lo stato di un ordine di produzione viene modificato in *Completato*, a meno che non si utilizzino codici di legame tra ciclo e distinta base. In questo secondo caso, il materiale viene consumato dopo la registrazione di una quantità dell'articolo padre per il passaggio operativo nelle registrazioni output.  

Quando l'ordine di produzione viene aggiornato, il metodo di consuntivazione viene copiato dalla scheda articolo. Poiché il metodo di consuntivazione per ogni componente dell'ordine di produzione determina la modalità e il momento di registrazione del consumo, è importante notare che è possibile modificare il metodo di consuntivazione per articoli specifici direttamente nell'ordine di produzione. Per ulteriori informazioni vedere [Componenti ordine produzione a livello in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md).

### <a name="production-output"></a>Output produzione

[!INCLUDE [prod_short](includes/prod_short.md)] offre la possibilità di tenere traccia del tempo speso per un ordine di produzione, nonché di registrare la quantità prodotta. Queste informazioni possono essere utili per determinare in modo più accurato i costi di produzione. Inoltre, i produttori che utilizzano un sistema di costing standard potrebbero registrare le informazioni effettive per sviluppare standard migliori.  

L'output può essere elaborato tramite le [registrazioni output](production-how-to-post-output-quantity.md) ma anche essere registrato automaticamente. [!INCLUDE [prod_short](includes/prod_short.md)] copia il metodo di consuntivazione dalla scheda del centro di lavoro o dell'area di produzione al ciclo dell'ordine di produzione durante l'aggiornamento. Come per il consumo dei materiali, per l'output sono disponibili i metodi di reporting Manuale, In avanti e A ritroso:

Nel metodo Manuale vengono utilizzate le registrazioni output per specificare il tempo consumato e la quantità prodotta.  

Il metodo In avanti registra l'output e il tempo previsti, che vengono registrati automaticamente al momento del rilascio di un ordine di produzione. I codici di collegamento tra ciclo e distinta base non costituiscono un fattore nella consuntivazione in avanti dell'output.  

Il metodo A ritroso registra l'output e il tempo previsti, che vengono registrati automaticamente al momento della chiusura di un ordine di produzione. I codici di collegamento tra ciclo e distinta base non costituiscono un fattore nella consuntivazione a ritroso dell'output.  

### <a name="posting-consumption-and-output"></a>Registrazione di consumo e output

È possibile utilizzare qualsiasi combinazione di consuntivazione automatica e registrazione manuale delle informazioni sia per il consumo che per l'output. Ad esempio, è possibile che tu voglia eseguire la consuntivazione in avanti automatica dei componenti, ma utilizzare comunque le registrazioni consumi per registrare gli scarti. Analogamente, potresti voler registrare automaticamente l'output, ma utilizzare le registrazioni output per registrare gli scarti dell'articolo padre o il tempo aggiuntivo speso per l'ordine.  

Se infine si immettono il consumo e l'output manualmente, è necessario determinare la sequenza in cui verranno registrate tali informazioni. È possibile registrare prima il consumo e quindi utilizzare un metodo rapido per immettere le informazioni in base alla quantità di output prevista. In alternativa, è possibile immettere prima l'output utilizzando la funzione **Esplodi ciclo**. Si registrerà quindi il consumo in base all'effettiva quantità di output.  

### <a name="production-journal"></a>Registrazioni di produzione

La funzionalità [Registrazioni di produzione](production-how-to-register-consumption-and-output.md) combina le funzioni di registrazioni consumi e registrazioni output in una singola registrazione, a cui è possibile accedere direttamente dall'ordine di produzione rilasciato.  

Lo scopo delle registrazioni di produzione consiste nel fornire un'unica interfaccia per registrare il consumo e l'output da un ordine di produzione.  

Le registrazioni di produzione includono una visualizzazione semplice e ti consentono di effettuare le seguenti operazioni:  

- Registrare facilmente l'output e il consumo correlati a un ordine di produzione  
- Correlare i componenti alle operazioni  
- Correlare i dati delle operazioni effettive alle stime standard nelle righe di cicli e componenti dell'ordine di produzione  
- Registrare e stampare una panoramica dei dati operativi registrati per un ordine di produzione  

Le registrazioni di produzione consentono di eseguire molte delle funzioni disponibili con le registrazioni consumi e output. Le dimensioni, la tracciabilità degli articoli e il contenuto delle collocazioni vengono gestiti allo stesso modo.  

Le registrazioni di produzione, tuttavia, presentano le seguenti differenze rispetto alle registrazioni consumi e output:  

- Vengono chiamate direttamente da una riga di ordine di produzione rilasciato e impostate con i dati pertinenti.  
- Consentono di definire i tipi di componenti da gestire in base al filtro del metodo di consuntivazione nelle registrazioni.  
- Quantità e tempi già registrati per l'ordine vengono visualizzati nella parte inferiore delle registrazioni come movimenti effettivi.  
- I campi in cui l'immissione di dati è irrilevante sono vuoti e non modificabili.  
- L'utente può specificare la modalità di preimpostazione delle quantità di output nelle registrazioni. È possibile specificare, ad esempio, che l'ultima operazione deve essere impostata su zero come quantità di output.  
- Se si esce dalle registrazioni senza registrare le modifiche, viene visualizzato un messaggio di richiesta che consente di tornare alle registrazioni.  
- Consentono di visualizzare operazioni e componenti in una struttura logica che fornisce una panoramica del processo di produzione.  

Nelle registrazioni di produzione le quantità dei consumi vengono registrate come movimenti contabili negativi per gli articoli, le quantità di output vengono registrate come movimenti contabili positivi e il tempo speso viene registrato come movimenti contabili capacità.  

## <a name="see-also"></a>Vedere anche

[Manufacturing](production-manage-manufacturing.md)
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
