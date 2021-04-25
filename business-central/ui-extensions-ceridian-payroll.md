---
title: Importazione dei dati di retribuzioni o stipendi tramite l'estensione Registro paga di Ceridian
description: Utilizzare questa estensione per importare le transazioni del registro paga dai servizi di Ceridian HR/Payroll (USA) e di Ceridian PowerPay (Canada).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f2129d26cab8de999ae6ae1e80943ee4066ab50f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787429"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="b7121-103">Estensione Registro paga di Ceridian</span><span class="sxs-lookup"><span data-stu-id="b7121-103">The Ceridian Payroll Extension</span></span>

<span data-ttu-id="b7121-104">Per indicare i pagamenti di stipendio e le transazioni correlate, è necessario importare e registrare in contabilità generale le transazioni finanziarie trasformate dal provider di retribuzioni.</span><span class="sxs-lookup"><span data-stu-id="b7121-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="b7121-105">A tale scopo, è necessario innanzitutto importare un file che si riceve dal provider di retribuzioni nella pagina **Contabilità generale**.</span><span class="sxs-lookup"><span data-stu-id="b7121-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="b7121-106">Successivamente si esegue il mapping tra i conti esterni nel file retribuzioni e i conti C/G pertinenti.</span><span class="sxs-lookup"><span data-stu-id="b7121-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="b7121-107">Infine, si registrano le transazioni retribuzioni in base alla mappatura dei conti.</span><span class="sxs-lookup"><span data-stu-id="b7121-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="b7121-108">Per ulteriori informazioni, vedere [Importare transazioni retributive](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="b7121-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="b7121-109">L'estensione Registro paga di Ceridian consente di importare le transazioni del registro paga dai servizi di Ceridian HR/Payroll (USA) e di Ceridian PowerPay (Canada).</span><span class="sxs-lookup"><span data-stu-id="b7121-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7121-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7121-110">See Also</span></span>

<span data-ttu-id="b7121-111">[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b7121-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="b7121-112">Finanze</span><span class="sxs-lookup"><span data-stu-id="b7121-112">Finance</span></span>](finance.md)  
<span data-ttu-id="b7121-113">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7121-113">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]