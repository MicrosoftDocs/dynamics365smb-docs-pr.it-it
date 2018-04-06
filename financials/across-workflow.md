---
title: Workflow | Microsoft Docs
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
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: 861ff6ac3c2789f83379e4c01c0e1b8f5847d2d6
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="workflow"></a><span data-ttu-id="953f5-105">Workflow</span><span class="sxs-lookup"><span data-stu-id="953f5-105">Workflow</span></span>
<span data-ttu-id="953f5-106">È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="953f5-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="953f5-107">I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti.</span><span class="sxs-lookup"><span data-stu-id="953f5-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="953f5-108">La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow.</span><span class="sxs-lookup"><span data-stu-id="953f5-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="953f5-109">Nella finestra **Workflow** creare un workflow elencando le fasi interessate nelle righe.</span><span class="sxs-lookup"><span data-stu-id="953f5-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="953f5-110">Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta.</span><span class="sxs-lookup"><span data-stu-id="953f5-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="953f5-111">È possibile definire le fasi del flusso di lavoro compilando i campi delle righe del flusso di lavoro in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="953f5-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="953f5-112">La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] include una serie di workflow preconfigurati, rappresentati da modelli di workflow che si possono copiare per creare workflow.</span><span class="sxs-lookup"><span data-stu-id="953f5-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="953f5-113">Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-".</span><span class="sxs-lookup"><span data-stu-id="953f5-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="953f5-114">Per ulteriori informazioni, vedere l'elenco dei modelli di workflow nella finestra Modelli del workflow.</span><span class="sxs-lookup"><span data-stu-id="953f5-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="953f5-115">Se uno scenario aziendale richiede un evento o una risposta del flusso di lavoro non supportati, il partner Microsoft deve implementarli tramite la personalizzazione del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="953f5-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="953f5-116">Per ulteriori informazioni, vedere [Procedura dettagliata: Implementazione di nuovi eventi e risposte workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) nella Guida per sviluppatori e professionisti IT.</span><span class="sxs-lookup"><span data-stu-id="953f5-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>  

 <span data-ttu-id="953f5-117">Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.</span><span class="sxs-lookup"><span data-stu-id="953f5-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="953f5-118">**Task**</span><span class="sxs-lookup"><span data-stu-id="953f5-118">**To**</span></span>|<span data-ttu-id="953f5-119">**Vedere**</span><span class="sxs-lookup"><span data-stu-id="953f5-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="953f5-120">Impostare gli utenti del flusso di lavoro, specificare la modalità di notifica per gli utenti e creare nuovi flussi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="953f5-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="953f5-121">Per i nuovi flussi di lavoro per gli scenari non sostenuti, implementare gli elementi necessari del flusso di lavoro personalizzando il codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="953f5-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="953f5-122">Impostazione dei workflow</span><span class="sxs-lookup"><span data-stu-id="953f5-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="953f5-123">Abilitare i flussi di lavoro, intervenire sulle relative notifiche, incluse le approvazioni di richieste, e approvare le richieste per eseguire un passaggio del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="953f5-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="953f5-124">Archiviare ed eliminare i flussi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="953f5-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="953f5-125">Utilizzo dei workflow</span><span class="sxs-lookup"><span data-stu-id="953f5-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="953f5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="953f5-126">See Also</span></span>  
[<span data-ttu-id="953f5-127">Vendite</span><span class="sxs-lookup"><span data-stu-id="953f5-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="953f5-128">Acquisti</span><span class="sxs-lookup"><span data-stu-id="953f5-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="953f5-129">Gestione di progetti</span><span class="sxs-lookup"><span data-stu-id="953f5-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="953f5-130">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="953f5-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

