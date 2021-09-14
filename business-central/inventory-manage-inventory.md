---
title: Gestione dei costi del magazzino
description: Questo argomento descrive come gestire i prodotti fisici trattati creando una scheda articolo Inventario.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 022d48ad3069729736794976301db7fe2c6a6b47
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482274"
---
# <a name="how-to-manage-inventory"></a>Come gestire l'inventario
Per ogni prodotto fisico trattato è necessario creare una scheda articolo di tipo **Magazzino**. Gli articoli che si offrono ai clienti ma che non sono presenti in magazzino possono essere registrati come articoli di catalogo che possono essere convertiti in articoli di magazzino se necessario. È possibile aumentare o diminuire la quantità di un articolo in magazzino registrando direttamente nei movimenti contabili articoli, ad esempio, dopo un conteggio fisico oppure se non si registrano gli acquisti.

Gli incrementi in magazzino e le diminuzioni vengono registrati automaticamente anche quando si registrano gli acquisti e i documenti di vendita rispettivamente. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md), [Procedura: Vendere prodotti](sales-how-sell-products.md)e [Fatturare le vendite](sales-how-invoice-sales.md). I trasferimenti tra le ubicazioni cambiano le quantità in giacenza nelle warehouse della società.   

Per incrementare la panoramica degli articoli e agevolare le operazioni di ricerca, è possibile classificare gli articoli e assegnare gli attributi per cercarli e ordinarli.

> [!NOTE]
> La gestione fisica degli articoli è detta attività di warehouse. Per ulteriori informazioni, vedere [Gestione warehouse](warehouse-manage-warehouse.md).

La pianificazione degli articoli per soddisfare la domanda è coperta nella funzionalità di pianificazione dell'offerta. Per ulteriori informazioni, vedere [Pianificazione](production-planning.md).  

## <a name="inventory-reconciliation"></a>Magazzino - Riconciliazione
Quando si registrano transazioni di magazzino, ad esempio spedizioni, fatture di vendite o rettifiche di magazzino, le modifiche ai costi degli articoli vengono registrate automaticamente nei movimenti di valorizzazione. Per riflettere la modifica del valore di magazzino nei registri finanziari, i costi di magazzino vengono registrati automaticamente nei conti giacenza magazzino correlati in contabilità generale. Per ogni transazione di magazzino registrata, verranno registrati i valori appropriati nel conto giacenza magazzino, nel conto di rettifica e nel conto COGS nella contabilità generale. Per ulteriori informazioni, vedere [Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Anche se i costi vengono registrati automaticamente in contabilità generale, è comunque necessario assicurarsi che i costi delle merci vengano trasferiti alle transazioni in uscita correlate, in particolare nel caso in cui si vendano merci prima di fatturare il relativo acquisto. Questa operazione è detta rettifica dei costi. I costi dell'articolo vengono rettificati automaticamente quando si registrano le transazioni articolo, ma è possibile anche rettificarli manualmente. Per ulteriori informazioni, vedere [Rettificare i costi articoli](inventory-how-adjust-item-costs.md).  

## <a name="related-tasks"></a>Attività correlate

La tabella seguente descrive le attività correlate.

|A |Vedere |
|---|----|
|Creare le schede articolo per gli articoli di magazzino trattati.|[Registrare nuovi articoli](inventory-how-register-new-items.md)|
|Strutturare gli articoli padre da vendere come kit costituiti da componenti del padre o da assemblare su ordine o per magazzino.|[Utilizzare le distinte base](inventory-how-work-BOMs.md)|
|Gestire una panoramica degli articoli e facilitare le operazioni di ricerca e ordinamento degli articoli organizzandoli in categorie.|[Classificare gli articoli](inventory-how-categorize-items.md)|
|Assegnare gli attributi dell'articolo dei diversi tipi di valore agli articoli per migliorare l'ordinamento e la ricerca degli articoli.|[Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)|
|Creare speciali schede articolo per gli articoli da offrire ai clienti per cui non viene gestito il magazzino.|[Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md)|
|Eseguire il conteggio fisico del magazzino con le pagine **Ordine magazzino fisico** e **Registrazione magazzino fisico**.|[Conteggiare l'inventario utilizzando documenti](inventory-how-count-inventory-with-documents.md)|
|Eseguire attività di conteggio fisico, rettifiche positive o negative e modificare le informazioni, quali ubicazione o numero di lotto, nei movimenti contabili articoli.|[Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md)|
|Visualizzare la disponibilità di articoli per ubicazione, periodo, evento di vendita o acquisto o in base all'utilizzo nei DB assemblaggi o produzione.|[Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)|
|Trasferire gli articoli in magazzino tra le ubicazioni con ordini di trasferimento, per gestire le attività di warehouse oppure con le registrazioni di riclassificazione articoli.|[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)|
|Impegnare gli articoli in entrata o di magazzino per ordini di vendita, ordini di acquisto, ordini di assistenza, ordini di assemblaggio o ordini di produzione.|[Prenotare articoli](inventory-how-to-reserve-items.md)|
|Imposta la tracciabilità degli articoli in modo da poter tenere traccia dei numeri di serie degli articoli, ad esempio per monitorare gli articoli in caso di richiami.|[Configurare la tracciabilità di articoli con numeri di serie, di lotto e di pacco](inventory-how-setup-item-tracking.md)|
|Assegnare numeri di serie o numeri di lotto a qualsiasi documento o riga di registrazione in entrata o in uscita.|[Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md)|
|È possibile trovare dove un numero seriale o di lotto è stato utilizzato nella sua catena di approvvigionamento, ad esempio in caso di richiamate.|[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)|
|Impostare la descrizione articolo di un cliente o un fornitore nella scheda articolo in modo che sia possibile inserire rapidamente la descrizione dell'articolo nei documenti commerciali.|[Utilizzare Cross reference articoli](inventory-how-use-item-cross-refs.md)|
|Bloccare gli articoli in modo che non vengano immessi in righe di acquisto o di vendita o che non vengano registrati in una qualsiasi transazione.|[Bloccare gli articoli](inventory-how-block-items.md)|
|È possibile gestire le operazioni aziendali in uffici vendite, reparti acquisti o uffici di programmazione impianti distribuiti tra più sedi.|[Utilizzare i centri di responsabilità](inventory-responsibility-centers.md)|
|Utilizzare risorse con competenze specifiche per vari servizi e articoli in assistenza.|[Impostare l'assegnazione delle risorse](service-how-setup-resource-allocation.md)|

## <a name="see-also"></a>Vedere anche

[Gestione warehouse](warehouse-manage-warehouse.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]