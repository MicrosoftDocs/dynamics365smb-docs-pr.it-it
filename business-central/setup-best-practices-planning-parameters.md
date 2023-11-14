---
title: Impostare le procedure ottimali - Pianificazione dei parametri
description: Questo argomento descrive le procedure consigliate per impostare i campi dei parametri di pianificazione selezionati con la Scheda dettaglio Pianificazione nella scheda articolo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Impostare le procedure ottimali: Pianificazione dei parametri

La Scheda dettaglio **Pianificazione** nella scheda articolo è l'elemento centrale della supply chain di una società. L'impostazione dei parametri di pianificazione corretti è molto importante per un controllo del magazzino conveniente e un'assistenza clienti di ottima qualità.  

 Nella seguente tabella vengono fornite le procedure consigliate sulla modalità di impostazione dei campi dei parametri di pianificazione selezionati. Per ulteriori informazioni su un campo, scegliere il collegamento nella colonna **Campo Setup**.  

|Campo Setup|Procedura consigliata|Commento|  
|-----------------|-------------------|-------------|  
|Metodo di riordino||Per ulteriori informazioni, vedere [Impostare le procedure ottimali: metodi di riordino](setup-best-practices-reordering-policies.md).|  
|Impegna|Selezionare **Mai** quando l'articolo viene pianificato utilizzando un punto di riordino.<br /><br /> Nella produzione selezionare **Mai** per consentire al sistema di pianificazione di soddisfare tutte le richieste.<br /><br /> Selezionare **Facoltativo** per gli articoli che si potrebbero voler riservare a clienti prioritari.<br /><br /> Selezionare **Sempre** per articoli specifici, come (tipo di articoli non standard), ad esempio, articoli di tipo vario che sono in entrata per domande specifiche.|Gli impegni in genere neutralizzano lo scopo della pianificazione, ovvero bilanciare la domanda e l'approvvigionamento. Pertanto, gli articoli impostati per la pianificazione in genere non devono essere impegnati.<br /><br /> Se l'utente impegna una quantità di magazzino per una richiesta futura, la struttura di pianificazione verrà disturbata e il punto di riordino potrebbe non funzionare correttamente. Anche se il livello della quantità scorte previste è ammesso relativamente al punto di riordino, le quantità potrebbero non essere disponibili a causa dell'impegno.|  
|Periodo di stabilizzazione|Impostare relativamente alla flessibilità del fornitore.<br /><br /> Un periodo più breve consente di ridurre il capitale di lavoro evitando scorte eccessive, ma comporta anche azioni di riprogrammazione.|Se il fornitore accetta le modifiche dell'ultimo minuto agli ordini, utilizzare un periodo più breve, ma essere pronti a più azioni di riprogrammazione. Se il fornitore richiede una pianificazione costante, estendere il periodo il più possibile.<br /><br /> Per informazioni sul campo **Periodo di stabilizzazione**, vedere [Mostra dettagli di pianificazione: Parametri di pianificazione](design-details-planning-parameters.md).|  
|Includi giacenze|Selezionare sempre quando si sta utilizzando il metodo di riordino lotto-per-lotto.|Non selezionare solo in circostanze particolari, come, ad esempio, quando gli articoli in magazzino non sono vendibili.|  
|Lead time di sicurezza|Impostare un valore compreso tra 1D e 6D.<br /><br /> Impostare un lead time di sicurezza di almeno un giorno per assicurarsi che i rifornimenti siano disponibili il giorno precedente alla richiesta.<br /><br /> Se si utilizza un nuovo fornitore, definire un tempo maggiore finché non sono note le prestazioni di consegna.<br /><br /> Nella produzione definire lead time di sicurezza più lunghi per componenti critici.|L'approvvigionamento pianificato dal sistema per evitare l'esaurimento delle scorte arriverà lo stesso giorno in cui si verifica l'esaurimento delle scorte. Potrebbe risultare in ritardo di alcune ore se, ad esempio, la domanda è richiesta di mattina e l'approvvigionamento arriva nel pomeriggio. **Nota:** Il campo **Lead time di sicurezza** utilizza il calendario di base. Pertanto, 14D non significa necessariamente due settimane.|  
|Scorta di sicurezza|Utilizzare per gli articoli con grandi fluttuazioni della domanda.<br /><br /> Nella produzione utilizzare per i componenti critici.<br /><br /> Utilizzare gli articoli che sono soggetti ai contratti di assistenza.|Se il campo **Punto riordino** non è compilato, la scorta di sicurezza funziona anche come punto di riordino.|  
|Periodo di accumulo lotti|Se si desiderano soltanto pochi ordini di grandi dimensioni e si accetta di conservare il magazzino, impostare un lungo periodo di accumulo lotti.<br /><br /> Se si desiderano più ordini do minori dimensioni e un magazzino minimo, impostare un breve periodo di accumulo lotti.|Il periodo di accumulo lotti corrisponde in genere al periodo più lungo in cui si tiene in giacenza nel magazzino.|  
|Punto riordino|Basare il punto di riordino sul profilo della domanda dell'articolo.|Se i dati storici mostrano che la domanda media dell'articolo è 100 unità durante un lead time di sette giorni, il punto di riordino può essere impostato su 100 come valore minimo.<br /><br /> Ciò significa che quando il livello di magazzino è minore di 100 unità, il sistema di pianificazione suggerirà il rifornimento poiché sono necessari sette giorni per l'approvvigionamento dell'articolo e devono essere presenti articoli sufficienti per soddisfare la domanda in quei sette giorni.|  
|Intervallo di tempo|Lasciare vuoto ovvero il livello di magazzino viene controllato ogni giorno.|Il controllo quotidiano del livello di magazzino garantisce la pianificazione ottimale del punto di riordino. **Nota:**  Un intervallo di tempo di 1S significa che il livello di magazzino può essere inferiore al punto di riordino per una settimana prima che venga suggerito un ordine di approvvigionamento.|  
|Precisione arrotondamento|In una produzione costosa, impostare su 0.00001.|Grandi quantità di arrotondamento di scarto o di consumo dei materiali possono totalizzare costi di magazzino molto elevati. Può quindi essere importante impostare una precisione di arrotondamento inferiore per ridurre questo costo potenziale.|  

> [!NOTE]  
> Le procedure consigliate per i parametri di pianificazione nelle schede articolo si applicano anche agli stessi campi nelle schede USK.  
>
> Se le società pianificano la domanda in ubicazioni diverse, è consigliabile definire le unità di stockkeeping per ogni ubicazione e che tutta la domanda venga creata utilizzando un valore nel campo **Cod. ubicazione**. Per ulteriori informazioni, vedi [Dettagli di progettazione: Pianificazione con o senza ubicazioni](production-planning-with-without-locations.md).  

## Vedere anche  
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)  
[Impostare aree di applicazione complesse utilizzando le procedure ottimali](set-up-complex-application-areas-using-best-practices.md)  
[Dettagli di progettazione: Pianificazione con o senza ubicazioni](production-planning-with-without-locations.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
