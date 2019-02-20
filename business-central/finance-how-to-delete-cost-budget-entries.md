---
title: Come eliminare i movimenti di budget costi | Microsoft Docs
description: Utilizzare il processo batch Elimina mov. budget costi per annullare i movimenti di budget costi dal registro budget costi.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 7a5647bcb5a58cdf0a38ec037994d6cbe7a9504d
ms.contentlocale: it-it
ms.lasthandoff: 11/29/2018

---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="fb0d2-103">Elimina mov. budget costi</span><span class="sxs-lookup"><span data-stu-id="fb0d2-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="fb0d2-104">Utilizzare il processo batch **Elimina mov. budget costi** per annullare i movimenti di budget costi dal registro budget costi.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="fb0d2-105">Per evitare qualsiasi gap nei movimenti di budget costi e nei movimenti del registro dei costi, non è possibile eliminare un unico movimento o un batch di movimenti a metà della lista dei movimenti del registro.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="fb0d2-106">Per eliminare un mov. budget costi</span><span class="sxs-lookup"><span data-stu-id="fb0d2-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="fb0d2-107">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina mov. budget costi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="fb0d2-108">Nel campo **A nr. registro**</span><span class="sxs-lookup"><span data-stu-id="fb0d2-108">The **To Register No.**</span></span> <span data-ttu-id="fb0d2-109">è incluso l'ultimo numero del movimento del registro e non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="fb0d2-110">È possibile utilizzare il campo **Da nr. registro**</span><span class="sxs-lookup"><span data-stu-id="fb0d2-110">You can use the **From Register No.**</span></span> <span data-ttu-id="fb0d2-111">per selezionare un numero di movimento del registro dal quale iniziare l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="fb0d2-112">Scegliere il pulsante **OK** per eliminare i movimenti di bugdet costi selezionati.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="fb0d2-113">Per evitare un'eliminazione accidentale dei movimenti di budget costi, è possibile chiudere i movimenti del registro contrassegnando le righe come **Chiuso** nel campo **Chiuso** della pagina **Registri budget costi**.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb0d2-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb0d2-114">See Also</span></span>  
<span data-ttu-id="fb0d2-115">[Contabilizzazione dei costi](finance-manage-cost-accounting.md)
[Creazione di budget di costi](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="fb0d2-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="fb0d2-116">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fb0d2-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

