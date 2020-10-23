---
title: Visualizzare e modificare in Excel da Business Central | Microsoft Docs
description: Informazioni su come aprire le pagine in Microsoft Excel da Business Central per una migliore analisi dei dati.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: b25413c8f0479aaccfc67ae96f2870690f993dfa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927274"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="feb07-103">Visualizzare e modificare in Excel da Business Central</span><span class="sxs-lookup"><span data-stu-id="feb07-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="feb07-104">Con le pagine che visualizzano un elenco di record in righe e colonne, come un elenco di clienti, ordini di vendita o fatture, è anche possibile visualizzare i record utilizzando Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="feb07-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="feb07-105">A questo proposito, sono disponibili due opzioni.</span><span class="sxs-lookup"><span data-stu-id="feb07-105">To do this, you have two options.</span></span> <span data-ttu-id="feb07-106">È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina.</span><span class="sxs-lookup"><span data-stu-id="feb07-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="feb07-107">Di seguito sono descritte le differenze tra le due azioni:</span><span class="sxs-lookup"><span data-stu-id="feb07-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="feb07-108">Apri in Excel</span><span class="sxs-lookup"><span data-stu-id="feb07-108">Open in Excel</span></span>

- <span data-ttu-id="feb07-109">Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="feb07-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="feb07-110">Ciò significa che la cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="feb07-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="feb07-111">In Excel è possibile apportare modifiche ai record, ma non ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="feb07-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="feb07-112">È possibile salvare le modifiche solo in un file Excel nel computer.</span><span class="sxs-lookup"><span data-stu-id="feb07-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="feb07-113">Questa azione è compatibile con Windows e macOS.</span><span class="sxs-lookup"><span data-stu-id="feb07-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="feb07-114">Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale l'azione **Apri in Excel** è disponibile per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="feb07-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="feb07-115">Tuttavia, se [!INCLUDE[prodshort](includes/prodshort.md)] in locale è configurato per la modifica dei dati in Excel, l'azione **Apri in Excel** è sostituita dall'azione **Modifica in Excel**.</span><span class="sxs-lookup"><span data-stu-id="feb07-115">However, if you set up [!INCLUDE[prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="feb07-116">Modifica in Excel</span><span class="sxs-lookup"><span data-stu-id="feb07-116">Edit in Excel</span></span>

- <span data-ttu-id="feb07-117">Con questa azione, Excel rispetta la maggior parte dei filtri nella pagina che limitano i record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="feb07-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="feb07-118">Ciò significa che la cartella di lavoro Excel conterrà quasi gli stessi record e le stesse colonne.</span><span class="sxs-lookup"><span data-stu-id="feb07-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="feb07-119">Il vantaggio dell'azione **Modifica in Excel** è che consente di apportare modifiche ai record in Excel e quindi di ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="feb07-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="feb07-120">È compatibile con Windows ma non con macOS.</span><span class="sxs-lookup"><span data-stu-id="feb07-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="feb07-121">Puoi cambiare la società con cui stai lavorando.</span><span class="sxs-lookup"><span data-stu-id="feb07-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="feb07-122">Per fare ciò, selezionare l'icona **Opzioni** ![Opzioni del componente aggiuntivo di Excel](media/cogwheel.png "Opzioni del componente aggiuntivo per Excel") nel riquadro del componente aggiuntivo di Excel, quindi seleziona la società dal campo **Società**.</span><span class="sxs-lookup"><span data-stu-id="feb07-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="feb07-123">Quando si cambia la società, assicurarsi che il campo **Ambiente** non sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="feb07-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="feb07-124">In tal caso, impostarlo su una delle opzioni disponibili; in caso contrario, il componente aggiuntivo non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="feb07-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="feb07-125">Se si apportano modifiche al componente aggiuntivo, è necessario ricaricarlo per aggiornare la connessione.</span><span class="sxs-lookup"><span data-stu-id="feb07-125">If you make changes to the add-in, you must reload it in order to update the connection.</span></span> <span data-ttu-id="feb07-126">Per ricaricare, utilizzare il ![menu del componente aggiuntivo per Excel](media/excel-addin-menu.png "Menu del componente aggiuntivo per Excel") nell'angolo in alto a destra del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="feb07-126">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span>

> [!NOTE]
> <span data-ttu-id="feb07-127">Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato configurato dall'amministratore ed è disponibile solo per il client Web.</span><span class="sxs-lookup"><span data-stu-id="feb07-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="feb07-128">Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="feb07-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="feb07-129">Vedere le differenze tra le opzioni</span><span class="sxs-lookup"><span data-stu-id="feb07-129">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="feb07-130">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="feb07-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="feb07-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="feb07-131">See Also</span></span>

[<span data-ttu-id="feb07-132">Analisi dei rendiconti finanziari in Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="feb07-132">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="feb07-133">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="feb07-133">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="feb07-134">Miglioramenti all'integrazione di Excel nella seconda ondata di rilascio del 2019</span><span class="sxs-lookup"><span data-stu-id="feb07-134">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
