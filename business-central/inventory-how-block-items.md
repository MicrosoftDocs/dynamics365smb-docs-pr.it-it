---
title: Come bloccare gli articoli per la vendita o l'acquisto
description: È possibile bloccare un articolo in modo che non venga immesso nelle righe dei documenti di acquisto o di vendita e non venga registrato in una transazione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="block-items-from-sales-or-purchasing" />Bloccare gli articoli per la vendita o l'acquisto

È possibile bloccare un articolo in modo che non venga immesso nelle righe dei documenti di acquisto o di vendita ed è possibile bloccarlo in modo che non venga registrato in una qualsiasi transazione. Ad esempio, questo è utile quando un articolo presenta un difetto noto. Se qualcuno sceglie un articolo bloccato su un documento di vendita o di acquisto, un messaggio informerà che l'articolo è bloccato.

Nella tabella seguente vengono illustrati diversi scenari che si verificano quando gli articoli sono bloccati.  

|Opzione|Descrizione|  
|--------------------|------------|  
|**Vendita bloccata**|Non è possibile immettere l'articolo in un documento di vendita né nel giornale di registrazione articoli di vendita.|  
|**Acquisto bloccato**|Non è possibile immettere l'articolo in un documento di acquisto, in un giornale di registrazione articoli di acquisto o nei processi di pianificazione degli acquisti.|  
|**Bloccato**|Non puoi includere l'articolo nelle transazioni.|  

> [!NOTE]
> Gli articoli bloccati possono essere restituiti. Ciò significa che nessuna delle impostazioni descritte precedentemente si applica agli ordini di reso e nelle note di credito.

Quando si utilizza l'azione **Copia da documento** per creare nuovi documenti basati su documenti esistenti, si viene avvisati se eventuali elementi nelle righe del documento di origine sono bloccati. Le righe del documento bloccate sono escluse dal nuovo documento e una notifica mostra una panoramica di tutte le righe del documento che sono bloccate nel documento di origine.

## <a name="to-block-an-item-from-being-entered-on-sales-lines" />Per bloccare un articolo in modo che non venga immesso in righe di vendita

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Seleziona l'articolo che desideri bloccare e quindi seleziona la casella di controllo **Vendita bloccata**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines" />Per bloccare un articolo in modo che non venga immesso in righe di acquisto

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Acquisto bloccato**.  

## <a name="to-block-an-item-from-being-posted" />Per bloccare un articolo in modo che non venga contabilizzato

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.
2. Selezionare l'articolo che si desidera bloccare e quindi selezionare la casella di controllo **Bloccato**.

## <a name="see-also" />Vedere anche

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
