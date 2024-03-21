---
title: Creare una previsione della domanda
description: Informazioni sulle funzionalità di previsione della domanda e su come creare previsioni di vendita e produzione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '9245, 99000919, 99000921, 99000922'
ms.date: 03/11/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-a-demand-forecast"></a>Creare una previsione della domanda

Nella pagina elenco **Previsioni della domanda** è possibile creare previsioni di produzione e di vendita. Quindi, per ogni previsione, specifichi varie impostazioni nella pagina **Panoramica delle previsioni della domanda**.  

La funzionalità di previsione viene utilizzata per creare la domanda prevista; la domanda effettiva viene creata da ordini di vendita e produzione. Durante la creazione della programmazione di produzione master (MPS), la previsione viene confrontata con gli ordini di vendita e produzione. Il campo **Tipo di previsione** nella previsione determina il tipo dei fabbisogni da considerare nel processo di confronto. Se la previsione riguarda un *articolo di vendita*, viene confrontata solo con gli ordini di vendita. Se si riferisce ai *componenti*, viene confrontata solo con la domanda dipendente dei componenti dell'ordine di produzione.  

La previsione consente alla società di creare scenari "what if" e di pianificare e soddisfare in modo efficiente e conveniente una domanda. Una previsione accurata può costituire una differenza essenziale nel determinare i livelli di soddisfazione del cliente rispetto alle date di promessa ordine e alla consegna tempestiva.  

Con il primo ciclo di rilascio del 2022, puoi anche definire il giusto livello di dettagli nei campi **Previsione per posizione** e **Previsione per variante** nella pagina **Panoramica delle previsioni della domanda**. I filtri e le altre impostazioni sono memorizzati nella tabella **Nome previsione della domanda**. Così puoi facilmente interrompere e continuare il tuo lavoro in un secondo momento. Se la tua organizzazione ha eseguito l'aggiornamento al primo ciclo di rilascio del 2022, devi attivare la nuova esperienza nella pagina [Gestione funzionalità](admin-feature-management.md).  

## <a name="sales-forecasts-and-production-forecasts"></a>Previsioni di vendita e previsioni di produzione

La funzionalità di previsione disponibile nell'applicazione può essere utilizzata per creare previsioni di vendita o di produzione, in combinazione o indipendentemente. La maggior parte delle società di tipo produzione su ordine non dispone di un magazzino di prodotti finiti, in quanto ogni articolo viene prodotto solo quando viene ordinato. L'anticipo degli ordini (previsione di vendita) è fondamentale per garantire un tempo di completamento ragionevole per i prodotti finiti (previsione di produzione). Ad esempio, le parti di componente con tempi di consegna prolungati, se non in ordine o in magazzino, possono ritardare la produzione.  

- La previsione di vendita è l'ipotesi più verosimile del reparto vendite riguardo a ciò che verrà venduto in futuro e viene specificata in base all'articolo e al periodo. La previsione di vendita, tuttavia, non è sempre adeguata per la produzione.  
- La previsione di produzione è la proiezione del responsabile della pianificazione di produzione del numero di elementi finali e subassemblati derivati da produrre nei periodi specifici per soddisfare la previsione di vendita.  

Nella maggior parte dei casi, pertanto, il responsabile della pianificazione di produzione modifica la previsione di vendita per adattarla alle condizioni di produzione, rispettando comunque la previsione di vendita stessa.  

Le previsioni vengono create manualmente nella pagina **Previsione della domanda**. Nel sistema possono essere presenti più previsioni, differenziate in base al nome e al tipo. Le previsioni possono essere copiate e modificate in base alle esigenze. 

> [!NOTE]
> Ai fini della pianificazione, è valida una sola previsione per volta.

La previsione consiste in un certo numero di record, ciascuno indicante il numero di articolo, la data della previsione e la quantità prevista. La previsione di un articolo è relativa a un periodo, definito dalla data della previsione e dalla data del successivo record di previsione. Dal punto di vista della pianificazione, la quantità prevista deve essere disponibile all'inizio del periodo della domanda.  

