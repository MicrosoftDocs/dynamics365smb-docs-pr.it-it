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
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 113c081e60b825c48cfb85ae3475a713a1a1e215
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "937948"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a><span data-ttu-id="014eb-103">Creazione di un ambiente sandbox</span><span class="sxs-lookup"><span data-stu-id="014eb-103">Creating a Sandbox Environment</span></span>
<span data-ttu-id="014eb-104">Un ambiente sandbox (anteprima) è un'istanza di non produzione di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="014eb-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="014eb-105">Isolato dalla produzione, un ambiente sandbox consente di esplorare, apprendere, dimostrare, sviluppare e testare in sicurezza il servizio senza il rischio di compromettere i dati e le impostazioni dell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="014eb-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="014eb-106">Per creare un ambiente sandbox</span><span class="sxs-lookup"><span data-stu-id="014eb-106">To create a sandbox environment</span></span>
<span data-ttu-id="014eb-107">Per poter creare un ambiente sandbox, è necessario possedere una sottoscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="014eb-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="014eb-108">Può esistere un solo ambiente sandbox per sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="014eb-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="014eb-109">Accedere all'istanza di produzione del servizio [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="014eb-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>
2. <span data-ttu-id="014eb-110">Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ambiente sandbox** e quindi scegliere il collegamento correlato.</span><span class="sxs-lookup"><span data-stu-id="014eb-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="014eb-111">Selezionare **Crea**.</span><span class="sxs-lookup"><span data-stu-id="014eb-111">Select **Create**.</span></span>  
  <span data-ttu-id="014eb-112">Verrà aperta un'altra scheda nel browser per completare l'impostazione dell'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="014eb-112">Another tab in your browser will open for finishing the setup of your sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="014eb-113">Se la funzione Blocco popup del browser è abilitata, modificarne l'impostazione per consentire la visualizzazione degli URL dall'indirizzo \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="014eb-113">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>   

4. <span data-ttu-id="014eb-114">Quando l'ambiente sandbox è pronto, si verrà reindirizzati all'introduzione guidata dell'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="014eb-114">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. <span data-ttu-id="014eb-115">Scegliere **Ulteriori informazioni** per leggere informazioni sugli scenari che è possibile provare in un ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="014eb-115">Choose **Learn more** to read about scenarios that you can try in a sandbox environment.</span></span> <span data-ttu-id="014eb-116">In alternativa scegliere **Chiudi** per passare al servizio Gestione ruolo utente dell'istanza sandbox di [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="014eb-116">Or, choose **Close** to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>
6. <span data-ttu-id="014eb-117">Nella parte superiore di Gestione ruolo utente viene visualizzato un avviso che informa che ci si trova in un ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="014eb-117">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="014eb-118">È possibile vedere il tipo di ambiente anche nella barra del titolo del client.</span><span class="sxs-lookup"><span data-stu-id="014eb-118">You can also see the type of the environment in the title bar of the client.</span></span>
<!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) --> <span data-ttu-id="014eb-119">Nell'ambiente sandbox è stato creato un tenant nuovo.</span><span class="sxs-lookup"><span data-stu-id="014eb-119">In the sandbox environment, a new tenant has been created.</span></span> <span data-ttu-id="014eb-120">Questo tenant viene caricato con i dati di esempio di default relativi alla società CRONUS.</span><span class="sxs-lookup"><span data-stu-id="014eb-120">This tenant is loaded with default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="014eb-121">Nessun dato viene copiato o altrimenti trasferito dall'ambiente di produzione durante la creazione dell'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="014eb-121">No data is copied or otherwise transferred from the production environment during the sandbox creation.</span></span>

7. <span data-ttu-id="014eb-122">È possibile tornare in qualsiasi momento nella pagina **Ambiente sandbox** e reimpostare l'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="014eb-122">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="014eb-123">La reimpostazione dell'ambiente sandbox ne determinerà la rimozione completa e la successiva creazione di un nuovo ambiente sandbox con i dati dimostrativi di default.</span><span class="sxs-lookup"><span data-stu-id="014eb-123">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

8. <span data-ttu-id="014eb-124">Per passare tra gli ambienti di produzione e sandbox, è possibile utilizzare l'utilità di avvio dell'app Business Central.</span><span class="sxs-lookup"><span data-stu-id="014eb-124">To switch between your production and sandbox environments, you can use the Business Central app launcher.</span></span>
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

9. <span data-ttu-id="014eb-125">È possibile per un amministratore o un altro utente limitare o persino bloccare l'accesso da parte di alcuni utenti all'ambiente sandbox.</span><span class="sxs-lookup"><span data-stu-id="014eb-125">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="014eb-126">Questa operazione può essere effettuata utilizzando le funzionalità di sicurezza standard del prodotto, ad esempio la scheda Utente, Gruppi di utenti e Set di autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="014eb-126">This can be done by using the standard security features of the product, such as the User card, User Groups, and Permission Sets.</span></span>

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="014eb-127">Funzionalità avanzata nell'ambiente sandbox</span><span class="sxs-lookup"><span data-stu-id="014eb-127">Advanced functionality in the sandbox environment</span></span>
### <a name="designer"></a><span data-ttu-id="014eb-128">Designer</span><span class="sxs-lookup"><span data-stu-id="014eb-128">Designer</span></span>
<span data-ttu-id="014eb-129">In un ambiente sandbox la funzionalità di **progettazione** è abilitata. È possibile attivarla selezionando l'icona di progettazione ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) in una pagina.</span><span class="sxs-lookup"><span data-stu-id="014eb-129">In a sandbox environment, you will find the **Designer** enabled, which you can activate by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="enable-the-advanced-user-experience"></a><span data-ttu-id="014eb-130">Consentire l'esperienza utente avanzata</span><span class="sxs-lookup"><span data-stu-id="014eb-130">Enable the advanced user experience</span></span>
<span data-ttu-id="014eb-131">È possibile abilitare e provare la funzionalità completa avanzata di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un tenant sandbox impostando il campo **Esperienza** nella pagina **Informazioni società**.</span><span class="sxs-lookup"><span data-stu-id="014eb-131">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="014eb-132">Dopo avere abilitato la funzionalità avanzata in un tenant sandbox, si ottiene l'accesso a tutti i profili e i servizi Gestione ruolo utente standard.</span><span class="sxs-lookup"><span data-stu-id="014eb-132">After you’ve enabled the advanced functionality in a sandbox tenant, you get access to all the standard Profiles and Role Centers.</span></span> <span data-ttu-id="014eb-133">È inoltre possibile creare una società di valutazione completamente configurata, inclusiva dei dati di esempio e dell'accesso alle aree avanzate del prodotto.</span><span class="sxs-lookup"><span data-stu-id="014eb-133">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a><span data-ttu-id="014eb-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="014eb-134">See Also</span></span>
<span data-ttu-id="014eb-135">[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="014eb-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
