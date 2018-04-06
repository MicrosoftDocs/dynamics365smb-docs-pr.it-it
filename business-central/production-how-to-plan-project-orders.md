---
title: Come pianificare gli ordini di progetto | Microsoft Docs
description: "Questa attività di pianificazione viene avviata da un ordine di vendita e utilizza la finestra **Pianifica ordine vendita**. Al termine della creazione di un ordine di produzione progetto, è possibile eseguire un'ulteriore pianificazione mediante la finestra **Pianificazione ordini**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6102c71bac7338c959e61045962d5a3452a2a0f6
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="plan-project-orders"></a>Pianificare gli ordini di progetto
Questa attività di pianificazione viene avviata da un ordine di vendita e utilizza la finestra **Pianifica ordine vendita**. Al termine della creazione di un ordine di produzione progetto, è possibile eseguire un'ulteriore pianificazione mediante la finestra **Pianificazione ordini**.  

## <a name="to-create-a-project-production-order"></a>Per creare un ordine di produzione progetto  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini vendita**, quindi scegliere il collegamento correlato.  
2.  Selezionare l'ordine di vendita che rappresenta il progetto di produzione, quindi scegliere l'azione **Pianificazione**.  
4.  Nella finestra **Pianifica ordine vendita** scegliere l'azione **Crea ordine produzione**.  
5.  Nella finestra **Crea Ordine da Vendite** selezionare l'opzione **Ordine progetto** nel campo **Tipo ordine**.  
6.  Scegliere il pulsante **Sì**.  
7.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini di produzione**, quindi scegliere il collegamento correlato.
8. Aprire l'ordine di produzione appena creato.  

    Si noti che il campo **Tipo Origine** dell'ordine di produzione include le **Testate Vendita** e nell'ordine sono disponibili più righe, una per ogni articolo di riga di vendita da produrre.  
9. Scegliere l'azione **Pianifica**.
10. Nella finestra **Pianificazione ordini**, scegliere l'azione **Aggiorna** per calcolare la nuova domanda.  

La riga di testata ordine per l'ordine progetto verrà visualizzata e tutte le righe di domanda non soddisfatta verranno espanse sotto tale riga. Benché l'ordine di produzione includa righe per svariati articoli prodotti, la domanda totale per tutte le righe di ordine di produzione viene elencata sotto una riga di testata ordine nella finestra **Pianificazione ordini** e viene visualizzata la ragione sociale originale del cliente. È ora possibile passare alla pianificazione della domanda, come illustrato in [Pianificare una nuova domanda ordine per ordine](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Le righe domanda nell'ordine di produzione progetto che hanno **Ord. prod.** nel campo **Sistema di rifornimento** rappresentano gli ordini di produzione sottostanti. Dopo aver generato tali ordini di produzione, occorre ricalcolare il piano nella finestra **Pianificazione ordini** per identificare la domanda di componenti non soddisfatta. In questo caso, vengono visualizzati come righe domanda in una normale riga di testata dell'ordine di produzione, cioè la relazione di progetto non è più visibile nella finestra. Tuttavia, se si utilizza la funzionalità Tracciabilità ordine, è possibile esaminare tutti gli ordini di approvvigionamento creati nell'ordine di vendita originale.  

## <a name="see-also"></a>Vedi anche
[Pianif.](production-planning.md)   
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

