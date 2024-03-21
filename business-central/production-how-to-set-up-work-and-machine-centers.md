---
title: Impostare aree di produzione e centri di lavoro
description: 'Una scheda Area di produzione consente di organizzare i valori e i requisiti fissi della risorsa di produzione e, quindi, di gestire l''output della produzione effettuata in tale area di produzione.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-work-centers-and-machine-centers"></a>Impostare aree di produzione e centri di lavoro

L'applicazione distingue tra tre tipi di capacità. Questi sono disposti in modo gerarchico. Ogni livello contiene i livelli inferiori.  

Il livello più alto è rappresentato dal reparto di produzione. Ai reparti di produzione vengono assegnate le aree di produzione. Ogni area di produzione può far parte di un solo reparto di produzione.

A ogni area di produzione è possibile assegnare diversi centri di lavoro. Un centro di lavoro può far parte di una sola area di produzione.  

La capacita pianificata di un'area di produzione consiste della disponibilità dei centri di lavoro corrispondenti oltre che della disponibilità pianificata dell'area stessa. La disponibilità pianificata di un reparto di produzione è data quindi dalla somma di tutte le disponibilità delle relative aree di produzione e dei relativi centri di lavoro.  

La disponibilità viene memorizzata nei movimenti di calendario.  

> [!IMPORTANT]
> Prima di impostare le aree di produzione o i centri di lavoro, è necessario impostare calendari del reparto produzione. Per ulteriori informazioni, vedere [Creare calendari del reparto produzione](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a>Per impostare un'area di produzione

Di seguito viene descritto come impostare un'area di produzione. I passaggi per impostare un calendario centro di lavoro sono gli stessi ad eccezione della Scheda dettaglio **Setup cicli**.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Aree di produzione**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nel campo **Gruppo aree di produzione** selezionare il raggruppamento di risorse di livello più alto in base a cui è organizzata l'area di produzione, se pertinente. Scegliere l'azione **Nuovo** nell'elenco a discesa.  
5. Nel campo **Area di produzione alternativa**, seleziona l'area di produzione da utilizzare se questo centro di lavoro non è disponibile o quando la domanda supera la sua capacità. L'area di produzione alternativa è solo a scopo informativo e non è inclusa automaticamente nei processi di pianificazione.
6. Selezionare il campo **Bloccato** se si desidera evitare che l'area di produzione venga utilizzata in qualsiasi elaborazione. In tal caso, non sarà quindi possibile registrare l'output per un articolo prodotto nell'area di produzione. Per ulteriori informazioni, vedere [Registrare l'output di produzione](production-how-to-post-output-quantity.md).
7. Nel campo **Costo Unitario Diretto** specificare il costo di produzione di un'unità di misura nell'area di produzione selezionata, escludendo altri elementi di costo. Tale valore viene spesso definito *costo diretto manodopera*.  
8. Nel campo **% costi indiretti** specificare il costo operativo generale dell'utilizzo dell'area di produzione come percentuale del costo unitario diretto. Tale importo percentuale viene aggiunto al costo diretto nel calcolo del costo unitario.  
9. Nel campo **Coeff. costi generali** specificare come importo assoluto qualunque costo non operativo, ad esempio le spese di manutenzione, dell'area di produzione.  

    Il campo **Costo Unitario** contiene il costo unitario calcolato della produzione di un'unità di misura nell'area di produzione specificata, inclusi tutti gli elementi di costo, come illustrato di seguito:  

    Costo Unitario = Costo Unitario Diretto + (Costo Unitario Diretto x % Costi Indiretti) + Coeff. Costi Generali.  

10. Nel campo **Calcolo costo unitario** specificare se basare il calcolo precedente sulla quantità di tempo utilizzata, ovvero **Ora**, o sul numero di unità prodotte, ovvero **Unità**.  
11. Selezionare il campo **Costo unitario specifico** se si desidera definire il costo unitario dell'area di produzione nella riga ciclo in cui viene utilizzato. Tale soluzione potrebbe risultare utile per le operazioni che prevedono costi delle capacità notevolmente diversi rispetto a quelli consueti per l'area di produzione specificata.  
12. Nel campo **Metodo consuntivazione** specificare se calcolare e registrare registrazione di output nell'area di produzione manualmente o automaticamente, mediante uno dei metodi seguenti.

    |Opzione|Descrizione|
    |------|-----------|
    |**Manuale**| Il tempo utilizzato, l'output e lo scarto vengono registrati manualmente nelle registrazioni di output o di produzione.|
    |**Da inizio ordine**|L'output viene registrato automaticamente quando l'ordine di produzione viene rilasciato.|
    |**Aut. fine**|L'output viene registrato automaticamente quando l'ordine di produzione viene terminato.|

    > [!NOTE]
    > Se necessario, il metodo per il calcolo del consumo selezionato qui può essere sostituito per singole operazioni, mediante la modifica delle impostazioni delle righe ciclo

