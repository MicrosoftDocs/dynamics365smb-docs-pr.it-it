---
title: Creare un'offerta di acquisto per richiedere un'offerta
description: Descrive come creare un documento di un'offerta di vendita o una richiesta di offerta (RdO) per registrare la propria offerta a un cliente per la vendita di prodotti in base a termini determinati.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Richiesta di offerte

Un'offerta di acquisto può essere utilizzata come bozza preliminare di un ordine di acquisto che può essere in seguito convertito in una fattura di acquisto.

## Creare un'offerta di acquisto

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Offerte acquisto**, quindi scegli il collegamento correlato.
2. Creare un nuovo documento nello stesso modo in cui si crea un ordine di acquisto. Ulteriori informazioni in [Registrare gli acquisti](purchasing-how-record-purchases.md).

## Convertire un'offerta di acquisto in un ordine di acquisto

Una volta che l'offerta del fornitore viene accettata, può essere convertita in ordine d'acquisto per elaborare l'acquisto.

1. Apri l'offerta di acquisto che si desidera convertire e scegli l'azione **Crea ordine**.

L'offerta di acquisto viene rimossa dal database. Viene creato un ordine di acquisto sulla base delle informazioni contenute nell'offerta di acquisto che puoi utilizzare per elaborare l'acquisto e, successivamente, immettere una fattura di acquisto. Nel campo **Nr. offerta** dell'ordine o della fattura di acquisto è presente il numero dell'offerta di acquisto da cui è stato convertito.

> [!NOTE]
> Non è possibile convertire direttamente un'offerta di acquisto direttamente in una fattura di acquisto, come è possibile con le offerte di vendita. Per i dettagli su come creare una fattura di acquisto, leggi [Registrare gli acquisti con le fatture di acquisto](purchasing-how-record-purchases.md).

## Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Inviare documenti tramite e-mail](ui-how-send-documents-email.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
