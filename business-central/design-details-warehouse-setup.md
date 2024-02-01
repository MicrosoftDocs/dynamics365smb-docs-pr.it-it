---
title: Dettagli di progettazione - Impostazione warehouse
description: 'La funzionalità Warehouse contiene diversi livelli di complessità, che sono in gran parte definiti dall''impostazione della collocazione nelle schede ubicazione.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-warehouse-setup"></a>Dettagli di progettazione: Impostazione warehouse

La funzionalità di warehouse in [!INCLUDE[prod_short](includes/prod_short.md)] contiene livelli diversi di complessità, che sono definiti dalle autorizzazioni di licenza nelle funzionalità offerte. Il livello di complessità in una soluzione warehouse è in gran parte definito dall'impostazione di collocazione nelle schede ubicazione, che a sua volta viene controllata dalla licenza perché l'accesso ai campi dell'impostazione di collocazione è definito dalla licenza. Inoltre, gli oggetti applicazione della licenza controllano quale documento dell'interfaccia utente utilizzare per le attività di warehouse supportate.  
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

Nella seguente tabella viene indicato quali funzionalità sono richieste per definire i livelli di complessità della warehouse, quali documenti dell'interfaccia utente supportano ogni livello e quali codici ubicazione riflettono questi livelli nel database di esempio di [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

|Livello di complessità|Descrizione|Documento IU|Posizione di esempio|Requisito minimo dell'area|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Nessuna attività di warehouse dedicata.<br /><br /> Registrazione carico/spedizione da ordini.|Ordine|BLU|Magazzino di base|  
|2|Nessuna attività di warehouse dedicata.<br /><br /> Registrazione carico/spedizione da ordini.<br /><br /> Il codice collocazione è obbligatorio.|Ordine, con codice collocazione|ARGENTO|Magazzino di base/Collocazione|  
|3 <br /><br /> **NOTA**: anche se le impostazioni sono definite **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile registrare carichi e spedizioni direttamente dai documenti commerciali di origine nelle ubicazioni in cui si selezionano queste caselle di controllo.|Attività warehouse di base, ordine per ordine.<br /><br /> Registrazione carico/spedizione da documenti di prelievo/stoccaggio in magazzino. <br /><br /> Il codice collocazione è obbligatorio.|Stoccaggio magazzino/Movimento di magazzino/Prelievo magazzino, con codice collocazione|(ARGENTO + Richiesto stoccaggio o Richiesto stoccaggio)|Magazzino di base/Collocazione/Stoccaggio/Prelievo|  
|4|Attività warehouse avanzate, per ordini multipli.<br /><br /> Registrazione di ricezione e spedizione consolidata basata sullo stoccaggio warehouse e le registrazioni di prelievo.|Carico warehouse, stoccaggio warehouse, prelievo warehouse, spedizione warehouse, prospetto prelievi|VERDE|Magazzino di base/Carico warehouse/Stoccaggio/Prelievo/Spedizione warehouse|  
|5|Attività warehouse avanzate, per ordini multipli.<br /><br /> Registrazione di ricezione e spedizione consolidata basata sullo stoccaggio warehouse e le registrazioni di prelievo.<br /><br /> Il codice collocazione è obbligatorio.|Carico warehouse, stoccaggio warehouse, prelievo warehouse, spedizione warehouse, prospetto prelievi, prospetto stoccaggi, con codice collocazione|(VERDE + Collocazione obbligatoria)|Magazzino di base/Collocazione/Carico warehouse/Stoccaggio/Prelievo/Spedizione warehouse|  
|6 <br /><br /> **Nota**: questo livello viene definito "WMS" poiché richiede la funzionalità più avanzata, Sistema di gestione warehouse (Warehouse Management Systems).|Attività warehouse avanzate, per ordini multipli<br /><br /> Registrazione di ricezione e spedizione consolidata basata sullo stoccaggio warehouse e le registrazioni di prelievo<br /><br /> Il codice collocazione è obbligatorio.<br /><br /> Il codice della zona e il codice di classe sono facoltativi.<br /><br /> Addetti warehouse diretti dal flusso di lavoro<br /><br /> Pianificazione rifornimento collocazione<br /><br /> Valutazione collocazione<br /><br /> Impostazione collocazione per capacità<br /><br /> Suddivisione in fasce orarie  <!-- Hand-held device integration -->|Carico warehouse, Stoccaggio warehouse, Prelievo warehouse, Spedizione warehouse, Movimentazione warehouse, Prospetto prelievi, Prospetto stoccaggi, Prelievo interno warehouse, Stoccaggio warehouse interno con codice collocazione/classe/area<br /><br /> Prospetti vari per la gestione delle collocazioni<br /><br /> Video ADCS|BIANCO|Magazzino di base/Collocazione/Stoccaggio/Carico warehouse/Prelievo/Spedizione warehouse/Sistemi di gestione warehouse/Prelievi e stoccaggi interni/Impostazione di collocazione/Sistema di acquisizione data automatizzata/Impostazione collocazione/<!-- Automated Data Capture System/ -->Impostazione della collocazione|  

