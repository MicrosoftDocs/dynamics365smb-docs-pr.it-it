---
title: Estensione Invia avviso di rimessa | Microsoft Docs
description: Descrive l'estensione Invia avviso di rimessa, che consente di inviare l'avviso di rimessa dai movimenti contabili fornitori e dalle voci di registrazione pagamenti tramite posta elettronica.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 06/06/2019
ms.author: sgroespe
ms.openlocfilehash: 9caa026f9edec42e56a035cf8d99228ca18c3c36
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621254"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="627f2-103">Invia avviso di rimessa</span><span class="sxs-lookup"><span data-stu-id="627f2-103">Send Remittance Advice</span></span>
<span data-ttu-id="627f2-104">Quando l'avviso di rimessa viene utilizzato per notificare ai fornitori che sono in corso dei pagamenti, è ora possibile inviare l'avviso di rimessa in blocco tramite posta elettronica dalle registrazioni pagamenti nonché inviarlo nuovamente dopo l'esecuzione dei pagamenti dai movimenti contabili fornitori utilizzando i profili di invio documenti.</span><span class="sxs-lookup"><span data-stu-id="627f2-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="627f2-105">Questa funzionalità è supportata solo in Business Central online e in locale nei seguenti paesi: Regno Unito, Stati Uniti, Canada, Australia, Nuova Zelanda e Sudafrica.</span><span class="sxs-lookup"><span data-stu-id="627f2-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="627f2-106">È possibile inviare l'avviso di rimessa in due modi:</span><span class="sxs-lookup"><span data-stu-id="627f2-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="627f2-107">Nella pagina **Registrazioni pagamenti**, scegliere **Naviga**, **Pagamenti**, **Invia avviso di rimessa** per inviare l'avviso di rimessa per uno o più righe di registrazione pagamenti via posta elettronica</span><span class="sxs-lookup"><span data-stu-id="627f2-107">In the **Payment Journal** page, choose **Navigate**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="627f2-108">Nella pagina **Movimenti contabili fornitori**, scegliere Azione, Funzioni, Invia avviso di rimessa per inviare l'avviso di rimessa via posta elettronica dopo la registrazione dei pagamenti fornitori per uno o più movimenti contabili fornitori</span><span class="sxs-lookup"><span data-stu-id="627f2-108">I the **Vendor Ledger Entries** page, choose Action, Functions, Send Remittance Advice to email remittance advice after posting of vendor payments, for one of multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="627f2-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="627f2-109">See Also</span></span>
[<span data-ttu-id="627f2-110">Sugg. pagamenti fornitore</span><span class="sxs-lookup"><span data-stu-id="627f2-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="627f2-111">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="627f2-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="627f2-112">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="627f2-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
