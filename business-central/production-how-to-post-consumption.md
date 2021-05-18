---
title: Registrare il consumo tramite processo batch
description: Se il metodo di consuntivazione è Manuale, i componenti devono essere registrati manualmente nelle registrazioni consumi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b3ee6ca54e21605b4e9cf340b04656694c9801e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935188"
---
# <a name="batch-post-production-consumption"></a>Registrare il consumo produzione tramite processo batch

Se il metodo di consuntivazione è **Manuale**, i componenti devono essere registrati manualmente nelle registrazioni consumi.  

>[!NOTE]
> Se è stato immesso un segno di spunta nel campo **Richiesto prelievo** della scheda Ubicazione per indicare che l'ubicazione richiede l'elaborazione dei prelievi di magazzino, non sarà necessario utilizzare questo processo batch. [!INCLUDE[prod_short](includes/prod_short.md)] gestirà il consumo quando si registra il prelievo di magazzino. Per ulteriori informazioni, vedere [Prelevare per la produzione in configurazioni della warehouse di base](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).  

È inoltre possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] sulla registrazione (*consuntivazione*) automatica dei componenti quando si avviano o si chiudono ordini di produzione. Per ulteriori informazioni vedere [Attivare la consuntivazione dei componenti in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Per registrare il consumo per una o più righe dell'ordine di produzione

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni consumi** e quindi scegliere il collegamento correlato.  
2. Compilare i campi inserendo i dati relativi agli ordini di produzione e al consumo. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Uso dell'azione **Calcolo basato su** per generare le righe di registrazione dagli ordini di produzione in base all'output attuale (la quantità di merci finite prodotte effettivamente) o sull'output previsto (la quantità di merci finite che ti aspetti di produrre).

    > [!NOTE]
    > Se è stata configurata la scheda Ubicazione per richiedere l'elaborazione del prelievo in magazzino, puoi immettere nel campo solo le quantità già prelevate tramite un'attività di magazzino nel campo **Quantità** nella pagina **Registrazioni consumi**, non qualsiasi quantità calcolata. Per ulteriori informazioni, vedi [Prelevare per produzione o assemblaggio in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

3. Per registrare il consumo scegliere l'azione **Registra**. Si riducono le relative scorte.

## <a name="see-also"></a>Vedere anche

[Manufacturing](production-manage-manufacturing.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
