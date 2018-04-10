---
title: Cessione o ritiro dei cespiti| Documenti Microsoft
description: "È necessario registrare un valore di cessione quando si scarta, si vende o si ritira un cespite."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: f2ccb2c7c020220383591c468b9f0729722ea1b8
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="af4b6-103">Smaltimento o ritiro dei cespiti</span><span class="sxs-lookup"><span data-stu-id="af4b6-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="af4b6-104">In caso di vendita o cessione di un cespite, occorre registrare il valore di cessione per calcolare e registrare il guadagno o la perdita.</span><span class="sxs-lookup"><span data-stu-id="af4b6-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="af4b6-105">L'ultimo movimento registrato per un cespite deve essere un movimento di cessione.</span><span class="sxs-lookup"><span data-stu-id="af4b6-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="af4b6-106">In caso di cessione parziale di un cespite è possibile registrare più di un movimento di cessione.</span><span class="sxs-lookup"><span data-stu-id="af4b6-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="af4b6-107">Il totale di tutti gli importi di cessione registrati deve essere un importo in Avere.</span><span class="sxs-lookup"><span data-stu-id="af4b6-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="af4b6-108">In caso di cessione di un cespite in cambio di un altro cespite, occorre registrare sia la vendita del cespite precedente (cessione) sia l'acquisto del nuovo (acquisizione).</span><span class="sxs-lookup"><span data-stu-id="af4b6-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="af4b6-109">Per ulteriori informazioni, vedere [Acquisire i cespiti](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="af4b6-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="af4b6-110">Per registrare una cessione tramite Registrazioni Cespiti in C/G</span><span class="sxs-lookup"><span data-stu-id="af4b6-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="af4b6-111">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="af4b6-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="af4b6-112">Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="af4b6-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="af4b6-113">Nel campo **Tipo reg. cespite** scegliere **Cessione**.</span><span class="sxs-lookup"><span data-stu-id="af4b6-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="af4b6-114">Scegliere l'azione **Inserisci conto cespiti**.</span><span class="sxs-lookup"><span data-stu-id="af4b6-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="af4b6-115">Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della cessione.</span><span class="sxs-lookup"><span data-stu-id="af4b6-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="af4b6-116">Il passaggio 4 funziona solo se è stato impostato quanto segue: nella finestra **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite, il campo **Conto cessione** contiene il conto di addebito contabilità generale e il campo **Conto saldo cessione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione.</span><span class="sxs-lookup"><span data-stu-id="af4b6-116">Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="af4b6-117">Per ulteriori informazioni, vedere Impostare la sezione "Per impostare categorie di registrazione cespiti" in [Impostare i valori generali per i cespiti](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="af4b6-117">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="af4b6-118">Scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="af4b6-118">Choose the **Post** action.</span></span>  

<span data-ttu-id="af4b6-119">In caso di vendita o di cessione parziale di un cespite occorre suddividere il cespite prima di registrare la transazione di cessione.</span><span class="sxs-lookup"><span data-stu-id="af4b6-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="af4b6-120">Per ulteriori informazioni, vedere [Trasferimento, divisione o raggruppamento dei cespiti](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="af4b6-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="af4b6-121">Per visualizzare i movimenti contabili di cessione</span><span class="sxs-lookup"><span data-stu-id="af4b6-121">To view disposal ledger entries</span></span>
<span data-ttu-id="af4b6-122">In caso di vendita o di cessione di un cespite, il valore di cessione viene registrato nella contabilità generale dove è possibile visualizzare il risultato.</span><span class="sxs-lookup"><span data-stu-id="af4b6-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="af4b6-123">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cespiti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="af4b6-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="af4b6-124">Selezionare il cespite di cui visualizzare i movimenti, quindi scegliere l'azione **Registri beni ammortizzabili**.</span><span class="sxs-lookup"><span data-stu-id="af4b6-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="af4b6-125">Selezionare il registro beni ammortizzabili di cui visualizzare i movimenti, quindi scegliere l'azione **Movimenti contabili**.</span><span class="sxs-lookup"><span data-stu-id="af4b6-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="af4b6-126">Selezionare una riga con **Cessione** nel campo **Categoria reg. cespite** e scegliere l'azione **Naviga**.</span><span class="sxs-lookup"><span data-stu-id="af4b6-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="af4b6-127">Nella finestra **Naviga** scegliere la riga del movimento contabile e fare clic sull'azione **Mostra**.</span><span class="sxs-lookup"><span data-stu-id="af4b6-127">In the **Navigate** window, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="af4b6-128">Viene visualizzata la finestra **Movimenti C/G** in cui è possibile visualizzare i movimenti che hanno comportato la registrazione di cessione.</span><span class="sxs-lookup"><span data-stu-id="af4b6-128">The **General Ledger Entries** window opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af4b6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af4b6-129">See Also</span></span>
[<span data-ttu-id="af4b6-130">Cespiti</span><span class="sxs-lookup"><span data-stu-id="af4b6-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="af4b6-131">Impostazione di cespiti</span><span class="sxs-lookup"><span data-stu-id="af4b6-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="af4b6-132">Finanze</span><span class="sxs-lookup"><span data-stu-id="af4b6-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="af4b6-133">Introduzione</span><span class="sxs-lookup"><span data-stu-id="af4b6-133">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="af4b6-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af4b6-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

