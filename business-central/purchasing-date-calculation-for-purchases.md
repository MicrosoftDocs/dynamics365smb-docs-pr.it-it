---
title: Calcolo della data per gli acquisti | Documenti Microsoft
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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 08d2f6498019b8ee0a646cec891ff897a62dc9de
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801762"
---
# <a name="date-calculation-for-purchases"></a>Calcolo della data per gli acquisti
[!INCLUDE[d365fin](includes/d365fin_md.md)] calcola automaticamente la data in cui sarà necessario ordinare un articolo da avere in magazzino in una determinata data. Questa è la data in cui si può prevedere che gli articoli ordinati in una data particolare possano essere disponibili per il prelievo.  

Se si specifica una data di carico richiesta nella testata di un ordine di acquisto, la data dell'ordine calcolata è la data in cui si deve effettuare l'ordine per ricevere gli articoli alla data richiesta. Quindi, la data in cui gli articoli saranno disponibili per il prelievo viene calcolata e immessa nel campo **Data carico prevista**.  

Se non si specifica una data di carico richiesta, la data d'ordine presente sulla riga verrà usata come data di partenza per il calcolo della data prevedibile per la ricezione degli articoli e della data in cui gli articoli saranno disponibili per il prelievo.  

## <a name="calculating-with-a-requested-receipt-date"></a>Calcolo con una data di carico richiesta  
Se è presente una data di carico richiesta sulla riga dell'ordine di acquisto, questa data verrà utilizzata come data di partenza per i calcoli successivi.  

- data di carico richiesta - calcolo lead time = data ordine  
- data di carico richiesta + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista  

Se è stata immessa una data di carico richiesta sulla testata dell'ordine di acquisto, questa data viene copiata nel campo corrispondente in tutte le righe. È possibile modificare questa data in qualsiasi riga oppure rimuoverla.  

## <a name="calculating-without-a-requested-delivery-date"></a>Calcolo senza una data di consegna richiesta  
Se si immette una riga di ordine di acquisto senza una data di consegna richiesta, il campo **Data ordine** nella riga viene compilato con la data nel campo **Data ordine** dell'intestazione dell'ordine di acquisto. Si tratta della data immessa o della work date. Le date seguenti vengono quindi calcolate per la riga dell'ordine di acquisto, con la data dell'ordine come punto di partenza.  

- data ordine + calcolo lead time = data carico pianificato  
- data carico pianificato + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista  

Se si modifica la data dell'ordine sulla riga, ad esempio quando gli articoli non sono disponibili presso il fornitore fino a una data successiva, le date corrispondenti nella riga saranno ricalcolate automaticamente.  

Se si modifica la data dell'ordine nell'intestazione, questa viene copiata nel campo **Data ordine** in tutte le righe e tutti i campi data correlati vengono ricalcolati.  

## <a name="see-also"></a>Vedi anche  
 [Calcolo della data per le vendite](sales-date-calculation-for-sales.md)   
 [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
