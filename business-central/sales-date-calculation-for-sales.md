---
title: Calcolo della data di consegna per le vendite
description: L'applicazione calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data e disponibile per il prelievo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="delivery-date-calculation-for-sales"></a>Calcolo della data di consegna per le vendite

In [!INCLUDE[prod_short](includes/prod_short.md)] viene automaticamente calcolata la prima data possibile di spedizione di un articolo nella riga ordine di vendita.

* Se il cliente ha richiesto una data di consegna specifica, viene calcolata la data in cui gli articoli devono essere disponibili per il prelievo affinché la consegna avvenga come da richiesta.
* Se il cliente non ha richiesto una data di consegna specifica, viene calcolata la data in cui gli articoli possono essere consegnati. Il calcolo inizia dalla data in cui gli articoli sono disponibili per il prelievo.

## <a name="calculating-a-requested-delivery-date"></a>Calcolo di una data di consegna richiesta

Se si specifica una data di consegna richiesta sulla riga dell'ordine di vendita, questa data diventa la data di partenza per i calcoli successivi.

- *data di consegna richiesta - durata spedizione = data di spedizione pianificata*
- *data di spedizione pianificata - tempo gest. uscita da whse. = data spedizione*

Se gli articoli sono disponibili per il prelievo alla data di spedizione, il processo di vendita può proseguire. In caso contrario, viene visualizzato un avviso di esaurimento delle scorte.

> [!NOTE]
> Se il processo si basa sul calcolo indietro, ad esempio, se si utilizza la data di consegna richiesta per ottenere la data di spedizione pianificata, si consiglia di utilizzare formule di data con durate fisse, ad esempio "5D" per cinque giorni o "1W" per una settimana. Le formule di data senza durate fisse, come "CW" per settimana corrente o CM per mese corrente, possono comportare calcoli della data errati. Per ulteriori informazioni sulle formule di data, vedi [Utilizzare date e orari del calendario](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Calcolo della prima data utile per la consegna

Se nella riga dell'ordine di vendita non si specifica una data di consegna richiesta, o se la data richiesta non può essere rispettata, viene calcolata la prima data in cui gli articoli saranno disponibili. Questa data viene quindi immessa nel campo **Data spedizione** della riga e le date in cui si prevede di spedire gli articoli e in cui essi saranno consegnati al cliente vengono calcolate secondo le seguenti formule.

- *data spedizione + tempo gest. uscita da whse. = data di spedizione pianificata*
- *data di spedizione pianificata + tempo spedizione = data di consegna pianificata*

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/).

## <a name="see-also"></a>Vedere anche

[Calcolo della data per gli acquisti](purchasing-date-calculation-for-purchases.md)  
[Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
