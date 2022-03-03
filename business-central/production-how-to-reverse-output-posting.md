---
title: Stornare la registrazione dell'output
description: La registrazione dell'output deve essere stornata in tre casi diversi. Questo argomento descrive la procedura per lo storno della registrazione di output.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: ed45facfc64dda670d0e1e4d7dd9b396b4c11fae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132787"
---
# <a name="reverse-output-posting"></a>Stornare la registrazione dell'output

La registrazione dell'output deve essere stornata in tre casi diversi. È possibile, ad esempio, che si verifichi un errore di immissione dei dati e che in un ordine di produzione venga registrata una quantità di output non corretta.  

## <a name="to-reverse-an-output-posting"></a>Per stornare una registrazione di output

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni output**, quindi scegli il collegamento correlato. Selezionare il batch.  
2. Compilare i campi come necessario. Per ulteriori informazioni, vedere [Registrare l'output e i tempi di lavorazione tramite processo batch](production-how-to-post-output-quantity.md).
3. Nel campo **Collega-a movimento** selezionare il movimento contabile articolo associato. In questo modo, verranno stornati i movimenti contabili articolo e capacità.  
4. Registrare lo storno mediante la contabilizzazione delle registrazioni.  

I movimenti delle registrazioni di output verranno registrati nei movimenti contabili magazzino come rettifica positiva.  

## <a name="see-also"></a>Vedi anche

 [Manufacturing](production-manage-manufacturing.md) [Impostazione della produzione](production-configure-production-processes.md)  
 [Pianif.](production-planning.md)  
 [Magazzino](inventory-manage-inventory.md)  
 [Acquisti](purchasing-manage-purchasing.md)  
 [Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]