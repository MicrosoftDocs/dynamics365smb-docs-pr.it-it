---
title: 'Procedura: Utilizzare le chiavi di allocazione nelle registrazioni COGE | Documenti Microsoft'
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bbacf9b5634d51478dd4d54ac4b587ea9bfaaf99
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-use-allocation-keys-in-general-journals"></a><span data-ttu-id="4d012-103">Procedura: Utilizzare le chiavi di allocazione nelle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d012-103">How to: Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="4d012-104">È possibile assegnare un movimento in una registrazione generale a più conti diversi, quando tale registrazione viene contabilizzata.</span><span class="sxs-lookup"><span data-stu-id="4d012-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="4d012-105">L'allocazione può essere effettuata per quantità, percentuale o importo.</span><span class="sxs-lookup"><span data-stu-id="4d012-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="4d012-106">Per impostare le chiavi di allocazione</span><span class="sxs-lookup"><span data-stu-id="4d012-106">To set up allocation keys</span></span>
1. <span data-ttu-id="4d012-107">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Reg. periodiche generali**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="4d012-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="4d012-108">Scegliere il campo **Nome batch** per aprire la finestra **Batch registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="4d012-108">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="4d012-109">È possibile modificare le allocazioni in un batch esistente nell'elenco o creare un nuovo batch con le allocazioni.</span><span class="sxs-lookup"><span data-stu-id="4d012-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="4d012-110">Per creare un nuovo batch, scegliere l'azione **Nuovo** e andare al passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="4d012-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="4d012-111">Per modificare le allocazioni di registrazioni esistenti, selezionare le registrazioni e andare al passaggio 7.</span><span class="sxs-lookup"><span data-stu-id="4d012-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="4d012-112">Nel campo **Nome** immettere un nome per il batch, ad esempio PULIZIE.</span><span class="sxs-lookup"><span data-stu-id="4d012-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="4d012-113">Nel campo **Descrizione** immettere una descrizione, ad esempio Registrazioni spese pulizie.</span><span class="sxs-lookup"><span data-stu-id="4d012-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="4d012-114">Al termine, chiudere la finestra.</span><span class="sxs-lookup"><span data-stu-id="4d012-114">When you are done, close the window.</span></span> <span data-ttu-id="4d012-115">Verrà visualizzata una nuova registrazione periodica vuota.</span><span class="sxs-lookup"><span data-stu-id="4d012-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="4d012-116">Compilare i campi nella riga.</span><span class="sxs-lookup"><span data-stu-id="4d012-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="4d012-117">Scegliere l'azione **Allocazioni**.</span><span class="sxs-lookup"><span data-stu-id="4d012-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="4d012-118">Aggiungere una riga per ciascuna allocazione.</span><span class="sxs-lookup"><span data-stu-id="4d012-118">Add a line for each allocation.</span></span> <span data-ttu-id="4d012-119">È necessario compilare il campo **Allocazione %**, **Quantità allocazione** o **Importo**.</span><span class="sxs-lookup"><span data-stu-id="4d012-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="4d012-120">È inoltre necessario compilare il campo **Nr. conto**</span><span class="sxs-lookup"><span data-stu-id="4d012-120">You must also fill in the **Account No.**</span></span> <span data-ttu-id="4d012-121">e, se si sta allocando la transazione tra dimensioni globali, anche i campi delle dimensioni globali.</span><span class="sxs-lookup"><span data-stu-id="4d012-121">field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="4d012-122">Se in una riga è stata immessa una percentuale, il valore del campo **Importo** viene calcolato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4d012-122">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="4d012-123">Questi importi hanno il segno opposto rispetto all'importo totale nel campo **Importo** delle registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="4d012-123">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="4d012-124">Dopo aver immesso le righe di allocazione, scegliere **OK** per tornare alla finestra **Reg. periodiche generali**.</span><span class="sxs-lookup"><span data-stu-id="4d012-124">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="4d012-125">Il campo **Importo allocato (VL)** viene compilato e corrisponde al campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="4d012-125">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="4d012-126">Effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="4d012-126">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="4d012-127">Per modificare una chiave di allocazione già impostata</span><span class="sxs-lookup"><span data-stu-id="4d012-127">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="4d012-128">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Reg. periodiche generali**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="4d012-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="4d012-129">Nella finestra **Registrazioni periodiche generali** selezionare le registrazioni con l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="4d012-129">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="4d012-130">Selezionare la riga con l'allocazione e scegliere l'azione **Allocazioni**.</span><span class="sxs-lookup"><span data-stu-id="4d012-130">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="4d012-131">Cambiare i campi pertinenti e quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d012-131">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d012-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d012-132">See Also</span></span>
[<span data-ttu-id="4d012-133">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="4d012-133">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="4d012-134">Contabilizzazione dei documenti e delle registrazioni</span><span class="sxs-lookup"><span data-stu-id="4d012-134">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="4d012-135">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4d012-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