13. Nel campo **Cod. Unità di Misura** immettere l'unità di tempo utilizzata per il calcolo del costo dell'area di produzione specificata e per la programmazione della capacità.
    Per tenere costantemente sotto controllo il consumo, è necessario innanzitutto impostare un metodo di misura. Le unità immesse sono unità di base. Ad esempio, il tempo di elaborazione viene misurato in ore e minuti.

    > [!NOTE]  
    > Se si decide di utilizzare Giorni, tenere presente che un giorno equivale a 24 ore e non a 8 ore lavorative.

14. Il campo **Capacità** consente di specificare se nell'area di produzione sono disponibili più macchinari o persone che lavorano contemporaneamente. Se nell'installazione di [!INCLUDE[prod_short](includes/prod_short.md)] non è inclusa la funzionalità Centro di lavoro, è necessario che il valore di questo campo sia impostato su **1**.  
15. Specificare nel campo **Efficienza** la percentuale di output standard previsto prodotta effettivamente dall'area di produzione selezionata. Se si immette un valore pari a **100**, si indica che l'output effettivo dell'area di produzione corrisponde all'output standard.  
16. Selezionare la casella di controllo **Calendario consolidato** se si utilizzano anche centri di lavoro. In questo modo viene eseguito il roll up dei movimenti di calendario dai calendari centro di lavoro.  
17. Selezionare un calendario reparto produzione nel campo **Cod. calendario reparto prod.**. Per ulteriori informazioni, vedere [Creare calendari del reparto produzione](production-how-to-create-work-center-calendars.md).  
18. Il campo **Tempo in coda** consente di specificare un intervallo di tempo fisso che deve trascorrere prima di potere iniziare l'attività assegnata all'area di produzione selezionata. 

> [!NOTE]
> Utilizzare i tempi in coda per fornire un buffer tra il momento in cui un componente arriva a una macchina o un'area di produzione e quando l'operazione inizia effettivamente. Ad esempio, un pezzo viene consegnato a un centro lavoro alle 10:00, ma ci vuole un'ora per montarlo sulla macchina, quindi l'operazione non inizia prima delle 11:00. Per tenere conto di quell'ora, il tempo in coda sarebbe un'ora. Il valore del campo **Tempo in coda** nella scheda Centro di Lavoro o Area di produzione sommato ai valori dei campi **Tempo di setup**, **Tempo lavorazione**, **Tempo attesa** e **Tempo spostamento** della riga del ciclo dell'articolo fornisce il lead time di produzione dell'articolo. Ciò consente di fornire tempi di produzione complessivi accurati.  

## <a name="considerations-about-capacity"></a>Considerazioni sulla capacità

La capacità e l'efficienza specificate per un'area di produzione e un centro di lavoro non influiscono solo sulla capacità disponibile. Influiscono anche sul tempo di produzione complessivo che consiste nel tempo di configurazione e nel tempo di esecuzione, entrambi definiti sulla riga del ciclo di produzione.  

Quando una specifica riga del ciclo di produzione viene assegnata a un'area di produzione e un centro di lavoro, il sistema calcola la capacità necessaria e il tempo necessario per completare l'operazione.  

### <a name="run-time"></a>Tempo lavorazione

Per calcolare il tempo lavorazione, il sistema alloca il tempo esatto definito nel campo **Tempo lavorazione** della riga del ciclo di produzione. Né l'efficienza né la capacità influiscono sul tempo assegnato. Ad esempio, se il tempo di lavorazione è definito come 2 ore, il tempo allocato sarà di 2 ore, indipendentemente dai valori nei campi efficienza e capacità nell'area di produzione.  

> [!NOTE]
> La capacità utilizzata nei calcoli è definita come il valore minimo tra la capacità definita nell'area produzione o nel centro di lavoro e la capacità simultanea definita per la riga del ciclo di produzione. Se un'area di produzione ha una capacità di 100, ma la capacità simultanea per la riga del ciclo di produzione è 2, *2* verrà utilizzato nei calcoli.

