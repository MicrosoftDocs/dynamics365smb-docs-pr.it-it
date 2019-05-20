---
title: 'Dettagli di progettazione: Criteri di riordino | Microsoft Docs'
description: Questo argomento fornisce una sintesi dei metodi per un rifornimento articoli.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 1212c6f2f7e9da03a15c7fb39496d85869ef3e73
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238649"
---
# <a name="design-details-reordering-policies"></a>Dettagli di progettazione: Metodi di riordino
I metodi di riordino consentono di definire la quantità da ordinare quando l'articolo deve essere rifornito. Esistono quattro metodi diversi di riordine.  

## <a name="fixed-reorder-qty"></a>Qtà Riordino Fissa
Il criterio Qtà Riordino Fissa è correlato alla pianificazione di magazzino dei tipici articoli C (costo di magazzino basso, basso rischio di obsolescenza e/o molti articoli). Questo metodo viene in genere utilizzato in connessione con un punto di riordino che riflette la domanda anticipata durante il lead time dell'articolo.  

### <a name="calculated-per-time-bucket"></a>Calcolato per intervallo di tempo  
 Se il sistema di pianificazione rileva che il punto di riordino è stato raggiunto o superato in un intervallo di tempo specificato (ciclo di riordino) - sopra o in corrispondenza del punto di riordino all'inizio del periodo e sotto o in corrispondenza del punto di riordino alla fine del periodo - verrà suggerito di creare un nuovo ordine di approvvigionamento della quantità di riordino specificata e di programmarlo dalla prima data successiva alla fine dell'intervallo di tempo.  

 Il concetto di punto di riordino programmato riduce il numero di suggerimenti di approvvigionamento. Ciò riflette un processo manuale di entrare nella warehouse spesso per controllare i contenuti effettivi nelle varie collocazioni.  

### <a name="creates-only-necessary-supply"></a>Crea solo l'approvvigionamento necessario  
 Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione controlla se l'approvvigionamento è già stato ordinato per essere ricevuto entro il lead time di un articolo. Se un ordine di approvvigionamento esistente risolverà il problema portando la giacenza disponibile al punto di riordino o oltre nel lead time, il sistema non suggerirà un nuovo ordine di approvvigionamento.  

 Gli ordini di approvvigionamento che vengono creati specificamente per soddisfare un punto di riordino sono esclusi dal bilanciamento dell'approvvigionamento ordinario e non verranno in alcun modo modificati in seguito. Di conseguenza, se un articolo che utilizza il punto di riordino deve essere eliminato (non compilato), è consigliabile verificare gli ordini di approvvigionamento inevasi manualmente o modificare il metodo di riordino lotto-per-Lotto con cui il sistema ridurrà o annullerà l'approvvigionamento superfluo.  

### <a name="combines-with-order-modifiers"></a>Combina con i modificatori di ordine  
 I modificatori di ordini, Quantità minima ordine, Quantità massima ordine e Molteplicità ordine, non devono svolgere un grande ruolo quando vengono utilizzati i criteri di quantità riordino fissa. Tuttavia, il sistema di pianificazione prende ancora in considerazione questi modificatori e diminuirà la quantità alle quantità di ordine massime specificate (e creerà due o più approvvigionamenti per raggiungere la quantità di ordine totale), aumenterà la quantità di ordine minima o arrotonderà la quantità di ordine fino a soddisfare la molteplicità ordine specificata.  

### <a name="combines-with-calendars"></a>Associazioni con i calendari  
 Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione verifica che l'ordine sia programmato per un giorno non lavorativo, in base ai calendari definiti nel campo **Codice calendario base** delle pagine **Informazioni società** e **Scheda Ubicazione**.  

 Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. In questo modo, potrebbe verificarsi che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.  

### <a name="should-not-be-used-with-forecast"></a>Non deve essere utilizzato con la previsione  
 Poiché la domanda prevista è già espressa nel livello del punto di riordino non è necessario includere una previsione nella pianificazione di un articolo utilizzando un punto di riordino. Se è necessario basare il piano su una previsione, utilizzare il metodo lotto per lotto.  

### <a name="must-not-be-used-with-reservations"></a>Non deve essere utilizzato con gli impegni  
 Se l'utente ha impegnato una quantità, ad esempio una quantità in magazzino, per una domanda remota, la struttura della pianificazione rimarrà alterata. Anche se il livello della quantità scorte previste è ammesso relativamente al punto di riordino, le quantità potrebbero non essere disponibili. Il sistema può provare a compensare creando ordini di eccezione; tuttavia, è consigliabile che il campo Impegno sia impostato su Mai negli articoli che sono pianificati utilizzando un punto di riordino.

## <a name="maximum-qty"></a>Qtà Massima
Il criterio Quantità massima è un modo per mantenere il magazzino utilizzando un punto di riordino.  

Tutto ciò che riguarda il metodo Qtà Riordino Fissa si applica anche a questi criteri. L'unica differenza è la quantità dell'approvvigionamento suggerito. Se si utilizza il metodo della quantità massima, la quantità di riordino verrà definita in modo dinamico in base al livello delle giacenze disponibili e quindi in genere differirà da ordine a ordine.  

