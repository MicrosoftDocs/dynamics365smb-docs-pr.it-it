---
title: Come eliminare workflow | Microsoft Docs
description: È possibile eliminare un flusso di lavoro che non si desidera utilizzare più. Lo stato di tutte le istanze dei passaggi del flusso di lavoro che sono definite nel flusso di lavoro deve essere impostato su **Completato**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 46b976894854781ee2d8198deed316f94189c007
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188326"
---
# <a name="delete-workflows"></a><span data-ttu-id="c3768-104">Eliminare i workflow</span><span class="sxs-lookup"><span data-stu-id="c3768-104">Delete Workflows</span></span>
<span data-ttu-id="c3768-105">È possibile eliminare un workflow che non si desidera utilizzare più.</span><span class="sxs-lookup"><span data-stu-id="c3768-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="c3768-106">Lo stato di tutte le istanze dei passaggi del flusso di lavoro che sono definite nel flusso di lavoro deve essere impostato su **Completato**.</span><span class="sxs-lookup"><span data-stu-id="c3768-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="c3768-107">Quando si elimina un flusso di lavoro, tutte le informazioni in esso contenute vengono perse.</span><span class="sxs-lookup"><span data-stu-id="c3768-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="c3768-108">Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe.</span><span class="sxs-lookup"><span data-stu-id="c3768-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="c3768-109">Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta.</span><span class="sxs-lookup"><span data-stu-id="c3768-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="c3768-110">È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3768-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="c3768-111">Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c3768-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="c3768-112">Per eliminare un flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="c3768-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="c3768-113">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c3768-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c3768-114">Selezionare il flusso di lavoro che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="c3768-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="c3768-115">Scegliere l'azione **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="c3768-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="c3768-116">In alternativa, aprire il flusso di lavoro che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="c3768-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="c3768-117">Nella pagina **Workflow** scegliere l'azione **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="c3768-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3768-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3768-118">See Also</span></span>  
 <span data-ttu-id="c3768-119">[Creare i workflow](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3768-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="c3768-120">[Abilitare i workflow](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3768-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="c3768-121">[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="c3768-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="c3768-122">[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="c3768-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="c3768-123">[Impostazione dei workflow](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3768-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="c3768-124">[Utilizzo dei workflow](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3768-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="c3768-125">Workflow</span><span class="sxs-lookup"><span data-stu-id="c3768-125">Workflow</span></span>](across-workflow.md)   
