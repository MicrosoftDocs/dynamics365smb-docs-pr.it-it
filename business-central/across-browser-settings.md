---
title: Impostazione del browser
description: Descrizione su come configurare i browser per utilizzare Business Central e i prodotti che include.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: b5083735be31b635cb3fc3ce404e7f182d04640f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384976"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="25ddf-103">Configurazione e risoluzione dei problemi del browser per utilizzare Business Central Web Client</span><span class="sxs-lookup"><span data-stu-id="25ddf-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="25ddf-104">In questo articolo viene descritto come configurare il browser di modo che [!INCLUDE[web_client](includes/web_client.md)] e tutte le relative funzionalità funzionino correttamente.</span><span class="sxs-lookup"><span data-stu-id="25ddf-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="25ddf-105">Leggi questo articolo se hai problemi ad aprire [!INCLUDE[web_client](includes/web_client.md)], poiché alcuni problemi potrebbero essere causati dalle impostazioni del browser.</span><span class="sxs-lookup"><span data-stu-id="25ddf-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="25ddf-106">L'articolo fornisce dettagli per la configurazione di Microsoft Edge, ma i requisiti per JavaScript, cookie e popup sono gli stessi per tutti i browser supportati.</span><span class="sxs-lookup"><span data-stu-id="25ddf-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="25ddf-107">Per altri browser, fai riferimento alle istruzioni fornite dal produttore.</span><span class="sxs-lookup"><span data-stu-id="25ddf-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="25ddf-108">Utilizzare un browser supportato</span><span class="sxs-lookup"><span data-stu-id="25ddf-108">Use a supported browser</span></span>

<span data-ttu-id="25ddf-109">Assicurati di utilizzare uno dei browser supportati.</span><span class="sxs-lookup"><span data-stu-id="25ddf-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="25ddf-110">Vedi [Requisiti minimi per l'utilizzo di Business Central](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="25ddf-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="25ddf-111">Consentire JavaScript in Business Central</span><span class="sxs-lookup"><span data-stu-id="25ddf-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="25ddf-112">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="25ddf-112">*Problem:*</span></span>

<span data-ttu-id="25ddf-113">Se il browser non consente JavaScript, vedrai **NotSupported/DisabledJavaScript** nella barra degli indirizzi e un messaggio **Errore HTTP 404.0 - Non trovato** quando tenti di aprire [!INCLUDE[prod_short](includes/prod_short.md)], e la</span><span class="sxs-lookup"><span data-stu-id="25ddf-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="25ddf-114">*Correzione:*</span><span class="sxs-lookup"><span data-stu-id="25ddf-114">*Fix:*</span></span>

1. <span data-ttu-id="25ddf-115">In Microsoft Edge, vai a **Impostazioni** > **Cookie e autorizzazioni sito** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="25ddf-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="25ddf-116">Effettua uno dei seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="25ddf-116">Do one of the following steps.</span></span> <span data-ttu-id="25ddf-117">Scegli il passaggio consigliato dall'organizzazione:</span><span class="sxs-lookup"><span data-stu-id="25ddf-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="25ddf-118">Sposta l'interruttore **Consentito** a sinistra (Off).</span><span class="sxs-lookup"><span data-stu-id="25ddf-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="25ddf-119">Quindi seleziona **Aggiungi** e digita l'indirizzo (URL) per [!INCLUDE[prod_short](includes/prod_short.md)] nella casella **Sito**.</span><span class="sxs-lookup"><span data-stu-id="25ddf-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="25ddf-120">Al termine, seleziona **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="25ddf-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="25ddf-121">Sposta l'interruttore **Consentito** a destra (On).</span><span class="sxs-lookup"><span data-stu-id="25ddf-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="25ddf-122">Consentire i cookie in Business Central</span><span class="sxs-lookup"><span data-stu-id="25ddf-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="25ddf-123">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="25ddf-123">*Problem:*</span></span>

<span data-ttu-id="25ddf-124">Se il browser non consente i cookie, verrà visualizzato il seguente errore:</span><span class="sxs-lookup"><span data-stu-id="25ddf-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="25ddf-125">**Impossibile trovare la pagina. Verificare l'indirizzo e riprovare.**</span><span class="sxs-lookup"><span data-stu-id="25ddf-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="25ddf-126">*Correzione:*</span><span class="sxs-lookup"><span data-stu-id="25ddf-126">*Fix:*</span></span>

1. <span data-ttu-id="25ddf-127">In Microsoft Edge, vai a **Impostazioni** > **Cookie e autorizzazioni del sito** > **Cookie e dati del sito**.</span><span class="sxs-lookup"><span data-stu-id="25ddf-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="25ddf-128">Sposta l'interruttore **Consenti ai siti di salvare e leggere i dati dei cookie** a destra (On).</span><span class="sxs-lookup"><span data-stu-id="25ddf-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="25ddf-129">Consentire popup in Business Central</span><span class="sxs-lookup"><span data-stu-id="25ddf-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="25ddf-130">si integra con diversi prodotti.</span><span class="sxs-lookup"><span data-stu-id="25ddf-130">integrates with several products.</span></span> <span data-ttu-id="25ddf-131">In alcuni casi, come con Microsoft Teams, vengono visualizzati [!INCLUDE[prod_short](includes/prod_short.md)] o "popup", nel prodotto.</span><span class="sxs-lookup"><span data-stu-id="25ddf-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="25ddf-132">Per questa funzionalità il browser deve consentire i popup in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="25ddf-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="25ddf-133">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="25ddf-133">*Problem:*</span></span>

<span data-ttu-id="25ddf-134">Se i popup per [!INCLUDE[prod_short](includes/prod_short.md)] sono bloccati, viene visualizzato un messaggio simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="25ddf-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="25ddf-135">**Si è verificato un errore. Il browser potrebbe bloccare i popup necessari per Business Central.**</span><span class="sxs-lookup"><span data-stu-id="25ddf-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="25ddf-136">*Correzione:*</span><span class="sxs-lookup"><span data-stu-id="25ddf-136">*Fix:*</span></span>

1. <span data-ttu-id="25ddf-137">In Microsoft Edge, vai a **Impostazioni** > **Cookie e autorizzazioni del sito** > **Popup e reindirizzamenti**.</span><span class="sxs-lookup"><span data-stu-id="25ddf-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="25ddf-138">Sposta l'interruttore **Bloccato** a destra (On).</span><span class="sxs-lookup"><span data-stu-id="25ddf-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="25ddf-139">Seleziona **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="25ddf-139">Select **Add**.</span></span> <span data-ttu-id="25ddf-140">Nella casella **Sito**, digita `https://businesscentral.dynamics.com`, quindi seleziona **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="25ddf-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="25ddf-141">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="25ddf-141">See Also</span></span>

[<span data-ttu-id="25ddf-142">Risoluzione dei problemi relativi a Teams</span><span class="sxs-lookup"><span data-stu-id="25ddf-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]