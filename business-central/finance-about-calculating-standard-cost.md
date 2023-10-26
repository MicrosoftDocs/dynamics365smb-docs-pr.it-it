---
title: Informazioni sul calcolo del costo standard
description: In un sistema di costi standard il costo unitario di magazzino viene determinato in base a un costo previsto o costo previsto.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
---
# <a name="about-calculating-standard-cost"></a>Informazioni sul calcolo del costo standard

Molte aziende di produzione scelgono una base di valutazione del costo standard. Ciò si applica anche alle società che eseguono la produzione leggera, come assemblaggio e kitting. In un sistema di costi standard il costo unitario di magazzino viene determinato in base a un costo previsto o costo previsto. Gli studi del costo passato e di quello futuro previsto forniscono la base per i costi standard. Questi costi sono congelati fino a quando non si decide di cambiarli. Il costo effettivo per la produzione di un prodotto può essere diverso dai costi standard previsti. Per consentire il controllo della gestione, il costo effettivo viene messo a confronto con il costo standard di un articolo specifico e le differenze, o *scostamenti*, vengono identificate e analizzate.  

I costi standard possono essere gestiti per articoli il cui rifornimento viene effettuato tramite acquisto, assemblaggio e produzione. Per ciascun metodo di rifornimento, i costi standard possono essere costituiti dai seguenti elementi.  

|Sistema di rifornimento|Elementi di costo standard|  
|--------------------------|----------------------------|  
|**Acquisto**|Costo diretto del materiale e costi generali di materiale se necessari.|  
|**Assemblaggio**|Costo diretto del materiale, costo di manodopera diretto o fisso e costo generale.|  
|**Ordine Produzione**|Costo diretto del materiale, costo di manodopera, costo di terzisti e costo generale.|  

## <a name="setting-up-standard-costs"></a>Impostazione dei costi standard

Poiché il costo standard di un articolo lavorato o assemblato è costituito da più elementi di costo, ovvero costi relativi a materiale, capacità e terzisti (diretti e generali), i costi standard devono essere stabiliti per ognuno di questi elementi.  

L'attività contabile di un'azienda di elaborazione articoli che utilizza il calcolo del costo standard è:  

- Stimare il costo standard di un articolo finito e impostarlo nella scheda articolo.  
- Registrare e allocare il costo effettivo degli elementi del costo chiave e rendere conto in modo appropriato degli scostamenti.  

Per determinare il costo diretto di un articolo finito, è necessario calcolare il totale dei costi di tutti i componenti. Un articolo assemblato o prodotto può includere sottoassemblaggi, anch'essi costituiti da più componenti.  

I seguenti elementi di costo principali compongono il costo diretto totale di un articolo elaborato completato:  

- Costi materiali.  
- Costo capacità.  
- Costo per conto lavoro solo per gli articoli prodotti.  

### <a name="material-costs"></a>Costi materiale

I costi del materiale sono quelli associati ai subassemblaggi e alle materie prime acquistate. Il costo unitario del materiale può essere costituito da elementi di costo diretti e indiretti.  

- Il costo diretto del materiale rappresenta un importo fatturato per le materie prime acquistate o il costo di produzione di un subassemblaggio.  
- Il costo indiretto del materiale, o *costo generale*, può rappresentare elementi, quali, i costi di gestione del magazzino per l'articolo finito, dopo la produzione.  

L'impostazione del costo del materiale per gli articoli acquistati in relazione al costo diretto o indiretto dipende dal metodo di costing selezionato per l'articolo specificato. Le informazioni sui costi vengono impostate per tutti i metodi di costo nella scheda articolo. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).

Il costo dello scarto (solo produzione) è un altro fattore da prendere in considerazione per la determinazione del costo totale del materiale. Quando viene scartata una determinata quantità di materie prime durante l'assemblaggio o la produzione di un articolo, in genere la quantità dei componenti necessari per produrre l'articolo aumenta. Questo, a sua volta, provoca un aumento del costo del materiale dei componenti consumati per la produzione di un articolo principale. Impostare i costi dello scarto per i materiali nel ciclo o nella DB di produzione.  

Il costo del materiale di un articolo prodotto può essere rappresentato in due modi che corrispondono alle basi di calcolo del costo seguenti.  

