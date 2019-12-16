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
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 99fe339426b755b70983d8ec9345858357043347
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808747"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="d905a-103">Visualizzare e modificare in Excel da Business Central</span><span class="sxs-lookup"><span data-stu-id="d905a-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="d905a-104">Con le pagine che visualizzano un elenco di record in righe e colonne, come un elenco di clienti, ordini di vendita o fatture, è anche possibile visualizzare i record utilizzando Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d905a-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="d905a-105">A questo proposito, sono disponibili due opzioni.</span><span class="sxs-lookup"><span data-stu-id="d905a-105">To do this, you have two options.</span></span> <span data-ttu-id="d905a-106">È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina.</span><span class="sxs-lookup"><span data-stu-id="d905a-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="d905a-107">Di seguito sono descritte le differenze tra le due azioni:</span><span class="sxs-lookup"><span data-stu-id="d905a-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="d905a-108">Apri in Excel</span><span class="sxs-lookup"><span data-stu-id="d905a-108">Open in Excel</span></span>

- <span data-ttu-id="d905a-109">Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d905a-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="d905a-110">Ciò significa che la cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d905a-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="d905a-111">In Excel è possibile apportare modifiche ai record, ma non ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d905a-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="d905a-112">È possibile salvare le modifiche solo in un file Excel nel computer.</span><span class="sxs-lookup"><span data-stu-id="d905a-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="d905a-113">Questa azione è compatibile con Windows e macOS.</span><span class="sxs-lookup"><span data-stu-id="d905a-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="d905a-114">Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale l'azione **Apri in Excel** è disponibile per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d905a-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="d905a-115">Tuttavia, se [!INCLUDE [prodshort](includes/prodshort.md)] in locale è configurato per la modifica dei dati in Excel, l'azione **Apri in Excel** è sostituita dall'azione **Modifica in Excel**.</span><span class="sxs-lookup"><span data-stu-id="d905a-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="d905a-116">Modifica in Excel</span><span class="sxs-lookup"><span data-stu-id="d905a-116">Edit in Excel</span></span>

- <span data-ttu-id="d905a-117">Con questa azione, Excel rispetta la maggior parte dei filtri nella pagina che limitano i record visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d905a-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="d905a-118">Ciò significa che la cartella di lavoro Excel conterrà quasi gli stessi record e le stesse colonne.</span><span class="sxs-lookup"><span data-stu-id="d905a-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="d905a-119">Il vantaggio dell'azione **Modifica in Excel** è che consente di apportare modifiche ai record in Excel e quindi di ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d905a-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="d905a-120">È compatibile con Windows ma non con macOS.</span><span class="sxs-lookup"><span data-stu-id="d905a-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="d905a-121">Ciò è stato migliorato nella seconda ondata di rilascio del 2019.</span><span class="sxs-lookup"><span data-stu-id="d905a-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="d905a-122">Per ulteriori informazioni, vedere [Miglioramenti all'integrazione di Excel](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="d905a-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="d905a-123">Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato configurato dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="d905a-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="d905a-124">Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="d905a-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="d905a-125">Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale, questa funzione è disponibile solo per il client Web.</span><span class="sxs-lookup"><span data-stu-id="d905a-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="d905a-126">Vedere le differenze tra le opzioni</span><span class="sxs-lookup"><span data-stu-id="d905a-126">See the differences between the options</span></span> 
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="d905a-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d905a-127">See Also</span></span>
[<span data-ttu-id="d905a-128">Utilizzo di Business Central</span><span class="sxs-lookup"><span data-stu-id="d905a-128">Working with Business Central</span></span>](ui-work-product.md)  
