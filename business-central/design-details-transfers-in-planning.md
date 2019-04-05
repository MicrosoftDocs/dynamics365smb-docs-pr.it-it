---
title: 'Dettagli di progettazione: Trasferimenti nella pianificazione | Microsoft Docs'
description: In questo argomento viene descritto il modo in cui utilizzare gli ordini di trasferimento come origine di approvvigionamento quando si pianificano i livelli di magazzino.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, transfer, sku, locations, warehouse
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: dbf1658893d5210c38994302ae817afa7349884a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801907"
---
# <a name="design-details-transfers-in-planning"></a>Dettagli di progettazione: Trasferimenti nella pianificazione
Gli ordini di trasferimento sono anche un'origine di approvvigionamento quando si lavora a livello di stockkeeping. Se si utilizzano più ubicazioni (warehouse), il sistema di rifornimento della USK può essere impostato su Trasferimento, implicando che l'ubicazione sia rifornita trasferendo le merci da un'altra ubicazione. In una situazione con più warehouse, le società potrebbero avere una catena di trasferimenti in cui l'approvvigionamento all'ubicazione VERDE viene trasferito da GIALLO e l'approvvigionamento a GIALLO viene trasferito da ROSSO e così via. All'inizio della catena, è presente un sistema di rifornimento di Ordine di produzione o di acquisto.  

![Esempio di flusso di trasferimento](media/nav_app_supply_planning_7_transfers1.png "Esempio di flusso di trasferimento")  

Confrontando la situazione in cui un ordine di approvvigionamento è direttamente rivolto a un ordine della domanda con una situazione in cui l'ordine di vendita viene rifornito tramite una catena di trasferimenti USK, è ovvio che l'attività di pianificazione nella seconda situazione può diventare molto complessa. Se la domanda cambia, potrebbe causare un effetto onda lungo la catena, in quanto tutti gli ordini di trasferimento più l'ordine di acquisto/produzione all'altro estremo della catena dovrebbero essere manipolati per ristabilire l'equilibrio tra domanda e approvvigionamento.  

![Esempio di saldo tra approvvigionamento e domanda nei trasferimenti](media/nav_app_supply_planning_7_transfers2.png "Esempio di saldo tra approvvigionamento e domanda nei trasferimenti")  

## <a name="why-is-transfer-a-special-case"></a>Perché il trasferimento è un caso particolare?  
Un ordine di trasferimento appare come qualsiasi altro ordine nel programma. In realtà è molto diverso.  

Un aspetto fondamentale che differenzia i trasferimenti nella pianificazione dagli ordini di acquisto e di produzione è che una riga di trasferimento rappresenta contemporaneamente la domanda e l'approvvigionamento. La parte in uscita, che viene spedita dall'ubicazione precedente, è la domanda. La parte in entrata, che deve essere ricevuta presso la nuova ubicazione, è l'approvvigionamento in tale ubicazione.  

![Contenuto della pagina Ordine di trasferimento](media/nav_app_supply_planning_7_transfers3.png "Contenuto della pagina Ordine di trasferimento")  

Ciò significa che quando il sistema manipola il lato approvvigionamento del trasferimento, deve apportare una modifica simile sul lato domanda.  

## <a name="transfers-are-dependent-demand"></a>I trasferimenti dipendono dalla domanda  
La domanda e l'approvvigionamento correlate hanno una qualche somiglianza con i componenti di una riga ordine di produzione, ma la differenza è che i componenti saranno nel livello successivo di pianificazione e con un articolo differente, mentre le due parti di trasferimento si trovano nello stesso livello, per lo stesso articolo.  

Una similarità importante è che così come i componenti dipendono dalla domanda, allo stesso modo lo è la domanda di trasferimento. La domanda da una riga di trasferimento viene dettata sul lato di approvvigionamento del trasferimento nel senso che se l'approvvigionamento viene modificato, la domanda ne viene direttamente interessata.  

A meno che la flessibilità di pianificazione sia impostata su Nessuna, una riga di trasferimento non dovrebbe mai essere considerata come una domanda indipendente nella pianificazione.  

