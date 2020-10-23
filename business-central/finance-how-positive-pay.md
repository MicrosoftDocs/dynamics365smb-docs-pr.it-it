---
title: Esportare file Positive Pay| Documenti Microsoft
description: Assicurarsi che la banca compensi solo gli assegni e gli importi convalidati tramite l'esportazione di file Positive Pay che contengano informazioni sul fornitore e pagamento.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1e75a5541654a6577417a37c0cef23302b37b649
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916953"
---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="b3ccb-103">Esportare un file Positive Pay</span><span class="sxs-lookup"><span data-stu-id="b3ccb-103">Export a Positive Pay File</span></span>
<span data-ttu-id="b3ccb-104">Per assicurarsi che la banca compensi solo gli assegni e gli importi convalidati, è possibile esportare un file Positive Pay con informazioni su fornitore, numero di assegno e importo del pagamento da inviare alla banca per riferimento quando si elaborano i pagamenti.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="b3ccb-105">è preconfigurato per supportare i file Positive Pay per Bank of America e City Bank.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-105">is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="b3ccb-106">Per impostare un conto bancario per i file Positive Pay</span><span class="sxs-lookup"><span data-stu-id="b3ccb-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="b3ccb-107">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="b3ccb-108">Aprire la scheda della banca per cui si desidera utilizzare il Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="b3ccb-109">Nel campo **Codice esportazione Positive Pay** immettere POSPAYBANK.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="b3ccb-110">Chiudere la pagina.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-110">Close the page.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="b3ccb-111">Per esportare un file Positive Pay</span><span class="sxs-lookup"><span data-stu-id="b3ccb-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="b3ccb-112">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="b3ccb-113">Selezionare il conto bancario per cui si desidera esportare un file Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="b3ccb-114">Scegliere l'opzione **Esportazione Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="b3ccb-115">Verrà visualizzata la pagina **Esportazione Positive Pay** che mostra i pagamenti che sono stati effettuati per il conto bancario dalla data dell'ultimo caricamento, come mostrato nei campi **Data ultimo caricamento** e **Data ultimo caricamento**.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-115">The **Positive Pay Export** page opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="b3ccb-116">Nel campo **Data limite caricamento** specificare una data prima della quale i pagamenti non sono inclusi nel file esportato.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="b3ccb-117">Scegliere l'azione **Esporta**.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="b3ccb-118">Nella pagina **Esporta file** scegliere il pulsante **Salva**, quindi salvare il file in un percorso appropriato.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-118">On the **Export File** page, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="b3ccb-119">Caricare il file nel sito elettronico della banca.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="b3ccb-120">Annotare o copiare il numero di conferma visualizzato quando il file viene caricato.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="b3ccb-121">Per visualizzare i record Positive Pay esportati</span><span class="sxs-lookup"><span data-stu-id="b3ccb-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="b3ccb-122">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="b3ccb-123">Selezionare il conto bancario per cui si desidera visualizzare i record di esportazione Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="b3ccb-124">Scegliere l'azione **Movimenti Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="b3ccb-125">Nella pagina **Movimenti Positive Pay** è possibile visualizzare tutti i record di esportazione Positive Pay per il conto corrente bancario.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-125">On the **Positive Pay Entries** page, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="b3ccb-126">Nel campo **Numero di conferma** immettere per ogni record esportare il numero di conferma che si riceve quando il caricamento del file alla banca è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="b3ccb-127">Per visualizzare le righe di pagamento, scegliere l'azione **Dettagli movimenti Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="b3ccb-128">Per riesportare file Positive Pay</span><span class="sxs-lookup"><span data-stu-id="b3ccb-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="b3ccb-129">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Conti correnti bancari** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="b3ccb-130">Selezionare il conto bancario per cui si desidera riesportare i file Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="b3ccb-131">Scegliere l'azione **Movimenti Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="b3ccb-132">Selezionare la riga per il file di esportazione Positive Pay da riesportare.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="b3ccb-133">Nella pagina **Movimenti Positive Pay** selezionare l'azione **Riesporta Positive Pay su file**.</span><span class="sxs-lookup"><span data-stu-id="b3ccb-133">On the **Positive Pay Entries** page, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3ccb-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3ccb-134">See Also</span></span>
[<span data-ttu-id="b3ccb-135">Finanze</span><span class="sxs-lookup"><span data-stu-id="b3ccb-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="b3ccb-136">Impostazione di dati finanziari</span><span class="sxs-lookup"><span data-stu-id="b3ccb-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="b3ccb-137">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="b3ccb-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="b3ccb-138">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3ccb-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
