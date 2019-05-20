---
title: Come registrare il consumo tramite processo batch | Microsoft Docs
description: Se il metodo di consuntivazione è **Manuale**, i componenti devono essere registrati manualmente nelle registrazioni consumi.
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
ms.openlocfilehash: 121dec9b91d0dd5215d9953e50154873a5ae2402
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253610"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="1f680-103">Registrare il consumo produzione tramite processo batch</span><span class="sxs-lookup"><span data-stu-id="1f680-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="1f680-104">Se il metodo di consuntivazione è **Manuale**, i componenti devono essere registrati manualmente nelle registrazioni consumi.</span><span class="sxs-lookup"><span data-stu-id="1f680-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="1f680-105">È inoltre possibile impostare il sistema sulla registrazione (*consuntivazione*) automatica dei componenti quando si avviano o si chiudono ordini di produzione.</span><span class="sxs-lookup"><span data-stu-id="1f680-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="1f680-106">Per ulteriori informazioni vedere [Attivare la consuntivazione dei componenti in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="1f680-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="1f680-107">Per registrare il consumo per una o più righe dell'ordine di produzione</span><span class="sxs-lookup"><span data-stu-id="1f680-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="1f680-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni consumi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1f680-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1f680-109">Compilare i campi inserendo i dati relativi agli ordini di produzione e al consumo.</span><span class="sxs-lookup"><span data-stu-id="1f680-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="1f680-110">Se l'ubicazione della warehouse in cui sono immagazzinati i componenti prevede l'utilizzo di collocazioni, ma non richiede l'elaborazione dei prelievi, assegnare un codice collocazione alla riga delle registrazioni per indicare da dove dovranno essere prelevati gli articoli nella warehouse.</span><span class="sxs-lookup"><span data-stu-id="1f680-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="1f680-111">Per ulteriori informazioni, vedere [Prelevare per la produzione o l'assemblaggio](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="1f680-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="1f680-112">Per registrare il consumo scegliere l'azione **Registra**.</span><span class="sxs-lookup"><span data-stu-id="1f680-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="1f680-113">I movimenti articolo collegati vengono ridotti.</span><span class="sxs-lookup"><span data-stu-id="1f680-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f680-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f680-114">See Also</span></span>  
<span data-ttu-id="1f680-115">[Manufacturing](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1f680-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="1f680-116">Impostazione della produzione</span><span class="sxs-lookup"><span data-stu-id="1f680-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="1f680-117">[Pianif.](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="1f680-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="1f680-118">Magazzino</span><span class="sxs-lookup"><span data-stu-id="1f680-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1f680-119">Acquisti</span><span class="sxs-lookup"><span data-stu-id="1f680-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1f680-120">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1f680-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
