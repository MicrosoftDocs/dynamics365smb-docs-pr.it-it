---
title: Utilizzo dei workflow | Microsoft Docs
description: È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6535523fb34504a4f964971f41d4803bdc7b2117
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304758"
---
# <a name="using-workflows"></a><span data-ttu-id="330ac-105">Utilizzo dei workflow</span><span class="sxs-lookup"><span data-stu-id="330ac-105">Using Workflows</span></span>
<span data-ttu-id="330ac-106">È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="330ac-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="330ac-107">I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti.</span><span class="sxs-lookup"><span data-stu-id="330ac-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="330ac-108">La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="330ac-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="330ac-109">Prima di poter iniziare a utilizzare i flussi di lavoro, è necessario impostare gli utenti del flusso di lavoro, creare i flussi di lavoro, potenzialmente preceduti dalla personalizzazione del codice, e specificare la modalità di ricezione delle notifiche da parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="330ac-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="330ac-110">Per ulteriori informazioni, vedere [Impostazione dei workflow](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="330ac-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="330ac-111">I passaggi di un flusso di lavoro tipici riguardano gli utenti che richiedono l'approvazione di attività e i responsabili dell'approvazione che accettano o rifiutano le richieste.</span><span class="sxs-lookup"><span data-stu-id="330ac-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="330ac-112">Di conseguenza, molti argomenti che trattano l'utilizzo dei workflow fanno riferimento alle approvazioni.</span><span class="sxs-lookup"><span data-stu-id="330ac-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="330ac-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="330ac-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="330ac-114">**Task**</span><span class="sxs-lookup"><span data-stu-id="330ac-114">**To**</span></span>|<span data-ttu-id="330ac-115">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="330ac-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="330ac-116">Impostare un flusso di lavoro per iniziare quando si verifica la prima spedizione Intrastat.</span><span class="sxs-lookup"><span data-stu-id="330ac-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="330ac-117">Abilitare i workflow</span><span class="sxs-lookup"><span data-stu-id="330ac-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="330ac-118">Richiedere l'approvazione di un task, come responsabile approvazione, accettare, declinare o delegare le approvazioni e inviare o visualizzare le notifiche di approvazione.</span><span class="sxs-lookup"><span data-stu-id="330ac-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="330ac-119">Utilizzare i workflow di approvazione</span><span class="sxs-lookup"><span data-stu-id="330ac-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="330ac-120">Creare le fasi del flusso di lavoro che limitano l'utilizzo di un certo tipo di record prima del verificarsi di un determinato evento, ad esempio l'approvazione del record.</span><span class="sxs-lookup"><span data-stu-id="330ac-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="330ac-121">Limitare e consentire l'utilizzo di un record</span><span class="sxs-lookup"><span data-stu-id="330ac-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="330ac-122">Visualizzare istanze dei passaggi del flusso di lavoro con lo stato Completato.</span><span class="sxs-lookup"><span data-stu-id="330ac-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="330ac-123">Visualizzare le istanze di fase workflow archiviate</span><span class="sxs-lookup"><span data-stu-id="330ac-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="330ac-124">Eliminare un flusso di lavoro che sicuramente non verrà più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="330ac-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="330ac-125">Eliminare i workflow</span><span class="sxs-lookup"><span data-stu-id="330ac-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="330ac-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="330ac-126">See Also</span></span>  
<span data-ttu-id="330ac-127">[Impostazione dei workflow](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="330ac-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="330ac-128">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="330ac-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="330ac-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="330ac-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
