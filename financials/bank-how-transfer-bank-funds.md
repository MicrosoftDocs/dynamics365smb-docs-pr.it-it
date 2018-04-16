---
title: Trasferire fondi bancari| Documenti Microsoft
description: "È possibile trasferire gli importi da un conto corrente bancario a un altro, incluse le valute diverse, tramite la registrazione della transazione nelle registrazioni COGE."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: f19fbdd0f0059e62080d0076bdc419712560d4f2
ms.contentlocale: it-it
ms.lasthandoff: 04/16/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="087c1-103">Trasferimento di fondi bancari</span><span class="sxs-lookup"><span data-stu-id="087c1-103">Transfer Bank Funds</span></span>
<span data-ttu-id="087c1-104">Talvolta, può anche essere necessario effettuare un bonifico da un conto corrente bancario ad un altro.</span><span class="sxs-lookup"><span data-stu-id="087c1-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="087c1-105">A tale scopo, è necessario registrare una transazione nelle registrazioni COGE.</span><span class="sxs-lookup"><span data-stu-id="087c1-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="087c1-106">L'attività varia a seconda se i conti correnti bancari utilizzano la stessa valuta o valute diverse.</span><span class="sxs-lookup"><span data-stu-id="087c1-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="087c1-107">Per registrare un bonifico tra conti correnti bancari con lo stesso codice valuta</span><span class="sxs-lookup"><span data-stu-id="087c1-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="087c1-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="087c1-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="087c1-109">In una riga di registrazioni compilare i campi **Data di registrazione** e **Nr. documento**.</span><span class="sxs-lookup"><span data-stu-id="087c1-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="087c1-110">Nel campo **Tipo conto** selezionare **Conti C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="087c1-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="087c1-111">Nel campo **Nr. conto** selezionare la banca da cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="087c1-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="087c1-112">Immettere l'importo da traferire nel campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="087c1-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="087c1-113">Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="087c1-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="087c1-114">Nel campo **Nr. contropartita** selezionare il conto bancario a cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="087c1-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="087c1-115">Effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="087c1-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="087c1-116">Per registrare un bonifico tra conti correnti bancari con codici valuta diversi</span><span class="sxs-lookup"><span data-stu-id="087c1-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="087c1-117">Per trasferire i fondi tra conti correnti bancari che utilizzano valute diverse, è necessario inserire due righe di registrazioni COGE.</span><span class="sxs-lookup"><span data-stu-id="087c1-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="087c1-118">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="087c1-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="087c1-119">Creare due righe di registrazione e compilare i campi **Data di registrazione** e **Nr. documento**.</span><span class="sxs-lookup"><span data-stu-id="087c1-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="087c1-120">Nella prima riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.</span><span class="sxs-lookup"><span data-stu-id="087c1-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="087c1-121">Nel campo **Nr. conto** selezionare il conto bancario da cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="087c1-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="087c1-122">Nel campo **Importo** immettere la quantità nella valuta del conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="087c1-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="087c1-123">Immettere gli importi in Avere con un segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="087c1-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="087c1-124">Immettere gli importi in Dare senza il segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="087c1-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="087c1-125">Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="087c1-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="087c1-126">Nel campo **Nr. contropartita** selezionare il conto bancario a cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="087c1-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="087c1-127">Nella seconda riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.</span><span class="sxs-lookup"><span data-stu-id="087c1-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="087c1-128">Nel campo **Nr. conto** selezionare il conto bancario a cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="087c1-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="087c1-129">Nel campo **Importo** immettere la quantità nella valuta del conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="087c1-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="087c1-130">Immettere gli importi in Avere con un segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="087c1-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="087c1-131">Immettere gli importi in Dare senza il segno meno (-).</span><span class="sxs-lookup"><span data-stu-id="087c1-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="087c1-132">Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="087c1-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="087c1-133">Nel campo **Nr. contropartita** selezionare il conto bancario da cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="087c1-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="087c1-134">Se i tassi di cambio utilizzati nelle registrazioni sono diversi dai tassi riportati nella finestra **Tassi di cambio valuta**, compilare una terza riga per il guadagno o la perdita nel tasso di cambio.</span><span class="sxs-lookup"><span data-stu-id="087c1-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="087c1-135">Immettere **Conto C/G** nel campo **Tipo conto**.</span><span class="sxs-lookup"><span data-stu-id="087c1-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="087c1-136">Nel campo **Nr. conto** immettere il numero di conto C/G per i guadagni o le perdite nel tasso di cambio.</span><span class="sxs-lookup"><span data-stu-id="087c1-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="087c1-137">Immettere utile o perdita in **Importo** campo con o senza un segno meno per i crediti e debiti rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="087c1-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="087c1-138">Effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="087c1-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="087c1-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="087c1-139">See Also</span></span>
[<span data-ttu-id="087c1-140">Gestione di conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="087c1-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="087c1-141">Impostazione delle attività bancarie</span><span class="sxs-lookup"><span data-stu-id="087c1-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="087c1-142">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="087c1-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="087c1-143">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="087c1-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

