---
title: Panoramica dei task di gestione dei pagamenti ai fornitori| Documenti Microsoft
description: Descrive i task per gestire i pagamenti ai fornitori o ai creditori, inclusa la registrazione delle righe di pagamento e la visualizzazione di una panoramica del saldo dovuto.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="d4382-103">Effettuare i pagamenti</span><span class="sxs-lookup"><span data-stu-id="d4382-103">Make Payments</span></span>
<span data-ttu-id="d4382-104">Quando si eseguono i pagamenti ai fornitori, si registrano le relative righe di pagamento nella finestra **Registrazioni pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="d4382-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="d4382-105">Per individuare i pagamenti in scadenza, è possibile utilizzare la funzione **Sugg. pagamenti fornitore**.</span><span class="sxs-lookup"><span data-stu-id="d4382-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="d4382-106">È inoltre possibile utilizzare il report **Fornitori - Scadenziario riepilogativo** per avere una panoramica dei pagamenti in scadenza.</span><span class="sxs-lookup"><span data-stu-id="d4382-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="d4382-107">Dalle registrazioni pagamenti è possibile stampare assegni automatici o registrare l'emissione degli assegni.</span><span class="sxs-lookup"><span data-stu-id="d4382-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="d4382-108">Se si seleziona **Assegno automatico** nel campo **Tipo pagamento banca**, tutte le righe che rappresentano assegni devono essere stampate prima che le registrazioni pagamenti possano essere contabilizzate.</span><span class="sxs-lookup"><span data-stu-id="d4382-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="d4382-109">Quando si registrano i pagamenti, è possibile esportarli in un file della banca da caricare nella banca per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="d4382-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="d4382-110">Una volta effettuati i pagamenti presso la banca, è necessario collegarli ai relativi movimenti contabili fornitori aperti.</span><span class="sxs-lookup"><span data-stu-id="d4382-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="d4382-111">Questa operazione può essere eseguita manualmente o importando un file del rendiconto bancario e collegando i pagamenti automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d4382-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="d4382-112">Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e Riconciliazione dei conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="d4382-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="d4382-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="d4382-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="d4382-114">Per</span><span class="sxs-lookup"><span data-stu-id="d4382-114">To</span></span> | <span data-ttu-id="d4382-115">Vedere</span><span class="sxs-lookup"><span data-stu-id="d4382-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="d4382-116">Utilizzare una funzione per suggerire i pagamenti fornitore in base ai criteri selezionati, ad esempio la data di scadenza, l'idoneità allo sconto e la liquidità.</span><span class="sxs-lookup"><span data-stu-id="d4382-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="d4382-117">Procedura: Suggerire i pagamenti ai fornitori</span><span class="sxs-lookup"><span data-stu-id="d4382-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="d4382-118">Emettere assegni per i pagamenti, come stampati o come assegni automatici.</span><span class="sxs-lookup"><span data-stu-id="d4382-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="d4382-119">Annullare gli assegni prima o dopo la registrazione.</span><span class="sxs-lookup"><span data-stu-id="d4382-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="d4382-120">Procedura: Utilizzo degli assegni</span><span class="sxs-lookup"><span data-stu-id="d4382-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="d4382-121">Assicurarsi che la banca compensi solo gli assegni e gli importi convalidati inviandole un file che contenga informazioni sul fornitore, l'assegno e il pagamento.</span><span class="sxs-lookup"><span data-stu-id="d4382-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="d4382-122">Procedura: Esportare un file Positive Pay</span><span class="sxs-lookup"><span data-stu-id="d4382-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="d4382-123">Esportare i pagamenti dalla finestra **Registrazioni pagamenti** a un file della banca che viene caricato nella banca per l'elaborazione, incluso l'EFT (trasferimento elettronico di fondi) nell'America del Nord.</span><span class="sxs-lookup"><span data-stu-id="d4382-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="d4382-124">Procedura: Esportare pagamenti in un file della banca</span><span class="sxs-lookup"><span data-stu-id="d4382-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="d4382-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4382-125">See Also</span></span>
[<span data-ttu-id="d4382-126">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="d4382-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="d4382-127">Acquisti</span><span class="sxs-lookup"><span data-stu-id="d4382-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="d4382-128">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="d4382-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="d4382-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d4382-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

