---
title: Connettere i dati a Flow| Documenti Microsoft
description: "È possibile rendere disponibili i dati di Financials come origine dati e specificare un URL OData dei service Web per creare un workflow automatizzato."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="7a109-103">Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato</span><span class="sxs-lookup"><span data-stu-id="7a109-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="7a109-104">È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="7a109-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="7a109-105">È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.</span><span class="sxs-lookup"><span data-stu-id="7a109-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="7a109-106">Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Flow</span><span class="sxs-lookup"><span data-stu-id="7a109-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="7a109-107">Nel browser passare a [flow.microsoft.com](https://flow.microsoft.com/en-us/), quindi accedere.</span><span class="sxs-lookup"><span data-stu-id="7a109-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="7a109-108">Scegliere **I miei flussi** dalla barra nella parte superiore della pagina.</span><span class="sxs-lookup"><span data-stu-id="7a109-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="7a109-109">Nella finestra **I miei flussi** selezionare **Creare da Vuoto**.</span><span class="sxs-lookup"><span data-stu-id="7a109-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="7a109-110">Selezionare uno dei trigger [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibili dall'elenco dei trigger:</span><span class="sxs-lookup"><span data-stu-id="7a109-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="7a109-111">*Approvazione di un cliente necessaria*,</span><span class="sxs-lookup"><span data-stu-id="7a109-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="7a109-112">*Approvazione batch registrazioni COGE necessaria*,</span><span class="sxs-lookup"><span data-stu-id="7a109-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="7a109-113">*Approvazione riga registrazioni COGE necessaria*,</span><span class="sxs-lookup"><span data-stu-id="7a109-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="7a109-114">*Approvazione articolo necessaria*,</span><span class="sxs-lookup"><span data-stu-id="7a109-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="7a109-115">*Approvazione di un documento di acquisto necessaria*,</span><span class="sxs-lookup"><span data-stu-id="7a109-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="7a109-116">*Approvazione di un documento di vendita necessaria*, o</span><span class="sxs-lookup"><span data-stu-id="7a109-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="7a109-117">*Approvazione di un fornitore necessaria*.</span><span class="sxs-lookup"><span data-stu-id="7a109-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="7a109-118">Flow richiederà la selezione di una società presso il tenant [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a109-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="7a109-119">Poiché ogni fase del flusso è indipendente dalla successiva, è possibile che sia necessario definire la società più volte quando si utilizza un modello [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a109-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="7a109-120">A questo punto, è stata stabilita correttamente la connessione ai dati di Finance and Operations, Business edition e si è pronti per iniziare a creare un flusso.</span><span class="sxs-lookup"><span data-stu-id="7a109-120">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="7a109-121">Per ulteriori informazioni, vedere la [Documentazione di Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="7a109-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="7a109-122">Per la risoluzione dei problemi di Microsoft Flow, vedere [Risoluzione dei problemi di integrazione con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="7a109-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7a109-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a109-123">See Also</span></span>
<span data-ttu-id="7a109-124">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="7a109-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="7a109-125">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="7a109-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="7a109-126">[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="7a109-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="7a109-127">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="7a109-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="7a109-128">Finanze</span><span class="sxs-lookup"><span data-stu-id="7a109-128">Finance</span></span>](finance.md)  

