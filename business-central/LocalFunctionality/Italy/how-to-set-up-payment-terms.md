---
title: Impostazione delle condizioni di pagamento
description: "Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale. Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/27/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 05e768e6c8c244571d6056551beda635994ec6aa
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-payment-terms"></a><span data-ttu-id="c40a2-104">Impostazione delle condizioni di pagamento</span><span class="sxs-lookup"><span data-stu-id="c40a2-104">Set Up Payment Terms</span></span>
<span data-ttu-id="c40a2-105">Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale.</span><span class="sxs-lookup"><span data-stu-id="c40a2-105">For each payment term, you can specify if the payment can be made in installments.</span></span> <span data-ttu-id="c40a2-106">Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="c40a2-106">For example, you can define that a payment can be made in three installments with a third of the payment due after 30, 60, and 90 days.</span></span>  

<span data-ttu-id="c40a2-107">Se una condizione di pagamento deve prevedere un unico pagamento, è necessario specificare come verrà calcolata la data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="c40a2-107">If a payment term must be paid in one installment, you must still specify how the due date will be calculated.</span></span>  

## <a name="to-set-up-payment-terms"></a><span data-ttu-id="c40a2-108">Per impostare le condizioni di pagamento</span><span class="sxs-lookup"><span data-stu-id="c40a2-108">To set up payment terms</span></span>  
1.  <span data-ttu-id="c40a2-109">Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Condizioni pagamento**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c40a2-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Terms**, and then choose the related link.</span></span>    
2.  <span data-ttu-id="c40a2-110">Compilare i campi della finestra **Condizioni pagamento**.</span><span class="sxs-lookup"><span data-stu-id="c40a2-110">Fill in the fields in the **Payment Terms** window.</span></span> [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]  
3.  <span data-ttu-id="c40a2-111">Scegliere l'azione **Calcola**.</span><span class="sxs-lookup"><span data-stu-id="c40a2-111">Choose the **Calculation** action.</span></span>  
4.  <span data-ttu-id="c40a2-112">Nella finestra **Righe condizioni pagamento**, compilare i campi come indicato nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="c40a2-112">In the **Payment Terms Lines** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c40a2-113">Campo</span><span class="sxs-lookup"><span data-stu-id="c40a2-113">Field</span></span>|<span data-ttu-id="c40a2-114">Description</span><span class="sxs-lookup"><span data-stu-id="c40a2-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c40a2-115">**% pagamento**</span><span class="sxs-lookup"><span data-stu-id="c40a2-115">**Payment %**</span></span>|<span data-ttu-id="c40a2-116">Specificare la percentuale del pagamento totale a cui si riferisce il pagamento rateale.</span><span class="sxs-lookup"><span data-stu-id="c40a2-116">Specify the percentage of the total payment that this installment is for.</span></span><br /><br /> <span data-ttu-id="c40a2-117">Ad esempio, se il pagamento deve essere effettuato in una rata, immettere **100**.</span><span class="sxs-lookup"><span data-stu-id="c40a2-117">For example, if the payment must be made in one installment, enter **100**.</span></span>|  
    |<span data-ttu-id="c40a2-118">**Calcolo Data di Scadenza**</span><span class="sxs-lookup"><span data-stu-id="c40a2-118">**Due Date Calculation**</span></span>|<span data-ttu-id="c40a2-119">Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato.</span><span class="sxs-lookup"><span data-stu-id="c40a2-119">Specify the formula that is used to calculate the date that a payment must be made.</span></span><br /><br /> <span data-ttu-id="c40a2-120">Ad esempio, se il pagamento deve essere effettuato in una rata dopo due settimane, immettere **14D**.</span><span class="sxs-lookup"><span data-stu-id="c40a2-120">For example, if the payment must be made in one installment after two weeks, enter **14D**.</span></span> <span data-ttu-id="c40a2-121">Per ulteriori informazioni, vedere la sezione "Utilizzo di formule per le date" in [Immissione di dati](../../ui-enter-data.md).</span><span class="sxs-lookup"><span data-stu-id="c40a2-121">For more information, see the "Using Date Formulas" section in [Entering Data](../../ui-enter-data.md)</span></span>|  
    |<span data-ttu-id="c40a2-122">**Calcolo Sconto per Data**</span><span class="sxs-lookup"><span data-stu-id="c40a2-122">**Discount Date Calculation**</span></span>|<span data-ttu-id="c40a2-123">Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato per ottenere uno sconto.</span><span class="sxs-lookup"><span data-stu-id="c40a2-123">Specify the formula that is used to calculate the date that a payment must be made in order to obtain a discount.</span></span>|  
    |<span data-ttu-id="c40a2-124">**Sconto %**</span><span class="sxs-lookup"><span data-stu-id="c40a2-124">**Discount %**</span></span>|<span data-ttu-id="c40a2-125">Specificare la percentuale di sconto che viene applicata per il pagamento anticipato di un importo fattura.</span><span class="sxs-lookup"><span data-stu-id="c40a2-125">Specify the discount percentage that is applied for early payment of an invoice amount.</span></span>|  

5.  <span data-ttu-id="c40a2-126">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="c40a2-126">Choose the **OK** button.</span></span>  

<span data-ttu-id="c40a2-127">Il campo **Nr. di pagamenti** nella finestra **Condizioni pagamento** viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c40a2-127">The **Payment Nos.** field in the **Payment Terms** window is updated.</span></span> <span data-ttu-id="c40a2-128">Le condizioni di pagamento impostate qui saranno un riferimento per il calcolo automatico della data di scadenza dei documenti registrati per clienti e fornitori.</span><span class="sxs-lookup"><span data-stu-id="c40a2-128">The payment terms that you set here will be a reference for automatic due date calculation for documents that you post for relevant customers and vendors.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c40a2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c40a2-129">See Also</span></span>  
 <span data-ttu-id="c40a2-130">[Procedura: Impostare i pagamenti automatici e gli effetti automatici](how-to-set-up-automatic-payments-and-automatic-bills.md) </span><span class="sxs-lookup"><span data-stu-id="c40a2-130">[How to: Set Up Automatic Payments and Automatic Bills](how-to-set-up-automatic-payments-and-automatic-bills.md) </span></span>  
 [<span data-ttu-id="c40a2-131">Funzionalità locale per l'Italia</span><span class="sxs-lookup"><span data-stu-id="c40a2-131">Italy Local Functionality</span></span>](italy-local-functionality.md)   

