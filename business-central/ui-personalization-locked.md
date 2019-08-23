---
title: Perché non è possibile personalizzare una pagina | Documenti Microsoft
description: Descrizione dei motivi per cui non è possibile personalizzare una pagina e delle azioni che è possibile intraprendere per sbloccare la pagina e personalizzarla.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796764"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="1ddaa-103">Perché non è possibile personalizzare una pagina</span><span class="sxs-lookup"><span data-stu-id="1ddaa-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="1ddaa-104">Vi sono due condizioni che impediscono la personalizzazione di una pagina.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="1ddaa-105">La pagina è protetta (come indicato da ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione")) oppure è bloccata (come indicato da ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata"))</span><span class="sxs-lookup"><span data-stu-id="1ddaa-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="1ddaa-106">Protetta dalla personalizzazione</span><span class="sxs-lookup"><span data-stu-id="1ddaa-106">Locked from Personalizing</span></span>

<span data-ttu-id="1ddaa-107">Se è presente un'icona ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") nel banner **Personalizzazione** quando viene aperta una pagina (come mostrato), ciò indica che attualmente non sono consentite ulteriori modifiche di personalizzazione nella pagina.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="1ddaa-108">![Blocco della personalizzazione](media/personalization-locked.png "Blocco della personalizzazione")</span><span class="sxs-lookup"><span data-stu-id="1ddaa-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="1ddaa-109">Ciò può avvenire per due motivi:</span><span class="sxs-lookup"><span data-stu-id="1ddaa-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="1ddaa-110">La pagina è stata personalizzata in precedenza, ma utilizzando una versione antecedente del prodotto.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="1ddaa-111">Il modo in cui la personalizzazione funziona in background è stato modificato dall'ultima volta che è stata personalizzata la pagina.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="1ddaa-112">Purtroppo, il vecchio e il nuovo modo non funzionano insieme.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="1ddaa-113">Finora, è stato utilizzato solo [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] per personalizzare la pagina.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="1ddaa-114">Sblocco della pagina</span><span class="sxs-lookup"><span data-stu-id="1ddaa-114">Unlocking the Page</span></span>

<span data-ttu-id="1ddaa-115">Se si desidera sbloccare una pagina e continuare a personalizzarla, scegliere ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") e quindi **Sblocca**.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="1ddaa-116">Prima di sbloccare la pagina, considerare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1ddaa-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="1ddaa-117">La personalizzazione corrente della pagina verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="1ddaa-118">Per la pagina verrà utilizzato il layout originale e sarà necessario cominciare da zero.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="1ddaa-119">In [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la pagina rimarrà così com'è e non verrà alterata dalle modifiche della nuova personalizzazione effettuate nel client Business Central.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="1ddaa-120">In seguito, la personalizzazione in [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] e quella nel client Business Central verranno completate indipendentemente l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="1ddaa-121">Bloccata per la personalizzazione</span><span class="sxs-lookup"><span data-stu-id="1ddaa-121">Blocked from Personalizing</span></span>

<span data-ttu-id="1ddaa-122">Se esiste un'icona ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata") nel banner Personalizzazione, ciò significa che qualsiasi personalizzazione della pagina è bloccata.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="1ddaa-123">![Blocco della personalizzazione](media/personalization-blocked.png "Blocco della personalizzazione")</span><span class="sxs-lookup"><span data-stu-id="1ddaa-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="1ddaa-124">Ciò è dovuto al fatto che Gestione ruolo utente o il ruolo attualmente associato al proprio account utente modifica questa pagina specificatamente per il ruolo.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-124">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="1ddaa-125">Contattare l'amministratore per assistenza oppure, se utile, cercare di passare a una Gestione ruolo utente (da [**Impostazioni personali**](https://businesscentral.dynamics.com?page=9176 "Passare direttamente alla pagina Impostazioni utente in Business Central")) che include l'adattamento al ruolo per questa pagina.</span><span class="sxs-lookup"><span data-stu-id="1ddaa-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ddaa-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1ddaa-126">See Also</span></span>
[<span data-ttu-id="1ddaa-127">Personalizzazione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="1ddaa-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="1ddaa-128">Gestione della personalizzazione</span><span class="sxs-lookup"><span data-stu-id="1ddaa-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="1ddaa-129">Modifica delle impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="1ddaa-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="1ddaa-130">Modifica delle funzionalità visualizzate</span><span class="sxs-lookup"><span data-stu-id="1ddaa-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
