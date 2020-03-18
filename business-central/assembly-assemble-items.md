---
title: Gestione assemblaggio | Microsoft Docs
description: Supporta le società che forniscono prodotti ai clienti combinando i componenti in semplici processi senza richiedere funzionalità di manufacturing, ma con funzionalità per assemblare gli articoli che si integrano con le funzionalità esistenti, ad esempio vendite, pianificazione, impegni e gestione warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 946b14c6d3a480bda217b9d78330343a8d772de1
ms.sourcegitcommit: 35552b250b37c97772129d1cb9fd9e2537c83824
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "3097722"
---
# <a name="assembly-management"></a>Gestione assemblaggio
Per supportare le società che forniscono prodotti ai clienti combinando i componenti in semplici processi senza richiedere funzionalità di manufacturing, [!INCLUDE[d365fin](includes/d365fin_md.md)] include funzionalità per assemblare gli articoli che si integrano con le funzionalità esistenti, ad esempio vendite, pianificazione, impegni e gestione warehouse.  

 Un articolo di assemblaggio è definito come articolo vendibile contenente una DB di assemblaggio. Per altre informazioni, vedere [Utilizzare le distinte base](inventory-how-work-BOMs.md).

 Gli ordini di assemblaggio sono ordini interni, come gli ordini di produzione, che vengono utilizzati per gestire il processo di assemblaggio e per collegare i requisiti di vendita con le attività di warehouse richieste. Gli ordini di assemblaggio differiscono da altri tipi di ordine perché prevedono sia l'output che il consumo in fase di registrazione. La testata dell'ordine di assemblaggio si comporta analogamente a una riga registrazioni output e le righe ordine di assemblaggio si comportano in modo analogo alle righe registrazioni consumi.  

 Per supportare una strategia di magazzino JIT (just-in-time) e la capacità di personalizzare i prodotti in base alle richieste del cliente, gli ordini di assemblaggio possono essere automaticamente creati e collegati non appena viene creata la riga ordine di vendita. Il collegamento tra di domanda di vendita e l'approvvigionamento di assemblaggio consente ai gestori dell'ordine di vendita di personalizzare rapidamente l'articolo di assemblaggio, promettere date di consegna in base alla disponibilità dei componenti e registrare l'output e la spedizione dell'articolo assemblato direttamente dalla propria interfaccia dell'ordine di vendita. Per ulteriori informazioni, vedere [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md).  

 In una sola riga ordine di vendita è possibile vendere una quantità disponibile che deve essere prelevata dallo stock insieme a una quantità che deve essere assemblata su ordine. Alcune regole sono disponibili per gestire la consegna di tali quantità in modo da assicurare che le quantità per l'assemblaggio su ordine abbiano la priorità rispetto alle quantità di magazzino in spedizione parziale. Per altre informazioni, vedere la sezione "Scenari di combinazione" in [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).  

 La funzionalità speciale consente di gestire la spedizione delle quantità per l'assemblaggio su ordine. Quando una quantità per l'assemblaggio su ordine è pronta per essere spedita, l'addetto warehouse incaricato registra un prelievo da magazzino per la riga ordine di vendita in questione. Questo, a sua volta, crea un movimento di magazzino per i componenti e registra l'output di assemblaggio e la spedizione dell'ordine di vendita. Per altre informazioni, vedere la sezione "Gestione di articoli da assemblare su ordine in prelievi magazzino" in [Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Ottenere informazioni sulla differenza tra l'assemblaggio di articoli immediatamente prima della spedizione di ordini di vendita e dell'assemblaggio di articoli destinati al magazzino.|[Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Compilare i campi nelle schede ubicazione e in Setup magazzino per definire il modo in cui gli articoli vengono trasmessi e prelevati dal reparto di assemblaggio.|[Impostare le warehouse di base con aree di operazioni](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Personalizzare un articolo di assemblaggio nella richiesta di un cliente durante il processo di vendita e convertirlo in vendita quando viene accettato.|[Offerta per una vendita assemblaggio su ordine](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Combinare componenti per creare un articolo in un semplice processo, su ordine o per magazzino.|[Assemblare articoli](assembly-how-to-assemble-items.md)|  
|Vendere articoli di assemblaggio che al momento non sono disponibili creando un ordine di assemblaggio collegato per fornire la quantità completa o parziale dell'ordine di vendita.|[Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md)|
|Quando alcuni articoli di assemblaggio su ordine sono già in magazzino, è possibile dedurne la relativa quantità dall'ordine di assemblaggio e impegnarla dal magazzino.|[Vendere gli articoli di magazzino nei flussi da assemblare su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Quando si vendono articoli di assemblaggio dal magazzino e non tutti gli articoli sono disponibili, è possibile avviare un ordine di assemblaggio per fornire automaticamente, interamente o in parte, la quantità dell'ordine di vendita.|[Vendere articoli di assemblaggio su ordine e articoli di magazzino insieme](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Creare articoli di assemblaggio personalizzati per ordini di vendita programmati prima di creare periodicamente gli ordini di vendita effettivi in base al contratto degli ordini programmati.|[Creare ordini di assemblaggio programmati](assembly-how-to-create-blanket-assembly-orders.md)|
|Annullare un ordine di assemblaggio registrato, ad esempio perché l'ordine è stato registrato con errori che devono essere corretti.|[Annullare la registrazione di assemblaggi](assembly-how-to-undo-assembly-posting.md)|
|Ottenere informazioni sulla differenza tra DB di assemblaggio e DB di produzione e le relative differenze di elaborazione.|[Utilizzare le distinte base](inventory-how-work-BOMs.md)|
|Apprendere come vengono gestiti l'output e il consumo in fase di assemblaggio quando si registrano ordini di assemblaggio e come vengono elaborati e distribuiti l'articolo e i costi risorse derivati nella contabilità generale.|[Dettagli di progettazione: Registrazione dell'ordine di assemblaggio](design-details-assembly-order-posting.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
