---
title: Assemblaggio su ordine o assemblaggio per magazzino | Microsoft Docs
description: Gli articoli di assemblaggio possono essere approvvigionati assemblandoli quando vengono ordinati o assemblandoli per essere conservati in magazzino fino a quando non vengono richiesti in un ordine di vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8d1cf0c03a985245a507ec7e7970706bfad31b83
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880930"
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Assemblaggio su ordine e assemblaggio per magazzino
Gli articoli di assemblaggio possono essere forniti nei seguenti due processi:  

-   Assemblaggio su ordine.  
-   Assemblaggio per magazzino.  

## <a name="assemble-to-order"></a>Assemblaggio su ordine  
In genere si utilizza l'*assemblaggio su ordine* per gli articoli che non si desidera immagazzinare perché si prevede di personalizzarli in base alle richieste del cliente o perché si desidera ridurre i costi di trasporto a magazzino. La funzionalità di supporto include:  

-   Capacità di personalizzare gli articoli di assemblaggio quando si accetta un ordine di vendita.  
-   Panoramica della disponibilità dell'articolo di assemblaggio e dei relativi componenti.  
-   Capacità di impegnare componenti di assemblaggio immediatamente per garantire l'evasione dell'ordine.  
-   Funzione per determinare la redditività dell'ordine personalizzato eseguendo il roll up di prezzo e costo.  
-   Integrazione nella warehouse per facilitare assemblaggio e spedizione.  
-   Capacità di assemblare su ordine nella fase di creazione di un'offerta di vendita o di un ordine di vendita programmato.  
-   Capacità di combinare le quantità di magazzino con le quantità per l'assemblaggio su ordine.  

Nel processo di assemblaggio su ordine, l'articolo è assemblato in risposta a un ordine di vendita e con un collegamento uno-a-uno tra l'ordine di assemblaggio e l'ordine di vendita.  

Quando si immette un articolo da assemblare su ordine in una riga di vendita, viene creato automaticamente un ordine di assemblaggio con una testata basata sulla riga vendita e con righe basate sulla DB di assemblaggio dell'articolo moltiplicate per la quantità dell'ordine. È possibile utilizzare la pagina **Righe di assemblaggio su ordine** per visualizzare le righe dell'ordine di assemblaggio collegato allo scopo di supportare la personalizzazione dell'articolo di assemblaggio e una data di consegna basata su informazioni relative alla disponibilità dei componenti. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Benché non rientri nel processo di default, è possibile vendere le quantità di magazzino con le quantità per l'assemblaggio su ordine. Per altre informazioni, vedere [Vendere gli articoli di magazzino nei flussi assemblaggio su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 Per abilitare il processo, il campo **Criteri di assemblaggio** nella scheda articolo deve essere impostato su **Assemblaggio su ordine**.  

## <a name="assemble-to-stock"></a>Assemblaggio per magazzino  
 In genere si utilizza l'*assemblaggio per magazzino* per gli articoli che si desidera assemblare prima delle vendite, ad esempio preparare una campagna di kit e tenerli in stock fino a quando vengono ordinati. Tali articoli sono in genere articoli standard, ad esempio in kit in pacchetti di cui non viene offerta la personalizzazione in base richieste del cliente.  

 Nel processo di assemblaggio per magazzino, l'articolo è assemblato senza una richiesta di vendita immediata ed è immagazzinato nella warehouse come articolo di magazzino per la vendita o il consumo successivo come subassemblaggio. Per ulteriori informazioni, vedere [Assemblare articoli](assembly-how-to-assemble-items.md). Da questo punto, l'articolo è prelevato ed elaborato come singolo articolo e viene gestito come un articolo di produzione completato.  

 Quando si immette un articolo con assemblaggio per magazzino in una riga vendita, la riga come qualsiasi altro articolo risulta venduta da magazzino. Ad esempio, la disponibilità viene controllata solo per l'articolo di assemblaggio.  

> [!NOTE]  
>  Benché non rientri del processo di default, è possibile assemblare un articolo su ordine anche se è impostato per l'assemblaggio per magazzino. Per altre informazioni, vedere [Vendere insieme articoli assemblaggio su ordine e articoli in magazzino](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 Per abilitare il processo, il campo **Criteri di assemblaggio** nella scheda articolo deve essere impostato su **Assemblaggio per magazzino**.  

