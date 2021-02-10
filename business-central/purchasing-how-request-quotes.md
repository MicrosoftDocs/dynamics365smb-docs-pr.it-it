---
title: Creare un'offerta di acquisto per richiedere un'offerta | Documenti Microsoft
description: Descrive come creare un documento di un'offerta di vendita o una richiesta di offerta (RdO) per registrare la propria offerta a un cliente per la vendita di prodotti in base a termini determinati.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cff54e778beb1bb08342835419998242eed4adf3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758469"
---
# <a name="request-quotes"></a>Richiedere le offerte
Un'offerta di acquisto può essere utilizzata come bozza preliminare di un ordine di acquisto e l'ordine può essere in seguito convertito in ordine o fattura di acquisto.


## <a name="to-create-a-purchase-quote"></a>Per creare un'offerta di acquisto
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Offerte acquisto** e quindi scegliere il collegamento correlato.
2. Creare un nuovo documento nello stesso modo in cui si crea un ordine di acquisto. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Per convertire un'offerta di acquisto in un ordine di acquisto
Una volta che l'offerta del fornitore viene accettata, può essere convertita in ordine o fattura di acquisto per elaborare l'acquisto.

1. Aprire un'offerta di acquisto pronta per essere convertita e scegliere l'azione **Crea ordine**.

L'offerta di acquisto viene rimossa dal database. Viene creato un ordine o una fattura di acquisto sulla base delle informazioni contenute nell'offerta di acquisto nella quale è possibile elaborare l'acquisto. Nel campo **Nr. offerta** dell'ordine o della fattura di acquisto è presente il numero dell'offerta di acquisto da cui è stato convertito.

## <a name="see-also"></a>Vedi anche
[Acquisti](purchasing-manage-purchasing.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
