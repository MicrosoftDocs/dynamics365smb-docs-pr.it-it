---
title: 'Procedura: Impostare i pagamenti automatici e gli effetti automatici'
description: In Business Central, è possibile gestire i pagamenti e gli effetti automatici.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e010769d7d3cc4a34c163f6644ae207714f42d3a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241805"
---
# <a name="set-up-automatic-payments-and-automatic-bills"></a><span data-ttu-id="94e27-103">Impostare i pagamenti automatici e gli effetti automatici</span><span class="sxs-lookup"><span data-stu-id="94e27-103">Set Up Automatic Payments and Automatic Bills</span></span>
<span data-ttu-id="94e27-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], è possibile gestire i pagamenti e gli effetti automatici.</span><span class="sxs-lookup"><span data-stu-id="94e27-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can manage automatic payments and bills.</span></span>  

<span data-ttu-id="94e27-105">Per utilizzare i pagamenti e gli effetti automatici, è necessario impostare le informazioni pertinenti.</span><span class="sxs-lookup"><span data-stu-id="94e27-105">To use automatic payments and automatic bills, you must set up the relevant information.</span></span>  

## <a name="to-add-bank-information-for-your-company"></a><span data-ttu-id="94e27-106">Per aggiungere le informazioni relative alla banca della società</span><span class="sxs-lookup"><span data-stu-id="94e27-106">To add bank information for your company</span></span>  

1.  <span data-ttu-id="94e27-107">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Informazioni società**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="94e27-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Company Information**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94e27-108">Nella Scheda dettaglio **Pagamenti** compilare i campi chiave come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="94e27-108">On the **Payments** FastTab, fill in the key fields as described in the following table.</span></span>  

    |<span data-ttu-id="94e27-109">Campo</span><span class="sxs-lookup"><span data-stu-id="94e27-109">Field</span></span>|<span data-ttu-id="94e27-110">Description</span><span class="sxs-lookup"><span data-stu-id="94e27-110">Description</span></span>|  
    |------------------------------------|---------------------------------------|  
    |<span data-ttu-id="94e27-111">**Metodo di pagamento**</span><span class="sxs-lookup"><span data-stu-id="94e27-111">**Payment Method**</span></span>|<span data-ttu-id="94e27-112">Selezionare il metodo di pagamento per il tipo dei pagamenti effettuati dal o al conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="94e27-112">Select the payment method for the type of payments made to or from this bank account.</span></span> <span data-ttu-id="94e27-113">Ad esempio, per il conto corrente bancario da utilizzare per i pagamenti automatici effettuati da clienti, selezionare un metodo di pagamento per bonifici bancari.</span><span class="sxs-lookup"><span data-stu-id="94e27-113">For example, for the bank account that will be used for automatic payments made by customers, select a payment method for bank transfers.</span></span>|  
    |<span data-ttu-id="94e27-114">**Conto effetti all'Incasso**</span><span class="sxs-lookup"><span data-stu-id="94e27-114">**Bills For Collection Acc. No.**</span></span>|<span data-ttu-id="94e27-115">Specificare il conto C/G sul quale verranno accreditati gli effetti per la riscossione.</span><span class="sxs-lookup"><span data-stu-id="94e27-115">Specify the general ledger account where bills for collection will be credited.</span></span>|  
    |<span data-ttu-id="94e27-116">**Conto effetti allo sconto**</span><span class="sxs-lookup"><span data-stu-id="94e27-116">**Bills For Discount Acc. No.**</span></span>|<span data-ttu-id="94e27-117">Specificare i conti di contabilità generale in cui verranno addebitati gli sconti di effetti.</span><span class="sxs-lookup"><span data-stu-id="94e27-117">Specify the general ledger account where bill discounts will be debited.</span></span>|  
    |<span data-ttu-id="94e27-118">**Conto effetti salvo buon fine**</span><span class="sxs-lookup"><span data-stu-id="94e27-118">**Bills Subj. to Coll. Acc. No.**</span></span>|<span data-ttu-id="94e27-119">Specificare il conto C/G sul quale verranno accreditati gli effetti soggetti alla riscossione.</span><span class="sxs-lookup"><span data-stu-id="94e27-119">Specify the general ledger account where bills subject to collection will be credited.</span></span>|  
    |<span data-ttu-id="94e27-120">**Conto spesa effetti**</span><span class="sxs-lookup"><span data-stu-id="94e27-120">**Expense Bill Account No.**</span></span>|<span data-ttu-id="94e27-121">Specificare i conti di contabilità generale in cui verranno registrate le spese per le ricevute bancarie.</span><span class="sxs-lookup"><span data-stu-id="94e27-121">Specify the general ledger account where expenses for bank receipts will be posted.</span></span>|  