La *durata* di un'operazione, al contrario, considera sia l'efficienza che la capacità. La durata è calcolata come *Tempo lavorazione / Efficienza / Capacità*. L'elenco seguente mostra alcuni esempi del calcolo della durata per lo stesso tempo lavorazione, definito come 2 ore per la riga del ciclo di produzione:

- L'efficienza dell'80% significa che avrai bisogno di 2,5 ore invece di due ore  
- L'efficienza del 200% significa che puoi completare il lavoro in un'ora - puoi scavare una buca due volte più velocemente se hai un escavatore che è il doppio di quello più piccolo  

    Puoi ottenere lo stesso risultato se usi due escavatori più piccoli invece di uno grande: usa *2* come la capacità e *100%* come l'efficienza  

La capacità frazionaria è complicata e ne parleremo più avanti. 

### <a name="setup-time"></a>Tempo di setup

L'allocazione del tempo per il tempo di setup dipende dalla capacità e viene calcolata come *Tempo di setup * Capacità*. Ad esempio, se la capacità è impostata su *2*, il tempo di setup assegnato sarà raddoppiato, poiché è necessario configurare due macchine per l'operazione.  

La *durata* del tempo di setup dipende dall'efficienza ed è calcolata come *Tempo di setup / Efficienza*. 

- L'efficienza dell'80% significa che avrai bisogno di 2,5 ore invece di due ore per il setup  
- L'efficienza del 200% significa che puoi completare il setup in 1 ora invece di 2 ore definite nella riga del ciclo di produzione  

La capacità frattale non è qualcosa di facile da eseguire e viene utilizzata in casi molto specifici.

### <a name="work-center-processing-multiple-orders-simultaneously"></a>Area di produzione che elabora più ordini contemporaneamente

Prendiamo come esempio una cabina per verniciatura a spruzzo. Ha lo stesso setup e tempo di lavorazione per ogni lotto elaborato. Ma ogni lotto può contenere più ordini individuali che vengono dipinti contemporaneamente.  

In questo caso, il tempo e il costo allocato agli ordini è gestito dal tempo di setup e dalla capacità simultanea. Si consiglia di non utilizzare il tempo di lavorazione nelle righe del ciclo di produzione.  

Il tempo di setup assegnato per ogni singolo ordine sarà in ordine inverso rispetto al numero di ordini (quantità) che vengono eseguiti contemporaneamente. Ecco altri esempi del calcolo del tempo di setup quando è definito come due ore per la riga del ciclo di produzione:

- Se sono presenti due ordini, la capacità simultanea nella riga del ciclo di produzione deve essere impostata su 0,5.

    Di conseguenza, la capacità assegnata per ciascuno sarà di un'ora, ma la durata per ogni ordine rimarrà di due ore.
- Se sono presenti due ordini con una quantità rispettivamente di uno e quattro, la capacità simultanea per la riga del ciclo di produzione del primo ordine è 0,2 e 0,8 per il secondo.  

    Di conseguenza, la capacità assegnata per il primo ordine sarà di 24 minuti e per il secondo 96. La durata per entrambi gli ordini rimane di due ore.  

In entrambi i casi, il tempo totale allocato per tutti gli ordini è di due ore.


### <a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a>Una risorsa efficiente può dedicare solo una parte della data del lavoro al lavoro produttivo

> [!NOTE]
> Non è uno scenario consigliato. Ti consigliamo di utilizzare invece l'efficienza. 

Uno delle aree di produzione rappresenta un lavoratore esperto che lavora con il 100% di efficienza sulle attività. Ma possono dedicare solo il 50% del tempo di lavoro alle attività perché il resto del tempo svolgono attività amministrative. Mentre questo lavoratore è in grado di completare un'attività di due ore in esattamente due ore, in media devi aspettare altre due ore mentre la persona si occupa di altri incarichi.  

Il tempo di lavorazione allocato è di due ore e la durata è di quattro ore.  

Non utilizzare il tempo di setup per tali scenari, poiché il sistema allocherà solo il 50% del tempo. Se il tempo di setup è impostato su *2*, il tempo di setup allocato è di un'ora e la durata è di due ore.

### <a name="consolidated-calendar"></a>Calendario consolidato

Quando il campo **Calendario consolidato** è selezionato, l'area di produzione non ha capacità proprie. La sua capacità è invece pari alla somma delle capacità di tutti i centri di lavoro assegnati all'area di produzione.  

> [!NOTE]
>  L'efficienza del centro di lavoro viene convertita nella capacità dell'area di produzione.

Ad esempio, se si dispone di due centri di lavoro con un'efficienza rispettivamente di 80 e 70, la voce di calendario consolidata avrà un'efficienza di 100, una capacità di 1,5 e una capacità totale di 12 ore (turno di otto ore * 1,5 capacità). 

