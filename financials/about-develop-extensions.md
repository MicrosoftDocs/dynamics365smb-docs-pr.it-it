---
title: Personalizzare Dynamics 365 for Financials| Documenti Microsoft
description: Sviluppare, mostrare e promuovere le proprie app ed estensioni per Dynamics 365 for Financials.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc355c7b4cd51412ec0b5c95398c2d7b50a13f94
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="2c3ff-103">Estensione di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c3ff-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="2c3ff-104">L'utilizzo di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] come piattaforma per sviluppatori di app offre numerosi vantaggi:</span><span class="sxs-lookup"><span data-stu-id="2c3ff-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="2c3ff-105">Possibilità di migliorare [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], una comprovata soluzione online di Microsoft, sfruttando le proprie competenze</span><span class="sxs-lookup"><span data-stu-id="2c3ff-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="2c3ff-106">Trarre vantaggio dal marchio Dynamics 365, che milioni di utenti conoscono e di cui si fidano</span><span class="sxs-lookup"><span data-stu-id="2c3ff-106">Leverage the Dynamics 365 brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="2c3ff-107">Raggiungere più clienti per le app aziendali grazie a [Microsoft AppSource](https://appsource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="2c3ff-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="2c3ff-108">Ottenere maggiori risultati con una piattaforma che una offre scalabilità ed esperienze moderne</span><span class="sxs-lookup"><span data-stu-id="2c3ff-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="2c3ff-109">Possibilità di offrire bundle con app aziendali intelligenti come PowerApps, Flow, Power BI, Cortana Intelligence e molte altre</span><span class="sxs-lookup"><span data-stu-id="2c3ff-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="2c3ff-110">Per pubblicare l'app [!INCLUDE[d365fin](includes/d365fin_md.md)] in AppSource:</span><span class="sxs-lookup"><span data-stu-id="2c3ff-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="2c3ff-111">Creare gli account necessari</span><span class="sxs-lookup"><span data-stu-id="2c3ff-111">Create your accounts</span></span>  
<span data-ttu-id="2c3ff-112">Microsoft desidera che i partner possano accedere a tutti gli strumenti necessari.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="2c3ff-113">A tal fine, è necessario un ID Microsoft Partner Network, un account come sviluppatore e un account Partner Source Business Center (PSBC).</span><span class="sxs-lookup"><span data-stu-id="2c3ff-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="2c3ff-114">Per ulteriori informazioni su come ottenere questi account, scaricare il documento [Creare gli account.pdf](https://go.microsoft.com/fwlink/?linkid=841514) dal Download Center.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="2c3ff-115">Comunicare la propria idea sull'app</span><span class="sxs-lookup"><span data-stu-id="2c3ff-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="2c3ff-116">Condividere l'idea dell'app [!INCLUDE[d365fin](includes/d365fin_md.md)] con Microsoft AppSource.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="2c3ff-117">Dopo la presentazione dell'idea, verrà fornito tutto il necessario per iniziare a lavorare sull'app.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="2c3ff-118">Per ulteriori informazioni su tutti i passaggi, scaricare il documento [Comunicare l'idea dell'app.pdf](https://go.microsoft.com/fwlink/?linkid=841515) dal Download Center.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="2c3ff-119">Sviluppare gli aspetti tecnici dell'app</span><span class="sxs-lookup"><span data-stu-id="2c3ff-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="2c3ff-120">Dopo aver impostato il proprio ambiente di sviluppo per l'app, è possibile realizzare l'app.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="2c3ff-121">Per ulteriori informazioni su quanto necessario conoscere sugli aspetti tecnici dell'app [!INCLUDE[d365fin](includes/d365fin_md.md)], scaricare il documento [Sviluppare gli aspetti tecnici dell'app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) dal Download Center.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="2c3ff-122">Sviluppare gli aspetti di marketing dell'app</span><span class="sxs-lookup"><span data-stu-id="2c3ff-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="2c3ff-123">Elencare le caratteristiche e la funzionalità dell'app non sarà necessario per convertire i potenziali clienti in acquirenti.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="2c3ff-124">Per ulteriori informazioni su come migliorare la proposta di mercato per l'app in AppSource, scaricare il documento [Sviluppare gli aspetti di marketing dell'app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) dal Download Center.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="2c3ff-125">Pubblicare l'app</span><span class="sxs-lookup"><span data-stu-id="2c3ff-125">Publish your app</span></span>  
<span data-ttu-id="2c3ff-126">Prima della pubblicazione, Microsoft collaborerà con il partner per assicurarsi che l'app risulti in evidenza in Microsoft AppSource e nella pagina di destinazione del partner.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="2c3ff-127">È necessario convalidare l'app per assicurarsi dell'efficacia del marketing, dell'affidabilità e dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="2c3ff-128">Per ulteriori informazioni sul processo di convalida e sulle modalità di pubblicazione dell'app, scaricare il documento [Pubblicare l'app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) dal Download Center.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="need-help"></a><span data-ttu-id="2c3ff-129">Ulteriore assistenza</span><span class="sxs-lookup"><span data-stu-id="2c3ff-129">Need help?</span></span>
<span data-ttu-id="2c3ff-130">Per ulteriore supporto o consulenza, è possibile contattare gli esperti di sviluppo app come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2c3ff-130">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="2c3ff-131">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="2c3ff-131">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="2c3ff-132">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="2c3ff-132">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="2c3ff-133">I partner in elenco:</span><span class="sxs-lookup"><span data-stu-id="2c3ff-133">Partners in this list:</span></span>

