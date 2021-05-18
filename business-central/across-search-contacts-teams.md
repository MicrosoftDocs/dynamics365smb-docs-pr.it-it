---
title: Ricerca di contatti da Microsoft Teams
description: Informazioni su come cercare clienti, fornitori e altri contatti di Business Central da Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 6d094e365ad0c7da73467e5a3160d926902c45d9
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935163"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="78f71-103">Ricerca di clienti, fornitori e altri contatti da Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="78f71-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="78f71-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="78f71-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="78f71-105">Introdotto nel primo ciclo di rilascio del 2021.</span><span class="sxs-lookup"><span data-stu-id="78f71-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="78f71-106">[!INCLUDE [prod_short](includes/prod_short.md)] dispone di un sistema completo di gestione dei contatti aziendali, essenziale per gli utenti nelle vendite, nelle operazioni o in altri ruoli dipartimentali.</span><span class="sxs-lookup"><span data-stu-id="78f71-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="78f71-107">Se sei un utente in uno di questi ruoli, dovrai spesso cercare, incontrare o avviare una conversazione con i tuoi fornitori, clienti e altri contatti.</span><span class="sxs-lookup"><span data-stu-id="78f71-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="78f71-108">Con l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams, puoi eseguire queste attività direttamente da Teams, senza dover passare a [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="78f71-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="78f71-109">Da Teams puoi:</span><span class="sxs-lookup"><span data-stu-id="78f71-109">From within Teams, you can:</span></span>

- <span data-ttu-id="78f71-110">cercare i contatti [!INCLUDE [prod_short](includes/prod_short.md)] dalla casella di comando Teams o dall'area di composizione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="78f71-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="78f71-111">I contatti possono includere potenziali clienti, fornitori, clienti o altre relazioni d'affari.</span><span class="sxs-lookup"><span data-stu-id="78f71-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="78f71-112">Condividi un contatto come scheda in una conversazione di Teams.</span><span class="sxs-lookup"><span data-stu-id="78f71-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="78f71-113">Visualizza i dettagli sul contatto, la cronologia delle interazioni e altri approfondimenti come pagamenti in sospeso o documenti aperti.</span><span class="sxs-lookup"><span data-stu-id="78f71-113">View details about the contact, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="78f71-114">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="78f71-114">Prerequisites</span></span>

