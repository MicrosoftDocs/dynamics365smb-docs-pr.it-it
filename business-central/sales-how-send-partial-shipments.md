---
title: Elaborare spedizioni parziali
description: Le spedizioni degli ordini di vendita possono essere elaborate in Business Central con spedizioni parziali utilizzando Avviso di spedizione e Qtà. nei campi di spedizione.
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 02/14/2024
ms.author: bholtorf
---
# Elaborare spedizioni parziali

In una spedizione parziale, un ordine non viene spedito tutto in una volta. Ad esempio, da un ordine di 100 unità, si ricevono 40 unità immediatamente e 60 in seguito. Per ogni ordine è possibile effettuare un numero illimitato di spedizioni.

Tuttavia, prima di poter utilizzare spedizioni parziali in [!INCLUDE [prod_short](includes/prod_short.md)], devi specificare che il cliente accetta spedizioni parziali impostando il campo **Avviso di spedizione** nella pagina **Scheda cliente**. In alternativa, se il cliente accetta solo spedizioni complete ma poi richiede o concorda con una spedizione parziale per uno specifico ordine di vendita, è possibile modificare il campo **Avviso di spedizione** prima della pubblicazione.

Per impostazione predefinita, [!INCLUDE [prod_short](includes/prod_short.md)] imposta il campo nella pagina **Scheda cliente** su **Parziale**, che consente spedizioni parziali. Tuttavia, se il campo è impostato per specificare **Completato**, il campo **Qtà da spedire** appare bloccato negli ordini cliente per quel cliente.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## Vedere anche

[Vendere prodotti con un ordine di vendita al cliente](sales-how-sell-products.md)  
[Spedire articoli](warehouse-how-ship-items.md)  
[Effettuare spedizioni dirette](sales-how-drop-shipment.md)  
[Vendite](sales-manage-sales.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
