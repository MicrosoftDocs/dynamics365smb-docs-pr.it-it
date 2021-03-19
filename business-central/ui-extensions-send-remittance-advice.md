---
title: Estensione Invia avviso di rimessa | Microsoft Docs
description: Descrive l'estensione Invia avviso di rimessa, che consente di inviare l'avviso di rimessa dai movimenti contabili fornitori e dalle voci di registrazione pagamenti tramite posta elettronica.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e0868a5919f82af9d19dbd692c8d27577e64b6b0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376964"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="abbd3-103">Invia avviso di rimessa</span><span class="sxs-lookup"><span data-stu-id="abbd3-103">Send Remittance Advice</span></span>

<span data-ttu-id="abbd3-104">Quando l'avviso di rimessa viene utilizzato per notificare ai fornitori che sono in corso dei pagamenti, è ora possibile inviare l'avviso di rimessa in blocco tramite posta elettronica dalle registrazioni pagamenti nonché inviarlo nuovamente dopo l'esecuzione dei pagamenti dai movimenti contabili fornitori utilizzando i profili di invio documenti.</span><span class="sxs-lookup"><span data-stu-id="abbd3-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="abbd3-105">Questa funzionalità è supportata solo in Business Central online e in locale nei seguenti paesi: Regno Unito, Stati Uniti, Canada, Australia, Nuova Zelanda e Sudafrica.</span><span class="sxs-lookup"><span data-stu-id="abbd3-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="abbd3-106">È possibile inviare l'avviso di rimessa in due modi:</span><span class="sxs-lookup"><span data-stu-id="abbd3-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="abbd3-107">Nella pagina **Registrazioni pagamenti**, scegliere **Correlato**, **Pagamenti**, **Invia avviso di rimessa** per inviare l'avviso di rimessa per uno o più righe di registrazione pagamenti via posta elettronica</span><span class="sxs-lookup"><span data-stu-id="abbd3-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="abbd3-108">Nella pagina **Movimenti contabili fornitori**, scegliere **Azione**, **Funzioni**, **Invia avviso di rimessa** per inviare l'avviso di rimessa via posta elettronica dopo la registrazione dei pagamenti fornitori per uno o più movimenti contabili fornitori</span><span class="sxs-lookup"><span data-stu-id="abbd3-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="abbd3-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="abbd3-109">See Also</span></span>

[<span data-ttu-id="abbd3-110">Sugg. pagamenti fornitore</span><span class="sxs-lookup"><span data-stu-id="abbd3-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="abbd3-111">[Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="abbd3-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="abbd3-112">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="abbd3-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="abbd3-113">Inviare documenti via e-mail</span><span class="sxs-lookup"><span data-stu-id="abbd3-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]