---
title: Annullare la registrazione di assemblaggi
description: Scopri come correggere gli errori in un ordine di assemblaggio registrato.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="undo-assembly-posting"></a>Annullare la registrazione di assemblaggi

Annulla la registrazione di un ordine di assemblaggio per correggere un errore o rimuovere una registrazione indesiderata.

Se annulli un ordine di assemblaggio registrato, viene creato una serie di movimenti contabili articoli correttivi per stornare i movimenti originali. Ogni movimento di output positivo per l'articolo di assemblaggio viene stornato da un movimento di output negativo. Ogni movimento di consumo negativo per un componente di assemblaggio viene stornato da un movimento di consumo positivo. Il collegamento a costo fisso viene creato automaticamente tra i movimenti correttivi e originali per assicurare lo storno del costo esatto.  

Quando annulli un ordine di assemblaggio completamente registrato, puoi ricreare l'ordine originale. Ad esempio, per apportare correzioni prima di registrarlo di nuovo.  

Quando annulli parzialmente un ordine di assemblaggio registrato, tutti campi relativi alla quantità interessati, ad esempio i campi **Quantità assemblata**, **Quantità consumata** e **Quantità residua**, vengono riportati ai valori presenti prima della registrazione.  

Per ricreare o ripristinare ordini di assemblaggio, l'articolo nella registrazione originale deve soddisfare le seguenti condizioni:  

* Essere ancora in inventario. Ovvero non è stato venduto o in altro modo consumato dalle transazioni in uscita.  
* Non essere riservato.  
* Essere presente nella collocazione in cui è stato inserito.  

Gli ordini di assemblaggio esistenti possono essere ripristinati solo se il numero di righe e la sequenza di righe dell'ordine di assemblaggio originale non vengono modificati.  

> [!TIP]  
> Per risolvere i conflitti dovuti a modifiche apportate alle righe, annulla manualmente le modifiche alle righe in questione prima di annullare l'ordine di assemblaggio registrato. Puoi registrare l'ordine di assemblaggio, quindi selezionare l'opzione per ricrearlo quando si annulla la registrazione.  

La procedura seguente illustra come annullare ordini di assemblaggio registrati contenenti articoli che sono stati assemblati per magazzino. Per annullare gli ordini di assemblaggio registrati con articoli assemblati su ordine, utilizza l'azione **Annulla spedizione** nella relativa spedizione registrata. Per ulteriori informazioni sull'annullamento delle spedizioni, vedi [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md). L'annullamento dell'ordine di assemblaggio registrato viene eseguito come descritto in questo articolo.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Per annullare la registrazione di un ordine di assemblaggio

È possibile annullare in tutto o in parte gli ordini di assemblaggio registrati.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini assemblaggio registrati**, quindi scegli il collegamento correlato.  

   Ogni registrazione parziale crea un ordine di assemblaggio registrato separato.  
2. Aprire l'ordine di assemblaggio registrato che si desidera annullare, quindi scegliere l'azione **Annulla assemblaggio**.  

    Se l'ordine di assemblaggio registrato è correlato a un ordine di assemblaggio completamente registrato che è stato eliminato, è possibile ricreare l'ordine eliminato. Ad esempio, potresti ricreare l'ordine perché desideri rielaborarlo.  
3. Per ricreare l'ordine di assemblaggio, scegli **Sì**. Per annullare la registrazione senza ricreare l'ordine di assemblaggio correlato, scegli **No**.  

Il campo **Stornato** nell'ordine di assemblaggio viene impostato su **Sì**. La registrazione dell'ordine di assemblaggio è ora stornata. È possibile elaborare l'intero ordine di assemblaggio se hai scelto di ricrearlo o l'ordine di assemblaggio aperto ripristinato allo stato originale.  

> [!NOTE]  
> Per ripristinare quantità da registrazioni parziali multiple in un ordine di assemblaggio, è necessario annullare tutti gli ordini di assemblaggio registrati seguendo i passaggi da 1 a 3.  

## <a name="see-also"></a>Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md)  
[Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md)  
[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
