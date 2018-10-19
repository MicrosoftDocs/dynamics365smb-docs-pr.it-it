---
title: Gestione della personalizzazione come amministratore in Business Central | Documenti Microsoft
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
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 78eea4df6f25772063cef5770eb1dcb433bee012
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="3fab3-103">Gestione della personalizzazione come amministratore</span><span class="sxs-lookup"><span data-stu-id="3fab3-103">Managing Personalization as an Administrator</span></span>
<span data-ttu-id="3fab3-104"><!--NAV in the Web client--> Gli utenti possono personalizzare l'area di lavoro per adattarla alle proprie preferenze.</span><span class="sxs-lookup"><span data-stu-id="3fab3-104"><!--NAV in the Web client--> Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="3fab3-105">In qualità di amministratore, è possibile controllare e gestire la personalizzazione disabilitando la possibilità per gli utenti di personalizzare le pagine e cancellando le personalizzazioni di pagina che gli utenti hanno effettuato.</span><span class="sxs-lookup"><span data-stu-id="3fab3-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="3fab3-106">Disabilitare la personalizzazione per un profilo</span><span class="sxs-lookup"><span data-stu-id="3fab3-106">Disable personalization for a profile</span></span>
<span data-ttu-id="3fab3-107">È possibile impedire a tutti gli utenti che appartengono a un profilo specifico di personalizzare le proprie pagine.</span><span class="sxs-lookup"><span data-stu-id="3fab3-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="3fab3-108">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Profili** e scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="3fab3-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="3fab3-109">Selezionare dall'elenco il profilo che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="3fab3-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="3fab3-110">Selezionare la casella di controllo **Disabilita personalizzazione** e quindi fare clic sul pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fab3-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="3fab3-111">Cancellare le personalizzazioni dell'utente</span><span class="sxs-lookup"><span data-stu-id="3fab3-111">Clear user personalizations</span></span>

<span data-ttu-id="3fab3-112">La cancellazione delle modifiche di personalizzazione della pagina ripristina la pagina al layout originale prima che fosse apportata qualsiasi personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="3fab3-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="3fab3-113">Ci sono due modi per eliminare le personalizzazioni che gli utenti hanno apportato alle pagine: utilizzando la finestra **Elimina personalizzazione utente** o la finestra **Scheda personalizzazione utente**.</span><span class="sxs-lookup"><span data-stu-id="3fab3-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** window and using the **User Personalization Card** window.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="3fab3-114">Eliminare le personalizzazioni dell'utente tramite la pagina Elimina personalizzazione utente</span><span class="sxs-lookup"><span data-stu-id="3fab3-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="3fab3-115">La finestra **Elimina personalizzazione utente** consente di eliminare la personalizzazione in base alla pagina e all'utente.</span><span class="sxs-lookup"><span data-stu-id="3fab3-115">The **Delete User Personalization** window enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="3fab3-116">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina personalizzazione utente** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="3fab3-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="3fab3-117">Nella pagina vengono elencate tutte le pagine che sono state personalizzate e l'utente a cui appartengono.</span><span class="sxs-lookup"><span data-stu-id="3fab3-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="3fab3-118">Un segno di spunta nelle colonne **Personalizzazione legacy** indica che la personalizzazione è stata effettuata in una versione precedente di [!INCLUDE[d365fin](includes/d365fin_md.md)] che gestiva la personalizzazione in modo diverso rispetto ad adesso.</span><span class="sxs-lookup"><span data-stu-id="3fab3-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="3fab3-119">Gli utenti che provano a personalizzare queste pagine vengono bloccati a meno che non scelgano di sbloccare la pagina.</span><span class="sxs-lookup"><span data-stu-id="3fab3-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="3fab3-120">Per ulteriori informazioni, vedere [Perché la personalizzazione di una pagina è bloccata](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="3fab3-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="3fab3-121">Selezionare la voce che si desidera eliminare, quindi scegliere l'azione **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="3fab3-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="3fab3-122">L'utente visualizzerà le modifiche dopo l'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="3fab3-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="3fab3-123">Eliminare le personalizzazioni dell'utente tramite la pagina Scheda personalizzazione utente</span><span class="sxs-lookup"><span data-stu-id="3fab3-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="3fab3-124">La finestra **Scheda personalizzazione utente** consente di eliminare la personalizzazione in tutte le pagine per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="3fab3-124">The **User Personalization Card** window enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="3fab3-125">Questa operazione richiede l'autorizzazione di scrittura per la tabella **Profilo** 2000000072.</span><span class="sxs-lookup"><span data-stu-id="3fab3-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="3fab3-126">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Personalizzazione utente** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="3fab3-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="3fab3-127">Nella finestra **Personalizzazione utente** vengono elencati tutti gli utenti che potenzialmente dispongono di pagine personalizzate.</span><span class="sxs-lookup"><span data-stu-id="3fab3-127">The **User Personalization** window lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="3fab3-128">Se non è presente un utente nell'elenco, significa che non dispone di pagine personalizzate.</span><span class="sxs-lookup"><span data-stu-id="3fab3-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="3fab3-129">Selezionare l'utente dalla lista, quindi scegliere l'azione **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="3fab3-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="3fab3-130">Nella scheda **Azioni**, scegliere **Cancella pagine personalizzate**.</span><span class="sxs-lookup"><span data-stu-id="3fab3-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="3fab3-131">L'utente visualizzerà le modifiche dopo l'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="3fab3-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fab3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fab3-132">See Also</span></span>
[<span data-ttu-id="3fab3-133">Personalizzazione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="3fab3-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="3fab3-134">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3fab3-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="3fab3-135">Modifica delle impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="3fab3-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="3fab3-136">Modifica delle funzionalità visualizzate</span><span class="sxs-lookup"><span data-stu-id="3fab3-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

