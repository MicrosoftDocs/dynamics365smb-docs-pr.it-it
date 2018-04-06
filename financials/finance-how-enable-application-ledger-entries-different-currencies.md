---
title: Collegare i movimenti in diverse valute| Documenti Microsoft
description: "Se si effettua una vendita in una valuta e si riceve il pagamento in un'altra, è possibile collegare il movimento contabile in più valute."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d98fdf358e387be1d53b188cc05c57108e8592b8
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="54fa2-103">Abilitare il collegamento dei movimenti contabili fornitore in valute diverse</span><span class="sxs-lookup"><span data-stu-id="54fa2-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="54fa2-104">Se si acquista da un fornitore con una valuta e si paga con un'altra valuta, è possibile collegare il pagamento all'acquisto.</span><span class="sxs-lookup"><span data-stu-id="54fa2-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="54fa2-105">In modo analogo, se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile collegare il pagamento alla fattura di vendita.</span><span class="sxs-lookup"><span data-stu-id="54fa2-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="54fa2-106">Nella procedura riportata di seguito viene descritto come configurare questa impostazione per i movimenti contabili fornitori nella finestra **Setup contabilità fornitori e acquisti**.</span><span class="sxs-lookup"><span data-stu-id="54fa2-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="54fa2-107">L'impostazione è simile per i movimenti contabili clienti nella finestra **Setup contabilità clienti e vendite**.</span><span class="sxs-lookup"><span data-stu-id="54fa2-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="54fa2-108">Per abilitare il collegamento dei movimenti contabili fornitore in valute diverse</span><span class="sxs-lookup"><span data-stu-id="54fa2-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="54fa2-109">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup contabilità fornitori e acquisti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="54fa2-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="54fa2-110">Nel campo **Collegamenti tra valute** selezionare una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="54fa2-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="54fa2-111">Opzione</span><span class="sxs-lookup"><span data-stu-id="54fa2-111">Option</span></span> | <span data-ttu-id="54fa2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54fa2-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="54fa2-113">Nessuno</span><span class="sxs-lookup"><span data-stu-id="54fa2-113">None</span></span> |<span data-ttu-id="54fa2-114">Collegamento fra valute non consentito.</span><span class="sxs-lookup"><span data-stu-id="54fa2-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="54fa2-115">UE</span><span class="sxs-lookup"><span data-stu-id="54fa2-115">EMU</span></span> |<span data-ttu-id="54fa2-116">Collegamento fra valute UE consentito</span><span class="sxs-lookup"><span data-stu-id="54fa2-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="54fa2-117">Tutto</span><span class="sxs-lookup"><span data-stu-id="54fa2-117">All</span></span> |<span data-ttu-id="54fa2-118">Collegamento fra tutte le valute consentito</span><span class="sxs-lookup"><span data-stu-id="54fa2-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="54fa2-119">Per impostare i conti C/G per le differenze di arrotondamento di applicazione delle valute</span><span class="sxs-lookup"><span data-stu-id="54fa2-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="54fa2-120">Se movimenti in diverse valute vengono collegati, è necessario impostare il conto di contabilità generale in cui verranno registrate le differenze di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="54fa2-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="54fa2-121">È necessario impostare i conti di contabilità generale prima di completare il task.</span><span class="sxs-lookup"><span data-stu-id="54fa2-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="54fa2-122">Per ulteriori informazioni, vedere [Contabilità generale e piano dei conti](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="54fa2-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="54fa2-123">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Categorie registrazione clienti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="54fa2-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="54fa2-124">Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="54fa2-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="54fa2-125">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Categorie registrazione fornitori**, quindi selezionare il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="54fa2-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="54fa2-126">Nei campi **Conto dare arrot. coll. val.** e **Conto avere arrot. coll. val.** immettere i conti di contabilità generale pertinenti per registrare le differenze di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="54fa2-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="54fa2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54fa2-127">See Also</span></span>
[<span data-ttu-id="54fa2-128">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="54fa2-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="54fa2-129">Gestione della contabilità clienti</span><span class="sxs-lookup"><span data-stu-id="54fa2-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="54fa2-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54fa2-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

