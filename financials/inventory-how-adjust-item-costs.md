---
title: 'Procedura: Modificare manualmente i costi degli articoli | Documenti Microsoft'
description: 'Procedura: Rettificare i costi degli articoli'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 00b5ac40bd0d3df346618b57173df67daba6c7fc
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Procedura: Rettificare i costi degli articoli manualmente
Il costo di un articolo (valore di magazzino) che si acquista e in seguito si vende può variare nel tempo, ad esempio perché un costo di spedizione viene aggiunto al costo di acquisto dopo che è stato venduto l'articolo. La rettifica dei costi è un'operazione particolarmente importante nel caso in cui si vendano merci prima di fatturare il relativo acquisto. Per conoscere sempre il valore di magazzino corretto, i costi degli articoli devono quindi essere regolarmente rettificati. In questo modo si garantisce che le statistiche relative ai margini siano aggiornate e che gli indicatore KPI finanziari siano corretti.

In [!INCLUDE[d365fin](includes/d365fin_md.md)]i costi degli articoli vengono rettificati automaticamente ogni volta che avviene una transazione di magazzino , ad esempio quando si registra una fattura di acquisto per un articolo.

È inoltre possibile utilizzare una funzione che consente di rettificare manualmente i costi di uno o più articoli. Ciò risulta utile, ad esempio, quando si è certi che i costi degli articoli vengono modificati per motivi diversi dalle transazioni dell'articolo.

**Nota**: i costi degli articoli vengono rettificati solo tramite il metodo di costing FIFO. Questo significa che il costo unitario di un articolo è il valore effettivo di tutto il carico dell'articolo e che il magazzino viene calcolato in base al presupposto secondo cui i primi articoli inseriti in magazzino sono i primi a essere venduti.

Tramite i processi della funzione di rettifica dei costi vengono elaborati solo i movimenti di valorizzazione che non sono ancora stati rettificati. Se si verifica una situazione in cui è necessario trasferire costi in entrata modificati ai movimenti in uscita associati, vengono creati nuovi movimenti di valorizzazione di rettifica, basati sulle informazioni dei movimenti di valorizzazione originali, ma che contengono l'importo di rettifica. La funzione di rettifica dei costi viene utilizzata la data di registrazione del movimento di valorizzazione originale, a meno che tale data non sia inclusa in un periodo di magazzino chiuso. In tal caso, viene utilizzata la data di inizio del successivo periodo di magazzino aperto. Se non si utilizzano i periodi di magazzino, la data nel campo **Consenti registraz. da** nella finestra **Setup contabilità generale** verrà definita quando la rettifica viene registrata.

Le modifiche apportate al valore di magazzino delle transazioni vengono automaticamente riconciliate con i registri finanziari quando si registrano transazioni dell'articolo. Per ulteriori informazioni, vedere [Avanzate: Magazzino - Riconciliazione](advanced-inventory-reconciliation.md).

## <a name="to-adjust-item-costs-manually"></a>Per rettificare i costi degli articoli manualmente
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Rettifica costo - Movimenti articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Rettifica costo - Movimenti articoli** specificare per quali articoli rettificare i costi.
3. Scegliere il pulsante **OK**.

## <a name="see-also"></a>Vedi anche
[Avanzate: Magazzino - Riconciliazione](advanced-inventory-reconciliation.md)  
[Magazzino](inventory-manage-inventory.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

