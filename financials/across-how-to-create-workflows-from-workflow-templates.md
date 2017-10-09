---
title: Come creare workflow da modelli di workflow | Microsoft Docs
description: "Per risparmiare tempo durante la creazione di nuovi flussi di lavoro, è possibile creare i flussi di lavoro da modelli di flusso di lavoro."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: dcf6f5f5b0364ebcaefdcbc43fdbd7471cb6079e
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-workflows-from-workflow-templates"></a><span data-ttu-id="d1b59-103">Procedura: Creare flussi di lavoro da modelli di flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="d1b59-103">How to: Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="d1b59-104">Per risparmiare tempo durante la creazione di nuovi workflow, è possibile creare i workflow da modelli di workflow.</span><span class="sxs-lookup"><span data-stu-id="d1b59-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="d1b59-105">I modelli di workflow sono flussi di lavoro non modificabili presenti nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d1b59-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d1b59-106">Il codice dei modelli di flusso di lavoro che vengono aggiunti da Microsoft hanno il prefisso "MS-".</span><span class="sxs-lookup"><span data-stu-id="d1b59-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="d1b59-107">Un altro modo per creare rapidamente un workflow consiste nell'importare un workflow esistente disponibile in un file all'esterno di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d1b59-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d1b59-108">Per ulteriori informazioni, vedere [Procedura: Esportare e importare workflow](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d1b59-108">For more information, see [How to: Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="d1b59-109">Nella finestra **Workflow** creare un workflow elencando le fasi interessate nelle righe.</span><span class="sxs-lookup"><span data-stu-id="d1b59-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="d1b59-110">Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta.</span><span class="sxs-lookup"><span data-stu-id="d1b59-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="d1b59-111">È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1b59-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="d1b59-112">Per ulteriori informazioni, vedere [Procedura: Creare workflow](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d1b59-112">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="d1b59-113">Per creare un flusso di lavoro da un modello di flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="d1b59-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="d1b59-114">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Workflow** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="d1b59-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d1b59-115">Scegliere l'azione **Crea flusso di lavoro da modello**.</span><span class="sxs-lookup"><span data-stu-id="d1b59-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="d1b59-116">Verrà aperta la finestra **Modelli del workflow**.</span><span class="sxs-lookup"><span data-stu-id="d1b59-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="d1b59-117">Selezionare un modello di flusso di lavoro e scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1b59-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="d1b59-118">Verrà visualizzata la finestra **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato.</span><span class="sxs-lookup"><span data-stu-id="d1b59-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="d1b59-119">Il valore nel campo **Codice** ad esempio con "-01" per indicare che questo è il primo workflow che viene creato dal modello di workflow.</span><span class="sxs-lookup"><span data-stu-id="d1b59-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="d1b59-120">Continuare la creazione del flusso di lavoro modificando i passaggi del flusso di lavoro o aggiungendone di nuovi.</span><span class="sxs-lookup"><span data-stu-id="d1b59-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="d1b59-121">Per ulteriori informazioni, vedere [Procedura: Creare workflow](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d1b59-121">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1b59-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1b59-122">See Also</span></span>  
 <span data-ttu-id="d1b59-123">[Procedura: Creare workflow](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d1b59-123">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="d1b59-124">[Procedura: Esportare e importare workflow](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d1b59-124">[How to: Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="d1b59-125">[Procedura: Visualizzare le istanze di fasi workflow archiviate](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="d1b59-125">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="d1b59-126">[Procedura: Eliminare i workflow](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d1b59-126">[How to: Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="d1b59-127">[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="d1b59-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="d1b59-128">[Impostazione dei workflow](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d1b59-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="d1b59-129">[Utilizzo dei workflow](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d1b59-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="d1b59-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="d1b59-130">Workflow</span></span>](across-workflow.md)   

