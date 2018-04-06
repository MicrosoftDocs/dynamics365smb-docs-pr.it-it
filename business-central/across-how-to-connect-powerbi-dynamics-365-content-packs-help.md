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
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="403b5-103">Connessione di Power BI a pacchetti di contenuto di Business Central.</span><span class="sxs-lookup"><span data-stu-id="403b5-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="403b5-104">Ottenere informazioni approfondite sui dati di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] è semplice con Power BI e con i pacchetti di contenuto di Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="403b5-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="403b5-105">Power BI recupera i dati e quindi sviluppa un dashboard e i report pronti per l'uso basati su tali dati.</span><span class="sxs-lookup"><span data-stu-id="403b5-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="403b5-106">È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con Power BI.</span><span class="sxs-lookup"><span data-stu-id="403b5-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="403b5-107">Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="403b5-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="403b5-108">I pacchetti di contenuto di Power BI richiedono l'autorizzazione per l'accesso alle tabelle da dove vengono recuperati i dati.</span><span class="sxs-lookup"><span data-stu-id="403b5-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="403b5-109">Più informazioni dettagliate sui requisiti sono descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="403b5-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="403b5-110">Come ci si connette</span><span class="sxs-lookup"><span data-stu-id="403b5-110">How to Connect</span></span>
1. <span data-ttu-id="403b5-111">Selezionare **Ottieni i dati** nella parte inferiore del riquadro di spostamento sinistro.</span><span class="sxs-lookup"><span data-stu-id="403b5-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="403b5-112">![Passare a Ottieni i dati](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="403b5-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="403b5-113">Nella casella **Servizi**, selezionare **Ottieni**.</span><span class="sxs-lookup"><span data-stu-id="403b5-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="403b5-114">Viene visualizzata una finestra con **AppSource** e **App per app Power BI**.</span><span class="sxs-lookup"><span data-stu-id="403b5-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="403b5-115">![Scegliere i pacchetti di contenuto da servizi in linea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="403b5-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="403b5-116">Selezionare **App** dalla scheda **App per app di Power BI** e scegliere il pacchetto di contenuti **Microsoft Dynamics 365 Business Central** che si desidera utilizzare e selezionare **Ottienilo ora**.</span><span class="sxs-lookup"><span data-stu-id="403b5-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="403b5-117">![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="403b5-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="403b5-118">Quando richiesto immettere il nome della *società* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="403b5-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="403b5-119">Questo non è il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="403b5-119">This is not the display name.</span></span>  
<span data-ttu-id="403b5-120">![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="403b5-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="403b5-121">Una volta eseguita la connessione, un dashboard, un report e un set di dati verranno automaticamente caricati nell'area di lavoro Power BI.</span><span class="sxs-lookup"><span data-stu-id="403b5-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="403b5-122">Al termine, i riquadri saranno aggiornati con i dati dell'account.</span><span class="sxs-lookup"><span data-stu-id="403b5-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="403b5-123">![Selezionare Dynamics 365 Business Central e scegliere Ottienilo ora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="403b5-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="403b5-124">Operazioni successive</span><span class="sxs-lookup"><span data-stu-id="403b5-124">What Now?</span></span>

- <span data-ttu-id="403b5-125">[Modificare i riquadri](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) nel dashboard.</span><span class="sxs-lookup"><span data-stu-id="403b5-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="403b5-126">[Selezionare un riquadro](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) per aprire il report sottostante.</span><span class="sxs-lookup"><span data-stu-id="403b5-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="403b5-127">Poiché il set di dati verrà programmato per l'aggiornamento giornaliero, è possibile modificare la pianificazione dell'aggiornamento o provare ad aggiornare su richiesta usando **Aggiorna ora**.</span><span class="sxs-lookup"><span data-stu-id="403b5-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="403b5-128">Requisiti di sistema</span><span class="sxs-lookup"><span data-stu-id="403b5-128">System Requirements</span></span>
<span data-ttu-id="403b5-129">Per importare i dati di [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI, è necessario disporre delle autorizzazioni per accedere ai servizi Web utilizzati per recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="403b5-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="403b5-130">I servizi Web necessari per ogni pacchetto di contenuti sono:</span><span class="sxs-lookup"><span data-stu-id="403b5-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="403b5-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="403b5-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="403b5-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="403b5-132">SalesOpportunities</span></span>
- <span data-ttu-id="403b5-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="403b5-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="403b5-134">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="403b5-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="403b5-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="403b5-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="403b5-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="403b5-136">SalesDashboard</span></span>
- <span data-ttu-id="403b5-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="403b5-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="403b5-138">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="403b5-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="403b5-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="403b5-139">PowerBIFinance</span></span>
- <span data-ttu-id="403b5-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="403b5-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="403b5-141">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="403b5-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="403b5-142">Lista commesse</span><span class="sxs-lookup"><span data-stu-id="403b5-142">Job List</span></span>
- <span data-ttu-id="403b5-143">Righe pianificazione commessa</span><span class="sxs-lookup"><span data-stu-id="403b5-143">Job Planning Lines</span></span>
- <span data-ttu-id="403b5-144">Righe task commessa</span><span class="sxs-lookup"><span data-stu-id="403b5-144">Job Task Lines</span></span>

<span data-ttu-id="403b5-145">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="403b5-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="403b5-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="403b5-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="403b5-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="403b5-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="403b5-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="403b5-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="403b5-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="403b5-149">SalesDashboard</span></span>
- <span data-ttu-id="403b5-150">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="403b5-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="403b5-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="403b5-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="403b5-152">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="403b5-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="403b5-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="403b5-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="403b5-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="403b5-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="403b5-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="403b5-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="403b5-156">Articoli</span><span class="sxs-lookup"><span data-stu-id="403b5-156">Items</span></span>
- <span data-ttu-id="403b5-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="403b5-157">SalesDashboard</span></span>
- <span data-ttu-id="403b5-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="403b5-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="403b5-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="403b5-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="403b5-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="403b5-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="403b5-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="403b5-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="403b5-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="403b5-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="403b5-163">Articoli</span><span class="sxs-lookup"><span data-stu-id="403b5-163">Items</span></span>
- <span data-ttu-id="403b5-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="403b5-164">SalesDashboard</span></span>
- <span data-ttu-id="403b5-165">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="403b5-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="403b5-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="403b5-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="403b5-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="403b5-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="403b5-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="403b5-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="403b5-169">Servizi Web</span><span class="sxs-lookup"><span data-stu-id="403b5-169">Web Services</span></span>
<span data-ttu-id="403b5-170">Un modo facile di individuare i servizi Web consiste nel ricercarli in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="403b5-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="403b5-171">Nell'elenco assicurarsi che la casella Pubblica sia contrassegnata per i servizi Web sopra elencati.</span><span class="sxs-lookup"><span data-stu-id="403b5-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="403b5-172">Troubleshooting</span><span class="sxs-lookup"><span data-stu-id="403b5-172">Troubleshooting</span></span>
<span data-ttu-id="403b5-173">Il dashboard di Power BI si basa sui servizi Web rilasciati che sono elencati sopra e visualizza i dati della società demo o della società dell'utente se si importano i dati della soluzione finanziario corrente.</span><span class="sxs-lookup"><span data-stu-id="403b5-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="403b5-174">Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.</span><span class="sxs-lookup"><span data-stu-id="403b5-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="403b5-175">Nome della società non corretto</span><span class="sxs-lookup"><span data-stu-id="403b5-175">Incorrect Company Name</span></span>  
<span data-ttu-id="403b5-176">Un errore comune consiste nell'immettere il nome visualizzato della società al posto del nome della società.</span><span class="sxs-lookup"><span data-stu-id="403b5-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="403b5-177">Per individuare il nome della società, cercare **Società**.</span><span class="sxs-lookup"><span data-stu-id="403b5-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="403b5-178">Quindi utilizzare il campo **Nome** quando si immette il nome della società.</span><span class="sxs-lookup"><span data-stu-id="403b5-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="403b5-179">Nome utente e password errate</span><span class="sxs-lookup"><span data-stu-id="403b5-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="403b5-180">Il nome utente e la password utilizzati per connettersi sono uguali a quelli usati per connettersi all'account Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="403b5-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="403b5-181">I pacchetti di contenuto richiedono inoltre la presenza di un account Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="403b5-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="403b5-182">Una volta immesse le credenziali, verranno individuati tutti i tenant Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a cui è possibile accedere.</span><span class="sxs-lookup"><span data-stu-id="403b5-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="403b5-183">Se non si dispone di un account Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] con licenza o di prova, verrà visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="403b5-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="403b5-184">Nessuna riga corrispondente alla chiave nella tabella</span><span class="sxs-lookup"><span data-stu-id="403b5-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="403b5-185">Se si immette un nome di società non valido durante il processo di connessione, è possibile che sia visualizzato il messaggio di errore "Nessuna riga corrispondente alla chiave nella tabella".</span><span class="sxs-lookup"><span data-stu-id="403b5-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="403b5-186">Immettere il nome di società corretto e riprovare.</span><span class="sxs-lookup"><span data-stu-id="403b5-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="403b5-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="403b5-187">See Also</span></span>
[<span data-ttu-id="403b5-188">Introduzione a Power BI</span><span class="sxs-lookup"><span data-stu-id="403b5-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="403b5-189">[Power BI - Concetti](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span><span class="sxs-lookup"><span data-stu-id="403b5-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="403b5-190">[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="403b5-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="403b5-191">Importazione dei dati aziendali da altri sistemi contabili</span><span class="sxs-lookup"><span data-stu-id="403b5-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="403b5-192">[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="403b5-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="403b5-193">Finanze</span><span class="sxs-lookup"><span data-stu-id="403b5-193">Finance</span></span>](finance.md)  
<span data-ttu-id="403b5-194">[Setup della creazione di report per [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="403b5-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

