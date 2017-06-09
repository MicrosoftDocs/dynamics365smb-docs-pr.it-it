---
title: Magazzino | Documenti Microsoft
description: Viene descritto come gestire gli articoli fisici.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Magazzino
Per ogni prodotto fisico trattato è necessario creare una scheda articolo di tipo **Magazzino**. Gli articoli che si offrono ai clienti ma che non sono presenti in magazzino possono essere registrati come articoli non in stock che possono essere convertiti in articoli di magazzino se necessario. È possibile aumentare o diminuire la quantità di un articolo in magazzino registrando direttamente nei movimenti contabili articoli, ad esempio, dopo un conteggio fisico oppure se non si registrano gli acquisti.

Gli incrementi in magazzino e le diminuzioni vengono registrati automaticamente anche quando si registrano gli acquisti e i documenti di vendita rispettivamente. Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md), [Procedura: Vendere prodotti](sales-how-sell-products.md)e [Procedura: Fatturare le vendite](sales-how-invoice-sales.md). I trasferimenti tra le ubicazioni cambiano le quantità in giacenza nelle warehouse della società.   

Per incrementare la panoramica degli articoli e agevolare le operazioni di ricerca, è possibile classificare gli articoli e assegnare gli attributi per cercarli e ordinarli.

È necessario assicurarsi che i costi degli articoli vengano trasmessi alla transazione di vendita in uscita, in particolare nei casi in cui si vendano merci prima di fatturare l'acquisto degli articoli. Questa operazione è nota come rettifica del costo ed è è possibile eseguirla manualmente o importare una verifica automatica quando si registra una transazione dell'articolo.

Le modifiche apportate al valore di magazzino delle transazioni vengono automaticamente riconciliate con i registri finanziari quando si registrano transazioni dell'articolo.

|Per |Vedere |
|---|----|
|Creare le schede articolo per gli articoli di magazzino trattati.|[Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md)|
|Strutturare gli articoli padre da vendere come kit costituiti da componenti del padre o da assemblare su ordine o per magazzino.|[Procedura: Utilizzare le distinte base](inventory-how-work-BOMs.md)|
|Gestire una panoramica degli articoli e facilitare le operazioni di ricerca e ordinamento degli articoli organizzandoli in categorie.|[Procedura: Classificare gli articoli](inventory-how-categorize-items.md)|
|Assegnare gli attributi dell'articolo dei diversi tipi di valore agli articoli per migliorare l'ordinamento e la ricerca degli articoli.|[Procedura: Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)|
|Creare speciali schede articolo per gli articoli da offrire ai clienti per cui non viene gestito il magazzino.|[Procedura: Utilizzare gli articoli non in stock](inventory-how-work-nonstock-items.md)|
|Aumentare o diminuire la quantità di magazzino di un articolo, ad esempio dopo un conteggio fisico o come un modo semplice per registrare i carichi di acquisto.|[Procedura: Rettificare il magazzino](inventory-how-adjust-inventory.md)|
|Visualizzare la disponibilità di articoli per ubicazione, periodo, evento di vendita o acquisto o in base all'utilizzo nei DB assemblaggi.|[Procedura: Ottenere una panoramica della disponibilità](inventory-how-availability-overview.md)|
|Trasferire gli articoli in magazzino tra le ubicazioni con ordini di trasferimento, per gestire le attività di warehouse oppure con le registrazioni di riclassificazione articoli.|[Procedura: Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)|
|Rivalutare o ammortizzare il valore di uno o più articoli in magazzino registrandone il corrente valore calcolato.|[Procedura: Rivalutare il magazzino](inventory-how-revalue-inventory.md)|
|Rettificare i costi articolo, automaticamente o manualmente, per inoltrare le modifiche dei costi dai movimenti in entrata ai movimenti in uscita correlati.|[Procedura: Rettificare i costi degli articoli](inventory-how-adjust-item-costs.md)|
|Ottenere informazioni sul modo in cui le modifiche apportate al valore di magazzino delle transazioni vengono automaticamente riconciliate con i registri finanziari.|[Avanzate: Magazzino - Riconciliazione](advanced-inventory-reconciliation.md).|

## <a name="see-also"></a>Vedi anche  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)    
[Catena di approvvigionamento](madeira-supply-chain.md)  
[Utilizzo di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
