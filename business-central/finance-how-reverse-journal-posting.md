---
title: Annullare una registrazione con un movimento di pareggio | Microsoft Docs
description: "Se è stata eseguita una registrazione errata nelle registrazioni generali, è possibile utilizzare la funzione Storno per annullare la registrazione con un audit trail corretto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: beed335b93ef9211e4fc53c25f97b3fed6137348
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="reverse-postings"></a><span data-ttu-id="fb3c4-103">Stornare le registrazioni</span><span class="sxs-lookup"><span data-stu-id="fb3c4-103">Reverse Postings</span></span>
<span data-ttu-id="fb3c4-104">Per stornare una registrazione errata, selezionare un movimento e creare movimenti di storno, ovvero movimenti identici a quelli originali ma con segno opposto nel campo relativo all'importo, con numero di documento e data di registrazione identici a quelli del movimento originale.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="fb3c4-105">Dopo lo storno di un movimento, è necessario creare il movimento corretto.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="fb3c4-106">È possibile stornare solo movimenti immessi da una riga di registrazioni generali.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="fb3c4-107">Un movimento può essere stornato solo una volta.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="fb3c4-108">Per ulteriori informazioni sulla registrazione dalle registrazioni generali, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="fb3c4-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="fb3c4-109">Se è stata eseguita una registrazione di quantità negativa, ad esempio se è stato creato un ordine di acquisto con un numero errato di articoli e lo si è registrato come ricevuto (ma non fatturato), è possibile annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="fb3c4-110">Se è stata eseguita una registrazione di quantità positiva, ad esempio se è stato creato un ordine di reso con un numero errato di articoli e lo si è registrato come spedito (ma non fatturato), è possibile annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="fb3c4-111">Per stornare la registrazione di un movimento di contabilità generale</span><span class="sxs-lookup"><span data-stu-id="fb3c4-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="fb3c4-112">È possibile stornare i movimenti da tutte le finestre **Movimenti contabili**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-112">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="fb3c4-113">La seguente procedura è basata sulla finestra **Movimenti C/G**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-113">The following procedure is based in the **General Ledger Entries** window.</span></span>
1. <span data-ttu-id="fb3c4-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Movimenti C/G** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="fb3c4-115">Selezionare il movimento che si desidera stornare quindi scegliere l'azione **Storno**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="fb3c4-116">Si noti che è necessario che il movimento derivi da una registrazione.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="fb3c4-117">Nella finestra **Storna movimenti transazioni**, selezionare il movimento appropriato quindi scegliere l'azione **Storna**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-117">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="fb3c4-118">Scegliere il pulsante **Sì** nel messaggio di conferma.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="fb3c4-119">Per annullare la registrazione di una quantità in una ricezione acquisti registrata</span><span class="sxs-lookup"><span data-stu-id="fb3c4-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="fb3c4-120">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ricezioni acquisti registrate** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fb3c4-121">Aprire il carico registrato che si desidera annullare.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="fb3c4-122">Selezionare la riga o le righe che si desidera annullare.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="fb3c4-123">Scegliere l'azione **Annulla carico**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="fb3c4-124">Una riga di rettifica viene registrata sotto la riga di carico selezionata.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="fb3c4-125">Se la quantità è stata ricevuta in un carico warehouse, una riga di rettifica viene inserita nel carico warehouse registrato.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="fb3c4-126">I campi **Quantità ricevuta** e **Qtà carichi non fatt.** nell'ordine di acquisto collegato verranno impostati su un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="fb3c4-127">Per annullare e successivamente ripetere la registrazione di una quantità in una spedizione di reso registrata</span><span class="sxs-lookup"><span data-stu-id="fb3c4-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="fb3c4-128">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Spedizioni reso registrate** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fb3c4-129">Aprire la spedizione reso registrata che si desidera annullare.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="fb3c4-130">Selezionare la riga o le righe che si desidera annullare.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="fb3c4-131">Scegliere l'azione **Eliminare spedizione reso**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="fb3c4-132">Nel documento registrato viene inserita una riga correttiva e i campi **Qtà reso spedita** e **Reso spedito non fatt.** nell'ordine di reso vengono impostati su un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="fb3c4-133">Ora tornare all'ordine di reso di acquisto per ripetere la registrazione.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="fb3c4-134">Nella finestra **Spedizione reso registrata** prendere nota del numero nel campo **Nr. ordine di reso**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-134">In the **Posted Return Shipment** window, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="fb3c4-135"> </span><span class="sxs-lookup"><span data-stu-id="fb3c4-135">field.</span></span>  
6.  <span data-ttu-id="fb3c4-136">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di reso acquisto** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="fb3c4-137">Aprire l'ordine di reso in questione quindi scegliere l'azione **Riapri**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="fb3c4-138">Correggere la voce nel campo **Quantità** e registrare nuovamente l'ordine di reso acquisto.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="fb3c4-139">Per registrare un movimento negativo</span><span class="sxs-lookup"><span data-stu-id="fb3c4-139">To post a negative entry</span></span>  
<span data-ttu-id="fb3c4-140">È possibile utilizzare il campo **Correzione** per registrare un addebito negativo anziché un credito oppure un accredito negativo anziché un addebito su un conto.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="fb3c4-141">Per soddisfare i requisiti legali, questo campo è visibile per impostazione predefinita in tutte le registrazioni.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="fb3c4-142">I campi **Dare** e **Avere** includono il movimento originale e il movimento corretto.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="fb3c4-143">Questi campi non influiscono sul saldo del conto.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="fb3c4-144">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="fb3c4-145">Nel campo **Nome batch** selezionare il nome di batch necessario.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="fb3c4-146">Immettere informazioni nei campi rilevanti.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="fb3c4-147">Nella riga di registrazione che si desidera attivare per i movimenti negativi, selezionare la casella di controllo **Correzione**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="fb3c4-148">Per contabilizzare la registrazione, scegliere l'azione **Registra**, quindi scegliere il pulsante **Sì**.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb3c4-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb3c4-149">See Also</span></span>
[<span data-ttu-id="fb3c4-150">Registrare le transazioni direttamente nella contabilità generale</span><span class="sxs-lookup"><span data-stu-id="fb3c4-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="fb3c4-151">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="fb3c4-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="fb3c4-152">Finanze</span><span class="sxs-lookup"><span data-stu-id="fb3c4-152">Finance</span></span>](finance.md)  
<span data-ttu-id="fb3c4-153">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fb3c4-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

