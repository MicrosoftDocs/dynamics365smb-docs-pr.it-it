---
title: Utilizzo dell'estensione per l'importazione del file retribuzioni di QuickBooks | Microsoft Docs
description: In questo argomento viene descritto come utilizzare l'estensione per importare transazioni di retribuzioni e stipendi da QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eae93ea8cf81a2fad6af2c3810f94d5292eef93f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757094"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="76594-103">Estensione per l'importazione del file retribuzioni di QuickBooks</span><span class="sxs-lookup"><span data-stu-id="76594-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="76594-104">Utilizzare l'estensione per l'importazione del file retribuzioni di Quickbooks per importare transazioni da QuickBooks nei conti C/G in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="76594-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="76594-105">Ad esempio, ciò è utile quando si esegue la transizione da QuickBooks a [!INCLUDE[prod_short](includes/prod_short.md)], oppure se si affida il servizio retribuzioni a terze parti ma si intende tenerne comunque traccia in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="76594-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="76594-106">Passaggi per importare dati delle retribuzioni</span><span class="sxs-lookup"><span data-stu-id="76594-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="76594-107">Il primo passaggio consiste nell'utilizzare le funzioni di esportazione in QuickBooks per esportare i dati delle retribuzioni in un file .IIF.</span><span class="sxs-lookup"><span data-stu-id="76594-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="76594-108">Il secondo passaggio consiste nell'aprire la pagina **Registrazioni COGE** in [!INCLUDE[prod_short](includes/prod_short.md)] e nell'utilizzare l'azione **Importa transazioni retribuzioni** per importare il file.</span><span class="sxs-lookup"><span data-stu-id="76594-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="76594-109">Durante il processo di importazione si esegue la mappatura dei conti C/G in QuickBooks ai conti corrispondenti in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="76594-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="76594-110">Il passaggio finale consiste nel registrare le transazioni di retribuzione in [!INCLUDE[prod_short](includes/prod_short.md)] in base alla mappatura dei conti.</span><span class="sxs-lookup"><span data-stu-id="76594-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="76594-111">Per ulteriori informazioni, vedere [Importare transazioni retributive](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="76594-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="76594-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76594-112">See Also</span></span>
<span data-ttu-id="76594-113">[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="76594-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="76594-114">[Finanze](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="76594-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="76594-115">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76594-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