> [!NOTE]
>  Utilizza il campo **Calendario consolidato** quando strutturi i cicli per pianificare le operazioni di produzione a livello di centro di lavoro, non a livello di area di produzione. Quando consolidi il calendario, la pagina **Carico area di produzione** e i report diventano una panoramica del carico aggregato in tutti i centri di lavoro assegnati all'area di produzione.

### <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Esempio: diversi centri di lavoro assegnati a un'area di produzione

Quando si impostano i centri di lavoro e le aree di produzione, è importante pianificare quali capacità formeranno la capacità totale.

Se vengono assegnati diversi centri di lavoro (ad esempio, 210 tavolo da imballaggio 1, 310 cabina verniciatura etc.) a un'area di produzione, risulta importante prendere in considerazione le singole capacità dei centri di lavoro in quanto il mancato funzionamento di uno di essi può interrompere l'intero processo. I gruppi di macchine possono essere immessi in base alla loro capacità, senza essere necessariamente inclusi nella pianificazione. Disattivando il campo **Calendario consolidato** viene assegnata nel planning solo la capacità dell'area di produzione e non del centro lavoro.

Se, tuttavia, centri di lavoro uguali tra loro (ad esempio, 210 tavolo da imballaggio 1 e 220 tavolo da imballaggio 2) vengono combinati in un'area di produzione, è importante considerare l'area di produzione come la somma dei centri di lavoro assegnati. L'area di produzione verrà pertanto elencata con capacità pari a zero. Attivando il campo **Calendario consolidato**, all'area di produzione viene assegnata la capacità standard.

Se le capacità delle aree di produzione non devono contribuire a formare la capacità totale, l'efficienza deve risultare uguale a zero.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Per impostare un centro lavoro o area di produzione con capacità-vincolata

È necessario impostare le risorse di produzione considerate critiche e contrassegnarle per l'accettazione soltanto di carichi limitati, escludendo in questo modo il carico illimitato predefinito che viene accettato da altre risorse di produzione. Una risorsa critica può essere costituita da un'area di produzione o da un centro lavoro che costituiscono strozzature nel ciclo produttivo e per i quali si desidera stabilire un limite finito di carico.

[!INCLUDE[prod_short](includes/prod_short.md)] non supporta il controllo della produzione o del reparto dettagliato. Consente di pianificare un utilizzo fattibile di risorse fornendo una pianificazione approssimativa, ma non consente di creare e gestire automaticamente pianificazioni dettagliate in base alle priorità o alle regole di ottimizzazione.

Nella pagina **Risorse critiche** è possibile effettuare impostazioni per evitare il sovraccarico di risorse specifiche e garantire che nessuna capacità resti senza allocazione se ciò può aumentare il tempo di completamento di un ordine di produzione. Nel campo **Smorzamento (% cap. totale)**, è possibile aggiungere il tempo di smorzamento alle risorse per ridurre al minimo la suddivisione dell'operazione. Ciò consente al sistema di programmare il carico nell'ultimo giorno possibile superando leggermente la percentuale di carico critico se ciò può ridurre il numero di operazioni che vengono suddivise.

Nella pianificazione con risorse vincolate alla capacità, il sistema garantisce che nessuna risorsa venga caricata oltre la propria capacità definita (carico critico). Questa operazione viene effettuata assegnando ogni operazione alla fascia oraria disponibile più vicina. Se la fascia oraria non è sufficiente a completare l'intera operazione, l'operazione verrà divisa in due o più parti e collocate nelle fasce orarie adiacenti disponibili.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Risorse critiche**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi come necessario.

> [!NOTE]
> Le operazioni nelle aree di produzione o nei centri di lavoro impostati come risorse vincolate verranno sempre pianificate in modo seriale. Ciò significa che se una risorsa vincolata ha più capacità disponibili, allora tali capacità possono solo essere pianificate in sequenza e non in parallelo, come invece accade nel caso in cui l'area di produzione o il centro di lavoro non è stato impostato come risorsa vincolata. In una risorsa vincolata, il campo Capacità nell'area di produzione o nel centro di lavoro è maggiore di 1.

> Nel caso che l'operazione venga suddivisa, il tempo di setup viene assegnato una sola volta perché si presuppone che vengano apportate alcune rettifiche manuali per ottimizzare la pianificazione.

## <a name="see-also"></a>Vedi anche

[Creare calendari del reparto produzione](production-how-to-create-work-center-calendars.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
