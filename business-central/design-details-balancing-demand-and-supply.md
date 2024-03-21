---
title: Dettagli di progettazione - Bilanciamento della domanda e dell'offerta
description: Questo articolo descrive come assegnare priorità agli obiettivi bilanciando l'offerta con la domanda.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# Dettagli di progettazione: Bilanciamento della domanda e dell'offerta

Per capire come funziona il sistema di pianificazione, è importante comprendere i suoi obiettivi prioritari:  

* Qualsiasi domanda verrà soddisfatta da approvvigionamento sufficiente.  
* Qualsiasi approvvigionamento serve a uno scopo.  

In genere, questi obiettivi vengono raggiunti equilibrando l'approvvigionamento con la domanda.  

## Domanda e offerta

Il termine *approvvigionamento* si riferisce a qualsiasi tipo di quantità positiva o in entrata, come ad esempio:

* Inventario
* Acquisti
* Assemblaggio
* Produzione
* Trasferimenti in entrata
* Resi di vendita  

Il termine *domanda* si riferisce a qualsiasi tipo di domanda lorda, come ad esempio:

* Un articolo per un ordine di vendita
* Un componente per un ordine di produzione

[!INCLUDE [prod_short](includes/prod_short.md)] ti consente di usare i tipi di domanda più tecnici, ad esempio i resi di acquisto e le giacenze negative.

Per ordinare le origini di offerta e domanda, il sistema di pianificazione le organizza su due sequenze temporali chiamate profili di magazzino. Un profilo è per gli eventi di domanda e l'altro è per i corrispondenti eventi di offerta. Ogni evento di approvvigionamento rappresenta un'entità su un ordine, ad esempio:

* Una riga ordine vendita
* Un movimento contabile articolo
* Una riga ordine di produzione

Quando vengono caricati i profili di magazzino, i set di domanda-offerta vengono bilanciati in modo da fornire un piano di offerta che soddisfi gli obiettivi elencati.

I livelli di magazzino e i parametri di pianificazione sono altri tipi di domanda e offerta. Questi tipi sono sottoposti al bilanciamento integrato per rifornire gli articoli di magazzino. Per ulteriori informazioni vedi [Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md).

## Il concetto di bilanciamento in breve

La domanda viene dai tuoi clienti. L'approvvigionamento è ciò che crei e rimuovi per stabilire il saldo. Il sistema di pianificazione inizia con la domanda e successivamente risale a ritroso fino all'offerta.  

I profili di magazzino contengono le informazioni sulle domande, le offerte, le quantità e l'intervallo. I profili compongono i due lati della bilancia.  

L'obiettivo della pianificazione consiste nel bilanciare la domanda e l'offerta di un articolo per garantire che l'offerta corrisponda alla domanda così come definito dalle regole e dai parametri di pianificazione.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Panoramica del bilanciamento dell'offerta e della domanda.":::

## Elaborare gli ordini prima della data di inizio pianificazione

Per evitare che un piano di approvvigionamento mostri suggerimenti irragionevoli, il sistema di pianificazione non pianificherà nulla nel periodo precedente la data di inizio pianificazione. La seguente regola si applica a tale periodo:

* Tutta la domanda e l'offerta prima della data di inizio del periodo di pianificazione sono considerate come parte del magazzino o spedite.  

Con poche eccezioni, il sistema di pianificazione non suggerisce le modifiche agli ordini di approvvigionamento nel periodo né crea nessun collegamento di tracciabilità per quel periodo. Le eccezioni a questa regola sono le seguenti:  

* Le scorte che si prevede saranno disponibili, inclusa la somma della domanda e dell'offerta nel periodo, sono inferiori a zero.  
* Gli ordini retrodatati richiedono numeri seriali o di lotto.  
* Il set di offerta-domanda è collegato da un metodo ordine su ordine. 

Se la giacenza disponibile iniziale è minore di zero, il sistema di pianificazione suggerisce un ordine di approvvigionamento di emergenza datato il giorno precedente al periodo di pianificazione per coprire la quantità mancante. Il magazzino previsto e disponibile sarà sempre almeno uguale a zero quando inizia la pianificazione per il periodo futuro. Nella riga di pianificazione per questo ordine di approvvigionamento verrà visualizzata un'icona di avviso di emergenza. Verranno inoltre fornite informazioni aggiuntive.

