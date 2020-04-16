---
title: Impostare i processi di troubleshooting | Documenti Microsoft
description: Informazioni su come impostare i processi che consentono ai rappresentanti dell'assistenza di identificare e risolvere i problemi con gli articoli in assistenza.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2e962552bf091e095a968f6f312e852e02aad8d6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195015"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="9e372-103">Impostazione del troubleshooting per gli articoli in assistenza</span><span class="sxs-lookup"><span data-stu-id="9e372-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="9e372-104">È possibile impostare delle indicazioni di troubleshooting per consentire ai tecnici di risolvere i problemi mentre forniscono assistenza.</span><span class="sxs-lookup"><span data-stu-id="9e372-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="9e372-105">Tali indicazioni potrebbero essere, ad esempio, un elenco di passaggi da eseguire per una riparazione o una serie di domande da chiedere in merito agli articoli.</span><span class="sxs-lookup"><span data-stu-id="9e372-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="9e372-106">Dopo aver impostato le indicazioni di troubleshooting, è possibile assegnarle ai gruppi di articoli di assistenza, agli articoli o agli articoli in assistenza.</span><span class="sxs-lookup"><span data-stu-id="9e372-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="9e372-107">Esiste una gerarchia di ereditarietà per le indicazioni.</span><span class="sxs-lookup"><span data-stu-id="9e372-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="9e372-108">Se le indicazioni vengono assegnate a un gruppo di articoli in assistenza, gli articoli inclusi in tale gruppo le erediteranno a meno che non ne vengano specificate altre.</span><span class="sxs-lookup"><span data-stu-id="9e372-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="9e372-109">Analogamente, gli articoli in assistenza erediteranno tutte le indicazioni dagli articoli.</span><span class="sxs-lookup"><span data-stu-id="9e372-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="9e372-110">Per impostare le indicazioni di troubleshooting</span><span class="sxs-lookup"><span data-stu-id="9e372-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="9e372-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Risoluzione dei problemi** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9e372-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9e372-112">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="9e372-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="9e372-113">Per assegnare le indicazioni di troubleshooting ai gruppi di articoli di assistenza, agli articoli o agli articoli di assistenza</span><span class="sxs-lookup"><span data-stu-id="9e372-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="9e372-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli**, **Articoli in assistenza** o **Gruppi articoli in assistenza** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="9e372-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9e372-115">Scegliere l'entità appropriata, quindi scegliere l'azione **Troubleshooting**.</span><span class="sxs-lookup"><span data-stu-id="9e372-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9e372-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9e372-116">See Also</span></span>
[<span data-ttu-id="9e372-117">Gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="9e372-117">Service Management</span></span>](service-service.md)