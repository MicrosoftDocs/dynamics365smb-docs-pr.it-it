---
title: Calcolo della data per le vendite | Microsoft Docs
description: Il programma calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data. Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo.
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
ms.openlocfilehash: a620b7ed9d06cdd8adf7b12bea2b55aecea32bcc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251130"
---
# <a name="date-calculation-for-sales"></a>Calcolo della data per le vendite
In [!INCLUDE[d365fin](includes/d365fin_md.md)] viene automaticamente calcolata la prima data possibile di spedizione di un articolo nella riga ordine di vendita.

Se il cliente ha richiesto una data di consegna specifica, viene calcolata la data in cui gli articoli devono essere disponibili per il prelievo affinché la consegna avvenga come da richiesta.

Se il cliente non richiede una data di consegna specifica, la data in cui gli articoli possono essere consegnati viene calcolata, a partire dalla data in cui gli articoli sono disponibili per il prelievo.

## <a name="calculating-a-requested-delivery-date"></a>Calcolo con una data di consegna richiesta
Se si specifica una data di consegna richiesta sulla riga dell'ordine di vendita, questa data verrà utilizzata come data di partenza per i calcoli successivi.

- data di consegna richiesta - durata spedizione = data di spedizione pianificata
- data di spedizione pianificata - tempo gest. uscita da whse. = data spedizione

Se gli articoli sono disponibili per il prelievo alla data di spedizione, il processo di vendita può proseguire.

Se non esistono articoli disponibili per il prelievo alla data di spedizione, verrà visualizzato un avviso di esaurimento delle scorte.

## <a name="calculating-the-earliest-possible-delivery-date"></a>Calcolo della prima data utile per la consegna
Se nella riga dell'ordine di vendita non si specifica una data di consegna richiesta, o se la data richiesta non può essere rispettata, viene calcolata la prima data in cui gli articoli saranno disponibili. Questa data viene quindi immessa nel campo Data spedizione della riga e le date in cui si prevede di spedire gli articoli e in cui essi saranno consegnati al cliente vengono calcolate secondo le seguenti formule.

- data spedizione + tempo gest. uscita da whse. = data di spedizione pianificata
- data di spedizione pianificata + durata spedizione = data di consegna pianificata


## <a name="see-also"></a>Vedi anche  
 [Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)   
 [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
