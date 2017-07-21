---
title: Imposta sulle vendite in Canada| Documenti Microsoft
description: Informazioni sull'imposta locale su vendite, beni e servizi in Canada.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a>Report imposta locale su vendite, beni e servizi in Canada
In Canada, quando un fornitore non è presente da un punto di vista commerciale nella provincia in cui vengono effettuati gli acquisti, il fornitore addebita solo le imposte Goods and Services Tax (GST) o Harmonized Sales Tax (HST). Tuttavia, se nella provincia è prevista un'imposta Provincial Sales Tax (PST), l'acquirente deve calcolare anche l'imposta PST e pagarla direttamente alla provincia. Se viene selezionato un codice Provincial Tax Area Code, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo usa per calcolare l'imposta PST e registrarla in modo da ottenere un debito d'imposta sia nella contabilità generale che nei record dell'imposta. Di conseguenza, il codice area imposte selezionato in questo campo deve essere solo un codice che include l'imposta PST e non GST.  

Per ulteriori informazioni sulle imposte di vendita, vedere [Imposte di vendita e categorie fiscali negli Stati Uniti e in Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Inviare il file GST/HST
Le informazioni fiscali nei documenti di acquisto vengono utilizzate per generare il trasferimento online di file GST/HST che è necessario inviare alle autorità fiscali. Il file include le imposte Goods and Services Tax (GST) e Harmonized Sales Tax (HST). Il file viene creato in un formato .tax, che può essere trasferito online.  

## <a name="see-also"></a>Vedi anche
[Finanza](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Imposte di vendita e categorie fiscali negli Stati Uniti e in Canada](us-finance-sales-tax.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

