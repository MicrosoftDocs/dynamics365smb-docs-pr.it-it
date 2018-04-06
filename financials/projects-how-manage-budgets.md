---
title: Impostare e gestire un budget per una commessa| Documenti Microsoft
description: Descrive come pianificare le risorse, prevedere e controllare i costi di un progetto impostando un budget per ciascuna commessa.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e88eaebf65d950dcbb6c0296be24e68628a9494e
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="e97e6-103">Gestire budget per le commesse</span><span class="sxs-lookup"><span data-stu-id="e97e6-103">Manage Job Budgets</span></span>
<span data-ttu-id="e97e6-104">È possibile impostare un budget per ogni commessa.</span><span class="sxs-lookup"><span data-stu-id="e97e6-104">You can set up a budget for each job.</span></span> <span data-ttu-id="e97e6-105">Il budget viene utilizzato per pianificare le risorse allocate a una commessa.</span><span class="sxs-lookup"><span data-stu-id="e97e6-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="e97e6-106">Il budget può essere generale con pochi movimenti oppure può contenere più movimenti divisi in livelli di attività.</span><span class="sxs-lookup"><span data-stu-id="e97e6-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="e97e6-107">È quindi possibile confrontare gli importi previsti con l'utilizzo effettivo come registrato nelle registrazioni commesse.</span><span class="sxs-lookup"><span data-stu-id="e97e6-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="e97e6-108">Monitorando le differenze tra l'utilizzo effettivo e quello a budget, è possibile controllare un progetto in corso e migliorare la qualità di commesse future riducendo il rischio di sottovalutazione dei costi.</span><span class="sxs-lookup"><span data-stu-id="e97e6-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="e97e6-109">Di seguito viene descritto come stimare i costi a budget durante la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e97e6-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="e97e6-110">Per informazioni su come registrare i prezzi e i costi di commesse a budget rispetto a quelli effettivi, vedere [Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="e97e6-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="e97e6-111">Per stimare i costi a budget per una commessa</span><span class="sxs-lookup"><span data-stu-id="e97e6-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="e97e6-112">Quando un cliente desidera conoscere il prezzo di una commessa che verrà fatturata in base all'utilizzo, è necessario determinare i costi a budget per la commessa.</span><span class="sxs-lookup"><span data-stu-id="e97e6-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="e97e6-113">A tale scopo, utilizzare la finestra **Righe task commessa**.</span><span class="sxs-lookup"><span data-stu-id="e97e6-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="e97e6-114">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e97e6-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e97e6-115">Aprire una commessa appropriata.</span><span class="sxs-lookup"><span data-stu-id="e97e6-115">Open a relevant job.</span></span>
3. <span data-ttu-id="e97e6-116">Selezionare una riga di task di tipo Registrazione quindi scegliere l'azione **Righe pianificazione commessa**.</span><span class="sxs-lookup"><span data-stu-id="e97e6-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="e97e6-117">In una nuova riga, compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="e97e6-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="e97e6-118">Per il campo **Tipo riga** fare riferimento alle seguenti informazioni.</span><span class="sxs-lookup"><span data-stu-id="e97e6-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="e97e6-119">Tipo riga</span><span class="sxs-lookup"><span data-stu-id="e97e6-119">Line Type</span></span> | <span data-ttu-id="e97e6-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e97e6-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="e97e6-121">**Sia Budget sia fatturabile**</span><span class="sxs-lookup"><span data-stu-id="e97e6-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="e97e6-122">Gli importi relativi a costi e prezzo immessi nella riga di pianificazione sono i costi a budget per la riga di pianificazione specifica.</span><span class="sxs-lookup"><span data-stu-id="e97e6-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="e97e6-123">L'importo dei prezzi verrà fatturato.</span><span class="sxs-lookup"><span data-stu-id="e97e6-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="e97e6-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="e97e6-124">**Budget**</span></span> |<span data-ttu-id="e97e6-125">Al cliente non viene addebitato l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e97e6-125">The customer is not charged for usage.</span></span> <span data-ttu-id="e97e6-126">L'utilizzo non è trasferito in una fattura ma verrà comunque utilizzato nel calcolo di WIP.</span><span class="sxs-lookup"><span data-stu-id="e97e6-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="e97e6-127">**Fatturabile**</span><span class="sxs-lookup"><span data-stu-id="e97e6-127">**Billable**</span></span> |<span data-ttu-id="e97e6-128">Al cliente viene addebitato l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e97e6-128">The customer is charged for usage.</span></span> <span data-ttu-id="e97e6-129">La quantità viene trasferita nella fattura, in base alla quantità specificata nel campo Qtà da trasferire in fattura.</span><span class="sxs-lookup"><span data-stu-id="e97e6-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="e97e6-130">Il campo **Data pianificazione** per la riga di pianificazione contiene la data in cui è previsto il completamento dell'utilizzo correlato alla riga di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e97e6-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="e97e6-131">È inoltre la data in cui la riga di pianificazione può essere trasferita a una fattura vendita ed essere registrata.</span><span class="sxs-lookup"><span data-stu-id="e97e6-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e97e6-132">Quando si compila il campo **Quantità**, tutte le informazioni sul prezzo totale e i costi totali saranno calcolate e immesse per quella riga di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e97e6-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="e97e6-133">È possibile modificarle in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="e97e6-133">You can edit them at any time.</span></span>

<span data-ttu-id="e97e6-134">Nella finestra **Scheda commessa**, è possibile ora vedere un riepilogo dei costi a budget totali, del prezzo a budget, del costo e del prezzo fatturabili per ciascun task.</span><span class="sxs-lookup"><span data-stu-id="e97e6-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="e97e6-135">Per informazioni su come registrare i prezzi e i costi di commesse a budget rispetto a quelli effettivi, vedere [Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="e97e6-135">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e97e6-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e97e6-136">See Also</span></span>
[<span data-ttu-id="e97e6-137">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="e97e6-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="e97e6-138">Finanze</span><span class="sxs-lookup"><span data-stu-id="e97e6-138">Finance</span></span>](finance.md)  
<span data-ttu-id="e97e6-139">[Acquisti](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="e97e6-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="e97e6-140">[Vendite](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="e97e6-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="e97e6-141">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e97e6-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

