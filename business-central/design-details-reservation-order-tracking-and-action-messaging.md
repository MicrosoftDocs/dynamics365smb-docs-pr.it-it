---
title: 'Dettagli di progettazione: Impegno, tracciabilità dell''ordine e messaggistica di azioni | Microsoft Docs'
description: Il sistema di impegno è completo e include funzionalità correlate e parallele di tracciabilità ordine e di messaggistica di azione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni
Il sistema di impegno è completo e include funzionalità correlate e parallele di tracciabilità ordine e di messaggistica di azione.  

 Al centro del sistema di impegno c'è il collegamento di un movimento di domanda e di un movimento di approvvigionamento corrispondente, tramite un impegno o la tracciabilità ordini. Un impegno è un collegamento generato dall'utente e un altro record di tracciabilità è un collegamento generato dal sistema. Una quantità dell'articolo immesso nel sistema di impegno è impegnato o l'ordine tracciato, ma non entrambi contemporaneamente. Come i sistemi gestiscono un articolo dipende da come è impostato l'articolo.  

 Il sistema di impegno interagisce con il sistema di pianificazione creando messaggi di azione nelle righe di pianificazione durante l'esecuzione della pianificazione. Un messaggio di azione può essere considerato un annesso a un record di tracciabilità ordini. I messaggi di azione, se sono creati dinamicamente nella tracciabilità ordini oppure durante l'esecuzione della pianificazione, forniscono uno strumento conveniente per un'efficiente pianificazione dell'approvvigionamento.  

