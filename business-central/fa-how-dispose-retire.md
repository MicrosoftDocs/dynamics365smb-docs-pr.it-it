---
title: Cessione o ritiro dei cespiti| Documenti Microsoft
description: È necessario registrare un valore di cessione quando si scarta, si vende o si ritira un cespite.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 16d052c67a2d9b5513e9dac901dfeddce0527512
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749420"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="c2e3c-103">Smaltimento o ritiro dei cespiti</span><span class="sxs-lookup"><span data-stu-id="c2e3c-103">Dispose of or Retire Fixed Assets</span></span>

<span data-ttu-id="c2e3c-104">In caso di vendita o cessione di un cespite, occorre registrare il valore di cessione per calcolare e registrare il guadagno o la perdita.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="c2e3c-105">L'ultimo movimento registrato per un cespite deve essere un movimento di cessione.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="c2e3c-106">In caso di cessione parziale di un cespite è possibile registrare più di un movimento di cessione.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="c2e3c-107">Il totale di tutti gli importi di cessione registrati deve essere un importo in Avere.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="c2e3c-108">In caso di cessione di un cespite in cambio di un altro cespite, occorre registrare sia la vendita del cespite precedente (cessione) sia l'acquisto del nuovo (acquisizione).</span><span class="sxs-lookup"><span data-stu-id="c2e3c-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="c2e3c-109">Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="c2e3c-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="c2e3c-110">I seguenti passaggi presuppongono che le categorie di registrazione pertinenti siano già state impostate nella pagina **Categorie registrazione cespiti**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-110">The following steps assume that you have already set up the relevant posting groups in the **FA Posting Groups** page.</span></span> <span data-ttu-id="c2e3c-111">Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="c2e3c-111">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="c2e3c-112">Per registrare una cessione tramite Registrazioni Cespiti in C/G</span><span class="sxs-lookup"><span data-stu-id="c2e3c-112">To post a disposal from the fixed asset G/L journal</span></span>

1. <span data-ttu-id="c2e3c-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni cespiti in C/G** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c2e3c-114">Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-114">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="c2e3c-115">Nel campo **Tipo reg. cespite** scegliere **Cessione**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-115">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="c2e3c-116">Scegliere l'azione **Inserisci conto cespiti**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-116">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="c2e3c-117">Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della cessione.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-117">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c2e3c-118">Il passaggio 4 funziona solo se è stato impostato quanto segue: nella pagina **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite, il campo **Conto cessione** contiene il conto di addebito contabilità generale e il campo **Conto saldo cessione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-118">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="c2e3c-119">Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="c2e3c-119">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="c2e3c-120">Scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="c2e3c-121">In caso di vendita o di cessione parziale di un cespite occorre suddividere il cespite prima di registrare la transazione di cessione.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-121">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="c2e3c-122">Per ulteriori informazioni, vedere [Trasferimento, divisione o raggruppamento dei cespiti](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="c2e3c-122">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="c2e3c-123">Per visualizzare i movimenti contabili di cessione</span><span class="sxs-lookup"><span data-stu-id="c2e3c-123">To view disposal ledger entries</span></span>
<span data-ttu-id="c2e3c-124">In caso di vendita o di cessione di un cespite, il valore di cessione viene registrato nella contabilità generale dove è possibile visualizzare il risultato.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-124">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="c2e3c-125">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c2e3c-126">Selezionare il cespite di cui visualizzare i movimenti, quindi scegliere l'azione **Registri beni ammortizzabili**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-126">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="c2e3c-127">Selezionare il registro beni ammortizzabili di cui visualizzare i movimenti, quindi scegliere l'azione **Movimenti contabili**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-127">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="c2e3c-128">Selezionare una riga con **Cessione** nel campo **Categoria reg. cespite** e scegliere l'azione **Trova movimenti**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-128">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Find Entries** action.</span></span>  
5. <span data-ttu-id="c2e3c-129">Nella pagina **Trova movimenti** scegliere la riga del movimento contabile e fare clic sull'azione **Mostra movimenti correlati**.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-129">On the **Find Entries** page, select the general ledger entry line, and then choose the **Show Related Entries** action.</span></span>  

<span data-ttu-id="c2e3c-130">Viene visualizzata la pagina **Movimenti C/G** in cui è possibile visualizzare i movimenti che hanno comportato la registrazione di cessione.</span><span class="sxs-lookup"><span data-stu-id="c2e3c-130">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2e3c-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c2e3c-131">See Also</span></span>

[<span data-ttu-id="c2e3c-132">Cespiti</span><span class="sxs-lookup"><span data-stu-id="c2e3c-132">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="c2e3c-133">Impostazione di cespiti</span><span class="sxs-lookup"><span data-stu-id="c2e3c-133">Setting Up Fixed Assets</span></span>](fa-setup.md)  
<span data-ttu-id="c2e3c-134">[Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="c2e3c-134">[To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
[<span data-ttu-id="c2e3c-135">Finanze</span><span class="sxs-lookup"><span data-stu-id="c2e3c-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="c2e3c-136">Introduzione</span><span class="sxs-lookup"><span data-stu-id="c2e3c-136">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="c2e3c-137">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2e3c-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c2e3c-138">Trova movimenti</span><span class="sxs-lookup"><span data-stu-id="c2e3c-138">Find Entries</span></span>](ui-find-entries.md)  
