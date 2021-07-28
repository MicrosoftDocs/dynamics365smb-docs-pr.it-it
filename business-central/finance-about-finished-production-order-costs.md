---
title: Informazioni sui costi di un ordine di produzione chiuso
description: La conclusione dell'ordine di produzione è fondamentale per completare il ciclo di vita dei costi di un articolo di produzione. I costi finali vengono calcolati nel processo batch Rettifica costo - Movimenti articoli.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9168ea7644390446f4e7a2cd8950d483d43e1013
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "6324049"
---
# <a name="about-finished-production-order-costs"></a>Informazioni sui costi di un ordine di produzione chiuso
La chiusura di un ordine di produzione è un'attività importante nel completamento del ciclo di vita del costing dell'articolo prodotto. I costi finali, inclusi gli scostamenti in un ambiente con costi standard, i valori effettivi in un ambiente con costi FIFO, medi o LIFO, vengono calcolati tramite il processo batch **Rettifica costo - Movimenti articoli** che consente la riconciliazione finanziaria dei costi di produzione degli articoli. Affinché un ordine di produzione venga considerato per la rettifica del costo, lo stato deve essere impostato come **Completato**. È pertanto essenziale che, al completamento, lo stato di un ordine di produzione venga modificato in **Completato**.  

## <a name="example"></a>Esempio  
 In un ambiente di costi standard, quando si consuma materiale per produrre un articolo, detto semplicemente, il costo dell'articolo più i costi generali e di manodopera confluiscono nel WIP. Quando l'articolo viene prodotto, il WIP viene ridotto dell'importo del costo standard dell'articolo. In genere, questi costi netti non sono uguali a zero. Perché l'importo sia uguale a zero, è necessario eseguire il processo batch **Rettifica costo - Movimenti articoli**, notando che solo gli ordini di produzione con stato **Completato** verranno considerati per la rettifica.  

## <a name="see-also"></a>Vedi anche  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]