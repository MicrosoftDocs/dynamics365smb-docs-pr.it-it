---
title: Come limitare e consentire l'utilizzo di un record | Documenti Microsoft
description: "Se si desidera limitare l'utilizzo di un record in determinate attività, ad esempio, fino all'approvazione del record, è possibile includere due risposte in un flusso di lavoro che controlla l'utilizzo del record."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="3f077-103">Limitare e consentire l'utilizzo di un record</span><span class="sxs-lookup"><span data-stu-id="3f077-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="3f077-104">Se si desidera limitare l'utilizzo di un record in determinate attività, ad esempio, fino all'approvazione del record, è possibile includere due risposte in un flusso di lavoro che controlla l'utilizzo del record.</span><span class="sxs-lookup"><span data-stu-id="3f077-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="3f077-105">Una risposta del flusso di lavoro limiterà l'utilizzo del record come definito dall'evento e dalle condizioni del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3f077-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="3f077-106">Un'altra risposta del flusso di lavoro consentirà l'utilizzo del record come definito dall'evento e dalle condizioni del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3f077-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="3f077-107">A tale scopo esistono due risposte nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Limitare l'utilizzo di un record.**</span><span class="sxs-lookup"><span data-stu-id="3f077-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="3f077-108">e **Consentire l'utilizzo di un record.**.</span><span class="sxs-lookup"><span data-stu-id="3f077-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="3f077-109">La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] offre il supporto per limitare la registrazione di un record, l'esportazione come pagamento e la stampa come controllo.</span><span class="sxs-lookup"><span data-stu-id="3f077-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="3f077-110">Per supportare altre restrizioni, è necessario che un partner Microsoft personalizzi il codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f077-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3f077-111">La funzionalità del flusso di lavoro per limitare e consentire l'utilizzo dei record non è correlata alla funzionalità per bloccare la registrazione di record relativi a fornitori, clienti e articoli.</span><span class="sxs-lookup"><span data-stu-id="3f077-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="3f077-112">Nella procedura riportata di seguito viene descritto come limitare la registrazione degli ordini di acquisto fino all'approvazione.</span><span class="sxs-lookup"><span data-stu-id="3f077-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="3f077-113">Il nuovo flusso di lavoro si baserà sul modello esistente del flusso di lavoro di approvazione della fattura di acquisto.</span><span class="sxs-lookup"><span data-stu-id="3f077-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="3f077-114">Per creare una fase del flusso di lavoro che limiti la registrazione degli ordini di acquisto non approvati</span><span class="sxs-lookup"><span data-stu-id="3f077-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="3f077-115">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Workflow** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="3f077-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3f077-116">Nella finestra **Workflow** creare un nuovo workflow denominato Workflow di approvazione ordine acquisto.</span><span class="sxs-lookup"><span data-stu-id="3f077-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="3f077-117">Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="3f077-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="3f077-118">Scegliere l'azione **Copia flusso di lavoro da modello**.</span><span class="sxs-lookup"><span data-stu-id="3f077-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="3f077-119">Scegliere il campo **Codice flusso di lavoro di origine** e nella finestra **Modelli del workflow** scegliere il modello Workflow di approvazione fattura acquisto.</span><span class="sxs-lookup"><span data-stu-id="3f077-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="3f077-120">Si noti che le prime due fasi del flusso di lavoro sono relative alla limitazione e all'autorizzazione dell'utilizzo delle fatture di acquisto.</span><span class="sxs-lookup"><span data-stu-id="3f077-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="3f077-121">Continuare a modificare la condizione di evento nella prima fase del nuovo flusso di lavoro per specificare che si applica agli ordini di acquisto.</span><span class="sxs-lookup"><span data-stu-id="3f077-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="3f077-122">Nella Scheda dettaglio **Fasi workflow** scegliere il campo **Condizioni evento** e per il filtro **Tipo di documento** scegliere **Ordine**.</span><span class="sxs-lookup"><span data-stu-id="3f077-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="3f077-123">Continuare per modificare, eliminare o aggiungere altre fasi del flusso di lavoro per creare un processo aziendale che inizia limitando la registrazione degli ordini di acquisto non approvati.</span><span class="sxs-lookup"><span data-stu-id="3f077-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3f077-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f077-124">See Also</span></span>  
<span data-ttu-id="3f077-125">[Creare i workflow](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="3f077-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="3f077-126">Workflow</span><span class="sxs-lookup"><span data-stu-id="3f077-126">Workflow</span></span>](across-workflow.md)   

