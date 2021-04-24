---
title: 'Procedura: Cumulare i carichi | Documenti Microsoft'
description: Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione Cumula carichi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 86617934ecdb0ac2f14f6cf717f8091ba96caf95
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772581"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Combinare i carichi in una singola fattura

Se si desidera fatturare più di un carico di acquisto per volta, utilizzare la funzione **Cumula carichi**.  

Prima di creare un carico di acquisto cumulato, è necessario che venga registrato più di un carico per lo stesso fornitore nella stessa valuta. In altri termini, è necessario compilare due o più ordini di acquisto e registrarli come ricevuti, ma non fatturati.  

Quando i carichi di acquisto vengono cumulati in una fattura e registrati, viene creata una fattura di acquisto registrata per le righe fatturate. Il campo **Quantità fatturata** dell'ordine di acquisto o dell'ordine di acquisto programmato di origine viene aggiornato in base alla quantità fatturata. Tuttavia, il documento di acquisto originale non viene eliminato, anche se è stato completamente ricevuto e fatturato; è necessario quindi eliminare il documento di acquisto manualmente.  

> [!NOTE]
> La fattura di acquisto risultante non può essere successivamente corretta o annullata. Se si desidera modificare una fattura di acquisto creata in questo modo, è necessario utilizzare le note di credito di acquisto. Per ulteriori informazioni, vedere [Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Per cumulare i carichi

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture acquisto** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).  
3. Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di carico**.  
4. Selezionare più righe di carico che si desidera includere nella fattura.  

    Se è stata selezionata una riga di carico non corretta o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura di acquisto ed eseguire nuovamente la funzione **Prendi righe di carico**.  
5. Per registrare la fattura scegliere l'azione **Registra**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Per rimuovere ordini di acquisto aperti dopo la registrazione del carico cumulativa

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina ordini acquisto fatturati** e quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Scegliere il pulsante **OK**.  

In alternativa, eliminare i singoli ordini manualmente.

Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di acquisto programmati.

## <a name="see-also"></a>Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Correggere o annullare le fatture di acquisto non pagate](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]