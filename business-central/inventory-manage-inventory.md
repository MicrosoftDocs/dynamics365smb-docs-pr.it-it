---
title: Gestione dell'inventario
description: Questo articolo descrive come gestire i prodotti fisici trattati creando una scheda articolo inventario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, stock'
ms.search.forms: '5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Gestire l'inventario

Per ogni prodotto fisico trattato è necessario creare una scheda articolo di tipo **Inventario**. Gli articoli che si offrono ai clienti ma che non sono presenti in magazzino possono essere registrati come articoli di catalogo che possono essere convertiti in articoli di magazzino se necessario. È possibile aumentare o diminuire la quantità di un articolo in magazzino registrando direttamente nei movimenti contabili articoli, ad esempio, dopo un conteggio fisico oppure se non si registrano gli acquisti.

Gli incrementi in magazzino e le diminuzioni vengono registrati automaticamente anche quando si registrano gli acquisti e i documenti di vendita rispettivamente. Per ulteriori informazioni, vedi [Registrare gli acquisti](purchasing-how-record-purchases.md), [Procedura: Vendere prodotti](sales-how-sell-products.md)e [Fatturare le vendite](sales-how-invoice-sales.md). I trasferimenti tra le ubicazioni cambiano le quantità in giacenza nelle warehouse della società.

Per ampliare la panoramica degli articoli e agevolare le operazioni di ricerca, è possibile classificare gli articoli e assegnare gli attributi per cercarli e ordinarli.

> [!NOTE]
> La gestione fisica degli articoli è detta attività di warehouse. Per ulteriori informazioni vedi [Panoramica di Warehouse Management](design-details-warehouse-management.md).

La pianificazione degli articoli per soddisfare la domanda è coperta nella funzionalità di pianificazione dell'offerta. Ulteriori informazioni in [Pianificazione](production-planning.md).  

## Riconciliazione dell'inventario

Quando si registrano transazioni di magazzino, ad esempio spedizioni, fatture di vendite o rettifiche di magazzino, le modifiche ai costi degli articoli vengono registrate automaticamente nei movimenti di valorizzazione. Per riflettere la modifica del valore di magazzino nei registri finanziari, i costi di magazzino vengono registrati automaticamente nei conti giacenza magazzino correlati in contabilità generale. Per ogni transazione di magazzino registrata, verranno registrati i valori appropriati nel conto giacenza magazzino, nel conto di rettifica e nel conto COGS nella contabilità generale. Ulteriori informazioni in [Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Anche se i costi vengono registrati automaticamente in contabilità generale, è comunque necessario assicurarsi che i costi delle merci vengano trasferiti alle transazioni in uscita correlate, in particolare nel caso in cui si vendano merci prima di fatturare il relativo acquisto. Questa operazione è detta rettifica dei costi. I costi dell'articolo vengono rettificati automaticamente quando si registrano le transazioni articolo, ma è possibile anche rettificarli manualmente. Ulteriori informazioni in [Rettifica costi articolo](inventory-how-adjust-item-costs.md).  

## Attività correlate

La tabella seguente descrive le attività correlate.

|A |Vedere |
|---|----|
|Creare le schede articolo per gli articoli di magazzino trattati.|[Registrare nuovi articoli](inventory-how-register-new-items.md)|
|Struttura gli articoli padre da vendere come kit costituiti da componenti del padre o da assemblare su ordine o per magazzino.|[Utilizzare le distinte base](inventory-how-work-BOMs.md)|
|Gestire una panoramica degli articoli e facilitare le operazioni di ricerca e ordinamento degli articoli organizzandoli in categorie.|[Classificare gli articoli](inventory-how-categorize-items.md)|
|Assegnare gli attributi dell'articolo dei diversi tipi di valore agli articoli per migliorare l'ordinamento e la ricerca degli articoli.|[Utilizzare gli attributi degli articoli](inventory-how-work-item-attributes.md)|
|Crea speciali schede articolo per gli articoli da offrire ai clienti che non vengono gestiti nell'inventario.|[Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md)|
|Eseguire il conteggio fisico del magazzino con le pagine **Ordine magazzino fisico** e **Registrazione magazzino fisico**.|[Conteggiare l'inventario utilizzando documenti](inventory-how-count-inventory-with-documents.md)|
|Eseguire attività di conteggio fisico, rettifiche positive o negative e modificare le informazioni, quali ubicazione o numero di lotto, nei movimenti contabili articoli.|[Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md)|
|Visualizza la disponibilità di articoli per ubicazione, periodo, evento di vendita o acquisto o in base all'utilizzo nelle distinte base assemblaggio o produzione.|[Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)|
|Trasferisci gli articoli in magazzino tra le ubicazioni con ordini di trasferimento, per gestire le attività di warehouse oppure con le registrazioni di riclassificazione articoli.|[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)|
|Impegna gli articoli in entrata o di magazzino per ordini di vendita, ordini di acquisto, ordini di assistenza, ordini di assemblaggio, ordini di trasferimento o ordini di produzione.|[Prenotare articoli](inventory-how-to-reserve-items.md)|
|Imposta la tracciabilità degli articoli in modo da poter tenere traccia dei numeri di serie, ad esempio per monitorare gli articoli a causa dei richiami.|[Configurare la tracciabilità di articoli con numeri di serie, di lotto e di pacco](inventory-how-setup-item-tracking.md)|
|Assegnare numeri di serie o numeri di lotto a qualsiasi documento o riga di registrazione in entrata o in uscita.|[Utilizzo dei numeri di serie e di lotto](inventory-how-work-item-tracking.md)|
|Trova dove un numero seriale o di lotto è stato utilizzato nella sua catena di approvvigionamento, ad esempio in caso di richiamate.|[Tracciare gli articoli tracciati](inventory-how-to-trace-item-tracked-items.md)|
|Imposta la descrizione articolo di un cliente o un fornitore nella scheda articolo in modo che sia possibile inserire rapidamente la descrizione dell'articolo nei documenti commerciali.|[Utilizzare i riferimenti dell'elemento](inventory-how-use-item-cross-refs.md)|
|Bloccare gli articoli in modo che non vengano immessi in righe di acquisto o di vendita o che non vengano registrati in una qualsiasi transazione.|[Bloccare gli articoli](inventory-how-block-items.md)|
|Gestisci le operazioni aziendali in uffici vendite, reparti acquisti o uffici di programmazione impianti distribuiti tra più sedi.|[Utilizzare i centri di responsabilità](inventory-responsibility-centers.md)|
|Utilizza risorse con funzioni specifiche per vari servizi e articoli in assistenza.|[Impostare l'assegnazione delle risorse](service-how-setup-resource-allocation.md)|

## Vedere anche

[Panoramica gestione del magazzino](design-details-warehouse-management.md)    
[Acquisti](purchasing-manage-purchasing.md)    
[Vendite](sales-manage-sales.md)    
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Funzionalità aziendali generali](ui-across-business-areas.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
