---
title: Come vendere gli articoli di magazzino nei flussi assemblaggio su ordine | Microsoft Docs
description: Se l'articolo è impostato per la scheda di assemblaggio su ordine, il processo di default dell'ordine di vendita presuppone che l'articolo non sia in magazzino e debba essere assemblato per tale ordine di vendita specifico. Di conseguenza, un ordine di assemblaggio collegato viene automaticamente creato quando si aggiunge l'articolo a una riga dell'ordine di vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53118269f151ec0768f80151613afbbf36d8d075
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880810"
---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>Vendere gli articoli di magazzino nei flussi da assemblare su ordine
Se il campo **Criteri di assemblaggio** nella scheda articolo di un articolo di assemblaggio contiene **Assemblaggio su ordine**, il processo di default dell'ordine di vendita presuppone che l'articolo non sia in magazzino e debba essere assemblato per tale ordine di vendita specifico. Di conseguenza, un ordine di assemblaggio collegato viene automaticamente creato quando si aggiunge l'articolo a una riga dell'ordine di vendita. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md). Tuttavia, se una parte della quantità dell'ordine di vendita è già disponibile in magazzino, interamente, è possibile ridurre la quantità dell'ordine di assemblaggio modificando il campo **Qtà per assemblaggio su ordine** nella riga dell'ordine di vendita.  

Questo è uno scenario raro poiché si prevede che gli articoli di assemblaggio su ordine siano sempre personalizzati ed è poco probabile che si trovino in magazzino nella configurazione richiesta da un altro cliente. Tuttavia, se una società dispone di quantità di assemblaggio su ordine in magazzino a causa di resi o annullamenti di ordini, queste quantità devono essere prelevate e vendute prima di assemblarne di nuove.  

> [!NOTE]  
>  Non sono disponibili funzionalità negli ordini di vendita che avvisino o assistano automaticamente l'utente nell'individuazione delle quantità di un ordine di assemblaggio già disponibili. In alternativa, è necessario monitorare le informazioni sulla disponibilità, ad esempio nel Dettaglio informazioni **Dettagli righe vendite**.  

Una funzionalità analoga è disponibile quando si vendono articoli di assemblaggio dal magazzino e la quantità non è disponibile, interamente o in parte, e può essere fornita da un ordine di assemblaggio. Per altre informazioni, vedere [Vendere insieme articoli assemblaggio su ordine e articoli in magazzino](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Alcune regole si applicano al campo **Qtà da spedire** nelle righe dell'ordine di vendita che contengono una combinazione di quantità per l'assemblaggio su ordine e quantità di magazzino. Per altre informazioni, vedere la sezione "Scenari di combinazione" in [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).  

Nella procedura, le quantità di assemblaggio su ordine vengono sostituite con le quantità di magazzino in una riga dell'ordine di vendita. I passaggi includono la verifica della disponibilità, la detrazione della quantità dall'ordine di assemblaggio collegato e l'impegno della quantità di magazzino per garantire che venga prelevata e spedita per l'ordine.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Per vendere gli articoli di magazzino nei flussi da assemblare su ordine  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.  
2.  Creare un ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).  
3.  In una riga dell'ordine di vendita per un articolo assemblato su ordine immettere la quantità richiesta nel campo **Quantità**.  
4.  Nel Dettaglio informazioni **Dettagli righe vendite** determinare se tutta o parte della quantità richiesta è disponibile.  
5.  Nel campo **Qtà per assemblaggio su ordine** dedurre la quantità disponibile in modo che solo la quantità non disponibile venga assemblata su ordine. Il campo **Quantità impegnata** viene diminuito di conseguenza per indicare che il collegamento da ordine a ordine, o impegno, si applica solo alla quantità da assemblare.  
6.  Nella Scheda dettaglio **Righe** scegliere **Funzioni** e quindi scegliere l'azione **Impegna**.  
7.  Nella pagina **Impegni** selezionare la riga o le righe del movimento contabile articolo che contengono le quantità disponibili, scegliere l'azione **Impegna da riga corrente**, quindi fare clic su **OK**.  

    Nella pagina **Quantità impegnata** della finestra **Ordine vendita** verrà indicato che l'intera quantità della riga dell'ordine è impegnata. Il campo **Qtà per assemblaggio su ordine** riflette ancora la sottoquantità che deve essere assemblata.  

8.  Rilasciare l'ordine di vendita per il prelievo degli articoli di magazzino e per l'assemblaggio degli articoli non disponibili. Per ulteriori informazioni, vedere [Assemblare articoli](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Il campo **Codice collocazione** nell'ordine di vendita può essere precompilato in base al campo **Cod. coll. sp. ass. su ordine** o il campo **Cod. coll. art. da assembl.** nella scheda ubicazione. In tal caso, il campo **Codice collocazione** nella riga dell'ordine di vendita può essere errato in questa combinazione di quantità di assemblaggio su ordine e assemblaggio per magazzino. Si consiglia di esaminare il campo **Cod. collocazione** e verificare che il posizionamento funzioni per tutte le quantità. In alternativa, immettere due quantità diverse in righe separate dell'ordine di vendita.  

## <a name="see-also"></a>Vedi anche  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
