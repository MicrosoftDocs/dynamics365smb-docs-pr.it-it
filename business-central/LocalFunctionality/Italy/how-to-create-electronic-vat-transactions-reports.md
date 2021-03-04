---
title: 'Procedura: Creare report elettronici di transazioni IVA'
description: È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata. Inviare il report alle autorità fiscali.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 486732b9b5d8b4ec5f7acbec08dafe0eb9eff3b3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749638"
---
# <a name="create-electronic-vat-transactions-reports"></a>Creare report elettronici di transazioni IVA
È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata. Inviare il report alle autorità fiscali.  

## <a name="to-create-a-vat-transactions-report"></a>Per creare un report di transazioni IVA  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Report IVA** e quindi scegliere il collegamento correlato.  
2.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |-------------------------------------|---------------------------------------|  
    |**Senza contratto**|I movimenti IVA che hanno generato questa riga non sono associati a un contratto.|  
    |**Contratto**|I movimenti IVA che hanno generato questa riga sono associati a un contratto.|  
    |**Altro**|I movimenti IVA che hanno generato questa riga non sono associati a un contratto speciale, ad esempio per manutenzione in corso o altre eccezioni.|  

    > [!TIP]  
    >  In [!INCLUDE[prod_short](../../includes/prod_short.md)], il contratto che le autorità fiscali cercano può essere ordini programmati oppure contratti di assistenza. Per identificare se la riga del report IVA appartiene a un ordine programmato o a un contratto di assistenza, è possibile eseguire il drill-down per visualizzare i movimenti IVA sottostanti dal campo **Importo**.  

Le note di credito vengono incluse nel report transazioni IVA se il cliente o il fornitore è di un paese esterno all'UE e non incluso nella blacklist. Per ulteriori informazioni, vedere [IVA italiana](italian-vat.md).  

Dopo avere creato il report IVA, è necessario inviarlo alle autorità fiscali. Per ulteriori informazioni, vedere [Esportare i report di transazioni IVA](how-to-export-vat-transactions-reports.md).  

## <a name="see-also"></a>Vedere anche  
 [IVA italiana](italian-vat.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]