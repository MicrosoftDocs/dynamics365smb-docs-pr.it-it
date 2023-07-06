---
title: Calcolare le date per gli acquisti
description: Questo articolo descrive come calcolare le date per gli acquisti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
---
# <a name="calculate-dates-for-purchases"></a><a name="calculate-dates-for-purchases"></a><a name="calculate-dates-for-purchases"></a>Calcolare le date per gli acquisti

Se vuoi avere gli articoli in inventario in una certa data, [!INCLUDE[prod_short](includes/prod_short.md)] può calcolare automaticamente la data in cui è necessario ordinarli. 

Il risultato è la data in cui puoi ritirare gli articoli che hai ordinato.  

Se specifichi una data di carico richiesta in una riga ordine di acquisto, la data dell'ordine calcolata è la data in cui è necessario effettuare l'ordine. La data in cui gli articoli saranno disponibili per il prelievo viene visualizzata nel campo **Data carico prevista**.  

Se non specifichi una data di carico richiesta, la data in cui prevedi di ricevere gli articoli si basa sulla data dell'ordine nella riga. 

La data di carico è anche la data in cui gli articoli saranno disponibili per il prelievo.  

> [!TIP]
> Per impostazione predefinita, molti dei campi della data citati in questo articolo sono nascosti nelle righe dell'ordine fornitore. Se un campo non è disponibile, puoi aggiungerlo personalizzando la pagina. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date"></a><a name="calculating-with-a-requested-receipt-date"></a><a name="calculating-with-a-requested-receipt-date"></a>Calcolo con una data di carico richiesta

Se è presente una data di carico richiesta sulla riga dell'ordine di acquisto, questa data verrà utilizzata per i calcoli seguenti:  

- data di carico richiesta - calcolo lead time = data ordine  
- data di carico richiesta + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista  

Se specifichi una data di carico richiesta in una riga dell'ordine d'acquisto, tale data viene assegnata alle nuove righe man mano che vengono create. Puoi modificare o rimuovere la data nelle righe.  

> [!NOTE]
> Se il processo si basa sul calcolo indietro, ad esempio, se si utilizza la data carico richiesta per ottenere la data dell'ordine, si consiglia di utilizzare formule di data con durate fisse, ad esempio "5D" per cinque giorni o "1W" per una settimana. Le formule di data senza durate fisse, come "CW" per settimana corrente o CM per mese corrente, possono comportare calcoli della data errati. Per ulteriori informazioni sulle formule di data, vedere [Utilizzare date e orari del calendario](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date"></a><a name="calculating-without-a-requested-receipt-date"></a><a name="calculating-without-a-requested-receipt-date"></a>Calcolo senza una data di carico richiesta

Se si immette una riga di ordine di acquisto senza una data di consegna richiesta, il campo **Data ordine** nella riga mostra la data nel campo **Data ordine** dell'intestazione dell'ordine di acquisto. È la data immessa o la data di lavoro. Le date vengono quindi calcolate per la riga dell'ordine di acquisto, con la data dell'ordine come punto di partenza come segue:  

- data ordine + calcolo lead time = data carico pianificato  
- data carico pianificato + tempo gest. entrata in whse. + lead time di sicurezza = data carico prevista  

Se modifichi la data dell'ordine sulla riga, [!INCLUDE[prod_short](includes/prod_short.md)] ricalcola le altre date.  

## <a name="default-values-for-lead-time-calculation"></a><a name="default-values-for-lead-time-calculation"></a><a name="default-values-for-lead-time-calculation"></a>Valori predefiniti per il calcolo del lead time

[!INCLUDE[prod_short](includes/prod_short.md)] utilizza la formula della data nel campo **Calcolo lead time** nella riga dell'ordine acquisto per calcolare l'ordine e le date carico previste.  

È possibile specificare manualmente la formula della data sulle righe. Altrimenti, [!INCLUDE[prod_short](includes/prod_short.md)] utilizzerà le formule definite nelle pagine seguenti in questo ordine di priorità:

1. Catalogo articolo/fornitore
2. Scheda articolo
3. Scheda unità di stockkeeping
4. Scheda fornitore

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/estimate-receipt-dates-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Calcolo della data per le vendite](sales-date-calculation-for-sales.md)  
[Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
