---
title: Come creare una previsione della domanda | Microsoft Docs
description: "Nella pagina **Previsione della domanda** è possibile creare previsioni di produzione e di vendita."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: b7937bf83074dcbe9cd2bf501d4a5f67c1712511
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="create-a-demand-forecast"></a>Creare una previsione della domanda
Nella pagina **Previsione della domanda** è possibile creare previsioni di produzione e di vendita.  

La funzionalità di previsione viene utilizzata per creare la domanda prevista; la domanda effettiva viene creata da ordini di vendita e produzione. Durante la creazione della programmazione di produzione master (MPS), la previsione viene confrontata con gli ordini di vendita e produzione. L'opzione *Componente* nella previsione determina il tipo dei fabbisogni da considerare nel processo di confronto. Se la previsione riguarda un articolo di vendita, viene confrontata solo con gli ordini di vendita. Se si riferisce ai componenti, viene confrontata solo con la domanda dipendente dei componenti dell'ordine di produzione.  

La previsione consente alla società di creare scenari "what if" e di pianificare e soddisfare in modo efficiente e conveniente una domanda. Una previsione accurata può costituire una differenza essenziale nel determinare i livelli di soddisfazione del cliente rispetto alle date di promessa ordine e alla consegna tempestiva.  

## <a name="sales-forecasts-and-production-forecasts"></a>Previsioni di vendita e previsioni di produzione  
La funzionalità di previsione disponibile nel programma può essere utilizzata per creare previsioni di vendita o di produzione, in combinazione o indipendentemente. La maggior parte delle società di tipo produzione su ordine non dispone di un magazzino di prodotti finiti, in quanto ogni articolo viene prodotto solo quando viene ordinato. L'anticipo degli ordini (previsione di vendita) è fondamentale per garantire un tempo di completamento ragionevole per i prodotti finiti (previsione di produzione). Ad esempio, le parti di componente con tempi di consegna prolungati, se non in ordine o in magazzino, possono ritardare la produzione.  

-   La previsione di vendita è l'ipotesi più verosimile del reparto vendite riguardo a ciò che verrà venduto in futuro e viene specificata in base all'articolo e al periodo. La previsione di vendita, tuttavia, non è sempre adeguata per la produzione.  
-   La previsione di produzione è la proiezione del responsabile della pianificazione di produzione del numero di elementi finali e subassemblati derivati da produrre nei periodi specifici per soddisfare la previsione di vendita.  

Nella maggior parte dei casi, pertanto, il responsabile della pianificazione di produzione modifica la previsione di vendita per adattarla alle condizioni di produzione, rispettando comunque la previsione di vendita stessa.  

Le previsioni vengono create manualmente nella pagina **Previsione della domanda**. Nel sistema possono essere presenti più previsioni, differenziate in base al nome e al tipo. Le previsioni possono essere copiate e modificate in base alle esigenze. Ai fini della pianificazione, è valida una sola previsione per volta.  

La previsione consiste in un certo numero di record, ciascuno indicante il numero di articolo, la data della previsione e la quantità prevista. La previsione di un articolo è relativa a un periodo, definito dalla data della previsione e dalla data del successivo record di previsione. Dal punto di vista della pianificazione, la quantità prevista deve essere disponibile all'inizio del periodo della domanda.  

È necessario designare una previsione come *Articolo di vendita*, *Componente* o *Entrambi*. Il tipo di previsione *Articolo di vendita* viene utilizzato per le previsioni di vendita. La previsione di produzione viene creata utilizzando il tipo *Componente*. Il tipo di previsione *Entrambi* viene utilizzato solo per fornire al responsabile della pianificazione una panoramica sia della previsione di vendita sia della previsione di produzione. Con questa opzione i movimenti previsioni non sono modificabili. Se si designano questi tipi di previsione a questo punto, è possibile utilizzare lo stesso prospetto per immettere una previsione di vendita mentre si crea una previsione di produzione e utilizzare lo stesso prospetto per visualizzare entrambe le previsioni contemporaneamente. Il sistema tratta i diversi input, vendita e produzione, in modo diverso nel calcolare la pianificazione, ovvero in base ad articolo, produzione e setup produzione.  

