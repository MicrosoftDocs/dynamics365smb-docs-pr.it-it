---
title: Come stornare la registrazione dell'output | Microsoft Docs
description: La registrazione dell'output deve essere stornata in tre casi diversi. È possibile, ad esempio, che si verifichi un errore di immissione dei dati e che in un ordine di produzione venga registrata una quantità di output non corretta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cad24d75cacc290ea69f3a4488efd8dc9832a42c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787779"
---
# <a name="reverse-output-posting"></a>Stornare la registrazione dell'output
La registrazione dell'output deve essere stornata in tre casi diversi. È possibile, ad esempio, che si verifichi un errore di immissione dei dati e che in un ordine di produzione venga registrata una quantità di output non corretta.  

## <a name="to-reverse-an-output-posting"></a>Per stornare una registrazione di output  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni output** e quindi scegliere il collegamento correlato. Selezionare il batch.  
2. Compilare i campi come necessario. Per ulteriori informazioni, vedere [Registrare l'output e i tempi di lavorazione tramite processo batch](production-how-to-post-output-quantity.md).
3.  Nel campo **Collega-a movimento** selezionare il movimento contabile articolo associato. In questo modo, verranno stornati i movimenti contabili articolo e capacità.  
4. Registrare lo storno mediante la contabilizzazione delle registrazioni.  

I movimenti delle registrazioni di output verranno registrati nei movimenti contabili magazzino come rettifica positiva.  

## <a name="see-also"></a>Vedi anche  
 [Manufacturing](production-manage-manufacturing.md)    
 [Impostazione della produzione](production-configure-production-processes.md)  
 [Pianif.](production-planning.md)      
 [Magazzino](inventory-manage-inventory.md)  
 [Acquisti](purchasing-manage-purchasing.md)  
 [Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]