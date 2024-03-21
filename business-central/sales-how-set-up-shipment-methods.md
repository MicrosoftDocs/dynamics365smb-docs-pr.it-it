---
title: Impostare i metodi di spedizione
description: È possibile impostare un codice per ciascuno dei metodi di spedizione offerti e immettere informazioni relative a ognuno di essi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: incoterms
ms.search.form: '11, 130'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-shipment-methods"></a>Impostare i metodi di spedizione

I metodi di spedizione dipendono spesso dagli articoli, dai clienti e dai fornitori. Se ad esempio il cliente ha sede su un'isola, può scegliere che gli articoli gli vengano spediti sempre per via aerea oppure sempre via mare. Alcuni clienti potrebbero richiedere la consegna il giorno successivo. Alcuni potrebbero voler ritirare l'ordine. Nelle schede cliente e fornitore è possibile specificare il tipo di consegna desiderato.

Impostare nella pagina **Metodi di spedizione** la descrizione e il codice di ciascun metodo di spedizione. È possibile ad esempio impostare il codice FOB e immettere Franco a bordo nel campo **Descrizione**. Sarà quindi possibile immettere il codice nei campi **Codice metodo di spedizione** altrove nel sistema ad esempio in una scheda cliente. In seguito, quando si creano nuovi ordini, fatture, note di credito e così via, il sistema immetterà la descrizione rappresentata dal codice. È possibile modificarla sul documento in base alle esigenze.

## <a name="to-set-up-a-shipment-method"></a>Per impostare un metodo di spedizione

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Metodi di spedizione**, quindi scegli il collegamento correlato.
2. Nella pagina **Metodi di spedizione** scegliere l'azione **Nuovo**.
3. Nella nuova riga specificare un codice e una descrizione per il metodo di spedizione.

> [!TIP]
> Se si utilizzano Incoterm, impostare i metodi di spedizione per rappresentare le regole Incoterm pertinenti.  

## <a name="see-also"></a>Vedere anche

[Impostare gli spedizionieri](sales-how-to-set-up-shipping-agents.md)  
[Rintracciare i colli](sales-how-track-packages.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Incoterm su iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