- <span data-ttu-id="78f71-115">Avere accesso a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="78f71-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="78f71-116">Avere installato l'app [!INCLUDE [prod_short](includes/prod_short.md)] in Teams.</span><span class="sxs-lookup"><span data-stu-id="78f71-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="78f71-117">Per ulteriori informazioni, vedere [Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="78f71-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="78f71-118">Hai un account [!INCLUDE [prod_short](includes/prod_short.md)] con accesso ai contatti in almeno un'azienda.</span><span class="sxs-lookup"><span data-stu-id="78f71-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="78f71-119">Sia che tu stia cercando dalla casella di comando o dalla casella di composizione del messaggio, ti potrebbe essere chiesto di accedere o configurare l'app la prima volta.</span><span class="sxs-lookup"><span data-stu-id="78f71-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="78f71-120">Questo passaggio è necessario per cercare i contatti nella società Business Central corretta.</span><span class="sxs-lookup"><span data-stu-id="78f71-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="78f71-121">Per informazioni sulla configurazione dell'app per scegliere la tua azienda, vedi [Modifica della società e di altre impostazioni in Teams](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="78f71-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="78f71-122">Cerca i contatti dalla casella di comando</span><span class="sxs-lookup"><span data-stu-id="78f71-122">Look up contacts from the command box</span></span>

<span data-ttu-id="78f71-123">La casella di comando si trova nella parte superiore di ogni schermata in Teams.</span><span class="sxs-lookup"><span data-stu-id="78f71-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="78f71-124">Ti consente di cercare, eseguire azioni rapide o avviare app, come l'app [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="78f71-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="78f71-125">La ricerca dalla casella di comando è ottima per cercare rapidamente i contatti e i relativi dati per uso personale.</span><span class="sxs-lookup"><span data-stu-id="78f71-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="78f71-126">Supponi, ad esempio, di voler cercare un indirizzo di posta elettronica di un fornitore per organizzare una riunione del calendario.</span><span class="sxs-lookup"><span data-stu-id="78f71-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="78f71-127">Oppure vuoi cercare la cronologia delle interazioni durante una riunione con un cliente.</span><span class="sxs-lookup"><span data-stu-id="78f71-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="78f71-128">Nella casella di comando, digita **@Business Central**, quindi seleziona l'app Business Central dai risultati.</span><span class="sxs-lookup"><span data-stu-id="78f71-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Apri l'app Business Central per cercare i contatti dalla casella di comando](media/teams-contacts-command-1.png)

2. <span data-ttu-id="78f71-130">Nella casella **Business Central**, inizia a digitare il testo di ricerca, come un nome, un indirizzo o un numero di telefono.</span><span class="sxs-lookup"><span data-stu-id="78f71-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="78f71-131">Durante la digitazione, verranno visualizzati i risultati corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="78f71-131">As you type, matching results will appear.</span></span>

    ![Ricerca contatti Business Central dalla casella di comando in Teams](media/teams-contacts-command-2.png)
3. <span data-ttu-id="78f71-133">Seleziona un contatto dai risultati.</span><span class="sxs-lookup"><span data-stu-id="78f71-133">Select a contact from the results.</span></span>

    <span data-ttu-id="78f71-134">La scheda del contatto viene visualizzata sotto la casella di comando.</span><span class="sxs-lookup"><span data-stu-id="78f71-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="78f71-135">Se desideri aggiungere la scheda del contatto a una conversazione, vai nell'angolo in alto a destra della scheda e seleziona **... (Più opzioni)** > **Copia**.</span><span class="sxs-lookup"><span data-stu-id="78f71-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="78f71-136">Quindi, incolla la copia nella casella di composizione del messaggio di una conversazione.</span><span class="sxs-lookup"><span data-stu-id="78f71-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="78f71-137">Per informazioni più generali sulla casella di comando in Teams, vedi [Teams: utilizza la casella di comando](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="78f71-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="78f71-138">Cerca i contatti dalla casella di composizione del messaggio</span><span class="sxs-lookup"><span data-stu-id="78f71-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="78f71-139">Il vantaggio di utilizzare la casella di composizione del messaggio è che puoi aggiungere una scheda del contatto direttamente a una conversazione, affinché gli altri possano vederla.</span><span class="sxs-lookup"><span data-stu-id="78f71-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="78f71-140">Sotto alla casella di composizione del messaggio, seleziona l'icona **Business Central** per avviare l'app.</span><span class="sxs-lookup"><span data-stu-id="78f71-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="78f71-141">Se non vedi l'icona **Business Central**, seleziona **... (Estensioni messaggi)**.</span><span class="sxs-lookup"><span data-stu-id="78f71-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Apri l'app Business Central per cercare i contatti dalla casella del messaggio](media/teams-contacts-message-box.png)

2. <span data-ttu-id="78f71-143">Nella casella **Business Central**, inizia a digitare il testo di ricerca, come un nome, un indirizzo o un numero di telefono.</span><span class="sxs-lookup"><span data-stu-id="78f71-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="78f71-144">Durante la digitazione, verranno visualizzati i risultati corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="78f71-144">As you type, matching results will appear.</span></span>

    ![Cerca i contatti Business Central dalla casella del messaggio](media/teams-contacts-5.png)
3. <span data-ttu-id="78f71-146">Seleziona un contatto dai risultati.</span><span class="sxs-lookup"><span data-stu-id="78f71-146">Select a contact from the results.</span></span>

    <span data-ttu-id="78f71-147">La scheda del contatto viene visualizzata nella casella di composizione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="78f71-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="78f71-148">La scheda del contatto non viene inviata immediatamente alla conversazione in modo che gli altri possano vederla.</span><span class="sxs-lookup"><span data-stu-id="78f71-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="78f71-149">Hai la possibilità di rivedere il contenuto della scheda e aggiungere del testo prima o dopo di essa come preferisci.</span><span class="sxs-lookup"><span data-stu-id="78f71-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="78f71-150">Quindi, invia il tuo messaggio alla chat quando sei pronto.</span><span class="sxs-lookup"><span data-stu-id="78f71-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="78f71-151">Ecco un altro modo</span><span class="sxs-lookup"><span data-stu-id="78f71-151">Here's another way</span></span>

1. <span data-ttu-id="78f71-152">Invece di usare l'icona **Business Central**, digita **@ Business Central** direttamente nella casella di composizione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="78f71-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="78f71-153">Immetti i termini di ricerca nella casella.</span><span class="sxs-lookup"><span data-stu-id="78f71-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="78f71-154">Utilizza i tasti freccia su e giù sulla tastiera per scegliere un contatto, quindi premi Invio per selezionarlo.</span><span class="sxs-lookup"><span data-stu-id="78f71-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="78f71-155">Visualizzazione dei dettagli della scheda del contatto</span><span class="sxs-lookup"><span data-stu-id="78f71-155">Viewing contact card details</span></span>

<span data-ttu-id="78f71-156">La scheda del contatto in Teams offre una rapida panoramica del cliente, fornitore o del contatto.</span><span class="sxs-lookup"><span data-stu-id="78f71-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="78f71-157">La scheda è interattiva&mdash;ciò significa che puoi visualizzare più informazioni o persino modificare un contatto utilizzando i pulsanti **Dettagli** o **Apri nuova finestra**.</span><span class="sxs-lookup"><span data-stu-id="78f71-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="78f71-158">Il pulsante **Dettagli** apre una finestra all'interno di Teams che mostra più informazioni sul contatto, ma non tutte quelle che vedresti in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="78f71-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="78f71-159">Per visualizzare tutte le informazioni su un contatto in [!INCLUDE [prod_short](includes/prod_short.md)], seleziona **Apri nuova finestra**.</span><span class="sxs-lookup"><span data-stu-id="78f71-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="78f71-160">La scheda del contatto funziona come le schede per i record, come articoli, clienti o ordini di vendita.</span><span class="sxs-lookup"><span data-stu-id="78f71-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="78f71-161">Per ulteriori informazioni sulle carte, vedi [Visualizza i dettagli della scheda](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="78f71-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="78f71-162">Tutti i partecipanti a una conversazione di Teams saranno in grado di visualizzare il contatto Business Central inviato alla conversazione.</span><span class="sxs-lookup"><span data-stu-id="78f71-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="78f71-163">Tuttavia per visualizzare maggiori dettagli sui record, utilizzando i pulsanti **Dettagli** o **Apri nuova finestra** in una scheda, sarà necessario accedere a [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="78f71-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="78f71-164">Per ulteriori informazioni, vedere [Gestione dell'integrazione di Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="78f71-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="78f71-165">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="78f71-165">See Also</span></span>

[<span data-ttu-id="78f71-166">Panoramica dell'integrazione di Business Central e Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="78f71-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="78f71-167">[Installare l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="78f71-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="78f71-168">Domande frequenti su Teams</span><span class="sxs-lookup"><span data-stu-id="78f71-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="78f71-169">Risoluzione dei problemi relativi a Teams</span><span class="sxs-lookup"><span data-stu-id="78f71-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="78f71-170">Sviluppo per l'integrazione di Teams</span><span class="sxs-lookup"><span data-stu-id="78f71-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]