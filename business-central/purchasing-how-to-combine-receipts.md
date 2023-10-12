---
title: Combinare i carichi in una singola fattura
description: 'Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione Cumula carichi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '136, 145, 146, 9308'
ms.date: 08/03/2022
ms.author: bholtorf
---
# Combinare i carichi in una singola fattura

Se desideri fatturare più di un carico di acquisto per volta, puoi selezionare più righe di carico sulla fattura di acquisto.  

Prima di creare un carico di acquisto cumulato, è necessario che venga registrato più di un carico per lo stesso fornitore nella stessa valuta. In altri termini, è necessario compilare due o più ordini di acquisto e registrarli come ricevuti, ma non fatturati.  

Quando i carichi di acquisto vengono cumulati in una fattura e registrati, viene creata una fattura di acquisto registrata per le righe fatturate. Il campo **Quantità fatturata** dell'ordine di acquisto o dell'ordine di acquisto programmato di origine viene aggiornato in base alla quantità fatturata. Tuttavia, il documento di acquisto originale non viene eliminato, anche se è stato completamente ricevuto e fatturato; è necessario quindi eliminare il documento di acquisto manualmente.  

> [!NOTE]
> La fattura di acquisto risultante non può essere successivamente corretta o annullata. Se si desidera modificare una fattura di acquisto creata in questo modo, è necessario utilizzare le note di credito di acquisto. Per ulteriori informazioni, vedere [Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## Per cumulare i carichi

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).  
3. Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di carico**.  
4. Selezionare più righe di carico che si desidera includere nella fattura.  

    Se è stata selezionata una riga di carico non corretta o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura di acquisto ed eseguire nuovamente la funzione **Prendi righe di carico**.  
5. Per registrare la fattura scegliere l'azione **Registra**.  

## Per rimuovere ordini di acquisto aperti dopo la registrazione del carico cumulativa

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Elimina ordini acquisto fatturati**, quindi seleziona il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Scegliere il pulsante **OK**.  

In alternativa, eliminare i singoli ordini manualmente.

Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di acquisto programmati.

## Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