Nella procedura di pianificazione, la domanda di trasferimento deve essere considerata soltanto dopo che il lato di approvvigionamento è stato elaborato dal sistema di pianificazione. Prima di questo, la domanda effettiva non è nota. La sequenza delle modifiche apportate è molto importante quando si tratta degli ordini di trasferimento.  

## <a name="planning-sequence"></a>Sequenza di pianificazione  
Nell'illustrazione seguente viene mostrato il possibile aspetto di una stringa di trasferimenti.  

![Esempio di flusso di trasferimento semplice](media/nav_app_supply_planning_7_transfers4.png "Esempio di flusso di trasferimento semplice")  

In questo esempio, un cliente ordina l'articolo presso l'ubicazione VERDE. L'ubicazione VERDE viene rifornita attraverso il trasferimento dalla warehouse centrale ROSSA. La warehouse centrale ROSSA viene approvvigionata tramite il trasferimento dalla produzione nell'ubicazione BLU.  

In questo esempio, il sistema di pianificazione inizierà alla domanda del cliente e risalirà la catena. Le domande e gli approvvigionamenti verranno elaborati un'ubicazione per volta.  

![Pianificazione forniture con trasferimenti](media/nav_app_supply_planning_7_transfers5.png "Pianificazione forniture con trasferimenti")  

## <a name="transfer-level-code"></a>Codice livello trasferimento  
La sequenza in cui le ubicazioni vengono elaborate nel sistema di pianificazione è determinata dal codice del livello di trasferimento dell'USK.  

Il codice del livello di trasferimento è un campo interno che viene calcolato e archiviato automaticamente in USK quando la USK viene creata o modificata. Il calcolo viene eseguito nell'ambito di tutte le USK per una determinata combinazione di articolo e variante e utilizza il codice ubicazione e il codice trasferire-da per determinare il ciclo che la pianificazione dovrà utilizzare nell'ambito delle USK per garantire l'elaborazione di tutte le domande.  

Il codice del livello di trasferimento sarà 0 per le unità di stockkeeping con ordine di produzione o di acquisto del sistema di rifornimento e sarà -1 per il primo livello di trasferimento, -2 per il secondo e così via. Nella catena di trasferimento descritta in precedenza, i livelli sarebbero quindi -1 per ROSSO e -2 per VERDE, come indicato nella seguente illustrazione.  

![Contenuto della pagina Scheda SKU](media/nav_app_supply_planning_7_transfers6.gif "Contenuto della pagina Scheda SKU")  

Per aggiornare la USK, il sistema di pianificazione rileverà se le unità di stockkeeping con il sistema di rifornimento Trasferimento sono impostate con riferimenti circolari.  

## <a name="planning-transfers-without-sku"></a>Pianificazione dei trasferimenti senza USK  

Anche se la funzionalità USK non viene utilizzata, è possibile utilizzare le ubicazioni ed eseguire trasferimenti manuali tra le ubicazioni. Per le società con un'impostazione di magazzino meno avanzata, il sistema di pianificazione supporta gli scenari in cui il magazzino esistente viene trasferito manualmente in un'altra ubicazione, ad esempio per soddisfare un ordine di vendita in tale ubicazione. Allo stesso tempo, il sistema di pianificazione dovrebbe rispondere alle modifiche nella domanda.  

Per supportare i trasferimenti manuali, la pianificazione analizzerà gli ordini di trasferimento esistenti e pianificherà l'ordine nel quale devono essere elaborate le ubicazioni. Internamente, il sistema di pianificazione opererà con USK temporanee contenenti codici a livello di trasferimento.  

![Codice livello trasferimento](media/nav_app_supply_planning_7_transfers7.png "Codice livello trasferimento")  

Se esistono più trasferimenti a una determinata ubicazione, il primo ordine di trasferimento definirà la direzione di pianificazione. I trasferimenti che sono in esecuzione nella direzione opposta verranno annullati.  

## <a name="changing-quantity-with-reservations"></a>Modificare la quantità con gli impegni  
Durante la modifica delle quantità in un approvvigionamento esistente, il sistema di pianificazione prende in considerazione gli impegni nel senso che la quantità impegnata rappresenta il limite inferiore a cui può essere ridotto l'approvvigionamento.  