|Base di calcolo del costo|Calcolo del costo del materiale|  
|----------------------------|-------------------------------|  
|Livello Singolo|L'articolo prodotto è uguale al costo totale di tutti gli articoli acquistati o sottoassemblati nella DB di produzione di tale articolo.|  
|Livello o multilivello di ricalcolo|L'articolo prodotto è la somme dei costi del materiale di tutti i subassemblaggi nella distinta base dell'articolo in questione e del costo di tutti gli articoli acquistati nella distinta base dell'articolo in questione.|  

### <a name="capacity-costs"></a>Costi della capacità

I costi capacità sono quelli associati alla manodopera interna e ai costi dei macchinari. È necessario impostare questi costi per ogni risorsa (in gestione assemblaggio) e area di produzione o centro di lavoro nel ciclo (in produzione). Come nel caso dei materiali, è possibile identificare sia elementi diretti che indiretti del costo della capacità. Il costo diretto di un'area di lavoro può ad esempio essere costituito dalla tariffa del reparto produzione stabilita per eseguire una funzione specifica. Il costo indiretto di un'area di lavoro può rappresentare alcune spese generali della fabbrica, ad esempio l'illuminazione, il riscaldamento e così via. Analogamente ai costi del materiale, è possibile esprimere i costi generali capacità come percentuale dei costi indiretti o coefficiente fisso dei costi generali.  

L'impostazione dei costi capacità degli articoli assemblati è costituita dai seguenti elementi:  

- Costo unitario diretto e indiretto della risorsa.  
- Tipo fisso o diretto dell'utilizzo delle risorse.  

L'impostazione dei costi capacità degli articoli prodotti è costituita dai seguenti elementi:  

- Costo unitario diretto e indiretto del centro di lavoro o area di produzione.  
- Impostazione dei tempi e della dimensione del lotto.  

Per calcolare il costo standard della capacità, è necessario stabilire le tariffe orarie standard richieste per eseguire operazioni nelle aree di produzione e nei centri di lavoro. Il tempo totale per completare un'operazione è costituito in genere dal tempo di setup e da quello di lavorazione, nonché dal tempo di attesa e da quello di spostamento.  

Impostare le tariffe per ognuno di questi tipi di tempo per ogni centro di lavoro o per ogni area di produzione in un singolo ciclo.  

> [!NOTE]  
>  Mentre le tariffe per i tempi di lavorazione si applicano a ogni singolo articolo prodotto, quelle per il tempo di setup si applicano a ogni lotto. Il tempo di setup del ciclo per ogni operazione deve pertanto essere diviso in modo proporzionale alla dimensione del lotto. Specificare la dimensione del loro nel campo corrispondente della Scheda dettaglio **Rifornimento** nella pagina **Scheda articolo**.  

Per specificare il tempo di setup nel ciclo per la pianificazione senza includere questa spesa nel calcolo del costo standard, deselezionare il campo **Costi setup incluso** nella pagina **Setup manufacturing**.  

A livello singolo, si tratta del costo della manodopera necessaria per produrre l'articolo finito, specificato nel ciclo dell'articolo di produzione. A più livelli, si tratta del costo della capacità specificato per ogni singolo articolo prodotto incluso nella distinta base dell'articolo principale.  

### <a name="subcontractor-costs"></a>Costi dei terzisti

I costi dei terzisti sono quelli associati ai servizi forniti da terzisti o fornitori esterni di un'azienda. Analogamente ai costi del materiale e della capacità, i costi dei terzisti possono essere costituiti da importi sia di costi diretti che generali. I costi diretti dei terzisti rappresentano l'addebito effettivo per ogni unità di servizio fornito. I costi generali dei terzisti possono, ad esempio, rappresentare i costi di spedizione e di gestione sostenuti dall'azienda in relazione a un ordine in conto lavoro.  

Poiché il conto lavoro rappresenta essenzialmente una capacità esterna, il costo, diretto e indiretto, dei servizi in conto lavoro viene impostato nella scheda area di produzione che rappresenta l'operazione di affidamento in conto lavoro.  

## <a name="updating-standard-costs"></a>Aggiornamento dei costi standard

Per aggiornare o calcolare il costo standard degli articoli di assemblaggio, utilizzare la funzione dalla scheda articolo.  

