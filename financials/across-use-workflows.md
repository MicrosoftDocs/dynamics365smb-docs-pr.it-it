---
title: Utilizzo dei workflow | Microsoft Docs
description: "È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a42e336dba385cbf24c19702ad64d76b26c15104
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="using-workflows"></a><span data-ttu-id="e3afd-105">Utilizzo dei workflow</span><span class="sxs-lookup"><span data-stu-id="e3afd-105">Using Workflows</span></span>
<span data-ttu-id="e3afd-106">È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="e3afd-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="e3afd-107">I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e3afd-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="e3afd-108">La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e3afd-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="e3afd-109">Prima di poter iniziare a utilizzare i flussi di lavoro, è necessario impostare gli utenti del flusso di lavoro, creare i flussi di lavoro, potenzialmente preceduti dalla personalizzazione del codice, e specificare la modalità di ricezione delle notifiche da parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e3afd-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="e3afd-110">Per ulteriori informazioni, vedere [Impostazione dei workflow](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="e3afd-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e3afd-111">I passaggi di un flusso di lavoro tipici riguardano gli utenti che richiedono l'approvazione di attività e i responsabili dell'approvazione che accettano o rifiutano le richieste.</span><span class="sxs-lookup"><span data-stu-id="e3afd-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="e3afd-112">Di conseguenza, molti argomenti che trattano l'utilizzo dei workflow fanno riferimento alle approvazioni.</span><span class="sxs-lookup"><span data-stu-id="e3afd-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="e3afd-113">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="e3afd-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="e3afd-114">**Task**</span><span class="sxs-lookup"><span data-stu-id="e3afd-114">**To**</span></span>|<span data-ttu-id="e3afd-115">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="e3afd-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e3afd-116">Impostare un flusso di lavoro per iniziare quando si verifica la prima spedizione Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e3afd-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="e3afd-117">Procedura: Abilitare i workflow</span><span class="sxs-lookup"><span data-stu-id="e3afd-117">How to: Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="e3afd-118">Richiedere l'approvazione di un task, come responsabile approvazione, accettare, declinare o delegare le approvazioni e inviare o visualizzare le notifiche di approvazione.</span><span class="sxs-lookup"><span data-stu-id="e3afd-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="e3afd-119">Procedura: Utilizzare i workflow di approvazione</span><span class="sxs-lookup"><span data-stu-id="e3afd-119">How to: Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="e3afd-120">Creare le fasi del flusso di lavoro che limitano l'utilizzo di un certo tipo di record prima del verificarsi di un determinato evento, ad esempio l'approvazione del record.</span><span class="sxs-lookup"><span data-stu-id="e3afd-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="e3afd-121">Procedura: Limitare e consentire l'utilizzo di un record</span><span class="sxs-lookup"><span data-stu-id="e3afd-121">How to: Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="e3afd-122">Visualizzare istanze dei passaggi del flusso di lavoro con lo stato Completato.</span><span class="sxs-lookup"><span data-stu-id="e3afd-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="e3afd-123">Procedura: Visualizzare le istanze di fasi workflow archiviate</span><span class="sxs-lookup"><span data-stu-id="e3afd-123">How to: View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="e3afd-124">Eliminare un flusso di lavoro che sicuramente non verrà più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e3afd-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="e3afd-125">Procedura: Eliminare i workflow</span><span class="sxs-lookup"><span data-stu-id="e3afd-125">How to: Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="e3afd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3afd-126">See Also</span></span>  
<span data-ttu-id="e3afd-127">[Impostazione dei workflow](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e3afd-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="e3afd-128">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="e3afd-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="e3afd-129">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e3afd-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