Quando si modifica la quantità in una riga ordine di trasferimento esistente, tenere presente che il limite inferiore sarà definito come la quantità massima impegnata della riga di trasferimento in uscita e in entrata.  

Ad esempio, se una riga ordine di trasferimento di 117 pezzi viene impegnato rispetto a una riga di vendita pari a 46 e una riga acquisto pari a 24, non è possibile ridurre la riga di trasferimento al di sotto dei 46 pezzi anche se questo può rappresentare un approvvigionamento eccedente nel lato in entrata.  

![Prenotazioni nella pianificazione dei trasferimenti](media/nav_app_supply_planning_7_transfers8.png "Prenotazioni nella pianificazione dei trasferimenti")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Modificare la quantità in una catena di trasferimento  
Nel seguente esempio, il punto di partenza è una situazione equilibrata con una catena di trasferimento che fornisce un ordine di vendita di 27 nell'ubicazione ROSSO con un ordine di acquisto corrispondente nell'ubicazione BLU, trasferito tramite l'ubicazione ROSA. Di conseguenza, oltre alle vendite e all'acquisto, esistono due ordini di trasferimento: BLUE-ROSA e ROSA-ROSSO.  

![Modifica della quantità nella pianificazione del trasferimento 1](media/nav_app_supply_planning_7_transfers9.png "Modifica della quantità nella pianificazione del trasferimento 1")  

A questo punto il responsabile della pianificazione presso l'ubicazione ROSA sceglie di impegnare rispetto all'acquisto.  

![Modifica della quantità nella pianificazione del trasferimento 2](media/nav_app_supply_planning_7_transfers10.png "Modifica della quantità nella pianificazione del trasferimento 2")  

In genere questo significa che il sistema di pianificazione ignorerà l'ordine di acquisto e la domanda di trasferimento. A condizione che esista un saldo, non esiste alcun problema. Ma cosa accade quando il cliente nell'ubicazione ROSSO rifiuta parzialmente l'ordine e la modifica in 22?  

![Modifica della quantità nella pianificazione del trasferimento 3](media/nav_app_supply_planning_7_transfers11.png "Modifica della quantità nella pianificazione del trasferimento 3")  

Quando il sistema di pianificazione viene eseguito nuovamente, deve liberarsi dell'approvvigionamento in eccesso. Tuttavia, l'impegno bloccherà l'acquisto e il trasferimento di una quantità pari a 27.  

![Modifica della quantità nella pianificazione del trasferimento 4](media/nav_app_supply_planning_7_transfers12.png "Modifica della quantità nella pianificazione del trasferimento 4")  

Il trasferimento ROSA-ROSSO è stato ridotto a 22. La parte in entrata del trasferimento BLU-ROSA non è impegnata, ma dal momento che la parte in uscita è impegnata, non è possibile ridurre la quantità al di sotto di 27.  

## <a name="lead-time-calculation"></a>Calcolo lead time  
Nel calcolo della data di scadenza di un ordine di trasferimento vengono presi in considerazione diversi tipi di lead time.  

I lead time attivi durante la pianificazione di un ordine di trasferimento sono:  

* Tempo Gest. Uscita da Whse.  
* Durata spedizione  
* Tempo Gest. Entrata in Whse.  
* Nella riga di pianificazione vengono utilizzati i seguenti campi per fornire informazioni sul calcolo.  
* Data spedizione trasferimento  
* Data Inizio  
* Data fine  
* Data Scadenza  

La data di spedizione della riga di trasferimento verrà visualizzata nel campo Data spedizione trasferimento e la data di carico della riga di trasferimento verrà visualizzata nel campo Data scadenza.  

Le date di inizio e di fine verranno utilizzate per descrivere il periodo di trasporto effettivo.  

Nell'illustrazione seguente viene mostrata l'interpretazione delle data e ora di inizio e data e ora di fine nelle righe di pianificazione relative a ordini di trasferimento.  

