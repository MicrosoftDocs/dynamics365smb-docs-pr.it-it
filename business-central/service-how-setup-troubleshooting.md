---
title: Impostare i processi di troubleshooting | Documenti Microsoft
description: Informazioni su come impostare i processi che consentono ai rappresentanti dell'assistenza di identificare e risolvere i problemi con gli articoli in assistenza.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2dfa02f0054cab20605281bb1cc580b522b893fd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "937483"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="00f16-103">Impostazione del troubleshooting per gli articoli in assistenza</span><span class="sxs-lookup"><span data-stu-id="00f16-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="00f16-104">È possibile impostare delle indicazioni di troubleshooting per consentire ai tecnici di risolvere i problemi mentre forniscono assistenza.</span><span class="sxs-lookup"><span data-stu-id="00f16-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="00f16-105">Tali indicazioni potrebbero essere, ad esempio, un elenco di passaggi da eseguire per una riparazione o una serie di domande da chiedere in merito agli articoli.</span><span class="sxs-lookup"><span data-stu-id="00f16-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="00f16-106">Dopo aver impostato le indicazioni di troubleshooting, è possibile assegnarle ai gruppi di articoli di assistenza, agli articoli o agli articoli in assistenza.</span><span class="sxs-lookup"><span data-stu-id="00f16-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="00f16-107">Esiste una gerarchia di ereditarietà per le indicazioni.</span><span class="sxs-lookup"><span data-stu-id="00f16-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="00f16-108">Se le indicazioni vengono assegnate a un gruppo di articoli in assistenza, gli articoli inclusi in tale gruppo le erediteranno a meno che non ne vengano specificate altre.</span><span class="sxs-lookup"><span data-stu-id="00f16-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="00f16-109">Analogamente, gli articoli in assistenza erediteranno tutte le indicazioni dagli articoli.</span><span class="sxs-lookup"><span data-stu-id="00f16-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="00f16-110">Per impostare le indicazioni di troubleshooting</span><span class="sxs-lookup"><span data-stu-id="00f16-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="00f16-111">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Troubleshooting** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="00f16-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="00f16-112">Compilare i campi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="00f16-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="00f16-113">Per assegnare le indicazioni di troubleshooting ai gruppi di articoli di assistenza, agli articoli o agli articoli di assistenza</span><span class="sxs-lookup"><span data-stu-id="00f16-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="00f16-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli**, **Articoli assistenza** o **Gruppi articoli in assistenza** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="00f16-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="00f16-115">Scegliere l'entità appropriata, quindi scegliere l'azione **Troubleshooting**.</span><span class="sxs-lookup"><span data-stu-id="00f16-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="00f16-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00f16-116">See Also</span></span>
[<span data-ttu-id="00f16-117">Gestione assistenza</span><span class="sxs-lookup"><span data-stu-id="00f16-117">Service Management</span></span>](service-service.md)