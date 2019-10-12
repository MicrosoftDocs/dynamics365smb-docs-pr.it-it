---
title: Dettagli di progettazione - Concetti centrali del sistema di pianificazione| Microsoft Docs
description: Le funzioni di pianificazione sono contenute in un processo batch che seleziona innanzitutto gli articoli pertinenti e il periodo per il quale pianificare, quindi suggerisce le azioni che l'utente può effettuare in base alla situazione di domanda/offerta e ai parametri di pianificazione degli articoli.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 025b8fb9100d8418e9e157e8098afe19d24843fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303750"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Dettagli di progettazione: Concetti centrali del sistema di pianificazione
Le funzioni di pianificazione sono contenute in un processo batch che seleziona innanzitutto articoli rilevanti e il periodo per la pianificazione. Quindi, in base al codice di ultimo livello di ciascun articolo (ubicazione della distinta base), il processo batch chiama un'unità di codice, che calcola un piano di approvvigionamento bilanciando approvvigionamento e domanda e suggerendo possibili azioni per l'utente. Le azioni suggerite vengono visualizzate come righe nel prospetto di pianificazione o nella richiesta di approvvigionamento.  

![Contenuto della pagina Prospetto pianificazione](media/NAV_APP_supply_planning_1_planning_worksheet.png "Contenuto della pagina Prospetto pianificazione")  

Si presume che il responsabile della pianificazione della società, ad esempio un addetto acquisti o un responsabile della pianificazione di produzione, sia l'utente del sistema di pianificazione. Il sistema di pianificazione aiuta l'utente eseguendo calcoli complessi ma chiari di un piano. L'utente può quindi concentrarsi sulla soluzione i problemi di più difficili, ad esempio quando si verificano delle situazioni insolite.  

Il sistema di pianificazione si basa sulla domanda prevista ed effettiva da parte dei clienti, ad esempio la previsione e gli ordini di vendita. L'esecuzione del calcolo della pianificazione ha come risultato alcune azioni specifiche suggerite dall'applicazione per l'utente da adottare relativamente al possibile approvvigionamento da fornitori, o reparti di assemblaggio o produzione o trasferimenti da altri magazzini. Queste azioni suggerite possono servire a creare nuovi ordini di approvvigionamento, ad esempio gli ordini di acquisto o di produzione. Se sono già presenti ordini di approvvigionamento, le azioni suggerite possono consistere nell'aumento o nell'accelerazione di tali ordini per rispondere alle modifiche nella domanda.  

Un altro obiettivo del sistema di pianificazione consiste nel garantire che il magazzino non aumenti in modo superfluo. Nel caso di un calo della domanda, il sistema di pianificazione suggerirà all'utente di rimandare, ridurre in quantità o annullare gli ordini di approvvigionamento esistenti.  

Per MRP e MPS, le funzioni Calcola piano - Solo cambiamenti e Calcola piano - Rigenerativo sono tutte funzioni all'interno di un unico codice contenente la logica di pianificazione. Tuttavia, il calcolo del piano di approvvigionamento implica sottosistemi diversi.  

Notare che il sistema di pianificazione non include alcuna logica dedicata per il livellamento delle capacità o la pianificazione accurata. Di conseguenza, tale lavoro di programmazione viene eseguito come disciplina separata. La mancanza di integrazione diretta tra le due aree significa inoltre che la capacità sostanziale o le modifiche di programmazione richiederanno una nuova esecuzione della pianificazione.  

## <a name="planning-parameters"></a>Parametri di pianificazione  
I parametri di pianificazione che l'utente imposta per un articolo o un gruppo di articoli controllano quali azioni il sistema di pianificazione suggerirà nelle diverse situazioni. I parametri di pianificazione sono definiti in ogni scheda articolo per controllare quando, quanto e come rifornire.  

I parametri di pianificazione possono essere definiti anche per qualsiasi combinazione di articoli, varianti e ubicazioni impostando un'unità di stockkeeping (USK) per ogni combinazione necessaria e quindi specificando i singoli parametri.  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md) e [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Pianificazione data inizio  
Per evitare un piano di approvvigionamento che incorpori ordini aperti in passato e suggerisca azioni potenzialmente impossibili, il sistema di pianificazione tratta tutte le date anteriori alla data di inizio della pianificazione come zona bloccata nella quale vale la seguente regola speciale:  

Tutta le domande e l'approvvigionamento prima della data di inizio del periodo di pianificazione verranno considerati come parte del magazzino o saranno spediti.  