### I numeri seriali o di lotto e i collegamenti ordine su ordine sono esenti dal periodo precedente  

Se sono richiesti numeri di serie o di lotto o esiste un collegamento ordine su ordine, il sistema di pianificazione ignora la regola relativa al periodo precedente. Includerà quantità retrodatate dalla data di inizio e può suggerire azioni correttive se l'offerta e la domanda non sono sincronizzate. Questi set di domanda-offerta devono corrispondere per garantire che una domanda specifica sia soddisfatta.

## Caricare i profili di magazzino

Per ordinare le origini di offerta e domanda, il sistema di pianificazione le organizza su due sequenze temporali chiamate profili di magazzino.  

Domanda e offerta con date di scadenza corrispondenti o successive alla data iniziale di pianificazione vengono caricate in ciascun profilo di magazzino. Una volta caricate, i tipi di domanda e offerta vengono ordinati in base alle priorità generali, ad esempio:

* Data di scadenza
* Codici di ultimo livello
* Ubicazione
* Variante

Vengono applicate delle priorità di ordine a diversi tipi per garantire che la domanda più importante sia completata per prima. Per ulteriori informazioni vedi [Priorità degli ordini](design-details-balancing-demand-and-supply.md#prioritize-orders).  

La domanda può anche essere negativa. Tratta la domanda negativa come offerta. Tuttavia, a differenza dell'offerta tipica, la domanda negativa è considerata un'offerta fissa. Il sistema di pianificazione può prenderla in considerazione, ma non suggerirà modifiche.  

In genere, il sistema di pianificazione considera tutti gli ordini di approvvigionamento dopo la data di inizio della pianificazione come oggetti da modificare per soddisfare la domanda. Tuttavia, non appena una quantità viene registrata da un ordine di approvvigionamento, non può essere modificata dal sistema di pianificazione. I seguenti ordini non possono essere ripianificati:  

* Ordini di produzione rilasciati in cui è stato registrato il consumo o l'output.  
* Ordini di assemblaggio in cui è stato registrato il consumo o l'output.  
* Ordini di trasferimento in cui è stata registrata la spedizione.  
* Ordini di acquisto in cui il carico è stato registrato.  

Oltre a caricare i tipi di offerta e di domanda, alcuni tipi vengono caricati con attenzione alle regole speciali e alle dipendenze. Le seguenti sezioni di questo articolo descrivono queste regole e dipendenze.  

### Le dimensioni articolo sono separate  

Il piano di approvvigionamento deve essere calcolato per ogni combinazione delle dimensioni dell'articolo, ad esempio la variante e l'ubicazione. Solo le combinazioni che includono la necessità di offerta e/o di domanda devono essere calcolate.  

Il sistema di pianificazione ricerca le combinazioni nel profilo di magazzino. Quando trova una nuova combinazione, crea un record di controllo interno che contiene le informazioni sulla combinazione. Il sistema di pianificazione inserisce la SKU come record di controllo o ciclo esterno. Di conseguenza, vengono impostati i parametri di pianificazione in base a una combinazione di variante e ubicazione e il sistema può procedere al ciclo interno. 

> [!NOTE]  
> Non devi immettere un record di SKU durante l'immissione della domanda e/o dell'offerta per una particolare combinazione di variante e ubicazione. Di conseguenza, se una SKU non esiste per una combinazione specifica, [!INCLUDE [prod_short](includes/prod_short.md)] crea un record SKU temporaneo in base ai dati dell'articolo. Se l'opzione **Ubicazione obbligatoria** è attivata nella **pagina Setup magazzino**, devi creare una SKU o attivare l'interruttore **Componenti nell'ubicazione**. Per ulteriori informazioni, vedi [Pianificazione con o senza ubicazioni](production-planning-with-without-locations.md).  

### I numeri seriali e di lotto vengono caricati dal livello di specifica  

I numeri di serie e di lotto vengono caricati nei profili del magazzino insieme alla domanda e all'offerta cui sono assegnati.  

Gli attributi di domanda e offerta sono ordinati per priorità ordini e per livello di specifica. Poiché le corrispondenze dei numeri di serie e di lotto riflettono il livello di specifica, una domanda più specifica verrà corrisposta prima di una domanda meno specifica. Ad esempio, una domanda specifica potrebbe essere un numero di lotto specificato per una riga di vendita. Una domanda meno specifica potrebbe essere una vendita di un qualsiasi numero di lotto.

> [!NOTE]  
> Le uniche regole di priorità dedicate per l'offerta e la domanda dotati di numeri seriali e di lotto, sono il livello di specifica definito dalle relative combinazioni di numeri seriali e di lotto e l'impostazione di tracciabilità articolo degli articoli interessati.  

Durante il bilanciamento, il sistema di pianificazione considera non flessibile l'approvvigionamento con numeri di serie e di lotto. Il sistema non aumenterà né ripianificherà tali ordini di approvvigionamento. L'unica eccezione a questo è se vengono utilizzati in una relazione ordine su ordine. Per ulteriori informazioni, vedi [I collegamenti ordine su ordine non sono mai interrotti](#order-to-order-links-are-never-broken). Questa eccezione protegge l'approvvigionamento dal ricevere vari messaggi di azione potenzialmente in conflitto quando un approvvigionamento contiene attributi che variano. Ad esempio, gli attributi variabili possono verificarsi quando l'approvvigionamento ha una raccolta di numeri di serie diversi.  

Un altro motivo per cui l'approvvigionamento con numeri seriali e di lotto non è flessibile è perché i numeri seriali e di lotto vengono spesso assegnati in una fase avanzata del processo. Potrebbe essere una fonte di confusione se le modifiche vengono suggerite a quel punto.  

Il bilanciamento del numero di serie e di lotto non rispetta la regola di non pianificare nulla prima della data di inizio della pianificazione. Se la domanda e l'offerta non sono sincronizzati, il sistema di pianificazione suggerisce delle modifiche o dei nuovi ordini, indipendentemente dalla data di inizio della pianificazione.  

### I collegamenti ordine su ordine non sono mai interrotti

Nella pianificazione di un articolo ordine su ordine, l'approvvigionamento collegato deve essere utilizzata solo per la sua destinazione originaria. La domanda collegata non deve essere coperta da un'altra offerta, anche se è disponibile per tempo e quantità. Ad esempio, non puoi usare un ordine di assemblaggio collegato a un ordine di vendita in uno scenario di assemblaggio su ordine per coprire un'altra domanda.  

La domanda e l'offerta ordine su ordine devono essere in totale pareggio. Il sistema di pianificazione assicurerà l'approvvigionamento senza considerare i parametri di dimensioni ordine, i modificatori e le quantità di magazzino (diverse dalle quantità correlate agli ordini collegati). Per lo stesso motivo, il sistema suggerirà approvvigionamenti eccedente in calo se la domanda collegata viene diminuita.  

Questo bilanciamento influisce anche sui tempi. L'orizzonte limitato che viene fornito dall'intervallo di tempo non viene considerato; l'approvvigionamento verrà riprogrammato se i tempi della domanda sono cambiati. Tuttavia, il tempo di smorzamento sarà rispettato e impedirà la riprogrammazione all'esterno degli approvvigionamenti ordine su ordine, ad eccezione degli approvvigionamenti interni di un ordine di produzione a più livelli (ordine di progetto).  

> [!NOTE]  
> I numeri seriali e di lotto possono inoltre essere specificati nella domanda ordine su ordine. In questo caso, l'approvvigionamento non viene considerato inflessibile, come nel caso dei numeri seriali e di lotto. In questo caso, il sistema aumenterà o diminuirà a seconda dei cambiamenti nella domanda. Se una domanda contiene più numeri seriali e di lotto diversi, ad esempio più di un numero di lotto, un ordine di approvvigionamento verrà suggerito per ogni lotto.  

> [!NOTE]  
> Le previsioni non devono condurre alla creazione degli ordini di approvvigionamento associati a un collegamento ordine-a-ordine. Se viene utilizzata la previsione, deve essere utilizzata solo come generatore della domanda dipendente in un ambiente di produzione.

### Il componente richiesto viene caricato in base alle modifiche dell'ordine di produzione

Nella gestione degli ordini di produzione, il sistema di pianificazione deve monitorare i componenti necessari prima di caricarli nel profilo della domanda. Le righe componenti derivanti da un ordine di produzione modificato sostituiranno quelle dell'ordine originale. In questo modo il sistema di pianificazione non duplica le righe di pianificazione per un componente necessario.  

### Consumare la scorta di sicurezza

La scorta di sicurezza è principalmente un tipo di domanda che viene caricata nel profilo di magazzino alla data di inizio della pianificazione.  

La scorta di sicurezza è una quantità di magazzino accantonata per compensare le incertezze della domanda durante il rifornimento. Tuttavia, può essere consumata per soddisfare una domanda. In tal caso, il sistema di pianificazione assicurerà che la scorta di sicurezza venga rapidamente sostituita. Il sistema suggerisce un ordine di approvvigionamento per reintegrare la quantità della scorta di sicurezza alla data in cui viene consumata. La riga di pianificazione relativa a tale ordine conterrà un'icona di avviso di eccezione indicante che la scorta di sicurezza è stata parzialmente o completamente consumata per un ordine di eccezione per la quantità mancante.  

### La domanda di previsione viene ridotta dagli ordini di vendita

La previsione della domanda esprime la domanda futura prevista. Mentre la domanda effettiva viene immessa, in genere come ordini vendita per articoli prodotti, viene utilizzata la previsione.

La previsione in se non viene ridotta dagli ordini di vendita. Tuttavia, le quantità previste che sono utilizzate nel calcolo della pianificazione vengono ridotte delle quantità dell'ordine di vendita prima che la quantità residua sia immessa nel profilo di magazzino della domanda. Per le vendite durante un periodo, la pianificazione include sia gli ordini di vendita aperti sia i movimenti contabili articoli delle vendite spedite. L'eccezione a questa regola è quando provengono da un ordine programmato.  

È necessario definire un periodo di previsione valido. La data della quantità prevista definisce l'inizio del periodo e la data della previsione successiva definisce la fine del periodo.  

La previsione per periodi precedenti al periodo di pianificazione non viene utilizzata, indipendentemente dal fatto che sia stata consumata o meno. La prima cifra di previsione interessante è la data di inizio o la data più vicina alla data di inizio della pianificazione.  

La previsione può riguardare diversi tipi di domanda:

* Domanda indipendente, come gli ordini di vendita
* Domanda dipendente, ad esempio i componenti dell'ordine di produzione.

Un articolo può avere entrambi i tipi di previsione. Durante la pianificazione, il consumo avviene separatamente, prima per domanda indipendente quindi per la domanda dipendente.  

### La domanda dell'ordine programmato viene ridotta dagli ordini di vendita

Le previsioni vengono completate dagli ordini di vendita programmati al fine di specificare la domanda futura di un cliente specifico. Analogamente alle previsioni (non specificato), le vendite effettive dovrebbero consumare la domanda prevista e la quantità residua dovrebbe immettere il profilo di magazzino della domanda. Il consumo non riduce la quantità dell'ordine programmato.

Il calcolo della pianificazione include gli ordini di vendita aperti collegati alla riga ordine di copertura specifica, ma non include alcun periodo di tempo valido. Non vengono inclusi neppure gli ordini registrati perché la procedura di registrazione ha già ridotto la quantità inevasa dell'ordine programmato.

## Assegnare la priorità agli ordini

All'interno di una determinata SKU, la data richiesta o disponibile rappresenta la massima priorità. La domanda di oggi deve essere gestita prima della domanda della prossima settimana. Ma, oltre a questa priorità generale, il sistema di pianificazione fornirà i seguenti suggerimenti in base alle priorità dell'ordine:

* Quale tipo di richiesta devi soddisfare per prima.
* Quale origine di approvvigionamento deve essere collegata prima di collegare altre origini di approvvigionamento.  

La domanda e l'offerta caricate contribuiscono a un profilo per la giacenza disponibile in base alle priorità.  

### Priorità sul lato della domanda  

1. Già spediti: Mov. contabili articolo  
2. Ord. reso di acquisto  
3. Ordine di vendita  
4. Ordine assistenza  
5. Necessità di componenti di produzione  
6. Riga ordine di assemblaggio  
7. Ordine di trasferimento in uscita  
8. Ordine programmato (non ancora utilizzato dagli ordini di vendita correlati)  
9. Previsione (non ancora utilizzata da altri ordini di vendita)  

> [!NOTE]  
> I resi di acquisto non vengono in genere inclusi nella pianificazione dell'approvvigionamento e devono essere sempre prenotati dal lotto che sta per essere reso. Se non prenotati, i resi di acquisto svolgono un ruolo nella disponibilità e hanno un'elevata priorità per evitare che il sistema suggerisca un ordine di approvvigionamento solo per un ordine di reso.  

### Priorità sul lato dell'approvvigionamento  

1. Già in magazzino: Mov. contabili articoli (Flessibilità pianificazione = Nessuna)  
2. Ordine di reso vendita (flessibilità pianificazione = nessuna)  
3. Ordine di trasferimento in ingresso  
4. Ordine di produzione  
5. Ordine di assemblaggio  
6. Ordine di acquisto  

### Priorità correlata allo stato di domanda e offerta  

Oltre alle priorità derivanti dal tipo di domanda e offerta, ci sono altre cose che influenzano la flessibilità della pianificazione. Ad esempio, le attività di warehouse e lo stato dei seguenti ordini:

* Vendite
* Acquisti
* Trasferimento
* Assemblaggio
* Produzione

Lo stato di questi ordini ha i seguenti effetti: 

1. Gestito parzialmente (flessibilità pianificazione = nessuna)  
2. Già nel processo nel warehouse (flessibilità pianificazione = Nessuna)  
3. Rilasciato - tutti i tipi di ordine (flessibilità pianificazione = illimitata)  
4. Ordine di produzione confermato (flessibilità pianificazione = illimitata)  
5. Pianificato/Aperto - tutti i tipi di ordine (flessibilità pianificazione = illimitata)

## Bilanciamento dell'offerta con la domanda

Il sistema di pianificazione bilancia domanda e offerta suggerendo azioni per rivedere gli ordini di approvvigionamento che non sono bilanciati. Questo bilanciamento avviene per ogni combinazione di variante e ubicazione.  

Immagina che ogni profilo di magazzino contenga due stringhe:

* Una stringa di eventi di domanda, ordinati per data e priorità
* Una stringa corrispondente di eventi di approvvigionamento

Ogni evento si riferisce al suo tipo e identificativo di origine. Le regole per bilanciare l'articolo sono chiare. La corrispondenza di domanda e offerta può verificarsi in qualsiasi momento nel processo, come segue:  

1. Non esiste alcuna domanda o approvvigionamento per l'articolo => la pianificazione è terminata (o non deve iniziare).  
2. La domanda esiste ma non esiste un'offerta => suggerire l'offerta.  
3. L'offerta esiste ma non esiste una domanda => offerta da annullare.  
4. Esistono sia la domanda che l'offerta => è necessario fare domande e fornire risposte affinché [!INCLUDE [prod_short](includes/prod_short.md)] possa garantire che la domanda venga soddisfatta e l'offerta sia sufficiente.

    Se l'intervallo di approvvigionamento non è appropriato, è possibile riprogrammare l'approvvigionamento come segue:  

    1. Se l'offerta viene inserita prima della domanda, è possibile riprogrammarla in modo che il magazzino sia più basso possibile.  
    2. Se l'offerta viene inserita successivamente alla domanda, è possibile programmarla. Altrimenti, il sistema suggerirà un nuovo approvvigionamento.  
    3. Se l'offerta soddisfa la domanda alla data, il sistema di pianificazione può verificare se la quantità di offerta può coprire la domanda.  

    Una volta impostati i tempi, la quantità da fornire può essere calcolata come segue:  

    1. Se la quantità di offerta è minore della domanda, la quantità di offerta può essere aumentata (o non aumentata se limitata da un criterio di quantità massima).  
    2. Se la quantità di offerta è maggiore della domanda, la quantità di offerta può essere diminuita (o non diminuita se limitata da un criterio di quantità minima).  

    A questo punto, esiste una di queste due situazioni:  

    1. La domanda corrente può essere coperta, nel qual caso può essere chiusa e si può procedere con la pianificazione della domanda successiva.  
    2. L'approvvigionamento ha raggiunto il massimo, lasciando una certa quantità di domanda scoperta. In questo caso, il sistema di pianificazione può chiudere l'approvvigionamento corrente e procedere a quello successivo.  

 La procedura inizia sempre con la domanda successiva e l'offerta corrente o viceversa. L'approvvigionamento corrente potrebbe essere in grado di soddisfare anche la domanda successiva o la domanda corrente se non è stata ancora interamente coperta.  

### Regole per le azioni per gli eventi di approvvigionamento

Per i calcoli dall'alto verso il basso in cui l'offerta deve soddisfare la domanda, la domanda è specificata. È al di fuori del controllo del sistema di pianificazione. Tuttavia, il sistema di pianificazione può gestire il lato dell'approvvigionamento e fornire i seguenti suggerimenti:

* Crea nuovi ordini di approvvigionamento
* Riprogramma gli ordini esistenti o modifica le quantità
* Annulla gli ordini di approvvigionamento non più necessari  

Per escludere un ordine di approvvigionamento dai suggerimenti di pianificazione, puoi dichiarare di non disporre di flessibilità di pianificazione (flessibilità pianificazione = nessuna). Quindi, l'approvvigionamento in eccesso da tale ordine verrà utilizzato per soddisfare la domanda, ma non verrà suggerita alcuna azione. 

In genere, tutti gli approvvigionamenti hanno una flessibilità di pianificazione che è limitata dalle condizioni di ciascuna delle azioni suggerite.  

* **Riprogramma all'esterno**: la data di un ordine di approvvigionamento esistente può essere programmata per soddisfare la data di scadenza della domanda a meno che:

  * Rappresenta il magazzino (sempre nel giorno zero).  
  * Contiene un metodo da ordine a ordine collegato a un'altra domanda.  
  * È fuori dalla finestra per la riprogrammazione nell'intervallo di tempo.
  * Esiste un approvvigionamento più recente che può essere utilizzato.  
  * D'altro canto, l'utente potrebbe scegliere di non ripianificare per i seguenti motivi:
  * L'ordine di approvvigionamento è associato a un'altra domanda in una data precedente.  
  * La riprogrammazione necessaria è talmente minima che è trascurabile.  

* **Riprogramma all'interno**: la data di un ordine di approvvigionamento esistente può essere programmata nel periodo, ad eccezione delle seguenti condizioni:

  * È collegata direttamente a un'altra domanda.  
  * È fuori dalla finestra per la riprogrammazione definita dall'intervallo di tempo.

> [!NOTE]  
> Nella pianificazione di un articolo tramite un punto di riordino, puoi riprogrammare l'ordine di approvvigionamento. Ciò spesso avviene negli ordini di approvvigionamento programmati in avanti attivati da un punto di riordino.

* **Aumentare la quantità**: la quantità di un ordine di approvvigionamento esistente può essere aumentata per soddisfare la domanda a meno che l'ordine di approvvigionamento sia collegato direttamente a una domanda da un collegamento ordine a ordine.  

> [!NOTE]  
> Anche se è possibile aumentare l'ordine di approvvigionamento, l'aumento potrebbe essere limitato a causa di quantità massima ordine definita.  

* **Riduci quantità**: un ordine di approvvigionamento esistente con un surplus rispetto a una domanda esistente può essere ridotto per soddisfare la domanda.  

> [!NOTE]  
> Anche se la quantità può essere diminuita, può ancora esservi un certo surplus rispetto alla domanda a causa di una quantità minima di ordine definita o ordine multiplo. 

* **Annulla**: come incidente speciale dell'azione di riduzione quantità, l'ordine di approvvigionamento può essere annullato se è stato diminuito a zero. 
* **Nuovo**: se non è presente alcun ordine di approvvigionamento già esistente o un ordine esistente non può essere modificato per soddisfare la quantità necessaria alla data di scadenza per la domanda, verrà proposto un nuovo ordine di approvvigionamento.  

### Determinare la quantità di approvvigionamento  

I parametri di pianificazione che definisci controllano la quantità suggerita di ogni ordine di approvvigionamento.  

Quando il sistema di pianificazione calcola la quantità di nuovo ordine di approvvigionamento o la modifica della quantità in un ordine esistente, la quantità suggerita può essere diversa dalla quantità effettivamente richiesta.  

Se è selezionata una quantità massima di magazzino o una quantità di ordine fissa, la quantità suggerita può essere aumentata per soddisfare la quantità fissa o la giacenza massima. Se un metodo di riordino utilizza un punto di riordino, la quantità può essere aumentata almeno per soddisfare il punto di riordino. 

La quantità suggerita può essere modificata nella sequenza:  

1. Fino alla quantità massima ordine.  
2. Fino alla quantità minima ordine.  
3. Fino a soddisfare la molteplicità di ordini più vicina.

### Collegamenti della tracciabilità ordini durante la pianificazione  

Per la tracciabilità dell'ordine durante la pianificazione, il sistema di pianificazione ridispone i collegamenti di tracciabilità ordine creati per le combinazioni articolo, variante e ubicazione. Il sistema riorganizza i collegamenti di tracciamento per i seguenti motivi:

* Per verificare i suggerimenti per coprire la domanda e garantire che tutti gli ordini di approvvigionamento siano necessari.  
* I collegamenti di tracciamento degli ordini devono essere ribilanciati regolarmente.  

Nel tempo, i collegamenti di tracciamento degli ordini diventano sbilanciati. I collegamenti di tracciabilità ordini si sbilanciano perché la rete di tracciabilità ordini non viene ridisposta fino a quando un evento di offerta o di domanda non viene chiuso.

Prima di bilanciare l'offerta con la domanda, il sistema di pianificazione elimina tutti i collegamenti di tracciabilità ordine. Durante il processo di bilanciamento, quando viene chiuso un evento di offerta o di domanda, il sistema crea nuovi collegamenti di tracciabilità ordine tra la domanda e l'offerta.  

> [!NOTE]  
> Anche se l'articolo non è impostato per la tracciabilità dinamica dell'ordine, il sistema di pianificazione creerà collegamenti di tracciabilità ordine.

## Chiusura della domanda e dell'offerta bilanciate

Il bilanciamento dell'approvvigionamento ha tre possibili esiti:

* La quantità e la data necessarie degli eventi di domanda sono soddisfatte e la pianificazione può essere chiusa. L'evento di offerta rimane aperto e può essere in grado di coprire la domanda successiva. L'evento di offerta aperto consente alla procedura di bilanciamento di iniziare di nuovo con l'evento di offerta corrente e la domanda successiva.  
* L'ordine di approvvigionamento non può essere modificato per soddisfare tutta la domanda. Un evento di domanda è ancora aperto, con una quantità scoperta che può essere coperta dal successivo evento di approvvigionamento. L'evento di approvvigionamento corrente viene quindi chiuso, in modo che il bilanciamento posso riprendere dall'inizio con la domanda corrente e l'evento di approvvigionamento successivo.  
* Tutta la domanda è stata coperta e non esiste una domanda successiva (o non c'è stata alcuna domanda). Il surplus di approvvigionamento può essere ridotto (o annullato) e quindi chiuso. Anche qualsiasi altro evento di approvvigionamento deve essere annullato.  

Infine, il sistema di pianificazione crea un collegamento di tracciabilità ordine tra offerta e domanda.  

### Creare la riga di pianificazione (azione suggerita)  

Se viene suggerita una qualsiasi azione, ad esempio **Nuovo**, **Modifica quantità**, **Riprogramma**, **Riprogramma e modifica quantità**, o **Annulla**, per esaminare l'ordine di approvvigionamento, tramite il sistema di pianificazione viene creata una riga di pianificazione nel prospetto di pianificazione. Per la tracciabilità dell'ordine, la riga di pianificazione viene creata non solo quando l'evento di offerta viene chiuso, ma anche se l'evento di domanda è chiuso. Ciò è vero anche se l'evento di offerta è ancora aperto e può essere modificato quando viene elaborato il successivo evento di domanda. La riga di pianificazione può essere modificata nuovamente, una volta creata.

Per ridurre il carico sul database durante la gestione degli ordini di produzione, la riga di pianificazione può essere gestita a tre livelli:

* Creare solo la riga di pianificazione con la data di scadenza e la quantità corrente ma senza il ciclo e i componenti.  
* Includi il ciclo: il ciclo di produzione pianificato include il calcolo delle date di inizio e di fine e dei periodi. Includi il ciclo risulta molto impegnativo in termini di accessi al database. Per determinare le date di scadenza e di fine, può essere necessario calcolare il ciclo anche se l'evento di approvvigionamento non è stato chiuso. Ad esempio, se stai pianificando in avanti.  
* Includi l'esplosione della distinta base: questa operazione può avvenire poco prima della chiusura dell'evento di approvvigionamento.

## Vedere anche  

[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)  
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]