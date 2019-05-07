---
title: 'Procedura dettagliata: Esecuzione di previsioni di flusso di cassa utilizzando le situazioni contabili | Documenti Microsoft'
description: In questa procedura dettagliata viene descritto come utilizzare le situazioni contabili per effettuare previsioni del flusso di cassa. Le situazioni contabili consentono di effettuare i calcoli che non possono essere eseguiti direttamente nel piano dei conti di cassa. Nelle situazioni contabili è possibile impostare i subtotali relativi agli incassi e alle uscite di cassa. I subtotali possono essere inclusi nei nuovi totali che potranno essere utilizzati per effettuare le previsioni del flusso di cassa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c09eedbb812df909a43e514dc462dcf8c1cf182a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "932625"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="e4ee6-106">Procedura dettagliata: Esecuzione di previsioni di flusso di cassa utilizzando le situazioni contabili</span><span class="sxs-lookup"><span data-stu-id="e4ee6-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="e4ee6-107">In questa procedura dettagliata viene descritto come utilizzare le situazioni contabili per effettuare previsioni del flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="e4ee6-108">Le situazioni contabili consentono di effettuare i calcoli che non possono essere eseguiti direttamente nel piano dei conti di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="e4ee6-109">Nelle situazioni contabili è possibile impostare i subtotali relativi agli incassi e alle uscite di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="e4ee6-110">I subtotali possono essere inclusi nei nuovi totali che potranno essere utilizzati per effettuare le previsioni del flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="e4ee6-111">Informazioni sulla procedura dettagliata</span><span class="sxs-lookup"><span data-stu-id="e4ee6-111">About This Walkthrough</span></span>  
<span data-ttu-id="e4ee6-112">In questa procedura dettagliata sono descritti i task seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4ee6-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="e4ee6-113">Impostazione di un nuovo nome della situazione contabile del conto di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="e4ee6-114">Impostazione delle righe della situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="e4ee6-115">Impostazione di un nuovo layout colonna.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="e4ee6-116">Assegnazione di un layout colonna a una situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="e4ee6-117">Visualizzazione e stampa della previsione del flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="e4ee6-118">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="e4ee6-118">Prerequisites</span></span>  
<span data-ttu-id="e4ee6-119">Per completare questa procedura dettagliata, sarà necessario:</span><span class="sxs-lookup"><span data-stu-id="e4ee6-119">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="e4ee6-120">Aver installato [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e4ee6-120">[!INCLUDE[d365fin](includes/d365fin_md.md)] installed.</span></span>  
- <span data-ttu-id="e4ee6-121">Registrazione delle righe del prospetto del flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="e4ee6-122">Ruoli</span><span class="sxs-lookup"><span data-stu-id="e4ee6-122">Roles</span></span>  
<span data-ttu-id="e4ee6-123">Questa procedura dettagliata comprende task svolti dal ruolo utente seguente:</span><span class="sxs-lookup"><span data-stu-id="e4ee6-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="e4ee6-124">Controller</span><span class="sxs-lookup"><span data-stu-id="e4ee6-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="e4ee6-125">Scenario</span><span class="sxs-lookup"><span data-stu-id="e4ee6-125">Story</span></span>  
<span data-ttu-id="e4ee6-126">Ken è un manager presso CRONUS che effettua previsioni del flusso di cassa mensili.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="e4ee6-127">Egli include interessi, vendite, acquisti e cespiti nella previsione che presenta alla DF Sara per un'opinione in merito.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="e4ee6-128">Impostazione di un nuovo nome della situazione contabile</span><span class="sxs-lookup"><span data-stu-id="e4ee6-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="e4ee6-129">Una situazione contabile è costituita da un nome della situazione contabile del conto di cassa con una serie di righe e da un layout colonna.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="e4ee6-130">Per impostare un nuovo nome situazione contabile</span><span class="sxs-lookup"><span data-stu-id="e4ee6-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="e4ee6-131">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Situazioni contabili** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e4ee6-132">Nella pagina **Descr. situazioni contabili** scegliere l'azione **Nuovo** per creare un nuovo nome della situazione contabile del conto di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="e4ee6-133">Nel campo **Nome** immettere **Previsione**.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="e4ee6-134">Nel campo **Descrizione** immettere **Previsione flusso di cassa**.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="e4ee6-135">Lasciare vuoti i campi **Default layout colonna** e **Nome visual. analisi**.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="e4ee6-136">Impostazione delle righe della situazione contabile</span><span class="sxs-lookup"><span data-stu-id="e4ee6-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="e4ee6-137">Dopo aver impostato un nome della situazione contabile, Ken definisce tutte le righe che verranno visualizzate nella situazione contabile del conto di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="e4ee6-138">Egli definisce le righe che possono essere visualizzate nei report, nonché le righe utilizzate solo per scopi di calcolo.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="e4ee6-139">Per impostare le righe della situazione contabile</span><span class="sxs-lookup"><span data-stu-id="e4ee6-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="e4ee6-140">Nella pagina **Descr. situazioni contabili** selezionare il nome della nuova situazione contabile **Previsione** creata.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="e4ee6-141">Nella scheda **Pagina iniziale** del gruppo **Processo** scegliere **Modifica situazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="e4ee6-142">Nella pagina **Situazione contabile** immettere ogni riga esattamente come indicato nella tabella riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e4ee6-143">Utilizzando la funzione **Inserisci conti di costo e nolo**, è possibile contrassegnare rapidamente i conti di cassa del relativo piano e copiarli nelle righe della situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="e4ee6-144">|Nr. Riga|Descrizione|Tipo totale|Totale|Tipo di riga|Tipo importo|Mostra|</span><span class="sxs-lookup"><span data-stu-id="e4ee6-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="e4ee6-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Importo|Saldo periodo|Movimenti|Importo netto|Sempre|</span><span class="sxs-lookup"><span data-stu-id="e4ee6-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="e4ee6-146">|C20|Importo fino alla data|Saldo alla data|Movimenti|Importo netto|Sempre|</span><span class="sxs-lookup"><span data-stu-id="e4ee6-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="e4ee6-147">|C30|Anno fiscale intero|Anno fiscale intero|Movimenti|Importo netto|Sempre|</span><span class="sxs-lookup"><span data-stu-id="e4ee6-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="e4ee6-148">Scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="e4ee6-149">Assegnazione del layout colonna al nome situaz. contabile.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="e4ee6-150">Ken è ora pronto per assegnare il layout colonna al nome della situazione contabile.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="e4ee6-151">Per assegnare il layout colonna al nome situaz. contabile.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="e4ee6-152">Nella pagina **Descr. situazioni contabili** selezionare **Previsione** nel campo **Nome**.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-152">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="e4ee6-153">Nel campo **Default layout colonna** selezionare il layout colonna **Flusso di cassa** da assegnare come layout colonna predefinito.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="e4ee6-154">Per visualizzare e stampare la previsione del flusso di cassa</span><span class="sxs-lookup"><span data-stu-id="e4ee6-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="e4ee6-155">Nella pagina **Descr. situazioni contabili**, scegliere l'azione **Sintesi** per visualizzare la previsione del flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-155">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="e4ee6-156">Nella pagina **Sintesi situaz. contabile** è possibile selezionare un importo e quindi visualizzare i movimenti di previsione del flusso di cassa che compongono l'importo.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-156">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="e4ee6-157">Inoltre, è possibile visualizzare la formula utilizzata per calcolare l'importo.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="e4ee6-158">È anche possibile filtrare gli importi per data e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="e4ee6-159">Scegliere l'azione **Stampa** per stampare la previsione del flusso di cassa.</span><span class="sxs-lookup"><span data-stu-id="e4ee6-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4ee6-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4ee6-160">See Also</span></span>  
 <span data-ttu-id="e4ee6-161">[Utilizzare le situazioni contabili](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="e4ee6-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="e4ee6-162">Procedure dettagliate per i processi aziendali</span><span class="sxs-lookup"><span data-stu-id="e4ee6-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="e4ee6-163">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4ee6-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
