---
title: Sales Tax e Goods and Services Tax in Canada | Documenti Microsoft
description: Ottenere informazioni su Goods and Services Tax (GST) o Harmonized Sales Tax (HST).
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 03/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e1866f5047a826f3d527267d901eb30279d5b4e4
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-goods-and-services-tax-in-canada"></a>Imposte sulla vendita e Goods and Services Tax in Canada
In Canada, quando un fornitore non è presente da un punto di vista commerciale nella provincia in cui vengono effettuati gli acquisti, il fornitore addebita solo le imposte Goods and Services Tax (GST) o Harmonized Sales Tax (HST). Tuttavia, se nella provincia è prevista un'imposta Provincial Sales Tax (PST), l'acquirente deve calcolare anche l'imposta PST e pagarla direttamente alla provincia. Se viene selezionato un codice Provincial Tax Area Code, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo usa per calcolare l'imposta PST e registrarla in modo da ottenere un debito d'imposta sia nella contabilità generale che nei record dell'imposta. Di conseguenza, il codice area imposte selezionato in questo campo deve essere solo un codice che include l'imposta PST e non GST.  

Per ulteriori informazioni sulle imposte di vendita, vedere [Imposte di vendita e categorie fiscali negli Stati Uniti e in Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Inviare il file GST/HST
Le informazioni fiscali nei documenti di acquisto vengono utilizzate per generare il trasferimento online di file GST/HST che è necessario inviare alle autorità fiscali. Il file include le imposte Goods and Services Tax (GST) e Harmonized Sales Tax (HST). Il file viene creato in un formato .tax, che può essere trasferito online.  

## <a name="see-also"></a>Vedi anche
[Finanza](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Imposte di vendita e categorie fiscali negli Stati Uniti e in Canada](us-finance-sales-tax.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