5.  <span data-ttu-id="94e27-122">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="94e27-122">Choose the **OK** button.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="94e27-123">Prima di esportare un effetto fornitore, è necessario selezionare il formato di pagamento nel campo **Formato esportazione pagamento** nella pagina **Scheda conto corrente bancario**.</span><span class="sxs-lookup"><span data-stu-id="94e27-123">Before you can export a vendor bill, you must select a payment format in the **Payment Export Format** field on the **Bank Account Card** page.</span></span>  
    >   
    >  <span data-ttu-id="94e27-124">Prima di esportare un effetto cliente, è necessario selezionare il formato di pagamento nel campo **Formato esport. addebito dir. SEPA** nella pagina **Scheda conto corrente bancario**.</span><span class="sxs-lookup"><span data-stu-id="94e27-124">Before you can export a customer bill, you must select a payment format in the **SEPA Direct Debit Exp. Format** field on the **Bank Account Card** page.</span></span>  

<span data-ttu-id="94e27-125">Di seguito viene descritto come impostare gli effetti automatici per vendite e incassi, ma gli stessi passaggi sono applicabili per l'impostazione di acquisti e debiti per l'utilizzo dei pagamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="94e27-125">The following procedure describes how to set up automatic bills for sales and receivables, but the same steps also apply to setting up purchases and payables for using automatic payments.</span></span>  

## <a name="to-set-up-automatic-bills-for-sales-and-receivables"></a><span data-ttu-id="94e27-126">Per impostare gli effetti automatici per vendite e incassi</span><span class="sxs-lookup"><span data-stu-id="94e27-126">To set up automatic bills for sales and receivables</span></span>  

1.  <span data-ttu-id="94e27-127">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup contabilità clienti e vendite**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="94e27-127">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94e27-128">Nella Scheda dettaglio **Effetti**, nel campo **Nr. temp. distinta effetto**</span><span class="sxs-lookup"><span data-stu-id="94e27-128">On the **Bills** FastTab, in the **Temporary Bill List No.**</span></span> <span data-ttu-id="94e27-129">selezionare il numero temporaneo della distinta effetti.</span><span class="sxs-lookup"><span data-stu-id="94e27-129">field, select the temporary bill list number.</span></span> <span data-ttu-id="94e27-130">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="94e27-130">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="94e27-131">Campo</span><span class="sxs-lookup"><span data-stu-id="94e27-131">Field</span></span>|<span data-ttu-id="94e27-132">Description</span><span class="sxs-lookup"><span data-stu-id="94e27-132">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="94e27-133">**Nr. temp. distinta effetto**</span><span class="sxs-lookup"><span data-stu-id="94e27-133">**Temporary Bill List No.**</span></span>|<span data-ttu-id="94e27-134">Selezionare la numerazione che sarà utilizzata le distinte effetti temporanee.</span><span class="sxs-lookup"><span data-stu-id="94e27-134">Select the number series that will be used for temporary bill lists.</span></span>|  
    |<span data-ttu-id="94e27-135">**Richiamo effetti - Descrizione**</span><span class="sxs-lookup"><span data-stu-id="94e27-135">**Recall Bill Description**</span></span>|<span data-ttu-id="94e27-136">Specificare il testo descrittivo che verrà utilizzato per gli effetti richiamati.</span><span class="sxs-lookup"><span data-stu-id="94e27-136">Specify the descriptive text that will be used for recalled bills.</span></span>|  
    |<span data-ttu-id="94e27-137">**Periodo rischio RIBA**</span><span class="sxs-lookup"><span data-stu-id="94e27-137">**Bank Receipts Risk Period**</span></span>|<span data-ttu-id="94e27-138">Specificare una formula di data per il calcolo del periodo di rischio in giorni, ad esempio **20G**.</span><span class="sxs-lookup"><span data-stu-id="94e27-138">Specify a date formula to calculate the risk period in days, such as **20D**.</span></span><br /><br /> <span data-ttu-id="94e27-139">Questo sarà un riferimento per la chiusura ricevute bancarie.</span><span class="sxs-lookup"><span data-stu-id="94e27-139">This will be a reference for bank receipt closing.</span></span> <span data-ttu-id="94e27-140">Gli effetti del cliente verranno chiusi solo alla fine del periodo di rischio specificato qui.</span><span class="sxs-lookup"><span data-stu-id="94e27-140">Customer bills will be closed only at the end of the risk period that you specify here.</span></span>|  

