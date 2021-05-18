---
title: Trasferimento di fondi bancari
description: È possibile trasferire gli importi da un conto corrente bancario a un altro, incluse le valute diverse, tramite la registrazione della transazione nelle registrazioni COGE.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985389"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="14c23-103">Trasferimento di fondi bancari</span><span class="sxs-lookup"><span data-stu-id="14c23-103">Transfer Bank Funds</span></span>

<span data-ttu-id="14c23-104">Talvolta, può anche essere necessario effettuare un bonifico da un conto corrente bancario in [!INCLUDE[prod_short](includes/prod_short.md)] a un altro.</span><span class="sxs-lookup"><span data-stu-id="14c23-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="14c23-105">A tale scopo, è necessario registrare la transazione nella pagina **Registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="14c23-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="14c23-106">L'attività varia a seconda se i conti correnti bancari utilizzano la stessa valuta o valute diverse.</span><span class="sxs-lookup"><span data-stu-id="14c23-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="14c23-107">Per registrare un bonifico tra conti correnti bancari con lo stesso codice valuta</span><span class="sxs-lookup"><span data-stu-id="14c23-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="14c23-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="14c23-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="14c23-109">In una riga di registrazioni compilare i campi **Data di registrazione** e **Nr. documento**.</span><span class="sxs-lookup"><span data-stu-id="14c23-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="14c23-110">Nel campo **Tipo conto** selezionare **Conti C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="14c23-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="14c23-111">Nel campo **Nr. conto** selezionare la banca da cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="14c23-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="14c23-112">Immettere l'importo da traferire nel campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="14c23-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="14c23-113">Successivamente, è necessario specificare il conto di contropartita.</span><span class="sxs-lookup"><span data-stu-id="14c23-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="14c23-114">Se non riesci a visualizzare i campi pertinenti, scegli l'azione **Mostra più colonne** per visualizzare tutti i campi disponibili.</span><span class="sxs-lookup"><span data-stu-id="14c23-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="14c23-115">Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.</span><span class="sxs-lookup"><span data-stu-id="14c23-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="14c23-116">Nel campo **Nr. contropartita** selezionare il conto bancario a cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="14c23-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="14c23-117">Effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="14c23-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="14c23-118">Per registrare un bonifico tra conti correnti bancari con codici valuta diversi</span><span class="sxs-lookup"><span data-stu-id="14c23-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="14c23-119">Per trasferire i fondi tra conti correnti bancari che utilizzano valute diverse, è necessario inserire due righe di registrazioni COGE.</span><span class="sxs-lookup"><span data-stu-id="14c23-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="14c23-120">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="14c23-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="14c23-121">Creare due righe di registrazione e compilare i campi **Data di registrazione** e **Nr. documento**.</span><span class="sxs-lookup"><span data-stu-id="14c23-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="14c23-122">Nella prima riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.</span><span class="sxs-lookup"><span data-stu-id="14c23-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="14c23-123">Nel campo **Nr. conto** selezionare il conto bancario da cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="14c23-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="14c23-124">Nel campo **Importo** immettere la quantità nella valuta del C/C bancario con o senza un segno meno.</span><span class="sxs-lookup"><span data-stu-id="14c23-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="14c23-125">Un importo senza segno è un debito e un importo con un segno meno è un credito.</span><span class="sxs-lookup"><span data-stu-id="14c23-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14c23-126">Alcune società preferiscono effettuare trasferimenti tra conti su righe di registrazione separate.</span><span class="sxs-lookup"><span data-stu-id="14c23-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="14c23-127">Altre società preferiscono registrare tutto su una riga di registrazione utilizzando un conto di contropartita.</span><span class="sxs-lookup"><span data-stu-id="14c23-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="14c23-128">Se non sai cosa fare, rivolgiti al tuo esperto locale.</span><span class="sxs-lookup"><span data-stu-id="14c23-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="14c23-129">Se la tua società preferisce utilizzare un conto di contropartita, imposta il campo **Tipo contropartita** su **Conto bancario** e imposta il campo **Nr contropartita** sul C/C bancario su cui desideri trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="14c23-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="14c23-130">Quindi procedi al passaggio 9 o 10.</span><span class="sxs-lookup"><span data-stu-id="14c23-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="14c23-131">Se la tua società preferisce utilizzare una riga di registrazione separata, vai al passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="14c23-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="14c23-132">Nella seconda riga di registrazioni selezionare **C/C bancario** nel campo **Tipo conto**.</span><span class="sxs-lookup"><span data-stu-id="14c23-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="14c23-133">Nel campo **Nr. conto** selezionare il conto bancario a cui si desidera trasferire i fondi.</span><span class="sxs-lookup"><span data-stu-id="14c23-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="14c23-134">Nel campo **Importo** immettere la quantità nella valuta del C/C bancario con o senza un segno meno.</span><span class="sxs-lookup"><span data-stu-id="14c23-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="14c23-135">Un importo senza segno è un debito e un importo con un segno meno è un credito.</span><span class="sxs-lookup"><span data-stu-id="14c23-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="14c23-136">Se i tassi di cambio utilizzati nelle registrazioni sono diversi da quelli riportati nella pagina **Tassi di cambio valuta**, compila una nuova riga di registrazione per le perdite o gli utili di conversione.</span><span class="sxs-lookup"><span data-stu-id="14c23-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="14c23-137">Immettere **Conto C/G** nel campo **Tipo conto**.</span><span class="sxs-lookup"><span data-stu-id="14c23-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="14c23-138">Nel campo **Nr. conto** immettere il numero di conto C/G per i guadagni o le perdite nel tasso di cambio.</span><span class="sxs-lookup"><span data-stu-id="14c23-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="14c23-139">Immettere le perdite o gli utili di conversione nel campo **Importo** con o senza segno meno.</span><span class="sxs-lookup"><span data-stu-id="14c23-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="14c23-140">Un importo senza segno è un debito e un importo con un segno meno è un credito.</span><span class="sxs-lookup"><span data-stu-id="14c23-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="14c23-141">Effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="14c23-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="14c23-142">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="14c23-142">See Also</span></span>

[<span data-ttu-id="14c23-143">Riconciliazione dei conti correnti bancari</span><span class="sxs-lookup"><span data-stu-id="14c23-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="14c23-144">Impostazione delle attività bancarie</span><span class="sxs-lookup"><span data-stu-id="14c23-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="14c23-145">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="14c23-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="14c23-146">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14c23-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]