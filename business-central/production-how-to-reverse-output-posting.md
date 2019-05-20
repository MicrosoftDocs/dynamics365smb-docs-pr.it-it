---
title: Come stornare la registrazione dell'output | Microsoft Docs
description: La registrazione dell'output deve essere stornata in tre casi diversi. È possibile, ad esempio, che si verifichi un errore di immissione dei dati e che in un ordine di produzione venga registrata una quantità di output non corretta.
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
ms.openlocfilehash: 09c8e38af535d5f178c2df8ce4513f199bfa4d1e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252989"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="44b94-104">Stornare la registrazione dell'output</span><span class="sxs-lookup"><span data-stu-id="44b94-104">Reverse Output Posting</span></span>
<span data-ttu-id="44b94-105">La registrazione dell'output deve essere stornata in tre casi diversi.</span><span class="sxs-lookup"><span data-stu-id="44b94-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="44b94-106">È possibile, ad esempio, che si verifichi un errore di immissione dei dati e che in un ordine di produzione venga registrata una quantità di output non corretta.</span><span class="sxs-lookup"><span data-stu-id="44b94-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="44b94-107">Per stornare una registrazione di output</span><span class="sxs-lookup"><span data-stu-id="44b94-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="44b94-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni output** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="44b94-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="44b94-109">Selezionare il batch.</span><span class="sxs-lookup"><span data-stu-id="44b94-109">Select your batch.</span></span>  
2. <span data-ttu-id="44b94-110">Compilare i campi come necessario.</span><span class="sxs-lookup"><span data-stu-id="44b94-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="44b94-111">Per ulteriori informazioni, vedere [Registrare l'output e i tempi di lavorazione tramite processo batch](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="44b94-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="44b94-112">Nel campo **Collega-a movimento** selezionare il movimento contabile articolo associato.</span><span class="sxs-lookup"><span data-stu-id="44b94-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="44b94-113">In questo modo, verranno stornati i movimenti contabili articolo e capacità.</span><span class="sxs-lookup"><span data-stu-id="44b94-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="44b94-114">Registrare lo storno mediante la contabilizzazione delle registrazioni.</span><span class="sxs-lookup"><span data-stu-id="44b94-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="44b94-115">I movimenti delle registrazioni di output verranno registrati nei movimenti contabili magazzino come rettifica positiva.</span><span class="sxs-lookup"><span data-stu-id="44b94-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44b94-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44b94-116">See Also</span></span>  
 <span data-ttu-id="44b94-117">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="44b94-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="44b94-118">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="44b94-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="44b94-119">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="44b94-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="44b94-120">Magazzino</span><span class="sxs-lookup"><span data-stu-id="44b94-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="44b94-121">Acquisti</span><span class="sxs-lookup"><span data-stu-id="44b94-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="44b94-122">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44b94-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
