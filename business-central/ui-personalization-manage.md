---
title: Gestione della personalizzazione come amministratore in Business Central | Documenti Microsoft
description: Informazioni su come personalizzare l'interfaccia utente in base alle esigenze professionali.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250597"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="33351-103">Gestione della personalizzazione come amministratore</span><span class="sxs-lookup"><span data-stu-id="33351-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="33351-104"> Gli utenti possono personalizzare l'area di lavoro per adattarla alle proprie preferenze.</span><span class="sxs-lookup"><span data-stu-id="33351-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="33351-105">In veste di amministratore, si controlla e si gestisce la personalizzazione:</span><span class="sxs-lookup"><span data-stu-id="33351-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="33351-106">Abilitando o disabilitando la funzionalità di personalizzazione per l'intera applicazione (solo installazione locale).</span><span class="sxs-lookup"><span data-stu-id="33351-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="33351-107">Abilitando o disabilitando la funzionalità di personalizzazione per gli utenti di un profilo specifico.</span><span class="sxs-lookup"><span data-stu-id="33351-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="33351-108">Annullando qualsiasi personalizzazione di pagina che gli utenti hanno effettuato.</span><span class="sxs-lookup"><span data-stu-id="33351-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="33351-109">Per abilitare o disabilitare la personalizzazione (solo locale)</span><span class="sxs-lookup"><span data-stu-id="33351-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="33351-110">Per impostazione predefinita, la personalizzazione non è abilitata nel client.</span><span class="sxs-lookup"><span data-stu-id="33351-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="33351-111">La personalizzazione viene abilitata o disabilitata modificando il file di configurazione (navsettings.json) dell'istanza del server Web Business Central che serve i client.</span><span class="sxs-lookup"><span data-stu-id="33351-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="33351-112">Per abilitare la personalizzazione, aggiungere la seguente riga nel file navsettings.json:</span><span class="sxs-lookup"><span data-stu-id="33351-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="33351-113">Per disabilitare la personalizzazione, rimuovere questa riga o modificarla in:</span><span class="sxs-lookup"><span data-stu-id="33351-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="33351-114">Per ulteriori informazioni su come modificare il file navsettings.json, vedere [Modificare direttamente il file navsettings.json](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span><span class="sxs-lookup"><span data-stu-id="33351-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="33351-115">Generare e scaricare i simboli dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="33351-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="33351-116">Questo passaggio è facoltativo e non necessario per abilitare la personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="33351-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="33351-117">Tuttavia, garantisce la possibilità di personalizzare le nuove pagine create dagli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="33351-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="33351-118">Innanzitutto, generare i simboli eseguendo finsql.exe con il comando `generatesymbolreference`.</span><span class="sxs-lookup"><span data-stu-id="33351-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="33351-119">Il file finsql.exe si trova nella cartella di installazione per [!INCLUDE[server](includes/server.md)] e Dynamics NAV Development Environment (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="33351-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="33351-120">Per generare i simboli, aprire un prompt dei comandi, accedere ala directory in cui si trova il file ed eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="33351-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="33351-121">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="33351-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="33351-122">Per ulteriori informazioni, vedere [Eseguire C/SIDE e AL contemporaneamente](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="33351-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="33351-123">Configurare l'istanza di [!INCLUDE[nav_server_md](includes/nav_server_md.md)] per **Abilitare il collegamento dei riferimenti dei simboli dell'applicazione all'avvio del server** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="33351-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="33351-124">Per ulteriori informazioni, vedere [Configurazione di Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="33351-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="33351-125">Per disabilitare la personalizzazione per un profilo</span><span class="sxs-lookup"><span data-stu-id="33351-125">To disable personalization for a profile</span></span>

<span data-ttu-id="33351-126">È possibile impedire a tutti gli utenti che appartengono a un profilo specifico di personalizzare le proprie pagine.</span><span class="sxs-lookup"><span data-stu-id="33351-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="33351-127">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Profili** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="33351-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="33351-128">Selezionare dall'elenco il profilo che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="33351-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="33351-129">Selezionare la casella di controllo **Disabilita personalizzazione** e quindi fare clic sul pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="33351-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="33351-130">Per eliminare personalizzazioni dell'utente</span><span class="sxs-lookup"><span data-stu-id="33351-130">To clear user personalizations</span></span>

<span data-ttu-id="33351-131">La cancellazione delle modifiche di personalizzazione della pagina ripristina la pagina al layout originale prima che fosse apportata qualsiasi personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="33351-131">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="33351-132">Ci sono due modi per eliminare le personalizzazioni che gli utenti hanno apportato alle pagine: utilizzando la pagina **Elimina personalizzazione utente** o la pagina **Scheda personalizzazione utente**.</span><span class="sxs-lookup"><span data-stu-id="33351-132">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="33351-133">Per eliminare le personalizzazioni dell'utente tramite la pagina Elimina personalizzazione utente</span><span class="sxs-lookup"><span data-stu-id="33351-133">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="33351-134">La pagina **Elimina personalizzazione utente** consente di eliminare la personalizzazione in base alla pagina e all'utente.</span><span class="sxs-lookup"><span data-stu-id="33351-134">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="33351-135">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina personalizzazione utente** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="33351-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="33351-136">Nella pagina vengono elencate tutte le pagine che sono state personalizzate e l'utente a cui appartengono.</span><span class="sxs-lookup"><span data-stu-id="33351-136">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="33351-137">Un segno di spunta nelle colonne **Personalizzazione legacy** indica che la personalizzazione è stata effettuata in una versione precedente di [!INCLUDE[d365fin](includes/d365fin_md.md)] che gestiva la personalizzazione in modo diverso rispetto ad adesso.</span><span class="sxs-lookup"><span data-stu-id="33351-137">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="33351-138">Gli utenti che provano a personalizzare queste pagine vengono bloccati a meno che non scelgano di sbloccare la pagina.</span><span class="sxs-lookup"><span data-stu-id="33351-138">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="33351-139">Per ulteriori informazioni, vedere [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="33351-139">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="33351-140">Selezionare la voce che si desidera eliminare, quindi scegliere l'azione **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="33351-140">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="33351-141">L'utente visualizzerà le modifiche dopo l'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="33351-141">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="33351-142">Per eliminare le personalizzazioni dell'utente tramite la pagina Scheda personalizzazione utente</span><span class="sxs-lookup"><span data-stu-id="33351-142">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="33351-143">La pagina **Scheda personalizzazione utente** consente di eliminare la personalizzazione in tutte le pagine per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="33351-143">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="33351-144">Questa operazione richiede l'autorizzazione di scrittura per la tabella **Profilo** 2000000072.</span><span class="sxs-lookup"><span data-stu-id="33351-144">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="33351-145">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Personalizzazione utente** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="33351-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="33351-146">Nella pagina **Personalizzazione utente** vengono elencati tutti gli utenti che potenzialmente dispongono di pagine personalizzate.</span><span class="sxs-lookup"><span data-stu-id="33351-146">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="33351-147">Se non è presente un utente nell'elenco, significa che non dispone di pagine personalizzate.</span><span class="sxs-lookup"><span data-stu-id="33351-147">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="33351-148">Selezionare l'utente dalla lista, quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="33351-148">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="33351-149">Nella scheda **Azioni**, scegliere **Cancella pagine personalizzate**.</span><span class="sxs-lookup"><span data-stu-id="33351-149">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="33351-150">L'utente visualizzerà le modifiche dopo l'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="33351-150">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="33351-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33351-151">See Also</span></span>
[<span data-ttu-id="33351-152">Personalizzazione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="33351-152">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="33351-153">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="33351-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="33351-154">Modifica delle impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="33351-154">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="33351-155">Modifica delle funzionalità visualizzate</span><span class="sxs-lookup"><span data-stu-id="33351-155">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