3.  <span data-ttu-id="94e27-141">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="94e27-141">Choose the **OK** button.</span></span>  

 <span data-ttu-id="94e27-142">A questo punto, è necessario specificare i codici effetto per i metodi di pagamento utilizzati per i pagamenti automatici e gli effetti automatici.</span><span class="sxs-lookup"><span data-stu-id="94e27-142">Next, you must specify bill codes for those payment methods that you use for automatic payments and automatic bills.</span></span>  

## <a name="to-specify-bill-codes-for-a-payment-method"></a><span data-ttu-id="94e27-143">Per specificare i codici effetto per un metodo di pagamento</span><span class="sxs-lookup"><span data-stu-id="94e27-143">To specify bill codes for a payment method</span></span>  

1.  <span data-ttu-id="94e27-144">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Metodi di pagamento**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="94e27-144">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Methods**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94e27-145">Selezionare il metodo di pagamento utilizzato per i trasferimenti bancari ai fornitori, quindi nel campo **Cod. effetto**, selezionare un codice effetto.</span><span class="sxs-lookup"><span data-stu-id="94e27-145">Select the payment method that you use for bank transfers to vendors, and then, in the **Bill Code** field, select a bill code.</span></span>  

    1.  <span data-ttu-id="94e27-146">Per creare un codice effetto, nel campo **Cod. effetto**, scegliere il campo quindi scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="94e27-146">To create a bill code, in the **Bill Code** field, choose the field, and then choose the **New** action.</span></span>  
    2.  <span data-ttu-id="94e27-147">Compilare i campi della pagina **Effetto**.</span><span class="sxs-lookup"><span data-stu-id="94e27-147">On the **Bill** page, fill in the fields.</span></span>

<span data-ttu-id="94e27-148">A questo punto, è possibile elaborare gli effetti cliente e fornitore in modo che vengano gestiti automaticamente.</span><span class="sxs-lookup"><span data-stu-id="94e27-148">Now, you can process customer bills and vendor bills so that they are handled automatically.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94e27-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94e27-149">See Also</span></span>  
 <span data-ttu-id="94e27-150">[Definizione dei metodi di pagamento](../../finance-payment-methods.md)   </span><span class="sxs-lookup"><span data-stu-id="94e27-150">[Defining Payment Methods](../../finance-payment-methods.md)   </span></span>  
  [<span data-ttu-id="94e27-151">Funzionalità locale per l'Italia</span><span class="sxs-lookup"><span data-stu-id="94e27-151">Italy Local Functionality</span></span>](italy-local-functionality.md)
