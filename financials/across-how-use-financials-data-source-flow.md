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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="98f95-103">Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un workflow automatizzato</span><span class="sxs-lookup"><span data-stu-id="98f95-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="98f95-104">È possibile utilizzare i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come parte di un flusso di lavoro in Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="98f95-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="98f95-105">È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Flow.</span><span class="sxs-lookup"><span data-stu-id="98f95-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="98f95-106">Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in Flow</span><span class="sxs-lookup"><span data-stu-id="98f95-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="98f95-107">Nel browser passare a [flow.microsoft.com](https://flow.microsoft.com/en-us/), quindi accedere.</span><span class="sxs-lookup"><span data-stu-id="98f95-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="98f95-108">Scegliere **I miei flussi** dalla barra nella parte superiore della pagina.</span><span class="sxs-lookup"><span data-stu-id="98f95-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="98f95-109">Nella finestra **I miei flussi** selezionare **Creare da Vuoto**.</span><span class="sxs-lookup"><span data-stu-id="98f95-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="98f95-110">Selezionare uno dei trigger [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibili dall'elenco dei trigger:</span><span class="sxs-lookup"><span data-stu-id="98f95-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="98f95-111">*Creazione di un record*,</span><span class="sxs-lookup"><span data-stu-id="98f95-111">*When a record is created*,</span></span>  
    <span data-ttu-id="98f95-112">*Eliminazione di un record*,</span><span class="sxs-lookup"><span data-stu-id="98f95-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="98f95-113">*Modifica di un record*,</span><span class="sxs-lookup"><span data-stu-id="98f95-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="98f95-114">*Approvazione di un cliente necessaria*,</span><span class="sxs-lookup"><span data-stu-id="98f95-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="98f95-115">*Approvazione batch registrazioni COGE necessaria*,</span><span class="sxs-lookup"><span data-stu-id="98f95-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="98f95-116">*Approvazione riga registrazioni COGE necessaria*,</span><span class="sxs-lookup"><span data-stu-id="98f95-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="98f95-117">*Approvazione articolo necessaria*,</span><span class="sxs-lookup"><span data-stu-id="98f95-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="98f95-118">*Approvazione di un documento di acquisto necessaria*,</span><span class="sxs-lookup"><span data-stu-id="98f95-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="98f95-119">*Approvazione di un documento di vendita necessaria*, o</span><span class="sxs-lookup"><span data-stu-id="98f95-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="98f95-120">*Approvazione di un fornitore necessaria*.</span><span class="sxs-lookup"><span data-stu-id="98f95-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="98f95-121">In Flow verrà visualizzata la richiesta per le informazioni necessarie per accedere ai dati di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="98f95-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="98f95-122">Se è stato selezionato uno dei seguenti trigger: *Creazione di un record*, *Modifica di un record* e *Eliminazione di un record* è necessario selezionare un nome di società e un nome di tabella.</span><span class="sxs-lookup"><span data-stu-id="98f95-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="98f95-123">Con qualsiasi altro trigger, è richiesto soltanto il nome della società per connettersi.</span><span class="sxs-lookup"><span data-stu-id="98f95-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="98f95-124">In Flow verrà visualizzata una lista delle società e delle tabelle disponibili tramite [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="98f95-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="98f95-125">Le tabelle, o punti finali, indicano tutti i servizi Web pubblicati tramite [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="98f95-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="98f95-126">In alternativa, creare un nuovo URL del servizio Web di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzano l'azione **Crea set di dati** nella pagina **Servizi Web** tramite la Guida di setup assistito o **Imposta dati reporting** oppure l'azione **Modifica in Excel** in qualsiasi elenco.</span><span class="sxs-lookup"><span data-stu-id="98f95-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="98f95-127">A questo punto, è stata stabilita correttamente la connessione ai dati di Finance and Operations, Business edition e si è pronti per iniziare a creare un flusso.</span><span class="sxs-lookup"><span data-stu-id="98f95-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="98f95-128">Per ulteriori informazioni, vedere la [Documentazione di Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="98f95-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="98f95-129">Per la risoluzione dei problemi di Microsoft Flow, vedere [Risoluzione dei problemi di integrazione con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="98f95-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="98f95-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98f95-130">See Also</span></span>
<span data-ttu-id="98f95-131">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="98f95-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="98f95-132">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="98f95-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="98f95-133">[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="98f95-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="98f95-134">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="98f95-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="98f95-135">Finanze</span><span class="sxs-lookup"><span data-stu-id="98f95-135">Finance</span></span>](finance.md)  

