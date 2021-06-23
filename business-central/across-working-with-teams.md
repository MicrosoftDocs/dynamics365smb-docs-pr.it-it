---
title: Condivisione dei record di Business Central in Microsoft Teams
description: Informazioni su come utilizzare l'app Business Central per Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: 8add662badbc0d791d6a37d0feb4e3a756519f00
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074589"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a><span data-ttu-id="4c2b9-103">Condivisione dei record di Business Central in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4c2b9-103">Sharing Business Central Records in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="4c2b9-104">[!INCLUDE [prod_short](includes/prod_short.md)] offre un'app che connette Microsoft Teams ai dati aziendali in [!INCLUDE [prod_short](includes/prod_short.md)], in modo da poter condividere rapidamente i dettagli tra i membri del team e rispondere più rapidamente alle richieste.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="4c2b9-105">In questo articolo viene descritto come utilizzare l'app per condividere i record di [!INCLUDE [prod_short](includes/prod_short.md)], come un cliente, un ordine vendita o una fattura, con i colleghi in una conversazione di Teams.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="4c2b9-106">Sintesi</span><span class="sxs-lookup"><span data-stu-id="4c2b9-106">Overview</span></span>

<span data-ttu-id="4c2b9-107">L'app [!INCLUDE [prod_short](includes/prod_short.md)] consente di:</span><span class="sxs-lookup"><span data-stu-id="4c2b9-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="4c2b9-108">Copiare un collegamento a qualsiasi record di Business Central e incollarlo in una conversazione di Teams per condividerlo con i colleghi.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="4c2b9-109">L'app espanderà il collegamento in una scheda interattiva compatta che visualizza le informazioni sul record.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="4c2b9-110">Una volta nella conversazione, l'utente e i colleghi possono visualizzare ulteriori dettagli sul record, modificare i dati e intraprendere azioni, senza uscire da Teams.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="4c2b9-111">[![Integrazione di Teams con Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="4c2b9-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4c2b9-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4c2b9-112">Prerequisites</span></span>

- <span data-ttu-id="4c2b9-113">Avere accesso a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="4c2b9-114">Avere installato l'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="4c2b9-115">Per ulteriori informazioni, vedere [Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="4c2b9-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="4c2b9-116">Tutti i partecipanti a una conversazione di Teams saranno in grado di visualizzare le schede per i record di Business Central inviati alla conversazione.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="4c2b9-117">Tuttavia per visualizzare maggiori dettagli sui record, utilizzando i pulsanti **Dettagli** o **Apri nuova finestra** in una scheda, sarà necessario accedere a [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="4c2b9-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="4c2b9-118">Per ulteriori informazioni, vedere [Gestione dell'integrazione di Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="4c2b9-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="4c2b9-119">Includere una scheda Business Central in una conversazione di Teams</span><span class="sxs-lookup"><span data-stu-id="4c2b9-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="4c2b9-120">Accedere a [!INCLUDE [prod_short](includes/prod_short.md)] utilizzando il browser.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="4c2b9-121">Aprire il record che si desidera condividere.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="4c2b9-122">L'app è progettata per visualizzare le pagine di tipo scheda da [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="4c2b9-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="4c2b9-123">Quindi aprire una pagina che visualizza un singolo record, come un articolo, un cliente o un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="4c2b9-124">Non è possibile utilizzarla per la Gestione ruolo utente o le pagine che visualizzano più record in un elenco.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="4c2b9-125">Copiare l'intero URL dalla barra degli indirizzi del browser.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Copiare l'URL di Business Central dal browser](media/teams-url-v2.png)
4. <span data-ttu-id="4c2b9-127">Accedere a Teams e avviare una conversazione, che può essere una chat con una persona, un gruppo di persone o un canale del team.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="4c2b9-128">Incollare l'URL nella casella del messaggio in cui si compone un messaggio.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Incollare l'URL di Business Central in Teams](media/teams-paste-url-v2.png)
6. <span data-ttu-id="4c2b9-130">La prima volta che si incolla un collegamento in una conversazione, verrà richiesto di accedere a [!INCLUDE [prod_short](includes/prod_short.md)] e fornire il consenso all'app per il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="4c2b9-131">Seguire le istruzioni sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4c2b9-132">È necessario eseguire questo passaggio solo una volta.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="4c2b9-133">Attendere mentre viene generata una scheda nella casella del messaggio.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="4c2b9-134">Quando viene visualizzata la scheda, esaminare attentamente il contenuto della scheda per eventuali informazioni sensibili prima di inviare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="4c2b9-135">Questo passaggio è importante perché una volta inviato il messaggio, tutti i partecipanti alla conversazione possono vedere la scheda.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="4c2b9-136">Se la scheda ha l'aspetto desiderato, selezionare **Invia** per inviarla alla conversazione.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="4c2b9-137">Dopo che viene visualizzata la scheda e prima di selezionare **Invia** è possibile eliminare l'URL incollato, se desiderato.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="4c2b9-138">Per visualizzare ulteriori dettagli o apportare modifiche al record visualizzato nella scheda, selezionare **Dettagli**.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="4c2b9-139">Per ulteriori informazioni, vedere la sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="4c2b9-140">Visualizzare i dettagli della scheda</span><span class="sxs-lookup"><span data-stu-id="4c2b9-140">View card details</span></span>

