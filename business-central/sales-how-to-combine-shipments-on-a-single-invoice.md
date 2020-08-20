---
title: 'Procedura: Combinare le spedizioni in una singola fattura | Documenti Microsoft'
description: Se si desidera fatturare più di una spedizione per volta, utilizzare la funzionalità per le spedizioni cumulate.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f6ce4c0c304fc8255789ec91fb3a00ba78170d6d
ms.sourcegitcommit: 6078bc9b2b571248d779722ce4125f250e7a3922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/07/2020
ms.locfileid: "3666924"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Combinare le spedizioni in una singola fattura
Se si desidera fatturare più di una spedizione per volta, utilizzare la funzionalità per le spedizioni cumulate.  

Prima di creare una spedizione cumulata, è necessario che venga registrata più di una spedizione di vendita per lo stesso cliente nella stessa valuta. In altri termini, è necessario creare due o più ordini di vendita e registrarli come spediti, ma non fatturati. 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Per combinare manualmente le spedizioni in una singola fattura  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture vendite** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).
3. Nel campo **Vendere a - Nr. cliente** immettere il cliente che riceverà la fattura per gli articoli spediti.  
4. Nella Scheda dettaglio **Righe** scegliere l'azione **Prendi righe di spedizione**.  
5. Selezionare le righe di spedizione che si desidera includere nella fattura:  

    - Per inserire tutte le righe, selezionare tutte le righe, quindi fare clic su **OK**.  
    - Per inserire righe specifiche, selezionare le righe, quindi fare clic su **OK**. È possibile utilizzare il tasto CTRL per selezionare più righe non consecutive.  

    Se viene selezionata una riga di spedizione errata o si desidera effettuare di nuovo la selezione, eliminare semplicemente le righe nella fattura ed eseguire nuovamente la funzione **Prendi righe di spedizione**.  
7. Per registrare la fattura scegliere l'azione **Registra**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Per combinare automaticamente le spedizioni in una singola fattura  
[!INCLUDE[d365fin](includes/d365fin_md.md)] selezionerà solo gli ordini di vendita in cui **Fatture cumulative** è scelto. 

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture cumulative** e quindi scegliere il collegamento correlato. Viene visualizzata la pagina di richiesta del processo batch.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Scegliere la casella di controllo **Registra fatture**.  
4. Scegliere il pulsante **OK**.  

> [!NOTE]  
>  Se la casella di controllo **Registra fatture** non è selezionata per il processo batch, sarà necessario registrare manualmente le fatture.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Per rimuovere ordini di vendita aperti dopo la registrazione della spedizione combinata 
Quando le spedizioni vengono cumulate in una fattura e registrate, per le righe fatturate viene creata una fattura di vendita registrata. Il campo **Quantità fatturata** dell'ordine di vendita o dell'ordine di vendita programmato di origine viene aggiornato in base alla quantità fatturata.  

Quando si fatturano spedizioni in questo modo, gli ordini da cui sono state registrate le spedizioni vengono mantenuti, anche se sono già stati completamente spediti e fatturati.   

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina ord. vendita fatturati** e quindi selezionare il collegamento correlato.  
2. Specificare nel campo del filtro **Nr.** quali ordini di vendite eliminare.  
3. Scegliere il pulsante **OK**.  

In alternativa, eliminare i singoli ordini di vendita manualmente.  

Ripetere i passaggi da 1 a 3 per tutti gli altri documenti interessati, ad esempio gli ordini di vendita programmati.

## <a name="see-also"></a>Vedere anche  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
