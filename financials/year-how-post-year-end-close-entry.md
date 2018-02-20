---
title: Analizzare e registrare il movimento di chiusura di fine anno | Documenti Microsoft
description: Descrive come aprire le registrazioni specificate nel processo batch Chiudi conto economico, quindi analizzare e registrare il movimento di chiusura di fine anno.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 78039e9387866ce17ff3be5a2ff509545e8439d2
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="43c4f-103">Registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="43c4f-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="43c4f-104">Dopo avere utilizzato il processo batch **Chiudi conto economico** per generare il movimento o i movimenti di chiusura di fine anno, è necessario aprire le registrazioni specificate nel processo batch, quindi analizzare e registrare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="43c4f-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="43c4f-105">Per registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="43c4f-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="43c4f-106">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="43c4f-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="43c4f-107">Nella finestra **Registrazione COGE**, nel campo **Nome batch**, selezionare il batch contenente i movimenti di chiusura.</span><span class="sxs-lookup"><span data-stu-id="43c4f-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="43c4f-108">Analizzare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="43c4f-108">Review the entries.</span></span>
4. <span data-ttu-id="43c4f-109">Per contabilizzare le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="43c4f-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="43c4f-110">Se viene rilevato un errore, viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="43c4f-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="43c4f-111">Se la registrazione avviene correttamente, i movimenti registrati vengono rimossi dalle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="43c4f-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="43c4f-112">Dopo il completamento della registrazione, in ogni conto economico viene registrato un movimento in modo che il relativo saldo sia uguale a zero, e il risultato dell'anno viene trasferito al conto patrimoniale.</span><span class="sxs-lookup"><span data-stu-id="43c4f-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="43c4f-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43c4f-113">See Also</span></span>
[<span data-ttu-id="43c4f-114">Chiudere periodi contabili</span><span class="sxs-lookup"><span data-stu-id="43c4f-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="43c4f-115">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="43c4f-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="43c4f-116">Chiudi conto economico</span><span class="sxs-lookup"><span data-stu-id="43c4f-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="43c4f-117">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43c4f-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

