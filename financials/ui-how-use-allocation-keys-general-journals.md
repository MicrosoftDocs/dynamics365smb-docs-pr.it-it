---
title: Utilizzare le chiavi di allocazione nelle registrazioni COGE | Documenti Microsoft
description: "Informazioni sul modo in cui è possibile utilizzare le chiavi di allocazione nelle registrazioni."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ee3e0f325623666eb720e3cc2656cfd1f6332eb
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="82071-103">Utilizzare le chiavi di allocazione nelle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="82071-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="82071-104">È possibile assegnare un movimento in una registrazione generale a più conti diversi, quando tale registrazione viene contabilizzata.</span><span class="sxs-lookup"><span data-stu-id="82071-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="82071-105">L'allocazione può essere effettuata per quantità, percentuale o importo.</span><span class="sxs-lookup"><span data-stu-id="82071-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="82071-106">Per impostare le chiavi di allocazione</span><span class="sxs-lookup"><span data-stu-id="82071-106">To set up allocation keys</span></span>
1. <span data-ttu-id="82071-107">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Reg. periodiche generali**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="82071-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="82071-108">Scegliere il campo **Nome batch** per aprire la finestra **Batch registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="82071-108">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="82071-109">È possibile modificare le allocazioni in un batch esistente nell'elenco o creare un nuovo batch con le allocazioni.</span><span class="sxs-lookup"><span data-stu-id="82071-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="82071-110">Per creare un nuovo batch, scegliere l'azione **Nuovo** e andare al passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="82071-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="82071-111">Per modificare le allocazioni di registrazioni esistenti, selezionare le registrazioni e andare al passaggio 7.</span><span class="sxs-lookup"><span data-stu-id="82071-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="82071-112">Nel campo **Nome** immettere un nome per il batch, ad esempio PULIZIE.</span><span class="sxs-lookup"><span data-stu-id="82071-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="82071-113">Nel campo **Descrizione** immettere una descrizione, ad esempio Registrazioni spese pulizie.</span><span class="sxs-lookup"><span data-stu-id="82071-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="82071-114">Al termine, chiudere la finestra.</span><span class="sxs-lookup"><span data-stu-id="82071-114">When you are done, close the window.</span></span> <span data-ttu-id="82071-115">Verrà visualizzata una nuova registrazione periodica vuota.</span><span class="sxs-lookup"><span data-stu-id="82071-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="82071-116">Compilare i campi nella riga.</span><span class="sxs-lookup"><span data-stu-id="82071-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="82071-117">Scegliere l'azione **Allocazioni**.</span><span class="sxs-lookup"><span data-stu-id="82071-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="82071-118">Aggiungere una riga per ciascuna allocazione.</span><span class="sxs-lookup"><span data-stu-id="82071-118">Add a line for each allocation.</span></span> <span data-ttu-id="82071-119">È necessario compilare il campo **Allocazione %**, **Quantità allocazione** o **Importo**.</span><span class="sxs-lookup"><span data-stu-id="82071-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="82071-120">È necessario compilare anche il campo **Nr. conto** e, se si sta allocando la transazione tra dimensioni globali, anche i campi delle dimensioni globali.</span><span class="sxs-lookup"><span data-stu-id="82071-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="82071-121">Se in una riga è stata immessa una percentuale, il valore del campo **Importo** viene calcolato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="82071-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="82071-122">Questi importi hanno il segno opposto rispetto all'importo totale nel campo **Importo** delle registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="82071-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="82071-123">Dopo aver immesso le righe di allocazione, scegliere **OK** per tornare alla finestra **Reg. periodiche generali**.</span><span class="sxs-lookup"><span data-stu-id="82071-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="82071-124">Il campo **Importo allocato (VL)** viene compilato e corrisponde al campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="82071-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="82071-125">Effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="82071-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="82071-126">Per modificare una chiave di allocazione già impostata</span><span class="sxs-lookup"><span data-stu-id="82071-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="82071-127">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Reg. periodiche generali**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="82071-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="82071-128">Nella finestra **Registrazioni periodiche generali** selezionare le registrazioni con l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="82071-128">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="82071-129">Selezionare la riga con l'allocazione e scegliere l'azione **Allocazioni**.</span><span class="sxs-lookup"><span data-stu-id="82071-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="82071-130">Cambiare i campi pertinenti e quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="82071-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="82071-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82071-131">See Also</span></span>
[<span data-ttu-id="82071-132">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="82071-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="82071-133">Contabilizzazione dei documenti e delle registrazioni</span><span class="sxs-lookup"><span data-stu-id="82071-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="82071-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82071-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

