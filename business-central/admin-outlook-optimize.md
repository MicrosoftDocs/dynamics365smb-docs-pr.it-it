---
title: Ottimizzazione di Outlook per la Posta in arrivo aziendale
description: Informazioni su come migliorare l'esperienza con la Posta in arrivo aziendale in Business Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064858"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="7f7d3-103">Ottimizzazione di Outlook per la Posta in arrivo aziendale</span><span class="sxs-lookup"><span data-stu-id="7f7d3-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="7f7d3-104">Questo articolo discute le operazioni necessarie per ottenere la migliore esperienza possibile con Posta in arrivo aziendale in Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="7f7d3-105">Aggiorna Outlook</span><span class="sxs-lookup"><span data-stu-id="7f7d3-105">Update Outlook</span></span>

<span data-ttu-id="7f7d3-106">Esegui aggiornamento alla versione di Outlook 2012 o successiva.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="7f7d3-107">Se non riesci ad aggiornare Outlook alla versione 2012 o successiva, assicurati di eseguire almeno l'aggiornamento alla versione 1905.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="7f7d3-108">Ciò impedisce l'esecuzione del componente aggiuntivo di Outlook utilizzando componenti Internet Explorer legacy</span><span class="sxs-lookup"><span data-stu-id="7f7d3-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="7f7d3-109">Come controllare la tua versione di Outlook</span><span class="sxs-lookup"><span data-stu-id="7f7d3-109">How to check your version of Outlook</span></span>

<span data-ttu-id="7f7d3-110">Se si utilizza Office 2019 o Microsoft 365, seguire questa guida del supporto Microsoft per verificare la versione di Outlook installata:</span><span class="sxs-lookup"><span data-stu-id="7f7d3-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="7f7d3-111">Informazioni su Office: quale versione di Office sto utilizzando?</span><span class="sxs-lookup"><span data-stu-id="7f7d3-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="7f7d3-112">Istruzioni per aggiornare Outlook</span><span class="sxs-lookup"><span data-stu-id="7f7d3-112">How to update Outlook</span></span>

<span data-ttu-id="7f7d3-113">Per aggiornare Outlook alla versione più recente, seguire questa guida del supporto Microsoft o contattare l'amministratore:</span><span class="sxs-lookup"><span data-stu-id="7f7d3-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="7f7d3-114">Installare gli aggiornamenti di Office</span><span class="sxs-lookup"><span data-stu-id="7f7d3-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="7f7d3-115">Installare Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="7f7d3-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="7f7d3-116">Assicurarsi che Microsoft Edge WebView2 sia installato sul tuo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="7f7d3-117">Come verificare se Microsoft Edge WebView2 è installato</span><span class="sxs-lookup"><span data-stu-id="7f7d3-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="7f7d3-118">Per verificare se Microsoft Edge WebView2 è installato su un computer, effettuare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="7f7d3-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="7f7d3-119">Dal menu Start:</span><span class="sxs-lookup"><span data-stu-id="7f7d3-119">From Start menu:</span></span>

1. <span data-ttu-id="7f7d3-120">Selezionare **Start** ![Start di Windows](media/windows-start-icon.png "Icona Start di Windows") > **Impostazioni** ![Impostazioni di Windows](media/windows-settings-icon.png "Icona Impostazioni di Windows") > **App e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="7f7d3-121">Nella casella di ricerca, digitare **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="7f7d3-122">Se Microsoft Edge WebView2 è installato, vedrai una voce chiamata **Microsoft Edge Runtime WebView2**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="7f7d3-123">Dal pannello di controllo:</span><span class="sxs-lookup"><span data-stu-id="7f7d3-123">From Control Panel:</span></span>

1. <span data-ttu-id="7f7d3-124">Nella casella di ricerca accanto a **Start** ![Start di Windows](media/windows-start-icon.png "Icona Start di Windows"), digitare **Pannello di controllo**, quindi selezionare il risultato.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="7f7d3-125">Scegliere **Programmi** > **Programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="7f7d3-126">Nella casella di ricerca, digitare **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="7f7d3-127">Se Microsoft Edge WebView2 è installato, vedrai una voce chiamata **Microsoft Edge Runtime WebView2**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="7f7d3-128">Come installare Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="7f7d3-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="7f7d3-129">Con il tuo browser, vai a [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="7f7d3-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="7f7d3-130">Scegliere **Scarica**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-130">Choose **Download**.</span></span>
3. <span data-ttu-id="7f7d3-131">Impostare **Seleziona architettura** in base al proprio sistema.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="7f7d3-132">Scegliere **Scarica**.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="7f7d3-133">La tua organizzazione potrebbe avere restrizioni sui componenti che possono essere installati sul tuo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="7f7d3-134">Contattare l'amministratore per l'assistenza.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="7f7d3-135">Utilizzare un browser supportato</span><span class="sxs-lookup"><span data-stu-id="7f7d3-135">Use a supported browser</span></span>

<span data-ttu-id="7f7d3-136">Prendere in considerazione la possibilità di utilizzare Outlook per il Web in uno dei browser supportati da Business Central.</span><span class="sxs-lookup"><span data-stu-id="7f7d3-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="7f7d3-137">Per un elenco di browser supportati, vedere [Requisiti minimi per l'utilizzo di Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="7f7d3-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="7f7d3-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7f7d3-138">See Also</span></span>

[<span data-ttu-id="7f7d3-139">Preparazione al business</span><span class="sxs-lookup"><span data-stu-id="7f7d3-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="7f7d3-140">Scaricare Business Central sul dispositivo mobile</span><span class="sxs-lookup"><span data-stu-id="7f7d3-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="7f7d3-141">Inviare documenti via e-mail</span><span class="sxs-lookup"><span data-stu-id="7f7d3-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="7f7d3-142">Finanze</span><span class="sxs-lookup"><span data-stu-id="7f7d3-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="7f7d3-143">Vendite</span><span class="sxs-lookup"><span data-stu-id="7f7d3-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="7f7d3-144">Acquisti</span><span class="sxs-lookup"><span data-stu-id="7f7d3-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7f7d3-145">Requisiti minimi per Outlook</span><span class="sxs-lookup"><span data-stu-id="7f7d3-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="7f7d3-146">Utilizzo di componenti aggiuntivi in Outlook sul Web</span><span class="sxs-lookup"><span data-stu-id="7f7d3-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]