---
title: 'Procedura: Creare report elettronici di transazioni IVA'
description: È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata. Inviare il report alle autorità fiscali.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 7a7f33e785b7aba371b74ff9695105722d99b828
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246357"
---
# <a name="create-electronic-vat-transactions-reports"></a>Creare report elettronici di transazioni IVA
È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata. Inviare il report alle autorità fiscali.  

## <a name="to-create-a-vat-transactions-report"></a>Per creare un report di transazioni IVA  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Report IVA**, quindi scegliere il collegamento correlato.  
2.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |-------------------------------------|---------------------------------------|  
    |**Senza contratto**|I movimenti IVA che hanno generato questa riga non sono associati a un contratto.|  
    |**Contratto**|I movimenti IVA che hanno generato questa riga sono associati a un contratto.|  
    |**Altro**|I movimenti IVA che hanno generato questa riga non sono associati a un contratto speciale, ad esempio per manutenzione in corso o altre eccezioni.|  

    > [!TIP]  
    >  In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], il contratto che le autorità fiscali cercano può essere ordini programmati oppure contratti di assistenza. Per identificare se la riga del report IVA appartiene a un ordine programmato o a un contratto di assistenza, è possibile eseguire il drill-down per visualizzare i movimenti IVA sottostanti dal campo **Importo**.  

Le note di credito vengono incluse nel report transazioni IVA se il cliente o il fornitore è di un paese esterno all'UE e non incluso nella blacklist. Per ulteriori informazioni, vedere [IVA italiana](italian-vat.md).  

Dopo avere creato il report IVA, è necessario inviarlo alle autorità fiscali. Per ulteriori informazioni, vedere [Esportare i report di transazioni IVA](how-to-export-vat-transactions-reports.md).  

## <a name="see-also"></a>Vedi anche  
 [IVA italiana](italian-vat.md)
