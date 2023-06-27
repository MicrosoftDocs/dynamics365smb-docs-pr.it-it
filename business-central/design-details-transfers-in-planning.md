---
title: Dettagli di progettazione - Trasferimenti nella pianificazione
description: Scopri come utilizzare gli ordini di trasferimento come origine di approvvigionamento quando si pianificano i livelli di magazzino.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# <a name="design-details-transfers-in-planning"></a>Dettagli di progettazione: Trasferimenti nella pianificazione

Gli ordini di trasferimento sono anche un'origine di approvvigionamento quando si lavora a livello di stockkeeping. Se si utilizzano più ubicazioni (warehouse), il sistema di rifornimento della USK può essere impostato su Trasferimento, implicando che l'ubicazione sia rifornita trasferendo le merci da un'altra ubicazione. In una situazione con più warehouse potresti avere una catena di trasferimenti. L'approvvigionamento all'ubicazione VERDE è stata trasferita dall'ubicazione GIALLA, l'approvvigionamento all'ubicazione GIALLA è trasferito dall'ubicazione ROSSA, e così via. All'inizio della catena, è presente un sistema di rifornimento di **Ordine di produzione** o **di acquisto**.  

![Esempio di flusso di trasferimento.](media/nav_app_supply_planning_7_transfers1.png "Esempio di flusso di trasferimento")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Se confronti le seguenti situazioni, è chiaro che l'attività di pianificazione in quest'ultimo può diventare complessa:

* Un ordine di approvvigionamento corrisponde direttamente a un ordine di domanda
* Un ordine cliente viene fornito tramite una catena di trasferimenti SKU

Se la domanda cambia, potrebbe causare un effetto onda lungo la catena. Tutti gli ordini di trasferimento, oltre all'ordine di acquisto e di produzione all'estremità opposta della catena, dovranno essere aggiornati per riequilibrare domanda e offerta.  

![Esempio di saldo tra approvvigionamento e domanda nei trasferimenti.](media/nav_app_supply_planning_7_transfers2.png "Esempio di saldo tra approvvigionamento e domanda nei trasferimenti")  

## <a name="why-is-a-transfer-a-special-case"></a>Perché il trasferimento è un caso speciale?

Gli ordini di trasferimento sono simili ad altri ordini, come gli ordini di acquisto e di produzione. Tuttavia sono diversi.  

Una differenza è che una riga trasferimento rappresenta sia la domanda che l'offerta. La parte in uscita che viene spedita è la domanda. La parte in entrata che viene ricevuta presso la nuova ubicazione, è l'approvvigionamento in tale ubicazione.  

![Contenuto della pagina Ordine di trasferimento.](media/nav_app_supply_planning_7_transfers3.png "Contenuto della pagina Ordine di trasferimento")  

Quando [!INCLUDE [prod_short](includes/prod_short.md)] cambia il lato approvvigionamento del trasferimento, deve apportare una modifica simile sul lato domanda.  

## <a name="transfers-are-dependent-demand"></a>I trasferimenti dipendono dalla domanda

La relazione tra domanda e offerta è simile ai componenti nelle righe ordine di produzione. La differenza è che i componenti nelle righe ordine di produzione si trovano al livello di pianificazione successivo e hanno un articolo diverso. Le due parti del trasferimento sono allo stesso livello per lo stesso articolo.  

Una similarità importante è che i componenti e i trasferimenti dipendono dalla domanda. La domanda da una riga trasferimento è dettata dal lato dell'offerta del trasferimento. Se l'offerta cambia, la domanda ne è direttamente interessata.

A meno che la flessibilità di pianificazione sia impostata su Nessuna, una riga di trasferimento non deve mai essere considerata come una domanda indipendente nella pianificazione.  

Nella procedura di pianificazione, la domanda di trasferimento deve essere considerata soltanto dopo che il sistema di pianificazione ha elaborato il lato di approvvigionamento. Prima che avvenga l'elaborazione, la domanda effettiva non è nota. La sequenza delle modifiche è importante per gli ordini di trasferimento.  

