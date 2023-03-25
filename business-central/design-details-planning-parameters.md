---
title: Dettagli di progettazione - Parametri di pianificazione
description: Questo argomento descrive i diversi parametri di pianificazione che puoi utilizzare e il modo in cui influiscono sul sistema di pianificazione.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'planning, design'
ms.date: 07/21/2021
ms.author: edupont
---
# Dettagli di progettazione: Parametri di pianificazione
In questo argomento vengono descritti i diversi parametri di pianificazione che è possibile utilizzare in [!INCLUDE[prod_short](includes/prod_short.md)].  

La modalità in cui l'approvvigionamento degli articoli è controllato dal sistema di pianificazione è determinato da diverse impostazioni nella scheda articolo o della USK e da impostazioni in Setup manufacturing. Nella seguente tabella viene mostrato come vengono utilizzati questi parametri nella pianificazione.  

|Scopo|Parametro|  
|-------------|---------------|  
|Definire se l'articolo deve essere pianificato|Metodo di riordino = Vuoto|  
|Definire quando riordinare|Intervallo di tempo<br /><br /> Punto riordino<br /><br /> Lead time di sicurezza|  
|Definire la quantità da riordinare|Scorta di sicurezza<br /><br /> Metodo di riordino:<br /><br /> -   Qtà Riordino Fissa più Qtà Riordino<br />-   Qtà Massima più Giacenza massima<br />-   Ordine<br />-   Lotto-per-Lotto|  
|Ottimizzare il momento e la quantità di riordino|Periodo di riprogrammazione<br /><br /> Periodo di accumulo lotti<br /><br /> Periodo di stabilizzazione|  
|Modificare gli ordini di approvvigionamento|Quantità minima ordine<br /><br /> Quantità massima ordine<br /><br /> Molteplicità ordine|  
|Delimitare l'articolo pianificato|Politica di produzione:<br /><br /> -   Prod. per Magazzino<br />-   Prod. su Ordine|  

## Definire se l'articolo verrà pianificato  
Per essere incluso nel processo di pianificazione, un articolo/USK deve disporre di un metodo di riordino, altrimenti deve essere pianificato manualmente, ad esempio utilizzando la funzionalità Pianificazione ordini.  

## Definire quando riordinare  
Le proposte di riordino vengono in genere rilasciate solo quando la quantità disponibile prevista è scesa o è inferiore a una quantità specificata. Questa quantità viene definita dal punto di riordino. In caso contrario, sarà uguale a zero. Zero può essere rettificato immettendo una scorta di sicurezza. Se l'utente ha definito un lead time di sicurezza, la proposta verrà consegnata nel periodo precedente alla data di scadenza richiesta.  

Il campo **Intervallo di tempo** viene utilizzato dai criteri dei punti di riordino (**Qtà Riordino Fissa** e **Qtà Massima**), dove il livello del magazzino viene controllato dopo ogni intervallo di tempo. Il primo intervallo di tempo inizia con la data di inizio pianificazione.  

> [!NOTE]  
>  Durante il calcolo degli intervalli di tempo, il sistema di pianificazione ignora i calendari attivi definiti nel campo **Codice calendario base** delle pagine **Informazioni società** e **Scheda Ubicazione**.  

Il lead time di sicurezza predefinito, nella pagina **Setup manufacturing**, deve essere impostato su almeno un giorno. La data di scadenza della domanda può essere nota, ma non l'ora di scadenza. Le righe di pianificazione retrocedono per soddisfare la domanda lorda e, se non viene definito alcun lead time di sicurezza, le merci possono giungere troppo tardi per soddisfare la domanda.  