Per esempi dell'utilizzo dei documenti IU in base al livello di complessità della warehouse, vedere [Dettagli di progettazione: Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).  

## <a name="bin-and-bin-content"></a>Collocazione e Contenuto collocazione

Una collocazione è un dispositivo di archiviazione progettato per contenere le parti di ricambio. È l'unità contenitore più piccola presente in [!INCLUDE[prod_short](includes/prod_short.md)]. Le quantità di articoli nelle collocazioni vengono denominate contenuto collocazione. Una ricerca dal campo **Articolo** oppure dal campo **Cod. collocazione** nella riga documenti correlata al warehouse visualizza la disponibilità calcolata dell'articolo nella collocazione.  

Al contenuto della collocazione può essere associata una proprietà Fissa, Dedicata o Predefinita per definire come può essere utilizzato il contenuto collocazione. Le collocazioni con nessuna di questi proprietà vengono denominato collocazioni variabili.  

Una collocazione fissa utilizza gli articoli assegnati al codice collocazione in questione. La proprietà della collocazione fissa garantisce che, anche se momentaneamente svuotato, il contenuto collocazione non scompaia e che la collocazione venga quindi nuovamente selezionata non appena viene rifornita.  

Una collocazione dedicata utilizza il contenuto collocazione che può essere selezionato solo per la risorsa dedicata, ad esempio un centro lavoro, che utilizza la collocazione in questione. Altro contenuto non di prelievo, come le quantità in uscita in una registrazione di spedizione, può ancora essere utilizzato da una collocazione dedicata. Solo il contenuto collocazione considerato dall'algoritmo **Crea prelievo** è protetto in una collocazione dedicata.  

La proprietà della collocazione predefinita viene utilizzata dal sistema per suggerire le collocazioni per le attività di warehouse. Nelle ubicazioni WMS, la proprietà di collocazione predefinita non viene utilizzata. Le ubicazioni in cui sono richieste le collocazioni, la proprietà viene utilizzata nei flussi in entrata per specificare dove posizionare gli articoli. Nei flussi in uscita, la proprietà viene utilizzata per specificare da dove prelevare gli articoli.  

> [!NOTE]  
>  Se gli articoli in uscita vengono collocati in più collocazioni, vengono prelevati prima gli articoli dalle collocazioni non predefinite, per svuotare il contenuto collocazione, e poi vengono prelevati gli articoli rimanenti dalla collocazione predefinita.  

Potrebbe esserci solo una collocazione predefinita per articolo per ubicazione.  

## <a name="bin-type"></a>Tipo collocazione

Nelle installazioni WMS è possibile limitare le attività di warehouse consentite per una collocazione assegnando un tipo di collocazione. Sono disponibili i seguenti tipi di collocazione:  

