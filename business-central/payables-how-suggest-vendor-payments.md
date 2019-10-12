---
title: Utilizzare il processo batch Suggerisci pagamenti fornitore| Documenti Microsoft
description: È possibile specificare le impostazioni di pagamento dei fornitori per ottenere suggerimenti o proposte per pagamenti in scadenza oppure per cui è disponibile uno sconto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 86e1d6740b50fcdf1649c3f1ed0de0116e487e0b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314264"
---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="073b6-103">Sugg. pagamenti fornitore</span><span class="sxs-lookup"><span data-stu-id="073b6-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="073b6-104">Nella pagina **Registraz. pagamenti** è possibile utilizzare il processo batch **Sugg. pagamenti fornitore** per suggerire le righe di pagamento.</span><span class="sxs-lookup"><span data-stu-id="073b6-104">On the **Payment Journal** page, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="073b6-105">Le righe per i pagamenti che scadono presto oppure i pagamenti dove è disponibile uno sconto sul pagamento vengono suggerite in base alle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="073b6-105">Lines for payments that are due soon or payments where a payment discount is available are suggested based on your settings.</span></span>

<span data-ttu-id="073b6-106">Per trarre completamente vantaggio dai pagamenti suggeriti, è prima necessario assegnare una priorità ai fornitori.</span><span class="sxs-lookup"><span data-stu-id="073b6-106">To benefit fully from payment suggestions, you must first prioritize your vendors.</span></span> <span data-ttu-id="073b6-107">Per ulteriori informazioni, vedere [Attribuire un ordine di priorità ai fornitori](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="073b6-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="073b6-108">I movimenti contabili fornitore con stato **In sospeso** non sono inclusi nel processo batch.</span><span class="sxs-lookup"><span data-stu-id="073b6-108">Vendor ledger entries that are **On Hold** are not included in the batch job.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="073b6-109">Per trarre vantaggio dagli sconti sui pagamenti, se si è immesso un importo disponibile, l'importo verrà utilizzato per:</span><span class="sxs-lookup"><span data-stu-id="073b6-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  
    * <span data-ttu-id="073b6-110">Movimenti fornitori scaduti con priorità innanzitutto in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="073b6-110">Prioritized overdue vendor entries first in order of priority.</span></span>   
    * <span data-ttu-id="073b6-111">Movimenti fornitori scaduti senza priorità.</span><span class="sxs-lookup"><span data-stu-id="073b6-111">Overdue vendor entries that are not prioritized.</span></span>  
    * <span data-ttu-id="073b6-112">Movimenti fornitori che vengono qualificati per gli sconti sui pagamenti, sistemati in base al numero di fornitori.</span><span class="sxs-lookup"><span data-stu-id="073b6-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="073b6-113">Per utilizzare la funzione di suggerimento pagamenti fornitori</span><span class="sxs-lookup"><span data-stu-id="073b6-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="073b6-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="073b6-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="073b6-115">Aprire le registrazioni rilevanti e scegliere l'azione **Sugg. pagamenti fornitore**.</span><span class="sxs-lookup"><span data-stu-id="073b6-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="073b6-116">Compilare i campi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="073b6-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="073b6-117">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="073b6-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="073b6-118">Per inserire la data di scadenza come data di registrazione nelle righe di registrazione pagamenti</span><span class="sxs-lookup"><span data-stu-id="073b6-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="073b6-119">Quando si esegue il processo batch **Sugg. pagamenti fornitore** per creare righe di pagamento per i fornitori, è possibile compilare due campi speciali per assicurarsi che le righe generate utilizzino la data di scadenza per calcolare la data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="073b6-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="073b6-120">Questi campi sono **Calcola data di registrazione da Collega a - Scadenza doc.** e **Offset Collega a - Scadenza doc.**</span><span class="sxs-lookup"><span data-stu-id="073b6-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="073b6-121">Non è possibile utilizzare il campo **Calcola data di registrazione da Collega a - Scadenza doc** insieme al campo **Trova sconti pagamenti** o al campo **Raggruppa per fornitore**.</span><span class="sxs-lookup"><span data-stu-id="073b6-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="073b6-122">Se la data di registrazione è basata sulla data di scadenza, gli sconti sui pagamenti potrebbero non essere calcolati correttamente, in quanto la data di registrazione potrebbe essere successiva alla data dello sconto sul pagamento.</span><span class="sxs-lookup"><span data-stu-id="073b6-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="073b6-123">Inoltre, se la data di registrazione calcolata è già trascorsa, la data di registrazione viene spostata alla data di lavoro e viene visualizzato un avviso.</span><span class="sxs-lookup"><span data-stu-id="073b6-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="073b6-124">In alternativa, è possibile creare manualmente le righe di pagamento utilizzando la data di scadenza per calcolare la data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="073b6-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="073b6-125">Dopo che si collegano movimenti contabili fornitori, è possibile utilizzare l'azione **Calcola data registrazione** per aggiornare la data di registrazione nella riga di registrazione con la data di scadenza della fattura relativa di acquisto.</span><span class="sxs-lookup"><span data-stu-id="073b6-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="073b6-126">Per ulteriori informazioni, vedere [Collegare manualmente le transazioni di acquisto](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="073b6-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="073b6-127">Se la fattura di acquisto è scaduta, la data di registrazione viene impostata sulla data di lavoro e il carattere nella riga diventa di colore rosso.</span><span class="sxs-lookup"><span data-stu-id="073b6-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="073b6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="073b6-128">See Also</span></span>
[<span data-ttu-id="073b6-129">Gestione della contabilità fornitori</span><span class="sxs-lookup"><span data-stu-id="073b6-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="073b6-130">Effettuare i pagamenti</span><span class="sxs-lookup"><span data-stu-id="073b6-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="073b6-131">Utilizzo delle registrazioni COGE</span><span class="sxs-lookup"><span data-stu-id="073b6-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="073b6-132">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="073b6-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
