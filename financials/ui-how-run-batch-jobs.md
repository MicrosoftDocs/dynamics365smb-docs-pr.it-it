---
title: 'Procedura: Eseguire i processi batch | Documenti Microsoft'
description: Informazioni su come funzionano i processi batch in Dynamics 365 for Financials.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1f4678ce0cfb18a746374226bb33020f70bf874d
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-run-batch-jobs"></a>Procedura: Eseguire i processi batch
Un processo batch è una routine che elabora i dati in batch, come, ad esempio, il processo **Rettifica tassi di cambio**. Alcuni processi batch eseguono attività contabili periodiche, ad esempio la chiusura del conto economico alla fine di un anno fiscale. Molti processi batch eseguono attività di calcolo, ad esempio il calcolo degli interessi finanziari, la rettifica dei tassi di cambio e il calcolo dei prezzi unitari.

Un processo batch è simile a un report, con la differenza che il processo batch utilizza il risultato delle attività che esegue per aggiornare direttamente le informazioni, anziché stampare i risultati.

## <a name="to-run-a-batch-job"></a>Per eseguire un processo batch
1. Per aprire la finestra di richiesta del processo batch pertinente, nell'angolo superiore destro, scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere il nome del processo batch, quindi scegliere il collegamento correlato.
2. Se per il processo batch è disponibile una Scheda dettaglio **Opzioni**, completarne i campi per determinare l'operazione che sarà eseguita dal processo batch.
3. È possibile che la finestra contenga una o più Schede dettaglio con filtri, che è possibile utilizzare per limitare i dati inclusi nel processo batch. È possibile immettere criteri nei filtri consigliati o aggiungere altri filtri.
4. Scegliere **OK** per avviare il processo batch.

## <a name="see-also"></a>Vedi anche
[Immissione di criteri di filtro](ui-enter-criteria-filters.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

