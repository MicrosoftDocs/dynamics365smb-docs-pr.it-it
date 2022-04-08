---
title: Aggiornare i costi standard
description: Periodicamente è necessario aggiornare i costi standard dei componenti ed eseguire il rollup dei nuovi costi nell'articolo padre.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4bada4ee28df77cc9700d5957ef8fb8b1a64535b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517448"
---
# <a name="update-standard-costs"></a>Aggiornare i costi standard
Periodicamente è necessario aggiornare i costi standard dei componenti ed eseguire il rollup dei nuovi costi nell'articolo padre. Il processo in genere è costituito dai quattro passaggi seguenti:  

1.  Aggiornare i costi ai livelli di capacità e componente. Per ulteriori informazioni, vedere il processo batch **Suggerisci costo std. articolo**.  
2.  Consolidamento e roll up dei costi dei componenti e della capacità per calcolare il costo totale di produzione o di assemblaggio degli articoli.  
3.  Implementare i costi standard che vengono registrati quando si eseguono i processi batch precedenti. I costi standard non saranno effettivi finché non verranno implementati. Usa il processo batch **Implementa modifiche costo std.** che consente di aggiornare il costo standard degli elementi riportati nella tabella Prospetto costo standard.  
4.  Implementare le modifiche per aggiornare il campo **Costo unitario** nella scheda articolo ed eseguire la rivalutazione di magazzino. Per ulteriori informazioni, vedere [Rivalutare il magazzino](inventory-how-revalue-inventory.md).  

Per ulteriori informazioni, vedere [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md).
  
## <a name="to-update-standard-costs"></a>Per aggiornare i costi standard

1.  Eseguire il processo batch **Rettifica costo - Movimenti articoli**.  
2.  Eseguire il processo batch **Registra costo magazzino in C/G**.  
3.  Aprire il **Prospetto costo standard** e utilizzare una o più delle funzioni seguenti:  

    1.  Eseguire il processo batch **Suggerisci costo std. articolo**.  
    2.  Analizzare i risultati e apportare le modifiche necessarie.  
    3.  Eseguire il processo batch **Suggerisci costo standard capacità**.  
    4.  Analizzare i risultati e apportare le modifiche necessarie.
    5. Eseguire il processo batch **Roll up del costo standard**.
    6.  Analizzare i risultati e apportare le modifiche necessarie.
    7.  Eseguire il processo batch **Implementa modifiche costo std.**  
4.  Analizzare e contabilizzare la pagina **Registrazioni rivalutazioni**, in cui sono stati inseriti i dati ricavati tramite i passaggi precedenti del processo.  

## <a name="see-also"></a>Vedi anche

 [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md)   
 [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)   
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md) [Contabilità](finance.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]