---
title: Utilizzare i dati per creare un'app| Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un'app aziendale utilizzando Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bfa7a36a7655b4b26dfbfd11688fe42eeb19cfe
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379325"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="32662-103">Collegamento ai dati Business Central per creare un'app aziendale utilizzando Power Apps</span><span class="sxs-lookup"><span data-stu-id="32662-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="32662-104">È possibile rendere disponibili i dati di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="32662-104">You can make your [!INCLUDE[prod_short](includes/prod_short.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="32662-105">È necessario disporre di un account valido con [!INCLUDE[prod_short](includes/prod_short.md)] e con Power Apps.</span><span class="sxs-lookup"><span data-stu-id="32662-105">You must have a valid account with [!INCLUDE[prod_short](includes/prod_short.md)] and with Power Apps.</span></span>  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a><span data-ttu-id="32662-106">Per aggiungere [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power Apps</span><span class="sxs-lookup"><span data-stu-id="32662-106">To add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="32662-107">Nel browser passare a [powerapps.microsoft.com](https://powerapps.microsoft.com/), quindi accedere.</span><span class="sxs-lookup"><span data-stu-id="32662-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="32662-108">Nella home page, nella sezione **Inizia dai dati** scegliere il riquadro **Altre origini dati**.</span><span class="sxs-lookup"><span data-stu-id="32662-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="32662-109">Viene aperto Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="32662-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="32662-110">Al primo accesso, è necessario specificare il paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="32662-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="32662-111">Nell'elenco delle connessioni disponibili, scegliere **Business Central**, quindi scegliere il pulsante **Crea**.</span><span class="sxs-lookup"><span data-stu-id="32662-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="32662-112">Power Apps verrà collegato a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="32662-112">Power Apps will connect to your [!INCLUDE[prod_short](includes/prod_short.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="32662-113">Se non si è un amministratore di [!INCLUDE[prod_short](includes/prod_short.md)], è possibile che sia necessario eseguire l'accesso con un altro account.</span><span class="sxs-lookup"><span data-stu-id="32662-113">If you are not an administrator of your [!INCLUDE[prod_short](includes/prod_short.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="32662-114">In Power Apps verrà visualizzato un elenco di *Ambienti e società* disponibili tramite [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="32662-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="32662-115">Scegliere l'ambiente e l'azienda che contiene i dati a cui si intende connettersi, ad esempio *PRODUCTION - My Company*.</span><span class="sxs-lookup"><span data-stu-id="32662-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="32662-116">Successivamente, verrà visualizzato un elenco di tabelle che sono esposte come parte dell'API per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="32662-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="32662-117">Selezionare la tabella a cui connettersi quindi scegliere **Connetti**.</span><span class="sxs-lookup"><span data-stu-id="32662-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="32662-118">Queste cosiddette tabelle sono esposte come endpoint dal connettore [!INCLUDE[prod_short](includes/prod_short.md)] per Power Apps.</span><span class="sxs-lookup"><span data-stu-id="32662-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prod_short](includes/prod_short.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="32662-119">Se si desidera includere dati di altre tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] nell'app, è necessario lavorare con un sviluppatore per definire un API personalizzata in [!INCLUDE[prod_short](includes/prod_short.md)] e quindi utilizzare tale API mediante un connettore personalizzato in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="32662-119">If you want to include data from other tables in [!INCLUDE[prod_short](includes/prod_short.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prod_short](includes/prod_short.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="32662-120">Per ulteriori informazioni, vedere [Creare un connettore personalizzato da zero](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="32662-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="32662-121">A questo punto, si è eseguita la connessione ai dati di [!INCLUDE[prod_short](includes/prod_short.md)] e si è pronti per iniziare a creare PowerApp.</span><span class="sxs-lookup"><span data-stu-id="32662-121">At this point, you have successfully connected to your [!INCLUDE[prod_short](includes/prod_short.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="32662-122">È possibile aggiungere ulteriori schermi ed eseguire la connessione a ulteriori dati di [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="32662-122">You can add additional screens and connect to additional data from your [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="32662-123">Per ulteriori informazioni, vedere [Creare un'app canvas da un esempio in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="32662-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="32662-124">Dopo avere pianificato e creato l'app, è possibile condividerla con i colleghi.</span><span class="sxs-lookup"><span data-stu-id="32662-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="32662-125">Per ulteriori informazioni, vedere [Salvare e pubblicare un'app canvas in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="32662-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="32662-126">Se si desidera eseguire la connessione a [!INCLUDE[prod_short](includes/prod_short.md)] in locale, è necessario scegliere il connettore **Business Central (locale)** nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="32662-126">If you want to connect to [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="32662-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="32662-127">See Also</span></span>

[<span data-ttu-id="32662-128">Creare un'app canvas da un modello in Power Apps</span><span class="sxs-lookup"><span data-stu-id="32662-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="32662-129">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="32662-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="32662-130">[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="32662-130">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="32662-131">Introduzione allo sviluppo di app di connessione per Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="32662-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]