|Tipo collocazione|Descrizione|  
|------------------|---------------------------------------|  
|AREARICEV|Articoli registrati come ricevuti ma non ancora stoccati.|  
|SPED|Articoli prelevati in base alle righe di spedizione warehouse ma non ancora registrati come spediti.|  
|PUT AWAY|In genere, articoli da archiviare in grandi unità di misura, ma a cui non si desidera accedere a scopo di prelievo. Poiché le collocazioni non vengono utilizzate per il prelievo, per gli ordini di produzione o per le spedizioni, l'utilizzo di una collocazione di tipo stoccaggio può essere limitato, ma questo tipo di collocazione può essere utile nel caso in cui venga acquistato un notevole quantitativo di articoli. Si consiglia di assegnare sempre a collocazioni di questo tipo una valutazione di collocazione bassa in modo che, quando gli articoli ricevuti vengono stoccati, vengano stoccate per prime altre collocazioni di tipo PUTPICK con valutazione più alta associate in modo fisso a tali articoli. Se si utilizza questo tipo di collocazione, sarà necessario eseguire periodicamente il rifornimento delle collocazioni in modo che gli articoli immagazzinati nelle collocazioni di questo tipo siano anche disponibili nelle collocazioni di tipo PUTPICK o PICK.|  
|PICK|Articoli da utilizzare solo per il prelievo. Il rifornimento di queste collocazioni può essere eseguito solo tramite spostamento, non tramite stoccaggio.|  
|PUTPICK|Articoli nelle collocazioni suggerite per le funzioni di stoccaggio e di prelievo. Collocazioni di questo tipo hanno presumibilmente valutazioni differenti. È possibile impostare le collocazioni di immagazzinamento a massa come collocazioni di questo tipo con valutazioni basse rispetto alle collocazioni di prelievo ordinarie o alle collocazioni di prelievo in sequenza da inizio ordine.|  
|QC|Questa collocazione viene utilizzata per le rettifiche di magazzino, se la si specifica nel campo **Codice collocazione rettifica** della scheda Ubicazione. È inoltre possibile impostare collocazioni di questo tipo per gli articoli difettosi e gli articoli che vengono controllati. È possibile spostare articoli in collocazioni di questo tipo se si desidera renderli inaccessibili al normale flusso degli articoli. **Nota:**  a differenza di tutti gli altri tipi di collocazione, il tipo di collocazione **CQ** non dispone di alcuna delle caselle di controllo per la gestione degli articoli selezionate per default. Ciò indica che tutti i contenuti inseriti in una collocazione QC sono esclusi dai flussi degli articoli.|  

Per tutti i tipi di collocazione, ad eccezione della PICK, PUTPICK e PUTAWAY, non è consentita nessun'altra attività per la collocazione se non quella definita dal tipo di collocazione. Ad esempio, una collocazione di tipo **Ricevi** può essere utilizzata solo per ricevere gli articoli o per prelevare gli articoli.  

> [!NOTE]  
> Solo il movimento può essere effettuato in collocazioni di tipo RICEVI e CQ. Analogamente, è possibile effettuare solo spostamenti dalle collocazioni di tipo SPED e CQ.  

## <a name="bin-ranking"></a>Valutazione collocazione

Nella gestione avanzata della warehouse, è possibile automatizzare e ottimizzare il modo in cui gli articoli vengono raccolti nei prospetti di prelievo e stoccaggio valutando le collocazioni in modo che gli articoli vengano suggeriti come prelevati o stoccati in base ai criteri di valutazione al fine di ottimizzare lo spazio della warehouse.  

I processi di stoccaggio vengono ottimizzati in base alla valutazione collocazione suggerendo le collocazioni con valutazione più elevata prima delle collocazioni con valutazione bassa. Analogamente, i processi di prelievo vengono ottimizzati suggerendo innanzitutto articoli del contenuto collocazione con valutazione collocazione alta. Inoltre, i rifornimenti collocazione vengono suggeriti dalle collocazioni con valutazione più bassa alle collocazioni con valutazione più elevata.  

La valutazione della collocazione con le informazioni del contenuto collocazione rappresentano le proprietà di base che consentono agli utenti di suddividere in fasce orarie gli articoli nella warehouse.  

## <a name="bin-setup"></a>Impostazione della collocazione
Nella gestione avanzata della warehouse, le collocazioni possono essere impostate con valori di capacità, ad esempio la quantità, la cubatura totale e il peso, per controllare quali articoli sono memorizzati nella collocazione e in che modo.  

In ciascuna scheda articolo è possibile assegnare un'unità di misura (UDM) per l'articolo, ad esempio pezzi, pallet, litri, grammi o scatole. È inoltre possibile avere una UDM di base per un articolo e specificare UDM maggiori basate sull'UDM di base. Ad esempio, è possibile definire un pallet di 16 pezzi, e l'ultima è la UDM di base.  

Se si desidera impostare una quantità massima di un articolo specifico da archiviare in una singola collocazione e l'articolo ha più di una UDM, è necessario impostare la quantità massima per ogni UDM presente nella scheda articolo. Di conseguenza, se un articolo è stato impostato per essere gestito in pezzi e pallet, anche il campo **Qtà massima** nella pagina **Contenuto collocazione** per tale articolo deve essere espresso in pezzi e pallet. In caso contrario, la quantità consentita per la collocazione non viene calcolata correttamente.  

