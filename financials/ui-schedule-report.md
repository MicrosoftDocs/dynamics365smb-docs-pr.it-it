---
title: Programmazione dell'esecuzione di un report per una data e un'ora specifiche | Documenti Microsoft
description: Informazioni su come inserire un report in una coda di processi e programmare per l'elaborazione per una data e un'ora specifiche.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, job queue
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0b97a5e48c4b339375ca9ad8cbe8388c5d47bb44
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="schedule-a-report-to-run"></a>Programmare l'esecuzione di un report
È possibile pianificare l'esecuzione di un report per data e orario specifici. I report previsti vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse. È possibile salvare il report elaborato in un file, ad esempio un file Excel, Word, PDF, o stamparlo con una stampante selezionata, o semplicemente elaborare il report. Se si sceglie di salvare il report in un file, il report elaborato viene inviato nell'area **Report elaborati** della home page, dove è possibile visualizzarlo.

È possibile programmare un report quando si apre un report. Scegliere l'azione **Programmazione**, quindi immettere informazioni, come la stampante e la data e l'ora. Il report viene aggiunto alla coda processi e sarà eseguito alla data specificata. Quando il report viene elaborato, l'elemento verrà rimosso dalla coda commesse. Se il report elaborato è stato salvato in un file, sarà disponibile nell'area **Report elaborati**.

## <a name="see-also"></a>Vedi anche
[Specificare la selezione della stampante per i report](ui-specify-printer-selection-reports.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

