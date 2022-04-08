---
title: Calcolo della data per gli acquisti
description: L'applicazione calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 35151e830c44cb3edd28988887f86b8abf7a3b51
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514883"
---
# <a name="date-calculation-for-purchases"></a>Calcolo della data per gli acquisti

[!INCLUDE[prod_short](includes/prod_short.md)] calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data. Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo.  

Se si specifica una data di carico richiesta nella testata di un ordine di acquisto, la data dell'ordine calcolata è la data in cui si deve effettuare l'ordine per ricevere gli articoli alla data richiesta. Quindi, la data in cui gli articoli saranno disponibili per il prelievo viene calcolata e immessa nel campo **Data carico prevista**.  

Se non si specifica una data di carico richiesta, la data d'ordine presente sulla riga verrà usata come data di partenza per il calcolo della data prevedibile per la ricezione degli articoli e della data in cui gli articoli saranno disponibili per il prelievo.  

## <a name="calculating-with-a-requested-receipt-date"></a>Calcolo con una data di carico richiesta

Se è presente una data di carico richiesta sulla riga dell'ordine di acquisto, questa data verrà utilizzata come data di partenza per i calcoli successivi.  

- data di carico richiesta - calcolo lead time = data ordine  
- data di carico richiesta + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista  

Se è stata immessa una data di carico richiesta sulla testata dell'ordine di acquisto, questa data viene copiata nel campo corrispondente in tutte le righe. È possibile modificare questa data in qualsiasi riga oppure rimuoverla.  

> [!NOTE]
> Se il processo si basa sul calcolo indietro, ad esempio, se si utilizza la data carico richiesta per ottenere la data dell'ordine, si consiglia di utilizzare formule di data con durate fisse, ad esempio "5D" per cinque giorni o "1W" per una settimana. Le formule di data senza durate fisse, come "CW" per settimana corrente o CM per mese corrente, possono comportare calcoli della data errati. Per ulteriori informazioni sulle formule di data, vedere [Utilizzare date e orari del calendario](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Calcolo senza una data di consegna richiesta

Se si immette una riga di ordine di acquisto senza una data di consegna richiesta, il campo **Data ordine** nella riga viene compilato con la data nel campo **Data ordine** dell'intestazione dell'ordine di acquisto. Si tratta della data immessa o della work date. Le date seguenti vengono quindi calcolate per la riga dell'ordine di acquisto, con la data dell'ordine come punto di partenza.  

- data ordine + calcolo lead time = data carico pianificato  
- data carico pianificato + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista  

Se si modifica la data dell'ordine sulla riga, ad esempio quando gli articoli non sono disponibili presso il fornitore fino a una data successiva, le date corrispondenti nella riga saranno ricalcolate automaticamente.  

Se si modifica la data dell'ordine nell'intestazione, questa viene copiata nel campo **Data ordine** in tutte le righe e tutti i campi data correlati vengono ricalcolati.  

## <a name="default-values-for-lead-time-calculation"></a>Valori predefiniti per il calcolo del lead time

[!INCLUDE[prod_short](includes/prod_short.md)] utilizza il valore del campo **Calcolo lead time** nella riga dell'ordine acquisto per calcolare l'ordine e le date carico previste.  

È possibile specificare manualmente il valore sulla riga o lasciare che il programma utilizzi i valori definiti nella scheda fornitore, nella scheda articolo, nella scheda unità di stockkeeping o nel catalogo del fornitore articolo.
Tuttavia, il valore del lead time sulla scheda fornitore viene utilizzato solo se non è specificato un lead time nella scheda articolo, nella scheda unità di stockkeeping o nel catalogo fornitore per l'articolo. Questo è anche l'ordine di priorità di riassegnazione per questi valori. Se sono tutti forniti, il lead time dalla scheda fornitore ha la priorità più bassa e il lead time dal catalogo fornitore dell'articolo ha la priorità più alta.  

## <a name="see-also"></a>Vedere anche

[Calcolo della data per le vendite](sales-date-calculation-for-sales.md)   
[Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]