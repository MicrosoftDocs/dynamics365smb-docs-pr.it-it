---
title: Creare gli ordini di produzione dagli ordini di vendita
description: Puoi creare gli ordini di produzione dagli ordini vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115238"
---
# <a name="create-production-orders-from-sales-orders"></a>Creare gli ordini di produzione dagli ordini di vendita
È possibile creare ordini di produzione per gli articoli prodotti direttamente dagli ordini di vendita.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Per creare gli ordini di produzione dagli ordini di vendita  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.  
2.  Selezionare l'ordine di vendita per il quale creare un ordine di produzione.  
3.  Scegliere l'azione **Pianifica**. Nella pagina **Pianifica ordine vendita** è possibile visualizzare la disponibilità dell'articolo presente nell'ordine di vendita.  
4.  Selezionare l'azione **Crea ordine produzione**.  
5.  Selezionare lo stato e il tipo di ordine.  
6.  Scegli il pulsante **Sì** per creare uno o più ordini di produzione per le righe che hanno **Ordine prod.** nel loro campo **Sistema di rifornimento**.


> [!NOTE]  
> Le righe domanda nell'ordine di produzione creato che hanno **Ord. prod.** nel campo **Sistema di rifornimento** rappresentano gli ordini di produzione sottostanti. Dopo aver generato tali ordini di produzione, ricordarsi di identificare la domanda di componenti non soddisfatta utilizzando la pagina **Pianificazione ordini** o la funzione **Ripianifica** dagli ordini creati. 

## <a name="order-type"></a>Tipo ordine  
È possibile scegliere tra due modi per creare gli ordini di produzione come illustrato nella tabella seguente.

|Opzione|Descrizione|
|------|-----------|
|Ordine articolo|Viene creato un ordine di produzione per ogni ordine di produzione necessario che è rappresentato da una riga nella finestra **Pianifica ordine vendita**.|
|Ordine progetto|Viene creato un ordine di produzione per tutti gli ordini di produzione necessari che sono rappresentati dalle righe nella finestra **Pianifica ordine vendita**. |

Quando si utilizzano gli ordini di produzione, il campo **Tipo Origine** dell'ordine di produzione include le **Testate Vendita** e nell'ordine sono disponibili più righe, una per ogni articolo di riga di vendita da produrre.  


## <a name="see-also"></a>Vedere anche  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