> [!NOTE]  
>  Le quantità impegnate vengono ignorate dal sistema di pianificazione, ovvero, il collegamento imposto creato tra approvvigionamento e domanda non può essere modificato tramite la pianificazione.  

 Il sistema di impegno costituisce anche la base strutturale del sistema di tracciabilità articolo. Per ulteriori informazioni, vedere [Dettagli del nuovo ciclo: Tracciabilità articolo](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Impegno  
 Un impegno è collegamento confermato che connette tra loro una domanda specifica e un'offerta specifica. Questo collegamento influisce direttamente sulla transazione di magazzino successiva e garantisce il collegamento appropriato dei movimenti articoli a scopo di costing. Un impegno sostituisce il metodo di costing predefinito di un articolo. Per ulteriori informazioni, vedere [Dettagli del nuovo ciclo: Tracciabilità articolo](design-details-item-tracking.md).  

 È possibile accedere alla pagina **Impegno** da tutte le righe ordine della domanda e dell'approvvigionamento. In questa pagina l'utente può specificare per quale movimento di domanda o di approvvigionamento creare un collegamento di impegno. L'impegno è costituito da una coppia di record che condividono lo stesso numero di movimento. Un record ha un segno negativo e punta alla domanda. L'altro record ha un segno positivo e punta all'approvvigionamento. Questi record sono memorizzati nella tabella **Movimenti impegni** con valore di stato **Impegno**. L'utente può visualizzare tutti gli impegni nella pagina **Mov. impegni**.  

### Compensazione negli impegni  
 Gli impegni vengono creati rispetto alle quantità di articolo disponibili. La disponibilità articolo viene calcolata fondamentalmente come segue:  

 quantità disponibile = magazzino + carichi pianificati - fabbisogno lordo  

 Nella seguente tabella vengono mostrati i dettagli delle entità di rete di ordini che fanno parte del calcolo della disponibilità.  

||Campo in T27|Tabella di origine|Filtro tabella|Campo di origine|  
|-|------------------|------------------|------------------|------------------|  
|**Magazzino**|Magazzino|Mov. Contabile Articoli|N/D|Quantità|  
|**Carichi programmati**|Carico ordine confermato (qtà)|Righe ordini prod.|=Confermato|Qtà residua (base)|  
|**Carichi programmati**|Carico ordine rilasc. (qtà)|Righe ordini prod.|=Rilasciato|Qtà residua (base)|  
|**Carichi programmati**|Qtà nell'ordine di assemblaggio|Testata assemblaggio|=Ordine|Qtà residua (base)|  
|**Carichi programmati**|Qtà nell'ordine acquisto|Righe Acquisto|=Ordine|Qtà inevasa (base)|  
|**Carichi programmati**|Carico ord. trasf. (qtà)|Riga trasferimento|N/D|Quantità inevasa|  
|**Fabbisogni Lordi**|Qtà nell'ordine vendita|Righe vendite|=Ordine|Qtà inevasa (base)|  
|**Fabbisogni Lordi**|Fabbisogni programmati (qtà)|Componenti ordini produzione|<>Simulato|Qtà residua (base)|  
|**Fabbisogni Lordi**|Qtà nel componente di assemblaggio|Riga assemblaggio|=Ordine|Qtà residua (base)|  
|**Fabbisogni Lordi**|Spedizione ord. trasf. (qtà)|Riga trasferimento|N/D|Quantità inevasa|  

 Per ulteriori informazioni, vedere [Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md).  

### Prenotazione manuale  
 Quando un utente crea intenzionalmente un impegno, l'utente guadagna la piena proprietà e la responsabilità di tali articoli. Ciò significa che l'utente deve anche modificare o annullare un impegno manualmente. Tali modifiche manuali possono causare la modifica automatica degli impegni interessati.  

 Nella seguente tabella viene indicato quali cambiamenti si verificano e quando:  

|Azione utente|Risposta del sistema|  
|-----------------|---------------------|  
|Riduzione della quantità impegnata|I campi di quantità correlati vengono aggiornati.|  
|Modifica dei campi di date|I campi di data correlati vengono aggiornati.<br /><br /> **Nota:** Se la data di scadenza in una domanda viene modificata per precedere la data di spedizione o la data di scadenza dell'approvvigionamento, l'impegno verrà annullato.|  
|Eliminazione dell'ordine|L'impegno viene annullato.|  
|Modificare l'ubicazione, la collocazione, la variante, il numero seriale o di lotto|L'impegno viene annullato.|  

> [!NOTE]  
>  La funzionalità di combinazione tardiva può inoltre modificare gli impegni senza informare l'utente, ridistribuendo gli impegni non specifici dei numeri seriali o di lotto. Per ulteriori informazioni, vedere "Dettagli di progettazione: Tracciabilità articolo e impegni".  

### Prenotazioni automatiche  
 Nella scheda articolo può essere impostata in modo da essere sempre impegnata automaticamente dalla domanda, come gli ordini di vendita. In quel caso, l'impegno viene creato in funzione del magazzino, degli ordini di acquisto, degli ordini di assemblaggio e di produzione. Viene rilasciato un avviso se l'approvvigionamento è insufficiente.  

 Inoltre, gli articoli vengono impegnati automaticamente da varie funzioni di pianificazione per mantenere una domanda collegata a uno specifico approvvigionamento. I movimenti di tracciabilità ordine per tali collegamenti di pianificazione contengono **Impegno** nel campo **Stato impegno** nella tabella **Movimenti impegni**. Gli impegni automatici vengono creati nei seguenti casi:  

-   Un ordine di produzione multilivello nel campo **Politica di produzione** degli articoli padre e figlio interessati è impostato su **Prod. su Ordine**. Il sistema di pianificazione crea degli impegni tra l'ordine di produzione padre e gli ordini di produzione sottostanti per garantire che vengano elaborati insieme. Tale associazione di impegni sostituisce il metodo predefinito di costing e di collegamento dell'articolo.  

-   Una produzione, un assemblaggio o un ordine di acquisto in cui il campo **Metodo di riordino** dell'articolo interessato è impostato su **Ordine**. Il sistema di pianificazione crea gli impegni tra domanda e approvvigionamento pianificato per garantire la creazione dello specifico approvvigionamento. Per ulteriori informazioni, vedere [Ordine](design-details-handling-reordering-policies.md#order).  

-   Un ordine di produzione creato da un ordine di vendita con la funzione **Pianifica ordine vendita** viene collegato all'ordine di vendita con un impegno automatico.  

-   Un ordine di assemblaggio creato automaticamente per una riga ordine vendita per completare la quantità nel campo **($ T_37_900 Qty. to Assemble to Order $)**. Tale impegno automatico collega la domanda di vendita e l'approvvigionamento di assemblaggio in modo che i gestori ordini di vendita possano personalizzare e promettere direttamente l'articolo di assemblaggio al cliente. Inoltre, l'impegno collega l'output di assemblaggio alla riga ordine di vendita attraverso l'attività di spedizione che soddisfa l'ordine del cliente.  

 Nel caso di un approvvigionamento o una domanda che non è allocata, il sistema di pianificazione assegna uno stato di impegno di tipo **Surplus**. Ciò può risultare dalla domanda dovuta a quantità previste o a parametri di pianificazione immessi dall'utente. Si tratta di surplus legittimo, riconosciuto dal sistema, e che non genera messaggi di azione. Il surplus può essere un approvvigionamento o una domanda effettiva eccedente che non viene tracciata. Ciò indica uno squilibrio nella rete di ordini, che causa l'emissione di messaggi di azione da parte del sistema. Notare che un messaggio di azione che suggerisce una modifica della quantità fa sempre riferimento al tipo **Surplus**. Per ulteriori informazioni, vedere la sezione "Esempio: tracciabilità ordini nelle vendita, nella produzione e nei trasferimenti" in questo argomento.  

 Gli impegni automatici creati durante l'esecuzione della pianificazione vengono gestiti nei seguenti modi:  

-   Si applicano a fronte delle quantità di articoli che fanno parte del calcolo della disponibilità, in quanto sono impegni manuali. Per ulteriori informazioni, vedere la sezione "Compensazione negli impegni" in questo argomento.  

-   Vengono inclusi e potenzialmente modificati in esecuzioni successive di pianificazione, a differenza degli articoli impegnati manualmente.  

## Tracciabilità ordine  
 La tracciabilità ordini aiuta il responsabile della pianificazione a gestire un piano di approvvigionamento valido fornendo una sintesi della compensazione tra approvvigionamento e domanda nella rete di ordini. I record di tracciabilità dell'ordine servono da base per la creazione di messaggi di azione dinamici e di suggerimenti per la riga di pianificazione durante l'esecuzione della pianificazione.  

> [!NOTE]  
>  Il sistema di tracciabilità ordine compensa le scorte disponibili man mano che gli ordini vengono immessi nella rete di ordini. Questo implica che il sistema non assegna priorità agli ordini che potrebbero essere più urgenti in termini di data di scadenza. Spetta quindi alla logica del sistema di pianificazione o alla saggezza di chi pianifica riordinare le priorità in modo significativo.  

> [!NOTE]  
>  I criteri di tracciabilità dell'ordine e la funzione Genera messaggi di azione non sono integrati con le Commesse. Ne consegue che la domanda correlata a una commessa non viene tracciata automaticamente. Poiché non viene tenuta traccia, è possibile che l'utilizzo di un rifornimento esistente con le informazioni sulla commessa venga tracciato in un'altra domanda, ad esempio, un ordine di vendita. Di conseguenza, si può verificare la situazione in cui le informazioni relative alla giacenza disponibile non sono sincronizzate.  

### Rete di ordini  
 Il sistema di tracciabilità ordine è basato sul principio che la rete di ordini deve sempre essere a saldo, per cui ogni domanda immessa nel sistema viene compensata da un approvvigionamento corrispondente e viceversa. Ciò avviene tramite l'identificazione di collegamenti logici tra tutti i movimenti di domanda e di approvvigionamento nella rete di ordini.  

 Il principio implica che un cambiamento nella domanda determina uno squilibrio corrispondente sul lato approvvigionamento della rete di ordini. Viceversa, una modifica nei risultati dell'approvvigionamento determina uno squilibrio corrispondente sul lato della domanda della rete di ordini. In realtà, la rete di ordini è in uno stato di cambiamento continuo in quanto gli utenti immettono, modificano ed eliminano ordini. La tracciabilità ordini elabora gli ordini in modo dinamico, rispondendo ad ogni variazione nel momento in cui viene immessa nel sistema e diventa parte della rete di ordini. Non appena vengono creati i nuovi record di tracciabilità, la rete di ordini è in saldo, ma solo finché non si verifica la modifica successiva.  

 Per aumentare la trasparenza dei calcoli nel sistema di pianificazione, la pagina **Elementi di pianificazione non tracciati** visualizza le quantità non tracciate, che rappresentano la differenza in quantità tra la domanda conosciuta e l'approvvigionamento suggerito. Ogni riga della pagina si riferisce alla causa della quantità eccedente, ad esempio **Ordine programmato**, **Livello della scorta di sicurezza**, **Quantità di riordino fissa**, **Quantità minima ordine**, **Arrotondamento** o **Smorzamento**.  

### Compensazione nella tracciabilità ordine  
 A differenza degli impegni, che possono essere creati solo a fronte di quantità articolo disponibili, è possibile utilizzare la tracciabilità ordine a fronte di tutte le altre entità della rete di ordini che fanno parte del calcolo dei fabbisogni del sistema di pianificazione. I fabbisogni netti vengono calcolati come segue:  

 fabbisogno = fabbisogno lordo + punto di riordino - carichi programmati - carichi pianificati - disponibilità calcolata  

> [!NOTE]  
>  La domanda correlata ai parametri di previsione o di pianificazione non viene tracciata dall'ordine.  

### Esempio: Tracciabilità ordine nelle vendite, nella produzione e nei trasferimenti  
 L'esempio seguente mostra quali movimenti di tracciabilità ordine vengono creati nella tabella **Movimenti impegni** come risultato di vari cambiamenti nella rete di ordini.  

 Presupporre che i seguenti dati per due articoli siano impostati per la tracciabilità dell'ordine.  

|Articolo 1|Name|"Componente"|
|-|-|-|
||Disponibilità|100 unità nell'ubicazione OVEST<br /><br />- 30 unità di LOTA<br />- 70 unità di LOTB|  
|Articolo 2|Name|"Articolo prodotto"|
||DB produzione|1 quantità di "Componente"|  
||Domanda|Vendita di 100 unità presso l'ubicazione EST|  
||Approvvigionamento|Ordine di produzione rilasciato (generato mediante la funzione **Pianifica ordine vendita** per la vendita di 100 unità)|  

Nella pagina **Setup manufacturing**, il campo **Componenti nell'ubicazione** è impostato su **ROSSO**.

 I seguenti movimenti di tracciabilità ordini sono disponibili nella tabella **Movimenti impegni** in base ai dati nella tabella.  

 ![Primo esempio di movimenti di tracciabilità ordini nella tabella Movimenti impegni.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### Numeri di movimento 8 e 9  
 Per la necessità del componente LOTA e LOTB rispettivamente, i collegamenti di tracciabilità ordine vengono creati dalla domanda nella tabella 5407, **Componenti ordini produzione**, all'approvvigionamento nella tabella 32, **Mov. contabili articoli**. Il campo **Stato impegno** contiene **Tracciabilità** per indicare che questi movimenti sono collegamenti tracciabilità ordine dinamici tra approvvigionamento e domanda.  

> [!NOTE]  
>  Il campo **Nr. lotto** è vuoto nelle righe della domanda, in quanto i numeri di lotto non sono specificati nelle righe componenti dell'ordine di produzione rilasciato.  

### Numeri di movimento 10  
 Dalla domanda di vendita nella tabella 37, **Righe vendite**, un collegamento di tracciabilità ordine viene creato nell'approvvigionamento nella tabella 5406, **Righe ordini prod.**. Il campo **Stato impegno** contiene **Impegno** e il campo **Vincolato** contiene **Ordine su ordine**. Questo perché l'ordine di produzione rilasciato è stato generato specificamente per l'ordine di vendita e deve rimanere collegato a differenza dei collegamenti di tracciabilità ordine con uno stato di impegno **Tracciabilità**, che vengono creati e modificati in modo dinamico. Per ulteriori informazioni, vedere la sezione "Prenotazioni automatiche" in questo argomento.  

 A questo punto nello scenario, le 100 unità di LOTA e LOTB vengono trasferite nell'ubicazione EST da un ordine di trasferimento.  

> [!NOTE]  
>  Solo la spedizione dell'ordine di trasferimento viene registrata in questa fase, non il carico.  

 Ora esistono i seguenti movimenti di tracciabilità ordini nella tabella **Movimenti impegni**.  

 ![Secondo esempio di movimenti di tracciabilità ordini nella tabella Movimenti impegni.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### Numeri di movimento 8 e 9  
 I movimenti di tracciabilità ordini per i due lotti del componente che riflettono la domanda nella tabella 5407 vengono modificati dallo stato di impegno di **Tracciabilità** a **Surplus**. Il motivo è che gli approvvigionamenti a cui erano collegati prima, nella tabella 32, sono stati utilizzati dalla spedizione dell'ordine di trasferimento.  

 Il surplus genuino, come n questo caso, riflette un approvvigionamento o una domanda effettiva eccedente che non viene tracciata. È un'indicazione di sbilanciamento nella rete di ordini, che genererà un messaggio di azione dal sistema di pianificazione a meno che non venga risolto in modo dinamico.  

### Numeri di movimento da 12 a 16  
 Poiché i due lotti del componente vengono registrati nell'ordine di trasferimento come spediti ma non ricevuti, tutti i movimenti di tracciabilità ordine positivi correlati sono del tipo di impegno **Surplus**, indicando che non sono allocati ad alcuna domanda. Per ciascun numero di lotto, un movimento si riferisce alla tabella 5741, **Riga trasferimento** e un movimento si riferisce all'ubicazione in transito in cui gli articoli ora esistono.  

 A questo punto nello scenario, l'ordine di trasferimento dei componenti dall'ubicazione EST a OVEST viene registrato come ricevuto.  

 Ora esistono i seguenti movimenti di tracciabilità ordini nella tabella **Movimenti impegni**.  

 ![Terzo esempio di movimenti di tracciabilità ordini nella tabella Movimenti impegni.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

 I movimenti di tracciabilità ordine sono ora simili al primo punto dello scenario, prima che l'ordine di trasferimento fosse registrato come solo spedito, eccetto i movimenti per il componente che ora hanno lo stato di impegno **Surplus**. Ciò avviene in quanto i componenti necessari sono ancora nell'ubicazione OVEST, come indicato dal fatto che il campo **Codice ubicazione** nella riga del componente dell'ordine di produzione contiene **OVEST** come impostato nel campo di setup **Componenti nell'ubicazione**. L'approvvigionamento che prima era allocato a questa domanda è stato trasferito nell'ubicazione EST e ora non può essere tracciato completamente a meno che la necessità di componenti nella riga ordine di produzione non venga modificata nell'ubicazione EST.  

 A questo punto dello scenario, il **Cod. ubicazione** nella riga ordine di produzione è impostato su **EST**. Inoltre, nella pagina **Righe tracciabilità articolo**, le 30 unità di LOTA e le 70 unità di LOTB vengono assegnate alla riga dell'ordine di produzione.  

 Ora esistono i seguenti movimenti di tracciabilità ordini nella tabella **Movimenti impegni**.  

 ![Quarto esempio di movimenti di tracciabilità ordini nella tabella Movimenti impegni.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### Numeri di movimento 21 e 22  
 Poiché la necessità di componenti è stata modificata nell'ubicazione EST e l'approvvigionamento è disponibile come movimenti contabili articoli nell'ubicazione EST, tutti i movimenti di tracciabilità ordine per i due numeri di lotto sono ora completamente tracciati, indicati dallo stato di impegno **Tracciabilità**.  

 Il campo **Nr. lotto** è ora compilato nel movimento tracciabilità ordine per la tabella 5407, poiché erano stati assegnati i numeri di lotto alle righe componente dell'ordine di produzione.  

 Per ulteriori esempi sui movimenti di tracciabilità ordini nella tabella **Movimenti impegni** vedere il white paper "Tabella movimenti impegni" in [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348) (è richiesto il login).

## Messaggistica di azione  
 Quando il sistema di tracciabilità ordini rileva uno sbilanciamento nella rete di ordini, crea automaticamente un messaggio di azione per informare l'utente. I messaggi di azione sono chiamate generate dal sistema per ogni azione che specifica i dettagli dello squilibrio e i suggerimenti su come ripristinare il saldo nella rete di ordini. Vengono visualizzati come righe di pianificazione nella pagina **Prospetto pianificazione** quando si sceglie **Genera messaggi di azione**. Inoltre, i messaggi di azione vengono visualizzati nelle righe di pianificazione generate in fase di pianificazione per riflettere i suggerimenti del sistema di pianificazione su come ripristinare il saldo nella rete di ordini. In entrambi i casi, i suggerimenti vengono creati nella rete di ordini, scegliendo **Esegui messaggi di azione**.  

 Un messaggio di azione indirizza un livello della DB alla volta. Se l'utente accetta il messaggio di azione, questo può provocare altri messaggi di azione al successivo livello della DB.  

 Nella seguente tabella vengono mostrati i messaggi di azione esistenti.  

|Messaggio azione|Description|  
|--------------------|---------------------------------------|  
|**Cambia Qtà**|Modifica la quantità in un ordine di approvvigionamento esistente per coprire una domanda modificata o nuova.|  
|**Ripianifica**|Ripianifica la data di scadenza di un ordine esistente.|  
|**Riprogr. e mod. qtà**|Ripianifica la data di scadenza e modifica la quantità di un ordine esistente.|  
|**Nuovo**|Crea un nuovo ordine se la domanda non può essere evasa dai uno dei messaggi di azione precedenti.|  
|**Annulla**|Annulla un ordine esistente.|  

 Il sistema di tracciabilità ordine tenta sempre di risolvere un eventuale sbilanciamento nella rete di ordini esistente. Se ciò non è possibile, viene generato un messaggio di azione per creare un nuovo ordine. Viene di seguito riportato l'elenco con priorità che il sistema di tracciamento dell'ordine utilizza quando determina come ripristinare il saldo. Se viene immessa una domanda aggiuntiva nella rete di ordini, nel sistema viene tentato di tracciare l'ordine tramite i controlli seguenti:  

1.  Controllare un approvvigionamento eccedente nel record di tracciabilità ordine esistente per questa domanda.  
2.  Controllo dei carichi pianificati e programmati ordinate in base alla data di carico. La data più recente possibile è selezionata.  
3.  Controllo delle scorte disponibili.  
4.  Controllo dell'esistenza di un ordine di approvvigionamento nel record corrente di tracciabilità ordini. In caso affermativo, viene visualizzato un messaggio di azione di tipo **Cambia** per aumentare l'ordine.  
5.  Controllare che non esista alcun ordine di approvvigionamento nel record corrente di tracciabilità ordini. In caso affermativo, viene visualizzato un messaggio di azione di tipo **Nuovo** per creare un nuovo ordine.  

 Una domanda aperta attraversa l'elenco e compensa l'approvvigionamento disponibile a ciascun passaggio. Tutte le domande residue vengono sempre coperte dal controllo 4 oppure 5.  

 Se si verifica una diminuzione della quantità di domanda, il sistema di tracciabilità ordini cerca di risolvere lo squilibrio eseguendo i controlli precedenti in ordine inverso. Ciò significa che i messaggi di azione esistenti potrebbero essere modificati o persino eliminati, se necessario. Il sistema di tracciabilità ordine presenta sempre il risultato netto dei calcoli all'utente.  

## Tracciabilità e pianificazione ordini  
 Quando il sistema di pianificazione viene eseguito, elimina tutti i record di tracciabilità ordini e i movimenti di messaggi di azione esistenti e li ricrea come suggerimenti della riga di pianificazione in base alle coppie e alle priorità di approvvigionamento e domanda. Una volta completata l'esecuzione della pianificazione, la rete di ordini è a saldo.  

### Sistema di pianificazione contro tracciabilità ordini e messaggistica di azione  
 Nel seguente confronto vengono mostrate le differenze tra i metodi utilizzati dal sistema di pianificazione per creare suggerimenti per una riga di pianificazione e i metodi utilizzati dal sistema di tracciabilità ordine per creare i record di tracciabilità ordine e i messaggi di azione.  

-   Il sistema di pianificazione si occupa dell'intero modello di approvvigionamento e domanda di un determinato articolo, mentre la tracciabilità ordine si occupa dell'ordine che l'ha attivata.  

-   Il sistema di pianificazione si occupa di tutti i livelli della gerarchia della DB, mentre la tracciabilità ordine si occupa di un livello della DB per volta.  

-   Il sistema di pianificazione stabilisce collegamenti tra approvvigionamento e domanda in base alla data di scadenza alla quale è assegnata la priorità. La tracciabilità ordini stabilisce collegamenti tra approvvigionamento e domanda in base alla sequenza di immissione degli ordini.  

-   A differenza della tracciabilità ordine, il sistema di pianificazione prende in considerazione i parametri di pianificazione.  

-   Il sistema di pianificazione crea i collegamenti in una modalità batch attivata dall'utente quando bilancia domanda e approvvigionamento, mentre la tracciabilità ordine crea i collegamenti automaticamente e in modo dinamico quando l'utente immette gli ordini.  

## Vedi anche  
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
