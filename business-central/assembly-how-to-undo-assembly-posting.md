---
title: Come annullare la registrazione di assemblaggi | Microsoft Docs
description: Talvolta può essere necessario annullare un ordine di assemblaggio registrato, ad esempio se l'ordine è stato registrato con errori che devono essere corretti o perché non avrebbe dovuto essere inizialmente registrato ed è necessario eseguirne il rollback.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4526ad4284cd3970e1573a1a8ea914cbd6253c83
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772881"
---
# <a name="undo-assembly-posting"></a>Annullare la registrazione di assemblaggi
Talvolta può essere necessario annullare un ordine di assemblaggio registrato, ad esempio se l'ordine è stato registrato con errori che devono essere corretti o perché non avrebbe dovuto essere inizialmente registrato ed è necessario eseguirne il rollback.

Se si annulla un ordine di assemblaggio registrato, viene creato un set di movimenti contabili articoli correttivi per stornare i movimenti originali. Ogni movimento di output positivo per l'articolo di assemblaggio viene stornato da un movimento di output negativo. Ogni movimento di consumo negativo per un componente di assemblaggio viene stornato da un movimento di consumo positivo. Il collegamento a costo fisso viene creato automaticamente tra i movimenti correttivi e originali per assicurare lo storno del costo esatto.  

Quando si annulla un ordine di assemblaggio registrato completamente, è possibile scegliere di ricreare l'ordine di assemblaggio nel relativo stato originale, ad esempio per apportare correzioni prima di registrarlo di nuovo. In alternativa, è possibile evitare di ricreare l'ordine di assemblaggio.  

Quando si annulla parzialmente un ordine di assemblaggio registrato, tutti campi relativi alla quantità interessati, ad esempio i campi **Quantità assemblata**, **Quantità consumata** e **Quantità residua**, vengono riportati ai valori presenti prima della registrazione in questione.  

Per ricreare o ripristinare ordini di assemblaggio, le seguenti condizioni devono essere applicate all'articolo di assemblaggio risultante dalla registrazione originale:  

-   Deve ancora essere in magazzino, ovvero non viene venduto o in altro modo consumato dalle transazioni in uscita.  
-   Non deve essere impegnato.  
-   Deve essere presente nella collocazione in cui è stato inserito.  

Inoltre, gli ordini di assemblaggio esistenti possono essere ripristinati solo se il numero di righe e la sequenza di righe dell'ordine di assemblaggio originale non vengono modificati.  

> [!TIP]  
>  Per risolvere i conflitti dovuti a modifiche apportate alle righe, è possibile annullare manualmente le modifiche alle righe in questione prima di annullare l'ordine di assemblaggio registrato correlato. In alternativa, è possibile registrare l'ordine di assemblaggio completamente, quindi selezionare l'opzione per ricrearlo quando si annulla la registrazione.  

La procedura seguente illustra come annullare ordini di assemblaggio registrati in cui gli articoli sono stati assemblati per magazzino. Per annullare gli ordini di assemblaggio registrati in cui gli articoli sono stati assemblati in un ordine di vendita, è necessario utilizzare la funzione **Eliminare spedizione** nella spedizione registrata che si riferisce all'ordine di assemblaggio registrato. Per ulteriori informazioni, vedere [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md). L'annullamento dell'ordine di assemblaggio registrato viene quindi eseguito automaticamente come descritto in questo argomento.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Per annullare la registrazione di un ordine di assemblaggio  
1.  Per annullare un ordine di assemblaggio registrato completamente o parzialmente, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di assemblaggio registrati**, quindi selezionare il collegamento correlato.  

    Verrà visualizzata la pagina **Ordini di assemblaggio registrati** con uno o più ordini di assemblaggio che sono stati registrati dall'ordine di assemblaggio in questione. Ogni registrazione parziale crea un ordine di assemblaggio registrato separato.  
2.  Aprire l'ordine di assemblaggio registrato che si desidera annullare, quindi scegliere l'azione **Annulla assemblaggio**.  

    Se l'ordine di assemblaggio registrato che si desidera annullare si riferisce a un ordine di assemblaggio registrato completamente che è stato eliminato, è possibile scegliere di ricrearlo, solitamente perché si desidera rielaborarlo.  
3.  Se si desidera ricreare l'ordine di assemblaggio, fare clic sul pulsante **Sì**. Per annullare la registrazione senza ricreare l'ordine di assemblaggio correlato, fare clic sul pulsante **No**.  

Il campo **Stornato** nella testata ordine di assemblaggio viene impostato su **Sì**. La registrazione dell'ordine di assemblaggio è ora stornata ed è possibile procedere all'elaborazione dell'intero ordine di assemblaggio se si è scelto di ricrearlo o dell'ordine di assemblaggio aperto ripristinato allo stato originale.  

> [!NOTE]  
>  Per ripristinare quantità da registrazioni parziali multiple in un ordine di assemblaggio, è necessario annullare tutti gli ordini di assemblaggio registrati in questione seguendo i passaggi da 1 a 3 precedenti per ogni ordine di assemblaggio registrato.  

## <a name="see-also"></a>Vedere anche  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Stornare le registrazioni e annullare carichi/spedizioni errati.](finance-how-reverse-journal-posting.md)  
[Elaborare i resi o gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md)    
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]