È necessario designare una previsione come *Articolo di vendita*, *Componente* o *Entrambi*. Il tipo di previsione *Articolo di vendita* viene utilizzato per le previsioni di vendita. La previsione di produzione viene creata utilizzando il tipo *Componente*. Il tipo di previsione *Entrambi* viene utilizzato solo per fornire al responsabile della pianificazione una panoramica sia della previsione di vendita sia della previsione di produzione. Con questa opzione i movimenti previsioni non sono modificabili. Se si designano questi tipi di previsione a questo punto, è possibile utilizzare lo stesso prospetto per immettere una previsione di vendita mentre si crea una previsione di produzione e utilizzare lo stesso prospetto per visualizzare entrambe le previsioni contemporaneamente. Il sistema tratta i diversi input, vendita e produzione, in modo diverso nel calcolare la pianificazione, ovvero in base ad articolo, produzione e setup produzione.  

## <a name="component-forecast"></a>Previsione di componenti

La previsione di componenti può essere considerata la previsione di un'opzione in relazione a un articolo principale. Ciò può risultare utile, ad esempio, se il responsabile della pianificazione è in grado di stimare la domanda per il componente.  

Poiché la previsione di componenti è progettata per definire le opzioni di un articolo principale, deve essere uguale o minore alla quantità di previsione degli articoli di vendita. Se la previsione di componenti è maggiore rispetto alla previsione di tipo articolo di vendita, la differenza tra i due tipi di previsione verrà trattata come domanda indipendente.  

## <a name="forecasting-periods"></a>Previsione di periodi

Il periodo di previsione è valido dalla data di inizio alla data di inizio della previsione successiva. La pagina relativa all'intervallo di tempo offre diverse opzioni tra cui scegliere per l'inserimento della domanda in una data specifica all'interno di un periodo. È pertanto consigliabile evitare di modificare l'ambito del periodo di previsione a meno che non si desideri spostare tutti i movimenti previsioni alla data di inizio di tale periodo.  

## <a name="forecast-by-locations"></a>Previsione in base alle ubicazioni

Nella pagina **Setup manufacturing** è possibile specificare se considerare le ubicazioni definite nelle previsioni quando si calcolano i piani. 

### <a name="use-forecast-by-locations"></a>Usare la previsione in base alle ubicazioni

Se attivi **Usa previsione in base a ubicazione**, [!INCLUDE[prod_short](includes/prod_short.md)] rispetterà tutti i codici ubicazione specificati per ogni voce previsione della domanda e calcolerà la previsione rimanente per ciascuna ubicazione.  

Considerare questo esempio: l'azienda acquista e vende articoli in due ubicazioni: EST e OVEST. Per entrambe le ubicazioni, sono stati configurati criteri di riordino lotto a lotto. Si crea una previsione per le due ubicazioni:

- 10 pezzi per ubicazione EST
- 4 pezzi per ubicazione OVEST

Quindi si crea un ordine cliente con una quantità di 12 pezzi nell'ubicazione OVEST. Il sistema di pianificazione suggerirà di eseguire le seguenti operazioni:

- Rifornimento di 10 pezzi per l'ubicazione EST, in base ai dati della previsione.  
- Rifornimento di 12 pezzi per l'ubicazione OVEST, in base all'ordine vendita. I quattro pezzi specificati nella previsione vengono completamente consumati dalla domanda effettiva dell'ordine vendita. Per ulteriori informazioni, vedere [La domanda di previsione viene ridotta dagli ordini di vendita](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

> [!NOTE]  
> Se le previsioni basate sull'ubicazione vengono visualizzate singolarmente, la previsione complessiva potrebbe non essere rappresentativa.

### <a name="do-not-use-forecast-by-locations"></a>Non utilizzare previsioni in base alle ubicazioni

Se disattivi **Usa previsione in base a ubicazione**, [!INCLUDE[prod_short](includes/prod_short.md)] ignorerà tutti i codici ubicazione specificati per ogni voce previsione della domanda e aggregherà le previsioni in una previsione per ubicazioni vuote.  

