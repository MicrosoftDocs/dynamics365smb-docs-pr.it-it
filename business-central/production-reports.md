---
title: Report e analisi di produzione
description: Vedere quali report di produzione e analisi sono disponibili nella versione standard di Business Central in modo da poter tenere traccia della propria attività.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216375"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Report di produzione e analisi in Business Central

Il report di produzione in [!INCLUDE [prod_short](includes/prod_short.md)] consente ai professionisti della produzione e aziendali di ottenere approfondimenti e statistiche sulle attività di produzione attuali e passate.  

## <a name="reports"></a>Report

La tabella seguente descrive alcuni dei report di produzione chiave.

|Report |ID oggetto|Descrizione  |
|---------|---------|---------|
|**Esplosione quantità DB**|99000753|Mostra una lista della DB con rientri per l'articolo o gli articoli che si specificano nel filtro. La DB di produzione viene completamente esplosa a tutti i livelli.|
|**Articolo - Produzione possibile (sequenza temporale)**|5871|Mostra come cinque diverse cifre sulla disponibilità principali cambiano nel tempo per un articolo della DB. Tali cifre cambiano in base agli eventi previsti di approvvigionamento e domanda e all'approvvigionamento basato sui componenti disponibili che possono essere assemblati o prodotti.<br>È possibile utilizzare il report per verificare se è possibile soddisfare un ordine di vendita per un articolo nella data stabilita osservando la disponibilità corrente insieme alle quantità potenziali che i suoi componenti possono fornire se un ordine di assemblaggio fosse avviato. Questo report mostra quando e quante unità di un articolo di assemblaggio e di produzione è possibile produrre sulla base della disponibilità dei componenti e della disponibilità corrente dell'articolo. Questo valore è indicato come quantità totale.<br>Le informazioni vengono mostrate in un grafico in cui ogni cifra sulla disponibilità è rappresentata da una linea che avanza lungo la sequenza temporale e si sposta verso l'alto e verso il basso al variare delle quantità. Le cifre sulla quantità provengono dallo stesso motore che fornisce informazioni nella finestra **Pagina Disponibilità articolo per livello DB** . |
|**Distribuzione dettaglio costi DB**|5872|Visualizza graficamente come il costo di un articolo prodotto o assemblato viene ripartito nella relativa DB.<br>Tali informazioni possono essere utili per decidere, ad esempio, se modificare i fornitori di componenti, sostituire l'utilizzo di capacità interna con manodopera in appalto o viceversa o quando si rivede e si modifica la distinta base di un articolo.<br>Il primo grafico nel report mostra il costo unitario totale dei componenti e delle risorse di manodopera dell'articolo padre suddivisi fino a cinque dettagli di costo diversi e rappresentati graficamente con diversi colori.<br>Il grafico a torta etichettato *Per materiale/manodopera* mostra la distribuzione proporzionale tra il materiale e i costi di manodopera dell'articolo padre nonché i costi generali di produzione. Il dettaglio dei costi del materiale include i costi del materiale dell'articolo. Il dettaglio del costo di manodopera include la capacità, i costi generali capacità e i costi in conto lavoro. Le quote di costo vengono visualizzate in modo diverso a seconda delle tue scelte nel campo **Mostra solo**.<br>Il grafico a torta con la didascalia *Per costo diretto/indiretto* mostra la distribuzione proporzionale i costi diretti e indiretti dell'articolo padre. Il dettaglio dei costi diretti include i costi di materiale, capacità e in conto lavoro. Il dettaglio dei costi indiretti include i costi generali capacità e i costi generali produzione.<br>La tabella nella parte inferiore del report verrà inclusa quando si seleziona la casella di controllo **Includi dettaglio**. Visualizza i valori selezionati nella finestra Dettaglio costi DB per singolo livello o ricalcolati, in base all'opzione scelta nel campo **Mostra dettaglio costi come**.|
|**Calcolo dettagliato**|99000756|Mostra una lista dei costi per ogni articolo tenendo in considerazione lo scarto.|
|**Dove-usato (livello principale)**|99000757|Mostra dove e in quali quantità gli articoli vengono utilizzati nella struttura di prodotto.<br>Il report fornisce soltanto l'articolo dove utilizzato, quando l'articolo di base viene utilizzato come articolo di livello superiore. Ad esempio, se l'articolo “A” viene utilizzato per produrre l'articolo “B” e l'articolo “B” viene utilizzato per produrre l'articolo “C”, il report mostrerà l'articolo B se si esegue questo report per l'articolo A. Se si esegue questo report per l'articolo B, allora l'articolo C verrà mostrato dove utilizzato.<br>La pagina **Righe dove-usato** può essere aperta direttamente dall'articolo.|
|**Lista confronto DB articolo**|99000758|Questo rapporto ti dà la possibilità di confrontare prodotti finali simili riguardo ai costi. Vedrai un elenco con tutti i componenti e i loro costi, nonché le quantità necessarie. La data calcolo è normalmente impostata sulla data di lavoro. |
|**Statistiche ordini produzione**|99000791|Specifica i vari costi che si sono accumulati per l'ordine di produzione selezionato.<br>Il contenuto del report è molto simile alla pagina **Statistiche ordini produzione**.<br>Per gli ordini di produzione che utilizzano la politica di produzione *Produzione su ordine*, la finestra mostra solo i costi di materiale e capacità degli articoli al più alto livello della DB.|
|**Elenco attività capacità**|99000780|Mostra gli ordini di produzione in attesa di essere elaborati nelle aree di produzione e nei centri di lavoro. Le stampe vengono effettuate per la capacità dell'area di produzione o del centro lavoro. Il report comprende informazioni quali l'ora di inizio e di fine, la data per ordine di produzione e la quantità di input.|
|**Carico area produzione** o **Carico centro lavoro**|99000783 oppure 99000784|Entrambi i report forniscono una lista del carico su un'area produzione o centro di lavoro. Il carico su un'area di produzione/centro di lavoro è la somma del numero di esecuzioni richieste di tutti gli ordini pianificati ed effettivi sull'area di lavoro in un periodo specificato.|
|**Ord. prod. Lista el. mancanti**|99000788|Questo report può essere utilizzato per vedere tutti i componenti che non sono disponibili a causa di scorte mancanti. Quindi, questa panoramica può essere utilizzata per vedere in tempo, se la sequenza temporale per un ordine di produzione pianificato o rilasciato se il tempo pianificato può essere mantenuto.|


## <a name="tasks"></a>Attività

I seguenti articoli descrivono alcune delle attività chiave per analizzare lo stato del tuo business:

* [Visualizzare il carico in aree di produzione e centri di lavoro](production-how-to-view-the-load-on-work-centers.md)  
* [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)

## <a name="see-also"></a>Vedere anche

[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
