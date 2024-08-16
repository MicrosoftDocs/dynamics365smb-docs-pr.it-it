---
title: 'Dettagli di progettazione: prenotazione, monitoraggio degli ordini e messaggistica di azione | Microsoft Docs'
description: Il sistema di prenotazione è completo e comprende le funzionalità correlate e parallele di monitoraggio degli ordini e messaggistica di azione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 08/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="design-details-reservation-order-tracking-and-action-messaging"></a>Dettagli di progettazione: impegno, tracciabilità ordini e messaggistica di azioni

Il sistema di prenotazione completo include le funzionalità interconnesse e parallele di monitoraggio degli ordini e messaggistica di azione.  

Il fulcro del sistema di prenotazione è il collegamento tra una voce di domanda e una voce di offerta corrispondente, tramite prenotazione o tracciamento degli ordini. Un impegno è un collegamento generato dall'utente e un altro record di tracciabilità ordini è un collegamento generato dal sistema. La quantità di un articolo immessa nel sistema di prenotazione viene prenotata o tracciata come ordine, ma non entrambe le cose contemporaneamente. Il modo in cui i sistemi gestiscono un articolo dipende da come è impostato l'articolo stesso.  

Il sistema di impegno interagisce con il sistema di pianificazione creando messaggi di azione nelle righe di pianificazione durante l'esecuzione della pianificazione. Un messaggio di azione può essere considerato un annesso a un record di tracciabilità ordini. I messaggi di azione, se sono creati dinamicamente nella tracciabilità ordini oppure durante l'esecuzione della pianificazione, forniscono uno strumento conveniente per un'efficiente pianificazione dell'approvvigionamento.  

