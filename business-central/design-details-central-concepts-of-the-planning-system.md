---
title: 'Dettagli di progettazione: Concetti centrali del sistema di pianificazione'
description: La pianificazione suggerisce all'utente le azioni da intraprendere in base alla situazione della domanda/offerta e ai parametri di pianificazione degli articoli.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Dettagli di progettazione: Concetti centrali del sistema di pianificazione

Le funzioni di pianificazione sono contenute in un processo batch che seleziona innanzitutto articoli rilevanti e il periodo per la pianificazione. Quindi, in base al codice di basso livello di ciascun articolo (posizione DBA), il processo batch chiama un'unità di codice che calcola un piano di approvvigionamento. L'unità di codice bilancia gli insiemi di domanda e offerta e suggerisce le azioni da intraprendere all'utente. Le azioni suggerite vengono visualizzate come righe nel prospetto di pianificazione o nella richiesta di approvvigionamento.  

![Contenuto della pagina Prospetti pianificazione.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Contenuto della pagina Prospetti pianificazione")  

Supponi che il responsabile della pianificazione della società, ad esempio un addetto acquisti o un responsabile della pianificazione di produzione, sia l'utente del sistema di pianificazione. Il sistema di pianificazione aiuta l'utente eseguendo calcoli complessi ma chiari di un piano. L'utente può quindi concentrarsi sulla soluzione i problemi di più difficili, ad esempio quando si verificano delle situazioni insolite.  

Il sistema di pianificazione si basa sulla domanda prevista ed effettiva da parte dei clienti, ad esempio la previsione e gli ordini di vendita. I calcoli di pianificazione suggeriscono le azioni che puoi intraprendere in merito all'approvvigionamento da fornitori, assemblaggio o produzione o ai trasferimenti da altri magazzini. Un esempio di azione suggerita può servire a creare nuovi ordini di approvvigionamento, ad esempio gli ordini di acquisto o di produzione. Se sono già presenti ordini di approvvigionamento, le azioni suggerite possono consistere nell'aumento o nell'accelerazione degli ordini per rispondere alle modifiche nella domanda.  

Un altro obiettivo del sistema di pianificazione consiste nel garantire che il magazzino non aumenti in modo superfluo. Nel caso di un calo della domanda, il sistema di pianificazione suggerirà all'utente di rimandare, ridurre in quantità o annullare gli ordini di approvvigionamento esistenti.  

Un'unità di codice contiene la logica di pianificazione e le seguenti funzioni:

* MRP e MPS
* Calcola piano - Solo cambiamenti
* Calcola piano - Rigenerativo

Tuttavia, il calcolo del piano di approvvigionamento implica sottosistemi diversi.  

Il sistema di pianificazione non include la logica dedicata per il livellamento delle capacità o la programmazione accurata. Questi lavori di programmazione vengono eseguiti separatamente. La mancanza di integrazione diretta tra le due aree significa inoltre che la capacità sostanziale o le modifiche di programmazione richiederanno una nuova esecuzione della pianificazione.  

## <a name="planning-parameters"></a>Parametri di pianificazione

I parametri di pianificazione che imposti per un articolo o un gruppo di articoli controllano quali azioni il sistema di pianificazione suggerirà nelle diverse situazioni. I parametri di pianificazione definiti per ogni articolo controllano quando, quanto e come rifornire.  

Puoi definire i parametri di pianificazione anche per qualsiasi combinazione di articoli, varianti e ubicazioni impostando un'unità di stockkeeping (SKU) per ogni combinazione necessaria e quindi specificando i singoli parametri. Per ulteriori informazioni, vedi [Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) e [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Pianificazione della data di inizio

Il sistema di pianificazione ti aiuta a evitare di avere ordini aperti in passato e azioni suggerite che non sono fattibili. La pianificazione considera tutte le date precedenti alla data di inizio come una zona bloccata. La seguente regola si applica alla zona bloccata:  

* La domanda e l'offerta prima della data di inizio del periodo di pianificazione sono considerate come parte del magazzino o spedite. In altre parole, si presuppone che il piano per il passato venga eseguito secondo il piano specificato. Per ulteriori informazioni vedi [Elaborare gli ordini prima della data di inizio pianificazione](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## <a name="dynamic-order-tracking-pegging"></a>Tracciabilità dinamica dell'ordine (pegging)

La tracciabilità dinamica dell'ordine e la sua creazione simultanea dei messaggi di azione nel prospetto di pianificazione non fa parte del sistema di pianificazione degli approvvigionamenti. Quando viene creata o modificata una domanda o un'offerta, il tracciamento dinamico dell'ordine collega la domanda e le quantità per coprirla in tempo reale.  

Ad esempio, se immetti o modifichi un ordine di vendita, il sistema di tracciamento dinamico dell'ordine avvierà immediatamente la ricerca di un'offerta appropriata per coprire la domanda. L'approvvigionamento può provenire dal magazzino o da un ordine di approvvigionamento previsto (ad esempio un ordine di acquisto o di produzione). Quando trova un'origine di approvvigionamento, [!INCLUDE [prod_short](includes/prod_short.md)] collega la domanda e l'offerta. Accedi al collegamento nelle pagine di sola visualizzazione dalle righe del documento. Quando non è possibile individuare l'approvvigionamento, il sistema di tracciabilità ordine dinamica crea dei messaggi di azione nel prospetto di pianificazione con suggerimenti per il piano di approvvigionamento.  

La tracciabilità dinamica degli ordini ti aiuta a valutare se accettare i suggerimenti degli ordini di approvvigionamento. Dal lato dell'offerta, mostra la domanda che ha creato l'offerta. Dal lato della domanda, identifica l'offerta che deve coprire la domanda.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Esempio di tracciabilità ordini dinamica.":::

Per ulteriori informazioni vedi [Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md).  

Nelle società con un flusso di articoli basso e strutture dei prodotti meno avanzate, può essere adatto utilizzare la tracciabilità dinamica dell'ordine per la pianificazione dell'approvvigionamento. Tuttavia, negli ambienti più occupati, il sistema di pianificazione deve essere utilizzato per garantire un piano di approvvigionamento correttamente equilibrato.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Tracciabilità dinamica dell'ordine rispetto al sistema di pianificazione

Potrebbe essere difficile fare una differenza tra il sistema di pianificazione e la tracciabilità dinamica dell'ordine. Entrambe le funzionalità visualizzano l'output nel prospetto di pianificazione suggerendo azioni che il responsabile deve eseguire. Tuttavia, il modo in cui viene prodotto questo output è diverso.  

Il sistema di pianificazione si occupa dell'intero modello di domanda e offerta di un articolo. Considera tutti i livelli della gerarchia DBA lungo la sequenza temporale. La tracciabilità dinamica dell'ordine riguarda solo la situazione dell'ordine che l'ha attivata. Quando si bilancia domanda e offerta, il sistema di pianificazione crea i collegamenti in una modalità batch attivata dall'utente. La tracciabilità dinamica degli ordini crea automaticamente i collegamenti quando inserisci una domanda o un'offerta. Ad esempio, quando crei un ordine di vendita o di acquisto.  

La tracciabilità dinamica dell'ordine collega l'offerta e la domanda quando vengono immessi i dati, in base all'ordine. Ciò può condurre a un disordine nelle priorità. Ad esempio, un ordine di vendita immesso per primo con data di scadenza il mese successivo potrebbe essere collegato all'approvvigionamento in magazzino. Il prossimo ordine di vendita in scadenza domani può causare un messaggio di azione per creare un nuovo ordine di acquisto per coprirlo. L'immagine seguente illustra questo scenario.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Esempio di tracciabilità ordini nella pianificazione approvvigionamenti 1.":::

Il sistema di pianificazione gestisce la domanda e l'offerta per gli articoli in un ordine prioritario. L'ordine ha la priorità in base alle date di scadenza e ai tipi di ordine. Cioè, in base al principio "prima richiesto, prima servito". Elimina tutti i collegamenti di tracciabilità ordine che sono stati creati in modo dinamico e li ristabilisce in base alla priorità della data di scadenza. Quando viene completato, il sistema di pianificazione ha riconciliato tutti gli sbilanciamenti tra approvvigionamento e domanda, come illustrato di seguito per gli stessi dati.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Esempio di tracciabilità ordini nella pianificazione approvvigionamenti 2.":::  

Dopo aver eseguito la pianificazione, la tabella Movimenti messaggi azione non contiene alcun messaggio di azione. Questi messaggi vengono sostituiti dalle azioni suggerite nel foglio di lavoro di pianificazione. Per ulteriori informazioni vedi [Collegamenti della tracciabilità ordini durante la pianificazione](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## <a name="sequence-and-priority-in-planning"></a>Sequenza e priorità nella pianificazione

La sequenza dei calcoli dei piano è importante per ottenere il completamento del processo entro un intervallo temporale ragionevole. La priorità dei requisiti e delle risorse svolge un ruolo importante nell'ottenimento dei risultati migliori.  

Il sistema di pianificazione è guidato dalla domanda. Gli articoli di alto livello devono essere pianificati prima degli articoli di basso livello, in quanto possono generare la domanda degli articoli di livello più basso. Ad esempio, pianifica le ubicazioni al dettaglio prima dei centri di distribuzione, in quanto il piano per un'ubicazione al dettaglio può includere una domanda aggiuntiva dal centro di distribuzione. A livello di contropartita dettagliata, se un ordine di approvvigionamento già rilasciato può soddisfare l'ordine di vendita, il sistema non deve creare un nuovo ordine di approvvigionamento. Un approvvigionamento con un numero di lotto specifico non deve essere allocato per soddisfare una domanda generica se un'altra domanda richiede questo specifico lotto.  

### <a name="item-priority--low-level-code"></a>Priorità articolo / Codice ultimo livello

In un ambiente di produzione, la domanda di un articolo finito e vendibile produrrà una domanda derivata di componenti riguardanti l'articolo finito. La struttura della distinta base controlla la struttura dei componenti e può coprire diversi livelli di articoli semilavorati (WIP). La pianificazione di un articolo a un livello causerà una domanda derivata di componenti al livello successivo. Ciò risulterà in una domanda derivata per gli articoli acquistati. Il sistema di pianificazione pianifica gli articoli in ordine di classificazione nella gerarchia DBA totale. Il sistema inizia con gli articoli vendibili finiti al livello superiore e prosegue lungo la struttura del prodotto fino agli articoli di livello inferiore (secondo il codice ultimo livello).  

L'immagine seguente mostra la sequenza in cui [!INCLUDE [prod_short](includes/prod_short.md)] suggerisce gli ordini di approvvigionamento al livello superiore. Presuppone che i suggerimenti siano stati accettati e mostra anche gli articoli di livello inferiore.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Pianificazione per le distinte base.":::

Per ulteriori informazioni sulle considerazioni di produzione, vedi [Caricare i profili di magazzino](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### <a name="optimizing-performance-for-low-level-calculations"></a>Ottimizzazione delle prestazioni per calcoli del codice di ultimo livello

I calcoli del codice di ultimo livello possono influire sulle prestazioni del sistema. Per ridurre l'impatto, è possibile disattivare l'interruttore **Calcolo dinamico del codice di ultimo livello** nella pagina **Setup manufacturing**. In tal caso, [!INCLUDE[prod_short](includes/prod_short.md)] suggerisce di creare una movimento ricorrente nella coda processi che aggiorna quotidianamente i codici di ultimo livello. È possibile garantire che il processo venga eseguito al di fuori dell'orario di lavoro specificando un'ora di inizio nel campo **Prima data/ora inizio**.

Puoi anche accelerare i calcoli del codice di ultimo livello attivando l'interruttore **Ottimizza il calcolo del codice di ultimo livello** nella pagina **Setup manufacturing**.

> [!IMPORTANT]
> Se si sceglie di ottimizzare le prestazioni, [!INCLUDE[prod_short](includes/prod_short.md)] utilizzerà nuovi metodi di calcolo per determinare i codici di ultimo livello. Se hai un'estensione che si basa sugli eventi utilizzati dai calcoli precedenti, l'estensione può smettere di funzionare.

### <a name="locations--transfer-level-priority"></a>Ubicazioni/priorità a livello di trasferimento

Per le società con più ubicazioni potrebbe essere necessario pianificare singolarmente ogni ubicazione. Ad esempio, il livello di scorta di sicurezza di un articolo e il metodo di riordino possono essere diversi da una posizione a un'altra. È necessario specificare i parametri di pianificazione per articolo e ubicazione.  

Puoi utilizzare le SKU per specificare i singoli parametri di pianificazione. Una USK può essere valutata come un articolo in una specifica ubicazione. Se non hai definito una SKU per quella ubicazione, [!INCLUDE [prod_short](includes/prod_short.md)] utilizzerà i parametri impostati nella scheda articolo. [!INCLUDE [prod_short](includes/prod_short.md)] calcola un piano solo per le ubicazioni attive, ovvero dove esiste una domanda o un'offerta per l'articolo specificato.  

Qualsiasi articolo può essere gestito in qualsiasi ubicazione, ma [!INCLUDE [prod_short](includes/prod_short.md)] ha un approccio al concetto di ubicazione piuttosto rigoroso. Ad esempio, un ordine di vendita per un articolo in un'ubicazione non può essere soddisfatto da una specifica quantità in stock di un'altra ubicazione. La quantità in stock deve essere prima trasferita nell'ubicazione specificata nell'ordine di vendita.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Pianificazione per le unità di stockkeeping.":::

Per ulteriori informazioni vedi [Dettagli di progettazione: Trasferimenti nella pianificazione](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Priorità ordini

All'interno di una determinata USK, la data richiesta o disponibile rappresenta la priorità più alta; la domanda della data corrente deve essere gestita prima della domanda dei giorni successivi. Oltre a questo tipo di priorità, i tipi di domanda e approvvigionamento vengono ordinati in base all'importanza del business per decidere quale domanda deve essere soddisfatta prima. Dal lato dell'offerta, la priorità dell'ordine determina l'origine dell'approvvigionamento da applicare per prima. Per ulteriori informazioni vedi [Assegnare la priorità agli ordini](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Previsioni della domanda e ordini programmati

Le previsioni e gli ordini programmati rappresentano la domanda prevista. L'ordine programmato, che copre gli acquisti destinati a un cliente in un determinato periodo di tempo, serve a ridurre le incertezze della previsione globale. L'ordine programmato è una previsione specifica del cliente sopra la previsione non specificata come nella seguente immagine.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Pianificazione con le previsioni.":::

Per ulteriori informazioni vedi [La domanda di previsione viene ridotta dagli ordini di vendita](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## <a name="planning-assignment"></a>Pianificazione assegnazione

Tutti gli articoli devono essere ripianificati perché il modello della domanda o dell'offerta è cambiato dall'ultima volta che è stato calcolato un piano. Se ad esempio hai immesso un nuovo ordine di vendita o ne hai modificato uno esistente, ricalcola il piano. Altri motivi per la ripianificazione includono una modifica nella previsione o nella scorta di sicurezza. La modifica di una distinta base aggiungendo o rimuovendo un componente molto probabilmente indica una modifica, ma solo per l'articolo del componente.  

Il sistema di pianificazione monitorizza tali eventi e assegna gli articoli appropriati per la pianificazione.  

Per più ubicazioni, l'assegnazione avviene a livello di articolo per ogni combinazione di ubicazione. Se un ordine di vendita è stato creato solo in un'ubicazione, [!INCLUDE [prod_short](includes/prod_short.md)] assegna l'articolo all'ubicazione per la pianificazione.  

Il motivo per selezionare gli articoli per la pianificazione è una questione di prestazioni del sistema. Se non viene apportata alcuna modifica nel modello domanda-offerta di un articolo, il sistema di pianificazione non suggerisce alcuna azione da intraprendere. Senza l'assegnazione di pianificazione, il sistema deve eseguire i calcoli per tutti gli articoli per determinare cosa pianificare. Per saperne di più sui motivi per assegnare gli articoli per la pianificazione, vedi [Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md).  

Di seguito vengono illustrate le opzioni di pianificazione disponibili:  

* **Calcola piano – rigenerativo** calcola tutti gli articoli selezionati, se sono necessari o meno.  
* **Calcola piano - Solo cambiamenti** calcola solo gli articoli selezionati con modifiche nel relativo modello domanda-offerta e, pertanto, sono stati assegnati per la pianificazione.  

Alcune persone ritengono che la pianificazione del saldo periodo debba essere eseguita immediatamente, ad esempio, quando vengono immessi gli ordini di vendita. Tuttavia, la pianificazione immediata potrebbe confondere perché la tracciabilità ordini dinamica e la messaggistica di azioni vengono calcolate immediatamente. [!INCLUDE[prod_short](includes/prod_short.md)] offre il controllo ATP (available-to-promise) in tempo reale. Fornisce avvisi pop-up quando immetti ordini di vendita e il piano di approvvigionamento corrente non è in grado di soddisfare la domanda.  

Il sistema di pianificazione pianifica solo per quegli articoli che hai preparato con i parametri di pianificazione appropriati. In caso contrario, presuppone che pianificherai gli articoli manualmente o in parte automaticamente utilizzando la funzionalità di pianificazione ordini. Per ulteriori informazioni sulle procedure di pianificazione automatiche, vedi [Dettagli di progettazione - Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Dimensioni articolo

La domanda e l'approvvigionamento possono portare codici di variante e codici di ubicazione che devono essere rispettati quando il sistema di pianificazione bilancia la domanda e l'approvvigionamento.  

[!INCLUDE [prod_short](includes/prod_short.md)] tratta i codici ubicazione e variante come dimensioni di articolo in una riga ordine di vendita, un movimento di inventario e così via. Di conseguenza, calcola un piano per ogni combinazione di variante e ubicazione come se la combinazione fosse un numero di articolo separato.  

Invece di calcolare combinazioni teoriche di variante e ubicazione, [!INCLUDE [prod_short](includes/prod_short.md)] calcola solo le combinazioni effettivamente presenti nel database. Per ulteriori informazioni su come il sistema di pianificazione si occupa dei codici ubicazione su richiesta, vedi [Dettagli di progettazione: Domanda nell'ubicazione Vuota](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Attributi articolo

Gli articoli hanno spesso attributi generali, come numero articolo, codice variante, codice ubicazione e tipo di ordine. Tuttavia, ogni evento di domanda e offerta può avere altre specifiche, ad esempio numeri di serie o di lotto. Il sistema di pianificazione pianifica questi attributi in determinati modi in base al relativo livello di specifica.  

Un collegamento ordine-a-ordine tra approvvigionamento e domanda è un altro tipo di attributo che riguarda il sistema di pianificazione. Per ulteriori informazioni, vedi [Collegamenti ordine su ordine](#order-to-order-links).

### <a name="specific-attributes"></a>Attributi specifici

Alcuni attributi della domanda sono specifici e un'offerta deve corrisponderli esattamente.

* Numeri di serie o di lotto che necessitano di applicazione specifica (questi attributi sono necessari se l'interruttore **Tracciabilità NS specifico** o **Tracciab. lotto specifico** è attivato nella pagina **Scheda cod. tracciab. articolo** per il codice di tracciabilità articolo utilizzato dall'articolo).  
* Collegamenti agli ordini di approvvigionamento creati manualmente o automaticamente per una domanda specifica (collegamenti ordine su ordine).  

Per questi attributi il sistema di pianificazione applica le seguenti regole:  

* La domanda con gli attributi specifici può essere soddisfatta solo dall'approvvigionamento con gli attributi corrispondenti.  
* L'approvvigionamento con attributi specifici può soddisfare una domanda che non richiede specificamente quegli attributi.  

Se gli approvvigionamenti previsti o di magazzino non possono soddisfare una domanda per attributi specifici, il sistema di pianificazione suggerisce un nuovo ordine di approvvigionamento senza tener conto dei parametri di pianificazione.  

### <a name="non-specific-attributes"></a>Attributi non specifici

Gli articoli con numeri di serie o di lotto senza un'impostazione di tracciabilità articolo specifica potrebbero avere numeri di serie o di lotto non specifici. Questi tipi di numeri possono essere applicati a qualsiasi numero di serie o di lotto. Il sistema di pianificazione ha più libertà per associare, ad esempio, una domanda serializzata con un approvvigionamento con un numero seriale, in genere in magazzino.  

La domanda e l'offerta con numeri di serie o di lotto, specifici o non specifici, hanno priorità elevata e sono esenti dalla zona bloccata. Faranno parte della pianificazione anche se scadono prima della data di inizio della pianificazione. Per ulteriori informazioni, vedi [I numeri seriali o di lotto vengono caricati dal livello di specifica](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Per ulteriori informazioni su come il sistema di pianificazione bilancia gli attributi, vedi [Numeri di serie o di lotto e collegamenti ordine-a-ordine sono esenti dal periodo precedente](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## <a name="order-to-order-links"></a>Collegamenti ordine su ordine

Ordine su ordine significa che acquisti, assembli o produci un articolo per una domanda specifica. Ci sono diversi motivi per scegliere questo criterio:

* La domanda è poco frequente.
* Il lead time è insignificante.
* Gli attributi richiesti variano.  

Un altro caso che utilizza i collegamenti ordine su ordine è quando un ordine di assemblaggio è collegato a un ordine di vendita in uno scenario assemblaggio su ordine.  

I collegamenti ordine su ordine vengono applicati tra la domanda e l'approvvigionamento in quattro modi:  

* Quando l'articolo pianificato utilizza il metodo di riordino **Ordine**  
* Se usi il criterio produzione su ordine per creare ordini di produzione di tipo progetto o multilivello (producendo i componenti nello stesso ordine di produzione)  
* Se crei ordini di produzione per ordini di vendita con la funzionalità Pianifica ordine vendita  
* Quando assembli un articolo in un ordine di vendita (**Criterio di assemblaggio** è impostato su **Assemblaggio su ordine**)  

Il sistema di pianificazione ti suggerisce solo di ordinare la quantità richiesta. L'ordine di acquisto, di produzione o di assemblaggio continua a essere associato alla domanda. Ad esempio, se un ordine di vendita viene modificato in tempo o quantità, il sistema di pianificazione suggerisce di modificare l'ordine di approvvigionamento di conseguenza.  

Quando sono presenti collegamenti ordine su ordine, il sistema di pianificazione non include l'approvvigionamento o il magazzino collegato nella procedura di bilanciamento. I pianificatori possono decidere se utilizzare l'offerta collegata o una nuova domanda. In quest'ultimo caso, possono eliminare l'ordine di approvvigionamento o riservare manualmente l'approvvigionamento collegato.  

Le prenotazioni e i collegamenti di tracciabilità degli ordini si interrompono se una situazione diventa impossibile. Ad esempio, quando si sposta la domanda a una data precedente all'offerta. I collegamenti ordine su ordine si adattano ai cambiamenti della domanda o dell'offerta e non si interrompono mai.  

## <a name="reservations"></a>Prenotazioni

Il sistema di pianificazione non include quantità impegnate nei calcoli. Ad esempio, se una quantità per un ordine di vendita è completamente o parzialmente prenotata, non è possibile utilizzarla per coprire un'altra domanda.

Il sistema di pianificazione non include quantità impegnate nel profilo di magazzino previsto. Deve considerare tutte le quantità per determinare quando è passato il punto di riordino e quante riordinarne per raggiungere il livello massimo di magazzino. Gli impegni non necessari possono aumentare il rischio che i livelli di magazzino diventino bassi poiché la logica di pianificazione non rileva le quantità impegnate.  

L'immagine seguente mostra come le prenotazioni possono ostacolare la pianificazione.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Pianificazione con gli impegni.":::

Per ulteriori informazioni vedi [Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Avvisi

La prima colonna nel prospetto di pianificazione è dedicata ai campi di avviso. Quando crei una riga di pianificazione per una situazione insolita, viene visualizzata un'icona di avviso.  

L'approvvigionamento nelle righe di pianificazione con avvisi in genere non viene modificato in base ai parametri di pianificazione. Al contrario, il sistema di pianificazione suggerisce un approvvigionamento per coprire la quantità di domanda esatta. Tuttavia, il sistema può essere impostato in modo da rispettare parametri di pianificazione per le righe di pianificazione con determinati avvisi. Le informazioni di avviso vengono visualizzate nella pagina **Elementi di pianificazione non tracciati**, che visualizza anche i collegamenti di tracciabilità alle entità di rete diverse dagli ordini. Sono disponibili tre tipi di avvisi:  

* Emergenza  
* Eccezione  
* Attenzione  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Avvisi del prospetto di pianificazione.":::

### <a name="emergency"></a>Emergenza

L'avviso di emergenza è visualizzato in due situazioni:  

* Quando alla data di inizio pianificazione le giacenze sono negative  
* Quando sono presenti eventi di approvvigionamento o domanda arretrati  

Se le giacenze di un articolo sono negative alla data di inizio pianificazione, il sistema di pianificazione suggerisce un approvvigionamento di emergenza per la quantità negativa che pervenga alla data di inizio pianificazione. Il testo di avviso riporta la data di inizio e la quantità dell'ordine di emergenza. Per ulteriori informazioni vedi [Gestione giacenze negative previste](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Le righe di documento con data di scadenza precedente la data di inizio pianificazione sono consolidate in un ordine di approvvigionamento di emergenza. L'arrivo dell'ordine è pianificato per la data di inizio pianificazione.  

### <a name="exception"></a>Eccezione

L'avviso di eccezione viene visualizzato se la proiezione delle giacenze disponibili scende al di sotto della scorta di sicurezza. Il sistema di pianificazione suggerisce un ordine di approvvigionamento per soddisfare la domanda alla data di scadenza. Il testo dell'avviso riporta la quantità di scorte di sicurezza dell'articolo e la data in cui è stata intaccata.  

La violazione del livello delle scorte di sicurezza è un'eccezione. Non deve accadere se il punto di riordino è impostato correttamente. Per ulteriori informazioni, vedi [Il ruolo del punto di riordino](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Le proposte di ordine di eccezione assicurano che normalmente le scorte disponibili previste non siano mai più basse del livello di scorta di sicurezza. La quantità proposta copre la scorta di sicurezza, senza considerare i parametri di pianificazione. Tuttavia, in alcuni scenari, verranno presi in considerazione i modificatori di ordine.  

> [!NOTE]  
> Il sistema di pianificazione potrebbe aver consumato la scorta di sicurezza intenzionalmente, pertanto la rifornirà immediatamente. Per ulteriori informazioni vedi [Consumare le scorte di sicurezza](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### <a name="attention"></a>Attenzione

L'avviso di attenzione è visualizzato in tre situazioni:  

* La data di inizio pianificazione precede la data di lavoro.  
* La riga di pianificazione suggerisce di cambiare un ordine di acquisto o di produzione rilasciato.  
* La giacenza disponibile supera il livello di overflow alla data di scadenza. Per ulteriori informazioni vedi [Restare al di sotto del livello di overflow](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> Nella pianificazione delle righe con avvisi, il campo **Accetta messaggio errore** non è selezionato perché si prevede che l'addetto alla pianificazione effettui indagini sulle righe prima di eseguire il piano.  

## <a name="error-logs"></a>Registri errore

Nella pagina di richiesta **Calcola piano**, l'utente può selezionare il campo **Interrompi e mostra primo errore** per interrompere l'esecuzione della pianificazione quando incontra il primo errore. Viene visualizzato un messaggio contenente le informazioni sull'errore. Se è presente un errore, nel prospetto di pianificazione verranno presentate solo le righe di pianificazione create correttamente prima dell'individuazione dell'errore.  

Se il campo non è selezionato, il processo batch **Calcola piano** continuerà fino a completamento. Gli errori non interrompono il processo batch. In caso di errori, un messaggio indica quanti articoli sono stati interessati. La pagina **Log errori pianificazione** fornisce ulteriori dettagli sull'errore e i collegamenti ai documenti interessati o alle impostazioni.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Messaggi di errore del prospetto di pianificazione.":::

## <a name="planning-flexibility"></a>Flessibilità pianificazione

Non è sempre fattibile pianificare un ordine di approvvigionamento esistente. Ad esempio, quando la produzione è iniziata o assumi altre persone in un giorno specifico per svolgere il lavoro. Per indicare se un ordine esistente può essere modificato dal sistema di pianificazione, tutte le righe dell'ordine di approvvigionamento dispongono di un campo **Flessibilità pianificazione** con due opzioni: **Illimitata** o **Nessuna**. Se il campo è impostato su **Nessuna**, il sistema di pianificazione non proverà a modificare la riga dell'ordine di approvvigionamento.  

Puoi scegliere manualmente un'opzione nel campo tuttavia, in alcuni casi verrà impostato automaticamente da [!INCLUDE [prod_short](includes/prod_short.md)]. Il fatto che la flessibilità di pianificazione possa essere impostata manualmente è importante perché ti consente di adattare l'utilizzo della funzionalità a flussi di lavoro e casi differenti. Per ulteriori informazioni su come viene utilizzato questo campo, vedi [Dettagli di progettazione - Trasferimenti nella pianificazione](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Pianificazione ordini

Lo strumento di base di pianificazione dell'approvvigionamento rappresentato dalla pagina **Pianificazione ordini** è progettato per un processo decisionale manuale. Non considera i parametri di pianificazione e pertanto non viene ulteriormente discusso in questo articolo. Per ulteriori informazioni, vedi [Pianificare una nuova domanda ordine per ordine](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Non è consigliabile utilizzare la pianificazione ordini se la società già utilizza i prospetti di pianificazione o di richiesta di approvvigionamento. Gli ordini di approvvigionamento creati mediante la pagina **Pianificazione ordini** possono essere modificati o eliminati durante le esecuzioni automatizzate di pianificazione. Queste modifiche si verificano perché l'esecuzione della pianificazione automatica utilizza i parametri di pianificazione che potrebbero non venire presi in considerazione quando manualmente hai creato la pianificazione nella pagina Pianificazione ordini.  

## <a name="finite-loading"></a>Carico finito

[!INCLUDE[prod_short](includes/prod_short.md)] fornisce un programma approssimativo per pianificare un uso ragionevole delle risorse. Non crea e mantiene automaticamente le pianificazioni dettagliate basate su priorità o regole di ottimizzazione.  

L'uso previsto della funzionalità delle risorse con limiti di capacità è il seguente:

* Per evitare di sovraccaricare le risorse
* Per garantire che la capacità non venga allocata se potrebbe ridurre il tempo di completamento di un ordine di produzione

Nella pianificazione con risorse vincolate alla capacità, [!INCLUDE [prod_short](includes/prod_short.md)] garantisce che nessuna risorsa venga caricata oltre la propria capacità definita (carico critico). Assegna ogni operazione alla fascia oraria disponibile più vicina. Se la fascia oraria non è sufficiente a completare l'intera operazione, divide l'operazione in due o più parti e le colloca nelle fasce orarie adiacenti disponibili.  

> [!NOTE]  
> Nel caso che l'operazione venga suddivisa, il tempo di setup viene assegnato una sola volta perché si presuppone che vengano apportate alcune rettifiche manuali per ottimizzare la pianificazione.  

Puoi aggiungere il tempo di stabilizzazione alle risorse per ridurre al minimo la suddivisione dell'operazione. Questa tempo permette a [!INCLUDE [prod_short](includes/prod_short.md)] di pianificare il carico nell'ultimo giorno possibile superando leggermente la percentuale di carico critico.  

## <a name="see-also"></a>Vedere anche

[Dettagli di progettazione: Trasferimenti nella pianificazione](design-details-transfers-in-planning.md)  
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)  
[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md)  
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
