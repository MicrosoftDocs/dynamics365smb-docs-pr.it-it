---
title: Analizzare e registrare il movimento di chiusura di fine anno | Documenti Microsoft
description: Descrive come aprire le registrazioni specificate nel processo batch Chiudi conto economico, quindi analizzare e registrare il movimento di chiusura di fine anno.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ca92d9535a9a15d46d93de6febdfd169c3d7d17a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755544"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="7e0b5-103">Registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="7e0b5-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="7e0b5-104">Dopo avere utilizzato il processo batch **Chiudi conto economico** per generare il movimento o i movimenti di chiusura di fine anno, è necessario aprire le registrazioni specificate nel processo batch, quindi analizzare e registrare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="7e0b5-105">Per registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="7e0b5-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="7e0b5-106">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="7e0b5-107">Nella pagina **Registrazione COGE**, nel campo **Nome batch**, selezionare il batch contenente i movimenti di chiusura.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-107">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="7e0b5-108">Analizzare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-108">Review the entries.</span></span>
4. <span data-ttu-id="7e0b5-109">Per contabilizzare le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7e0b5-110">Se viene rilevato un errore, viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="7e0b5-111">Se la registrazione avviene correttamente, i movimenti registrati vengono rimossi dalle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="7e0b5-112">Dopo il completamento della registrazione, in ogni conto economico viene registrato un movimento in modo che il relativo saldo sia uguale a zero, e il risultato dell'anno viene trasferito al conto patrimoniale.</span><span class="sxs-lookup"><span data-stu-id="7e0b5-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e0b5-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e0b5-113">See Also</span></span>
[<span data-ttu-id="7e0b5-114">Chiudere periodi contabili</span><span class="sxs-lookup"><span data-stu-id="7e0b5-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="7e0b5-115">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="7e0b5-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="7e0b5-116">Chiudi conto economico</span><span class="sxs-lookup"><span data-stu-id="7e0b5-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="7e0b5-117">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e0b5-117">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
