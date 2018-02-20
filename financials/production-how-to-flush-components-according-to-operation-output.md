---
title: Come eseguire la consuntivazione dei componenti in base all'output dell'operazione | Microsoft Docs
description: Per gli articoli impostati con il metodo di consuntivazione a ritroso, il comportamento di default prevede di calcolare e registrare il consumo di componenti quando si modifica lo stato di un ordine di produzione rilasciato in **Completato**. Per ulteriori informazioni, vedere Metodo consuntivazione.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f61e3150f1978795a20d4ad68656d6d1e72402a0
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="flush-components-according-to-operation-output"></a>Eseguire la consuntivazione dei componenti in base all'output dell'operazione
Per gli articoli impostati con il metodo di consuntivazione a ritroso, il comportamento di default prevede di calcolare e registrare il consumo di componenti quando si modifica lo stato di un ordine di produzione rilasciato in **Completato**.  

Se inoltre si definiscono i codici legame tra ciclo e distinta base, il calcolo e la registrazione si verificano una volta completata ogni operazione e la quantità effettivamente consumata nell'operazione viene registrata. Per ulteriori informazioni, vedere [Creare cicli](production-how-to-create-routings.md).  

Ad esempio, se un ordine di produzione per produrre 800 metri richiede 8 chilogrammi di un componente, quando si registrano 200 metri come output, 2 chilogrammi vengono automaticamente registrati come consumo.  

Questa funzionalità si rivela particolarmente utile per i seguenti motivi:  

-   **Valutazione di magazzino** - i movimenti di valorizzazione per output e consumo vengono creati in parallelo con lo stato di avanzamento dell'ordine di produzione. Senza codice legame tra ciclo e distinta base, il valore di magazzino aumenterà man mano che l'output viene registrato e diminuirà in un momento successivo quando il valore di consumo di componenti viene registrato insieme all'ordine di produzione chiuso.  
-   **Disponibilità di magazzino** - con la registrazione graduale del consumo, la disponibilità degli articoli componenti è più aggiornata, il che è importante per mantenere l'equilibrio interno tra offerta e domanda. Senza codice legame tra ciclo e distinta base, altre domande del componente potrebbero ritenere che sia disponibile finché è in sospeso una registrazione di consumo in ritardo.  
-   **JIT (just-in-time)** – grazie alla possibilità di personalizzare i prodotti alle richieste del cliente, è possibile ridurre lo spreco assicurandosi che le modifiche di sistema e di lavoro si verifichino solo quando è necessario.  

La procedura che segue mostra come combinare la consuntivazione a ritroso e i codici di legame tra ciclo e distinta base in modo che la quantità di cui è stata effettuata la consuntivazione per operazione sia proporzionale all'effettivo output dell'operazione completata.  

## <a name="to-flush-components-according-to-operation-output"></a>Per eseguire la consuntivazione dei componenti in base all'output dell'operazione  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Modifica**.  
3.  Nella Scheda dettaglio **Rifornimento**, nel campo **Metodo consuntivazione**, selezionare **Avanti**.  

    > [!NOTE]  
    >  Selezionare **Prelievo+ Avanti** se il componente è utilizzato in un'ubicazione impostata per l'utilizzo di stoccaggi e prelievi guidati.  

4.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cicli**, quindi scegliere il collegamento correlato.  
5.  Definire codici di legame tra ciclo e distinta base per ogni operazione che consuma il componente. Per ulteriori informazioni, vedere [Creare cicli](production-how-to-create-routings.md).  
6.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **DB produzione**, quindi scegliere il collegamento correlato.  
7.  Definire codici di legame tra ciclo e distinta base da ogni istanza del componente all'operazione in cui viene consumato.

    > [!IMPORTANT]  
    >  Il componente deve avere un collegamento ciclo all'ultima operazione del ciclo.  

## <a name="see-also"></a>Vedi anche  
[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Pianif.](production-planning.md)   
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

