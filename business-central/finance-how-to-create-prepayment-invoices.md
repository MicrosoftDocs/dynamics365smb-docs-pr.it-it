---
title: Come creare fatture di pagamenti anticipati | Microsoft Docs
description: Informazioni su come gestire situazioni in cui un pagamento anticipato viene richiesto ai clienti o dal fornitore.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3a1f79f089ef8633ca51be35930c5de5c2401b29
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387401"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="b7e6d-103">Creare fatture per i pagamenti anticipati</span><span class="sxs-lookup"><span data-stu-id="b7e6d-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="b7e6d-104">Se è necessario che i clienti inviino il pagamento prima della spedizione di un ordine, è possibile utilizzare la funzionalità di pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="b7e6d-105">Lo stesso vale se il fornitore richiede di inviare il pagamento prima di spedire un ordine.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="b7e6d-106">È possibile creare un processo di pagamento anticipato quando si crea un ordine di vendita o di acquisto.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="b7e6d-107">Se è impostata una percentuale di pagamento anticipato predefinita per il cliente o il fornitore, verrà automaticamente inclusa nella fattura di pagamento anticipato risultante.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="b7e6d-108">È inoltre possibile specificare una percentuale di pagamento anticipato per l'intero documento.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="b7e6d-109">Dopo avere creato un ordine di vendita o di acquisto, è possibile creare una fattura pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="b7e6d-110">È possibile utilizzare le percentuali di default per ogni riga di vendita o di acquisto oppure rettificare l'importo come necessario.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="b7e6d-111">È ad esempio possibile specificare un importo totale per l'intero ordine.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="b7e6d-112">La procedura seguente descrive come fatturare un pagamento anticipato per un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="b7e6d-113">I passaggi sono simili per un ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="b7e6d-114">Per creare una fattura di pagamento anticipato</span><span class="sxs-lookup"><span data-stu-id="b7e6d-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="b7e6d-115">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b7e6d-116">Creare un nuovo ordine di vendita per un cliente pertinente.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="b7e6d-117">Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="b7e6d-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="b7e6d-118">Nella scheda dettaglio **Pagamento anticipato** il campo **% pagamento anticipato** specifica la percentuale da utilizzare per calcolare l'importo del pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="b7e6d-119">Se nella scheda cliente è impostata una percentuale pagamento anticipato di default, il campo viene compilato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="b7e6d-120">È possibile modificare la percentuale.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="b7e6d-121">Scegliere il campo **Comprimi pagamento anticipato** se si desidera creare righe nella fattura di pagamento anticipato che combinano righe dell'ordine cliente se:</span><span class="sxs-lookup"><span data-stu-id="b7e6d-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="b7e6d-122">Le righe hanno lo stesso conto di contabilità generale per i pagamenti anticipati, come determinato in Setup registrazioni COGE.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="b7e6d-123">Le righe hanno le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="b7e6d-124">Se si desidera specificare una fattura pagamento anticipato con una riga per ogni riga dell'ordine di vendita associata a una percentuale pagamento anticipato, non scegliere il campo **Comprimi pagamento anticipato**.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="b7e6d-125">La data di scadenza per il pagamento anticipato viene calcolata automaticamente in base al valore di **Cod. condizioni pagam. ant.**.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="b7e6d-126">Compilare le righe di vendita.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="b7e6d-127">Se è stata specificata una percentuale di pagamento anticipato predefinita per il cliente o nella scheda dettaglio **Pagamento anticipato** sul documento, questo valore viene copiato in ogni riga.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="b7e6d-128">È possibile modificare il contenuto del campo **% pagamento anticipato** nella riga.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="b7e6d-129">Per visualizzare l'importo del pagamento anticipato totale, scegliere l'azione **Statistiche**.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="b7e6d-130">Se si desidera rettificare l'importo del pagamento anticipato totale per l'ordine, è possibile modificare il contenuto del campo **Importo pagamento anticipato** nella pagina **Statistiche ordini vendita**.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="b7e6d-131">Se il campo **Prezzi IVA inclusa** è selezionato, il campo **Importo pagam. ant. IVA incl.** è modificabile.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="b7e6d-132">Se si modifica il contenuto del campo **Importo pagamento anticipato**, l'importo verrà distribuito proporzionalmente tra tutte le righe, ad eccezione di quelle in cui è presente il valore **0** nel campo **% pagamento anticipato**.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="b7e6d-133">Per stampare un report test prima di registrare una fattura pagamento anticipato, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Report test pagamento anticipato**.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="b7e6d-134">Per registrare la fattura pagamento anticipato, scegliere l'azione **Pagamento anticipato** e quindi scegliere l'azione **Registra fattura pagamento anticipato**.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="b7e6d-135">Per registrare e stampare la fattura pagamento anticipato, scegliere l'azione **Registra e stampa fattura pagam. ant.**</span><span class="sxs-lookup"><span data-stu-id="b7e6d-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="b7e6d-136">È possibile emettere fatture pagamento anticipato aggiuntive per l'ordine.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="b7e6d-137">A tale scopo, aumentare l'importo pagamento anticipato in una o più righe, rettificare la data del documento, se necessario, e registrare la fattura pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="b7e6d-138">Verrà creata una nuova fattura per la differenza tra gli importi pagamento anticipato fatturati fino a quel momento e il nuovo importo pagamento anticipato.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="b7e6d-139">Se ci si trova in America del Nord, non è possibile modificare la percentuale di pagamento anticipato dopo che la fattura pagamento anticipato è stata registrata.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="b7e6d-140">Ciò è impedito nella versione nordamericana di [!INCLUDE[prod_short](includes/prod_short.md)] perché altrimenti il calcolo dell'imposta sulle vendite risulterebbe errato.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="b7e6d-141">Quando si è pronti per registrare il resto della fattura, effettuare la registrazione come con qualsiasi fattura. L'importo pagamento anticipato verrà automaticamente dedotto dall'importo dovuto.</span><span class="sxs-lookup"><span data-stu-id="b7e6d-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7e6d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7e6d-142">See Also</span></span>

[<span data-ttu-id="b7e6d-143">Fatturazione dei pagamenti anticipati</span><span class="sxs-lookup"><span data-stu-id="b7e6d-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="b7e6d-144">Procedura dettagliata: impostazione e fatturazione dei pagamenti anticipati vendite</span><span class="sxs-lookup"><span data-stu-id="b7e6d-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="b7e6d-145">Finanze</span><span class="sxs-lookup"><span data-stu-id="b7e6d-145">Finance</span></span>](finance.md)  
<span data-ttu-id="b7e6d-146">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7e6d-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]