In altre parole, si presuppone che il piano per il passato sia eseguito secondo il piano specificato.  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="dynamic-order-tracking-pegging"></a>Tracciabilità dinamica dell'ordine (Pegging)  
La tracciabilità dinamica dell'ordine, con la sua creazione simultanea dei messaggi di azione nel prospetto di pianificazione, non fa parte del sistema di pianificazione degli approvvigionamenti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Questa funzionalità collega, in tempo reale, la domanda e le quantità che potrebbero coprirla, ogni volta che viene creata o modificata una nuova domanda o un nuovo approvvigionamento.  

Ad esempio, se l'utente immette o modifica un ordine di vendita, il sistema di tracciamento dinamico dell'ordine avvierà immediatamente la ricerca di un approvvigionamento appropriato per coprire la domanda. Tale approvvigionamento può provenire dal magazzino o da un ordine di approvvigionamento previsto (ad esempio un ordine di acquisto o di produzione). Quando viene individuata un'origine di approvvigionamento, viene creato un collegamento tra domanda e approvvigionamento e tale collegamento viene visualizzato in pagine di sola lettura a cui è possibile accedere dalle righe del documento implicate. Quando non è possibile individuare l'approvvigionamento appropriato, il sistema di tracciabilità ordine dinamica crea dei messaggi di azione nel prospetto di pianificazione con suggerimenti per il piano di approvvigionamento che riflettono il bilanciamento dinamico. Di conseguenza, il sistema di tracciamento dell'ordine dinamico offre un sistema di pianificazione di base che può essere d'aiuto sia per il responsabile che per altri ruoli nella catena di approvvigionamento interna.  

Di conseguenza, la tracciabilità dinamica dell'ordine può essere considerata uno strumento che consente all'utente di valutare se accettare i suggerimenti di approvvigionamento. Dal lato dell'offerta, un utente può vedere quale domanda ha creato l'approvvigionamento e dal lato della domanda, quale approvvigionamento deve coprire la domanda.  

