---
title: Come esportare e importare workflow | Microsoft Docs
description: Per trasferire i workflow ad altri database di Business Central, ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e4fda3ed6e3a29eb035b4e8509a0e9ea89b21a3c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305382"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="c3928-103">Importa ed esporta workflow</span><span class="sxs-lookup"><span data-stu-id="c3928-103">Export and Import Workflows</span></span>
<span data-ttu-id="c3928-104">Per trasferire i workflow ad altri database di [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio per risparmiare tempo durante la creazione di nuovi workflow, è possibile esportare e importare i workflow.</span><span class="sxs-lookup"><span data-stu-id="c3928-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="c3928-105">Un altro modo per creare rapidamente i flussi di lavoro prevede la creazione dei flussi di lavoro dai modelli di flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c3928-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="c3928-106">Per ulteriori informazioni, vedere [Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c3928-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="c3928-107">Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe.</span><span class="sxs-lookup"><span data-stu-id="c3928-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="c3928-108">Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta.</span><span class="sxs-lookup"><span data-stu-id="c3928-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="c3928-109">È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="c3928-110">Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c3928-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="c3928-111">Per esportare un flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="c3928-111">To export a workflow</span></span>  
1.  <span data-ttu-id="c3928-112">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c3928-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c3928-113">Selezionare un workflow e scegliere l'azione **Esporta in file**.</span><span class="sxs-lookup"><span data-stu-id="c3928-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="c3928-114">Nella pagina **Esporta file** fare clic sul pulsante **Salva**.</span><span class="sxs-lookup"><span data-stu-id="c3928-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="c3928-115">Nella pagina **Esporta** selezionare un percorso per il file e scegliere il pulsante **Salva**.</span><span class="sxs-lookup"><span data-stu-id="c3928-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="c3928-116">Per importare un flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="c3928-116">To import a workflow</span></span>  
1.  <span data-ttu-id="c3928-117">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="c3928-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c3928-118">Selezionare l'azione **Importa da file**.</span><span class="sxs-lookup"><span data-stu-id="c3928-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="c3928-119">Nella pagina **Importa** selezionare il file XML contenente il flusso di lavoro e quindi scegliere il pulsante **Apri**.</span><span class="sxs-lookup"><span data-stu-id="c3928-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="c3928-120">Se il codice del flusso di lavoro è già esistente nel database, i passaggi del flusso di lavoro verranno sovrascritti dai passaggi il flusso di lavoro importato.</span><span class="sxs-lookup"><span data-stu-id="c3928-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3928-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3928-121">See Also</span></span>  
 <span data-ttu-id="c3928-122">[Creare i workflow](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3928-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="c3928-123">[Creare flussi di lavoro da modelli di flusso di lavoro](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="c3928-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="c3928-124">[Visualizzare le istanze di fase workflow archiviate](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="c3928-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="c3928-125">[Eliminare i workflow](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3928-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="c3928-126">[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="c3928-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="c3928-127">[Impostazione dei workflow](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3928-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="c3928-128">[Utilizzo dei workflow](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c3928-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="c3928-129">Workflow</span><span class="sxs-lookup"><span data-stu-id="c3928-129">Workflow</span></span>](across-workflow.md)   
