---
title: Annullare una registrazione con un movimento di pareggio| Documenti Microsoft
description: "Se è stata eseguita una registrazione errata nelle registrazioni generali, è possibile utilizzare la funzione Storno per annullare la registrazione con un audit trail corretto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="bed91-103">Procedura: Stornare una registrazione</span><span class="sxs-lookup"><span data-stu-id="bed91-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="bed91-104">Per stornare una registrazione errata, selezionare un movimento e creare movimenti di storno, ovvero movimenti identici a quelli originali ma con segno opposto nel campo relativo all'importo, con numero di documento e data di registrazione identici a quelli del movimento originale.</span><span class="sxs-lookup"><span data-stu-id="bed91-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="bed91-105">Dopo lo storno di un movimento, è necessario creare il movimento corretto.</span><span class="sxs-lookup"><span data-stu-id="bed91-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="bed91-106">È possibile stornare solo movimenti immessi da una riga di registrazioni generali.</span><span class="sxs-lookup"><span data-stu-id="bed91-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="bed91-107">Un movimento può essere stornato solo una volta.</span><span class="sxs-lookup"><span data-stu-id="bed91-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="bed91-108">Per ulteriori informazioni sulla registrazione dalle registrazioni generali, vedere [Procedura: Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="bed91-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="bed91-109">È possibile stornare i movimenti da tutte le finestre **Movimenti contabili**.</span><span class="sxs-lookup"><span data-stu-id="bed91-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="bed91-110">La seguente procedura è basata sulla finestra **Movimenti C/G**.</span><span class="sxs-lookup"><span data-stu-id="bed91-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="bed91-111">Per stornare la registrazione di un movimento di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="bed91-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="bed91-112">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Movimenti C/G**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="bed91-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="bed91-113">Selezionare il movimento che si desidera stornare quindi scegliere l'azione **Storno**.</span><span class="sxs-lookup"><span data-stu-id="bed91-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="bed91-114">Si noti che è necessario che il movimento derivi da una registrazione.</span><span class="sxs-lookup"><span data-stu-id="bed91-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="bed91-115">Nella finestra **Storna movimenti transazioni**, selezionare il movimento appropriato quindi scegliere l'azione **Storna**.</span><span class="sxs-lookup"><span data-stu-id="bed91-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="bed91-116">Scegliere il pulsante **Sì** nel messaggio di conferma.</span><span class="sxs-lookup"><span data-stu-id="bed91-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="bed91-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bed91-117">See Also</span></span>
[<span data-ttu-id="bed91-118">Procedura: Registrare le transazioni direttamente nella contabilità generale</span><span class="sxs-lookup"><span data-stu-id="bed91-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="bed91-119">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="bed91-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="bed91-120">Finanze</span><span class="sxs-lookup"><span data-stu-id="bed91-120">Finance</span></span>](finance.md)  
<span data-ttu-id="bed91-121">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bed91-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