## <a name="combination-scenarios"></a>Scenari di combinazione  
 Il principio generale della gestione assemblaggio consiste nel fatto che una volta combinate in una riga ordine di vendita, le quantità per l'assemblaggio su ordine devono essere spedite prima delle quantità di magazzino.  

 Se un ordine di assemblaggio è collegato a una riga ordine di vendita, il valore del campo **Qtà per assemblaggio su ordine** nella riga ordine di vendita viene copiato nel campo **Quantità da assemblare** tramite il campo **Quantità** nell'intestazione dell'ordine di assemblaggio. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

 Inoltre, il valore nel campo **Quantità da assemblare** è correlato al campo **Qtà da spedire** nella riga ordine di vendita e tale relazione gestisce la spedizione delle quantità per l'assemblaggio su ordine, sia parzialmente che completamente. Questo vale sia quando la quantità completa della riga vendita è assemblata su ordine e negli scenari di combinazione in cui una parte della quantità della riga vendita è assemblata su ordine e un'altra parte viene spedita dal magazzino. Tuttavia, nello scenario di combinazione si dispone di flessibilità aggiuntiva in caso di spedizione parziale, in quanto è possibile modificare il campo **Quantità da assemblare**, in base a regole predefinite, per specificare quante unità vengono spedite parzialmente dal magazzino e quante unità vengono spedite parzialmente mediante assemblaggio su ordine.  

 Se la quantità completa della riga di vendita deve essere assemblata su ordine e spedita, il valore del campo **Qtà da spedire** viene copiato nel campo **Quantità da assemblare** nell'ordine di assemblaggio collegato quando si modifica la quantità da inviare. Ciò garantisce che la quantità spedita sia totalmente fornita dalla quantità per l'assemblaggio su ordine.  

 Tuttavia, negli scenari di combinazione, il valore completo del campo **Qtà da spedire** non viene copiato nel campo **Quantità da assemblare** nell'intestazione dell'ordine di assemblaggio. Viene invece inserito un valore di default nel campo **Quantità da assemblare** calcolato in base al campo **Qtà da spedire** secondo una regola predefinita che assicura che vengano spedite prima le quantità per l'assemblaggio su ordine.  

 Se si desidera deviare da questa impostazione di default, ad esempio perché si desidera assemblare solo una quantità maggiore o minore di quella specificata nel campo **Qtà da spedire**, è possibile modificare il campo **Quantità da assemblare**, ma esclusivamente in base a regole predefinite, come illustrato di seguito  

 Un esempio del motivo per cui è consigliabile modificare la quantità da assemblare è la possibilità di registrare parzialmente la spedizione di quantità di magazzino prima che possa essere spedito l'output di assemblaggio.  

 Di seguito sono illustrate le regole che definiscono i valori minimo e massimo che è possibile immettere manualmente in **Quantità da assemblare** per deviare dal valore di default in uno scenario di combinazione. La tabella viene visualizzata in uno scenario di combinazione in cui il campo **Qtà da spedire** nella riga ordine di vendita collegato viene modificato da 7 a 4 e nel campo **Quantità da assemblare** viene immesso di default il valore 4.  

||Riga ordine vendita|Testata ordine di assemblaggio|  
|-|----------------------|---------------------------|  
||**Quantità**|**Qtà da spedire**|**Qtà per assemblaggio su ordine**|**Quantità spedita**|**Quantità**|**Quantità da assemblare**|**Quantità assemblata**|**Quantità residua**|  
|Iniziale|10|7|7|0|7|7|0|7|  
|Cambia||4||||4 (immesso di default)|||  

 Sulla base della situazione precedente, è possibile modificare soltanto il campo **Quantità da assemblare** come segue:  

-   La quantità minima che è possibile immettere è 1. Ciò avviene in quanto è necessario assemblare almeno un'unità per poter vendere le quattro unità, presupponendo che le tre restanti siano disponibili in magazzino.  
-   La quantità massima che è possibile immettere è 4. Questo avviene per garantire che non sia assemblata una quantità di questo articolo di assemblaggio su ordine maggiore della quantità richiesta per la vendita.  

## <a name="see-also"></a>Vedi anche  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
