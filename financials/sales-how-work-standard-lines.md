---
title: Impostare e utilizzare righe standard per vendite e acquisti ricorrenti| Documenti Microsoft
description: "È possibile impostare righe di vendita e acquisto più frequentemente usate e quindi inserirle nei documenti di vendita e di acquisto per compilare rapidamente le righe con informazioni standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: it-it
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="d10fd-103">Procedura: Creare righe di vendite e acquisti ricorrenti</span><span class="sxs-lookup"><span data-stu-id="d10fd-103">How to: Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="d10fd-104">Se è spesso necessario creare righe di vendita e acquisto con informazioni simili, è possibile impostare righe standard da inserire nei documenti di vendita e di acquisto ricorrenti, ad esempio, per ordini di approvvigionamento ricorrenti.</span><span class="sxs-lookup"><span data-stu-id="d10fd-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="d10fd-105">La seguente procedura illustra come utilizzare le righe di vendita standard.</span><span class="sxs-lookup"><span data-stu-id="d10fd-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="d10fd-106">Funziona in modo simile per le righe di acquisto standard.</span><span class="sxs-lookup"><span data-stu-id="d10fd-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="d10fd-107">Per impostare righe di vendita standard</span><span class="sxs-lookup"><span data-stu-id="d10fd-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="d10fd-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici vendite standard**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d10fd-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d10fd-109">Nella finestra **Righe vendita standard** scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="d10fd-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="d10fd-110">Compilare i campi appropriati della Scheda dettaglio **Generale**.</span><span class="sxs-lookup"><span data-stu-id="d10fd-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="d10fd-111">Nella Scheda dettaglio **Righe**, immettere le informazioni nei campi per preparare le righe di vendita che riflettono le righe standard che si prevede di utilizzare come righe ricorrenti nei documenti di vendita.</span><span class="sxs-lookup"><span data-stu-id="d10fd-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="d10fd-112">Per inserire le righe di vendita standard in una fattura di vendita</span><span class="sxs-lookup"><span data-stu-id="d10fd-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="d10fd-113">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fatture**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d10fd-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d10fd-114">Aprire la fattura di vendita in cui si desidera inserire una più righe di vendita standard.</span><span class="sxs-lookup"><span data-stu-id="d10fd-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="d10fd-115">Scegliere l'azione **Ottieni righe vendita ricorrenti**.</span><span class="sxs-lookup"><span data-stu-id="d10fd-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="d10fd-116">Nella finestra **Righe vendita ricorrenti**, scegliere il pulsante di ricerca nel campo **Codice** e selezionare una serie di righe di vendita standard.</span><span class="sxs-lookup"><span data-stu-id="d10fd-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="d10fd-117">Scegliere il pulsante **OK** per inserire le righe di vendita standard della fattura, in cui è possibile riutilizzare la riga come è o modificarne le informazioni.</span><span class="sxs-lookup"><span data-stu-id="d10fd-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="d10fd-118">Per creare più fatture di vendita in base alle righe di vendita standard</span><span class="sxs-lookup"><span data-stu-id="d10fd-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="d10fd-119">È possibile utilizzare il processo batch **Crea fattura di vendita periodica**</span><span class="sxs-lookup"><span data-stu-id="d10fd-119">You can use the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="d10fd-120">per creare fatture di vendita in base a righe di vendita standard assegnate ai clienti e con date di registrazione comprese nell'intervallo di date valide specificato nel codice di vendita standard.</span><span class="sxs-lookup"><span data-stu-id="d10fd-120">batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="d10fd-121">Nella finestra **Righe vendita ricorrenti** è anche possibile specificare un metodo di pagamento in addebito diretto e un mandato di addebito diretto.</span><span class="sxs-lookup"><span data-stu-id="d10fd-121">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="d10fd-122">Le fatture di vendita create con il processo batch **Crea fattura di vendita periodica**</span><span class="sxs-lookup"><span data-stu-id="d10fd-122">The sales invoices that are created with the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="d10fd-123">includeranno le informazioni necessarie per riscuotere il pagamento per le fatture di vendita con addebito diretto SEPA.</span><span class="sxs-lookup"><span data-stu-id="d10fd-123">batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="d10fd-124">Per ulteriori informazioni, vedere Riscuotere pagamenti con addebito diretto SEPA.</span><span class="sxs-lookup"><span data-stu-id="d10fd-124">For more information, see Collect Payments with SEPA Direct Debit.</span></span>

1. <span data-ttu-id="d10fd-125">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Crea fatture di vendita periodiche**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d10fd-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d10fd-126">In **Crea fattura di vendita periodica**</span><span class="sxs-lookup"><span data-stu-id="d10fd-126">In the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="d10fd-127">compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="d10fd-127">window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="d10fd-128">Nel campo **Codice** immettere il codice delle righe di vendita standard assegnato a un cliente per cui si desidera creare fatture di vendita.</span><span class="sxs-lookup"><span data-stu-id="d10fd-128">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="d10fd-129">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="d10fd-129">Choose the **OK** button.</span></span>

<span data-ttu-id="d10fd-130">Le fatture di vendita vengono create per i clienti con il codice di vendita cliente standard specificato e con eventuali informazioni sull'addebito diretto specificate, per la registrazione alla data specificata.</span><span class="sxs-lookup"><span data-stu-id="d10fd-130">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="d10fd-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d10fd-131">See Also</span></span>  
[<span data-ttu-id="d10fd-132">Vendite</span><span class="sxs-lookup"><span data-stu-id="d10fd-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="d10fd-133">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d10fd-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