![Esempio di tracciabilità ordini dinamica](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Esempio di tracciabilità ordini dinamica")  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md).  

Nelle società con un flusso di articoli basso e strutture dei prodotti meno avanzate, potrebbe essere adatto utilizzare la tracciabilità dinamica dell'ordine come strumento principale di pianificazione dell'approvvigionamento. Tuttavia, negli ambienti più occupati, il sistema di pianificazione deve essere utilizzato per garantire sempre un piano di approvvigionamento correttamente equilibrato.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Tracciabilità dinamica dell'ordine rispetto al sistema di pianificazione  
Ad una rapida occhiata, potrebbe essere difficile fare una differenza tra il sistema di pianificazione e la tracciabilità dinamica dell'ordine. Entrambe le funzionalità visualizzano l'output nel prospetto di pianificazione suggerendo azioni che il responsabile deve eseguire. Tuttavia, il modo in cui viene prodotto questo output è diverso.  

Il sistema di pianificazione si occupa dell'intero modello di approvvigionamento e domanda di un articolo tramite tutti i livelli della gerarchia della DB lungo la linea temporale, mentre la tracciabilità dinamica dell'ordine si occupa solo della situazione dell'ordine che l'ha attivata. Per il bilanciamento tra approvvigionamento e domanda, il sistema di pianificazione crea dei collegamenti in una modalità batch attivata dall'utente, mentre la tracciabilità ordine dinamica crea collegamenti automaticamente e immediatamente, ogni volta che l'utente immette una domanda o un approvvigionamento nell'applicazione, ad esempio un ordine di vendita o di acquisto.  

La tracciabilità dinamica dell'ordine stabilisce i collegamenti tra l'approvvigionamento e la domanda quando vengono immessi i dati, in base all'ordine. Ciò può condurre a un certo disordine nelle priorità. Ad esempio, un ordine di vendita immesso prima, con una data di scadenza il mese successivo, può essere collegato all'approvvigionamento in magazzino, mentre l'ordine di vendita successivo con scadenza domani può indurre un messaggio di azione a creare un nuovo ordine di acquisto per coprirlo, come illustrato di seguito.  

![Esempio di tracciabilità ordini nella pianificazione approvvigionamenti 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Esempio di tracciabilità ordini nella pianificazione approvvigionamenti 1")  

Invece, il sistema di pianificazione si occupa di tutta la domanda e l'approvvigionamento di un determinato articolo, secondo una priorità basata sulle date di scadenza e sui tipi di ordine, ovvero in base al concetto secondo cui il primo che necessita è il primo che viene servito. Elimina tutti i collegamenti di tracciabilità ordine che sono stati creati in modo dinamico e li ristabilisce in base alla priorità della data di scadenza. Quando viene completato, il sistema di pianificazione ha riconciliato tutti gli sbilanciamenti tra approvvigionamento e domanda, come illustrato di seguito per gli stessi dati.  

![Esempio di tracciabilità ordini nella pianificazione approvvigionamenti 2](media/NAV_APP_supply_planning_1_planning_graph.png "Esempio di tracciabilità ordini nella pianificazione approvvigionamenti 2")  

Dopo la pianificazione dell'esecuzione, non resta alcun messaggio nella tabella Movimenti messaggi azione, in quanto sono stati sostituiti dalle azioni suggerite nel prospetto di pianificazione  

Per ulteriori informazioni, vedere i collegamenti di tracciabilità ordine durante la pianificazione in [Dettagli di progettazione: Bilanciamento approvvigionamento con domanda](design-details-balancing-supply-with-demand.md).  

## <a name="sequence-and-priority-in-planning"></a>Sequenza e priorità nella pianificazione  
Quando si imposta un piano, la sequenza dei calcoli è importante per ottenere il completamento del processo entro un intervallo temporale ragionevole. Inoltre, la priorità dei requisiti e delle risorse svolge un ruolo importante nell'ottenimento dei risultati migliori.  

Il sistema di pianificazione in [!INCLUDE[d365fin](includes/d365fin_md.md)] è guidato dalla domanda. Gli articoli di alto livello devono essere pianificati prima degli articoli di basso livello, in quanto il piano per gli articoli di alto livello potrebbe generare la domanda aggiuntiva degli articoli di livello più basso. Questo significa, ad esempio, che le ubicazioni al dettaglio devono essere pianificate prima dei centri di distribuzione, in quanto il piano per un'ubicazione al dettaglio può includere una domanda aggiuntiva dal centro di distribuzione. A livello di contropartita dettagliata, questo significa anche che un ordine di vendita non deve avviare un nuovo ordine di approvvigionamento se un ordine di approvvigionamento già rilasciato può soddisfare l'ordine di vendita. Analogamente, un approvvigionamento che presenta un numero di lotto specifico non deve essere allocato per soddisfare una domanda generica se un'altra domanda richiede questo specifico lotto.  

### <a name="item-priority--low-level-code"></a>Priorità articolo / Codice ultimo livello  
In un ambiente di produzione, la domanda di un articolo finito e vendibile produrrà una domanda derivata di componenti riguardanti l'articolo finito. La struttura della distinta base controlla la struttura dei componenti e può coprire diversi livelli di articoli semilavorati (WIP). La pianificazione di un articolo a un livello causerà una domanda derivata di componenti al livello successivo, e così via. Infine, ciò risulterà in una domanda derivata per gli articoli acquistati. Di conseguenza, il sistema di pianificazione pianifica gli articoli in base alla loro valutazione nella gerarchia DB totale, a partire dagli articoli vendibili finiti nel livello superiore e continuando nella struttura di prodotti fino agli articoli di livello più basso (in base al codice di ultimo livello).  

![Pianificazione per le distinte base](media/NAV_APP_supply_planning_1_BOM_planning.png "Pianificazione per le distinte base")  

Le cifre mostrano in quale sequenza il sistema offre suggerimenti per gli ordini di approvvigionamento di articoli del livello massimo e, presupponendo che l'utente accetterà i suggerimenti, anche per gli articoli dei livelli inferiori.  

Per ulteriori informazioni sulle considerazioni di produzione, vedere [Dettagli di progettazione - Carico dei profili di magazzino](design-details-loading-the-inventory-profiles.md).  

### <a name="locations--transfer-level-priority"></a>Ubicazioni/priorità a livello di trasferimento  
Per le società che lavorano in più ubicazioni potrebbe essere necessario pianificare singolarmente ogni ubicazione. Ad esempio, il livello di scorta di sicurezza di un articolo e il metodo di riordino potrebbero essere diversi da una posizione a un'altra. In questo caso, i parametri di pianificazione devono essere specificati per articolo e anche per ubicazione.  

Ciò è supportato con l'utilizzo delle unità di stockkeeping, in cui i singoli parametri di pianificazione possono essere specificati a livello di stockkeeping. Una USK può essere valutata come un articolo in una specifica ubicazione. Se l'utente non ha definito una USK per tale ubicazione, l'applicazione imposterà i valori predefiniti ai parametri che sono stati impostati nella scheda articolo. L'applicazione calcola un piano solo per le ubicazioni attive, ovvero dove esiste una domanda o un approvvigionamento per l'articolo specificato.  

In linea di principio, qualsiasi articolo può essere gestito in qualsiasi ubicazione, ma l'approccio dell'applicazione al concetto di ubicazione è piuttosto rigoroso. Ad esempio, un ordine di vendita in un'ubicazione non può essere soddisfatto da una specifica quantità in stock in un'altra ubicazione. La quantità in stock deve essere prima trasferita nell'ubicazione specificata nell'ordine di vendita.  

![Pianificazione per le unità di stockkeeping](media/NAV_APP_supply_planning_1_SKU_planning.png "Pianificazione per le unità di stockkeeping")  

Per ulteriori informazioni, vedere [Dettagli di progettazione - Trasferimenti nella pianificazione](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Priorità ordini  
All'interno di una determinata USK, la data richiesta o disponibile rappresenta la priorità più alta; la domanda della data corrente deve essere gestita prima della domanda dei giorni successivi. Oltre a questo tipo di priorità, i diversi tipi di domanda e approvvigionamento vengono ordinati in base all'importanza del business per decidere quale domanda deve essere soddisfatte prima di soddisfare un'altra domanda. Dal lato fornitore, la priorità dell'ordine indicherà quale origine di approvvigionamento deve essere collegata prima di collegare altre origini di approvvigionamento.  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Assegnazione priorità ordini](design-details-prioritizing-orders.md).  

## <a name="demand-forecasts-and-blanket-orders"></a>Previsioni della domanda e ordini programmati  
Le previsioni e gli ordini programmati rappresentano la domanda prevista. L'ordine programmato, che copre gli acquisti destinati a un cliente in un determinato periodo di tempo, serve a ridurre le incertezze della previsione globale. L'ordine programmato è una previsione specifica del cliente sopra la previsione non specificata come illustrato di seguito.  

![Pianificazione con le previsioni](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Pianificazione con le previsioni")  

Per ulteriori informazioni, vedere la sezione "La domanda di previsione viene ridotta dagli ordini di vendita" in [Dettagli di progettazione - Carico dei profili di magazzino](design-details-loading-the-inventory-profiles.md).  

## <a name="planning-assignment"></a>Compiti di pianificazione  
Tutti gli articoli devono essere pianificati, tuttavia, non esiste motivo per calcolare un piano per un articolo a meno che non ci sia stato una modifica nella domanda o nel modello di approvvigionamento dall'ultima volta in cui è stato calcolato un piano.  

Se l'utente ha immesso un nuovo ordine di vendita o ne ha cambiato uno esistente, esiste motivo per ricalcolare il piano. Altri motivi includono una modifica nella previsione o la scorta di sicurezza desiderata. Modificare una distinta base aggiungendo o rimuovendo un componente che molto probabilmente indicherebbe una modifica, ma solo per l'articolo del componente.  

Il sistema di pianificazione monitorizza tali eventi e assegna gli articoli appropriati per la pianificazione.  

Per più ubicazioni, l'assegnazione avviene a livello di articolo per ogni combinazione di ubicazione. Se, ad esempio, un ordine di vendita è stato creato solo in un'ubicazione, l'applicazione assegnerà l'articolo a tale specifica ubicazione per la pianificazione.  

Il motivo per selezionare gli articoli per la pianificazione è una questione di prestazioni del sistema. Se non viene apportata alcuna modifica nel modello domanda-approvvigionamento di un articolo, il sistema di pianificazione non suggerirà alcuna azione da intraprendere. Senza l'assegnazione di pianificazione, il sistema deve eseguire i calcoli per tutti gli articoli per determinare cosa pianificare e cosa sfrutta maggiormente le risorse di sistema.  

L'elenco completo dei motivi per l'assegnazione di un articolo per la pianificazione viene fornito in [Dettagli di progettazione - Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md).  

Le opzioni di pianificazione in [!INCLUDE[d365fin](includes/d365fin_md.md)] sono:  

-   Calcola piano – rigenerativo: calcola tutti gli articoli selezionati, se sono necessari o meno.  
-   Calcola piano - Solo cambiamenti: calcola solo gli articoli selezionati con alcune modifiche nel relativo modello domanda-approvvigionamento e, pertanto, sono stati assegnati per la pianificazione.  

Alcuni utenti ritengono che la pianificazione del saldo periodo debba essere eseguita immediatamente, ad esempio, quando vengono immessi gli ordini di vendita. Tuttavia, ciò potrebbe confondere perché la tracciabilità ordini dinamica e la messaggistica di azioni vengono calcolate immediatamente. Inoltre, [!INCLUDE[d365fin](includes/d365fin_md.md)] offre il controllo in tempo reale ATP (available-to-promise) che fornisce gli avvisi a comparsa quando si immettono gli ordini di vendita se la domanda non può essere soddisfatta nel piano di approvvigionamento corrente.  

Oltre a queste considerazioni, il sistema di pianificazione pianifica solo per quegli articoli che l'utente ha preparato con i parametri di pianificazione appropriati. In caso contrario, si presuppone che l'utente pianificherà gli articoli manualmente o in parte automaticamente utilizzando la funzionalità di pianificazione ordini.  

Per ulteriori informazioni sulle procedure di pianificazione automatiche, vedere [Dettagli di progettazione - Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Dimensioni articolo  
La domanda e l'approvvigionamento possono portare codici di variante e codici di ubicazione che devono essere rispettati quando il sistema di pianificazione bilancia la domanda e l'approvvigionamento.  

Il sistema tratta i codici ubicazione e variante come dimensioni di articolo in una riga ordine di vendita, un movimento di inventario e così via. Di conseguenza, calcola un piano per ogni combinazione di variante e ubicazione come se la combinazione fosse un numero di articolo separato.  

Invece di calcolare una qualunque combinazione teorica di variante e ubicazione, vengono calcolate solo le combinazioni effettivamente presenti nel database.  

Per ulteriori informazioni su come il sistema di pianificazione si occupa dei codici ubicazione su richiesta, vedere [Dettagli di progettazione: Domanda nell'ubicazione Vuota](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Attributi articolo  
Oltre alle dimensioni dell'articolo corrente, ad esempio il numero articolo, il codice variante, il codice ubicazione e il tipo di ordine, ogni evento di domanda e approvvigionamento può portare specifiche aggiuntive nei numeri di serie o di lotto. Il sistema di pianificazione pianifica questi attributi in determinati modi in base al relativo livello di specifica.  

Un collegamento ordine-a-ordine tra approvvigionamento e domanda è un altro tipo di attributo che riguarda il sistema di pianificazione.  

### <a name="specific-attributes"></a>Attributi specifici  
Alcuni attributi a richiesta sono specifici e devono essere corrisposti esattamente da un approvvigionamento corrispondente. Sono disponibili i seguenti due attributi specifici:  

-   Numeri di serie o di lotto richiesti che necessitano di applicazione specifica (la casella di controllo **Tracciabilità NS specifico** o **Tracciab. lotto specifico** è selezionata nella pagina **Scheda cod. tracciab. articolo** per il codice di tracciabilità articolo utilizzato dall'articolo).  
-   Collegamenti agli ordini di approvvigionamento creati manualmente o automaticamente per una domanda specifica (collegamenti ordine su ordine).  

Per questi attributi, il sistema di pianificazione applica le seguenti regole:  

-   La domanda con gli attributi specifici può essere soddisfatta solo dall'approvvigionamento con gli attributi corrispondenti.  
-   L'approvvigionamento con attributi specifici può soddisfare una domanda che non richiede specificamente quegli attributi.  

Di conseguenza, se una domanda di attributi specifici non può essere soddisfatta dal magazzino o dagli approvvigionamenti previsti, il sistema di pianificazione suggerirà un nuovo ordine di approvvigionamento per coprire la domanda specifica senza considerare i parametri di pianificazione.  

### <a name="non-specific-attributes"></a>Attributi non specifici  
Gli articoli con numeri seriali/di lotto senza un'impostazione di tracciabilità articolo specifica possono includere numeri seriali/di lotto che non devono necessariamente essere applicati allo stesso esatto numero seriale o di lotto, ma possono essere applicati a un numero seriale o di lotto qualsiasi. Ciò consente al sistema di pianificazione più libertà per associare, ad esempio, una domanda serializzata con un approvvigionamento con un numero seriale, in genere in magazzino.  

La domanda e l'approvvigionamento con i numeri seriali o di lotto, specifici o non specifici, sono considerati di alta priorità e sono quindi esenti dalla zona bloccata, ciò significa che faranno parte della pianificazione anche se la scadenza è precedente alla data di inizio della pianificazione.  

Per ulteriori informazioni, vedere la sezione "I numeri seriali o di lotto vengono caricati dal livello di specifica" in [Dettagli di progettazione - Carico dei profili di magazzino](design-details-loading-the-inventory-profiles.md).  

Per ulteriori informazioni su come il sistema di pianificazione bilancia gli attributi, vedere "I numeri seriali o di lotto e i collegamenti ordine su ordine sono esenti dalla zona bloccata" in [Dettagli di progettazione - Gestione ordini prima della data di inizio pianificazione](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="order-to-order-links"></a>Collegamenti ordine su ordine  
L'approvvigionamento ordine su ordine significa che un articolo viene acquistato, assemblato o prodotto esclusivamente per coprire una domanda specifica. In genere si riferisce ad articoli A e le motivazioni per scegliere questo metodo può essere quello di una domanda poco frequente, un lead time insignificante o la variazione degli attributi necessari.  

Un altro caso particolare che utilizza i collegamenti ordine-a-ordine è quando un ordine di assemblaggio è collegato a un ordine di vendita in uno scenario assemblaggio su ordine.  

I collegamenti ordine su ordine vengono applicati tra la domanda e l'approvvigionamento in quattro modi:  

-   Quando l'articolo pianificato utilizza il metodo di riordino Ordine.  
-   Se si utilizza la politica di produzione Produzione su ordine per creare ordini di produzione di tipo progetto o multilivello (producendo i componenti necessari nello stesso ordine di produzione).  
-   Se si creano ordini di produzione per ordini di vendita con la funzionalità Pianifica ordine vendita.  
-   Durante l'assemblaggio di un articolo a un ordine di vendita. (I criteri di assemblaggio vengono impostati all'assemblaggio su ordine.  

In queste istanze, il sistema di pianificazione suggerirà solo di ordinare la quantità richiesta. Una volta creato, l'ordine di acquisto, di produzione o di assemblaggio continuerà a essere associato alla corrispondente domanda. Ad esempio, se un ordine di vendita viene modificato in tempo o quantità, il sistema di pianificazione suggerirà che l'ordine di approvvigionamento è stato modificato di conseguenza.  

Quando sono presenti collegamenti ordine su ordine, il sistema di pianificazione non include l'approvvigionamento o il magazzino collegato nella procedura di bilanciamento. Spetta all'utente valutare se l'approvvigionamento collegato deve essere utilizzato per coprire un'altra domanda o una nuova e, in questo caso, eliminare l'ordine di approvvigionamento o impegnare manualmente l'approvvigionamento collegato.  

Gli impegni e i collegamenti di tracciabilità ordine verranno interrotti se la situazione diventa impossibile, come lo spostamento della domanda a una data precedente all'approvvigionamento. Tuttavia, il collegamento ordine su ordine si adatta a tutte le modifiche nella rispettiva domanda o nel rispettivo approvvigionamento e non viene mai interrotto.  

## <a name="reservations"></a>Prenotazioni  
Il sistema di pianificazione non include quantità impegnate nel calcolo. Ad esempio, se un ordine di vendita è stato completamente o parzialmente impegnato rispetto alla quantità in magazzino, la quantità impegnata in magazzino non può essere utilizzata per coprire altre domande. Il sistema di pianificazione non include questo set di domanda e approvvigionamento nel calcolo.  

Tuttavia, il sistema di pianificazione includerà ancora le quantità impegnate nel profilo della giacenza disponibile perché tutte le quantità devono essere considerate nella determinazione del superamento del punto di riordino e la quantità di riordino per raggiungere e non superare il livello massimo di magazzino. Di conseguenza, gli impegni inutili condurranno a maggiori rischi che i livelli di magazzino diventino bassi poiché la logica di pianificazione non rileva le quantità impegnate.  

L'esempio seguente mostra come gli impegni possono ostacolare il piano più fattibile.  

![Pianificazione con gli impegni](media/NAV_APP_supply_planning_1_reservations.png "Pianificazione con gli impegni")  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Avvisi  
La prima colonna nel prospetto di pianificazione è dedicata ai campi di avviso. Per ogni riga di pianificazione creata per una situazione insolita viene visualizzata in questo campo un'icona di avviso; fare clic su di essa per ottenere ulteriori informazioni.  

L'approvvigionamento nelle righe di pianificazione con avvisi in genere non viene modificato in base ai parametri di pianificazione. Al contrario, il sistema di pianificazione suggerisce solo un approvvigionamento per coprire la quantità di domanda esatta. Tuttavia, il sistema può essere impostato in modo da rispettare parametri specifici per le righe di pianificazione con determinati avvisi. Per ulteriori informazioni, vedere la descrizione di queste opzioni per il processo batch **Calcola piano - Pianif. magaz.** e per il processo batch **Calcola piano - Approvv. magaz.** rispettivamente.  

Le informazioni di avviso vengono visualizzate nella pagina **Elementi di pianificazione non tracciati**, che viene utilizzata anche per visualizzare i collegamenti di tracciabilità alle entità di rete diversa dagli ordini. Sono disponibili i seguenti tipi di avviso:  

-   Emergenza  
-   Eccezione  
-   Attenzione  

![Avvisi del prospetto di pianificazione](media/NAV_APP_supply_planning_1_warnings.png "Avvisi del prospetto di pianificazione")  

### <a name="emergency"></a>Emergenza  
L'avviso di emergenza è visualizzato in due situazioni:  

-   Quando alla data di inizio pianificazione le giacenze sono negative.  
-   Quando sono presenti eventi di approvvigionamento o domanda arretrati.  

Se le giacenze di un articolo sono negative alla data di inizio pianificazione, il sistema di pianificazione suggerisce un approvvigionamento di emergenza per la quantità negativa che pervenga alla data di inizio pianificazione. Il testo di avviso riporta la data di inizio e la quantità dell'ordine di emergenza. Per ulteriori informazioni, vedere [Dettagli di progettazione: Gestione giacenze negative previste](design-details-handling-projected-negative-inventory.md).  

Tutte le righe di documento con data di scadenza precedente la data di inizio pianificazione sono consolidate in un unico ordine di approvvigionamento di emergenza che pervenga nella data di inizio pianificazione.  

### <a name="exception"></a>Eccezione  
L'avviso di eccezione viene visualizzato se la proiezione delle giacenze disponibili scende al di sotto della scorta di sicurezza. Il sistema di pianificazione suggerisce un ordine di approvvigionamento per soddisfare la domanda alla data di scadenza. Il testo dell'avviso riporta la quantità di scorte di sicurezza dell'articolo e la data in cui è stata intaccata.  

Intaccare la scorta di sicurezza è considerato un'eccezione perché non dovrebbe verificarsi se il punto di riordino è stato impostato correttamente. Per ulteriori informazioni, vedere [Dettagli di progettazione - Il ruolo del punto di riordino](design-details-the-role-of-the-reorder-point.md).  

Le proposte d'ordine eccezionali assicurano che normalmente le scorte disponibili previste non siano mai più basse del livello di scorta di sicurezza. Ciò significa che la quantità proposta sia sufficiente per coprire la scorta di sicurezza, senza considerare i parametri di pianificazione. Tuttavia, in alcuni scenari, verranno presi in considerazione i modificatori di ordine.  

> [!NOTE]  
>  Il sistema di pianificazione potrebbe aver consumato la scorta di sicurezza intenzionalmente, pertanto la rifornirà immediatamente. Per ulteriori informazioni, vedere [La scorta di sicurezza può essere consumata](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Attenzione  
L'avviso di attenzione è visualizzato in tre situazioni:  

-   La data di inizio pianificazione precede la data di lavoro.  
-   La riga di pianificazione suggerisce di cambiare un ordine di acquisto o di produzione rilasciato.  
-   La giacenza disponibile supera il livello di overflow alla data di scadenza. Per ulteriori informazioni, vedere [Dettagli di progettazione: Al di sotto del livello di overflow](design-details-staying-under-the-overflow-level.md).  

> [!NOTE]  
>  Nella pianificazione delle righe con avvisi, il campo **Accetta messaggio errore** non è selezionato perché si prevede che l'addetto alla pianificazione effettui ulteriori indagini su tali righe prima di eseguire il piano.  

## <a name="error-logs"></a>Registri errore  
Nella pagina di richiesta Calcola piano, l'utente può selezionare il campo **Interrompi e mostra primo errore** per interrompere l'esecuzione della pianificazione quando incontra il primo errore. Contemporaneamente verrà visualizzato un messaggio contenente informazioni sull'errore. Se è presente un errore, nel prospetto pianificazione verranno presentate solo le righe di pianificazione create prima dell'individuazione dell'errore.  

Se il campo non è selezionato, il processo batch Calcola piano continuerà fino a completamento. Gli errori non verranno interrotti dal processo batch. Se si verificano uno o più errori, nell'applicazione verrà visualizzato un messaggio al termine, indicante la quantità di articoli interessati da errori. Verrà quindi aperta la pagina **Log errori pianificazione**, in cui saranno disponibili ulteriori dettagli sull'errore e per fornire collegamenti ai documenti interessati o alle schede di impostazione.  

![Messaggi di errore del prospetto di pianificazione](media/NAV_APP_supply_planning_1_error_log.png "Messaggi di errore del prospetto di pianificazione")  

## <a name="planning-flexibility"></a>Flessibilità pianificazione  
Non è sempre pratico pianificare un ordine di approvvigionamento esistente, ad esempio quando viene avviata la produzione o quando viene impiegato del personale aggiuntivo un giorno specifico per svolgere una commessa. Per indicare se un ordine esistente può essere modificato dal sistema di pianificazione, tutte le righe dell'ordine di approvvigionamento dispongono di un campo Flessibilità pianificazione con due opzioni: Illimitata o Nessuna. Se il campo è impostato su Nessuno, il sistema di pianificazione non proverà a modificare la riga dell'ordine di approvvigionamento.  

Il campo può essere impostato manualmente dall'utente, tuttavia, in alcuni casi verrà impostato automaticamente dal sistema. Il fatto che la flessibilità di pianificazione possa essere impostata manualmente dall'utente è importante perché consente di adattare l'utilizzo della funzionalità a flussi di lavoro e casi differenti.  

Per ulteriori informazioni su come viene utilizzato questo campo, vedere [Dettagli di progettazione - Trasferimenti nella pianificazione](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Pianificazione ordini  
Lo strumento di base di pianificazione dell'approvvigionamento rappresentato dalla pagina **Pianificazione ordini** è progettato per un processo decisionale manuale. Non considera i parametri di pianificazione e pertanto non viene ulteriormente discusso in questo documento. Per ulteriori informazioni sulla funzionalità di Pianificazione ordini, fare riferimento alla guida di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Non è consigliabile utilizzare Pianificazione ordini se la società già utilizza i prospetti di pianificazione o di richiesta di approvvigionamento. Gli ordini di approvvigionamento creati mediante la pagina **Pianificazione ordini** possono essere modificati o eliminati durante le esecuzioni automatizzate di pianificazione. Ciò si verifica perché in fase di pianificazione automatica vengono utilizzati parametri di pianificazione che potrebbero non venire presi in considerazione dall'utente che ha creato la pianificazione manuale nella pagina Pianificazione ordini.  

##  <a name="finite-loading"></a>Programmazione limitata  
[!INCLUDE[d365fin](includes/d365fin_md.md)] è un sistema ERP standard, non un sistema di controllo della produzione o del reparto. Consente di pianificare un utilizzo fattibile di risorse fornendo una pianificazione approssimativa, ma non consente di creare e gestire automaticamente pianificazioni dettagliate in base alle priorità o alle regole di ottimizzazione.  

L'utilizzo previsto della funzionalità Risorse critiche è 1) evitare il sovraccarico di risorse specifiche e 2) garantire che nessuna capacità resti senza allocazione se ciò può aumentare il tempo di completamento di un ordine di produzione. La funzionalità non include funzioni o opzioni per assegnare priorità o ottimizzare le operazioni come ci si potrebbe aspettare in un sistema di invio. Tuttavia, può fornire informazioni di capacità approssimative utili per identificare i colli di bottiglia e per evitare il sovraccarico delle risorse.  

Nella pianificazione con risorse vincolate alla capacità, il sistema garantisce che nessuna risorsa venga caricata oltre la propria capacità definita (carico critico). Questa operazione viene effettuata assegnando ogni operazione alla fascia oraria disponibile più vicina. Se la fascia oraria non è sufficiente a completare l'intera operazione, l'operazione verrà divisa in due o più parti e collocate nelle fasce orarie adiacenti disponibili.  

> [!NOTE]  
>  Nel caso che l'operazione venga suddivisa, il tempo di setup viene assegnato una sola volta perché si presuppone che vengano apportate alcune rettifiche manuali per ottimizzare la pianificazione.  

Il tempo di smorzamento può essere aggiunto alle risorse per ridurre al minimo la suddivisione dell'operazione. Ciò consente al sistema di programmare il carico nell'ultimo giorno possibile superando leggermente la percentuale di carico critico se ciò può ridurre il numero di operazioni che vengono suddivise.  

Ciò completa la sintesi dei concetti centrali relativi alla pianificazione di approvvigionamenti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nelle sezioni che seguono questi concetti vengono analizzati in modo più approfondito e inseriti nel contesto delle procedure di pianificazione di base, del bilanciamento tra approvvigionamento e domanda, nonché dell'uso di metodi di riordino.  

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Trasferimenti nella pianificazione](design-details-transfers-in-planning.md)   
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)
