---
title: "Come registrare le capacità | Microsoft Docs"
description: "Nelle registrazioni delle rettifiche delle capacità vengono registrate le capacità utilizzate che non sono assegnate all'ordine di produzione. La manutenzione, ad esempio, deve essere assegnata alla capacità ma non a un ordine di produzione."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a30e62bf2bf62c547398d733fcfe80b0204805cf
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a>Registrare le capacità
Nelle registrazioni delle rettifiche delle capacità vengono registrate le capacità utilizzate che non sono assegnate all'ordine di produzione. La manutenzione, ad esempio, deve essere assegnata alla capacità ma non a un ordine di produzione.  

## <a name="to-post-capacities"></a>Per registrare le capacità  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni capacità**, quindi scegliere il collegamento correlato.  
2.  Immettere la **data di registrazione** e il **nr. di documento** .  
3.  Immettere nel campo **Tipo** il tipo di capacità, **Centri di Lavoro** o **Aree di Produzione** che si sta registrando.  
4.  Nel campo **Nr.** immettere il numero del centro di lavoro o dell'area di produzione.  
5.  Compilare i campi rimanenti **Ora Inizio**, **Ora Fine**, **Quantità** e **Scarto** inserendo i relativi dati.  
6.  Per registrare le capacità scegliere l'azione **Registra**.  

## <a name="to-view-work-center-ledger-entries"></a>Per visualizzare i movimenti contabili relativi alle aree di produzione:  
Nelle finestre **Scheda area di produzione** e **Scheda centri lavoro**, è possibile visualizzare le capacità registrate come risultato di ordini di produzione chiusi.    
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Aree di produzione** e quindi scegliere il collegamento correlato.  
2.  Aprire la scheda **Area di produzione** pertinente dall'elenco e scegliere l'azione **Movimenti contabili capacità**.  

Nella finestra **Movimenti Contabili Capacità** vengono visualizzati i movimenti registrati relativi all'area di produzione in ordine di registrazione.   

## <a name="see-also"></a>Vedi anche  
[Manufacturing](production-manage-manufacturing.md)    
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)      
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

