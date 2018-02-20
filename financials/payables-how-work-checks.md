---
title: Emettere, stampare, annullare un assegno| Documenti Microsoft
description: Descrive come emettere o stampare assegni tramite le registrazioni dei pagamenti e annullare movimenti contabili degli assegni in Finance and Operations, Business edition.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3f8bece0d0d1de9a6fd17b84df73d466ccdf403
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-checks"></a><span data-ttu-id="61ee3-103">Utilizzo degli assegni</span><span class="sxs-lookup"><span data-stu-id="61ee3-103">Work With Checks</span></span>
<span data-ttu-id="61ee3-104">È possibile emettere assegni elettronici e manuali in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="61ee3-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="61ee3-105">In entrambi i metodi vengono utilizzate le registrazioni pagamenti per emettere assegni ai fornitori.</span><span class="sxs-lookup"><span data-stu-id="61ee3-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="61ee3-106">È inoltre possibile annullare assegni e visualizzare movimenti contabili assegni.</span><span class="sxs-lookup"><span data-stu-id="61ee3-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="61ee3-107">Il processo di emissione degli assegni comporta il suggerimento di pagamenti, la creazione di movimenti contabili e la stampa di assegni automatici.</span><span class="sxs-lookup"><span data-stu-id="61ee3-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="61ee3-108">Per assicurarsi che la banca compensi solo gli assegni e gli importi convalidati, è possibile inviarle un file che contenga informazioni sul fornitore, l'assegno e il pagamento.</span><span class="sxs-lookup"><span data-stu-id="61ee3-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="61ee3-109">Per ulteriori informazioni, vedere [Esportare un file Positive Pay](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="61ee3-109">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="61ee3-110">La stampante deve essere configurata per i moduli di assegni e deve essere definito il layout dell'assegno da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="61ee3-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="61ee3-111">Per ulteriori informazioni, vedere [Definire i layout degli assegni](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="61ee3-111">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="61ee3-112">Per emettere assegni</span><span class="sxs-lookup"><span data-stu-id="61ee3-112">To issue checks</span></span>
1. <span data-ttu-id="61ee3-113">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni pagamenti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="61ee3-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="61ee3-114">Compilare le registrazioni con pagamenti rilevanti, ad esempio utilizzando la funzione Sugg. pagamenti fornitore.</span><span class="sxs-lookup"><span data-stu-id="61ee3-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="61ee3-115">Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="61ee3-115">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="61ee3-116">Nel campo **Tipo pagamento banca** nelle righe di registrazione per il pagamento che si desidera effettuare con assegni, selezionare una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="61ee3-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="61ee3-117">**Assegno automatico**: selezionare questa opzione per stampare un assegno relativo all'importo specificato nella riga di registrazione pagamenti.</span><span class="sxs-lookup"><span data-stu-id="61ee3-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="61ee3-118">È necessario stampare gli assegni prima di poter registrare le righe di registrazione.</span><span class="sxs-lookup"><span data-stu-id="61ee3-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="61ee3-119">È possibile selezionare **Assegno automatico** solo se il campo **Tipo contropartita** o il campo **Tipo conto** è impostato su **Conto bancario**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="61ee3-120">**Assegno manuale**: selezionare questa opzione se è stato creato un assegno manualmente e si desidera creare un corrispondente movimento contabile per questo importo.</span><span class="sxs-lookup"><span data-stu-id="61ee3-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="61ee3-121">Non è possibile stampare assegni tramite questa opzione da [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="61ee3-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="61ee3-122">È possibile selezionare **Assegno manuale** solo se il campo **Tipo contropartita** o il campo **Tipo conto** è impostato su **Conto bancario**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="61ee3-123">È necessario stampare gli assegni automatici prima di poter registrare le righe di registrazione correlate.</span><span class="sxs-lookup"><span data-stu-id="61ee3-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="61ee3-124">In caso di assegni automatici, scegliere **Stampa assegno**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="61ee3-125">Nella finestra **Assegno** compilare i campi secondo le proprie necessità.</span><span class="sxs-lookup"><span data-stu-id="61ee3-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="61ee3-126">Selezionare il pulsante **Stampa**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="61ee3-127">Se si desidera stampare gli assegni provenienti da vari conti correnti bancari utilizzando più di una valuta, eseguire un singolo processo batch **Stampa assegno** per ogni valuta, specificando il conto corrente bancario appropriato.</span><span class="sxs-lookup"><span data-stu-id="61ee3-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="61ee3-128">Per annullare assegni stampati che non sono registrati</span><span class="sxs-lookup"><span data-stu-id="61ee3-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="61ee3-129">È possibile annullare gli assegni non registrati dopo che sono stati stampati utilizzando l'azione **Annullo assegno** della finestra **Registrazioni pagamenti**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="61ee3-130">Nella finestra **Registrazioni pagamenti** scegliere **Annullo assegno**, quindi scegliere gli assegni da annullare.</span><span class="sxs-lookup"><span data-stu-id="61ee3-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="61ee3-131">Per annullare gli assegni</span><span class="sxs-lookup"><span data-stu-id="61ee3-131">To void checks</span></span>
<span data-ttu-id="61ee3-132">Una volta che i pagamenti tramite assegno sono stati registrati, è possibile annullare gli assegni dai movimenti contabili bancari risultanti.</span><span class="sxs-lookup"><span data-stu-id="61ee3-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="61ee3-133">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **C/C bancari**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="61ee3-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="61ee3-134">Selezionare il conto corrente bancario appropriato, scegliere l'azione **Modifica**, quindi scegliere l'azione **Mov. contabili assegni**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="61ee3-135">Nella finestra **Mov. contabili assegni** scegliere l'azione **Annullo assegno**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="61ee3-136">Selezionare la casella di controllo **Annullo solo assegno**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="61ee3-137">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="61ee3-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="61ee3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61ee3-138">See Also</span></span>
[<span data-ttu-id="61ee3-139">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="61ee3-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="61ee3-140">Impostazione delle attività bancarie</span><span class="sxs-lookup"><span data-stu-id="61ee3-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="61ee3-141">Esportare un file Positive Pay</span><span class="sxs-lookup"><span data-stu-id="61ee3-141">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="61ee3-142">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61ee3-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

