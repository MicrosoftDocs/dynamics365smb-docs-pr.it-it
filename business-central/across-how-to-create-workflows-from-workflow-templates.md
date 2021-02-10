---
title: Come creare workflow da modelli di workflow | Microsoft Docs
description: Per risparmiare tempo durante la creazione di nuovi workflow, è possibile creare i workflow da modelli di workflow.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 407bf7cd60416a178e9ec8a5d0b154a7583e87e1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754844"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="11b39-103">Creare workflow da modelli di workflow</span><span class="sxs-lookup"><span data-stu-id="11b39-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="11b39-104">Per risparmiare tempo durante la creazione di nuovi workflow, è possibile creare i workflow da modelli di workflow.</span><span class="sxs-lookup"><span data-stu-id="11b39-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="11b39-105">I modelli di workflow sono flussi di lavoro non modificabili presenti nella versione generica di [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="11b39-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="11b39-106">Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-".</span><span class="sxs-lookup"><span data-stu-id="11b39-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="11b39-107">Un altro modo per creare rapidamente un workflow consiste nell'importare un workflow esistente disponibile in un file all'esterno di [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="11b39-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="11b39-108">Per ulteriori informazioni, vedere [Esportare e importare workflow](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="11b39-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="11b39-109">Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe.</span><span class="sxs-lookup"><span data-stu-id="11b39-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="11b39-110">Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta.</span><span class="sxs-lookup"><span data-stu-id="11b39-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="11b39-111">È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="11b39-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="11b39-112">Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="11b39-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="11b39-113">Per creare un flusso di lavoro da un modello di flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="11b39-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="11b39-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="11b39-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="11b39-115">Scegliere l'azione **Crea flusso di lavoro da modello**.</span><span class="sxs-lookup"><span data-stu-id="11b39-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="11b39-116">Verrà aperta la pagina **Modelli del workflow**.</span><span class="sxs-lookup"><span data-stu-id="11b39-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="11b39-117">Selezionare un modello di flusso di lavoro e scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="11b39-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="11b39-118">Verrà visualizzata la pagina **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato.</span><span class="sxs-lookup"><span data-stu-id="11b39-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="11b39-119">Il valore nel campo **Codice** ad esempio con "-01" per indicare che questo è il primo workflow che viene creato dal modello di workflow.</span><span class="sxs-lookup"><span data-stu-id="11b39-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="11b39-120">Continuare la creazione del flusso di lavoro modificando i passaggi del flusso di lavoro o aggiungendone di nuovi.</span><span class="sxs-lookup"><span data-stu-id="11b39-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="11b39-121">Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="11b39-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="11b39-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11b39-122">See Also</span></span>  
 <span data-ttu-id="11b39-123">[Creare i workflow](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="11b39-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="11b39-124">[Importare ed esportare workflow](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="11b39-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="11b39-125">[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="11b39-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="11b39-126">[Eliminare i workflow](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="11b39-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="11b39-127">[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="11b39-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="11b39-128">[Impostazione dei workflow](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="11b39-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="11b39-129">[Utilizzo dei workflow](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="11b39-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="11b39-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="11b39-130">Workflow</span></span>](across-workflow.md)   
