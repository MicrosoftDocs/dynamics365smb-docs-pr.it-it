---
title: Utilizzare i dati per creare un'app| Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un'app aziendale utilizzando Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 8f0eb7a1562a8300bd7181ef6470c70f60934470
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528640"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="40157-103">Collegamento ai dati Business Central per creare un'app aziendale utilizzando Power Apps</span><span class="sxs-lookup"><span data-stu-id="40157-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="40157-104">È possibile rendere disponibili i dati di [!INCLUDE[prodshort](includes/prodshort.md)] come origine dati in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="40157-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="40157-105">È necessario disporre di un account valido con [!INCLUDE[prodshort](includes/prodshort.md)] e con Power Apps.</span><span class="sxs-lookup"><span data-stu-id="40157-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="40157-106">Per aggiungere [!INCLUDE[prodshort](includes/prodshort.md)] come origine dati in Power Apps</span><span class="sxs-lookup"><span data-stu-id="40157-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="40157-107">Nel browser passare a [powerapps.microsoft.com](https://powerapps.microsoft.com/), quindi accedere.</span><span class="sxs-lookup"><span data-stu-id="40157-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="40157-108">Nella home page, nella sezione **Inizia dai dati** scegliere il riquadro **Altre origini dati**.</span><span class="sxs-lookup"><span data-stu-id="40157-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="40157-109">Viene aperto Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="40157-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="40157-110">Al primo accesso, è necessario specificare il paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="40157-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="40157-111">Nell'elenco delle connessioni disponibili, scegliere **Business Central**, quindi scegliere il pulsante **Crea**.</span><span class="sxs-lookup"><span data-stu-id="40157-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="40157-112">Power Apps verrà collegato a [!INCLUDE[prodshort](includes/prodshort.md)] utilizzando le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="40157-112">Power Apps will connect to your [!INCLUDE[prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="40157-113">Se non si è un amministratore di [!INCLUDE[prodshort](includes/prodshort.md)], è possibile che sia necessario eseguire l'accesso con un altro account.</span><span class="sxs-lookup"><span data-stu-id="40157-113">If you are not an administrator of your [!INCLUDE[prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="40157-114">In Power Apps verrà visualizzato un elenco di *Ambienti e società* disponibili tramite [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="40157-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="40157-115">Scegliere l'ambiente e l'azienda che contiene i dati a cui si intende connettersi, ad esempio *PRODUCTION - My Company*.</span><span class="sxs-lookup"><span data-stu-id="40157-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="40157-116">Successivamente, verrà visualizzato un elenco di tabelle che sono esposte come parte dell'API per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="40157-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="40157-117">Selezionare la tabella a cui connettersi quindi scegliere **Connetti**.</span><span class="sxs-lookup"><span data-stu-id="40157-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="40157-118">Queste cosiddette tabelle sono esposte come endpoint dal connettore [!INCLUDE[prodshort](includes/prodshort.md)] per Power Apps.</span><span class="sxs-lookup"><span data-stu-id="40157-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prodshort](includes/prodshort.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="40157-119">Se si desidera includere dati di altre tabelle in [!INCLUDE[prodshort](includes/prodshort.md)] nell'app, è necessario lavorare con un sviluppatore per definire un API personalizzata in [!INCLUDE[prodshort](includes/prodshort.md)] e quindi utilizzare tale API mediante un connettore personalizzato in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="40157-119">If you want to include data from other tables in [!INCLUDE[prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="40157-120">Per ulteriori informazioni, vedere [Creare un connettore personalizzato da zero](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="40157-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="40157-121">A questo punto, si è eseguita la connessione ai dati di [!INCLUDE[prodshort](includes/prodshort.md)] e si è pronti per iniziare a creare PowerApp.</span><span class="sxs-lookup"><span data-stu-id="40157-121">At this point, you have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="40157-122">È possibile aggiungere ulteriori schermi ed eseguire la connessione a ulteriori dati di [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="40157-122">You can add additional screens and connect to additional data from your [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="40157-123">Per ulteriori informazioni, vedere [Creare un'app canvas da un esempio in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="40157-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="40157-124">Dopo avere pianificato e creato l'app, è possibile condividerla con i colleghi.</span><span class="sxs-lookup"><span data-stu-id="40157-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="40157-125">Per ulteriori informazioni, vedere [Salvare e pubblicare un'app canvas in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="40157-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="40157-126">Se si desidera eseguire la connessione a [!INCLUDE[prodshort](includes/prodshort.md)] in locale, è necessario scegliere il connettore **Business Central (locale)** nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="40157-126">If you want to connect to [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="40157-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="40157-127">See Also</span></span>

[<span data-ttu-id="40157-128">Creare un'app canvas da un modello in Power Apps</span><span class="sxs-lookup"><span data-stu-id="40157-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="40157-129">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="40157-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="40157-130">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="40157-130">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="40157-131">Introduzione allo sviluppo di app di connessione per Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="40157-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
