---
title: Utilizzare report di Business Central in Power BI | Microsoft Docs
description: Rendere disponibili i dati come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187894"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="00bd4-103">Uso di [!INCLUDE [prodlong](includes/prodlong.md)] come origine dati di Power BI per la creazione di report</span><span class="sxs-lookup"><span data-stu-id="00bd4-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="00bd4-104">È possibile rendere disponibili i dati di [!INCLUDE[prodlong](includes/prodlong.md)] come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="00bd4-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="00bd4-105">È necessario disporre di un account valido con [!INCLUDE[prodshort](includes/prodshort.md)] e con Power BI.</span><span class="sxs-lookup"><span data-stu-id="00bd4-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="00bd4-106">Devi anche scaricare [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span><span class="sxs-lookup"><span data-stu-id="00bd4-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="00bd4-107">Per ulteriori informazioni, vedere [Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="00bd4-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="00bd4-108">Per aggiungere [!INCLUDE[prodshort](includes/prodshort.md)] come origine dati in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="00bd4-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="00bd4-109">In Power BI Desktop, nel riquadro di spostamento sinistro, scegliere **Ottieni i dati**.</span><span class="sxs-lookup"><span data-stu-id="00bd4-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="00bd4-110">Nella pagina **Ottieni i dati**, scegliere **Servizi online**, quindi **Microsoft Dynamics 365 Business Central** e infine il pulsante **Connetti**.</span><span class="sxs-lookup"><span data-stu-id="00bd4-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="00bd4-111">Power BI visualizza una procedura guidata per il processo di connessione, incluso l'accesso a [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="00bd4-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="00bd4-112">Scegli **Accedi**, quindi seleziona l'account pertinente.</span><span class="sxs-lookup"><span data-stu-id="00bd4-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="00bd4-113">Utilizza lo stesso account usato per accedere a [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="00bd4-113">Use the same account that you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="00bd4-114">Fare clic sul pulsante **Connetti** per continuare.</span><span class="sxs-lookup"><span data-stu-id="00bd4-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="00bd4-115">La procedura guidata di Power BI mostra un elenco di ambienti, origini dati e società di Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00bd4-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="00bd4-116">Le origini dati, indicano tutti i servizi Web pubblicati tramite [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="00bd4-116">These data sources represent all the web services that you have published from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="00bd4-117">Puoi anche creare un nuovo URL del servizio web in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="00bd4-117">You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="00bd4-118">Scegli uno dei seguenti metodi:</span><span class="sxs-lookup"><span data-stu-id="00bd4-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="00bd4-119">Usa l'azione **Crea set di dati** della pagina **Servizi Web**</span><span class="sxs-lookup"><span data-stu-id="00bd4-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="00bd4-120">Usa la guida del setup assistito **Imposta creazione di report**</span><span class="sxs-lookup"><span data-stu-id="00bd4-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="00bd4-121">Scegli l'azione **Modifica in Excel** in qualsiasi elenco</span><span class="sxs-lookup"><span data-stu-id="00bd4-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="00bd4-122">Specificare i dati che si desidera aggiungere al modello dati quindi scegliere il pulsante **Carica**.</span><span class="sxs-lookup"><span data-stu-id="00bd4-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="00bd4-123">Ripetere i passaggi precedenti per aggiungere ulteriori [!INCLUDE [prodshort](includes/prodshort.md)], o altri dati, per il modello dati Power BI.</span><span class="sxs-lookup"><span data-stu-id="00bd4-123">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="00bd4-124">Una volta eseguita la connessione a [!INCLUDE [prodshort](includes/prodshort.md)], non verrà richiesto nuovamente di eseguire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="00bd4-124">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="00bd4-125">Dopo che i dati sono stati caricati puoi vederli nel riquadro di spostamento destro nella pagina.</span><span class="sxs-lookup"><span data-stu-id="00bd4-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="00bd4-126">Hai stabilito correttamente la connessione ai dati di [!INCLUDE [prodshort](includes/prodshort.md)] e sei pronto per iniziare a creare il report di Power BI.</span><span class="sxs-lookup"><span data-stu-id="00bd4-126">You have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="00bd4-127">Prima di creare il report, è consigliabile importare il file del tema [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="00bd4-127">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="00bd4-128">Il file del tema creerà una tavolozza dei colori in modo da creare report con lo stesso stile cromatico delle app [!INCLUDE [prodshort](includes/prodshort.md)] senza dover defifnire i colori personalizzati per ogni elemento grafico.</span><span class="sxs-lookup"><span data-stu-id="00bd4-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="00bd4-129">Per ulteriori informazioni, vedere [Documentazione di Power BI](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="00bd4-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="00bd4-130">Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="00bd4-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="00bd4-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="00bd4-131">See Also</span></span>

[<span data-ttu-id="00bd4-132">Abilitare i dati aziendali per Power BI</span><span class="sxs-lookup"><span data-stu-id="00bd4-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="00bd4-133">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="00bd4-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="00bd4-134">Introduzione</span><span class="sxs-lookup"><span data-stu-id="00bd4-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="00bd4-135">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="00bd4-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="00bd4-136">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="00bd4-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="00bd4-137">Finanze</span><span class="sxs-lookup"><span data-stu-id="00bd4-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="00bd4-138">Avvio rapido: connettersi ai dati in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="00bd4-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
