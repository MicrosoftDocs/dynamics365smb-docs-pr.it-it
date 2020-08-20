---
title: Impostazione delle condizioni di pagamento
description: Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale. Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 106af2b330168e8fefc645fedeb738a748c953fe
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676790"
---
# <a name="set-up-payment-terms"></a><span data-ttu-id="4c6da-104">Impostazione delle condizioni di pagamento</span><span class="sxs-lookup"><span data-stu-id="4c6da-104">Set Up Payment Terms</span></span>
<span data-ttu-id="4c6da-105">Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale.</span><span class="sxs-lookup"><span data-stu-id="4c6da-105">For each payment term, you can specify if the payment can be made in installments.</span></span> <span data-ttu-id="4c6da-106">Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="4c6da-106">For example, you can define that a payment can be made in three installments with a third of the payment due after 30, 60, and 90 days.</span></span>  

<span data-ttu-id="4c6da-107">Se una condizione di pagamento deve prevedere un unico pagamento, è necessario specificare come verrà calcolata la data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="4c6da-107">If a payment term must be paid in one installment, you must still specify how the due date will be calculated.</span></span>  

## <a name="to-set-up-payment-terms"></a><span data-ttu-id="4c6da-108">Per impostare le condizioni di pagamento</span><span class="sxs-lookup"><span data-stu-id="4c6da-108">To set up payment terms</span></span>  
1.  <span data-ttu-id="4c6da-109">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Condizioni pagamento** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="4c6da-109">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Terms**, and then choose the related link.</span></span>    
2.  <span data-ttu-id="4c6da-110">Compilare i campi nella pagina **Condizioni pagamento**.</span><span class="sxs-lookup"><span data-stu-id="4c6da-110">Fill in the fields on the **Payment Terms** page.</span></span> [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]  
3.  <span data-ttu-id="4c6da-111">Scegliere l'azione **Calcola**.</span><span class="sxs-lookup"><span data-stu-id="4c6da-111">Choose the **Calculation** action.</span></span>  
4.  <span data-ttu-id="4c6da-112">Nella pagina **Righe condizioni pagamento**, compilare i campi come indicato nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="4c6da-112">On the **Payment Terms Lines** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="4c6da-113">Campo</span><span class="sxs-lookup"><span data-stu-id="4c6da-113">Field</span></span>|<span data-ttu-id="4c6da-114">Description</span><span class="sxs-lookup"><span data-stu-id="4c6da-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="4c6da-115">**% pagamento**</span><span class="sxs-lookup"><span data-stu-id="4c6da-115">**Payment %**</span></span>|<span data-ttu-id="4c6da-116">Specificare la percentuale del pagamento totale a cui si riferisce il pagamento rateale.</span><span class="sxs-lookup"><span data-stu-id="4c6da-116">Specify the percentage of the total payment that this installment is for.</span></span><br /><br /> <span data-ttu-id="4c6da-117">Ad esempio, se il pagamento deve essere effettuato in una rata, immettere **100**.</span><span class="sxs-lookup"><span data-stu-id="4c6da-117">For example, if the payment must be made in one installment, enter **100**.</span></span>|  
    |<span data-ttu-id="4c6da-118">**Calcolo Data di Scadenza**</span><span class="sxs-lookup"><span data-stu-id="4c6da-118">**Due Date Calculation**</span></span>|<span data-ttu-id="4c6da-119">Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato.</span><span class="sxs-lookup"><span data-stu-id="4c6da-119">Specify the formula that is used to calculate the date that a payment must be made.</span></span><br /><br /> <span data-ttu-id="4c6da-120">Ad esempio, se il pagamento deve essere effettuato in una rata dopo due settimane, immettere **14D**.</span><span class="sxs-lookup"><span data-stu-id="4c6da-120">For example, if the payment must be made in one installment after two weeks, enter **14D**.</span></span> <span data-ttu-id="4c6da-121">Per ulteriori informazioni, vedere [Utilizzo di formule per le date](../../ui-enter-date-ranges.md#using-date-formulas).</span><span class="sxs-lookup"><span data-stu-id="4c6da-121">For more information, see [Using Date Formulas](../../ui-enter-date-ranges.md#using-date-formulas)</span></span>|  
    |<span data-ttu-id="4c6da-122">**Calcolo Sconto per Data**</span><span class="sxs-lookup"><span data-stu-id="4c6da-122">**Discount Date Calculation**</span></span>|<span data-ttu-id="4c6da-123">Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato per ottenere uno sconto.</span><span class="sxs-lookup"><span data-stu-id="4c6da-123">Specify the formula that is used to calculate the date that a payment must be made in order to obtain a discount.</span></span>|  
    |<span data-ttu-id="4c6da-124">**Sconto %**</span><span class="sxs-lookup"><span data-stu-id="4c6da-124">**Discount %**</span></span>|<span data-ttu-id="4c6da-125">Specificare la percentuale di sconto che viene applicata per il pagamento anticipato di un importo fattura.</span><span class="sxs-lookup"><span data-stu-id="4c6da-125">Specify the discount percentage that is applied for early payment of an invoice amount.</span></span>|  

5.  <span data-ttu-id="4c6da-126">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c6da-126">Choose the **OK** button.</span></span>  

<span data-ttu-id="4c6da-127">Il campo **Nr. di pagamenti** nella pagina **Condizioni pagamento** viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4c6da-127">The **Payment Nos.** field on the **Payment Terms** page is updated.</span></span> <span data-ttu-id="4c6da-128">Le condizioni di pagamento impostate qui saranno un riferimento per il calcolo automatico della data di scadenza dei documenti registrati per clienti e fornitori.</span><span class="sxs-lookup"><span data-stu-id="4c6da-128">The payment terms that you set here will be a reference for automatic due date calculation for documents that you post for relevant customers and vendors.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c6da-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c6da-129">See Also</span></span>  
 <span data-ttu-id="4c6da-130">[Impostare i pagamenti automatici e gli effetti automatici](how-to-set-up-automatic-payments-and-automatic-bills.md) </span><span class="sxs-lookup"><span data-stu-id="4c6da-130">[Set Up Automatic Payments and Automatic Bills](how-to-set-up-automatic-payments-and-automatic-bills.md) </span></span>  
 [<span data-ttu-id="4c6da-131">Funzionalità locale per l'Italia</span><span class="sxs-lookup"><span data-stu-id="4c6da-131">Italy Local Functionality</span></span>](italy-local-functionality.md)   