## <a name="planning-sequence"></a>Sequenza di pianificazione

L'immagine seguente mostra un esempio di stringa di trasferimento.  

![Esempio di flusso di trasferimento semplice.](media/nav_app_supply_planning_7_transfers4.png "Esempio di flusso di trasferimento semplice")  

In questo esempio, un cliente ordina l'articolo presso l'ubicazione VERDE. L'ubicazione VERDE viene rifornita attraverso il trasferimento dalla warehouse centrale ROSSA. La warehouse centrale ROSSA viene approvvigionata tramite il trasferimento dalla produzione nell'ubicazione BLU.  

In questo esempio, il sistema di pianificazione inizia alla domanda del cliente e risale la catena. Le domande e le offerte sono elaborate per un'ubicazione alla volta.  

![Pianificazione forniture con trasferimenti.](media/nav_app_supply_planning_7_transfers5.png "Pianificazione forniture con trasferimenti")  

## <a name="transfer-level-code"></a>Codice livello trasferimento

La sequenza in cui le ubicazioni vengono elaborate nel sistema di pianificazione è determinata dal codice del livello di trasferimento della SKU.  

Il codice del livello di trasferimento è un campo interno. Il campo viene calcolato e archiviato nella SKU quando crei o modifichi la SKU. Il calcolo viene eseguito su tutte le SKU per una data combinazione di articolo e variante articolo. Il calcolo utilizza il codice di ubicazione e il codice di origine trasferimento per determinare il percorso da utilizzare per le SKU. Il calcolo assicura che tutte le domande vengano elaborate.  

Il codice del livello di trasferimento sarà 0 per le unità di stockkeeping con ordine di produzione o di acquisto per il sistema di rifornimento e sarà -1 per il primo livello di trasferimento, -2 per il secondo e così via. Nell'esempio descritto nella sezione precedente, i livelli sono quindi -1 per ROSSO e -2 per VERDE, come indicato nella seguente illustrazione.  

![Contenuto della pagina Scheda SKU.](media/nav_app_supply_planning_7_transfers6.gif "Contenuto della pagina Scheda SKU")  

Per aggiornare la SKU, il sistema di pianificazione rileva se il sistema di approvvigionamento per le unità di stockkeeping ha riferimenti circolari.  

## <a name="planning-transfers-without-sku"></a>Pianificazione dei trasferimenti senza SKU

Per configurazioni warehouse meno avanzate, puoi utilizzare le ubicazioni ed effettuare trasferimenti manuali tra le ubicazioni, anche se non utilizzi le SKU. Ad esempio, il trasferimento potrebbe riguardare un ordine di vendita in tale ubicazione. Il sistema di pianificazione risponde alle modifiche nella domanda.  

Per i trasferimenti manuali, il sistema di pianificazione analizza gli ordini di trasferimento e pianifica l'ordine nel quale devono essere elaborate le ubicazioni. Internamente, il sistema di pianificazione usa con le SKU temporanee contenenti i codici a livello di trasferimento.  

![Codice livello trasferimento.](media/nav_app_supply_planning_7_transfers7.png "Codice livello trasferimento")  

Se esistono più trasferimenti a un'ubicazione, il primo ordine di trasferimento definisce la direzione di pianificazione. I trasferimenti nella direzione opposta vengono annullati.  

## <a name="changing-quantity-with-reservations"></a>Modificare la quantità con gli impegni

Quando si modificano le quantità di un approvvigionamento, il sistema di pianificazione tiene conto degli impegni. La quantità riservata rappresenta il limite inferiore di quanto ridurre l'approvvigionamento.  

Quando modifichi la quantità in una riga ordine di trasferimento, tieni presente il limite inferiore. Il limite inferiore è la quantità prenotata più alta delle righe di trasferimento in uscita e in entrata.

