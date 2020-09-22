---
title: Collegare e modificare le impostazioni salvate nei report | Documenti Microsoft
description: Descrive l'utilizzo delle opzioni predefinite e dei filtri per personalizzare un report e generare dati corretti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d61e599b9e86f28de6edcf4ccff5b245503880fe
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784611"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="f2b42-103">Gestire impostazioni salvate per report e processi batch</span><span class="sxs-lookup"><span data-stu-id="f2b42-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="f2b42-104">Quando si eseguono report, gli utenti di norma vedono una pagina che consente loro di selezionare opzioni e impostare filtri per modificare i dati inclusi nel report generato.</span><span class="sxs-lookup"><span data-stu-id="f2b42-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="f2b42-105">Questa pagina è denominata la pagina di richiesta.</span><span class="sxs-lookup"><span data-stu-id="f2b42-105">This page is called the request page.</span></span> <span data-ttu-id="f2b42-106">Un report può includere uno o più *impostazioni salvate* che gli utenti possono applicare al report dalla pagina di richiesta.</span><span class="sxs-lookup"><span data-stu-id="f2b42-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="f2b42-107">Le *impostazioni salvate* sono fondamentalmente opzioni e filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f2b42-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="f2b42-108">L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti.</span><span class="sxs-lookup"><span data-stu-id="f2b42-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="f2b42-109">Per ulteriori informazioni, vedere [Uso delle impostazioni salvate](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="f2b42-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="f2b42-110">Questo argomento fa essenzialmente riferimento a “report" ma informazioni simili si applicano ai processi batch.</span><span class="sxs-lookup"><span data-stu-id="f2b42-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="f2b42-111">Se si dispone delle autorizzazioni appropriate, è possibile visualizzare, creare e modificare le impostazioni salvate per tutti i report di tutti gli utenti in una società.</span><span class="sxs-lookup"><span data-stu-id="f2b42-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="f2b42-112">È possibile assegnare le impostazioni salvate per un report ai singoli utenti o a tutti gli utenti della società.</span><span class="sxs-lookup"><span data-stu-id="f2b42-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="f2b42-113">Per creare e modificare impostazioni salvate per tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="f2b42-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="f2b42-114">È possibile gestire le impostazioni salvate nella pagina **Impostazioni report**.</span><span class="sxs-lookup"><span data-stu-id="f2b42-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="f2b42-115">Sono disponibili due modi per aprire questa pagina:</span><span class="sxs-lookup"><span data-stu-id="f2b42-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="f2b42-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Impostazioni report** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="f2b42-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="f2b42-117">Aprire un report, scegliere la funzionalità di ricerca nel campo **Utilizza valori predefiniti da:**, quindi scegliere l'azione **Seleziona da elenco completo**.</span><span class="sxs-lookup"><span data-stu-id="f2b42-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="f2b42-118">Nella pagina vengono visualizzate tutte le voci delle impostazioni salvate esistenti per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="f2b42-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="f2b42-119">Se esiste un nome utente nel campo **Assegnato a**, solo tale utente può utilizzare le impostazioni salvate per il report associato.</span><span class="sxs-lookup"><span data-stu-id="f2b42-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="f2b42-120">Se è presente un segno di spunta nel campo **Condiviso con tutti gli utenti**, tutti gli utenti possono utilizzare le impostazioni salvate per il report.</span><span class="sxs-lookup"><span data-stu-id="f2b42-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="f2b42-121">Nella pagina **Impostazioni report**, è possibile:</span><span class="sxs-lookup"><span data-stu-id="f2b42-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="f2b42-122">Scegliere l'azione **Nuovo** per creare da zero una nuova voce di impostazioni salvate.</span><span class="sxs-lookup"><span data-stu-id="f2b42-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="f2b42-123">Selezionare una voce di impostazioni salvate dall'elenco e scegliere l'azione **Copia** per creare una copia.</span><span class="sxs-lookup"><span data-stu-id="f2b42-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="f2b42-124">Selezionare una voce di impostazioni salvate dall'elenco e scegliere l'azione **Modifica** per modificare una voce di impostazioni salvate.</span><span class="sxs-lookup"><span data-stu-id="f2b42-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="f2b42-125">Tenere in considerazione il nome che viene assegnato a una voce di impostazioni salvate.</span><span class="sxs-lookup"><span data-stu-id="f2b42-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="f2b42-126">Se si crea una voce di impostazioni salvate per tutti gli utenti e le si assegna lo stesso nome di una voce di impostazioni salvate esistente solo per un utente specifico, tale utente non potrà utilizzare la voce di impostazioni salvate assegnata a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="f2b42-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="f2b42-127">Nella sezione **Impostazioni salvate** nella pagina di richiesta, l'utente vedrà due voci di impostazioni salvate con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="f2b42-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="f2b42-128">Tuttavia, indipendentemente dall'opzione scelta, verrà usata la voce di impostazioni salvate specifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f2b42-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="f2b42-129">La funzionalità Impostazioni salvate è disponibile solo nei report in cui la [proprietà SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) della pagina di richiesta del report è impostata su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="f2b42-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="f2b42-130">La proprietà **SaveValues** viene impostata nell'ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="f2b42-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f2b42-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f2b42-131">See Also</span></span>
[<span data-ttu-id="f2b42-132">Utilizzo di report, processi batch e XMLport</span><span class="sxs-lookup"><span data-stu-id="f2b42-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
