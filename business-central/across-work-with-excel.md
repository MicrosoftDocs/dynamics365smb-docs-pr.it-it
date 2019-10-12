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
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 2474f83fd9fa137b40756a3d07ac025208f3ac6c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308262"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="2c0ef-103">Visualizzare e modificare in Excel da Business Central</span><span class="sxs-lookup"><span data-stu-id="2c0ef-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="2c0ef-104">Con le pagine che visualizzano un elenco di record in righe e colonne, come un elenco di clienti, ordini di vendita o fatture, è anche possibile visualizzare i record utilizzando Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="2c0ef-105">A questo proposito, sono disponibili due opzioni.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-105">To do this, you have two options.</span></span> <span data-ttu-id="2c0ef-106">È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="2c0ef-107">Di seguito sono descritte le differenze tra le due azioni:</span><span class="sxs-lookup"><span data-stu-id="2c0ef-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="2c0ef-108">Apri in Excel</span><span class="sxs-lookup"><span data-stu-id="2c0ef-108">Open in Excel</span></span>

-    <span data-ttu-id="2c0ef-109">Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="2c0ef-110">Ciò significa che la cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2c0ef-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="2c0ef-111">In Excel è possibile apportare modifiche ai record, ma non ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2c0ef-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2c0ef-112">È possibile salvare le modifiche solo in un file Excel nel computer.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="2c0ef-113">Questa azione è compatibile con Windows e macOS.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="2c0ef-114">Per [!INCLUDE[prodshort](includes/prodshort.md)] locale, l'azione **Apri in Excel** non è disponibile se è già presente l'azione **Modifica in Excel**.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="2c0ef-115">Modifica in Excel</span><span class="sxs-lookup"><span data-stu-id="2c0ef-115">Edit in Excel</span></span>

-    <span data-ttu-id="2c0ef-116">Con questa azione, la cartella di lavoro Excel non rispetta i filtri nella pagina che limitano i record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="2c0ef-117">Ciò significa che la cartella di lavoro Excel conterrà tutti i record e le colonne disponibili, indipendentemente da ciò che è visualizzato nella pagina.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="2c0ef-118">Il vantaggio dell'azione **Modifica in Excel** è che consente di apportare modifiche ai record in Excel e quindi di ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2c0ef-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="2c0ef-119">È compatibile con Windows ma non con macOS.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="2c0ef-120">Per [!INCLUDE[prodshort](includes/prodshort.md)] locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato installato dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="2c0ef-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="2c0ef-121">Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="2c0ef-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="2c0ef-122">Vedere le differenze tra le opzioni</span><span class="sxs-lookup"><span data-stu-id="2c0ef-122">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="2c0ef-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2c0ef-123">See Also</span></span>
[<span data-ttu-id="2c0ef-124">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="2c0ef-124">Working with Business Central</span></span>](ui-work-product.md)  
