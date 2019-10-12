---
title: Utilizzare i dati per creare un'app| Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un'app aziendale utilizzando PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305027"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a><span data-ttu-id="e37f7-103">Collegamento ai dati Business Central per creare un'app aziendale utilizzando PowerApps</span><span class="sxs-lookup"><span data-stu-id="e37f7-103">Connecting to Your Business Central Data to Build a Business App Using PowerApps</span></span>
<span data-ttu-id="e37f7-104">È possibile rendere disponibili i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e37f7-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in PowerApps.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e37f7-105">È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e37f7-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with PowerApps.</span></span>  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a><span data-ttu-id="e37f7-106">Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps</span><span class="sxs-lookup"><span data-stu-id="e37f7-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in PowerApps</span></span>
1. <span data-ttu-id="e37f7-107">Nel browser passare a [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), quindi accedere.</span><span class="sxs-lookup"><span data-stu-id="e37f7-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="e37f7-108">Nella home page, scegliere **App**, **Crea un'app** e **Canvas** per creare una nuova app canvas.</span><span class="sxs-lookup"><span data-stu-id="e37f7-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="e37f7-109">Questa app verrà progettata per l'uso su un dispositivo mobile, ma è anche possibile scegliere di utilizzare un altro modello.</span><span class="sxs-lookup"><span data-stu-id="e37f7-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="e37f7-110">Il passaggio successivo per creare una PowerApp è selezionare i dati.</span><span class="sxs-lookup"><span data-stu-id="e37f7-110">The next step to create a PowerApp is to select your data.</span></span> <span data-ttu-id="e37f7-111">Scegliere l'icona della freccia, quindi scegliere l'opzione **Nuova connessione** nella parte in alto a sinistra della pagina.</span><span class="sxs-lookup"><span data-stu-id="e37f7-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="e37f7-112">Nell'elenco delle connessioni disponibili, scegliere **Business Central**, quindi scegliere il pulsante **Crea**.</span><span class="sxs-lookup"><span data-stu-id="e37f7-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="e37f7-113">PowerApps verrà collegato a [!INCLUDE [prodshort](includes/prodshort.md)] utilizzando le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="e37f7-113">PowerApps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="e37f7-114">Se non si è un amministratore di [!INCLUDE [prodshort](includes/prodshort.md)], è possibile che sia necessario eseguire l'accesso con un altro account.</span><span class="sxs-lookup"><span data-stu-id="e37f7-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4.  <span data-ttu-id="e37f7-115">In PowerApps verrà visualizzato un elenco di *Ambienti e società* disponibili tramite [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e37f7-115">PowerApps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="e37f7-116">Scegliere l'ambiente e l'azienda che contiene i dati a cui si intende connettersi.</span><span class="sxs-lookup"><span data-stu-id="e37f7-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="e37f7-117">Successivamente, verrà visualizzato un elenco di API.</span><span class="sxs-lookup"><span data-stu-id="e37f7-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="e37f7-118">Selezionare l'**API** a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="e37f7-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="e37f7-119">Queste cosiddette tabelle fanno parte dell'API [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e37f7-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="e37f7-120">Non è necessario configurare personalmente i punti finali in quanto questa operazione viene eseguita dal connettore [!INCLUDE [prodshort](includes/prodshort.md)] per PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e37f7-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for PowerApps does it for you.</span></span>  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

<span data-ttu-id="e37f7-121">A questo punto, si è eseguita la connessione ai dati di [!INCLUDE [prodshort](includes/prodshort.md)] e si è pronti per iniziare a creare PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e37f7-121">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="e37f7-122">È possibile aggiungere ulteriori schermi ed eseguire la connessione a ulteriori dati di [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e37f7-122">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="e37f7-123">Per ulteriori informazioni, vedere [Creare un'app canvas da un modello in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="e37f7-123">For more information, see [Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="e37f7-124">Dopo avere pianificato e creato l'app, è possibile condividerla con i colleghi.</span><span class="sxs-lookup"><span data-stu-id="e37f7-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="e37f7-125">Per ulteriori informazioni, vedere [Salvare e pubblicare un'app canvas in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="e37f7-125">For more information, see [Save and publish a canvas app in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="e37f7-126">Se si desidera eseguire la connessione a [!INCLUDE [prodshort](includes/prodshort.md)] in locale, è necessario scegliere il connettore **Business Central (locale)** nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="e37f7-126">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e37f7-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e37f7-127">See Also</span></span>

<span data-ttu-id="e37f7-128">[Creare un'app canvas da un modello in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="e37f7-128">[Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)</span></span>  
[<span data-ttu-id="e37f7-129">Introduzione</span><span class="sxs-lookup"><span data-stu-id="e37f7-129">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="e37f7-130">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="e37f7-130">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="e37f7-131">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="e37f7-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="e37f7-132">Finanze</span><span class="sxs-lookup"><span data-stu-id="e37f7-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="e37f7-133">Introduzione allo sviluppo di app di connessione per Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="e37f7-133">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
