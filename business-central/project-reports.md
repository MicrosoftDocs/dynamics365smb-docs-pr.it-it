---
title: Report e analisi di progetto
description: Vedere quali report di progetto e analisi sono disponibili nella versione standard di Business Central in modo da poter tenere traccia della propria attività.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: ff5294df5cdbeaf0054249f017906bfd60ee4bf7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216379"
---
# <a name="project-reports-and-analytics-in-business-central"></a>Report di progetto e analisi in Business Central

Il report di progetto in [!INCLUDE [prod_short](includes/prod_short.md)] consente ai professionisti di progetto e aziendali di ottenere approfondimenti e statistiche sulle attività di progetto attuali e passate.  

## <a name="reports"></a>Report

La tabella seguente descrive alcuni dei report delle commesse chiave.

|Report |ID oggetto|Descrizione  |
|---------|---------|---------|
|**Analisi commessa**|1008|Analizza il processo utilizzando le impostazioni specificate. È possibile ad esempio creare un report in cui siano visualizzati i prezzi a budget, i prezzi di utilizzo e i prezzi fatturabili e in cui venga eseguito il confronto dei tre insiemi di prezzi.<br>Utilizzare una combinazione dei campi **Importo** disponibili per creare un'analisi personalizzata. Per ciascun campo, selezionare uno dei seguenti valori relativi a prezzo, costo o margine: programmazione, utilizzo, contratto e fatturato. <br>Indicare se la valuta è specificata in Valuta locale o Valuta estera. |
|**Righe pianificazione commessa**|1006|Questo report mostra le diverse righe di pianificazione e attività commessa, inclusi il tipo di riga, le quantità, l'unità di misura, i costi totali, ecc.|
|**Commessa - Confronto Effettivo/Budget**|1009|Confronta gli importi di utilizzo e programmati per le commesse selezionate. Sono indicati la quantità, il costo totale e l'importo per ciascuna riga della commessa selezionata. <br>Il report è destinato alle commesse già completate, ma può essere utilizzato in qualsiasi momento nel corso di una commessa.<br>Negli Stati Uniti, in Canada e in Messico, questo rapporto non è disponibile. Utilizzare invece i report **Confronto Costo effettivo/Costo budget** (10210) o **Confronto Prezzo effettivo/Prezzo budget** (10211).|
|**Fatturazione suggerita commessa**|1011|Viene visualizzata una lista di tutte le commesse, suddivise per cliente, l'importo già fatturato per il cliente e l'importo residuo da fatturare, ovvero la fatturazione suggerita. <br>Negli Stati Uniti, in Canada e in Messico, questo rapporto non è disponibile. Utilizzare invece il rapporto **Fatturazione suggerita del costo commessa** (10219).|
|**Commesse per cliente**|1012|Viene visualizzata una lista di tutte le commesse, suddivise per cliente. In questo modo è possibile confrontare il prezzo programmato, la percentuale di completamento, il prezzo fatturato e la percentuale degli importi fatturati per ciascun **cliente a cui fatturare**.|
|**Articoli per commessa** o **Commesse per articolo**|1013 oppure 1014|Una panoramica sugli articoli usati in un lavoro. A seconda del report che si desidera utilizzare per ottenere una panoramica degli elementi pianificati per un progetto, è possibile impostare un filtro aggiuntivo. Il report mostra gli elementi rilevanti e un valore accumulato sui costi.|
|**Dettaglio transazione commessa**|1007|Questo rapporto ti fornirà una panoramica sulle attività di commessa pubblicate come risorse ed elementi. Include informazioni dettagliate sui costi totali e sui prezzi totali più un'informazione sugli riga e così via. Il report mostra i dati dei movimenti contabili commesse.|
|**WIP commessa in C/G**|1010|Viene visualizzato il valore WIP nelle commesse selezionate, confrontato all'importo registrato nella contabilità generale.|




## <a name="tasks"></a>Attività

I seguenti articoli descrivono alcune delle attività chiave per analizzare lo stato del tuo business:

* [Monitorare lo stato di avanzamento e le prestazioni delle commesse](projects-how-monitor-progress-performance.md)  


## <a name="see-also"></a>Vedere anche

[Impostazione della Gestione progetti](projects-setup-projects.md)  
[Gestione progetti](projects-manage-projects.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
