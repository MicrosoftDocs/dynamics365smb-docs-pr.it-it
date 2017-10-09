---
title: Collegare e modificare le impostazioni salvate nei report | Documenti Microsoft
description: Descrive l'utilizzo delle opzioni predefinite e dei filtri per personalizzare un report e generare dati corretti.
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2783c3a80beed5de6b7f7a63ff6811648ef48df3
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="b9155-103">Gestione impostazioni salvate nei report</span><span class="sxs-lookup"><span data-stu-id="b9155-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="b9155-104">A seconda del report che viene eseguito, potrebbe apparire una pagina che consente di impostare determinate opzioni e filtri per variare i dati inclusi nel report generato.</span><span class="sxs-lookup"><span data-stu-id="b9155-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="b9155-105">Questa pagina è nota come la pagina di richiesta report.</span><span class="sxs-lookup"><span data-stu-id="b9155-105">This page is known as the report request page.</span></span> <span data-ttu-id="b9155-106">Un report può includere uno o più *impostazioni salvate* che è possibile applicare al report dalla pagina di richiesta.</span><span class="sxs-lookup"><span data-stu-id="b9155-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="b9155-107">Le *impostazioni salvate* sono fondamentalmente opzioni e filtri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="b9155-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="b9155-108">L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti.</span><span class="sxs-lookup"><span data-stu-id="b9155-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="b9155-109">È possibile visualizzare le impostazioni salvate a disposizione dell'utente per un report nella sezione **Impostazioni salvate** della pagina di richiesta report.</span><span class="sxs-lookup"><span data-stu-id="b9155-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="to-apply-saved-settings-to-a-report"></a><span data-ttu-id="b9155-110">Per applicare le impostazioni salvate a un report</span><span class="sxs-lookup"><span data-stu-id="b9155-110">To apply saved settings to a report</span></span>
1. <span data-ttu-id="b9155-111">Aprire il report.</span><span class="sxs-lookup"><span data-stu-id="b9155-111">Open the report.</span></span>

   <span data-ttu-id="b9155-112">Viene visualizzata la pagina di richiesta report.</span><span class="sxs-lookup"><span data-stu-id="b9155-112">The report request page appears.</span></span>    
2. <span data-ttu-id="b9155-113">Nella sezione **Impostazioni salvate** della pagina impostare il campo **Nome** sulle impostazioni salvate che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b9155-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="b9155-114">La sezione **Impostazioni salvate** viene visualizzata solo se il report è già stato eseguito in precedenza o se esistono movimenti salvati delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b9155-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="b9155-115">Esiste sempre una voce Impostazioni salvate, che viene chiamata **Filtri e opzioni utilizzati di recente**.</span><span class="sxs-lookup"><span data-stu-id="b9155-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="b9155-116">Queste impostazioni sono i valori delle opzioni e dei filtri che sono stati utilizzati l'ultima volta che è stato eseguito il report.</span><span class="sxs-lookup"><span data-stu-id="b9155-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="administer-saved-report-settings-for-users"></a><span data-ttu-id="b9155-117">L'amministratore ha salvato le impostazioni dei report per gli utenti</span><span class="sxs-lookup"><span data-stu-id="b9155-117">Administer saved report settings for users</span></span>
<span data-ttu-id="b9155-118">Se si dispone delle autorizzazioni appropriate, è possibile visualizzare, creare e modificare le impostazioni salvate per tutti i report di tutti gli utenti nella società.</span><span class="sxs-lookup"><span data-stu-id="b9155-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="b9155-119">È possibile assegnare le impostazioni salvate per un report ai singoli utenti o a tutti gli utenti della società.</span><span class="sxs-lookup"><span data-stu-id="b9155-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="b9155-120">È possibile gestire le impostazioni salvate nella pagina 1506 **Impostazioni report**.</span><span class="sxs-lookup"><span data-stu-id="b9155-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="b9155-121">Per aprire questa pagina, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Impostazioni report**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="b9155-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="b9155-122">Nella pagina **Impostazioni report** è possibile creare impostazioni ex novo o duplicarle e modificare le impostazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="b9155-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="b9155-123">Per modificare le opzioni e i filtri di un'impostazione, scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="b9155-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

> [!NOTE]
> <span data-ttu-id="b9155-124">La funzionalità Impostazioni salvate nei report è rilevante solo quando la proprietà SaveValues della pagina di richiesta è impostata su Sì.</span><span class="sxs-lookup"><span data-stu-id="b9155-124">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="b9155-125">La proprietà SaveValues è impostata nell'ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="b9155-125">The SaveValues property property is set in the development environment.</span></span>  

> [!Important]
> <span data-ttu-id="b9155-126">Se si crea un articolo impostazioni salvato per tutti gli utenti con lo stesso nome di un'impostazione salvata esistente per un utente specifico, tale utente non potrà utilizzare le impostazioni salvate assegnata a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="b9155-126">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="b9155-127">Nel campo Impostazioni salvate nella pagina di richiesta del report, l'utente vedrà due opzioni delle impostazioni salvate con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="b9155-127">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="b9155-128">Tuttavia, indipendentemente dall'opzione che sceglie, verranno usate le impostazioni salvate specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b9155-128">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9155-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9155-129">See Also</span></span>
[<span data-ttu-id="b9155-130">Utilizzo dei report</span><span class="sxs-lookup"><span data-stu-id="b9155-130">Working with Reports</span></span>](ui-work-report.md)  

