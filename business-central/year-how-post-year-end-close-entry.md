---
title: Registrare il movimento di chiusura di fine anno
description: Descrive come aprire le registrazioni specificate nel processo batch Chiudi conto economico, quindi analizzare e registrare il movimento di chiusura di fine anno.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c822685ae5723bc6b13f9fedad45dbddefdb956
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776594"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="6b097-103">Registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="6b097-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="6b097-104">Dopo avere utilizzato il processo batch **Chiudi conto economico** per generare il movimento o i movimenti di chiusura di fine anno, è necessario aprire le registrazioni specificate nel processo batch, quindi analizzare e registrare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="6b097-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="6b097-105">A seconda dei processi di lavoro delle organizzazioni, è possibile scegliere di chiudere o meno i periodi contabili e gli anni fiscali in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6b097-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6b097-106">La procedura seguente presuppone che sia stato chiuso l'anno fiscale utilizzando l'opzione *Periodi contabili*, che sia stato generato un movimento di chiusura di fine anno utilizzando il processo batch **Chiudi conto economico** e che si è ora pronti a registrare il movimento di chiusura di fine anno insieme alla compensazione dei movimenti conti patrimonio netto.</span><span class="sxs-lookup"><span data-stu-id="6b097-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="6b097-107">L'organizzazione può scegliere di lavorare in modo diverso, ad esempio di registrare il movimento di chiusura di fine anno come parte della chiusura dell'anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="6b097-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="6b097-108">Per registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="6b097-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="6b097-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="6b097-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6b097-110">Nella pagina **Registrazione COGE**, nel campo **Nome batch**, selezionare il batch contenente i movimenti di chiusura.</span><span class="sxs-lookup"><span data-stu-id="6b097-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="6b097-111">Analizzare i movimenti.</span><span class="sxs-lookup"><span data-stu-id="6b097-111">Review the entries.</span></span>
4. <span data-ttu-id="6b097-112">Per contabilizzare le registrazioni, scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="6b097-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="6b097-113">Se viene rilevato un errore, viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="6b097-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="6b097-114">Se la registrazione avviene correttamente, i movimenti registrati vengono rimossi dalle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="6b097-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="6b097-115">Dopo il completamento della registrazione, in ogni conto economico viene registrato un movimento in modo che il relativo saldo sia uguale a zero, e il risultato dell'anno viene trasferito al conto patrimoniale.</span><span class="sxs-lookup"><span data-stu-id="6b097-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b097-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b097-116">See Also</span></span>

[<span data-ttu-id="6b097-117">Chiudere periodi contabili</span><span class="sxs-lookup"><span data-stu-id="6b097-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="6b097-118">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="6b097-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="6b097-119">Chiudi conto economico</span><span class="sxs-lookup"><span data-stu-id="6b097-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="6b097-120">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6b097-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]