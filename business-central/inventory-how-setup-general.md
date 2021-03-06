---
title: Definire le impostazioni generali di magazzino
description: Viene descritto come definire le impostazioni generali del magazzino in modo da poter gestire il magazzino e le scorte.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1430123f433cfc101e0ae94ce0598d9c0cdd58b2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785825"
---
# <a name="set-up-general-inventory-information"></a>Impostare le informazioni generali di magazzino

Le impostazioni generali di magazzino vengono impostate nella pagina **Setup magazzino**.

## <a name="to-set-up-general-inventory-information"></a>Per impostare le informazioni generali di magazzino

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup magazzino** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup magazzino** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Per informazioni dettagliate sui campi di determinazione dei costi, **Reg. automatica costi**, **Reg. costi previsti in C/G** e **Metodo di costing di default**, vedere [Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md) e [Dettagli di progettazione: Registrazione del costo previsto](design-details-expected-cost-posting.md). Per ulteriori informazioni sui costi in generale, vedere [Gestione dei costi di magazzino](finance-manage-inventory-costs.md).  

Se si desidera includere il tempo di gestione della warehouse nel calcolo della promessa d'ordine nella riga di acquisto, è possibile impostarlo come valore di default nella pagina **Setup magazzino** per il magazzino e per l'ubicazione. Per ulteriori informazioni, vedere [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> L'interruttore **Rettifica costo automatica** è attivato per impostazione predefinita per garantire che i valori di magazzino siano sempre corretti nella contabilità generale, che a sua volta mantiene aggiornate le statistiche sulle vendite e sui profitti. Le modifiche ai costi vengono assegnate dai movimenti in entrata, ad esempio movimenti per acquisti o output di produzione, ai movimenti in uscita correlati, ad esempio vendite o trasferimenti. Questo è utile per i nuovi clienti [!INCLUDE[prod_short](includes/prod_short.md)] e le piccole imprese con livelli di transazioni di magazzino relativamente bassi. Tuttavia, man mano che un'azienda cresce e i livelli di magazzino aumentano, ciò può rallentare le prestazioni del sistema. Per ridurre al minimo le prestazioni durante la registrazione, selezionare un'opzione di tempo per definire quanto indietro nel tempo dalla data di lavoro può verificarsi una transazione in entrata per attivare potenzialmente la rettifica dei movimenti di valore in uscita correlati. In alternativa, è possibile rettificare manualmente i costi a intervalli regolari con il processo batch Rettifica costo - Movimenti articoli.

## <a name="see-also"></a>Vedere anche
[Setup magazzino](inventory-setup-inventory.md)  
[Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)    
[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]