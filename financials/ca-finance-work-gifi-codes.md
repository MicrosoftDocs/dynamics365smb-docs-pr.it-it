---
title: Codici GIFI in Canada | Documenti Microsoft
Description: "In Canada, è possibile impostare codici GIFI (General Index of Financial Information) e assegnarli alla registrazione conti"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="39ed1-103">Procedura: Utilizzare i codici GIFI in Canada</span><span class="sxs-lookup"><span data-stu-id="39ed1-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="39ed1-104">Le informazioni fiscali possono includere conti di contabilità generale, report, conti economici, conti patrimoniali e conti profitti/perdite.</span><span class="sxs-lookup"><span data-stu-id="39ed1-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="39ed1-105">Le informazioni fiscali vengono classificate tramite codici.</span><span class="sxs-lookup"><span data-stu-id="39ed1-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="39ed1-106">L'utilizzo dei codici consente al governo di elaborare le informazioni, preparare l'archiviazione elettronica e convalidare le informazioni fiscali elettronicamente.</span><span class="sxs-lookup"><span data-stu-id="39ed1-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="39ed1-107">L'utilizzo dei codici consente anche alle organizzazioni statistiche di lavorare in modo più efficiente, in quanto le informazioni finanziarie sono accessibili più facilmente.</span><span class="sxs-lookup"><span data-stu-id="39ed1-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="39ed1-108">Per ulteriori informazioni, vedere il [il sito Web della Canada Revenue Agency](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="39ed1-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="39ed1-109">L'agenzia Canada Revenue Agency utilizza i codici General Index of Financial Information (GIFI) per raccogliere, convalidare ed elaborare elettronicamente le informazioni finanziarie e fiscali.</span><span class="sxs-lookup"><span data-stu-id="39ed1-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="39ed1-110">È consigliabile assegnare i codici GIFI solo ai conti di registrazione, in modo che tutti i totali vengano calcolati dal software fiscale.</span><span class="sxs-lookup"><span data-stu-id="39ed1-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="39ed1-111">Quando un conto è associato a un codice GIFI, viene riportato all'agenzia delle entrate in base a questo campo codice.</span><span class="sxs-lookup"><span data-stu-id="39ed1-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="39ed1-112">Più conti possono avere tutti lo stesso codice GIFI, ma ogni conto può avere un solo codice GIFI.</span><span class="sxs-lookup"><span data-stu-id="39ed1-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="39ed1-113">È possibile esportare le informazioni sui saldi in base al codice GIFI e salvare il file esportato in Excel, questa procedura è utile per il trasferimento delle informazioni al software fiscale.</span><span class="sxs-lookup"><span data-stu-id="39ed1-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="39ed1-114">Per impostare i codici GIFI</span><span class="sxs-lookup"><span data-stu-id="39ed1-114">To set up GIFI codes</span></span>
<span data-ttu-id="39ed1-115">In Dynamics NAV, è necessario impostare i codici GIFI per conti di contabilità generale, report, conti economici, conti patrimoniali e conti profitti/perdite.</span><span class="sxs-lookup"><span data-stu-id="39ed1-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="39ed1-116">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici GIFI**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="39ed1-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="39ed1-117">Nella finestra **Codici GIFI** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="39ed1-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="39ed1-118">Impostare codici GIFI compilando i campi.</span><span class="sxs-lookup"><span data-stu-id="39ed1-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="39ed1-119">Per associare i codici GIFI con i conti C/G</span><span class="sxs-lookup"><span data-stu-id="39ed1-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="39ed1-120">Per creare un report con informazioni finanziarie in base al codice GIFI, ogni codice GIFI deve essere associato ai conti appropriati nel piano dei conti.</span><span class="sxs-lookup"><span data-stu-id="39ed1-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="39ed1-121">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="39ed1-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="39ed1-122">Selezionare un conto di contabilità generale e scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="39ed1-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="39ed1-123">Nella Scheda dettaglio **Contabilità industriale** nel campo **Codice GIFI** selezionare un codice GIFI appropriato.</span><span class="sxs-lookup"><span data-stu-id="39ed1-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="39ed1-124">Per visualizzare i saldi dei conti utilizzando il report con codice GIFI</span><span class="sxs-lookup"><span data-stu-id="39ed1-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="39ed1-125">È possibile analizzare i saldi del conto in base al codice GIFI utilizzando il report **Saldi dei conti per codice GIFI**.</span><span class="sxs-lookup"><span data-stu-id="39ed1-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="39ed1-126">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici GIFI**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="39ed1-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="39ed1-127">Specificare cosa includere nel report compilando i campi.</span><span class="sxs-lookup"><span data-stu-id="39ed1-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="39ed1-128">Selezionare il pulsante **Stampa** o **Anteprima**.</span><span class="sxs-lookup"><span data-stu-id="39ed1-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="39ed1-129">Per esportare le informazioni sui saldi in base ai codici GIFI</span><span class="sxs-lookup"><span data-stu-id="39ed1-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="39ed1-130">È possibile esportare le informazioni sui saldi in base ai codici GIFI e salvare il file esportato in Excel.</span><span class="sxs-lookup"><span data-stu-id="39ed1-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="39ed1-131">È possibile modificare, salvare, o eliminare il file.</span><span class="sxs-lookup"><span data-stu-id="39ed1-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="39ed1-132">È possibile utilizzare il file per trasferire le informazioni al software fiscale.</span><span class="sxs-lookup"><span data-stu-id="39ed1-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="39ed1-133">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici GIFI**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="39ed1-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="39ed1-134">Specificare gli elementi da esportare in Excel compilando i campi.</span><span class="sxs-lookup"><span data-stu-id="39ed1-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="39ed1-135">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="39ed1-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="39ed1-136">Il file di Excel ha le seguenti caratteristiche:</span><span class="sxs-lookup"><span data-stu-id="39ed1-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="39ed1-137">Il saldo è arrotondato alla percentuale più vicina, ma il valore della cella mantiene la stessa percentuale come in contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="39ed1-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="39ed1-138">I numeri negativi sono rappresentati come numero positivo tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="39ed1-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="39ed1-139">Di conseguenza, -123 è rappresentato come (123).</span><span class="sxs-lookup"><span data-stu-id="39ed1-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="39ed1-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39ed1-140">See Also</span></span>
<span data-ttu-id="39ed1-141">[Finanze](finance.md) </span><span class="sxs-lookup"><span data-stu-id="39ed1-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="39ed1-142">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="39ed1-142">Setting Up Finance</span></span>](finance-setup-finance.md)

