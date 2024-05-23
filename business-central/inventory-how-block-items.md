---
title: Come bloccare articoli o varianti di articoli in documenti di vendita o di acquisto
description: Puoi bloccare articoli e varianti di articoli in modo che non vengano immessi nelle righe di documenti di acquisto o di vendita e non vengano registrati in una transazione.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
ms.service: dynamics-365-business-central
---
# Bloccare articoli o varianti di articoli in documenti di vendita o di acquisto

Puoi bloccare articoli e varianti di articoli in modo che non vengano immessi nelle righe di documenti di acquisto o di vendita e puoi bloccarli in modo che non vengano registrati nelle transazioni. Ad esempio, questo è utile quando un articolo presenta un difetto noto. Se qualcuno sceglie un articolo o una variante bloccato in un documento di vendita o di acquisto, un messaggio informerà che l'articolo è bloccato.

Nella tabella seguente vengono illustrati diversi scenari che si verificano quando gli articoli o le varianti vengono bloccati.  

|Opzione|Descrizione|  
|--------------------|------------|  
|**Vendite bloccate**|Non puoi scegliere l'articolo o la variante in un documento di vendita né nel giornale di registrazione articoli di vendita.|  
|**Acquisti bloccati**|Non puoi scegliere l'articolo o la variante in un documento di acquisto, in un giornale di registrazione articoli di acquisto o nei processi di pianificazione degli acquisti.|  
|**Bloccato**|Non puoi includere l'articolo o la variante quando registri le transazioni.|  

> [!NOTE]
> Gli articoli bloccati possono essere restituiti. Ciò significa che nessuna delle impostazioni descritte precedentemente si applica agli ordini di reso e nelle note di credito.

Quando usi l'azione **Copia da documento** per creare nuovi documenti basati su documenti esistenti, vieni avvisato se eventuali articoli o varianti nelle righe del documento di origine sono bloccati. Le righe del documento bloccate sono escluse dal nuovo documento e una notifica mostra una panoramica di tutte le righe del documento che sono bloccate nel documento di origine.

## Per bloccare un articolo  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli** e scegli il collegamento correlato.  
2. A seconda di ciò che vuoi fare, seleziona l'articolo e scegli una o più delle seguenti caselle di controll:
    * **Bloccato**
    * **Vendite bloccate**
    * **Acquisti bloccati**  

## Per bloccare una variante di articolo  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli** e scegli il collegamento correlato.  
2. Seleziona l'articolo che ha una variante che desideri bloccare, scegli **Varianti**, quindi seleziona una o più delle seguenti caselle di controllo:  
    * **Bloccato**
    * **Vendite bloccate**
    * **Acquisti bloccati**

## Vedi anche  

[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]