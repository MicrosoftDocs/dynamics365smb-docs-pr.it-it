---
title: 'Dettagli di progettazione: Carico dei profili di magazzino | Microsoft Docs'
description: Per ordinare le numerose origini di approvvigionamento e di domanda, il sistema di pianificazione le organizza su due sequenze temporali chiamate profili di magazzino.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5b47a898b7e1d574abaf521e917f780fd105c4a8
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-loading-the-inventory-profiles"></a>Dettagli di progettazione: Carico dei profili di magazzino
Per ordinare le numerose origini di approvvigionamento e di domanda, il sistema di pianificazione le organizza su due sequenze temporali chiamate profili di magazzino.  

 I normali tipi di domanda e approvvigionamento con date di scadenza corrispondenti o successive alla data iniziale di pianificazione vengono caricati in ciascun profilo di magazzino. Una volta caricati, i diversi tipi di domanda e approvvigionamento vengono ordinati in base alle priorità globali, ad esempio la data di scadenza, i codici di ultimo livello, l'ubicazione e la variante. Inoltre, vengono applicate delle priorità di ordine a diversi tipi per garantire che la domanda più importante sia completata per prima. Per ulteriori informazioni, vedere [Dettagli di progettazione: Assegnazione priorità ordini](design-details-prioritizing-orders.md).  

 Come precedentemente citato, la domanda potrebbe essere anche negativa. Ciò significa che deve essere considerata come approvvigionamento; tuttavia, a differenza dei tipi normali di approvvigionamento, la domanda negativa viene considerata un approvvigionamento fisso. Il sistema di pianificazione può prenderlo in considerazione, ma non suggerirà modifiche.  

 In genere, il sistema di pianificazione considera tutti gli ordini di approvvigionamento dopo la data di inizio della pianificazione come oggetti da modificare per soddisfare la domanda. Tuttavia, non appena una quantità viene registrata da un ordine di approvvigionamento, non può più essere modificata dal sistema di pianificazione. Di conseguenza, i seguenti ordini diversi non possono essere ripianificati:  

-   Ordini di produzione rilasciati in cui è stato registrato il consumo o l'output.  

-   Ordini di assemblaggio in cui è stato registrato il consumo o l'output.  

-   Ordini di trasferimento in cui è stata registrata la spedizione.  

-   Ordini di acquisto in cui il carico è stato registrato.  

 Oltre a caricare i tipi di approvvigionamento e di domanda, alcuni tipi vengono caricati con attenzione alle regole speciali e alle dipendenze descritte di seguito.  

## <a name="item-dimensions-are-separated"></a>Le dimensioni articolo sono separate  
 Il piano di approvvigionamento deve essere calcolato in base alla combinazione delle dimensioni dell'articolo, ad esempio la variante e l'ubicazione. Tuttavia, non esiste motivo per calcolare una combinazione teorica. Solo le combinazioni che includono la necessità di approvvigionamento e/o di domanda devono essere calcolate.  

 Ciò è controllato dal sistema di pianificazione attraverso l'esecuzione del profilo di magazzino. Quando viene trovata una nuova combinazione, viene creato un record di controllo interno che contiene le informazioni effettive sulla combinazione. Il programma inserisce la USK come record di controllo o ciclo esterno. Di conseguenza, vengono impostati i parametri di pianificazione appropriati in base a una combinazione di variante e ubicazione e il programma può procedere al ciclo interno.  