Ad esempio, una riga ordine di trasferimento di 117 pezzi è riservata per le seguenti righe:

* Una riga vendita di 46
* Una riga acquisto di 24

Anche se il lato in entrata potrebbe avere un approvvigionamento in eccesso, non è possibile ridurre la riga di trasferimento al di sotto di 46.  

![Prenotazioni nella pianificazione dei trasferimenti.](media/nav_app_supply_planning_7_transfers8.png "Prenotazioni nella pianificazione dei trasferimenti")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Modificare la quantità in una catena di trasferimento

Ecco un esempio di ciò che accade quando modifichi una quantità in una modifica di trasferimento.

Il punto di partenza è una situazione equilibrata con una catena di trasferimento che fornisce un ordine di vendita di 27 presso l'ubicazione ROSSA. C'è un ordine di acquisto corrispondente all'ubicazione BLU. Entrambi i trasferimenti passano attraverso l'ubicazione ROSA. Ci sono due ordini di trasferimento, BLU-ROSA e ROSA-ROSSO.  

![Modifica della quantità nella pianificazione del trasferimento 1.](media/nav_app_supply_planning_7_transfers9.png "Modifica della quantità nella pianificazione del trasferimento 1")  

A questo punto il responsabile della pianificazione presso l'ubicazione ROSA sceglie di impegnare per l'acquisto.  

![Modifica della quantità nella pianificazione del trasferimento 2.](media/nav_app_supply_planning_7_transfers10.png "Modifica della quantità nella pianificazione del trasferimento 2")  

In genere la prenotazione significa che il sistema di pianificazione ignora l'ordine di acquisto e la domanda di trasferimento. Non c'è problema finché c'è equilibrio. Ma cosa succede quando l'ubicazione ROSSA cambia l'ordine da 27 a 22?  

![Modifica della quantità nella pianificazione del trasferimento 3.](media/nav_app_supply_planning_7_transfers11.png "Modifica della quantità nella pianificazione del trasferimento 3")  

Quando il sistema di pianificazione viene eseguito nuovamente, deve liberarsi dell'approvvigionamento in eccesso. Tuttavia, l'impegno blocca l'acquisto e il trasferimento di una quantità pari a 27.  

![Modifica della quantità nella pianificazione del trasferimento 4.](media/nav_app_supply_planning_7_transfers12.png "Modifica della quantità nella pianificazione del trasferimento 4")  

Il trasferimento ROSA-ROSSO è stato ridotto a 22. La parte in entrata del trasferimento BLU-ROSA non è riservata, ma la parte in uscita lo è. La prenotazione comporta l'impossibilità di ridurre la quantità al di sotto di 27.  

## <a name="lead-time-calculation"></a>Calcolo del lead time

Nel calcolo della data di scadenza di un ordine di trasferimento vengono presi in considerazione diversi tipi di lead time.  

I seguenti lead time sono attivi durante la pianificazione di un ordine di trasferimento:  

* Tempo di gestione uscita dalla warehouse  
* Durata spedizione  
* Tempo di gestione entrata nella warehouse  

Nella riga di pianificazione vengono utilizzati i seguenti campi per fornire informazioni sul calcolo:  

* Data spedizione trasferimento  
* Data di inizio  
* Data di fine  
* Data di scadenza  

La data di spedizione della riga di trasferimento viene visualizzata nel campo **Data spedizione trasferimento**. La data di carico della riga di trasferimento viene visualizzata nel campo **Data di scadenza**.  

Le date di inizio e di fine descrivono il periodo di trasporto effettivo.  

Nell'immagine seguente viene mostrata l'interpretazione delle data e ora di inizio e data e ora di fine nelle righe di pianificazione per ordini di trasferimento.  

![Data e ora di Central nella pianificazione del trasferimento.](media/nav_app_supply_planning_7_transfers13.png "Data e ora di Central nella pianificazione del trasferimento")  

