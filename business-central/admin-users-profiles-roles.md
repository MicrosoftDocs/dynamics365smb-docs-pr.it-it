---
title: Gestire utenti e ruoli | Microsoft Docs
description: Informazioni su come gestire utenti e Gestioni ruolo utente in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801946"
---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="ce2d3-103">Informazioni su utenti, profili e Gestioni ruolo utente</span><span class="sxs-lookup"><span data-stu-id="ce2d3-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="ce2d3-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], gli utenti vengono aggiunti da un amministratore che concede anche l'accesso per gli utenti alle aree di [!INCLUDE[d365fin](includes/d365fin_md.md)] necessarie per il loro lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="ce2d3-105">L'accesso alle funzionalità è gestito tramite *gruppi utente* e *profili*.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="ce2d3-106">In qualità di amministratore, è possibile rimuovere utenti nell'ambito della sottoscrizione di [!INCLUDE[d365fin](includes/d365fin_md.md)] e assegnare le autorizzazioni utente nei gruppi utente.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="ce2d3-107">Aggiunta di utenti</span><span class="sxs-lookup"><span data-stu-id="ce2d3-107">Adding Users</span></span>

<span data-ttu-id="ce2d3-108">Per aggiungere utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'amministratore di Office 365 della società deve innanzitutto creare gli utenti tramite l'interfaccia di amministrazione di Office 365.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="ce2d3-109">Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="ce2d3-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="ce2d3-110">Quindi, l'amministratore può assegnare le autorizzazioni a ciascun utente e ai gruppi utente.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="ce2d3-111">Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ce2d3-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="ce2d3-112">Le autorizzazioni più efficaci che un utente può avere è il set di autorizzazioni SUPER.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="ce2d3-113">Ogni società deve avere almeno un utente con tale set di autorizzazioni, ma la procedura ottimale consiste nell'assegnare a ogni utente soltanto le autorizzazioni necessarie alle loro esigenze lavorative in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ce2d3-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="ce2d3-114">Ad esempio, ciò consente di accertare che gli utenti hanno accesso solo ai dati pertinenti al loro lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="ce2d3-115">È una procedura ottimale assicurare che anche l'amministratore Office 365 disponga del set di autorizzazioni SUPER in [!INCLUDE[prodshort](includes/prodshort.md)] in quanto ciò semplifica molte attività amministrative, inclusa la configurazione dell'integrazione con altre app.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="ce2d3-116">Utenti di distribuzioni locali</span><span class="sxs-lookup"><span data-stu-id="ce2d3-116">Users of on-premises deployments</span></span>

<span data-ttu-id="ce2d3-117">Per le distribuzioni locali di [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore può scegliere tra diversi meccanismi di autorizzazione delle credenziali per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="ce2d3-118">Pertanto, quando si crea un utente, fornire informazioni diverse a seconda del tipo di credenziali che si stanno utilizzando nell'istanza specifica di [!INCLUDE[server](includes/server.md)].</span><span class="sxs-lookup"><span data-stu-id="ce2d3-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="ce2d3-119">Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella sezione Amministrazione del contenuto per sviluppatori e professionisti IT per [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce2d3-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="ce2d3-120">Profili</span><span class="sxs-lookup"><span data-stu-id="ce2d3-120">Profiles</span></span>

<span data-ttu-id="ce2d3-121">A tutte le persone nella società che hanno accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] viene assegnato un *profilo* che consente l'utilizzo di una *Gestione ruolo utente*.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="ce2d3-122">I profili sono raccolte di utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] che condividono la stessa Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="ce2d3-123">Gestione ruolo utente è il punto di ingresso e la home page per [!INCLUDE[d365fin](includes/d365fin_md.md)] che offre rapido accesso alle attività più importanti e visualizza diverse informazioni approfondite e indicatori di prestazioni chiave (KPI) sul proprio lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ce2d3-124">Nella versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)] online, non è possibile aggiungere, modificare o eliminare profili.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="ce2d3-125">Creare un profilo</span><span class="sxs-lookup"><span data-stu-id="ce2d3-125">Create a profile</span></span>