<span data-ttu-id="4c2b9-141">Una volta che una scheda è stata inviata a una conversazione, tutti i partecipanti con le [autorizzazioni adeguate](admin-teams-integration.md#permissions) possono selezionare **Dettagli** per aprire una finestra che visualizza ulteriori informazioni sul record ed eventualmente apportare modifiche al record.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="4c2b9-142">Non importa se sei tu a inviare la scheda o a riceverla.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="4c2b9-143">La funzionalità **Dettagli** è particolarmente utile per i destinatari, perché fornisce loro rapidamente informazioni concise e mirate sul record, anziché dover eseguire la scansione dell'intero record.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="4c2b9-144">La finestra dei dettagli è simile a quella che viene visualizzata nel record di [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="4c2b9-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="4c2b9-145">Tuttavia è leggermente adattata per Teams.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="4c2b9-146">Al termine della visualizzazione e delle modifiche, chiudere la finestra per tornare alla conversazione di Teams.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="4c2b9-147">Ecco un paio di cose da tenere a mente quando si utilizzano i dettagli della scheda:</span><span class="sxs-lookup"><span data-stu-id="4c2b9-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="4c2b9-148">Per visualizzare i dettagli della scheda, gli utenti devono disporre dell'autorizzazione per la pagina e i relativi dati in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="4c2b9-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="4c2b9-149">Le schede nelle chat di Teams non vengono aggiornate automaticamente alle modifiche.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="4c2b9-150">Tutte le modifiche salvate in un record nella finestra dei dettagli vengono salvate in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="4c2b9-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="4c2b9-151">Ma la scheda in Teams non mostrerà le modifiche nella conversione, finché non incollerai nuovamente il collegamento.</span><span class="sxs-lookup"><span data-stu-id="4c2b9-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="4c2b9-152">Per ulteriori informazioni sull'utilizzo delle schede e sui dettagli delle schede, vedi [Domande frequenti su Teams](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="4c2b9-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c2b9-153">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4c2b9-153">See Also</span></span>

[<span data-ttu-id="4c2b9-154">Panoramica dell'integrazione di Business Central e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4c2b9-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="4c2b9-155">[Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="4c2b9-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="4c2b9-156">Domande frequenti su Teams</span><span class="sxs-lookup"><span data-stu-id="4c2b9-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="4c2b9-157">Risoluzione dei problemi relativi a Teams</span><span class="sxs-lookup"><span data-stu-id="4c2b9-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="4c2b9-158">Sviluppo per l'integrazione di Teams</span><span class="sxs-lookup"><span data-stu-id="4c2b9-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]