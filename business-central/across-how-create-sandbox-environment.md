---
title: Creare un ambiente sandbox | Microsoft Docs
description: Creare un ambiente per l'esplorazione, l'apprendimento, le dimostrazioni, lo sviluppo e i test.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/10/2019
ms.author: solsen
ms.openlocfilehash: 7d189ab6fa5aff518b643c797b7600570fcad43e
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910638"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a><span data-ttu-id="06bb8-103">Creazione di un ambiente sandbox in [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="06bb8-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="06bb8-104">Con [!INCLUDE [prodshort](includes/prodshort.md)], è possibile creare facilmente un ambiente sicuro in cui testare, istruire o risolvere i problemi senza disturbare i processi di lavoro o i dati aziendali della società.</span><span class="sxs-lookup"><span data-stu-id="06bb8-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="06bb8-105">Tale ambiente non di produzione è denominato *sandbox*.</span><span class="sxs-lookup"><span data-stu-id="06bb8-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="06bb8-106">Isolato dalla produzione, un ambiente sandbox consente di esplorare, apprendere, dimostrare, sviluppare e testare in sicurezza il servizio senza il rischio di compromettere i dati e le impostazioni dell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="06bb8-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="06bb8-107">L'amministratore può creare ambienti sandbox nell'[interfaccia di amministrazione](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), ma se si desidera testare rapidamente qualcosa, è possibile creare un ambiente sandbox da [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="06bb8-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="06bb8-108">Tecnicamente, gli ambienti sandbox sono molto diversi dagli ambienti di produzione, anche se l'amministratore crea un sandbox che include dati di produzione.</span><span class="sxs-lookup"><span data-stu-id="06bb8-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="06bb8-109">Non è possibile utilizzare un sandbox per il benchmarking e, ad esempio, non è possibile richiedere un'esportazione del database.</span><span class="sxs-lookup"><span data-stu-id="06bb8-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="06bb8-110">Se si desidera creare un sandbox per il benchmarking, l'amministratore può creare un ambiente di produzione dedicato nell'interfaccia di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="06bb8-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="06bb8-111">Per ulteriori informazioni, vedere [Tipi di ambienti](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="06bb8-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a><span data-ttu-id="06bb8-112">Per creare un ambiente sandbox in [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="06bb8-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="06bb8-113">Accedere all'istanza di produzione di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="06bb8-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="06bb8-114">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ambiente sandbox** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="06bb8-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="06bb8-115">Fare clic sul pulsante **Crea**.</span><span class="sxs-lookup"><span data-stu-id="06bb8-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="06bb8-116">Viene visualizzata un'altra scheda con [!INCLUDE[d365fin](includes/d365fin_md.md)] dove è possibile completare la configurazione del proprio ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="06bb8-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="06bb8-117">Se la funzione Blocco popup del browser è abilitata, modificarne l'impostazione per consentire la visualizzazione degli URL dall'indirizzo \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="06bb8-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="06bb8-118">Quando l'ambiente sandbox è pronto, si verrà reindirizzati all'introduzione guidata dell'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="06bb8-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="06bb8-119">È possibile scegliere il pulsante **Ulteriori informazioni** per informazioni sugli scenari per sviluppatori che è possibile provare in un ambiente sandbox o scegliere il pulsante **Chiudi** per passare a Gestione ruolo utente dell'istanza sandbox di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="06bb8-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="06bb8-120">Nella parte superiore di Gestione ruolo utente viene visualizzato un avviso che informa che ci si trova in un ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="06bb8-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="06bb8-121">È possibile vedere il tipo di ambiente anche nella barra del titolo del client.</span><span class="sxs-lookup"><span data-stu-id="06bb8-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="06bb8-122">Un ambiente sandbox creato in questo modo contiene solo i dati di dimostrazione predefiniti per l'azienda CRONUS.</span><span class="sxs-lookup"><span data-stu-id="06bb8-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="06bb8-123">Nessun dato viene copiato o altrimenti trasferito dall'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="06bb8-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="06bb8-124">È inoltre possibile creare un ambiente sandbox contenente i dati di produzione.</span><span class="sxs-lookup"><span data-stu-id="06bb8-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="06bb8-125">Questa operazione deve essere eseguita mediante l'Interfaccia di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="06bb8-125">You must do this through the administration center.</span></span> <span data-ttu-id="06bb8-126">Per ulteriori informazioni, vedere [Gestione di ambienti](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in Guida per sviluppatori e professionisti IT.</span><span class="sxs-lookup"><span data-stu-id="06bb8-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="06bb8-127">È possibile tornare in qualsiasi momento nella pagina **Ambiente sandbox** e reimpostare l'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="06bb8-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="06bb8-128">La reimpostazione dell'ambiente sandbox ne determinerà la rimozione completa e la successiva creazione di un nuovo ambiente sandbox con i dati dimostrativi di default.</span><span class="sxs-lookup"><span data-stu-id="06bb8-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="06bb8-129">Un amministratore può limitare o persino bloccare l'accesso di alcuni utenti all'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="06bb8-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="06bb8-130">Questa operazione può essere effettuata utilizzando le funzionalità di sicurezza standard del prodotto, ad esempio la scheda Utente, gruppi di utenti e set di autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="06bb8-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="06bb8-131">Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="06bb8-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="06bb8-132">Funzionalità avanzata nell'ambiente sandbox</span><span class="sxs-lookup"><span data-stu-id="06bb8-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="06bb8-133">L'ambiente sandbox non è meno utile perché include un paio di funzioni utili.</span><span class="sxs-lookup"><span data-stu-id="06bb8-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="06bb8-134">Designer</span><span class="sxs-lookup"><span data-stu-id="06bb8-134">Designer</span></span>

<span data-ttu-id="06bb8-135">In un ambiente sandbox, la **funzionalità di progettazione** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="06bb8-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="06bb8-136">È possibile attivare la funzionalità di progettazione selezionando l'icona ![progettazione](./media/across-sandbox/sandbox-inclient-design-icon.png) in una pagina o selezionando **Design** nel menu ![Impostazioni](media/ui-experience/settings_icon_small.png) Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="06bb8-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="06bb8-137">Per abilitare l'esperienza utente avanzata</span><span class="sxs-lookup"><span data-stu-id="06bb8-137">To enable the advanced user experience</span></span>
<span data-ttu-id="06bb8-138">È possibile abilitare e provare la funzionalità completa della versione standard di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un tenant sandbox impostando il campo **Esperienza** nella pagina **Informazioni società**.</span><span class="sxs-lookup"><span data-stu-id="06bb8-138">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="06bb8-139">Dopo aver abilitato l'esperienza utente *Premium*, si ottiene l'accesso a tutti i profili standard (ruoli) e alla Gestione ruolo utente nella versione standard.</span><span class="sxs-lookup"><span data-stu-id="06bb8-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="06bb8-140">È inoltre possibile creare una società di valutazione completamente configurata, inclusiva dei dati di esempio e dell'accesso alle aree avanzate del prodotto.</span><span class="sxs-lookup"><span data-stu-id="06bb8-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="06bb8-141">In alternativa, contattare un partner di rivendita per una dimostrazione delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="06bb8-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="06bb8-142">Per ulteriori informazioni, vedere [Come trovare un partner di rivendita?](across-faq.md#findpartner)</span><span class="sxs-lookup"><span data-stu-id="06bb8-142">For more information, see [How do I find a reselling partner?](across-faq.md#findpartner).</span></span>  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="06bb8-143">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="06bb8-143">See Also</span></span>

<span data-ttu-id="06bb8-144">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="06bb8-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="06bb8-145">Versioni di valutazione e sottoscrizioni di [[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="06bb8-145">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="06bb8-146">Gestione di ambienti nell'interfaccia di amministrazione di Business Central</span><span class="sxs-lookup"><span data-stu-id="06bb8-146">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