1.  <span data-ttu-id="ce2d3-126">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Lista profili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profile List**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="ce2d3-127">Nella pagina **Lista profili**, scegliere l'azione **Nuovo** per aprire la pagina **Scheda Nuovo profilo**.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-127">On the **Profile List** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="ce2d3-128">Nel campo **ID profilo** immettere un nome che descriva il ruolo previsto degli utenti.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="ce2d3-129">Nel campo **Descrizione** immettere una descrizione dell'ID profilo, ad esempio **Gestore ordini**.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="ce2d3-130">Impostare il campo **ID Gestione ruolo utente** nella Gestione ruolo utente che si intende assegnare al profilo.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="ce2d3-131">La procedura per modificare un profilo esistente è identica, tranne che si seleziona un profilo esistente nella pagina **Lista profili** invece di scegliere l'azione **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profile List** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="ce2d3-132">Copia di un profilo</span><span class="sxs-lookup"><span data-stu-id="ce2d3-132">Copy a profile</span></span>
<span data-ttu-id="ce2d3-133">La copia di un profilo consente di risparmiare tempo se si desidera utilizzare impostazioni simili in un profilo e si desidera soltanto modificare poche impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="ce2d3-134">Aprire il profilo che si desidera copiare, quindi scegliere l'azione **Copia profilo**.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="ce2d3-135">Nel campo **Nuovo ID profilo** immettere un nome per il profilo che si desidera copiare.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="ce2d3-136">Impostare il campo **Nuovo ambito profilo** su una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="ce2d3-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="ce2d3-137">**Sistema** per rendere il nuovo profilo disponibile a tutti i database del tenant che utilizzano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="ce2d3-138">**Tenant** per rendere il nuovo profilo disponibile solo al database del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="ce2d3-139">Al termine, scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="ce2d3-140">Importazione ed esportazione di profili</span><span class="sxs-lookup"><span data-stu-id="ce2d3-140">Export and import profiles</span></span>

<span data-ttu-id="ce2d3-141">È possibile esportare e importare i profili come file XML a e da un database [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce2d3-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="ce2d3-142">L'esportazione e l'importazione di un profilo consentono di risparmiare tempo quando si configura l'interfaccia utente perché si riutilizza una configurazione di profilo esistente anziché dover configurare un profilo da zero.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="ce2d3-143">Se si dispone di un profilo configurato in un database [!INCLUDE[d365fin](includes/d365fin_md.md)] e si desidera riutilizzare tutte o alcune delle stesse configurazioni del profilo in un database diverso, è possibile esportare il profilo in un file XML.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="ce2d3-144">Quindi, è possibile importare il file XML del profilo nel secondo database.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="ce2d3-145">Per esportare un profilo, è possibile scegliere l'azione **Esporta profili** nella pagina **Lista profili** o **Scheda profilo** oppure cercare e aprire la pagina **Esporta profili**.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="ce2d3-146">Salvare il file XML in un'ubicazione sul computer o sulla rete.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="ce2d3-147">Per importare un profilo, è possibile scegliere l'azione **Importa profilo** nella pagina **Lista profili** oppure cercare e aprire la pagina **Importa profili**.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span> 

    > [!NOTE]  
    >  <span data-ttu-id="ce2d3-148">Non è possibile importare un profilo già esistente nel database, anche se il file XML è denominato in modo diverso o ha un contenuto diverso.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="ce2d3-149">È necessario eliminare il profilo esistente prima di importare quello nuovo.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="ce2d3-150">Configurazione e personalizzazione</span><span class="sxs-lookup"><span data-stu-id="ce2d3-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="ce2d3-151">Gli utenti possono personalizzare l'interfaccia utente della versione personale personalizzando l'interfaccia utente con le proprie credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="ce2d3-152">Questa personalizzazione può essere eliminata dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="ce2d3-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="ce2d3-153">Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="ce2d3-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce2d3-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce2d3-154">See Also</span></span>  
[<span data-ttu-id="ce2d3-155">Gestione di utenti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="ce2d3-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="ce2d3-156">Gestione della personalizzazione come amministratore</span><span class="sxs-lookup"><span data-stu-id="ce2d3-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="ce2d3-157">Personalizzazione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ce2d3-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