L'esempio mostra i seguenti calcoli:  

* Data spedizione + Gestione in uscita = Data Inizio  
* Data inizio + Durata spedizione = Data fine  
* Data Fine + Gest. Entrata = Data Carico  

## <a name="safety-lead-time"></a>Lead time di sicurezza

Il campo **Lead time di sicurezza predefinito** nella pagina **Setup produzione** e il campo **Lead time di sicurezza** correlato della pagina **Scheda articolo** non verranno considerati nel calcolo di un ordine di trasferimento. Tuttavia, il lead time di sicurezza influenza il piano totale. Il lead time di sicurezza influisce sull'ordine di approvvigionamento (acquisto o produzione) all'inizio della catena di trasferimento. Questo è il punto in cui gli articoli sono stati collocati nell'ubicazione da cui verranno trasferiti.  

![Elementi della data di scadenza del trasferimento.](media/nav_app_supply_planning_7_transfers14.png "Elementi della data di scadenza del trasferimento")  

Nella riga dell'ordine di produzione, la Data Fine + Lead Time di Sicurezza + Tempo Gest. Entrata in Whse. = Data Scadenza.  

Nella riga dell'ordine di acquisto, la Data Carico Pianificato + Lead Time di Sicurezza + Tempo Gest. Entrata in Whse. = Data Carico Prevista.  

## <a name="reschedule"></a>Ripianifica

Nella riprogrammazione di una riga di trasferimento, il sistema di pianificazione trova la parte in uscita e modifica la data e l'ora.

> [!NOTE]
> Se un lead time è definito, si verificherà un vuoto tra la spedizione e il carico. Il lead time può essere costituito da più elementi, ad esempio il tempo di trasporto e il tempo di gestione warehouse. In un asse temporale, il sistema di pianificazione si sposta indietro nel tempo durante il calcolo del saldo degli elementi.  

![Modifica della data di scadenza nella pianificazione del trasferimento.](media/nav_app_supply_planning_7_transfers15.png "Modifica della data di scadenza nella pianificazione del trasferimento")  

Quando si modifica la data di scadenza in una riga di trasferimento, è necessario calcolare il lead time per aggiornare il lato in uscita del trasferimento.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a>Numeri seriali e di lotto nelle catene di trasferimento

Se la domanda usa numeri seriali o di lotto e il motore di pianificazione è in esecuzione, verranno creati gli ordini di trasferimento. Per ulteriori informazioni su questo concetto, vedere gli attributi dell'articolo. Se, tuttavia, i numeri seriali o di lotto vengono rimossi dalla domanda, gli ordini di trasferimento usano ancora i numeri seriali o di lotto e pertanto verranno trascurati dalla pianificazione (non eliminati).  

## <a name="order-to-order-links"></a>Collegamenti ordine su ordine

In questo esempio, la SKU BLU è impostata con un criterio di riordino **Ordine**. Le SKU ROSA e ROSSA hanno il criterio di riordino **lotto per lotto**. La creazione di un ordine cliente per 27 nell'ubicazione ROSSA comporta una catena di trasferimenti. L'ultimo trasferimento è nell'ubicazione BLU, ed è riservato con l'associazione. In questo esempio, gli impegni non sono impegni imposti dal responsabile della pianificazione presso l'ubicazione ROSA. Il sistema di pianificazione crea le associazioni. La differenza importante è che il sistema di pianificazione può modificare l'ultimo.  

![Collegamenti ordine su ordine nella pianificazione del trasferimento.](media/nav_app_supply_planning_7_transfers16.png "Collegamenti ordine su ordine nella pianificazione del trasferimento")  

Se la domanda viene modificata da 27 a 22, il sistema di pianificazione abbasserà la quantità lungo la catena. Anche l'impegno dell'associazione è ridotto.  

## <a name="see-also"></a>Vedere anche

[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Pianificazione con o senza ubicazioni](production-planning-with-without-locations.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