> [!NOTE]  
> Le quantità impegnate vengono ignorate dal sistema di pianificazione, ovvero, il collegamento imposto creato tra approvvigionamento e domanda non può essere modificato tramite la pianificazione.  

 Il sistema di impegno costituisce anche la base strutturale del sistema di tracciabilità articolo. Per maggiori informazioni, vai a [Dettagli di progettazione: Monitoraggio articolo](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## <a name="reservation"></a>Impegno

 Un impegno è collegamento confermato che connette tra loro una domanda specifica e un'offerta specifica. Questo collegamento influisce direttamente sulla transazione di magazzino successiva e garantisce il collegamento appropriato dei movimenti articoli a scopo di costing. Un impegno sostituisce il metodo di costing predefinito di un articolo. Per maggiori informazioni, vai a [Dettagli di progettazione: Monitoraggio articolo](design-details-item-tracking.md).  

 La pagina  **Prenotazione** è accessibile da tutte le righe d'ordine, sia di tipo domanda che di tipo offerta. In questa pagina, l'utente può specificare per quale voce di domanda o di offerta creare una prenotazione collegare. L'impegno è costituito da una coppia di record che condividono lo stesso numero di movimento. Un record ha un segno negativo e punta alla domanda. L'altro record ha un segno positivo e punta all'approvvigionamento. Questi record vengono memorizzati nella tabella *Inserimento prenotazione* con il valore di stato *Prenotazione*. L'utente può visualizzare tutti gli impegni nella pagina **Mov. impegni**.  

### <a name="offsetting-in-reservations"></a>Compensazione negli impegni

 Gli impegni vengono creati rispetto alle quantità di articolo disponibili. La disponibilità articolo viene calcolata fondamentalmente come segue:  

 `available quantity = inventory + scheduled receipts - gross requirements`

 Nella seguente tabella vengono mostrati i dettagli delle entità di rete di ordini che fanno parte del calcolo della disponibilità.  

||Campo nell'elemento T27|Tabella di origine|Filtro tabella|Campo di origine|  
|-|------------------|------------------|------------------|------------------|  
|**Magazzino**|Inventario|Mov. Contabile Articoli|N/D|Quantità|  
|**Carichi programmati**|Carico ordine confermato (qtà)|Righe ordini prod.|=Confermato|Qtà residua (base)|  
|**Carichi programmati**|Carico ordine rilasc. (qtà)|Righe ordini prod.|=Rilasciato|Qtà residua (base)|  
|**Carichi programmati**|Qtà nell'ordine di assemblaggio|Testata assemblaggio|=Ordine|Qtà residua (base)|  
|**Carichi programmati**|Qtà nell'ordine acquisto|Righe Acquisto|=Ordine|Qtà inevasa (base)|  
|**Carichi programmati**|Carico ord. trasf. (qtà)|Riga trasferimento|N/D|Quantità inevasa|  
|**Fabbisogni Lordi**|Qtà nell'ordine vendita|Righe vendite|=Ordine|Qtà inevasa (base)|  
|**Fabbisogni Lordi**|Fabbisogni programmati (qtà)|Componenti ordini produzione|<>Simulato|Qtà residua (base)|  
|**Fabbisogni Lordi**|Qtà nel componente di assemblaggio|Riga assemblaggio|=Ordine|Qtà residua (base)|  
|**Fabbisogni Lordi**|Spedizione ord. trasf. (qtà)|Riga trasferimento|N/D|Quantità inevasa|  

 Per maggiori informazioni, consultare [Dettagli di progettazione: Disponibilità in magazzino](design-details-availability-in-the-warehouse.md).  

### <a name="manual-reservation"></a>Impegno manuale

Quando un utente crea intenzionalmente un impegno, l'utente guadagna la piena proprietà e la responsabilità di tali articoli. Ciò significa che l'utente deve anche modificare o annullare un impegno manualmente. Tali modifiche manuali potrebbero causare la modifica automatica delle prenotazioni interessate.  

La tabella seguente mostra quando e quali modifiche potrebbero verificarsi:  

|Azione utente|Risposta del sistema|  
|-----------------|---------------------|  
|Riduzione della quantità impegnata|I campi di quantità correlati vengono aggiornati.|  
|Modifica dei campi di date|I campi di data correlati vengono aggiornati.<br /><br /> **Nota:** Se la data di scadenza in una domanda viene modificata per precedere la data di spedizione o la data di scadenza dell'approvvigionamento, l'impegno verrà annullato.|  
|Eliminazione dell'ordine|L'impegno viene annullato.|  
|Modificare l'ubicazione, la collocazione, la variante, il numero seriale o di lotto|L'impegno viene annullato.|  

> [!NOTE]  
> La funzionalità di combinazione tardiva può inoltre modificare gli impegni senza informare l'utente, ridistribuendo gli impegni non specifici dei numeri seriali o di lotto. Per maggiori informazioni, vai a [Dettagli di progettazione: monitoraggio e prenotazioni degli articoli](design-details-item-tracking-and-reservations.md).  

### <a name="automatic-reservations"></a>Impegni automatici

L'elemento scheda può essere impostato per riservare automaticamente gli articoli in base alla domanda, ad esempio gli ordini di vendita. In quel caso, l'impegno viene creato in funzione del magazzino, degli ordini di acquisto, degli ordini di assemblaggio e di produzione. Se la fornitura è insufficiente, viene emesso un avviso.  

Inoltre, diverse funzioni di pianificazione riservano automaticamente gli articoli per mantenere una domanda collegata a una fornitura specifica. Le voci di tracciamento degli ordini per tali collegamenti di pianificazione contengono **Prenotazione** nel campo **Stato prenotazione** nella tabella *Voce prenotazione* . Gli impegni automatici vengono creati nei seguenti casi:  

- Un ordine di produzione multilivello nel campo **Politica di produzione** degli articoli padre e figlio interessati è impostato su **Prod. su Ordine**. Il sistema di pianificazione crea delle prenotazioni tra l'ordine di produzione padre e l'ordine di produzione sottostante per garantire che vengano elaborati insieme. Questo vincolo di prenotazione sostituisce il metodo di applicazione e di determinazione dei costi predefinito dell'articolo.  

- Una produzione, un assemblaggio o un ordine di acquisto in cui il campo **Metodo di riordino** dell'articolo interessato è impostato su **Ordine**. Il sistema di pianificazione crea gli impegni tra domanda e approvvigionamento pianificato per garantire la creazione dello specifico approvvigionamento. Per maggiori informazioni, vai su [Ordina](design-details-handling-reordering-policies.md#order).  

- Un ordine di produzione creato da un ordine di vendita con la funzione **Pianifica ordine vendita** viene collegato all'ordine di vendita con un impegno automatico.  

- Un ordine di assemblaggio creato automaticamente per una riga di ordine di vendita per soddisfare la quantità nel campo  **Qtà da assemblare su ordine** . Tale impegno automatico collega la domanda di vendita e l'approvvigionamento di assemblaggio in modo che i gestori ordini di vendita possano personalizzare e promettere direttamente l'articolo di assemblaggio al cliente. Inoltre, l'impegno collega l'output di assemblaggio alla riga ordine di vendita attraverso l'attività di spedizione che soddisfa l'ordine del cliente.  

Per l'offerta o la domanda non assegnate, il sistema di pianificazione assegna automaticamente lo stato di prenotazione **Surplus**. Ciò può risultare dalla domanda dovuta a quantità previste o a parametri di pianificazione immessi dall'utente. Si tratta di un surplus legittimo, riconosciuto dal sistema, che non dà origine a messaggi di azione. Il surplus potrebbe anche essere reale, un eccesso di domanda o di offerta che non viene monitorato. Ciò indica uno squilibrio nella rete di ordini, che causa l'emissione di messaggi di azione da parte del sistema. Notare che un messaggio di azione che suggerisce una modifica della quantità fa sempre riferimento al tipo **Surplus**. Per ulteriori informazioni, consultare la sezione  [Esempio: monitoraggio degli ordini in Vendite, Produzione e Trasferimenti](#example-order-tracking-in-sales-production-and-transfers) di questo articolo.  

Le prenotazioni automatiche create durante l'esecuzione pianificata vengono gestite nei seguenti modi:  

- Si applicano alle quantità degli articoli incluse nel calcolo della disponibilità, proprio come le prenotazioni manuali. Per ulteriori informazioni, consultare la sezione "Compensazione nelle prenotazioni" di questo articolo.  

- A differenza degli elementi prenotati manualmente, vengono inclusi e potenzialmente modificati nelle successive pianificazioni.  

## <a name="order-tracking"></a>Tracciabilità ordini

La tracciabilità ordini aiuta il responsabile della pianificazione a gestire un piano di approvvigionamento valido fornendo una sintesi della compensazione tra approvvigionamento e domanda nella rete di ordini. I record di tracciabilità ordini servono da base per la creazione di messaggi di azione dinamici e di suggerimenti per la riga di pianificazione durante l'esecuzione della pianificazione.  

> [!NOTE]  
> Il sistema di tracciabilità ordini compensa le scorte disponibili man mano che gli ordini vengono immessi nella rete di ordini. Questo implica che il sistema non assegna priorità agli ordini che potrebbero essere più urgenti in termini di data di scadenza. Spetta quindi alla logica del sistema di pianificazione o alla saggezza di chi pianifica riordinare le priorità in modo significativo.  

> [!NOTE]  
> La politica di tracciamento degli ordini e la funzione Ottieni messaggi di azione non sono integrate con Projects. Ne consegue che la domanda correlata a un progetto non viene tracciata automaticamente. Poiché non c'è tracciabilità, è possibile che l'utilizzo di un rifornimento esistente con le informazioni sul progetto venga tracciato in un'altra domanda, ad esempio, un ordine di vendita. Di conseguenza, potresti trovarti in una situazione in cui le informazioni relative all'inventario disponibile non sono sincronizzate.  

### <a name="the-order-network"></a>Rete di ordini

Il sistema di tracciamento degli ordini si basa sul principio secondo cui la rete degli ordini deve sempre rimanere in equilibrio, garantendo che ogni domanda che entra nel sistema venga compensata da una corrispondente offerta e viceversa. Ciò avviene tramite l'identificazione di collegamenti logici tra tutti i movimenti di domanda e di approvvigionamento nella rete di ordini.  

Il principio implica che un cambiamento nella domanda determina uno squilibrio corrispondente sul lato approvvigionamento della rete di ordini. Viceversa, una modifica nei risultati dell'approvvigionamento determina uno squilibrio corrispondente sul lato della domanda della rete di ordini. In realtà, la rete di ordini è in uno stato di cambiamento continuo in quanto gli utenti immettono, modificano ed eliminano ordini. La tracciabilità ordini elabora gli ordini in modo dinamico, rispondendo ad ogni variazione nel momento in cui viene immessa nel sistema e diventa parte della rete di ordini. Non appena vengono creati i nuovi record di tracciabilità ordini, la rete di ordini è in saldo, ma solo finché non si verifica la modifica successiva.  

Per aumentare la trasparenza dei calcoli nel sistema di pianificazione, la pagina **Elementi di pianificazione non tracciati** visualizza le quantità non tracciate, che rappresentano la differenza in quantità tra la domanda conosciuta e l'approvvigionamento suggerito. Ogni riga della pagina si riferisce alla causa della quantità eccedente, ad esempio **Ordine programmato**, **Livello della scorta di sicurezza**, **Quantità di riordino fissa**, **Quantità minima ordine**, **Arrotondamento** o **Smorzamento**.  

### <a name="offsetting-in-order-tracking"></a>Compensazione nella tracciabilità ordini

A differenza degli impegni, che possono essere creati solo a fronte di quantità articolo disponibili, è possibile utilizzare la tracciabilità ordini a fronte di tutte le altre entità della rete di ordini che fanno parte del calcolo dei fabbisogni del sistema di pianificazione. I fabbisogni netti vengono calcolati come segue:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> La domanda correlata ai parametri di previsione o di pianificazione non viene tracciata dall'ordine.  

### <a name="example-order-tracking-in-sales-production-and-transfers"></a>Esempio: tracciabilità ordini in vendite, produzione e trasferimenti

Lo scenario seguente mostra quali voci di tracciamento degli ordini vengono create nella tabella  *Voci di prenotazione* come risultato di varie modifiche alla rete degli ordini.  

Presupporre che i seguenti dati per due articoli siano impostati per la tracciabilità ordini.  

|Elemento|Parametro|Dettaglio|
|-|-|-|
|Articolo 1|Nome|Componente|
||Disponibilità|100 unità in posizione EST<br /><br />- 30 unità di LOTA<br />- 70 unità di LOTB|  
|Articolo 2|Nome|Articolo prodotto|
||DB produzione|1 q.tà per componente|  
||Domanda|Vendita per 100 unità in posizione WEST|  
||Approvvigionamento|Ordine di produzione rilasciato (generato con la funzione  *Pianificazione ordini di vendita* per la vendita di 100 unità)|  

Nella pagina **Impostazione produzione**, il campo **Componenti nella posizione** è impostato su *EST*.

Nella tabella  *Voce di prenotazione* sono presenti le seguenti voci di tracciamento degli ordini in base ai dati nella tabella.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Voci di prenotazione**

|Nr. movimento|Positivo|Nr. articolo|Codice ubicazione|Quantità|Stato impegno|Descrizione|Nr. lotto|Tipo di origine|ID origine|Vincolato|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|COMPONENTE|EST|-70|Tracciabilità|Componente|-|5407|101004|-|
|8|Sì|COMPONENTE|EST|70|Tracciabilità|Componente|LOTB|32|-|-| 
|9|-|COMPONENTE|EST|-30|Tracciabilità|Componente|-|5407|1001004|-| 
|9|Sì|COMPONENTE|EST|30|Tracciabilità|Componente|Lotta|32|-|-| 
|10|-|ARTICOLO PRODOTTO|OVEST|-100|Impegno|Articolo prodotto|-|37|1001|Ordine-a-ordine|
|10|Sì|ARTICOLO PRODOTTO|OVEST|100|Impegno|Articolo prodotto|-|5406|101004|Ordine-a-ordine|


#### <a name="entry-numbers-8-and-9"></a>Numeri di movimento 8 e 9

Per la necessità di componenti rispettivamente per LOTA e LOTB, vengono creati collegamenti di tracciamento degli ordini dalla domanda nella tabella 5407, *Componente ordine di produzione*, alla fornitura nella tabella 32, *Voce contabile articolo*. Il campo  **Stato prenotazione** contiene *Tracciamento* per indicare che queste voci sono collegamenti di tracciamento dinamico degli ordini tra domanda e offerta.  

> [!NOTE]  
> Il campo  **Numero lotto**  è vuoto nelle righe di domanda perché i numeri di lotto non sono specificati nelle righe dei componenti dell'ordine di produzione rilasciato.  

#### <a name="entry-number-10"></a>Numero di movimento 10

Dalla domanda di vendita nella tabella 37, *Linee di vendita*, viene creato un tracciamento dell'ordine collegare per la fornitura nella tabella 5406, *Riga ordine produzione*. IL **Stato della prenotazione**  il campo contiene *Prenotazione*, e il **Legame**  il campo contiene *Ordine su ordine*. Ciò avviene perché l'ordine di produzione rilasciato è stato generato specificatamente per l'ordine di vendita e deve rimanere collegato, a differenza dei collegamenti di tracciamento degli ordini con stato di prenotazione Tracciamento, che vengono creati e modificati dinamicamente. Per maggiori informazioni, vai al [Prenotazioni automatiche](#automatic-reservations)  sezione di questo articolo.  

 In questo puntare nello scenario, le 100 unità di LOTA e LOTB vengono trasferite nella posizione WEST tramite un ordine di trasferimento.  

> [!NOTE]  
> Solo la spedizione dell'ordine di trasferimento viene registrata in questa fase, non il carico.  

 Ora sono presenti le seguenti voci di tracciamento degli ordini nel *Inserimento prenotazione*  tavolo.  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Voci di prenotazione**

|Nr. movimento|Positivo|Nr. articolo|Codice ubicazione|Quantità|Stato impegno|Descrizione|Nr. lotto|Tipo di origine|ID origine|Vincolato|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|COMPONENTE|EST|-30|Surplus|Componente|-|5407|1001004|-| 
|10|-|ARTICOLO PRODOTTO|OVEST|-100|Impegno|Articolo prodotto|-|37|1001|Ordine-a-ordine|
|10|Sì|ARTICOLO PRODOTTO|OVEST|100|Impegno|Articolo prodotto|-|5406|101004|Ordine-a-ordine|
|12|Sì|COMPONENTE|OVEST|70|Surplus|Componente|LOTB|5741|1011|-| 
|14|Sì|COMPONENTE|OVEST|30|Surplus|Componente|Lotta|5741|1011|-| 
|15|Sì|COMPONENTE|REGISTRO FUORI.|70|Surplus|Componente|LOTB|32|-|-| 
|16|Sì|COMPONENTE|REGISTRO FUORI.|30|Surplus|Componente|Lotta|32|-|-| 

#### <a name="entry-numbers-8-and-9-1"></a>Numeri di movimento 8 e 9

Le voci di tracciamento degli ordini per i due lotti del componente che riflettono la domanda nella tabella 5407 vengono modificate da uno stato di prenotazione di *Tracciamento* a *Surplus*. Il motivo è che le forniture collegate in precedenza, nella tabella 32, vengono utilizzate dalla spedizione dell'ordine di trasferimento.  

Il surplus genuino, come n questo caso, riflette un approvvigionamento o una domanda effettiva eccedente che non viene tracciata. È un'indicazione di uno squilibrio nella rete degli ordini che, a meno che non venga risolto dinamicamente, genera un messaggio di azione da parte del sistema di pianificazione.  

#### <a name="entry-numbers-12-to-16"></a>Numeri di movimento da 12 a 16

Poiché i due lotti del componente vengono registrati nell'ordine di trasferimento come spediti ma non ricevuti, tutte le voci di tracciamento ordine positive correlate sono di tipo prenotazione *Surplus*, a indicare che non sono assegnate ad alcuna domanda. Per ogni numero di lotto, una voce si riferisce alla tabella 5741,  *Riga di trasferimento*, e una voce si riferisce alla registrazione contabile dell'articolo nella posizione di transito in cui si trovano ora gli articoli.  

In questo puntare nello scenario, l'ordine di trasferimento dei componenti dalla posizione  *EST* a  *OVEST*  viene registrato come ricevuto.  

Ora sono presenti le seguenti voci di tracciamento degli ordini nel *Inserimento prenotazione*  tavolo.  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Voci di prenotazione**

|Nr. movimento|Positivo|Nr. articolo|Codice ubicazione|Quantità|Stato impegno|Descrizione|Nr. lotto|Tipo di origine|ID origine|Vincolato|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|COMPONENTE|EST|-70|Surplus|Componente|-|5407|101004|-| 
|9|-|COMPONENTE|EST|-30|Surplus|Componente|-|5407|1001004|-|
|10|-|ARTICOLO PRODOTTO|OVEST|-100|Impegno|Articolo prodotto|-|37|1001|Ordine-a-ordine|
|10|Sì|ARTICOLO PRODOTTO|OVEST|100|Impegno|Articolo prodotto|-|5406|101004|Ordine-a-ordine|
|17|Sì|COMPONENTE|OVEST|70|Surplus|Componente|LOTB|32|-|-| 
|18|Sì|COMPONENTE|OVEST|30|Surplus|Componente|Lotta|32|-|-| 

Le voci di tracciamento degli ordini sono ora simili al primo puntare nello scenario prima che l'ordine di trasferimento venisse registrato come solo spedito, ad eccezione delle voci per il componente che ora hanno lo stato di prenotazione *Surplus*. Ciò accade perché il componente necessario è ancora in posizione  *EAST*, il che riflette il fatto che il campo  **Codice posizione** nella riga del componente dell'ordine di produzione contiene  *EAST* come impostato nel campo  **Componenti in posizione** . La fornitura che in precedenza era stata assegnata a questa domanda è stata trasferita alla posizione  *WEST*  e non può essere completamente tracciata a meno che la necessità del componente sulla riga dell'ordine di produzione non venga modificata nella posizione  *WEST* .  

In questo puntare nello scenario, il **codice ubicazione** sulla riga del componente dell'ordine di produzione è impostato su *WEST*. Inoltre, nella pagina  **Righe di tracciamento articolo**, le 30 unità di LOTA e le 70 unità di LOTB vengono assegnate alla riga del componente dell'ordine di produzione.  

Ora sono presenti le seguenti voci di tracciamento degli ordini nel *Inserimento prenotazione*  tavolo.  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Voci di prenotazione**

|Nr. movimento|Positivo|Nr. articolo|Codice ubicazione|Quantità|Stato impegno|Descrizione|Nr. lotto|Tipo di origine|ID origine|Vincolato|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|ARTICOLO PRODOTTO|OVEST|-100|Impegno|Articolo prodotto|-|37|1001|Ordine-a-ordine|
|10|Sì|ARTICOLO PRODOTTO|OVEST|100|Impegno|Articolo prodotto|-|5406|101004|Ordine-a-ordine|
|21|-|COMPONENTE|OVEST|-70|Tracciabilità|Componente|LOTB|5407|101004|-| 
|21|Sì|COMPONENTE|OVEST|70|Tracciabilità|Componente|LOTB|32|-|-| 
|22|-|COMPONENTE|OVEST|-30|Tracciabilità|Componente|Lotta|5407|1001004|-| 
|22|Sì|COMPONENTE|OVEST|30|Tracciabilità|Componente|Lotta|32|-|-| 

#### <a name="entry-numbers-21-and-22"></a>Numeri di movimento 21 e 22

Poiché il componente deve essere modificato in posizione  *WEST* e la fornitura è disponibile come voci del registro articoli in posizione  *WEST*, tutte le voci di tracciamento degli ordini per i due numeri di lotto sono ora completamente tracciate, come indicato dallo stato di prenotazione di  *Tracciamento*.  

Il campo  **Numero lotto**  è ora compilato nella voce di tracciamento ordine per la tabella 5407 perché i numeri di lotto sono stati assegnati alle righe dei componenti dell'ordine di produzione.  

## <a name="action-messaging"></a>Messaggistica di azione

Quando il sistema di tracciabilità ordini rileva uno sbilanciamento nella rete di ordini, crea automaticamente un messaggio di azione per informare l'utente. I messaggi di azione sono chiamate generate dal sistema per l'azione dell'utente che specificano i dettagli dello squilibrio e suggerimenti su come ripristinare l'equilibrio nella rete degli ordini. Vengono visualizzati come linee di pianificazione nella pagina  **Fogli di lavoro di pianificazione** quando si sceglie l'azione  **Ottieni messaggi di azione** . Inoltre, durante l'esecuzione della pianificazione vengono generati messaggi di azione sulle linee di pianificazione per riflettere i suggerimenti del sistema di pianificazione per ripristinare l'equilibrio nella rete degli ordini. In entrambi i casi, i suggerimenti vengono eseguiti sulla rete degli ordini, quando si sceglie l'azione  **Esegui messaggio di azione** .  

Un messaggio di azione indirizza un livello della DB alla volta. Se l'utente accetta il messaggio di azione, ciò potrebbe dare origine a ulteriori messaggi di azione al livello BOM successivo.  

Nella seguente tabella vengono mostrati i messaggi di azione esistenti.  

|Messaggio azione|Description|  
|--------------------|---------------------------------------|  
|**Cambia Qtà**|Modifica la quantità in un ordine di approvvigionamento esistente per coprire una domanda modificata o nuova.|  
|**Ripianifica**|Ripianifica la data di scadenza di un ordine esistente.|  
|**Riprogr. e mod. qtà**|Ripianifica la data di scadenza e modifica la quantità di un ordine esistente.|  
|**Nuova**|Crea un nuovo ordine se la domanda non può essere soddisfatta tramite nessuno dei messaggi di azione precedenti.|  
|**Annulla**|Annulla un ordine esistente.|  

Il sistema di tracciabilità ordini tenta sempre di risolvere un eventuale sbilanciamento nella rete di ordini esistente. Se ciò non è possibile, viene inviato un messaggio di azione per creare un nuovo ordine. Viene di seguito riportato l'elenco con priorità che il sistema di tracciamento dell'ordine utilizza quando determina come ripristinare il saldo. Se una domanda aggiuntiva entra nella rete degli ordini, il sistema cerca di tracciare l'ordine attraverso i seguenti controlli:  

1. Controllare un approvvigionamento eccedente nel record di tracciabilità ordini esistente per questa domanda.  
1. Controllo dei carichi pianificati e programmati ordinate in base alla data di carico. La data più recente possibile è selezionata.  
1. Controllo delle scorte disponibili.  
1. Controllo dell'esistenza di un ordine di approvvigionamento nel record corrente di tracciabilità ordini. In tal caso, il sistema emette un messaggio di azione di tipo  *Modifica* per aumentare l'ordine.  
1. Controllare che non esista alcun ordine di approvvigionamento nel record corrente di tracciabilità ordini. In tal caso, il sistema emette un messaggio di azione di tipo *Nuovo* per creare un nuovo ordine.  

Una domanda aperta attraversa l'elenco e compensa l'approvvigionamento disponibile a ciascun passaggio. Tutte le domande residue vengono sempre coperte dal controllo 4 oppure 5.  

Se si verifica una diminuzione della quantità di domanda, il sistema di tracciabilità ordini cerca di risolvere lo squilibrio eseguendo i controlli precedenti in ordine inverso. Ciò significa che i messaggi di azione esistenti potrebbero essere modificati o persino eliminati, se necessario. Il sistema di tracciabilità ordini presenta sempre il risultato netto dei calcoli all'utente.  

## <a name="order-tracking-and-planning"></a>Tracciabilità e pianificazione ordini

Quando il sistema di pianificazione viene eseguito, elimina tutti i record di tracciabilità ordini e i movimenti di messaggi di azione esistenti e li ricrea come suggerimenti della riga di pianificazione in base alle coppie e alle priorità di approvvigionamento e domanda. Una volta completata l'esecuzione della pianificazione, la rete degli ordini è in equilibrio.  

### <a name="planning-system-versus-order-tracking-and-action-messaging"></a>Sistema di pianificazione rispetto a tracciabilità ordini e messaggistica di azioni

 Nel seguente confronto vengono mostrate le differenze tra i metodi utilizzati dal sistema di pianificazione per creare suggerimenti per una riga di pianificazione e i metodi utilizzati dal sistema di tracciabilità ordini per creare i record di tracciabilità ordini e i messaggi di azione.  

- Il sistema di pianificazione si occupa dell'intero modello di approvvigionamento e domanda di un determinato articolo, mentre la tracciabilità ordini si occupa dell'ordine che l'ha attivata.  

- Il sistema di pianificazione si occupa di tutti i livelli della gerarchia della DB, mentre la tracciabilità ordini si occupa di un livello della DB per volta.  

- Il sistema di pianificazione stabilisce collegamenti tra approvvigionamento e domanda in base alla data di scadenza alla quale è assegnata la priorità. La tracciabilità ordini stabilisce collegamenti tra approvvigionamento e domanda in base alla sequenza di immissione degli ordini.  

- Il sistema di pianificazione tiene conto dei parametri di pianificazione, mentre il monitoraggio degli ordini no.  

- Il sistema di pianificazione crea i collegamenti in una modalità batch attivata dall'utente quando bilancia domanda e approvvigionamento, mentre la tracciabilità ordini crea i collegamenti automaticamente e in modo dinamico quando l'utente immette gli ordini.  

## <a name="see-also"></a>Vedere anche

[Dettagli di progettazione: concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
