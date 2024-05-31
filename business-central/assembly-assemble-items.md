---
title: Gestione assemblaggio
description: Informazioni su come fornire prodotti ai clienti combinando componenti in processi semplici senza utilizzare le funzionalità di produzione.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/26/2024
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# <a name="assembly-management"></a>Gestione assemblaggio

Le società possono fornire prodotti ai clienti combinando componenti senza utilizzare le funzionalità di produzione. Le funzionalità per l'assemblaggio degli articoli si integrano con funzionalità correlate come vendite, pianificazione, impegni e warehouse.  

Un articolo di assemblaggio è un articolo vendibile contenente una DB assemblaggio. Per ulteriori informazioni sulle distinte materiali di assemblaggio, vai a [Utilizzare le distinte materiali di assemblaggio](assembly-how-work-assembly-boms.md).

Gli ordini di assemblaggio sono ordini interni, proprio come gli ordini di produzione. Utilizza gli ordini di assemblaggio per gestire il processo di assemblaggio e collegare i fabbisogni di vendita con le attività di warehouse. Gli ordini di assemblaggio riguardano sia l'output che il consumo durante la registrazione. Le intestazioni dell'ordine di assemblaggio sono simili alle righe di registrazione output. Le righe dell'ordine di assemblaggio sono simili alle righe di registrazione consumi.  

Puoi utilizzare una strategia di inventario just-in-time e personalizzare i prodotti per soddisfare le richieste dei clienti. Gli ordini di assemblaggio possono essere automaticamente creati e collegati quando crei una riga dell'ordine di vendita. Il collegamento tra la domanda di vendita e l'offerta di assemblaggio offre diverse opportunità durante l'elaborazione degli ordini di vendita:

* Personalizzare immediatamente gli articoli di assemblaggio.
* Date di consegna promesse in base alla disponibilità dei componenti.
* Registra l'output e la spedizione dell'articolo assemblato direttamente dagli ordini di vendita.

Per ulteriori informazioni sulla vendita di articoli di assemblaggio, vai a [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

Le righe negli ordini di vendita possono contenere articoli da prelevare dal magazzino e articoli da assemblare per l'ordine. Le quantità da assemblare su ordine hanno la priorità sulle quantità di magazzino nella spedizione parziale. Per ulteriori informazioni sulla vendita di articoli di assemblaggio e magazzino, vai a [Scenari di combinazione](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Quando una quantità per l'assemblaggio su ordine è pronta per essere spedita, l'addetto warehouse può registrare un prelievo da magazzino per la riga ordine di vendita. La registrazione di un prelievo da magazzino fa un paio di cose:

* Crea un movimento di magazzino per i componenti
* Registra l'output assemblaggio e la spedizione dell'ordine di vendita.

Per ulteriori informazioni sugli articoli assemblaggio su ordine e sui prelievi di magazzino, vai a [Gestione di articoli assemblaggio su ordine con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|  
|Informazioni sull'assemblaggio degli articoli per gli ordini di vendita e lo stoccaggio.|[Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Usa le schede ubicazione e setup magazzino per definire il modo in cui gli articoli vengono trasmessi e prelevati dall'assemblaggio.|[Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Fai un'offerta per un articolo di assemblaggio personalizzato e poi converti l'offerta in una vendita quando il cliente la accetta.|[Offerta per una vendita assemblaggio su ordine](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Combina i componenti per creare un articolo, su ordine o per magazzino.|[Assemblare articoli](assembly-how-to-assemble-items.md)|  
|Vendi gli articoli di assemblaggio che al momento non sono disponibili creando un ordine di assemblaggio collegato per fornire la quantità completa o parziale dell'ordine di vendita.|[Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md)|
|Quando alcuni articoli di assemblaggio su ordine sono già in magazzino, deduci la quantità dall'ordine di assemblaggio e impegnala dal magazzino.|[Vendere gli articoli di magazzino nei flussi da assemblare su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Quando gli articoli di assemblaggio non sono in magazzino, utilizza un ordine di assemblaggio per fornire la quantità parziale o totale.|[Vendere articoli di assemblaggio su ordine e articoli di magazzino insieme](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Crea gli articoli di assemblaggio personalizzati per ordini di vendita programmati prima di creare gli ordini di vendita.|[Creare ordini di assemblaggio programmati](assembly-how-to-create-blanket-assembly-orders.md)|
|Annulla un ordine di assemblaggio registrato, ad esempio perché l'ordine è stato registrato con errori.|[Annullare la registrazione di assemblaggi](assembly-how-to-undo-assembly-posting.md)|
|Scopri come lavorare con le distinte base di assemblaggio e le principali differenze rispetto alle distinte base di produzione.|[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)|
|Informazioni sulla registrazione del consumo e dell'output di assemblaggio e su come [!INCLUDE [prod_short](includes/prod_short.md)] distribuisce i costi degli articoli e delle risorse nella contabilità generale.|[Dettagli di progettazione: registrazione dell'ordine di assemblaggio](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a>Vedere anche

[Usare le distinte base](inventory-how-work-BOMs.md)  
[Inventario](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Dettagli di progettazione: pianificazione dell'approvvigionamento](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