Il processo di aggiornamento o del calcolo dei costi standard in genere è costituito dai task seguenti:  

1.  Aggiornamento dei costi ai livelli di capacità e componente. Per ulteriori informazioni, vedere i processi batch **Suggerisci costo std. articolo** e **Suggerisci costo standard capacità**.  
2.  Consolidamento e roll up dei costi dei componenti e della capacità per calcolare il costo totale di assemblaggio o di produzione degli articoli. Per ulteriori informazioni, vedi la sezione [Per calcolare il costo standard di un articolo di assemblaggio](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Implementazione dei costi standard che vengono registrati quando si eseguono i processi batch precedenti. I costi standard non saranno effettivi finché non vengono implementati. Usa il processo batch **Implementa modifiche costo std.** che consente di aggiornare il costo standard degli elementi riportati nella tabella Prospetto costo standard.  
4.  Implementazione delle modifiche per aggiornare il campo **Costo unitario** nella scheda articolo ed eseguire la rivalutazione di magazzino. Per ulteriori informazioni, vedere [Rivalutare il magazzino](inventory-how-revalue-inventory.md).

## <a name="use-batch-jobs-to-update-standard-costs"></a>Utilizzare processi batch per aggiornare costi standard
Le seguenti sezioni descrivono i processi batch che puoi utilizzare per aggiornare costi standard.
### <a name="suggest-item-standard-cost"></a>Suggerisci costo std. articolo

 Crea suggerimenti per la variazione dei costi e le quote dei costi standard nelle schede articolo. Una volta completato il processo batch, puoi visualizzare il risultato nella finestra Prospetto costo standard.

> [!NOTE]  
> Questo processo batch è destinato solo agli articoli acquistati. Se vuoi aggiornare un articolo con una distinta base di produzione o di assemblaggio, devi innanzitutto compilare il prospetto inserendo tutti i componenti e successivamente eseguire il processo batch Roll up del costo standard.

Questo processo batch crea solo suggerimenti. Non implementa le modifiche suggerite. Se i suggerimenti vengono ritenuti soddisfacenti e desideri implementarli, ovvero aggiornarli nelle schede articolo e inserirli in Registrazioni rivalutazioni, seleziona Implementa modifiche costo std. nella finestra Prospetto costo standard.
#### <a name="options"></a>Opzioni

**Costo Standard**: immetti il fattore di rettifica da utilizzare per aggiornare il costo standard. È anche possibile selezionare un metodo di arrotondamento per il nuovo costo standard. È necessario compilare il campo utilizzando un valore decimale per l'aumento percentuale, ad esempio 1,1.

**% costi indiretti**: immetti il fattore di rettifica da utilizzare per aggiornare la percentuale dei costi indiretti. È anche possibile selezionare un metodo di arrotondamento per la nuova percentuale dei costi indiretti. È necessario compilare il campo utilizzando un valore decimale per l'aumento percentuale, ad esempio 1,1.

**Coefficiente costi generali**: immetti il fattore di rettifica da utilizzare per aggiornare il coefficiente costi generali. Puoi anche selezionare un metodo di arrotondamento per il nuovo coefficiente costi generali. È necessario compilare il campo utilizzando un valore decimale per l'aumento percentuale, ad esempio 1,1.

### <a name="suggest-workmach-ctr-std-cost"></a>Sugg. costo std centro lav/area prod

Crea suggerimenti per la variazione dei costi e le quote dei costi standard nelle schede area di produzione, centri lavoro o risorse. Una volta completato il processo batch, puoi vedere il risultato nella finestra **Prospetto costo standard**.

Questo processo batch crea solo suggerimenti. Non implementa le modifiche suggerite. Se i suggerimenti sono soddisfacenti e desideri implementarli, ovvero aggiornarli nel centro di lavoro e nelle schede risorse e inserirli nella finestra Registrazioni rivalutazioni, seleziona **Implementa modifiche costo std.** nella finestra **Prospetto costo standard**.

Se dopo aver eseguito il processo batch desideri controllare l'impatto sulla produzione, o sui reparti assemblaggio, esegui il processo batch **Roll up del costo standard** per aggiornare i costi standard a livello di aree di produzione, centri di lavoro, risorse di assemblaggio e distinte base di produzione.
#### <a name="options-1"></a>Opzioni
**Costo Standard**: immetti il fattore di rettifica da utilizzare per aggiornare il costo standard. È anche possibile selezionare un **metodo di arrotondamento** per il nuovo costo standard. È necessario compilare il campo utilizzando un valore decimale per l'aumento percentuale, ad esempio 1,1.

**% costi indiretti**: immetti il fattore di rettifica da utilizzare per aggiornare la percentuale dei costi indiretti. È anche possibile selezionare un metodo di arrotondamento per la nuova percentuale dei costi indiretti. È necessario compilare il campo utilizzando un valore decimale per l'aumento percentuale, ad esempio 1,1.

**Coefficiente costi generali**: immetti il fattore di rettifica da utilizzare per aggiornare il coefficiente costi generali. Puoi anche selezionare un metodo di arrotondamento per il nuovo coefficiente costi generali. È necessario compilare il campo utilizzando un valore decimale per l'aumento percentuale, ad esempio 1,1.

### <a name="post-inventory-cost-to-gl"></a>Registra costo magazzino in C/G

 Registra le modifiche alle quantità e al valore del magazzino nei movimenti contabili articoli e nei movimenti di valorizzazione quando registri transazioni di magazzino, ad esempio spedizioni vendite o carichi di acquisto.

A meno che non sia selezionata la casella di controllo **Reg. automatica costi** nella finestra **Setup magazzino**, i costi di magazzino non vengono registrati in modo dinamico nella contabilità generale e i costi COGS non sono calcolati con una vendita. Di conseguenza, devi registrare manualmente il processo batch nella contabilità generale eseguendo il processo batch **Registra costo magazzino in C/G** per eseguire l'aggiornamento della contabilità generale e stampare potenzialmente un report dei movimenti di valorizzazione registrati.

Il processo batch utilizza i movimenti di valorizzazione come base. Per calcolare il valore da registrare, utilizza la differenza tra i campi **Importo costo (effettivo)** e **Costo registrato in C/G** nei movimenti di valorizzazione. Se è stata selezionata la casella di controllo **Reg. costi previsti in C/G** nella finestra **Setup magazzino**, il processo batch registra anche la differenza tra il campo **Importo costo (previsto)** e il campo **Costo prev. reg. in C/G** in conti provvisori nella contabilità generale.

> [!NOTE]
> Se non hai selezionato la casella di controllo **Reg. costi previsti in C/G** nel campo della finestra **Setup magazzino**, l'ultima sezione del report elencherà i movimenti di valorizzazione precedentemente ignorati in quanto rappresentano i costi previsti.

> [!NOTE] 
> Se nel processo batch si verifica un errore relativo alle dimensioni o al loro setup, l'errore viene ignorato e il movimento viene registrato nella contabilità generale utilizzando le dimensioni del movimento di valorizzazione.

Per fare in modo che non si verifichino errori durante l'elaborazione del processo batch, puoi eseguire il report **Registra costo mag. in C/G - Test** per visualizzare tutti gli errori che potrebbero verificarsi. Puoi quindi correggere gli errori ed eseguire il processo batch **Registra costo magazzino in C/G** con la certezza che tutti i movimenti verranno elaborati.
 
> [!IMPORTANT]  
> Prima di utilizzare questo processo batch, esegui il processo batch **Rettifica costo - Mov. art**. In questo modo, all'esecuzione del processo batch i costi che verranno registrati nella contabilità generale saranno aggiornati.
#### <a name="options-2"></a>Opzioni

|Opzione  |Descrizione  |
|--------------|---------|
|**Metodo di registrazione**|il processo batch consente di registrare il valore di magazzino nella contabilità generale per categoria di registrazione o per movimento registrato. Se si effettua la registrazione in base ai movimenti, si ottiene una specifica dettagliata degli effetti del magazzino sulla contabilità generale, ma si creano anche numerosi movimenti C/G. Se effettui la registrazione in base alla categoria di registrazione, il processo batch crea un movimento C/G per combinazione di data di registrazione e categoria di registrazione. Questo significa che viene creato un movimento C/G per ogni combinazione di data di registrazione, categoria di registrazione business, categoria di registrazione di articoli o servizi, categoria di registrazione magazzino e codice ubicazione. Il processo batch crea inoltre movimenti C/G separati per costi con segni diversi.|
|**Nr. Documento**|in questo campo puoi immettere un numero di documento se hai selezionato il metodo di registrazione per categoria di magazzino. Il numero di documento appare nei movimenti registrati.|
|**Registra**|Seleziona questo campo se vuoi registrare automaticamente il processo batch nella contabilità generale. Se non scegli di registrare il costo di magazzino nella contabilità generale, tramite il processo batch verrà stampato solo un report di test in cui sono riportati i valori che possono essere registrati nella contabilità generale e su cui è presente l'indicazione **Report test (non registrato)**.|

### <a name="roll-up-standard-cost"></a>Roll up del costo standard

Esegue il roll up dei costi standard di articoli assemblati e lavorati. Questi sono influenzati dalla variazione nei costi standard dei componenti suggerita dal processo batch **Suggerisci costo std. articolo**. Inoltre, vengono influenzati dalla variazione del costo standard delle risorse di assemblaggio e della capacità di produzione suggerita dal processo batch **Sugg. costo std centro lav/area prod**.

Quando si effettua il roll-up dopo aver eseguito uno o entrambi i processi batch, tutte le modifiche apportate ai costi standard nel prospetto verranno introdotte nelle distinte base di produzione o assemblaggio associate e i costi verranno applicati in ogni livello della distinta base.

> [!NOTE] 
> Questa funzione esegue il roll-up solo del costo standard nelle schede articolo, non nelle schede USK.

Questo processo batch crea solo suggerimenti. Non implementa le modifiche suggerite. Se ritieni i suggerimenti soddisfacenti e desideri implementarli, ovvero aggiornarli nelle schede articolo e inserirli nella finestra **Registrazioni rivalutazioni**, puoi usare il processo batch **Implementa modifiche costo std.**. Puoi accedere a questo processo batch dalla finestra **Prospetto costo standard**.
#### <a name="options-3"></a>Opzioni

**Data calcolo**: immetti la data relativa alla versione della distinta base di produzione per la quale desideri eseguire il roll-up.
 
### <a name="implement-standard-cost-change"></a>Implem. modifiche costo std.

Aggiorna il costo standard riportato nella tabella **Articolo** in base alle modifiche suggerite nella tabella **Prospetto costo standard**. I suggerimenti per le modifiche dei costi standard possono essere creati mediante il processo batch **Suggerisci costo std. articolo** e/o **Sugg. costo std centro lav/area prod** e anche essere modificati. Il contenuto di tutti i campi dei suggerimenti di modifica dei costi standard verrà trasferito. Quando implementi i suggerimenti, puoi vedere le modifiche dei costi standard nella scheda articolo e/o nella scheda area di produzione o centro di lavoro. Viene inoltre creata una registrazione di rivalutazione per l'aggiornamento del valore dello stock esistente.
#### <a name="options-4"></a>Opzioni

**Data di registrazione**: immetti la data in cui deve essere eseguita la rivalutazione.

**Nr. documento**: immetti il numero delle righe delle registrazioni di rivalutazione. Se nel campo Nome Batch Registrazioni Magazzino è indicata una numerazione, il numero del documento riflette i movimenti contabili creati dalla contabilizzazione delle registrazioni rivalutazioni. In caso contrario, è possibile immettere un numero manualmente.

**Def. reg. magazzino**: immetti il nome della definizione delle registrazioni rivalutazioni.

**Nome batch registrazioni magazzino**: immetti il nome delle registrazioni rivalutazioni effettive

Seleziona **OK** per avviare il processo batch. Se non vuoi eseguire il processo batch subito, seleziona **Annulla** per chiudere la finestra.

## <a name="see-also"></a>Vedere anche

[Dettagli di progettazione: metodi di determinazione dei costi](design-details-costing-methods.md)  
[Aggiornare i costi standard](finance-how-to-update-standard-costs.md)  
[Dettagli di progettazione: determinazione dei costi di inventario](design-details-inventory-costing.md)  
[Utilizzare le distinte base di assemblaggio](assembly-how-work-assembly-boms.md)  
[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
