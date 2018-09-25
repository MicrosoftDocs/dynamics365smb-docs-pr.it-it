---
title: Collegare e modificare le impostazioni salvate nei report | Documenti Microsoft
description: Descrive l'utilizzo delle opzioni predefinite e dei filtri per personalizzare un report e generare dati corretti.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: 2a7ab137a9bf8ec3580e718053f8e67320e3af5a
ms.contentlocale: it-it
ms.lasthandoff: 08/06/2018

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="1bc55-103">Gestione impostazioni salvate nei report</span><span class="sxs-lookup"><span data-stu-id="1bc55-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="1bc55-104">Quando si esegue un report, gli utenti di norma vedono una pagina che consente loro di impostare determinate opzioni e filtri per variare i dati inclusi nel report generato.</span><span class="sxs-lookup"><span data-stu-id="1bc55-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="1bc55-105">Questa pagina è chiamata la pagina di richiesta report.</span><span class="sxs-lookup"><span data-stu-id="1bc55-105">This page is called the report request page.</span></span> <span data-ttu-id="1bc55-106">Un report può includere uno o più *impostazioni salvate* che gli utenti possono applicare al report dalla pagina di richiesta.</span><span class="sxs-lookup"><span data-stu-id="1bc55-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="1bc55-107">Le *impostazioni salvate* sono fondamentalmente opzioni e filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="1bc55-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="1bc55-108">L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti.</span><span class="sxs-lookup"><span data-stu-id="1bc55-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="1bc55-109">Per ulteriori informazioni su come utilizzare le impostazioni salvate, vedere [Uso delle impostazioni salvate](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="1bc55-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="1bc55-110">Se si dispone delle autorizzazioni appropriate, è possibile visualizzare, creare e modificare le impostazioni salvate per tutti i report di tutti gli utenti nella società.</span><span class="sxs-lookup"><span data-stu-id="1bc55-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="1bc55-111">È possibile assegnare le impostazioni salvate per un report ai singoli utenti o a tutti gli utenti della società.</span><span class="sxs-lookup"><span data-stu-id="1bc55-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="1bc55-112">Creare e modificare le impostazioni salvate per tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="1bc55-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="1bc55-113">È possibile gestire le impostazioni salvate nella pagina **1560 Impostazioni report**.</span><span class="sxs-lookup"><span data-stu-id="1bc55-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="1bc55-114">Sono disponibili due modi per aprire questa pagina:</span><span class="sxs-lookup"><span data-stu-id="1bc55-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="1bc55-115">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Impostazioni report**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="1bc55-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="1bc55-116">Aprire un report, scegliere la funzionalità di ricerca accanto alla casella **Utilizza valori predefiniti da:**, scegliere **Seleziona da elenco completo**.</span><span class="sxs-lookup"><span data-stu-id="1bc55-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="1bc55-117">Nella pagina vengono visualizzate tutte le voci delle impostazioni salvate esistenti per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="1bc55-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="1bc55-118">Se esiste un nome utente nella colonna **Assegnato a**, solo tale utente può utilizzare le impostazioni salvate per il report associato.</span><span class="sxs-lookup"><span data-stu-id="1bc55-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="1bc55-119">Se è presente un segno di spunta nella colonna **Condiviso con tutti gli utenti**, tutti gli utenti possono utilizzare le impostazioni salvate per il report.</span><span class="sxs-lookup"><span data-stu-id="1bc55-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="1bc55-120">Nella pagina **Impostazioni report**, è possibile:</span><span class="sxs-lookup"><span data-stu-id="1bc55-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="1bc55-121">Scegliere **Nuovo** per creare da zero una nuova voce di impostazioni salvate.</span><span class="sxs-lookup"><span data-stu-id="1bc55-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="1bc55-122">Selezionare una voce di impostazioni salvate dall'elenco e scegliere **Copia** per creare una copia.</span><span class="sxs-lookup"><span data-stu-id="1bc55-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="1bc55-123">Selezionare una voce di impostazioni salvate dall'elenco e scegliere **Modifica** per modificare una voce di impostazioni salvate.</span><span class="sxs-lookup"><span data-stu-id="1bc55-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="1bc55-124">Tenere in considerazione il nome che viene assegnato a una voce di impostazioni salvate.</span><span class="sxs-lookup"><span data-stu-id="1bc55-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="1bc55-125">Se si crea una voce di impostazioni salvate per tutti gli utenti e le si assegna lo stesso nome di una voce di impostazioni salvate esistente solo per un utente specifico, tale utente non potrà utilizzare la voce di impostazioni salvate assegnata a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="1bc55-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="1bc55-126">Nel campo **Impostazioni salvate** nella pagina di richiesta del report, l'utente vedrà due voci di impostazioni salvate con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="1bc55-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="1bc55-127">Tuttavia, indipendentemente dall'opzione che sceglie, verrà usata la voce di impostazioni salvate specifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1bc55-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="1bc55-128">La funzionalità delle impostazioni salvate è disponibile solo nei report in cui la [proprietà SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) della pagina di richiesta del report è impostata su `Yes`.</span><span class="sxs-lookup"><span data-stu-id="1bc55-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="1bc55-129">La proprietà **SaveValues** viene impostata nell'ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="1bc55-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1bc55-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bc55-130">See Also</span></span>
[<span data-ttu-id="1bc55-131">Utilizzo dei report</span><span class="sxs-lookup"><span data-stu-id="1bc55-131">Working with Reports</span></span>](ui-work-report.md)  

