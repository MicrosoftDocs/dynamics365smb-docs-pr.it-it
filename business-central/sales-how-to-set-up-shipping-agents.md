---
title: 'Procedura: Impostare gli spedizionieri | Documenti Microsoft'
description: È possibile impostare un codice per ciascuno degli spedizionieri di cui si avvale l'azienda e immettere informazioni relative a ognuno di essi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 221578a174c6bd0dd87377340e97cd54a98d177b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778399"
---
# <a name="set-up-shipping-agents"></a>Impostare gli spedizionieri
È possibile impostare un codice per ciascuno degli spedizionieri di cui si avvale l'azienda e immettere informazioni relative a ognuno di essi.  

Se viene immesso l'indirizzo Internet di uno spedizioniere che fornisce servizi per rintracciare colli su Internet, è possibile utilizzare la funzione di tracciabilità automatica dei colli. Per ulteriori informazioni, vedere [Rintracciare i colli](sales-how-track-packages.md).

Quando sugli ordini di vendita vengono impostati i relativi spedizionieri è possibile specificare anche i servizi offerti da ciascuno spedizioniere.  
Per ciascuno di essi è possibile impostare un numero qualsiasi di servizi e per ogni servizio si può impostare il tempo di spedizione.  

Quando a una riga di ordine di vendita viene assegnato un servizio spedizioniere, il tempo di spedizione del servizio sarà compreso nel calcolo della promessa d'ordine relativa a quella riga. Per ulteriori informazioni, vedere [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Per impostare uno spedizioniere  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Spedizionieri** e quindi scegliere il collegamento correlato.  
2.  Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Scegliere l'azione **Servizi spedizioniere**.
4. In **Servizi spedizioniere** compilare tutti i campi in base alle esigenze.

> [!NOTE]  
>  Se uno spedizioniere viene eliminato dalla riga di ordine, verrà eliminato anche il codice di servizio spedizioniere. Il contenuto di campi parzialmente basato sul servizio spedizioniere verrà ricalcolato.  

## <a name="see-also"></a>Vedere anche
[Impostare i metodi di pagamento:](sales-how-set-up-shipment-methods.md)  
[Rintracciare i colli](sales-how-track-packages.md)    
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]