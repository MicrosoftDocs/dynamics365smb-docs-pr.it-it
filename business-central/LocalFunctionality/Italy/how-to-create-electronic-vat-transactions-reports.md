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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8d8f726dd8db734e187e3da71f0876432441d750
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676544"
---
# <a name="create-electronic-vat-transactions-reports"></a><span data-ttu-id="9da4b-104">Creare report elettronici di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="9da4b-104">Create Electronic VAT Transactions Reports</span></span>
<span data-ttu-id="9da4b-105">È necessario creare una lista di transazioni che includono l'IVA con importi oltre la soglia corrente effettuati entro la data specificata.</span><span class="sxs-lookup"><span data-stu-id="9da4b-105">You must create a list of transactions that include VAT with amounts over the current threshold on or before the specified occurrence date.</span></span> <span data-ttu-id="9da4b-106">Inviare il report alle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="9da4b-106">You submit this report to the tax authorities.</span></span>  

## <a name="to-create-a-vat-transactions-report"></a><span data-ttu-id="9da4b-107">Per creare un report di transazioni IVA</span><span class="sxs-lookup"><span data-stu-id="9da4b-107">To create a VAT transactions report</span></span>  

1.  <span data-ttu-id="9da4b-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Report IVA** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9da4b-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Report**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9da4b-109">Compilare i campi come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9da4b-109">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9da4b-110">Campo</span><span class="sxs-lookup"><span data-stu-id="9da4b-110">Field</span></span>|<span data-ttu-id="9da4b-111">Description</span><span class="sxs-lookup"><span data-stu-id="9da4b-111">Description</span></span>|  
    |-------------------------------------|---------------------------------------|  
    |<span data-ttu-id="9da4b-112">**Senza contratto**</span><span class="sxs-lookup"><span data-stu-id="9da4b-112">**Without Contract**</span></span>|<span data-ttu-id="9da4b-113">I movimenti IVA che hanno generato questa riga non sono associati a un contratto.</span><span class="sxs-lookup"><span data-stu-id="9da4b-113">The VAT entries that resulted in this line are not associated with a contract.</span></span>|  
    |<span data-ttu-id="9da4b-114">**Contratto**</span><span class="sxs-lookup"><span data-stu-id="9da4b-114">**Contract**</span></span>|<span data-ttu-id="9da4b-115">I movimenti IVA che hanno generato questa riga sono associati a un contratto.</span><span class="sxs-lookup"><span data-stu-id="9da4b-115">The VAT entries that resulted in this line are associated with a contract.</span></span>|  
    |<span data-ttu-id="9da4b-116">**Altro**</span><span class="sxs-lookup"><span data-stu-id="9da4b-116">**Other**</span></span>|<span data-ttu-id="9da4b-117">I movimenti IVA che hanno generato questa riga non sono associati a un contratto speciale, ad esempio per manutenzione in corso o altre eccezioni.</span><span class="sxs-lookup"><span data-stu-id="9da4b-117">The VAT entries that resulted in this line are not associated with a special contract, such as ongoing maintenance or other exceptions.</span></span>|  

    > [!TIP]  
    >  <span data-ttu-id="9da4b-118">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], il contratto che le autorità fiscali cercano può essere ordini programmati oppure contratti di assistenza.</span><span class="sxs-lookup"><span data-stu-id="9da4b-118">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], the contract that the tax authorities are looking for can be blanket orders or service contracts.</span></span> <span data-ttu-id="9da4b-119">Per identificare se la riga del report IVA appartiene a un ordine programmato o a un contratto di assistenza, è possibile eseguire il drill-down per visualizzare i movimenti IVA sottostanti dal campo **Importo**.</span><span class="sxs-lookup"><span data-stu-id="9da4b-119">To identify if the VAT report line belongs to a blanket order or service contract, you can drill down to see the underlying VAT entries from the **Amount** field.</span></span>  

<span data-ttu-id="9da4b-120">Le note di credito vengono incluse nel report transazioni IVA se il cliente o il fornitore è di un paese esterno all'UE e non incluso nella blacklist.</span><span class="sxs-lookup"><span data-stu-id="9da4b-120">Credit memos are included in the VAT transaction report if the customer or vendor is from a country/region that is outside the EU and not black-listed.</span></span> <span data-ttu-id="9da4b-121">Per ulteriori informazioni, vedere [IVA italiana](italian-vat.md).</span><span class="sxs-lookup"><span data-stu-id="9da4b-121">For more information, see [Italian VAT](italian-vat.md).</span></span>  

<span data-ttu-id="9da4b-122">Dopo avere creato il report IVA, è necessario inviarlo alle autorità fiscali.</span><span class="sxs-lookup"><span data-stu-id="9da4b-122">Now that you have created the VAT report, you must submit it to the tax authorities.</span></span> <span data-ttu-id="9da4b-123">Per ulteriori informazioni, vedere [Esportare i report di transazioni IVA](how-to-export-vat-transactions-reports.md).</span><span class="sxs-lookup"><span data-stu-id="9da4b-123">For more information, see [Export VAT Transactions Reports](how-to-export-vat-transactions-reports.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="9da4b-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9da4b-124">See Also</span></span>  
 [<span data-ttu-id="9da4b-125">IVA italiana</span><span class="sxs-lookup"><span data-stu-id="9da4b-125">Italian VAT</span></span>](italian-vat.md)
