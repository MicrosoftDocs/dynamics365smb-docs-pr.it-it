---
title: 'Procedura: Creare report elettronici di transazioni IVA'
description: È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata. Inviare il report alle autorità fiscali.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 486732b9b5d8b4ec5f7acbec08dafe0eb9eff3b3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749638"
---
# <a name="create-electronic-vat-transactions-reports"></a><span data-ttu-id="1384e-104">Creare report elettronici di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="1384e-104">Create Electronic VAT Transactions Reports</span></span>
<span data-ttu-id="1384e-105">È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata.</span><span class="sxs-lookup"><span data-stu-id="1384e-105">You must create a list of transactions that include VAT with amounts over the current threshold on or before the specified occurrence date.</span></span> <span data-ttu-id="1384e-106">Inviare il report alle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="1384e-106">You submit this report to the tax authorities.</span></span>  

## <a name="to-create-a-vat-transactions-report"></a><span data-ttu-id="1384e-107">Per creare un report di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="1384e-107">To create a VAT transactions report</span></span>  

1.  <span data-ttu-id="1384e-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Report IVA** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1384e-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Report**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1384e-109">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1384e-109">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1384e-110">Campo</span><span class="sxs-lookup"><span data-stu-id="1384e-110">Field</span></span>|<span data-ttu-id="1384e-111">Description</span><span class="sxs-lookup"><span data-stu-id="1384e-111">Description</span></span>|  
    |-------------------------------------|---------------------------------------|  
    |<span data-ttu-id="1384e-112">**Senza contratto**</span><span class="sxs-lookup"><span data-stu-id="1384e-112">**Without Contract**</span></span>|<span data-ttu-id="1384e-113">I movimenti IVA che hanno generato questa riga non sono associati a un contratto.</span><span class="sxs-lookup"><span data-stu-id="1384e-113">The VAT entries that resulted in this line are not associated with a contract.</span></span>|  
    |<span data-ttu-id="1384e-114">**Contratto**</span><span class="sxs-lookup"><span data-stu-id="1384e-114">**Contract**</span></span>|<span data-ttu-id="1384e-115">I movimenti IVA che hanno generato questa riga sono associati a un contratto.</span><span class="sxs-lookup"><span data-stu-id="1384e-115">The VAT entries that resulted in this line are associated with a contract.</span></span>|  
    |<span data-ttu-id="1384e-116">**Altro**</span><span class="sxs-lookup"><span data-stu-id="1384e-116">**Other**</span></span>|<span data-ttu-id="1384e-117">I movimenti IVA che hanno generato questa riga non sono associati a un contratto speciale, ad esempio per manutenzione in corso o altre eccezioni.</span><span class="sxs-lookup"><span data-stu-id="1384e-117">The VAT entries that resulted in this line are not associated with a special contract, such as ongoing maintenance or other exceptions.</span></span>|  

    > [!TIP]  
    >  <span data-ttu-id="1384e-118">In [!INCLUDE[prod_short](../../includes/prod_short.md)], il contratto che le autorità fiscali cercano può essere ordini programmati oppure contratti di assistenza.</span><span class="sxs-lookup"><span data-stu-id="1384e-118">In [!INCLUDE[prod_short](../../includes/prod_short.md)], the contract that the tax authorities are looking for can be blanket orders or service contracts.</span></span> <span data-ttu-id="1384e-119">Per identificare se la riga del report IVA appartiene a un ordine programmato o a un contratto di assistenza, è possibile eseguire il drill-down per visualizzare i movimenti IVA sottostanti dal campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="1384e-119">To identify if the VAT report line belongs to a blanket order or service contract, you can drill down to see the underlying VAT entries from the **Amount** field.</span></span>  

<span data-ttu-id="1384e-120">Le note di credito vengono incluse nel report transazioni IVA se il cliente o il fornitore è di un paese esterno all'UE e non incluso nella blacklist.</span><span class="sxs-lookup"><span data-stu-id="1384e-120">Credit memos are included in the VAT transaction report if the customer or vendor is from a country/region that is outside the EU and not black-listed.</span></span> <span data-ttu-id="1384e-121">Per ulteriori informazioni, vedere [IVA italiana](italian-vat.md).</span><span class="sxs-lookup"><span data-stu-id="1384e-121">For more information, see [Italian VAT](italian-vat.md).</span></span>  

<span data-ttu-id="1384e-122">Dopo avere creato il report IVA, è necessario inviarlo alle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="1384e-122">Now that you have created the VAT report, you must submit it to the tax authorities.</span></span> <span data-ttu-id="1384e-123">Per ulteriori informazioni, vedere [Esportare i report di transazioni IVA](how-to-export-vat-transactions-reports.md).</span><span class="sxs-lookup"><span data-stu-id="1384e-123">For more information, see [Export VAT Transactions Reports](how-to-export-vat-transactions-reports.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="1384e-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1384e-124">See Also</span></span>  
 [<span data-ttu-id="1384e-125">IVA italiana</span><span class="sxs-lookup"><span data-stu-id="1384e-125">Italian VAT</span></span>](italian-vat.md)
