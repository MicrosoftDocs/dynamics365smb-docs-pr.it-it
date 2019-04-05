---
title: Importazione dei dati di retribuzioni o stipendi tramite l'estensione Registro paga di Ceridian | Documenti Microsoft
description: Utilizzare questa estensione per importare le transazioni del registro paga dai servizi di Ceridian HR/Payroll (USA) e di Ceridian PowerPay (Canada).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: ed3ba9f10ce24c97760dce972aa96134f1bc1119
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "800908"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="e6643-103">Estensione per il registro paga di Ceridian</span><span class="sxs-lookup"><span data-stu-id="e6643-103">The Ceridian Payroll Extension</span></span>
<span data-ttu-id="e6643-104">Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni.</span><span class="sxs-lookup"><span data-stu-id="e6643-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="e6643-105">A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella pagina **Contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="e6643-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="e6643-106">Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e6643-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="e6643-107">Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.</span><span class="sxs-lookup"><span data-stu-id="e6643-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="e6643-108">Per ulteriori informazioni, vedere [Importare transazioni retributive](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="e6643-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="e6643-109">L'estensione per il registro paga di Ceridian consente di importare le transazioni del registro paga dai servizi di Ceridian HR/Payroll (USA) e di Ceridian PowerPay (Canada).</span><span class="sxs-lookup"><span data-stu-id="e6643-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6643-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6643-110">See Also</span></span>
<span data-ttu-id="e6643-111">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="e6643-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="e6643-112">[Finanze](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="e6643-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="e6643-113">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e6643-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
