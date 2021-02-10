---
title: 'Procedura: Pianificare movimentazioni warehouse nei prospetti | Documenti Microsoft'
description: Pianificare i movimenti nel prospetto utilizzando la funzione di rifornimento collocazione o manualmente pianificando le righe che si desidera creare come istruzioni di movimento.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1ae0386c4fc2e3ac216d4228c94e7447a808cf50
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756119"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Pianificare movimentazioni warehouse nei prospetti
Pianificare i movimenti nel prospetto utilizzando la funzione di rifornimento collocazione o manualmente pianificando le righe che si desidera creare come istruzioni di movimento.  

## <a name="to-calculate-a-replenishment-movement"></a>Per calcolare un movimento di rifornimento  
Man mano che gli articoli nella warehouse vengono spediti ai clienti, le collocazioni con le valutazioni più elevate contengono un numero di articoli sempre minore. Per reintegrare le collocazioni di prelievo a valutazione elevata mediante gli articoli disponibili in altre collocazioni, è possibile eseguire la funzione **Calcola rifornimento collocazione** nella pagina **Prospetto movimentazioni**.

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto movimentazioni** e quindi scegliere il collegamento correlato.  
2.  Sceliere l'azione **Calcola rifornimento collocazione**.  

    [!INCLUDE[prod_short](includes/prod_short.md)] crea alcune righe con indicazioni precise in merito allo spostamento di articoli dalle collocazioni con valutazione inferiore alle collocazioni con valutazione più elevata.  

    > [!NOTE]  
    >  Una movimentazione viene suggerita in base al metodo FEFO quando si attiva la funzione **Crea movimento** se vengono soddisfatte le seguenti condizioni per un articolo:  
    >   
    >  -   L'articolo ha una data di scadenza.  
    > -   La casella di controllo **Prelievo in base a FEFO** della scheda ubicazione viene selezionata.  
    > -   Nella scheda Ubicazione viene selezionata la casella di controllo **Collocazione obbligatoria**.  
    > -   I campi **Dal codice zona** e **Dal codice collocazione** sono vuoti.  

    Per ulteriori informazioni, vedere [Prelievo in base al metodo FEFO](warehouse-picking-by-fefo.md).  

3.  Esaminare le righe e, se necessario, modificarle oppure eliminarne alcune nel caso in cui non sia possibile eseguire tutte le indicazioni riportate poiché richiedono troppo tempo.  
4.  Scegliere l'azione **Crea movimento** per creare un'istruzione warehouse destinata agli impiegati warehouse.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Per spostare l'intero contenuto di una o più collocazioni tramite la funzione Prendi contenuto collocazione  
Il prospetto movimentazioni consente anche di pianificare altri movimenti delle giacenze all'interno della warehouse. Ad esempio, quando si desidera posizionare gli articoli in una collocazione per il controllo qualità, è possibile pianificare questa azione utilizzando il prospetto movimenti, quindi creare un movimento per ottenere le istruzioni da fornire a un impiegato della warehouse.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto movimentazioni** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Ottieni contenuto collocazione**. La pagina di richiesta consente di applicare un filtro in modo da determinare le collocazioni e gli articoli da visualizzare nelle righe del prospetto movimenti.  
3.  Compilare i campi pertinenti nella pagina di richiesta del processo batch. Se, ad esempio, si desidera visualizzare il contenuto di tutte le collocazioni di una determinata zona dell'ubicazione, compilare il campo **Cod. zona**. Se si desidera recuperare le righe per ogni collocazione contenente un articolo specifico, compilare il campo **Nr. articolo**.  

    > [!NOTE]  
    >  Non è possibile spostare manualmente gli articoli all'interno o all'esterno di una collocazione di tipo Ricevi poiché gli articoli presenti in questo tipo di collocazione devono essere registrati come stoccati prima di essere inseriti nella giacenza disponibile.  

4.  Se si desidera recuperare un numero elevato di righe, scegliere **Ordina** per selezionare un metodo di ordinamento per le righe visualizzate nel prospetto, quindi scegliere **OK**.  

    > [!NOTE]  
    >  Le righe movimento vengono richiamate in base al metodo FEFO quando si attiva la funzione **Ottieni contenuto collocazione** se vengono soddisfatte le seguenti condizioni per un articolo:  
    >   
    >  -   L'articolo ha una data di scadenza.  
    > -   La casella di controllo **Prelievo in base a FEFO** della scheda ubicazione viene selezionata.  
    > -   Nella scheda Ubicazione viene selezionata la casella di controllo **Collocazione obbligatoria**.  
    > -   I campi **Dal codice zona** e **Dal codice collocazione** sono vuoti.  

5.  Completare alcune delle righe recuperate per riflettere le modifiche che si desidera apportare. Per ogni articolo da spostare, è necessario compilare i campi **Nr. articolo**, **Dal codice collocazione**, **A codice collocazione** e **Quantità**.  
6.  Eliminare le righe incomplete utilizzate a scopo informativo.  
7.  Quando le righe del prospetto movimenti rifletteranno accuratamente il modo in cui si desidera venga eseguita l'azione, scegliere l'azione **Crea movimento** per creare le istruzioni destinate all'impiegato della warehouse.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