> [!NOTE]  
>  Il programma non richiede all'utente di immettere un record di USK durante l'immissione della domanda e/o dell'approvvigionamento per una particolare combinazione di variante e ubicazione. Di conseguenza, se un USK non esiste per una combinazione specifica, il programma crea un record USK temporaneo in base ai dati della scheda articolo. Se il campo Ubicazione obbligatoria è impostato su Sì nella finestra Setup magazzino, è necessario creare una USK oppure impostare Componenti nell'ubicazione su Sì. Per ulteriori informazioni, vedere [Dettagli di progettazione: Domanda nell'ubicazione vuota](design-details-demand-at-blank-location.md).  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>I numeri seriali o di lotto vengono caricati dal livello di specifica  
 Gli attributi in forma di numeri di serie o di lotto vengono caricati nei profili del magazzino insieme alla domanda e all'approvvigionamento a cui sono assegnati.  

 Gli attributi di domanda e approvvigionamento sono ordinati per priorità ordini nonché per livello di specifica. Poiché le corrispondenze del numero seriale o di lotto riflettono il livello di specifica, la domanda più specifica, ad esempio un numero di lotti selezionato in modo specifico per una riga di vendita, cercherà una corrispondenza prima della domanda meno specifica, ad esempio una vendita da un numero qualsiasi di lotto selezionato.  

> [!NOTE]  
>  Non vi sono regole di priorità dedicate per l'approvvigionamento e la domanda dotati di numeri seriali o di lotto, eccetto il livello di specifica definito dalle relative combinazioni di numeri seriali e di lotto e l'impostazione di tracciabilità articolo degli articoli interessati.  

 Durante la contropartita, il sistema di pianificazione considera l'approvvigionamento che offre i numeri di serie o di lotto come inflessibili e non prova ad aumentare o ripianificare tali ordini di approvvigionamento (a meno che non siano utilizzati in una relazione ordine-a-ordine). Vedere I collegamenti da ordine a ordine non sono mai interrotti). Ciò protegge l'approvvigionamento dal ricevere vari messaggi di azione potenzialmente in conflitto quando un approvvigionamento contiene attributi che variano, ad esempio una raccolta di numeri seriali differenti.  

 Un altro motivo per cui l'approvvigionamento con numero seriale o di lotto non è flessibile è che ai numeri seriali o di lotto in genere vengono assegnati in ritardo nel processo potrebbe confondere se vengono suggerite le modifiche.  

 Il saldo dei numeri seriali o di lotto non rispetta la [Zona bloccata](design-details-dealing-with-orders-before-the-planning-starting-date.md). Se la domanda e l'approvvigionamento non sono sincronizzati, il sistema di pianificazione suggerirà delle modifiche o dei nuovi ordini, indipendentemente dalla data di inizio della pianificazione.  

## <a name="order-to-order-links-are-never-broken"></a>I collegamenti ordine su ordine non sono mai interrotti  
 Nella pianificazione di un articolo ordine su ordine, l'approvvigionamento collegato non deve essere utilizzato per domande diverse da quella originariamente di destinazione. La domanda collegata non dovrebbe essere coperta da un altro approvvigionamento casuale, anche se, in questa situazione, è disponibile per tempo e quantità. Ad esempio, un ordine di assemblaggio collegato a un ordine di vendita in uno scenario di assemblaggio su ordine non può essere utilizzato per coprire un'altra domanda.  

 La domanda e l'approvvigionamento ordine su ordine devono essere in totale pareggio. Il sistema di pianificazione assicurerà l'approvvigionamento in tutte le condizioni senza considerare i parametri di dimensioni ordine, i modificatori e le quantità di magazzino (diverse dalle quantità correlate agli ordini collegati). Per lo stesso motivo, il sistema suggerirà approvvigionamenti eccedente in calo se la domanda collegata viene diminuita.  

 Questo bilanciamento influisce anche sui tempi. L'orizzonte limitato che viene fornito dall'intervallo di tempo non viene considerato; l'approvvigionamento verrà riprogrammato se i tempi della domanda sono cambiati. Tuttavia, il tempo di smorzamento sarà rispettato e impedirà la riprogrammazione all'esterno degli approvvigionamenti ordine su ordine, ad eccezione degli approvvigionamenti interni di un ordine di produzione a più livelli (ordine di progetto).  

> [!NOTE]  
>  I numeri seriali e di lotto possono inoltre essere specificati nella domanda ordine su ordine. In questo caso, l'approvvigionamento non viene considerato inflessibile per impostazione predefinita, come nel caso dei numeri seriali o di lotto. In questo caso, il sistema aumenterà o diminuirà a seconda dei cambiamenti nella domanda. Inoltre, se una domanda contiene più numeri seriali o di lotto diversi, ad esempio più di un numero di lotto, un ordine di approvvigionamento verrà suggerito per lotto.  

> [!NOTE]  
>  Le previsioni non devono condurre alla creazione degli ordini di approvvigionamento associati a un collegamento ordine-a-ordine. Se viene utilizzata la previsione, deve essere utilizzata solo come generatore della domanda dipendente in un ambiente di produzione.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Il componente richiesto viene caricato in base alle modifiche dell'ordine di produzione  
 Nella gestione degli ordini di produzione, il sistema di pianificazione deve monitorare i componenti necessari prima di caricarli nel profilo della domanda. Le righe componenti derivanti da un ordine di produzione corretto sostituiranno quelle dell'ordine originale. In questo modo il sistema di pianificazione stabilisce sicuramente che le righe di pianificazione per componenti necessari non vengano mai duplicate.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> La scorta di sicurezza può essere consumata  
 La scorta di sicurezza è principalmente un tipo di domanda e pertanto viene caricata nel profilo di magazzino alla data di inizio della pianificazione.  

 La scorta di sicurezza è una quantità di magazzino accantonata per compensare le incertezze della domanda durante il lead time di rifornimento. Tuttavia, può essere consumato se è necessario attingere per soddisfare una domanda. In tal caso, il sistema assicura che la scorta di sicurezza sia rapidamente reintegrata suggerendo un ordine di approvvigionamento per rifornire la quantità di scorta di sicurezza alla data in cui è stata consumata. La riga di pianificazione relativa a tale ordine conterrà un'icona di avviso di eccezione indicante che la scorta di sicurezza è stata parzialmente o completamente consumata per mezzo di un ordine di eccezione per la quantità mancante.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>La domanda di previsione viene ridotta dagli ordini di vendita  
 La previsione di produzione esprime la domanda futuro prevista. Mentre la domanda effettiva viene immessa, in genere come ordini vendita per articoli prodotti, viene utilizzata la previsione.  

 La previsione stessa non viene effettivamente ridotta dagli ordini di vendita; rimane la stessa. Tuttavia, le quantità previste utilizzate nel calcolo della pianificazione vengono ridotte (delle quantità dell'ordine di vendita) prima che l'eventuale quantità residua sia immessa nel profilo di magazzino della domanda. Quando il sistema di pianificazione esamina le vendite effettive del periodo, sono inclusi sia gli ordini di vendita aperti che i movimenti contabili articoli di vendita, a meno che non siano derivati da un ordine programmato.  

 È richiesto un utente per definire un periodo di previsione valido. La data della quantità prevista definisce l'inizio del periodo e la data della previsione successiva definisce la fine del periodo.  

 La previsione per periodi precedenti al periodo di pianificazione non viene utilizzata, indipendentemente dal fatto che sia stata consumata o meno. La prima cifra di previsione interessante è la data di inizio o la data più vicina precedente alla data di inizio pianificazione.  

 La previsione può riguardare una domanda indipendente, ad esempio ordini di vendita, o una domanda dipendente, come i componenti dell'ordine di produzione (modulo-previsione). Un articolo può avere entrambi i tipi di previsione. Durante la pianificazione, il consumo avviene separatamente, prima per domanda indipendente quindi per la domanda dipendente.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>La domanda dell'ordine programmato viene ridotta dagli ordini di vendita  
 Le previsioni vengono completate dall'ordine di vendita programmato al fine di specificare la domanda futura da un cliente specifico. Analogamente alle previsioni (non specificato), le vendite effettive dovrebbero consumare la domanda prevista e la quantità residua dovrebbe immettere il profilo di magazzino della domanda. Di nuovo, il consumo non riduce effettivamente l'ordine programmato.  

 Il calcolo della pianificazione considera gli ordini vendita aperti collegati alla riga ordine di copertura specifica, ma non considera alcun periodo di tempo valido. Non vengono considerati neppure gli ordini registrati, poiché la procedura di registrazione ha già ridotto la quantità inevasa dell'ordine programmato.  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
 [Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
 [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)

