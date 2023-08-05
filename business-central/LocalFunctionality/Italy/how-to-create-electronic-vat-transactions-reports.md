---
title: 'Creare report elettronici di transazioni IVA [IT]'
description: È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/29/2021
ms.author: edupont
---
# Creare i report elettronici di transazioni IVA nella versione italiana
È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata. Inviare il report alle autorità fiscali.  

## Per creare un report di transazioni IVA  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Report IVA**, quindi scegli il collegamento correlato.  
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

## Vedere anche  
 [IVA italiana](italian-vat.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]