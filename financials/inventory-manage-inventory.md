---
title: Gestione dei costi del magazzino | Documenti Microsoft
description: Descrive come gestire i prodotti fisici che si vendono, ad esempio, la gestione dello stock nella warehouse.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 1aa1a7c2ec56c3f123bde67a9870be4efd99bdb5
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---

# <a name="inventory"></a>Magazzino
Per ogni prodotto fisico trattato è necessario creare una scheda articolo di tipo **Magazzino**. Gli articoli che si offrono ai clienti ma che non sono presenti in magazzino possono essere registrati come articoli non in stock che possono essere convertiti in articoli di magazzino se necessario. È possibile aumentare o diminuire la quantità di un articolo in magazzino registrando direttamente nei movimenti contabili articoli, ad esempio, dopo un conteggio fisico oppure se non si registrano gli acquisti.

Gli incrementi in magazzino e le diminuzioni vengono registrati automaticamente anche quando si registrano gli acquisti e i documenti di vendita rispettivamente. Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md), [Procedura: Vendere prodotti](sales-how-sell-products.md)e [Procedura: Fatturare le vendite](sales-how-invoice-sales.md). I trasferimenti tra le ubicazioni cambiano le quantità in giacenza nelle warehouse della società.   

Per incrementare la panoramica degli articoli e agevolare le operazioni di ricerca, è possibile classificare gli articoli e assegnare gli attributi per cercarli e ordinarli.

> [!NOTE]
> La gestione fisica degli articoli è detta attività di warehouse. Per ulteriori informazioni, vedere [Gestione warehouse](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Magazzino - Riconciliazione
Quando si registrano transazioni di magazzino, ad esempio spedizioni, fatture di vendite o rettifiche di magazzino, le modifiche ai costi degli articoli vengono registrate automaticamente nei movimenti di valorizzazione. Per riflettere la modifica del valore di magazzino nei registri finanziari, i costi di magazzino vengono registrati automaticamente nei conti giacenza magazzino correlati in contabilità generale. Per ogni transazione di magazzino registrata, verranno registrati i valori appropriati nel conto giacenza magazzino, nel conto di rettifica e nel conto COGS nella contabilità generale. Per ulteriori informazioni, vedere [Procedura: Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Anche se i costi vengono registrati automaticamente in contabilità generale, è comunque necessario assicurarsi che i costi delle merci vengano trasferiti alle transazioni in uscita correlate, in particolare nel caso in cui si vendano merci prima di fatturare il relativo acquisto. Questa operazione è detta rettifica dei costi. I costi dell'articolo vengono rettificati automaticamente quando si registrano le transazioni articolo, ma è possibile anche rettificarli manualmente. Per ulteriori informazioni, vedere [Procedura: Rettificare i costi articoli.](inventory-how-adjust-item-costs.md).

|Per |Vedere |
|---|----|
|Creare le schede articolo per gli articoli di magazzino trattati.|[Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md)|
|Strutturare gli articoli padre da vendere come kit costituiti da componenti del padre o da assemblare su ordine o per magazzino.|[Procedura: Utilizzare le distinte base](inventory-how-work-BOMs.md)|
|Gestire una panoramica degli articoli e facilitare le operazioni di ricerca e ordinamento degli articoli organizzandoli in categorie.|[Procedura: Classificare gli articoli](inventory-how-categorize-items.md)|
|Assegnare gli attributi dell'articolo dei diversi tipi di valore agli articoli per migliorare l'ordinamento e la ricerca degli articoli.|[Procedura: Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)|
|Creare speciali schede articolo per gli articoli da offrire ai clienti per cui non viene gestito il magazzino.|[Procedura: Utilizzare gli articoli non in stock](inventory-how-work-nonstock-items.md)|
|Eseguire attività di conteggio fisico, rettifiche positive o negative e modificare le informazioni, quali ubicazione o numero di lotto, nei movimenti contabili articoli.|[Procedura: Conteggio, rettifica e riclassificazione dell'inventario](inventory-how-count-adjust-reclassify.md)|
|Visualizzare la disponibilità di articoli per ubicazione, periodo, evento di vendita o acquisto o in base all'utilizzo nei DB assemblaggi o produzione.|[Procedura: Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)|
|Trasferire gli articoli in magazzino tra le ubicazioni con ordini di trasferimento, per gestire le attività di warehouse oppure con le registrazioni di riclassificazione articoli.|[Procedura: Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)|
|Impegnare gli articoli in entrata o di magazzino per ordini di vendita, ordini di acquisto, ordini di assistenza, ordini di assemblaggio o ordini di produzione.|[Procedura: Impegnare articoli](inventory-how-to-reserve-items.md)|
|Assegnare i numeri seriali o i numeri di lotto a qualsiasi riga di registrazione del documento in uscita o in entrata, ad esempio per tenere traccia degli articoli in caso di richiamate.|[Procedura: Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md)|
|È possibile trovare dove un numero seriale o di lotto è stato utilizzato nella sua catena di approvvigionamento, ad esempio in caso di richiamate.|[Procedura: Analizzare articoli tracciati](inventory-how-to-trace-item-tracked-items.md)|
|È possibile gestire le operazioni aziendali in uffici vendite, reparti acquisti o uffici di programmazione impianti distribuiti tra più sedi.|[Procedura: Utilizzare i centri di responsabilità](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)    
[Utilizzo di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

