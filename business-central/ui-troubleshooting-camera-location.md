---
title: 'Risoluzione dei problemi: accesso alla fotocamera e alla posizione'
description: In questo articolo viene descritto come risolvere i problemi relativi all'accesso alle informazioni sulla fotocamera e sulla posizione in Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.openlocfilehash: b44044b9ec2c71ad3b99f25b4a941a3ab473ca4f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912023"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="19527-103">Risoluzione dei problemi: accesso alla fotocamera e alla posizione</span><span class="sxs-lookup"><span data-stu-id="19527-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="19527-104">È possibile che si riscontrino problemi quando si prova ad accedere alla fotocamera e alle informazioni sulla posizione di un dispositivo da [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="19527-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="19527-105">È possibile trovare le possibili cause e risoluzioni di questi problemi di seguito.</span><span class="sxs-lookup"><span data-stu-id="19527-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="19527-106">Il dispositivo deve avere fotocamera e funzionalità di posizione</span><span class="sxs-lookup"><span data-stu-id="19527-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="19527-107">Per accedere alla fotocamera o alla posizione di un utente da un dispositivo, il dispositivo deve avere, rispettivamente, una fotocamera fisica o la capacità di recuperare le informazioni sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="19527-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="19527-108">Se il dispositivo dispone di fotocamera e funzionalità di posizione, ma si riscontrano ancora problemi, è possibile che alcuni driver necessitino di aggiornamento o reinstallazione.</span><span class="sxs-lookup"><span data-stu-id="19527-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="19527-109">Anche se non si è sicuri, si consiglia sempre di aggiornare il sistema operativo del dispositivo, i driver e il browser alla versione più recente per la migliore esperienza.</span><span class="sxs-lookup"><span data-stu-id="19527-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="19527-110">Autorizzazioni di accesso non abilitate</span><span class="sxs-lookup"><span data-stu-id="19527-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="19527-111">È necessario abilitare l'accesso generale alla fotocamera e alla posizione dalle impostazioni sulla privacy del dispositivo e concedere esplicitamente a [!INCLUDE[prodshort](includes/prodshort.md)] l'autorizzazione ad accedervi.</span><span class="sxs-lookup"><span data-stu-id="19527-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prodshort](includes/prodshort.md)] to access them.</span></span> <span data-ttu-id="19527-112">Ad esempio, per vedere o modificare le autorizzazioni per un dispositivo in esecuzione su Windows, andare a **Impostazioni**, scegliere **Privacy** e quindi **Autorizzazioni dell'app**.</span><span class="sxs-lookup"><span data-stu-id="19527-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="19527-113">Per i dispositivi mobili, è necessario concedere le autorizzazioni di accesso alla fotocamera e alla posizione all'app mobile [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="19527-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prodshort](includes/prodshort.md)] Mobile App.</span></span> <span data-ttu-id="19527-114">Per farlo per un dispositivo iOS, andare a **Impostazioni**, scegliere **Privacy** e quindi **Fotocamera** o **Posizione**.</span><span class="sxs-lookup"><span data-stu-id="19527-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="19527-115">Per i dispositivi Android, andare a **Impostazioni**, scegliere **App e notifiche**, **Avanzate**, **Gestione autorizzazioni** e quindi **Fotocamera** o **Posizione**.</span><span class="sxs-lookup"><span data-stu-id="19527-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="19527-116">Inoltre, se si sta utilizzando [!INCLUDE[prodshort](includes/prodshort.md)] in un browser, è necessario concedere al sito [!INCLUDE[prodshort](includes/prodshort.md)] l'autorizzazione ad accedere alla fotocamera o alle informazioni sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="19527-116">In addition, if you are using [!INCLUDE[prodshort](includes/prodshort.md)] in a browser, you must also grant the [!INCLUDE[prodshort](includes/prodshort.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="19527-117">Per visualizzare o modificare le autorizzazioni di un sito nel browser Microsoft Edge, andare a **Impostazioni**, scegliere **Autorizzazioni sito** e quindi **Fotocamera** o **Posizione**.</span><span class="sxs-lookup"><span data-stu-id="19527-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="19527-118">Da notare che questo potrebbe essere diverso per altri browser.</span><span class="sxs-lookup"><span data-stu-id="19527-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="19527-119">Per impostazione predefinita, il dispositivo o il browser visualizzerà una richiesta per accedere a queste funzionalità quando l'utente le attiva per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="19527-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="19527-120">Alcuni browser precedenti non consentono l'accesso alla fotocamera e alla posizione.</span><span class="sxs-lookup"><span data-stu-id="19527-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="19527-121">Ad esempio, la fotocamera non è disponibile in Internet Explorer o nel browser Edge legacy.</span><span class="sxs-lookup"><span data-stu-id="19527-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="19527-122">Connessione client Web non protetta</span><span class="sxs-lookup"><span data-stu-id="19527-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="19527-123">La fotocamera e le funzionalità di posizione sono disponibili solo quando si accede al client Web tramite connessioni HTTP protette da SSL, utilizzando lo schema URI `https://`.</span><span class="sxs-lookup"><span data-stu-id="19527-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="19527-124">L'unica eccezione è la connessione a `http://localhost`, utilizzato per scopi di sviluppo e test.</span><span class="sxs-lookup"><span data-stu-id="19527-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="19527-125">Lavorare con le tecnologie di virtualizzazione</span><span class="sxs-lookup"><span data-stu-id="19527-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="19527-126">Quando ci si collega a [!INCLUDE[prodshort](includes/prodshort.md)] tramite Desktop remoto o un'altra virtualizzazione, l'accesso alla fotocamera o alla posizione potrebbe non essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="19527-126">When connecting to [!INCLUDE[prodshort](includes/prodshort.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="19527-127">In tal caso, utilizzare invece il sistema fisico.</span><span class="sxs-lookup"><span data-stu-id="19527-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="19527-128">Software antivirus</span><span class="sxs-lookup"><span data-stu-id="19527-128">Antivirus Software</span></span>
<span data-ttu-id="19527-129">Alcuni programmi software antivirus bloccano l'accesso alla fotocamera e alla posizione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="19527-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="19527-130">Ricordare di controllare le impostazioni del software antivirus.</span><span class="sxs-lookup"><span data-stu-id="19527-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="19527-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="19527-131">See Also</span></span>
[<span data-ttu-id="19527-132">Implementazione della fotocamera in AL</span><span class="sxs-lookup"><span data-stu-id="19527-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="19527-133">Implementazione della posizione in AL</span><span class="sxs-lookup"><span data-stu-id="19527-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