### <a name="calculated-per-time-bucket"></a>Calcolato per intervallo di tempo  
La quantità di riordino viene determinata in un punto del tempo (alla fine di un intervallo di tempo) quando il sistema di pianificazione rileva che il punto di riordino è stato superato. A questo punto, il sistema misura l'interruzione dal livello di magazzino previsto corrente fino al magazzino massimo specificato. Ciò costituisce la quantità che deve essere riordinata. Il sistema controlla quindi se l'approvvigionamento è già stato ordinato altrove in modo che possa essere caricato entro il lead time e, in caso affermativo, riduce la quantità del nuovo ordine di approvvigionamento della quantità già ordinata.  

Il sistema assicurerà che la giacenza disponibile raggiunga almeno il livello del punto di riordino, nel caso l'utente abbia dimenticato di specificare una quantità di magazzino massima.  

### <a name="combines-with-order-modifiers"></a>Combina con i modificatori di ordine  
In base all'impostazione, è consigliabile combinare i criteri Quantità massima con i modificatori di ordini per garantire una quantità minima dell'ordine o per arrotondarla a un numero intero di unità di misura di acquisto, o suddividerla in più lotti come definito dalla quantità massima ordine.  

### <a name="combines-with-calendars"></a>Associazioni con i calendari  
Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione verifica che l'ordine sia programmato per un giorno non lavorativo, in base ai calendari definiti nel campo **Codice calendario base** delle pagine **Informazioni società** e **Scheda Ubicazione**.  

Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. In questo modo, potrebbe verificarsi che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.

## <a name="order"></a>Ordinamento
In un ambiente di produzione su ordine, un articolo viene acquistato o prodotto esclusivamente per coprire una domanda specifica. In genere si riferisce ad articoli A e le motivazioni per scegliere il metodo di riordino Ordine può essere quello di una domanda poco frequente, un lead time insignificante o la variazione degli attributi necessari.  

Il programma crea un collegamento ordine su ordine, che funge da connessione preliminare tra l'approvvigionamento, un ordine di approvvigionamento o il magazzino e la domanda che deve soddisfare.  

Oltre all'utilizzo del metodo Ordine, il collegamento ordine-a-ordine può essere applicato durante la pianificazione nei seguenti modi:  

* Se si utilizza la politica di produzione Produzione su ordine per creare ordini di produzione di tipo progetto o multilivello (producendo i componenti necessari nello stesso ordine di produzione).  
* Se si utilizza la funzionalità Pianifica ordine vendita per creare un ordine di produzione da un ordine di vendita.  

Anche se un'azienda manifatturiera si considera come ambiente di produzione su ordine, potrebbe essere meglio utilizzare un metodo di riordino lotto-per-lotto se gli articoli sono standard puro senza variazione negli attributi. Di conseguenza, verrà utilizzato il magazzino non pianificato e si accumuleranno solo ordini di vendita con la stessa data di spedizione o all'interno di un intervallo di tempo definito.  

### <a name="order-to-order-links-and-past-due-dates"></a>Collegamenti ordine su ordine e date di scadenza arretrate  
A differenza della maggior parte dei set di approvvigionamento-domanda, gli ordini collegati con date di scadenza precedenti alla data di inizio della pianificazione sono completamente pianificati dal sistema. Il motivo economico di questa eccezione è che la domanda e l'approvvigionamento specifici devono essere sincronizzati attraverso l'esecuzione. Per ulteriori informazioni sulla zona bloccata che si applica alla maggior parte dei tipi di domanda-approvvigionamento, vedere [Dettagli di progettazione: Gestione ordini prima della data di inizio pianificazione](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Lotto-per-Lotto
I criteri lotto per lotto sono i più flessibili perché il sistema reagisce solo alla domanda effettiva, agiscono inoltre sulla domanda prevista dalla previsione e dagli ordini programmati e stabiliscono la quantità dell'ordine in base alla domanda. I criteri lotto per lotto sono destinati agli elementi A e B dove il magazzino può essere accettato ma dovrebbe essere evitato.  

Per certi aspetti, il metodo lotto per lotto è simile al metodo Ordine, ma presenta un approccio generico agli articoli; può accettare quantità in magazzino e aggrega la domanda e il corrispondente approvvigionamento in intervalli di tempo definiti dall'utente.  

L'intervallo di tempo è definito nel campo **Intervallo di tempo**. Il sistema utilizza l'intervallo di tempo minimo pari a un giorno, che è l'unità di misura più piccola per gli eventi di domanda e approvvigionamento offerta dal sistema (sebbene, nella pratica, gli ordini di produzione e le richieste di componenti possano essere misurate in secondi).  

L'intervallo di tempo fissa anche dei limiti sui tempi di riprogrammazione di un ordine di approvvigionamento esistente per soddisfare una domanda specificata. Se l'approvvigionamento rientra nell'intervallo di tempo, viene riprogrammato all'interno o all'esterno in modo da soddisfare la domanda. In caso contrario, se risiede in un periodo precedente, causerà un accumulo di magazzino inutile e dovrà essere annullato. Se risiede dopo, verrà invece creato un nuovo ordine di approvvigionamento.  

Con questo metodo, è possibile definire una scorta di sicurezza per compensare possibili fluttuazioni nell'approvvigionamento o per soddisfare una domanda improvvisa.  

Poiché la quantità dell'ordine di approvvigionamento è basato sulla domanda effettiva e può essere sensato utilizzare i modificatori di ordini: arrotondare la quantità di ordine fino a soddisfare un multiplo dell'ordine specificato (o unità di misura dell'acquisto), aumentare l'ordine a una quantità ordine minima specificata oppure diminuire la quantità alla quantità massima specificata (e creare quindi due o più approvvigionamenti per raggiungere la quantità necessaria totale).

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
