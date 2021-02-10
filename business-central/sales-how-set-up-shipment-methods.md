---
title: Come impostare metodi di spedizione | Documenti Microsoft
description: È possibile impostare un codice per ciascuno dei metodi di spedizione offerti e immettere informazioni relative a ognuno di essi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f1916724c995f875d15b931e919d07d2253dcdb1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748296"
---
# <a name="set-up-shipment-methods"></a>Impostare i metodi di spedizione
I metodi di spedizione, denominati anche incoterm, dipendono spesso dagli articoli, dai clienti e dai fornitori. Se ad esempio il cliente ha sede su un'isola, può scegliere che gli articoli gli vengano spediti sempre per via aerea oppure sempre via mare. Alcuni clienti potrebbero richiedere la consegna il giorno successivo. Alcuni potrebbero voler ritirare l'ordine. Nelle schede cliente e fornitore è possibile specificare il tipo di consegna desiderato.

Impostare nella pagina **Metodi di spedizione** la descrizione e il codice di ciascun metodo di spedizione. È possibile ad esempio impostare il codice FOB e immettere Franco a bordo nel campo **Descrizione**. Sarà quindi possibile immettere il codice nei campi **Codice metodo di spedizione** altrove nel sistema ad esempio in una scheda cliente. In seguito, quando si creano nuovi ordini, fatture, note di credito e così via, il sistema immetterà la descrizione rappresentata dal codice. È possibile modificarla sul documento in base alle esigenze.

## <a name="to-set-up-a-shipment-code"></a>Per impostare un codice spedizione
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Metodi di spedizione** e quindi scegliere il collegamento correlato.
2. Nella pagina **Metodi di spedizione** scegliere l'azione **Nuovo**.
3. Nella nuova riga specificare un codice e una descrizione per il metodo di spedizione.

## <a name="see-also"></a>Vedere anche
[Incoterm](https://iccwbo.org/resources-for-business/incoterms-rules)  
[Impostare gli spedizionieri](sales-how-to-set-up-shipping-agents.md)  
[Rintracciare i colli](sales-how-track-packages.md)    
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