Considerare questo esempio: l'azienda acquista e vende articoli in due ubicazioni: EST e OVEST. Per entrambe le ubicazioni, sono stati configurati criteri di riordino lotto a lotto. Si crea una previsione per le due ubicazioni:

- 10 pezzi per ubicazione EST
- 4 pezzi per ubicazione OVEST

Quindi si crea un ordine cliente con una quantità di 12 pezzi nell'ubicazione OVEST. Il sistema di pianificazione suggerirà di eseguire le seguenti operazioni:

- Rifornimento di 12 pezzi per l'ubicazione OVEST, in base all'ordine vendita.  
- Rifornimento di 2 pezzi per l'ubicazione vuota. I 10 e i 4 pezzi specificati nella previsione vengono consumati parzialmente dalla domanda effettiva dell'ordine vendita. [!INCLUDE[prod_short](includes/prod_short.md)]ha ignorato i codici ubicazione specificati dall'utente e utilizza invece un'ubicazione vuota.  

> [!NOTE]  
> È possibile impostare un filtro in base alle ubicazioni, ma i risultati basati sull'ubicazione potrebbero non corrispondere ai risultati della pianificazione senza filtri.

## <a name="to-create-a-demand-forecast"></a>Per creare una previsione della domanda

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Previsione della domanda**, quindi seleziona il collegamento correlato.  
2. Nella Scheda dettaglio **Generale** selezionare una previsione nel campo **Nome previsione della domanda**. Possono essere presenti più previsioni, differenziate da nome e tipo di previsione.  
3. Nel campo **Filtro ubicazione**, selezionare l'ubicazione a cui la previsione viene applicata.
4. Nel campo **Visualizza per** per modificare il periodo visualizzato in ciascuna colonna. È possibile selezionare i seguenti intervalli: **Giorno**, **Settimana**, **Mese**, **Trimestre**, **Anno** oppure il **Periodo contabile** come impostato nell'area finanziaria.

> [!NOTE]  
> È consigliabile valutare l'intervallo di tempo che si desidera utilizzare per le previsioni future per garantirne la coerenza. Quando si immette una quantità di previsione, questa è valida nel primo giorno dell'intervallo di tempo selezionato. Se, ad esempio, si seleziona un mese, la quantità di previsione viene immessa nel primo giorno del mese. Se si seleziona un trimestre, la quantità di previsione viene immessa nel primo giorno del primo mese del trimestre.

5. Nel campo **Visualizza come**, selezionare come vengono visualizzate le quantità di previsione per l'intervallo di tempo. Se si seleziona **Saldo periodo**, nel saldo per l'intervallo di tempo verrà visualizzato il saldo periodo. Se si seleziona **Saldo alla data**, nella pagina verrà visualizzato il saldo all'ultimo giorno dell'intervallo di tempo.  
6. Nel campo **Tipo previsione**, selezionare **Articolo di vendita**, **Componente** o **Entrambi**. Se si seleziona **Articolo di vendita** o **Componente**, è possibile modificare la quantità in base al periodo. Se si seleziona **Entrambi**, non è possibile modificare la quantità, ma è possibile fare clic sul pulsante della freccia in giù e visualizzare i mov. previsioni domanda.  
7. Specificare un filtro in **Filtro data** se si desidera limitare la quantità di dati visualizzati.  
8. Nella scheda dettagli **Matrice previsioni domanda**, immettere le quantità previste digitando una quantità nella cella che rappresenta un articolo in una data o un periodo particolari. Si noti che nelle celle vuote, il pulsante di ricerca apre una pagina vuota che indica che è necessario immettere un valore manualmente.   

> [!NOTE]  
> È anche possibile modificare una previsione esistente. Nella pagina **Matrice previsioni domanda**, scegliere l'azione **Copia previsioni della domanda** e compilare la pagina **Previsione della domanda** con una previsione esistente. Modificare quindi le quantità come appropriato.  

## <a name="see-also"></a>Vedi anche

[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)
[Inventario](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