## <a name="component-forecast"></a>Previsione di componenti  
La previsione di componenti può essere considerata la previsione di un'opzione in relazione a un articolo principale. Ciò può risultare utile, ad esempio, se il responsabile della pianificazione è in grado di stimare la domanda per il componente.  

Poiché la previsione di componenti è progettata per definire le opzioni di un articolo principale, deve essere uguale o minore alla quantità di previsione degli articoli di vendita. Se la previsione di componenti è maggiore rispetto alla previsione di tipo articolo di vendita, la differenza tra i due tipi di previsione verrà trattata come domanda indipendente.  

## <a name="forecasting-periods"></a>Previsione di periodi  
 Il periodo di previsione è valido dalla data di inizio alla data di inizio della previsione successiva. La pagina relativa all'intervallo di tempo offre diverse opzioni tra cui scegliere per l'inserimento della domanda in una data specifica all'interno di un periodo. È pertanto consigliabile evitare di modificare l'ambito del periodo di previsione a meno che non si desideri spostare tutti i movimenti previsioni alla data di inizio di tale periodo.  

## <a name="forecast-by-locations"></a>Previsione in base alle ubicazioni  
Può essere indicato nel setup manufacturing se si desidera filtrare le previsioni in base all'ubicazione durante il calcolo di un piano. Se le previsioni basate sull'ubicazione, tuttavia, vengono visualizzate singolarmente, la previsione complessiva potrebbe non essere rappresentativa.

## <a name="to-create-a-demand-forecast"></a>Per creare una previsione della domanda

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Previsione della domanda** e quindi scegliere il collegamento correlato.  
2.  Nella Scheda dettaglio **Generale** selezionare una previsione nel campo **Nome previsione della domanda**. Possono essere presenti più previsioni, differenziate da nome e tipo di previsione.  
3.  Nel campo **Filtro ubicazione**, selezionare l'ubicazione a cui la previsione viene applicata.  
4.  Nel campo **Tipo previsione**, selezionare **Articolo di vendita**, **Componente** o **Entrambi**. Se si seleziona **Articolo di vendita** o **Componente**, è possibile modificare la quantità in base al periodo. Se si seleziona **Entrambi**, non è possibile modificare la quantità, ma è possibile fare clic sul pulsante della freccia in giù e visualizzare i mov. previsioni domanda.  
5.  Specificare un filtro in **Filtro data** se si desidera limitare la quantità di dati visualizzati.  
6.  Nella Scheda dettaglio **Matrice previsioni domanda** immettere le quantità previste di **Articoli di vendita** o **Componenti** per i vari periodi.  
7.  Nella Scheda dettaglio **Opzioni matrice** impostare l'intervallo di tempo nel campo **Visualizza per** per modificare il periodo visualizzato in ogni colonna. È possibile selezionare i seguenti intervalli: **Giorno**, **Settimana**, **Mese**, **Trimestre**, **Anno** oppure il **Periodo contabile** come impostazione in Gestione contabile.  

    > [!NOTE]  
    >  È consigliabile valutare l'intervallo di tempo che si desidera utilizzare per le previsioni future per garantirne la coerenza. Quando si immette una quantità di previsione, questa è valida nel primo giorno dell'intervallo di tempo selezionato. Se, ad esempio, si seleziona un mese, la quantità di previsione viene immessa nel primo giorno del mese. Se si seleziona un trimestre, la quantità di previsione viene immessa nel primo giorno del primo mese del trimestre.  

8.  Nel campo **Visualizza come**, selezionare come vengono visualizzate le quantità di previsione per l'intervallo di tempo. Se si seleziona **Saldo periodo**, nel saldo per l'intervallo di tempo verrà visualizzato il saldo periodo. Se si seleziona **Saldo alla data**, nella pagina verrà visualizzato il saldo all'ultimo giorno dell'intervallo di tempo.  

> [!NOTE]  
>  È anche possibile modificare una previsione esistente. Nella pagina **Matrice previsioni domanda**, scegliere l'azione **Copia previsioni della domanda** e compilare la pagina **Previsione della domanda** con una previsione esistente. Modificare quindi le quantità come appropriato.  

## <a name="see-also"></a>Vedi anche  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

