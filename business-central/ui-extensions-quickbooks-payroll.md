---
title: Utilizzo dell'estensione per l'importazione del file retribuzioni di QuickBooks | Microsoft Docs
description: In questo argomento viene descritto come utilizzare l'estensione per importare transazioni di retribuzioni e stipendi da QuickBooks.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 01/09/2019
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 79729b42b660399893aebe1116c80ef3b3209042
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.contentlocale: it-it
ms.lasthandoff: 01/15/2019

---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Estensione per l'importazione del file retribuzioni di QuickBooks
Utilizzare l'estensione per l'importazione del file retribuzioni di Quickbooks per importare transazioni da QuickBooks nei conti C/G in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ad esempio, ciò è utile quando si esegue la transizione da QuickBooks a [!INCLUDE[d365fin](includes/d365fin_md.md)], oppure se si affida il servizio retribuzioni a terze parti ma si intende tenerne comunque traccia in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="steps-to-import-payroll-data"></a>Passaggi per importare dati delle retribuzioni
Il primo passaggio consiste nell'utilizzare le funzioni di esportazione in QuickBooks per esportare i dati delle retribuzioni in un file .IIF. Il secondo passaggio consiste nell'aprire la pagina **Registrazioni COGE** in [!INCLUDE[d365fin](includes/d365fin_md.md)] e nell'utilizzare l'azione **Importa transazioni retribuzioni** per importare il file. Durante il processo di importazione si esegue la mappatura dei conti C/G in QuickBooks ai conti corrispondenti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il passaggio finale consiste nel registrare le transazioni di retribuzione in [!INCLUDE[d365fin](includes/d365fin_md.md)] in base alla mappatura dei conti. 

Per ulteriori informazioni, vedere [Importare transazioni retributive](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Vedi anche
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)    
[Finanze](finance.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

