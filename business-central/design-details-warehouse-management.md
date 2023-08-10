---
title: Gestire le attività di warehouse
description: 'Oltre ai carichi e alle spedizioni, Business Central supporta una serie di attività di warehouse interne.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/05/2022
ms.custom: bap-template
---

# <a name="warehouse-management-overview"></a>Panoramica gestione del magazzino

Ci sono due cose importanti per tutte le aziende che spostano fisicamente le merci dentro e fuori dalla warehouse:

* Hanno una panoramica dei livelli di warehouse e del posizionamento degli articoli nella warehouse.
* Possono ricevere, prelevare e spedire gli articoli in modo rapido e preciso.

Per aiutare le aziende a raggiungere questi obiettivi, le funzionalità di warehouse in [!INCLUDE[prod_short](includes/prod_short.md)] aggiungono le seguenti funzionalità alla gestione dell'inventario:

* Collocazioni
* Spedizioni warehouse
* Prelievi magazzino
* Prospetto movimenti

Implementa queste funzionalità in diverse combinazioni per adattare i processi di warehouse alla tua azienda. Consenti l'aumento della complessità man mano che la tua azienda cresce e i tuoi processi cambiano.

## <a name="overview-of-different-configuration-options"></a>Panoramica delle diverse opzioni di configurazione

È possibile configurare le funzionalità warehouse in vari modi. È importante scegliere opzioni che migliorino i tuoi processi senza causare sovraccarico. La tabella seguente fornisce una panoramica delle configurazioni tipiche per i beni fisici.

|Livello di complessità|Descrizione|Impostazioni|Codice collocazione|Esempio di flusso in entrata|Esempio di flusso in uscita|Esempio di flusso interno|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Nessuna attività di warehouse dedicata.|Contabilizzazione di ordini e registrazioni.||Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordine di acquisto|Ordine di vendita| Ordine di produzione -> Registrazioni consumi|  
|Di base|Registrazione di ricezione e spedizione consolidata per più ordini.|**Richiesto carico**<br>**Richiesta spedizione**.|Facoltativo. Controllato dall'interruttore Il codice collocazione è obbligatorio|Ordini di acquisto -> Carico warehouse|Ordine vendita -> Spedizione warehouse|Come sopra.|
|Di base|Ordine per ordine.|Richiesto stoccaggio o Richiesto prelievo. </br><br/> **NOTA**: anche se le impostazioni sono definite **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile registrare carichi e spedizioni direttamente dai documenti commerciali di origine nelle ubicazioni in cui si selezionano queste caselle di controllo.|Facoltativo. Controllato dall'interruttore **Il codice collocazione è obbligatorio**.|Ordine di acquisto -> Stoccaggio in magazzino|Ordine vendita -> Prelievi magazzino|Ordine di produzione -> Prelievo in magazzino|
|Avanzate|Registrazione di ricezione e spedizione consolidata per più ordini.<br /><br />Attività di prelievo/stoccaggio consolidate per più documenti di origine.|Richiesto carico + Richiesto stoccaggio</br> Richiesta spedizione + Richiesto prelievo|Facoltativo. Controllato dall'interruttore Il codice collocazione è obbligatorio|Ordini di acquisto -> Carico warehouse -> Stoccaggio warehouse|Ordini di vendita -> Spedizioni warehouse -> Prospetto prelievi -> Prelievi warehouse| Ordine di produzione -> Prospetto prelievi -> Prelievi warehouse -> Registrazioni consumi|
|Avanzate|Come sopra + Attività di prelievo/stoccaggio diretti|Prelievo e stoccaggio diretti (gli interruttori dipendenti verranno abilitati automaticamente)|Obbligatorio|Come sopra.|Come sopra.| Ordine di produzione -> Prospetto prelievi -> Prelievi warehouse -> Registrazioni consumi|

La complessità aumenta con le dimensioni dell'organizzazione e il numero di reparti e persone coinvolti. Un processo può essere semplice, ad esempio, quando la stessa persona crea e registra un documento di vendita. I processi possono anche essere più complessi e coinvolgere diversi passaggi e persone. I seguenti passaggi sono un esempio di un processo più complesso:

1. Un gestore ordini crea un ordine di vendita.
1. Un responsabile di warehouse crea le istruzioni di prelievo.
1. Un dipendente di warehouse completa il flusso registrando la spedizione warehouse.

