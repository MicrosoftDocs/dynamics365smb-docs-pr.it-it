---
title: Gestione della personalizzazione come amministratore in Financials | Documenti Microsoft
description: Informazioni su come personalizzare l'interfaccia utente in base alle esigenze professionali.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 2d9b45bf21d325e60beadedfc94827d7f3fda075
ms.contentlocale: it-it
ms.lasthandoff: 04/18/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="a14d4-103">Gestione della personalizzazione come amministratore</span><span class="sxs-lookup"><span data-stu-id="a14d4-103">Managing Personalization as an Administrator</span></span>
<!--NAV in the Web client-->
<span data-ttu-id="a14d4-104">Gli utenti possono personalizzare l'area di lavoro per adattarla alle proprie preferenze.</span><span class="sxs-lookup"><span data-stu-id="a14d4-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="a14d4-105">In qualità di amministratore, è possibile controllare e gestire la personalizzazione disabilitando la possibilità per gli utenti di personalizzare le pagine e cancellando le personalizzazioni di pagina che gli utenti hanno effettuato.</span><span class="sxs-lookup"><span data-stu-id="a14d4-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="a14d4-106">Disabilitare la personalizzazione per un profilo</span><span class="sxs-lookup"><span data-stu-id="a14d4-106">Disable personalization for a profile</span></span>
<span data-ttu-id="a14d4-107">È possibile impedire a tutti gli utenti che appartengono a un profilo specifico di personalizzare le proprie pagine.</span><span class="sxs-lookup"><span data-stu-id="a14d4-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="a14d4-108">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Profili**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="a14d4-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="a14d4-109">Selezionare dall'elenco il profilo che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="a14d4-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="a14d4-110">Selezionare la casella di controllo **Disabilita personalizzazione** e quindi fare clic sul pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="a14d4-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="a14d4-111">Cancellare le personalizzazioni dell'utente</span><span class="sxs-lookup"><span data-stu-id="a14d4-111">Clear user personalizations</span></span>

<span data-ttu-id="a14d4-112">La cancellazione delle modifiche di personalizzazione della pagina ripristina la pagina al layout originale prima che fosse apportata qualsiasi personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="a14d4-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="a14d4-113">Ci sono due modi per eliminare le personalizzazioni che gli utenti hanno apportato alle pagine: utilizzando la pagina **Elimina personalizzazione utente** o la pagina **Scheda personalizzazione utente**.</span><span class="sxs-lookup"><span data-stu-id="a14d4-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="a14d4-114">Eliminare le personalizzazioni dell'utente tramite la pagina Elimina personalizzazione utente</span><span class="sxs-lookup"><span data-stu-id="a14d4-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="a14d4-115">La pagina **Elimina personalizzazione utente** consente di eliminare la personalizzazione in base alla pagina e all'utente.</span><span class="sxs-lookup"><span data-stu-id="a14d4-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="a14d4-116">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Elimina personalizzazione utente**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="a14d4-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="a14d4-117">Nella pagina vengono elencate tutte le pagine che sono state personalizzate e l'utente a cui appartengono.</span><span class="sxs-lookup"><span data-stu-id="a14d4-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="a14d4-118">Un segno di spunta nelle colonne **Personalizzazione legacy** indica che la personalizzazione è stata effettuata in una versione precedente di [!INCLUDE[d365fin](includes/d365fin_md.md)] che gestiva la personalizzazione in modo diverso rispetto ad adesso.</span><span class="sxs-lookup"><span data-stu-id="a14d4-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="a14d4-119">Gli utenti che provano a personalizzare queste pagine vengono bloccati a meno che non scelgano di sbloccare la pagina.</span><span class="sxs-lookup"><span data-stu-id="a14d4-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="a14d4-120">Per ulteriori informazioni, vedere [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="a14d4-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="a14d4-121">Selezionare la voce che si desidera eliminare, quindi scegliere l'azione **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="a14d4-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="a14d4-122">L'utente visualizzerà le modifiche dopo l'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="a14d4-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="a14d4-123">Eliminare le personalizzazioni dell'utente tramite la pagina Scheda personalizzazione utente</span><span class="sxs-lookup"><span data-stu-id="a14d4-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="a14d4-124">La pagina **Scheda personalizzazione utente** consente di eliminare la personalizzazione in tutte le pagine per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="a14d4-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="a14d4-125">Questa operazione richiede l'autorizzazione di scrittura per la tabella **Profilo** 2000000072.</span><span class="sxs-lookup"><span data-stu-id="a14d4-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="a14d4-126">Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Personalizzazione utente**, quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="a14d4-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="a14d4-127">Nella pagina **Personalizzazione utente** vengono elencati tutti gli utenti che potenzialmente dispongono di pagine personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a14d4-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="a14d4-128">Se non è presente un utente nell'elenco, significa che non dispone di pagine personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a14d4-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="a14d4-129">Selezionare l'utente dalla lista, quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="a14d4-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="a14d4-130">Nella scheda **Azioni**, scegliere **Cancella pagine personalizzate**.</span><span class="sxs-lookup"><span data-stu-id="a14d4-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="a14d4-131">L'utente visualizzerà le modifiche dopo l'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="a14d4-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="a14d4-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a14d4-132">See Also</span></span>
[<span data-ttu-id="a14d4-133">Personalizzazione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="a14d4-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="a14d4-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a14d4-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a14d4-135">Modifica delle impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="a14d4-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="a14d4-136">Modifica delle funzionalità visualizzate</span><span class="sxs-lookup"><span data-stu-id="a14d4-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

