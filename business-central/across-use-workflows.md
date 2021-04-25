---
title: Utilizzo dei workflow
description: È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. Informazioni sui differenti passaggi da eseguire per iniziare a utilizzare i flussi di lavoro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92b32957bb7b20dda304be8a99bb17c5c5947498
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787009"
---
# <a name="using-workflows"></a><span data-ttu-id="e7ef4-104">Utilizzo dei workflow</span><span class="sxs-lookup"><span data-stu-id="e7ef4-104">Using Workflows</span></span>
<span data-ttu-id="e7ef4-105">È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="e7ef4-106">I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="e7ef4-107">La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="e7ef4-108">Prima di poter iniziare a utilizzare i flussi di lavoro, è necessario impostare gli utenti del flusso di lavoro, creare i flussi di lavoro, potenzialmente preceduti dalla personalizzazione del codice, e specificare la modalità di ricezione delle notifiche da parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="e7ef4-109">Per ulteriori informazioni, vedere [Impostazione dei workflow](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="e7ef4-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e7ef4-110">I passaggi di un flusso di lavoro tipici riguardano gli utenti che richiedono l'approvazione di attività e i responsabili dell'approvazione che accettano o rifiutano le richieste.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="e7ef4-111">Di conseguenza, molti argomenti che trattano l'utilizzo dei workflow fanno riferimento alle approvazioni.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="e7ef4-112">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="e7ef4-113">**Task**</span><span class="sxs-lookup"><span data-stu-id="e7ef4-113">**To**</span></span>|<span data-ttu-id="e7ef4-114">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="e7ef4-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e7ef4-115">Impostare un flusso di lavoro per iniziare quando si verifica la prima spedizione Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="e7ef4-116">Abilitare i workflow</span><span class="sxs-lookup"><span data-stu-id="e7ef4-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="e7ef4-117">Richiedere l'approvazione di un task, come responsabile approvazione, accettare, declinare o delegare le approvazioni e inviare o visualizzare le notifiche di approvazione.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="e7ef4-118">Utilizzare i workflow di approvazione</span><span class="sxs-lookup"><span data-stu-id="e7ef4-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="e7ef4-119">Creare le fasi del flusso di lavoro che limitano l'utilizzo di un certo tipo di record prima del verificarsi di un determinato evento, ad esempio l'approvazione del record.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="e7ef4-120">Limitare e consentire l'utilizzo di un record</span><span class="sxs-lookup"><span data-stu-id="e7ef4-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="e7ef4-121">Visualizzare istanze dei passaggi del flusso di lavoro con lo stato Completato.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="e7ef4-122">Visualizzare le istanze di fase workflow archiviate</span><span class="sxs-lookup"><span data-stu-id="e7ef4-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="e7ef4-123">Eliminare un flusso di lavoro che sicuramente non verrà più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e7ef4-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="e7ef4-124">Eliminare i workflow</span><span class="sxs-lookup"><span data-stu-id="e7ef4-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="e7ef4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7ef4-125">See Also</span></span>  
<span data-ttu-id="e7ef4-126">[Impostazione dei workflow](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e7ef4-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="e7ef4-127">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="e7ef4-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="e7ef4-128">[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e7ef4-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]