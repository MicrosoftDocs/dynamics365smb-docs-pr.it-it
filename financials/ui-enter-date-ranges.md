---
title: Impostazione di intervalli di date in Finance and Operations, Business edition | Documenti Microsoft
description: Informazioni su come ottenere un report per visualizzare i dati relativi a periodi di tempo specifici utilizzando gli intervalli di date in Finance and Operations, Business edition.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: da2fea4e095c8211f30aaa7c570a84a005e7cbc8
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="entering-date-ranges-in-finance-and-operations-business-edition"></a>Immettere intervalli di date in Finance and Operations, Business edition 
È possibile impostare filtri contenenti una data di inizio e una data di fine per visualizzare solo la data inclusa in un intervallo di date o di ore specifico. All'impostazione di intervalli di date si applicano regole speciali. Si consideri come esempio la **Lista primi 10 clienti**:

![Impostare un intervallo di date nella pagina di richiesta per la Lista primi 10 clienti](./media/ui-enter-date-ranges/customer-top10-list.png)

In questo campo è possibile limitare il report a un intervallo di date, ad esempio, alle ultime 2 settimane o a un totale di 6 settimane o a qualsiasi intervallo che si desidera. Per impostare gli intervalli di date, immettere le date quindi utilizzare **..** o **|** per impostare l'intervallo. Nell'esempio, per visualizzare i 10 clienti principali per le prime 2 settimane di maggio, impostare il filtro data come *05 01 17..05 14 17*.
Di seguito vengono proposti altri esempi:

| Significato | Esempio | movimenti inclusi |
|---|---|---|
|uguale a| 12 15 16 |Solo i movimenti registrati il 15 dicembre 2016.|
|intervallo| 12 15 16..01 15 17<br /><br />..12 15 16|Movimenti registrati in date comprese tra il 15 dicembre 2016 e il 15 gennaio 2017, inclusi.<br /><br />Movimenti registrati prima del 15 dicembre 2016, incluso.|
|oppure|12 15 16&#124;12 16 16|Movimenti registrati il 15 dicembre o il 16 dicembre 2016. Se sono presenti movimenti registrati in entrambi i giorni, verranno visualizzati tutti.|

È inoltre possibile combinare i vari tipi di formato.

| Esempio | movimenti inclusi |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Movimenti registrati il 15 dicembre 2016 o in date comprese tra il 01° dicembre 2016 e il 31 maggio 2017 inclusi. |
|..12 14 16&#124;12 30 16.. | Movimenti registrati il 14 dicembre, o in giorni precedenti, o movimenti registrati il 30 dicembre, o successivamente, ossia tutti i movimenti esclusi quelli registrati in date comprese tra il 15 e il 29 dicembre, incluse. |

Si noti che negli esempi è stato utilizzato il formato data MMGGAA degli Stati Uniti. Quando [!INCLUDE[d365fin](includes/d365fin_md.md)] sarà disponibile in altri mercati, sarà possibile utilizzare i formati abituali per il proprio paese.

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Immissione di criteri di filtro](ui-enter-criteria-filters.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

