---
title: Utilizzo dell'estensione per l'importazione del file retribuzioni di QuickBooks | Microsoft Docs
description: In questo argomento viene descritto come utilizzare l'estensione per importare transazioni di retribuzioni e stipendi da QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 838095fe81af36a421a49f19400b0abd5cdce17b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784767"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Estensione per l'importazione del file retribuzioni di QuickBooks
Utilizzare l'estensione per l'importazione del file retribuzioni di Quickbooks per importare transazioni da QuickBooks nei conti C/G in [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, ciò è utile quando si esegue la transizione da QuickBooks a [!INCLUDE[prod_short](includes/prod_short.md)], oppure se si affida il servizio retribuzioni a terze parti ma si intende tenerne comunque traccia in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="steps-to-import-payroll-data"></a>Passaggi per importare dati delle retribuzioni
Il primo passaggio consiste nell'utilizzare le funzioni di esportazione in QuickBooks per esportare i dati delle retribuzioni in un file .IIF. Il secondo passaggio consiste nell'aprire la pagina **Registrazioni COGE** in [!INCLUDE[prod_short](includes/prod_short.md)] e nell'utilizzare l'azione **Importa transazioni retribuzioni** per importare il file. Durante il processo di importazione si esegue la mappatura dei conti C/G in QuickBooks ai conti corrispondenti in [!INCLUDE[prod_short](includes/prod_short.md)]. Il passaggio finale consiste nel registrare le transazioni di retribuzione in [!INCLUDE[prod_short](includes/prod_short.md)] in base alla mappatura dei conti. 

Per ulteriori informazioni, vedere [Importare transazioni retributive](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Vedi anche
[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni ](ui-extensions.md)    
[Finanze](finance.md)    
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]