![Data e ora di Central nella pianificazione del trasferimento](media/nav_app_supply_planning_7_transfers13.png "Data e ora di Central nella pianificazione del trasferimento")  

In questo esempio, significa che:  

* Data spedizione + Gestione in uscita = Data Inizio  
* Data inizio + Durata spedizione = Data fine  
* Data Fine + Gest. Entrata = Data Carico  

## <a name="safety-lead-time"></a>Lead time di sicurezza  
Il lead time di sicurezza predefinito nella pagina Setup manufacturing e il campo Lead time di sicurezza correlato nella scheda articolo non verranno considerati nel calcolo di un ordine di trasferimento. Tuttavia, il lead time di sicurezza continuerà a influenzare il piano totale come influirà sull'ordine di rifornimento (acquisto o produzione) all'inizio della catena di trasferimento quando gli articoli vengono collocati nell'ubicazione dalla quale verranno trasferiti.  

![Elementi della data di scadenza del trasferimento](media/nav_app_supply_planning_7_transfers14.png "Elementi della data di scadenza del trasferimento")  

Nella riga dell'ordine di produzione, la Data Fine + Lead Time di Sicurezza + Tempo Gest. Entrata in Whse. = Data Scadenza.  

Nella riga dell'ordine di acquisto, la Data Carico Pianificato + Lead Time di Sicurezza + Tempo Gest. Entrata in Whse. = Data Carico Prevista.  

## <a name="reschedule"></a>Ripianifica  
Nella riprogrammazione di una riga di trasferimento esistente, il sistema di pianificazione deve trovare la parte in uscita e modificare la data e l'ora in questa riga. È importante notare che se è stato definito il lead time, si verificherà un gap tra la spedizione e il carico. Come citato, il lead time può essere costituito da più elementi, ad esempio il tempo di trasporto e il tempo di gestione warehouse. In un asse temporale, il sistema di pianificazione si sposterà indietro nel tempo durante il calcolo del saldo degli elementi.  

![Modifica della data di scadenza nella pianificazione del trasferimento](media/nav_app_supply_planning_7_transfers15.png "Modifica della data di scadenza nella pianificazione del trasferimento")  

Di conseguenza, quando si modifica la data di scadenza in una riga di trasferimento, è necessario calcolare il lead time per aggiornare il lato in uscita del trasferimento.  

## <a name="seriallot-numbers-in-transfer-chains"></a>Numeri seriali e di lotto nelle catene di trasferimento  
Se la domanda contiene più numeri seriali o di lotto e il motore di pianificazione è in esecuzione, verranno creati alcuni ordini di trasferimento creati direttamente. Per ulteriori informazioni su questo concetto, vedere gli attributi dell'articolo. Se, tuttavia, i numeri seriali o di lotto vengono rimossi dalla domanda, ordini di trasferimento creati nella catena includeranno ancora i numeri seriali o di lotto e pertanto verranno trascurati dalla pianificazione (non eliminati).  

## <a name="order-to-order-links"></a>Collegamenti ordine su ordine  
In questo esempio, la USK BLU è impostata con il metodo di riordino Ordine, mentre ROSA e ROSSO utilizzano il metodo lotto per lotto. Quando un ordine di vendita di 27 viene creato nell'ubicazione ROSSO, verrà generata una catena di trasferimenti con l'ultima giunzione in corrispondenza dell'ubicazione BLU che è impegnata con il legame. In questo esempio, gli impegni non sono impegni imposti dal responsabile della pianificazione presso l'ubicazione ROSA, ma legami creati dal sistema di pianificazione. La differenza importante è che il sistema di pianificazione può modificare l'ultimo.  

![Collegamenti ordine su ordine nella pianificazione del trasferimento](media/nav_app_supply_planning_7_transfers16.png "Collegamenti ordine su ordine nella pianificazione del trasferimento")  

Se la domanda viene modificata da 27 a 22, il sistema abbasserà la quantità lungo la catena e sarà ridotto anche l'impegno vincolante.  

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Tabella Assegnazione pianificazione](design-details-planning-assignment-table.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Domanda nell'ubicazione Vuota](design-details-demand-at-blank-location.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)
