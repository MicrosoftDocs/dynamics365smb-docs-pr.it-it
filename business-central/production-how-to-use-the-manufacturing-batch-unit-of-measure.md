---
title: Utilizzare l'unità di misura batch di produzione
description: Questo argomento offre una panoramica su come utilizzare le unità di misura batch di produzione in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
---
# Utilizzare le unità di misura batch di produzione
Se un articolo viene inserito in stock utilizzando un'unità di misura ma viene prodotto in un'altra, viene creato un ordine di produzione che utilizza un'unità di misura batch di produzione per calcolare la quantità corretta di componenti durante il processo batch **Aggiorna ordine produzione**. Un esempio di calcolo di un'unità di misura è il caso in cui un articolo prodotto viene inserito in stock in pezzi, ma viene prodotto in tonnellate.  

## Per creare una DB di produzione tramite un'unità di misura batch  
1.  L'unità di misura batch di produzione viene impostata come unità di misura alternativa nella pagina **Unità di misura articoli** nell'articolo da produrre. L'unità di misura batch non sostituisce l'unità di misura di base nell'articolo.  
2.  Creare una distinta base di produzione per l'articolo impostato con l'unità di misura batch di produzione. Per ulteriori informazioni, vedere [Creare distinte base di produzione](production-how-to-create-production-boms.md).  
3.  Nel campo **Codice unità di misura** selezionare l'unità di misura base di produzione.  
4.  Per ogni riga della DB di produzione, nel campo **Quantità per** immettere la quantità di questo articolo componente necessaria per creare l'unità di misura batch.  
5.  Aprire la **Scheda articolo** per l'articolo correlato.  

    Nella Scheda dettaglio **Rifornimento**, nel campo **Nr. DB di produzione**, selezionare la DB di produzione creata in precedenza.  
6.  Creare una testata dell'ordine di produzione utilizzando l'articolo impostato con l'unità di misura batch di produzione. Per ulteriori informazioni, vedere [Creare ordini di produzione](production-how-to-create-production-orders.md).  
7.  Scegliere l'azione **Aggiorna**, quindi scegliere il pulsante **OK**.  

Nella Scheda dettaglio **Righe**, scegliere l'azione **Riga** e quindi l'azione **Componenti** per visualizzare il risultato. L'applicazione calcola la quantità corretta di componenti necessari per soddisfare la DB di produzione in base all'unità di misura batch di produzione.  

## Per calcolare un'unità di misura batch di produzione in un ordine di produzione  
1.  Creare una testata dell'ordine di produzione utilizzando l'articolo impostato con l'unità di misura batch di produzione.  
2.  Nel campo **Nr. articolo** nella riga dell'ordine di produzione digitare lo stesso numero di articolo utilizzato nella testata.  
3.  Nel campo **Quantità** immettere la stessa quantità utilizzata nella testata.  
4.  Nel campo **Codice unità di misura** selezionare il codice unità di misura del batch di produzione.  
5.  Scegliere l'azione **Aggiorna**.
6.  Nella Scheda dettaglio **Calcola** deselezionare la casella di controllo **Righe**.  
7.  Scegliere il pulsante **OK**.  
8.  Nella Scheda dettaglio **Righe**, scegliere l'azione **Riga** e quindi l'azione **Componenti** per visualizzare il risultato. La quantità corretta di componenti necessari per soddisfare la DB di produzione viene calcolata in base all'unità di misura batch di produzione.  

## Vedi anche  
[Creare cicli](production-how-to-create-routings.md)  
[Creare le distinte base di produzione](production-how-to-create-production-boms.md)     
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Pianif.](production-planning.md)   
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]