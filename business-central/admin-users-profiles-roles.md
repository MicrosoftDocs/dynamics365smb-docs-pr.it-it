---
title: Gestire utenti e ruoli | Microsoft Docs
description: Informazioni su come gestire utenti e Gestioni ruolo utente in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="c859b-103">Informazioni su utenti, profili e Gestioni ruolo utente</span><span class="sxs-lookup"><span data-stu-id="c859b-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="c859b-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], gli utenti vengono aggiunti da un amministratore che concede anche l'accesso per gli utenti alle aree di [!INCLUDE[d365fin](includes/d365fin_md.md)] necessarie per il loro lavoro.</span><span class="sxs-lookup"><span data-stu-id="c859b-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="c859b-105">L'accesso alle funzionalità è gestito tramite *gruppi utente* e *profili*.</span><span class="sxs-lookup"><span data-stu-id="c859b-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="c859b-106">In qualità di amministratore, è possibile rimuovere utenti nell'ambito della sottoscrizione di [!INCLUDE[d365fin](includes/d365fin_md.md)] e assegnare le autorizzazioni utente nei gruppi utente.</span><span class="sxs-lookup"><span data-stu-id="c859b-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="c859b-107">Aggiunta di utenti</span><span class="sxs-lookup"><span data-stu-id="c859b-107">Adding Users</span></span>

<span data-ttu-id="c859b-108">Per aggiungere utenti in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'amministratore di Office 365 della società deve innanzitutto creare gli utenti tramite l'interfaccia di amministrazione di Office 365.</span><span class="sxs-lookup"><span data-stu-id="c859b-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="c859b-109">Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="c859b-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="c859b-110">Quindi, l'amministratore può assegnare le autorizzazioni a ciascun utente e ai gruppi utente.</span><span class="sxs-lookup"><span data-stu-id="c859b-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="c859b-111">Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="c859b-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="c859b-112">Utenti di distribuzioni locali</span><span class="sxs-lookup"><span data-stu-id="c859b-112">Users of on-premises deployments</span></span>

<span data-ttu-id="c859b-113">Per le distribuzioni locali di [!INCLUDE[d365fin](includes/d365fin_md.md)], l'amministratore può scegliere tra diversi meccanismi di autorizzazione delle credenziali per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c859b-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="c859b-114">Pertanto, quando si crea un utente, fornire informazioni diverse a seconda del tipo di credenziali che si stanno utilizzando nell'istanza specifica di [!INCLUDE[server](includes/server.md)].</span><span class="sxs-lookup"><span data-stu-id="c859b-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="c859b-115">Per ulteriori informazioni, vedere [Tipi di autenticazione e credenziali](/dynamics365/business-central/dev-itpro/administration/users-credential-types) nella sezione Amministrazione del contenuto per sviluppatori e professionisti IT per [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c859b-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="c859b-116">Profili</span><span class="sxs-lookup"><span data-stu-id="c859b-116">Profiles</span></span>

<span data-ttu-id="c859b-117">A tutte le persone nella società che hanno accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] viene assegnato un *profilo* che consente l'utilizzo di una *Gestione ruolo utente*.</span><span class="sxs-lookup"><span data-stu-id="c859b-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="c859b-118">I profili sono raccolte di utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] che condividono la stessa Gestione ruolo utente.</span><span class="sxs-lookup"><span data-stu-id="c859b-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="c859b-119">Gestione ruolo utente è il punto di ingresso e la home page per [!INCLUDE[d365fin](includes/d365fin_md.md)] che offre rapido accesso alle attività più importanti e visualizza diverse informazioni approfondite e indicatori di prestazioni chiave (KPI) sul proprio lavoro.</span><span class="sxs-lookup"><span data-stu-id="c859b-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c859b-120">Nella versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)] online, non è possibile aggiungere, modificare o eliminare profili.</span><span class="sxs-lookup"><span data-stu-id="c859b-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="c859b-121">Configurazione e personalizzazione</span><span class="sxs-lookup"><span data-stu-id="c859b-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="c859b-122">Gli utenti possono personalizzare l'interfaccia utente della versione personale personalizzando l'interfaccia utente con le proprie credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="c859b-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="c859b-123">Questa personalizzazione può essere eliminata dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="c859b-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="c859b-124">Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="c859b-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="c859b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c859b-125">See Also</span></span>  
[<span data-ttu-id="c859b-126">Gestione di utenti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="c859b-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="c859b-127">Gestione della personalizzazione come amministratore</span><span class="sxs-lookup"><span data-stu-id="c859b-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="c859b-128">Personalizzazione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c859b-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

