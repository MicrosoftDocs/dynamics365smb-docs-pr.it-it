---
title: Come connettere Power BI a Business Central | Documenti Microsoft
description: "Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con Power BI e con i pacchetti di contenuto di Business Central."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 48c57e03f4679ea05792304fe13bdf896be2f1e3
ms.contentlocale: it-it
ms.lasthandoff: 11/22/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="caf2a-103">Connessione di Power BI a pacchetti di contenuto di Dynamics 365 Business Central.</span><span class="sxs-lookup"><span data-stu-id="caf2a-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="caf2a-104">Ottenere informazioni approfondite sui dati di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] è semplice con Power BI e con i pacchetti di contenuto di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="caf2a-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="caf2a-105">Power BI recupera i dati e quindi sviluppa un dashboard e i report pronti per l'uso basati su tali dati.</span><span class="sxs-lookup"><span data-stu-id="caf2a-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="caf2a-106">È necessario disporre di un account valido con Dynamics 365 e con Power BI.</span><span class="sxs-lookup"><span data-stu-id="caf2a-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="caf2a-107">Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) per creare i propri report di Power BI.</span><span class="sxs-lookup"><span data-stu-id="caf2a-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="caf2a-108">I pacchetti di contenuto di Power BI richiedono l'autorizzazione per l'accesso alle tabelle da dove vengono recuperati i dati.</span><span class="sxs-lookup"><span data-stu-id="caf2a-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="caf2a-109">Più informazioni dettagliate sui requisiti sono descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="caf2a-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="caf2a-110">Come ci si connette</span><span class="sxs-lookup"><span data-stu-id="caf2a-110">How to Connect</span></span>
1. <span data-ttu-id="caf2a-111">Selezionare **Ottieni i dati** nella parte inferiore del riquadro di spostamento sinistro.</span><span class="sxs-lookup"><span data-stu-id="caf2a-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="caf2a-112">![Passare a Ottieni i dati](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="caf2a-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="caf2a-113">È inoltre possibile iniziare dall'interno di Dynamics 365 Business Edition.</span><span class="sxs-lookup"><span data-stu-id="caf2a-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="caf2a-114">Dalla Gestione ruolo utente, passare a **Selezione report** nella sezione Gestione ruolo utente Power BI.</span><span class="sxs-lookup"><span data-stu-id="caf2a-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="caf2a-115">Selezionare **Assistenza** o **Organizzazione personale** dalla barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="caf2a-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="caf2a-116">Quando viene selezionata una di queste azioni, si verrà reindirizzati alla raccolta dell'organizzazione in Power BI o alla libreria dei servizi in Power BI, che verranno filtrate per visualizzare solo i pacchetti di contenuto relativi a [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="caf2a-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="caf2a-117">Nella casella **Servizi**, selezionare **Ottieni**.</span><span class="sxs-lookup"><span data-stu-id="caf2a-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="caf2a-118">Viene visualizzata una pagina con **AppSource** e **App per app Power BI**.</span><span class="sxs-lookup"><span data-stu-id="caf2a-118">This will open a page with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="caf2a-119">![Scegliere i pacchetti di contenuto da servizi in linea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="caf2a-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="caf2a-120">Selezionare **App** dalla scheda **App per app di Power BI** e scegliere il pacchetto di contenuti **Microsoft Dynamics 365 Business Central** che si desidera utilizzare e selezionare **Ottienilo ora**.</span><span class="sxs-lookup"><span data-stu-id="caf2a-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="caf2a-121">![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="caf2a-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="caf2a-122">Quando richiesto immettere il nome della *società* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="caf2a-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="caf2a-123">Questo non è il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="caf2a-123">This is not the display name.</span></span> <span data-ttu-id="caf2a-124">Il nome della società è disponibile nella pagina 'Società' all'interno dell'istanza di [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="caf2a-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="caf2a-125">![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="caf2a-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="caf2a-126">Una volta eseguita la connessione, un dashboard, un report e un set di dati verranno automaticamente caricati nell'area di lavoro Power BI.</span><span class="sxs-lookup"><span data-stu-id="caf2a-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="caf2a-127">Al termine, i riquadri saranno aggiornati con i dati della società [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="caf2a-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="caf2a-128">![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="caf2a-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="caf2a-129">Operazioni successive</span><span class="sxs-lookup"><span data-stu-id="caf2a-129">What Now?</span></span>

- <span data-ttu-id="caf2a-130">Provare a [porre una domanda nella casella delle domande e risposte](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) nella parte superiore del dashboard.</span><span class="sxs-lookup"><span data-stu-id="caf2a-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="caf2a-131">[Modificare i riquadri](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) nel dashboard.</span><span class="sxs-lookup"><span data-stu-id="caf2a-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="caf2a-132">[Selezionare un riquadro](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) per aprire il report sottostante.</span><span class="sxs-lookup"><span data-stu-id="caf2a-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="caf2a-133">Poiché il set di dati verrà programmato per l'aggiornamento giornaliero, è possibile modificare la pianificazione dell'aggiornamento o provare ad aggiornare su richiesta usando **Aggiorna ora**.</span><span class="sxs-lookup"><span data-stu-id="caf2a-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="caf2a-134">Requisiti di sistema</span><span class="sxs-lookup"><span data-stu-id="caf2a-134">System Requirements</span></span>
<span data-ttu-id="caf2a-135">Per importare i dati di [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI, è necessario disporre delle autorizzazioni per accedere ai servizi Web utilizzati per recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="caf2a-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="caf2a-136">I servizi Web necessari per ogni pacchetto di contenuti sono:</span><span class="sxs-lookup"><span data-stu-id="caf2a-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="caf2a-137">Report in Gestione ruolo utente</span><span class="sxs-lookup"><span data-stu-id="caf2a-137">Role Center Reports</span></span>

<span data-ttu-id="caf2a-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="caf2a-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="caf2a-139">Opportunità di vendita</span><span class="sxs-lookup"><span data-stu-id="caf2a-139">Sales Opportunities</span></span>
- <span data-ttu-id="caf2a-140">Modello di Excel Visualizza socetà</span><span class="sxs-lookup"><span data-stu-id="caf2a-140">Excel Template View Company</span></span>
- <span data-ttu-id="caf2a-141">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-141">Power BI Report Labels</span></span>

<span data-ttu-id="caf2a-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="caf2a-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="caf2a-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="caf2a-143">PowerBIFinance</span></span>
- <span data-ttu-id="caf2a-144">Modello di Excel Visualizza socetà</span><span class="sxs-lookup"><span data-stu-id="caf2a-144">Excel Template View Company</span></span>
- <span data-ttu-id="caf2a-145">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-145">Power BI Report Labels</span></span>

<span data-ttu-id="caf2a-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="caf2a-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="caf2a-147">Lista commesse</span><span class="sxs-lookup"><span data-stu-id="caf2a-147">Job List</span></span>
- <span data-ttu-id="caf2a-148">Righe pianificazione commessa</span><span class="sxs-lookup"><span data-stu-id="caf2a-148">Job Planning Lines</span></span>
- <span data-ttu-id="caf2a-149">Righe task commessa</span><span class="sxs-lookup"><span data-stu-id="caf2a-149">Job Task Lines</span></span>
- <span data-ttu-id="caf2a-150">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-150">Power BI Report Labels</span></span>
- <span data-ttu-id="caf2a-151">Modello di Excel Visualizza socetà</span><span class="sxs-lookup"><span data-stu-id="caf2a-151">Excel Template View Company</span></span>

<span data-ttu-id="caf2a-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="caf2a-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="caf2a-153">Dashboard vendite</span><span class="sxs-lookup"><span data-stu-id="caf2a-153">Sales Dashboard</span></span>
- <span data-ttu-id="caf2a-154">Modello di Excel Visualizza socetà</span><span class="sxs-lookup"><span data-stu-id="caf2a-154">Excel Template View Company</span></span>
- <span data-ttu-id="caf2a-155">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="caf2a-156">Report pagina liste</span><span class="sxs-lookup"><span data-stu-id="caf2a-156">List Page Reports</span></span> 

<span data-ttu-id="caf2a-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="caf2a-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="caf2a-158">Vendite articolo per cliente</span><span class="sxs-lookup"><span data-stu-id="caf2a-158">Item Sales by Customer</span></span>
- <span data-ttu-id="caf2a-159">Lista acquisti articolo Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="caf2a-160">Lista vendite articolo Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="caf2a-161">Dashboard vendite</span><span class="sxs-lookup"><span data-stu-id="caf2a-161">Sales Dashboard</span></span>
- <span data-ttu-id="caf2a-162">Lista clienti Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-162">Power BI Customer List</span></span>
- <span data-ttu-id="caf2a-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="caf2a-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="caf2a-164">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-164">Power BI Report Labels</span></span> 

<span data-ttu-id="caf2a-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="caf2a-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="caf2a-166">Lista importo C/G Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="caf2a-167">Importo a budget C/G Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="caf2a-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="caf2a-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="caf2a-169">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-169">Power BI Report Labels</span></span>

<span data-ttu-id="caf2a-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="caf2a-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="caf2a-171">Vendite articolo per cliente</span><span class="sxs-lookup"><span data-stu-id="caf2a-171">Item Sales by Customer</span></span>
- <span data-ttu-id="caf2a-172">Lista acquisti articolo Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="caf2a-173">Lista vendite articolo Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="caf2a-174">Dashboard vendite</span><span class="sxs-lookup"><span data-stu-id="caf2a-174">Sales Dashboard</span></span>
- <span data-ttu-id="caf2a-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="caf2a-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="caf2a-176">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-176">Power BI Report Labels</span></span>

<span data-ttu-id="caf2a-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="caf2a-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="caf2a-178">Lista commesse Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-178">Power BI Jobs List</span></span>
- <span data-ttu-id="caf2a-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="caf2a-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="caf2a-180">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-180">Power BI Report Labels</span></span>

<span data-ttu-id="caf2a-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="caf2a-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="caf2a-182">Lista acquisti Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-182">Power BI Purchase List</span></span>
- <span data-ttu-id="caf2a-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="caf2a-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="caf2a-184">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-184">Power BI Report Labels</span></span>

<span data-ttu-id="caf2a-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="caf2a-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="caf2a-186">Lista vendite Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-186">Power BI Sales List</span></span>
- <span data-ttu-id="caf2a-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="caf2a-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="caf2a-188">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-188">Power BI Report Labels</span></span>


<span data-ttu-id="caf2a-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="caf2a-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="caf2a-190">Lista acquisti articolo Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="caf2a-191">Lista vendite articolo Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="caf2a-192">Lista fornitori Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-192">Power BI Vendor List</span></span>
- <span data-ttu-id="caf2a-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="caf2a-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="caf2a-194">Etichette report Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="caf2a-195">Servizi Web</span><span class="sxs-lookup"><span data-stu-id="caf2a-195">Web Services</span></span>
<span data-ttu-id="caf2a-196">Un modo facile di individuare i servizi Web consiste nel ricercarli in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="caf2a-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="caf2a-197">Nell'elenco assicurarsi che la casella Pubblica sia contrassegnata per i servizi Web sopra elencati.</span><span class="sxs-lookup"><span data-stu-id="caf2a-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="caf2a-198">Troubleshooting</span><span class="sxs-lookup"><span data-stu-id="caf2a-198">Troubleshooting</span></span>
<span data-ttu-id="caf2a-199">Il dashboard di Power BI si basa sui servizi Web rilasciati che sono elencati sopra e visualizza i dati della società demo o della società dell'utente se si importano i dati della soluzione finanziario corrente.</span><span class="sxs-lookup"><span data-stu-id="caf2a-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="caf2a-200">Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.</span><span class="sxs-lookup"><span data-stu-id="caf2a-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="caf2a-201">Nome della società non corretto</span><span class="sxs-lookup"><span data-stu-id="caf2a-201">Incorrect Company Name</span></span>  
<span data-ttu-id="caf2a-202">Un errore comune consiste nell'immettere il nome visualizzato della società al posto del nome della società.</span><span class="sxs-lookup"><span data-stu-id="caf2a-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="caf2a-203">Per individuare il nome della società, cercare **Società**.</span><span class="sxs-lookup"><span data-stu-id="caf2a-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="caf2a-204">Quindi utilizzare il campo **Nome** quando si immette il nome della società.</span><span class="sxs-lookup"><span data-stu-id="caf2a-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="caf2a-205">Nome utente e password errate</span><span class="sxs-lookup"><span data-stu-id="caf2a-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="caf2a-206">Il nome utente e la password utilizzati per connettersi sono uguali a quelli usati per connettersi all'account Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="caf2a-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="caf2a-207">I pacchetti di contenuto richiedono inoltre la presenza di un account Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="caf2a-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="caf2a-208">Una volta immesse le credenziali, verranno individuati tutti i tenant Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a cui è possibile accedere.</span><span class="sxs-lookup"><span data-stu-id="caf2a-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="caf2a-209">Se non si dispone di un account Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] con licenza o di prova, verrà visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="caf2a-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="caf2a-210">Nessuna riga corrispondente alla chiave nella tabella</span><span class="sxs-lookup"><span data-stu-id="caf2a-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="caf2a-211">Se si immette un nome di società non valido durante il processo di connessione, è possibile che sia visualizzato il messaggio di errore "Nessuna riga corrispondente alla chiave nella tabella".</span><span class="sxs-lookup"><span data-stu-id="caf2a-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="caf2a-212">Immettere il nome di società corretto e riprovare.</span><span class="sxs-lookup"><span data-stu-id="caf2a-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="caf2a-213">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="caf2a-213">See Also</span></span>
[<span data-ttu-id="caf2a-214">Introduzione a Power BI</span><span class="sxs-lookup"><span data-stu-id="caf2a-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="caf2a-215">Power BI - Concetti di base</span><span class="sxs-lookup"><span data-stu-id="caf2a-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="caf2a-216">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="caf2a-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="caf2a-217">Introduzione</span><span class="sxs-lookup"><span data-stu-id="caf2a-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="caf2a-218">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="caf2a-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="caf2a-219">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="caf2a-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="caf2a-220">Finanze</span><span class="sxs-lookup"><span data-stu-id="caf2a-220">Finance</span></span>](finance.md)  
<span data-ttu-id="caf2a-221">[Setup della creazione di report per [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="caf2a-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

