---
title: Elaborare spedizioni parziali
description: Le spedizioni degli ordini di vendita possono essere elaborate in Business Central con spedizioni parziali utilizzando Avviso di spedizione e Qtà. nei campi di spedizione.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 08/12/2022
ms.author: a-reishima
---
# Elaborare spedizioni parziali

In una spedizione parziale, un ordine non viene spedito tutto in una volta. Ad esempio, da un ordine di 100 unità, si ricevono 40 unità immediatamente e 60 in seguito. Per ogni ordine è possibile effettuare un numero illimitato di spedizioni.

Tuttavia, prima di poter utilizzare spedizioni parziali in [!INCLUDE [prod_short](includes/prod_short.md)], devi specificare che il cliente accetta spedizioni parziali impostando il campo **Avviso di spedizione** nella pagina **Scheda cliente**. In alternativa, se il cliente solitamente accetta solo spedizioni complete ma poi richiede o concorda con una spedizione parziale per uno specifico ordine di vendita, è possibile modificare il campo **Avviso di spedizione** prima della pubblicazione.

Per impostazione predefinita, [!INCLUDE [prod_short](includes/prod_short.md)] imposta il campo nella pagina **Scheda cliente** su **Parziale**, che consente spedizioni parziali. Se, tuttavia, il campo è stato modificato in **Completato**, il campo **Qtà da spedire** è bloccato negli ordini cliente per quel cliente.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## Vedere anche

[Vendere prodotti con un ordine di vendita al cliente](sales-how-sell-products.md)  
[Spedire articoli](warehouse-how-ship-items.md)  
[Effettuare spedizioni dirette](sales-how-drop-shipment.md)  
[Vendite](sales-manage-sales.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