Il livello di complessità è influenzato anche dai tipi di documenti utilizzati nelle attività di warehouse. Ad esempio, è possibile utilizzare i documenti di entrata e stoccaggio di warehouse per il flusso in entrata, ma utilizzare i documenti di prelievo magazzino per il flusso in uscita.

Un altro fattore che influisce sulla complessità è il modo in cui la tua warehouse fisica è rappresentata in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni vedi [Modellazione della warehouse fisica](#modeling-the-physical-warehouse).

## <a name="modeling-the-physical-warehouse"></a>Modellazione della warehouse fisica

Hai diverse opzioni per rappresentare la configurazione della warehouse nel mondo reale in [!INCLUDE[prod_short](includes/prod_short.md)]. Le tue scelte determinano come lavorerai con le funzionalità della warehouse.

Il posizionamento degli articoli può essere scaffali, ubicazioni o collocazioni e ci sono pro e contro per ogni opzione.

### <a name="locations-and-bins"></a>Ubicazioni e collocazioni

Per gestire i beni fisici, devi disporre di almeno una ubicazione. È possibile utilizzare più ubicazioni o collocazioni per modellare la warehouse e la struttura organizzativa.

In genere, le ubicazioni sono il modo preferito per organizzare le operazioni distribuite in più aree geografiche. In alcuni casi, tuttavia, potresti voler creare più ubicazioni che si trovano nello stesso luogo. L'utilizzo delle ubicazioni presenta i seguenti vantaggi:

* Concedi l'accesso utilizzando le pagine **Impiegato warehouse** e **Centri di responsabilità**.
* Definisci calendari, cicli e tempi di gestione in entrata e in uscita per il calcolo e la pianificazione delle date. Per ulteriori informazioni, vedi [Informazioni sulla funzionalità di pianificazione](production-about-planning-functionality.md).
* Specifica le dimensioni predefinite e utilizza diverse impostazioni di registrazione dell'inventario.
* Imposta i parametri di pianificazione. Per ulteriori informazioni vedi [Parametri di pianificazione](production-about-planning-functionality.md#planning-parameters).  
* Utilizza funzionalità di warehouse diverse per ogni ubicazione.

### <a name="shelves-and-bins"></a>Scaffali e collocazioni

Se conservi sempre un articolo nello stesso posto, puoi utilizzare il campo **Nr. scaffale** nelle pagine **Scheda Articolo** o **Scheda Unità di stockkeeping**. Questo campo può essere un sistema di archiviazione manuale di base negli ambienti senza collocazioni. Il valore viene copiato dalla scheda articolo nelle righe del documento e nei report, ma solo a scopo informativo. Il valore non viene utilizzato nelle attività della warehouse o nei calcoli di disponibilità.

Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli:

* Una o più collocazioni fisse per un articolo.
* Collocazioni per operazioni specifiche, ad esempio una collocazione di spedizione o una collocazione di output di produzione.
* Limiti di capacità e peso della collocazione (solo per stoccaggi e prelievi diretti).
* Valutazione collocazione (solo per stoccaggi e prelievi diretti).

## <a name="typical-warehouse-workflow"></a>Flusso di lavoro tipico della warehouse

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|  
|In un flusso di base ordine per ordine, utilizza uno stoccaggio di magazzino per registrare il carico degli articoli nelle ubicazioni, inclusi eventuali carichi in eccesso. Oppure, se stai consolidando più ordini nel carico, utilizza un carico warehouse.|[Flusso in entrata](design-details-inbound-warehouse-flow.md)|
|Registra la spedizione di articoli dalle ubicazioni warehouse. Utilizza ordine per ordine un prelievo di magazzino. Oppure, se stai consolidando più ordini nella spedizione, utilizza una spedizione warehouse.|[Flusso in uscita](design-details-outbound-warehouse-flow.md)|
|Gestisci gli articoli all'interno dell'ubicazione warehouse. Ad esempio, quando sposti i componenti in produzione o esegui un conteggio dell'inventario fisico.|[Flusso interno](design-details-internal-warehouse-flows.md)|

Imposta i processi di warehouse adatti alla tua attività. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).

## <a name="terminology-related-to-warehouse-management"></a>Terminologia relativa a Warehouse Management

### <a name="complexity-levels"></a>Livelli di complessità

Usiamo i termini "base" e "avanzato" per differenziare i livelli di complessità. Questa semplice differenziazione copre numerosi livelli di complessità nei setup dell'ubicazione, ciascuno supportato da documenti di warehouse differenti. Il livello più avanzato di warehouse è denominato "stoccaggio e prelievo diretto". Per utilizzare lo stoccaggio e il prelievo diretti per un'ubicazione, attiva l'interruttore **Stoccaggio e prelievo diretti** nella pagina **Scheda ubicazione**.

### <a name="warehouse-flows"></a>Flussi di warehouse

* Flusso in entrata - Sposta gli articoli nell'ubicazione della warehouse e li rende disponibili, ad esempio gli acquisti e i trasferimenti in entrata.
* Flusso in uscita - Preleva e spedisci gli articoli ai clienti o ad altre ubicazioni.
* Flusso interno - Gestisci gli articoli all'interno di un'ubicazione. Ad esempio, sposti i componenti in produzione o esegui un conteggio dell'inventario fisico.

### <a name="basic-documents"></a>Documenti di base

I seguenti documenti vengono utilizzati nei flussi warehouse di base.

* Stoccaggio in magazzino
* Prelievi magazzino
* Movimento di magazzino
* Reg. Magazzino
* Registrazioni riclassificazione articolo

### <a name="advanced-documents"></a>Documenti avanzati

I seguenti documenti vengono utilizzati nei flussi warehouse avanzati.

* Carico warehouse
* Prospetto stoccaggi
* Stoccaggio warehouse
* Prospetto prelievi
* Prelievo warehouse
* Movimento worksheet
* Movimentazione warehouse
* Prelievi interni warehouse
* Stoccaggi interni warehouse
* Prospetto creaz. collocazione
* Prospetto creaz. cont. colloc.
* Registrazione degli articoli di warehouse
* Registrazioni della riclassificazione articoli warehouse

### <a name="pages-and-settings"></a>Pagine e impostazioni

Questa sezione descrive i concetti alla base delle pagine principali e delle impostazioni per la gestione della warehouse.

#### <a name="bins-and-bin-content"></a>Collocazioni e contenuto della collocazione

Una collocazione è un dispositivo di archiviazione progettato per contenere le parti di ricambio. È l'unità contenitore più piccola presente in [!INCLUDE[prod_short](includes/prod_short.md)]. Le quantità di articoli nelle collocazioni vengono denominate *contenuto collocazione*. Una ricerca dal campo **Articolo** oppure dal campo **Cod. collocazione** nella riga documenti correlata al warehouse visualizza la disponibilità calcolata dell'articolo nella collocazione.  

Il contenuto della collocazione può essere **Fisso**, **Dedicato**, o **Predefinito** per definire come può essere utilizzato il contenuto collocazione. Le collocazioni con nessuna di questi proprietà vengono denominato collocazioni *variabili*.  

Una collocazione fissa utilizza gli articoli assegnati al codice collocazione. La proprietà collocazione fissa assicura che anche se la collocazione viene svuotata, il contenuto non scompare. È possibile selezionare nuovamente la collocazione non appena il suo contenuto viene rifornito.  

Una collocazione dedicata utilizza il contenuto collocazione che può essere selezionato solo per la risorsa dedicata che utilizza la collocazione. Ad esempio, un centro lavoro. Altro contenuto non di prelievo, come le quantità in uscita in una registrazione di spedizione, può essere utilizzato da una collocazione dedicata. Solo il contenuto collocazione considerato dall'algoritmo **Crea prelievo** è protetto in una collocazione dedicata.  

[!INCLUDE [prod_short](includes/prod_short.md)] utilizza la proprietà della collocazione **Predefinito** per suggerire le collocazioni per le attività di warehouse. Nelle ubicazioni che utilizzano lo stoccaggio e il prelievo diretti, la proprietà di collocazione predefinita non viene utilizzata. Le ubicazioni in cui sono richieste le collocazioni, specifica dove posizionare gli articoli nei flussi in entrata. Nei flussi in uscita, la proprietà specifica da dove prelevare gli articoli.  

> [!NOTE]  
> Se gli articoli in uscita vengono collocati in più collocazioni, vengono prelevati prima gli articoli dalle collocazioni non predefinite, per svuotare il contenuto collocazione, e poi vengono prelevati gli articoli rimanenti dalla collocazione predefinita.  

Puoi avere solo una collocazione predefinita per articolo per ubicazione.  

#### <a name="bin-type"></a>Tipo collocazione

Le ubicazioni che utilizzano lo stoccaggio e il prelievo diretti possono utilizzare i tipi di collocazione. I tipi di collocazione controllano le attività consentite per una collocazione. Sono disponibili i seguenti tipi di collocazione:  

|Tipo collocazione|Descrizione|  
|------------------|---------------------------------------|  
|AREARICEV|Articoli ricevuti ma non stoccati.|  
|SHIP|Articoli prelevati in base alle righe di spedizione warehouse ma non registrati come spediti.|  
|PUT AWAY|In genere, articoli da archiviare in grandi unità di misura, ma a cui non vuoi accedere a scopo di prelievo. Queste collocazioni non vengono utilizzate per il prelievo, né per gli ordini di produzione né per le spedizioni, pertanto il loro utilizzo potrebbe essere limitato. Questo tipo di collocazione è utile quando acquisti una grande quantità di articoli. Le collocazioni devono sempre avere una valutazione di collocazione bassa, in modo che gli articoli con collocazioni PUTPICK con valutazione superiore vengano stoccati per primi. Rifornisci regolarmente questo tipo di collocazione in modo che i relativi articoli siano disponibili nelle collocazioni di tipo PUTPICK o PICK.|  
|PRELIEVO|Articoli da utilizzare solo per il prelievo. Il rifornimento di queste collocazioni può essere eseguito solo tramite spostamento e non tramite stoccaggio.|  
|PUTPICK|Articoli nelle collocazioni suggerite per stoccaggi e prelievi. Collocazioni di questo tipo hanno presumibilmente valutazioni differenti. Imposta le collocazioni di immagazzinamento di massa come collocazioni con valutazioni più basse rispetto alle collocazioni di prelievo ordinarie o alle collocazioni di prelievo nelle aree di prelievo in sequenza da inizio ordine.|  
|QC|Questa collocazione viene utilizzata per le rettifiche di magazzino, se la si specifica nel campo **Codice collocazione rettifica** della scheda Ubicazione. È inoltre possibile impostare collocazioni di questo tipo per gli articoli difettosi e gli articoli che vengono controllati. È possibile spostare articoli in collocazioni di questo tipo se si desidera renderli inaccessibili al normale flusso degli articoli. **Nota:** a differenza di tutti gli altri tipi di collocazione, il tipo di collocazione **CQ** non dispone di alcuna delle caselle di controllo per la gestione degli articoli selezionate per default. I contenuti inseriti in una collocazione QC sono esclusi dai flussi degli articoli.|  

Ad eccezione dei tipi di collocazione PICK, PUTPICK e PUTAWAY, il tipo di collocazione definisce l'attività consentita per una collocazione. Ad esempio, una collocazione di tipo RECEIVE può essere utilizzata solo per ricevere gli articoli o per prelevare gli articoli.  

> [!NOTE]  
> È necessario utilizzare i movimenti per spostare gli articoli nelle collocazioni RECEIVE e QC. Utilizza i movimenti per spostare gli articoli dalle collocazioni SHIP e QC.  

#### <a name="bin-ranking"></a>Valutazione collocazione

Nella gestione avanzata della warehouse, è possibile automatizzare e ottimizzare il modo in cui gli articoli vengono raccolti nei prospetti di prelievo e stoccaggio in base alla valutazione collocazione. Gli articoli vengono suggeriti per prelievi o stoccaggi in base alla valutazione collocazione.

I processi di stoccaggio vengono ottimizzati in base alla valutazione collocazione suggerendo le collocazioni con valutazione più elevata prima delle collocazioni con valutazione bassa. I processi di prelievo suggeriscono innanzitutto articoli del contenuto collocazione con valutazione collocazione alta. I rifornimenti collocazione suggeriscono prima le collocazioni con valutazione più bassa e poi con quella più alta.  

Valutazione collocazione e contenuto collocazione sono le proprietà di base che guidano i dipendenti della warehouse.  

#### <a name="bin-setup"></a>Impostazione della collocazione

Nella gestione warehouse avanzata, è possibile specificare i seguenti valori di capacità per controllare come e in quali collocazioni si immagazzinano gli articoli:

* Quantità
* Cubatura totale
* Peso  

È possibile assegnare un'unità di misura di base agli articoli. Un'unità di misura di base può essere costituita da pezzi, pallet, litri, grammi o scatole. Puoi anche creare unità di misura più grandi in base alla tua unità di misura di base. Ad esempio, se i pezzi sono l'unità di misura base, un pallet potrebbe equivalere a 16 pezzi.  

Se un articolo ha più di un'unità di misura, imposta la quantità massima per ogni unità di misura nella scheda articolo. Se un articolo è stato impostato per essere gestito in pezzi e pallet, anche il campo **Qtà massima** nella pagina **Contenuto collocazione** per tale articolo deve essere espresso in pezzi e pallet. In caso contrario, la quantità consentita per la collocazione non viene calcolata correttamente.  

Prima di impostare le restrizioni alla capacità per i contenuti della collocazione in una collocazione, assicurati che le unità di misura e le dimensioni dell'articolo siano stati impostati nell'articolo.  

> [!NOTE]  
> È possibile utilizzare più unità di misura solo nelle ubicazioni che utilizzano lo stoccaggio e il prelievo diretti. In tutte le altre configurazioni puoi usare il contenuto collocazione solo nell'unità di misura di base. In tutte le transazioni con una unità di misura superiore a quella di base dell'articolo, la quantità viene convertita nell'unità di misura di base.  

#### <a name="zone"></a>Area

Nella gestione avanzata della warehouse, le collocazioni possono essere raggruppate in zone per gestire la conduzione del flusso di lavoro delle attività di warehouse per le ubicazioni.  

Un'area potrebbe essere un'area ricevimento o di approvvigionamento e ogni area può essere costituita da una o più collocazioni.  

La maggior parte delle proprietà assegnate a una zona è assegnata alle collocazioni create per la zona.  

#### <a name="warehouse-class"></a>Classe warehouse

Nella gestione avanzata della warehouse, è possibile assegnare codici classe warehouse alle seguenti entità: 

* Articoli
* Collocazioni
* Zone

Le classi warehouse controllano dove immagazzinare gli articoli. È possibile suddividere una zona in diverse classi warehouse. Ad esempio, puoi immagazzinare gli articoli nella zona di ricezione come bloccati, pericolosi o un'altra classe.

Quando si utilizzano le classi warehouse e una collocazione di carico o di spedizione predefinita, devi scegliere manualmente le collocazioni appropriate nelle righe di carico e di spedizione warehouse.  

Nei flussi in entrata, il codice di classe è evidenziato solo nelle righe in entrata dove il codice di classe dell'articolo non corrisponde alla collocazione di carico predefinita. Se le collocazioni predefinite corrette non sono assegnate, la quantità non può essere caricata.  

#### <a name="location"></a>Ubicazione

Un'ubicazione è una struttura fisica o un luogo in cui le scorte vengono ricevute, immagazzinate e spedite. Un'ubicazione può essere una warehouse, un'auto di servizio, uno showroom, uno stabilimento o un'area di uno stabilimento. L'inventario è spesso organizzato in collocazioni e zone.

#### <a name="first-expired-first-out"></a>FEFO (First Expired First Out)

Se si seleziona la casella di controllo **Prelievo in base a FEFO** nella Scheda dettaglio **Criteri per collocazione** nella pagina **Scheda ubicazione**, gli articoli tracciati vengono prelevati nell'ubicazione in base alla data di scadenza. Gli articoli con le date di scadenza meno recenti vengono prelevati per primi.  

Le attività di warehouse in tutti i documenti di spostamento e prelievo sono ordinate secondo il metodo FEFO, a meno che gli articoli non dispongano di numeri seriali o di lotto assegnati. Se solo una parte della quantità della riga è definita con numeri seriali o di lotto, la quantità rimanente da prelevare viene ordinata secondo il metodo FEFO.  

Quando si effettuano prelievi tramite il metodo FEFO, gli articoli la cui scadenza è più imminente vengono raccolti in una lista di tracciabilità articolo temporanea basata sulla data di scadenza. Se due articoli hanno la stessa data di scadenza, viene selezionato automaticamente quello con il numero di lotto o seriale inferiore. Se i numeri di lotto o seriale sono identici, viene selezionato automaticamente l'articolo registrato per primo. Alla lista di tracciabilità articolo FEFO temporanea vengono applicati i criteri standard relativi alla selezione degli articoli nella collocazione, ad esempio Valutazione collocazione e Breakbulk.  

#### <a name="put-away-template"></a>Modello stoccaggio

Il modello di stoccaggio specifica un set di regole in ordine di priorità che si applicano quando crei gli stoccaggi. Ad esempio, un modello di stoccaggio può richiedere di posizionare gli articoli in una collocazione con contenuto collocazione con la stessa unità di misura. Se non è possibile trovare una collocazione simile con una capacità sufficiente, l'articolo deve essere collocato in una collocazione vuota. Assegni il modello di stoccaggio a un articolo e a un'ubicazione.  

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Vedere anche

[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
