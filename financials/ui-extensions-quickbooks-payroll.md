---
title: Utilizzo dell'estensione per l'importazione del file retribuzioni di Quickbooks | Documenti Microsoft
description: Descrive come utilizzare l'estensione per importare transazioni di retribuzioni e stipendi dal servizio retribuzioni di Quickbooks.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b719a7d2b6b5590ae63920b63aaba8c2313a8661
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-payroll-file-import-extension-to-dynamics-365-for-financials"></a><span data-ttu-id="947a5-103">Estensione per l'importazione del file retribuzioni di Quickbooks in Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="947a5-103">The Quickbooks Payroll File Import Extension to Dynamics 365 for Financials</span></span>
<span data-ttu-id="947a5-104">Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni.</span><span class="sxs-lookup"><span data-stu-id="947a5-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="947a5-105">A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella finestra **Contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="947a5-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="947a5-106">Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti.</span><span class="sxs-lookup"><span data-stu-id="947a5-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="947a5-107">Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.</span><span class="sxs-lookup"><span data-stu-id="947a5-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="947a5-108">Per ulteriori informazioni, vedere [Procedura: Importare transazioni retributive](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="947a5-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="947a5-109">L'estensione per l'importazione del file retribuzioni di Quickbooks consente di importare transazioni retributive del servizio retribuzioni di Quickbooks.</span><span class="sxs-lookup"><span data-stu-id="947a5-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="947a5-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="947a5-110">See Also</span></span>
<span data-ttu-id="947a5-111">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="947a5-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="947a5-112">[Finanze](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="947a5-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="947a5-113">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="947a5-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

