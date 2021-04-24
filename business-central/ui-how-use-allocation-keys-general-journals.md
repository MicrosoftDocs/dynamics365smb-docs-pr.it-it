---
title: Utilizzare le chiavi di allocazione nelle registrazioni COGE | Documenti Microsoft
description: Informazioni sul modo in cui è possibile utilizzare le chiavi di allocazione nelle registrazioni.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2760b53bfa1e277d4c4763810d580f5b66a223dc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772256"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="0d1dc-103">Utilizzare le chiavi di allocazione nelle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="0d1dc-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="0d1dc-104">È possibile assegnare un movimento in una registrazione generale a più conti diversi, quando tale registrazione viene contabilizzata.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="0d1dc-105">L'allocazione può essere effettuata per quantità, percentuale o importo.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="0d1dc-106">Per impostare le chiavi di allocazione</span><span class="sxs-lookup"><span data-stu-id="0d1dc-106">To set up allocation keys</span></span>
1. <span data-ttu-id="0d1dc-107">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni periodiche generali** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d1dc-108">Scegliere il campo **Nome batch** per aprire la pagina **Batch registrazioni COGE**.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="0d1dc-109">È possibile modificare le allocazioni in un batch esistente nell'elenco o creare un nuovo batch con le allocazioni.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="0d1dc-110">Per creare un nuovo batch, scegliere l'azione **Nuovo** e andare al passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="0d1dc-111">Per modificare le allocazioni di registrazioni esistenti, selezionare le registrazioni e andare al passaggio 7.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="0d1dc-112">Nel campo **Nome** immettere un nome per il batch, ad esempio PULIZIE.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="0d1dc-113">Nel campo **Descrizione** immettere una descrizione, ad esempio Registrazioni spese pulizie.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="0d1dc-114">Al termine, chiudere la pagina.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-114">When you are done, close the page.</span></span> <span data-ttu-id="0d1dc-115">Verrà visualizzata una nuova registrazione periodica vuota.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="0d1dc-116">Compilare i campi nella riga.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="0d1dc-117">Scegliere l'azione **Allocazioni**.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="0d1dc-118">Aggiungere una riga per ciascuna allocazione.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-118">Add a line for each allocation.</span></span> <span data-ttu-id="0d1dc-119">È necessario compilare il campo **Allocazione %**, **Quantità allocazione** o **Importo**.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="0d1dc-120">È necessario compilare anche il campo **Nr. conto** e, se si sta allocando la transazione tra dimensioni globali, anche i campi delle dimensioni globali.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="0d1dc-121">Se in una riga è stata immessa una percentuale, il valore del campo **Importo** viene calcolato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="0d1dc-122">Questi importi hanno il segno opposto rispetto all'importo totale nel campo **Importo** delle registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="0d1dc-123">Dopo aver immesso le righe di allocazione, scegliere **OK** per tornare alla pagina **Reg. periodiche generali**.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="0d1dc-124">Il campo **Importo allocato (VL)** viene compilato e corrisponde al campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="0d1dc-125">Effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="0d1dc-126">Per modificare una chiave di allocazione già impostata</span><span class="sxs-lookup"><span data-stu-id="0d1dc-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="0d1dc-127">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni periodiche generali** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d1dc-128">Nella pagina **Registrazioni periodiche generali** selezionare le registrazioni con l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="0d1dc-129">Selezionare la riga con l'allocazione e scegliere l'azione **Allocazioni**.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="0d1dc-130">Cambiare i campi pertinenti e quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d1dc-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d1dc-131">See Also</span></span>
[<span data-ttu-id="0d1dc-132">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="0d1dc-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="0d1dc-133">Contabilizzazione dei documenti e delle registrazioni</span><span class="sxs-lookup"><span data-stu-id="0d1dc-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="0d1dc-134">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d1dc-134">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]