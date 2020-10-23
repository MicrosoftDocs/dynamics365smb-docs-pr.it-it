---
title: Utilizzo dei dati di Business Central in Microsoft Teams | Microsoft Docs
description: Informazioni su come utilizzare l'app Business Central per Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989425"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="7617d-103">Utilizzo dei dati Business Central in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7617d-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="7617d-104">[!INCLUDE [prodshort](includes/prodshort.md)] offre un'app che connette Microsoft Teams ai dati aziendali in [!INCLUDE [prodshort](includes/prodshort.md)], in modo da poter condividere rapidamente i dettagli tra i membri del team e rispondere più rapidamente alle richieste.</span><span class="sxs-lookup"><span data-stu-id="7617d-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="7617d-105">In questo articolo viene descritto come utilizzare l'app per condividere i dati [!INCLUDE [prodshort](includes/prodshort.md)] con i colleghi in una conversazione di Teams.</span><span class="sxs-lookup"><span data-stu-id="7617d-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="7617d-106">Sintesi</span><span class="sxs-lookup"><span data-stu-id="7617d-106">Overview</span></span>

<span data-ttu-id="7617d-107">L'app [!INCLUDE [prodshort](includes/prodshort.md)] consente di:</span><span class="sxs-lookup"><span data-stu-id="7617d-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="7617d-108">Copiare un collegamento a qualsiasi record di Business Central e incollarlo in una conversazione di Teams per condividerlo con i colleghi.</span><span class="sxs-lookup"><span data-stu-id="7617d-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="7617d-109">Il collegamento viene aperto in una scheda interattiva compatta che visualizza le informazioni sul record.</span><span class="sxs-lookup"><span data-stu-id="7617d-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="7617d-110">Una volta nella conversazione, l'utente e i colleghi possono visualizzare ulteriori dettagli sul record, modificare i dati e intraprendere azioni, senza uscire da Teams.</span><span class="sxs-lookup"><span data-stu-id="7617d-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="7617d-111">[![Integrazione di Teams con Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7617d-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7617d-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7617d-112">Prerequisites</span></span>

- <span data-ttu-id="7617d-113">Avere accesso a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7617d-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="7617d-114">Avere installato l'app [!INCLUDE [prodshort](includes/prodshort.md)] in Teams.</span><span class="sxs-lookup"><span data-stu-id="7617d-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="7617d-115">Per ulteriori informazioni, vedere [Installare l'app [!INCLUDE [prodshort](includes/prodshort.md)] per Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="7617d-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="7617d-116">Tutti i partecipanti a una conversazione di Teams saranno in grado di visualizzare le schede per i record di Business Central inviati alla conversazione.</span><span class="sxs-lookup"><span data-stu-id="7617d-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="7617d-117">Tuttavia per visualizzare maggiori dettagli sui record, utilizzando i pulsanti **Dettagli** o **Apri nuova finestra** in una scheda, sarà necessario accedere a [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="7617d-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="7617d-118">Per ulteriori informazioni, vedere [Gestione dell'integrazione di Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="7617d-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="7617d-119">Includere una scheda Business Central in una conversazione di Teams</span><span class="sxs-lookup"><span data-stu-id="7617d-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="7617d-120">Accedere a [!INCLUDE [prodshort](includes/prodshort.md)] utilizzando il browser.</span><span class="sxs-lookup"><span data-stu-id="7617d-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="7617d-121">Aprire il record che si desidera condividere.</span><span class="sxs-lookup"><span data-stu-id="7617d-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="7617d-122">L'app è progettata per visualizzare le pagine di tipo scheda da [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="7617d-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="7617d-123">Quindi aprire una pagina che visualizza un singolo record, come un articolo, un cliente o un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="7617d-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="7617d-124">Non è possibile utilizzarla per la Gestione ruolo utente o le pagine che visualizzano più record in un elenco.</span><span class="sxs-lookup"><span data-stu-id="7617d-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="7617d-125">Copiare l'intero URL dalla barra degli indirizzi del browser.</span><span class="sxs-lookup"><span data-stu-id="7617d-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Copiare l'URL di Business Central dal browser](media/teams-url.png)
4. <span data-ttu-id="7617d-127">Accedere a Teams e avviare una conversazione, che può essere una chat con una persona, un gruppo di persone o un canale del team.</span><span class="sxs-lookup"><span data-stu-id="7617d-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="7617d-128">Incollare l'URL nella casella in cui si aggiunge un messaggio.</span><span class="sxs-lookup"><span data-stu-id="7617d-128">Paste the URL into the box where you add a message.</span></span>

   ![Incollare l'URL di Business Central in Teams](media/teams-paste-url.png)
6. <span data-ttu-id="7617d-130">La prima volta che si incolla un collegamento in una conversazione, verrà richiesto di accedere a [!INCLUDE [prodshort](includes/prodshort.md)] e fornire il consenso all'app per il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="7617d-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="7617d-131">Seguire le istruzioni sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="7617d-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7617d-132">È necessario eseguire questo passaggio solo una volta.</span><span class="sxs-lookup"><span data-stu-id="7617d-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="7617d-133">Attendere mentre viene generata una scheda nella casella del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7617d-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="7617d-134">Quando viene visualizzata la scheda, esaminare attentamente il contenuto della scheda per eventuali informazioni sensibili prima di inviare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7617d-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="7617d-135">Questo passaggio è importante perché una volta inviato il messaggio, tutti i partecipanti alla conversazione possono vedere la scheda.</span><span class="sxs-lookup"><span data-stu-id="7617d-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="7617d-136">Se la scheda ha l'aspetto desiderato, selezionare **Invia** per inviarla alla conversazione.</span><span class="sxs-lookup"><span data-stu-id="7617d-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="7617d-137">Dopo che viene visualizzata la scheda e prima di selezionare **Invia** è possibile eliminare l'URL incollato, se desiderato.</span><span class="sxs-lookup"><span data-stu-id="7617d-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="7617d-138">Per visualizzare ulteriori dettagli o apportare modifiche al record, selezionare **Dettagli**.</span><span class="sxs-lookup"><span data-stu-id="7617d-138">To view more details or make changes to the record, select **Details**.</span></span>

    <span data-ttu-id="7617d-139">La pagina dei dettagli è simile a quella che viene visualizzata in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="7617d-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="7617d-140">Tuttavia è leggermente adattata per Teams.</span><span class="sxs-lookup"><span data-stu-id="7617d-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="7617d-141">Al termine della visualizzazione e delle modifiche, chiudere la finestra per tornare alla conversazione di Teams.</span><span class="sxs-lookup"><span data-stu-id="7617d-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7617d-142">Eventuali modifiche apportate non si rifletteranno nella scheda fino alla volta successiva che si incolla il collegamento in una conversazione.</span><span class="sxs-lookup"><span data-stu-id="7617d-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="7617d-143">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7617d-143">See Also</span></span>

[<span data-ttu-id="7617d-144">Panoramica dell'integrazione di Business Central e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7617d-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="7617d-145">[Installare l'app [!INCLUDE [prodshort](includes/prodshort.md)] per Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="7617d-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="7617d-146">Sviluppo per l'integrazione di Teams</span><span class="sxs-lookup"><span data-stu-id="7617d-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="7617d-147">Introduzione</span><span class="sxs-lookup"><span data-stu-id="7617d-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
