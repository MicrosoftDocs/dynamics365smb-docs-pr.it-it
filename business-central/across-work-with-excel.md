---
title: Visualizzare e modificare in Excel da Business Central
description: Informazioni su come aprire le pagine in Microsoft Excel da Business Central per una migliore analisi dei dati.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786934"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="2aedc-103">Visualizzare e modificare in Excel da Business Central</span><span class="sxs-lookup"><span data-stu-id="2aedc-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="2aedc-104">Con le pagine che visualizzano un elenco di record in righe e colonne, come un elenco di clienti, ordini di vendita o fatture, è anche possibile visualizzare i record utilizzando Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2aedc-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="2aedc-105">A questo proposito, sono disponibili due opzioni.</span><span class="sxs-lookup"><span data-stu-id="2aedc-105">To do this, you have two options.</span></span> <span data-ttu-id="2aedc-106">È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina.</span><span class="sxs-lookup"><span data-stu-id="2aedc-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="2aedc-107">Di seguito sono descritte le differenze tra le due azioni:</span><span class="sxs-lookup"><span data-stu-id="2aedc-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="2aedc-108">Apri in Excel</span><span class="sxs-lookup"><span data-stu-id="2aedc-108">Open in Excel</span></span>

- <span data-ttu-id="2aedc-109">Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="2aedc-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="2aedc-110">La cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2aedc-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="2aedc-111">In Excel è possibile apportare modifiche ai record, ma non ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2aedc-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2aedc-112">È possibile salvare le modifiche solo in un file Excel nel computer.</span><span class="sxs-lookup"><span data-stu-id="2aedc-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="2aedc-113">Questa azione è compatibile con Windows e macOS.</span><span class="sxs-lookup"><span data-stu-id="2aedc-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="2aedc-114">Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale l'azione **Apri in Excel** è disponibile per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2aedc-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="2aedc-115">Tuttavia, se [!INCLUDE[prod_short](includes/prod_short.md)] in locale è configurato per la modifica dei dati in Excel, l'azione **Apri in Excel** è sostituita dall'azione **Modifica in Excel**.</span><span class="sxs-lookup"><span data-stu-id="2aedc-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="2aedc-116">Modifica in Excel</span><span class="sxs-lookup"><span data-stu-id="2aedc-116">Edit in Excel</span></span>

- <span data-ttu-id="2aedc-117">Con questa azione, Excel rispetta la maggior parte dei filtri sulla pagina che limitano i record visualizzati, quindi la cartella di lavoro di Excel conterrà quasi gli stessi record e colonne.</span><span class="sxs-lookup"><span data-stu-id="2aedc-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="2aedc-118">Il vantaggio dell'azione **Modifica in Excel** è che consente di apportare modifiche ai record in Excel e quindi di ripubblicare le modifiche in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2aedc-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="2aedc-119">È compatibile con Windows ma non con macOS.</span><span class="sxs-lookup"><span data-stu-id="2aedc-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="2aedc-120">Puoi cambiare la società con cui stai lavorando.</span><span class="sxs-lookup"><span data-stu-id="2aedc-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="2aedc-121">Per cambiare la società, seleziona l'icona **Opzioni** ![Opzioni del componente aggiuntivo di Excel](media/cogwheel.png "Opzioni del componente aggiuntivo per Excel") nel riquadro del componente aggiuntivo di Excel, quindi seleziona la società nel campo **Società**.</span><span class="sxs-lookup"><span data-stu-id="2aedc-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="2aedc-122">Quando si cambia la società, assicurarsi che il campo **Ambiente** non sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="2aedc-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="2aedc-123">In tal caso, impostarlo su una delle opzioni disponibili; in caso contrario, il componente aggiuntivo non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="2aedc-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="2aedc-124">Se si apportano modifiche al componente aggiuntivo, è necessario ricaricarlo per aggiornare la connessione.</span><span class="sxs-lookup"><span data-stu-id="2aedc-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="2aedc-125">Per ricaricare, utilizzare il ![menu del componente aggiuntivo per Excel](media/excel-addin-menu.png "Menu del componente aggiuntivo per Excel") nell'angolo in alto a destra del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="2aedc-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="2aedc-126">Se non riesci a caricare il componente aggiuntivo, contatta l'amministratore.</span><span class="sxs-lookup"><span data-stu-id="2aedc-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="2aedc-127">Se sei l'amministratore, vedi [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="2aedc-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="2aedc-128">Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato configurato dall'amministratore ed è disponibile solo per il client Web.</span><span class="sxs-lookup"><span data-stu-id="2aedc-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="2aedc-129">Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="2aedc-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="2aedc-130">Vedere le differenze tra le opzioni</span><span class="sxs-lookup"><span data-stu-id="2aedc-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="2aedc-131">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="2aedc-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="2aedc-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2aedc-132">See Also</span></span>

[<span data-ttu-id="2aedc-133">Analisi dei rendiconti finanziari in Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="2aedc-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="2aedc-134">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="2aedc-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="2aedc-135">Miglioramenti all'integrazione di Excel nella seconda ondata di rilascio del 2019</span><span class="sxs-lookup"><span data-stu-id="2aedc-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]