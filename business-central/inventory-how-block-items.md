---
title: Come bloccare gli articoli per la vendita o l'acquisto
description: In Business Central, un articolo può essere contrassegnato come bloccato per la vendita, per l'acquisto o per tutti gli scopi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e13d59e939e71a252e08afc26d2fb1ec76b247c9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238534"
---
# <a name="block-items-from-sales-or-purchasing"></a>Bloccare gli articoli per la vendita o l'acquisto
È possibile bloccare un articolo in modo che non venga immesso in righe di acquisto o di vendita ed è possibile bloccarlo in modo che non venga registrato in una qualsiasi transazione.  

Nella tabella seguente vengono descritti diversi scenari che si verificano quando gli articoli sono bloccati.  

|Opzione|Description|  
|--------------------|------------|  
|**Vendita bloccata**|Non è possibile immettere l'articolo in un documento di vendita né nel giornale di registrazione articoli di vendita.|  
|**Acquisto bloccato**|Non è possibile immettere l'articolo in un documento di acquisto, in un giornale di registrazione articoli di acquisto o nei processi di pianificazione degli acquisti.|  
|**Bloccato**|Non è possibile usare l'articolo per alcuna transazione articolo. Per ulteriori informazioni sul blocco di un articolo per tutti gli scopi, vedere la scheda Articolo.|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Per bloccare un articolo in modo che non venga immesso in righe di vendita  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.  
2.  Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Vendita bloccata**.  

Se si tenta di immettere l'articolo in un documento di vendita o in una riga di giornale di registrazione, viene visualizzato un errore indicante che l'articolo è bloccato.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Per bloccare un articolo in modo che non venga immesso in righe di acquisto  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.  
2.  Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Acquisto bloccato**.  

Se si tenta di immettere l'articolo in un documento di acquisto o in una riga di giornale di registrazione, viene visualizzato un errore indicante che l'articolo è bloccato.

## <a name="to-block-an-item-from-being-posted"></a>Per bloccare un articolo in modo che non venga contabilizzato
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Bloccato**.

Se si tenta di registrare un qualsiasi tipo di transazione per l'articolo, viene visualizzato un messaggio di errore indicante che l'articolo è bloccato.

## <a name="see-also"></a>Vedi anche  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  