---
title: Come stornare la registrazione dell'output | Microsoft Docs
description: "La registrazione dell'output deve essere stornata in tre casi diversi. È possibile, ad esempio, che si verifichi un errore di immissione dei dati e che in un ordine di produzione venga registrata una quantità di output non corretta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f2430dcf45303e04baad406880783ab0f74dd4f2
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-output-posting"></a>Stornare la registrazione dell'output
La registrazione dell'output deve essere stornata in tre casi diversi. È possibile, ad esempio, che si verifichi un errore di immissione dei dati e che in un ordine di produzione venga registrata una quantità di output non corretta.  

## <a name="to-reverse-an-output-posting"></a>Per stornare una registrazione di output  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni output**, quindi scegliere il collegamento correlato. Selezionare il batch.  
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
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