I seguenti tre campi aggiuntivi relativi al periodo di riordino giocano un ruolo nella definizione del momento in cui eseguire il riordino: **Periodo di riprogrammazione**, **Periodo di accumulo lotti** e **Periodo di stabilizzazione**. Per ulteriori informazioni, vedere [Ottimizzare il momento e la quantità di riordino](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## Definire la quantità da riordinare  
Se il sistema di pianificazione rileva la necessità di un riordino, il metodo di riordino selezionato viene utilizzato per determinare quando e quanto ordinare.  

Indipendentemente dal metodo di riordino, il sistema di pianificazione in genere segue questa logica:  

1. La quantità della proposta d'ordine viene calcolata per soddisfare il livello di magazzino minimo specificato dell'articolo, in genere la quantità di scorta di sicurezza. Se non viene specificato nulla, il livello di magazzino minimo è zero.  
2. Se le scorte disponibili previste sono inferiori alla scorta di sicurezza, viene suggerito un ordine di approvvigionamento retroprogrammato. La quantità ordine riempie almeno la scorta di sicurezza e può essere aumentata dalla domanda lorda entro l'intervallo di tempo, dal metodo di riordino e ai modificatori di ordini.  
3. Se le giacenze previste sono pari o inferiori al punto di riordino (calcolato dalle modifiche aggregate all'interno dell'intervallo di tempo) e superiori alle scorte di sicurezza, viene suggerito un ordine di eccezione programmato in una data successiva. La domanda lorda da soddisfare e il metodo di riordino determineranno la quantità dell'ordine. Al minimo, la quantità dell'ordine soddisfarà il punto di riordino.  
4. Se esiste più domanda lorda dovuta prima della data finale della proposta di ordine programmata in avanti e questa domanda porta le scorte disponibili previste calcolate correntemente al di sotto della scorta di sicurezza, la quantità dell'ordine viene aumentata per coprire il disavanzo. L'ordine di approvvigionamento suggerito viene pianificato a ritroso dalla data di scadenza della domanda lorda che avrebbe violato la scorta di sicurezza.  
5. Se il campo **Intervallo di tempo** non è compilato, verrà aggiunta solo la domanda lorda nella stessa data di scadenza.  

     I seguenti campi relativi al periodo di riordino giocano un ruolo nella definizione della quantità da riordinare: **Periodo di riprogrammazione**, **Periodo di accumulo lotti** e **Periodo di stabilizzazione**. Per ulteriori informazioni, vedere [Ottimizzare il momento e la quantità di riordino](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

### Metodi di riordino  
I seguenti metodi di riordino influiscono sulla quantità da riordinare.  

|Metodo di riordino|Descrizione|  
|-----------------------|---------------------------------------|  
|**Qtà Riordino Fissa**|Al minimo, la quantità dell'ordine sarà uguale alla quantità di riordino. Può essere aumentata per soddisfare la domanda o il livello di magazzino desiderato. Questo metodo di riordino viene in genere utilizzato con un punto di riordino.|  
|**Qtà Massima**|La quantità dell'ordine verrà calcolata per soddisfare la giacenza massima. Se vengono utilizzati i modificatori della quantità, la giacenza massima può essere superata. Non è consigliabile utilizzare l'intervallo di tempo insieme alla quantità massima. L'intervallo di tempo in genere verrà sostituito. Questo metodo di riordino viene in genere utilizzato con un punto di riordino.|  
|**Ordine**|La quantità dell'ordine verrà calcolata per soddisfare ogni singolo evento di domanda e l'insieme di domanda e approvvigionamento rimarrà collegato fino all'esecuzione. Nessun parametro di pianificazione viene considerato.|  
|**Lotto-per-Lotto**|La quantità viene calcolata per soddisfare la somma della domanda che arriva in scadenza nell'intervallo di tempo.|  

##  Ottimizzare il momento e la quantità di riordino  
Per ottenere un piano di approvvigionamento razionale, un responsabile ottimizzerà i parametri di pianificazione per limitare i suggerimenti di ripianificazione, l'accumulo della domanda (quantità di riordino dinamica) o per evitare azioni di pianificazione non significative. I seguenti campi relativi al periodo di riordino aiutano a ottimizzare il riordino in termini di tempo e quantità.  

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Periodo di riprogrammazione**|Questo campo viene utilizzato per determinare se il messaggio di azione deve ripianificare un ordine esistente o annullarlo e creare un nuovo ordine. L'ordine esistente verrà riprogrammato all'interno di un periodo di riprogrammazione prima dell'approvvigionamento corrente e fino a un periodo di riprogrammazione dopo l'approvvigionamento corrente.|  
|**Periodo di accumulo lotti**|Con il metodo di riordino lotto per lotto, questo campo viene utilizzato per accumulare più esigenze di approvvigionamento in un unico ordine di approvvigionamento. A partire dal primo approvvigionamento pianificato, il sistema accumula tutte le necessità di approvvigionamento nel periodo di accumulo lotti in un approvvigionamento, che viene inserito nella data del primo approvvigionamento. La domanda esterna al periodo di accumulo lotto non è coperta da questo approvvigionamento.|  
|**Periodo di stabilizzazione**|Questo campo viene utilizzato per evitare la riprogrammazione secondaria di un approvvigionamento esistente nel tempo. Le modifiche a partire dalla data di approvvigionamento fino a un periodo di stabilizzazione dalla data di approvvigionamento non genereranno messaggi di azione.<br /><br /> Il periodo di stabilizzazione specifica un periodo di tempo durante il quale non deve essere proposta alcuna ripianificazione degli ordini di approvvigionamento esistenti. Ciò limita il numero di inutili ripianificazioni dell'approvvigionamento esistente a una data successiva se la data riprogrammata è compresa nel periodo di stabilizzazione.<br /><br /> Di conseguenza, un delta positivo tra la nuova data di approvvigionamento suggerita e la data di approvvigionamento originale sarà sempre maggiore del periodo di stabilizzazione.|  
> [!NOTE]
> Con il metodo di riordino lotto per lotto, il valore del campo **Periodo di accumulo lotti** deve essere uguale o superiore rispetto al valore del campo **Periodo di stabilizzazione**. In caso contrario, il periodo di stabilizzazione verrà automaticamente ridotto durante la procedura di pianificazione in base al periodo di accumulo lotti.  

I tempi del periodo di riprogrammazione, del periodo di stabilizzazione e del periodo di accumulo lotti sono basati su una data di approvvigionamento. L'intervallo di tempo si basa sulla data di inizio della pianificazione, come indicato nell'illustrazione seguente.  

![Elementi dell'intervallo di tempo.](media/supply_planning_5_time_bucket_elements.png "Elementi dell'intervallo di tempo")  

Negli esempi che seguono, le frecce nere rappresentano l'approvvigionamento (su) e la domanda (giù) esistenti. Le frecce rosse, verdi e arancioni sono suggerimenti di pianificazione.  

**Esempio 1**: la data modificata si trova al di fuori del periodo di riprogrammazione, ciò causa l'annullamento dell'approvvigionamento esistente. Un nuovo approvvigionamento viene suggerito per soddisfare la domanda nel periodo di accumulo lotti.  

![Periodo di riprogrammazione e periodo di accumulo lotti.](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "Periodo di riprogrammazione e periodo di accumulo lotti")  

**Esempio 2**: la data modificata si trova nel periodo di riprogrammazione, ciò causa la riprogrammazione dell'approvvigionamento esistente. Un nuovo approvvigionamento viene suggerito per soddisfare la domanda al di fuori del periodo di accumulo lotti.  

![Periodo di riprogrammazione, periodo di accumulo lotti e riprogrammazione.](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "Periodo di riprogrammazione, periodo di accumulo lotti e riprogrammazione")  

**Esempio 3**: esiste una domanda nel periodo di stabilizzazione e la quantità di approvvigionamento nel periodo di accumulo lotti corrisponde alla quantità dell'approvvigionamento. La domanda successiva è scoperta e viene suggerito un nuovo approvvigionamento.  

![Periodo di stabilizzazione e periodo di accumulo lotti.](media/supply_planning_5_dampener_period_lot_accumulation_period.png "Periodo di stabilizzazione e periodo di accumulo lotti")  

**Esempio 4**: esiste una domanda nel periodo di stabilizzazione e l'approvvigionamento resta nella stessa data. Tuttavia, la quantità di approvvigionamento corrente non è sufficiente a soddisfare la domanda nel periodo di accumulo lotti, pertanto viene suggerita un'azione di modifica della quantità dell'ordine di approvvigionamento esistente.  

![Periodo di stabilizzazione, periodo di accumulo lotti e quantità di modifica.](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "Periodo di stabilizzazione, periodo di accumulo lotti e quantità di modifica")  

**Valori predefiniti:** il valore predefinito del campo **Intervallo di tempo** e i tre campi relativi al periodo di riordino sono vuoti. Per tutti i campi, a eccezione del campo **Periodo di stabilizzazione**, ciò significa 0D (zero giorni). Se il campo **Periodo di stabilizzazione** è vuoto, verrà utilizzato il valore globale nel campo **Periodo di stabilizzazione di default** della pagina **Setup manufacturing**.  

## Modificare gli ordini di approvvigionamento  
Una volta che la quantità della proposta di ordine è stata calcolata, uno o più i modificatori di ordini possono rettificarla. Ad esempio, la quantità ordine massima è più grande o uguale alle quantità ordine minima , che è più grande o uguale al molteplicità ordine.  

La quantità viene diminuita se supera la quantità massima ordine. Quindi, viene aumentata se è inferiore alla quantità minima ordine. Infine, viene arrotondato in modo che corrisponda a una molteplicità ordini specificata. Qualsiasi quantità residua utilizza le stesse rettifiche fino a che la domanda totale non è stata convertita nelle proposte di ordine.  

## Delimitare l'articolo  
L'opzione **Politica di produzione** definisce quali ordini aggiuntivi saranno proposti dal calcolo MRP.  

Se viene utilizzata l'opzione **Prod. per Magazzino**, gli ordini riguarderanno solo l'articolo in questione.  

Se viene utilizzata l'opzione **Prod. su ordine**, il sistema di pianificazione analizzerà la DB di produzione dell'articolo e creerà delle proposte di ordine collegate aggiuntive per questi articoli di livello inferiore che sono definite anche come produzione su ordine. Questo processo continua fintanto che sono presenti articoli di tipo produzione su ordine nelle strutture DB decrescenti.

## Usare codici di ultimo livello per gestire la domanda derivata

Utilizzare i codici di ultimo livello per far avanzare la domanda derivata di componenti fino ai livelli inferiori della distinta base. Per una spiegazione più approfondita di questo concetto, vedere [Priorità articolo/Codice ultimo livello](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

È possibile assegnare un codice di ultimo livello a ogni parte della struttura di prodotto o nella distinta base interna. Il livello di assemblaggio superiore finale viene indicato come livello 0, ossia come articolo finale. Più alto è il numero del codice di ultimo livello, più basso è l'articolo nella gerarchia. Ad esempio, gli articoli finali hanno un codice di ultimo livello 0 e le parti di articolo che vanno nell'assemblaggio hanno codici di ultimo livello 1, 2, 3 e così via. Il risultato è che la pianificazione delle parti dei componenti viene coordinata in base alle necessità di tutti i numeri di parte di alto livello. Quando si calcola una pianificazione, la distinta base viene espansa nel prospetto di pianificazione e le domande lorde per il livello 0 vengono passate ai livelli di pianificazione sottostanti come domande lorde per il successivo livello di pianificazione.

Selezionare il campo **Codice dinamico di ultimo livello** per specificare se assegnare e calcolare immediatamente i codici di ultimo livello per ogni componente nella struttura del prodotto. Se la quantità di dati è considerevole, è possibile che tale funzione produca effetti negativi sulle prestazioni del sistema, ad esempio durante la registrazione automatica dei costi. Non essendo una funzione retroattiva, è opportuno considerarne l'uso in anticipo.

In alternativa al calcolo automatico che viene effettuato in modo dinamico quando il campo viene selezionato, è possibile eseguire il processo batch **Calcolo codice ultimo livello** dal menu **Manufacturing** facendo clic su **Progettazione prodotto**, **Calcolo codice ultimo livello**.

> [!IMPORTANT]
> Se non viene selezionato il campo **Cod. ultimo livello dinamico**, allora è necessario eseguire il processo batch **Calcolo codice ultimo livello** prima di calcolare un piano di approvvigionamento (processo batch **Calcola piano**).  

> [!NOTE]
> Anche con il campo **Cod. ultimo livello dinamico** selezionato, i codici di ultimo livello degli articoli componenti non vengono modificati dinamicamente se una distinta base di produzione padre viene eliminata o impostata come non certificata. Ciò può causare difficoltà nell'aggiunta di nuovi articoli alla fine della struttura del prodotto poiché può risultare superato il numero massimo di codici di ultimo livello. Pertanto, per le strutture di prodotti di grandi dimensioni che raggiungono il limite dei codici di ultimo livello, è consigliabile eseguire frequentemente il processo batch **Calcolo cod. ultimo livello** per mantenere la struttura.  

### Ottimizzare il calcolo del codice di ultimo livello

Selezionare il campo **Ottimizza il calcolo del codice di ultimo livello** per specificare che si desidera utilizzare il nuovo metodo più veloce di calcolo del codice di ultimo livello. Si noti che il nuovo calcolo viene eseguito in modo diverso e il suo utilizzo potrebbe interrompere le estensioni che si basano sul metodo esistente. Il nuovo metodo di calcolo sostituirà il metodo attuale in una versione futura.

## Vedere anche  
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]