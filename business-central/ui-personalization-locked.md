---
title: Perché non è possibile personalizzare una pagina | Documenti Microsoft
description: Descrizione dei motivi per cui non è possibile personalizzare una pagina e delle azioni che è possibile intraprendere per sbloccare la pagina e personalizzarla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 41b0989d388ee7ded2619136ded0a03d5830b78b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387552"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="31d9c-103">Perché non è possibile personalizzare una pagina</span><span class="sxs-lookup"><span data-stu-id="31d9c-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="31d9c-104">Vi sono due condizioni che impediscono la personalizzazione di una pagina.</span><span class="sxs-lookup"><span data-stu-id="31d9c-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="31d9c-105">La pagina è protetta (come indicato dall'icona ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione")) oppure è bloccata (come indicato dall'icona ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata")).</span><span class="sxs-lookup"><span data-stu-id="31d9c-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="31d9c-106">Protetta dalla personalizzazione</span><span class="sxs-lookup"><span data-stu-id="31d9c-106">Locked from Personalizing</span></span>

<span data-ttu-id="31d9c-107">Se è presente un'icona ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") nel banner **Personalizzazione** quando viene aperta una pagina (come mostrato), ciò indica che attualmente non sono consentite ulteriori modifiche di personalizzazione nella pagina.</span><span class="sxs-lookup"><span data-stu-id="31d9c-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="31d9c-108">Ciò può avvenire per due motivi:</span><span class="sxs-lookup"><span data-stu-id="31d9c-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="31d9c-109">La pagina è stata personalizzata in precedenza, ma utilizzando una versione antecedente del prodotto.</span><span class="sxs-lookup"><span data-stu-id="31d9c-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="31d9c-110">Il modo in cui la personalizzazione funziona in background è stato modificato dall'ultima volta che è stata personalizzata la pagina.</span><span class="sxs-lookup"><span data-stu-id="31d9c-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="31d9c-111">Purtroppo, il vecchio e il nuovo modo non funzionano insieme.</span><span class="sxs-lookup"><span data-stu-id="31d9c-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="31d9c-112">Finora, è stato utilizzato solo [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] per personalizzare la pagina.</span><span class="sxs-lookup"><span data-stu-id="31d9c-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="31d9c-113">Sblocco della pagina</span><span class="sxs-lookup"><span data-stu-id="31d9c-113">Unlocking the Page</span></span>

<span data-ttu-id="31d9c-114">Se si desidera sbloccare una pagina e continuare a personalizzarla, scegliere l'icona ![Blocco della personalizzazione](media/personalization-lock-icon.png "Blocco della personalizzazione") e quindi scegliere **Sblocca**.</span><span class="sxs-lookup"><span data-stu-id="31d9c-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="31d9c-115">Prima di sbloccare la pagina, considerare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="31d9c-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="31d9c-116">La personalizzazione corrente della pagina verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="31d9c-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="31d9c-117">Per la pagina verrà utilizzato il layout originale e sarà necessario cominciare da zero.</span><span class="sxs-lookup"><span data-stu-id="31d9c-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="31d9c-118">In [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la pagina rimarrà così com'è e non verrà alterata dalle modifiche della nuova personalizzazione effettuate nel client Business Central.</span><span class="sxs-lookup"><span data-stu-id="31d9c-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="31d9c-119">In seguito, la personalizzazione in [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] e quella nel client Business Central verranno completate indipendentemente l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="31d9c-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="31d9c-120">Bloccata per la personalizzazione</span><span class="sxs-lookup"><span data-stu-id="31d9c-120">Blocked from Personalizing</span></span>

<span data-ttu-id="31d9c-121">Se esiste un'icona ![Personalizzazione bloccata](media/personalization-blocked-icon.png "Personalizzazione bloccata") nel banner **Personalizzazione**, ciò significa che qualsiasi personalizzazione della pagina è bloccata.</span><span class="sxs-lookup"><span data-stu-id="31d9c-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="31d9c-122">Ciò è dovuto al fatto che Gestione ruolo utente o il ruolo attualmente associato al proprio account utente modifica questa pagina specificatamente per il ruolo.</span><span class="sxs-lookup"><span data-stu-id="31d9c-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="31d9c-123">Contattare l'amministratore per l'assistenza.</span><span class="sxs-lookup"><span data-stu-id="31d9c-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="31d9c-124">In alternativa, provare a passare a un Centro ruoli che include l'adattamento dei ruoli per questa pagina.</span><span class="sxs-lookup"><span data-stu-id="31d9c-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="31d9c-125">Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="31d9c-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="31d9c-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="31d9c-126">See Also</span></span>
[<span data-ttu-id="31d9c-127">Personalizzare l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="31d9c-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="31d9c-128">Personalizzare pagine per profili</span><span class="sxs-lookup"><span data-stu-id="31d9c-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="31d9c-129">Modificare le impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="31d9c-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="31d9c-130">Modifica delle funzionalità visualizzate</span><span class="sxs-lookup"><span data-stu-id="31d9c-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]