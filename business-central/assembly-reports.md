---
title: Report di assemblaggio e analisi in Business Central
description: Vedere quali report di assemblaggio e analisi sono disponibili nella versione standard di Business Central in modo da poter tenere traccia della propria attività.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216377"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>Report di assemblaggio e analisi in Business Central

Il report di assemblaggio in [!INCLUDE [prod_short](includes/prod_short.md)] consente ai professionisti della produzione e aziendali di ottenere approfondimenti e statistiche sulle attività di montaggio attuali e passate.  

## <a name="reports"></a>Report

La tabella seguente descrive alcuni dei report di assemblaggio chiave.

|Report |ID oggetto|Descrizione  |
|---------|---------|---------|
|**DB assemblaggio**|801|Visualizza una lista di distinte base: nome, numero di DB, componenti di DB e altre eventuali distinte base che fanno parte della DB. I componenti della distinta base vengono definiti nella tabella Componenti DB. Qui vedrai anche l'unità di misura e la quantità necessaria di ciascun componente per unità di misura di base. |
|**Articolo - Produzione possibile (sequenza temporale)**|5871|Mostra come cinque diverse cifre sulla disponibilità principali cambiano nel tempo per un articolo della DB. Tali cifre cambiano in base agli eventi previsti di approvvigionamento e domanda e all'approvvigionamento basato sui componenti disponibili che possono essere assemblati o prodotti.<br>È possibile utilizzare il report per verificare se è possibile soddisfare un ordine di vendita per un articolo nella data stabilita osservando la disponibilità corrente insieme alle quantità potenziali che i suoi componenti possono fornire se un ordine di assemblaggio fosse avviato. Questo report mostra quando e quante unità di un articolo di assemblaggio e di produzione è possibile produrre sulla base della disponibilità dei componenti e della disponibilità corrente dell'articolo. Questo valore è indicato come quantità totale.<br>Le informazioni vengono mostrate in un grafico in cui ogni cifra sulla disponibilità è rappresentata da una linea che avanza lungo la sequenza temporale e si sposta verso l'alto e verso il basso al variare delle quantità. Le cifre sulla quantità provengono dallo stesso motore che fornisce informazioni nella finestra **Pagina Disponibilità articolo per livello DB** . |
|**Distribuzione dettaglio costi DB**|5872|Visualizza graficamente come il costo di un articolo prodotto o assemblato viene ripartito nella relativa DB.<br>Tali informazioni possono essere utili per decidere, ad esempio, se modificare i fornitori di componenti, sostituire l'utilizzo di capacità interna con manodopera in appalto o viceversa o quando si rivede e si modifica la distinta base di un articolo.<br>Il primo grafico nel report mostra il costo unitario totale dei componenti e delle risorse di manodopera dell'articolo padre suddivisi fino a cinque dettagli di costo diversi e rappresentati graficamente con diversi colori.<br>Il grafico a torta etichettato *Per materiale/manodopera* mostra la distribuzione proporzionale tra il materiale e i costi di manodopera dell'articolo padre nonché i costi generali di produzione. Il dettaglio dei costi del materiale include i costi del materiale dell'articolo. Il dettaglio del costo di manodopera include la capacità, i costi generali capacità e i costi in conto lavoro. Le quote di costo vengono visualizzate in modo diverso a seconda delle tue scelte nel campo **Mostra solo**.<br>Il grafico a torta con la didascalia *Per costo diretto/indiretto* mostra la distribuzione proporzionale i costi diretti e indiretti dell'articolo padre. Il dettaglio dei costi diretti include i costi di materiale, capacità e in conto lavoro. Il dettaglio dei costi indiretti include i costi generali capacità e i costi generali produzione.<br>La tabella nella parte inferiore del report verrà inclusa quando si seleziona la casella di controllo Includi dettaglio. Visualizza i valori selezionati nella finestra Dettaglio costi DB per singolo livello o ricalcolati, in base all'opzione scelta nel campo Mostra dettaglio costi come.|
|**Lista dove-usato**|809|Visualizza una lista delle distinte base di cui gli articoli selezionati figurano come componenti. Una panoramica utile nel caso in cui sia necessario modificare un componente in una distinta base inserita in un articolo di assemblaggio. Ad esempio, se il tuo fornitore non può più consegnare un articolo specifico che hai utilizzato per il tuo assemblaggio/produzione. In tali scenari, questo report fornisce una semplice panoramica delle distinte base in cui è incluso il componente. È possibile impostare un filtro per il numero del componente.|
|**DB - Materie prime**|810|Questo report può fornire una panoramica sui componenti necessari, sia per l'assemblaggio che per la produzione. Vedrai l'inventario, l'unità di misura di base, il fornitore principale se il numero di fornitore è scritto nella scheda articolo stessa e il calcolo del lead time.|
|**DB - Sotto-assemblaggi**|811|Se si producono e/o si assemblano sottoassiemi, utilizzare questo report per ottenere una panoramica su questo tipo di componente. Questo report mostra l'unità di misura di base, l'inventario, i costi unitari e un numero articolo alternativo. |
|**DB assemblaggio - Prodotti finiti**|812|Mostra una lista di articoli o di distinte base che non sono componenti di distinte base. **Nota**: questo report non è limitato solo alla distinta base, quindi ricordare di impostare il filtro nel campo **DB assemblaggio** o nei campi **Sistema di rifornimento**|
|**Assemblaggio su ordine - Vendite**|915|Mostra le cifre di vendita chiave per gli articoli componente di assemblaggio che possono essere venduti come parte di un assemblaggio nelle vendite assemblaggio su ordine e come articolo separato direttamente dal magazzino.<br>Utilizzare questo report per analizzare le cifre relative a quantità, costo, vendite e profitti per i componenti di assemblaggio per decidere, ad esempio, se assegnare un prezzo diverso a un kit o se utilizzare o meno un determinato articolo negli assemblaggi.<br>Nella riga **In assemblaggio** vengono mostrate le cifre di vendita per la quantità totale venduta come parte di un articolo di assemblaggio. Le vendite dell'articolo di assemblaggio che si sommano a questo totale vengono visualizzate se si seleziona il campo **Mostra dettagli assemblaggio**.<br>Lo stato attivo si trova sui componenti di assemblaggio, ma le cifre vengono calcolate dal margine di profitto dell'articolo padre, ovvero l'articolo di assemblaggio. Di conseguenza, l'importo di vendita di ciascun componente viene calcolato in base al costo e al margine di profitto dell'articolo padre nella formula seguente.<br>Nel report vengono mostrate le informazioni relative agli articoli che soddisfano uno o entrambi i criteri seguenti:<br>- Presenti nella DB assemblaggio di un articolo che utilizza i criteri di assemblaggio Assemblaggio su ordine.<br>- Venduti come parte della vendita assemblaggio su ordine.|

## <a name="tasks"></a>Attività

I seguenti articoli descrivono alcune delle attività chiave per analizzare lo stato del tuo business:

* [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)

## <a name="see-also"></a>Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Utilizzare le distinte base](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
