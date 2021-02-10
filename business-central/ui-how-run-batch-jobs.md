---
title: Creare ed eseguire un processo batch | Documenti Microsoft
description: È possibile eseguire i processi batch per elaborare i dati e aggiornare le informazioni, ad esempio, per attività contabili periodiche oppure per effettuare dei calcoli.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 04ae13561f44d544d38b04e3a881a0e707b441b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760519"
---
# <a name="run-batch-jobs-and-xmlports"></a>Eseguire processi batch e XMLports
Un processo batch è una routine che elabora i dati in batch, come, ad esempio, il processo **Rettifica tassi di cambio**. Alcuni processi batch eseguono attività contabili periodiche, ad esempio la chiusura del conto economico alla fine di un anno fiscale. Molti processi batch eseguono attività di calcolo, ad esempio il calcolo degli interessi finanziari, la rettifica dei tassi di cambio e il calcolo dei prezzi unitari.

Un processo batch è simile a un report, con la differenza che il processo batch utilizza il risultato delle attività che esegue per aggiornare direttamente le informazioni, anziché stampare i risultati.

È possibile pianificare l'esecuzione di un processo batch. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Per eseguire un processo batch
1. Per aprire la pagina di richiesta del processo batch pertinente, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere il nome del processo batch e quindi scegliere il collegamento correlato.
2. Se per il processo batch è disponibile una Scheda dettaglio **Opzioni**, completarne i campi per determinare l'operazione che sarà eseguita dal processo batch.
3. È possibile che la pagina contenga una o più Schede dettaglio con filtri, che è possibile utilizzare per limitare i dati inclusi nel processo batch. È possibile immettere criteri nei filtri consigliati o aggiungere altri filtri.
4. Scegliere **OK** per avviare il processo batch.

## <a name="see-also"></a>Vedere anche
[Ricerca, filtro e ordinamento di elenchi](ui-enter-criteria-filters.md)  
[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
