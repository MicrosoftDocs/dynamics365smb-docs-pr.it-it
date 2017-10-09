---
title: Chiusura dei periodi contabili per un anno fiscale | Documenti Microsoft
description: Descrive come chiudere i periodi contabili alla base di un anno fiscale.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 859801a5e9d9b900aed6af5fe672f650932b2e79
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-close-accounting-periods"></a><span data-ttu-id="334fb-103">Procedura: Chiudere i periodi contabili</span><span class="sxs-lookup"><span data-stu-id="334fb-103">How to: Close Accounting Periods</span></span>
<span data-ttu-id="334fb-104">Al termine di un anno fiscale, è necessario chiudere i periodi di cui è costituito.</span><span class="sxs-lookup"><span data-stu-id="334fb-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="334fb-105">Per chiudere periodi contabili</span><span class="sxs-lookup"><span data-stu-id="334fb-105">To close accounting periods</span></span>
1. <span data-ttu-id="334fb-106">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Periodi contabili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="334fb-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="334fb-107">Nella finestra **Periodi contabili** scegliere l'azione **Chiudi anno**.</span><span class="sxs-lookup"><span data-stu-id="334fb-107">In the **Accounting Periods** window, choose the **Close Year** action.</span></span>

    <span data-ttu-id="334fb-108">Se più anni fiscali sono aperti, viene automaticamente selezionato quello meno recente per la chiusura.</span><span class="sxs-lookup"><span data-stu-id="334fb-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="334fb-109">Viene visualizzato un messaggio che identifica l'anno che verrà chiuso e le conseguenze di tale operazione.</span><span class="sxs-lookup"><span data-stu-id="334fb-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="334fb-110">Per chiudere l'anno, scegliere il pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="334fb-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="334fb-111">L'anno fiscale viene chiuso e vengono selezionati i campi **Chiuso** e **Data bloccata** per tutti i periodi dell'anno.</span><span class="sxs-lookup"><span data-stu-id="334fb-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="334fb-112">L'anno fiscale non può essere riaperto e i segni di spunta nei campi **Chiuso** e **Data bloccata** non possono essere rimossi.</span><span class="sxs-lookup"><span data-stu-id="334fb-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="334fb-113">Non è possibile chiudere un anno fiscale prima di crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="334fb-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="334fb-114">Si noti che una volta chiuso un anno fiscale, non è possibile modificare la data iniziale di quello successivo.</span><span class="sxs-lookup"><span data-stu-id="334fb-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="334fb-115">Anche se l'anno fiscale è stato chiuso, è possibile registrarvi dei movimenti C/G.</span><span class="sxs-lookup"><span data-stu-id="334fb-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="334fb-116">In questo caso, i movimenti vengono contrassegnati come registrati in un anno fiscale chiuso e viene selezionato il campo **Mov. anno prec.**</span><span class="sxs-lookup"><span data-stu-id="334fb-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="334fb-117">Una volta chiuso un anno fiscale, è necessario chiudere i conti economici e trasferire i risultati dell'anno su un conto nello stato patrimoniale.</span><span class="sxs-lookup"><span data-stu-id="334fb-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="334fb-118">È possibile ripetere queste operazioni ogni volta che si effettua una registrazione sull'anno fiscale chiuso.</span><span class="sxs-lookup"><span data-stu-id="334fb-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="334fb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="334fb-119">See Also</span></span>
[<span data-ttu-id="334fb-120">Chiusura registri</span><span class="sxs-lookup"><span data-stu-id="334fb-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="334fb-121">Procedura: Registrare il movimento di chiusura di fine anno</span><span class="sxs-lookup"><span data-stu-id="334fb-121">How to: Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="334fb-122">Procedura: aprire un nuovo anno fiscale</span><span class="sxs-lookup"><span data-stu-id="334fb-122">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="334fb-123">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="334fb-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