Prima di impostare le restrizioni alla capacità per i contenuti della collocazione in una collocazione, è necessario innanzitutto assicurarsi che i UDM e le dimensioni dell'articolo siano stati impostati nella scheda articolo.  

> [!NOTE]  
> È possibile solo utilizzare più UDM nelle installazioni WMS. In tutte le altre configurazioni il contenuto collocazione può essere solo nell'unità di misura di base. In tutte le transazioni con una UDM superiore alla UDM di base dell'articolo, la quantità viene convertita nella UDM di base.  

## <a name="zone"></a>Area

Nella gestione avanzata della warehouse, le collocazioni possono essere raggruppate in zone per gestire la conduzione del flusso di lavoro delle attività di warehouse.  

Un'area potrebbe essere un'area ricevimento o di approvvigionamento e ogni area può essere costituita da una o più collocazioni.  

La maggior parte delle proprietà assegnate a una zona sarà assegnata per impostazione predefinita alla collocazione creata da quella specifica zona.  

## <a name="class"></a>Classe
Nella gestione avanzata della warehouse, è possibile assegnare codici di classe warehouse ad articoli, collocazioni e zone per controllare dove vengono archiviate le classi degli articoli, ad esempio le merci bloccate. È possibile suddividere una zona in diverse classi warehouse. Ad esempio, gli articoli nella zona di ricezione possono essere memorizzati come bloccati, pericolosi o un'altra classe.  

Quando si utilizzano le classi warehouse e una collocazione di carico o di spedizione predefinita, è necessario compilare manualmente le collocazioni appropriate nelle righe di carico e di spedizione warehouse.  

Nei flussi in entrata, il codice di classe è evidenziato solo nelle righe in entrata dove il codice di classe dell'articolo non corrisponde alla collocazione di carico predefinita. Se le collocazioni predefinite corrette non sono assegnate, la quantità non può essere caricata.  

## <a name="location"></a>Ubicazione

Un'ubicazione è una struttura fisica o un'area in cui viene ricevuta, archiviata e spedita la giacenza, potenzialmente organizzata nelle collocazioni. Un'ubicazione può essere un warehouse, un auto assistenza, una sala esposizione, un impianto o un'area in un impianto.  

## <a name="first-expired-first-out"></a>FEFO (First Expired First Out)

Se si seleziona la casella di controllo **Prelievo in base a FEFO** nella Scheda dettaglio **Criteri per collocazione** nella scheda ubicazione, gli articoli tracciati vengono prelevati in base alla data di scadenza. Gli articoli con le date di scadenza meno recenti vengono prelevati per primi.  

Le attività di warehouse in tutti i documenti di spostamento e prelievo sono ordinate secondo il metodo FEFO, a meno che gli articoli in questione non dispongano già di numeri seriali o di lotto assegnati. Se solo una parte della quantità della riga è già definita con numeri seriali o di lotto, la quantità rimanente da prelevare verrà ordinata secondo il metodo FEFO.  

Quando si effettuano prelievi tramite il metodo FEFO, gli articoli disponibili la cui scadenza è più imminente vengono raccolti in una lista di tracciabilità articolo temporanea basata sulla data di scadenza. Se due articoli hanno la stessa data di scadenza, viene selezionato automaticamente quello con il numero di lotto o seriale inferiore. Se i numeri di lotto o seriale sono identici, viene selezionato automaticamente l'articolo registrato per primo. Alla lista di tracciabilità articolo FEFO temporanea vengono applicati i criteri standard relativi alla selezione degli articoli nella collocazione, ad esempio Valutazione collocazione e Breakbulk.  

## <a name="put-away-template"></a>Modello stoccaggio

Il modello di stoccaggio può essere assegnato a un articolo e a un'ubicazione. Il modello di stoccaggio specifica un set di regole in ordine di priorità che devono essere rispettate quando si creano gli stoccaggi. Ad esempio, un modello di stoccaggio può richiedere che l'articolo sia posizionato nella collocazione con il contenuto della collocazione corrispondente a UDM e se non è possibile trovare una simile collocazione con abbastanza capacità, allora l'articolo deve essere posizionato in una collocazione vuota.  

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Dettagli di progettazione: disponibilità nella warehouse](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