* <span data-ttu-id="2c3ff-134">Sono elencati in ordine alfabetico</span><span class="sxs-lookup"><span data-stu-id="2c3ff-134">Are listed alphabetically</span></span>  
* <span data-ttu-id="2c3ff-135">Hanno fornito o stanno fornendo assistenza a un minimo di tre partner per la pubblicazione di app in Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="2c3ff-135">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="2c3ff-136">Offrono un pacchetto di servizio di assistenza (riportato nel rispettivo sito Web) correlato al servizio di supporto app che offrono</span><span class="sxs-lookup"><span data-stu-id="2c3ff-136">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="2c3ff-137">Se si ritiene di dover essere elencati come partner di supporto per le app, non esitare a contattare [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2c3ff-137">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="2c3ff-138">Domande?</span><span class="sxs-lookup"><span data-stu-id="2c3ff-138">Questions?</span></span>
<span data-ttu-id="2c3ff-139">Le [domande frequenti](https://go.microsoft.com/fwlink/?linkid=841520) offrono risposta alle domande più comuni sulle app per [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2c3ff-139">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="2c3ff-140">In caso di ulteriori domande, non esitare a contattare il rappresentate Microsoft locale o l'indirizzo di posta elettronica [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2c3ff-140">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="2c3ff-141">Ulteriori risorse</span><span class="sxs-lookup"><span data-stu-id="2c3ff-141">Further Resources</span></span>
<span data-ttu-id="2c3ff-142">La [pagina degli argomenti DLP](https://mbspartner.microsoft.com/BFI/Topic/76) offre ulteriori risorse per lo sviluppo di app.</span><span class="sxs-lookup"><span data-stu-id="2c3ff-142">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="2c3ff-143">Alcuni argomenti selezionati sono disponibili di seguito:</span><span class="sxs-lookup"><span data-stu-id="2c3ff-143">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="2c3ff-144">Registrazione dell'utente e fatturazione successiva </span><span class="sxs-lookup"><span data-stu-id="2c3ff-144">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="2c3ff-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c3ff-145">See Also</span></span>
<span data-ttu-id="2c3ff-146">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="2c3ff-146">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="2c3ff-147">[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2c3ff-147">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="2c3ff-148">https://appsource.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="2c3ff-148">https://appsource.microsoft.com</span></span>](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
