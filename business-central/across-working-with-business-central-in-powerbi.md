---
title: Connettersi a Power BI da Business Central locale | Documenti Microsoft
description: 'Ottenere informazioni dettagliate, business intelligence e KPI dai dati di Business Central utilizzando Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Connettersi a Power BI da Business Central locale

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## Introduzione

Per utilizzare [!INCLUDE [prod_short](includes/prod_short.md)] locale, è necessario che sia abilitato per l'integrazione di Power BI. Questa attività è in genere eseguita da un amministratore. Per ulteriori informazioni sull'abilitazione dell'integrazione di Power BI con Business Central online, vedi [Configurare Business Central locale per l'integrazione di Power BI](admin-powerbi-setup.md).

Alcune funzionalità sono disponibili solo con Business Central Online e non in locale. Per ulteriori informazioni, vedi [Introduzione a Business Central e Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="setup"></a>Configurare [!INCLUDE[prod_short](includes/prod_short.md)] locale per l'integrazione Power BI

Questa sezione spiega i requisiti per una distribuzione di [!INCLUDE[prod_short](includes/prod_short.md)] locale da integrare con Power BI.

1. Configura [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) o [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) come metodo di autenticazione per la distribuzione.  
    
    > [!NOTE]
    > L'integrazione di Power BI non supporta l'autenticazione di Windows e non è supportata sul client Windows.

2. Abilitare i servizi Web OData e l'endpoint ODataV4.

    Il servizio Web OData deve essere abilitato in [!INCLUDE[server](includes/server.md)] e la porta OData aperta nel firewall. Per ulteriori informazioni, vedere [Configurazione di Business Central Server - Servizi Web OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Il server locale deve essere accessibile da Internet.

3. Concedere agli account utente [!INCLUDE[prod_short](includes/prod_short.md)] una chiave di accesso al servizio Web.

    Una chiave di accesso al servizio Web è necessaria solo per visualizzare i dati di [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI. È possibile assegnare una chiave di accesso al servizio Web a ciascun account utente. In alternativa, creare un account specifico con una chiave di accesso al servizio Web utilizzabile da tutti gli utenti. Per ulteriori informazioni, vedere [Autenticazione dei servizi Web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Creare una registrazione dell'applicazione per [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    Per visualizzare i report Power BI incorporati nelle pagine [!INCLUDE[prod_short](includes/prod_short.md)] è necessario registrare un'applicazione per [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. L'applicazione registrata richiede l'autorizzazione per i servizi Power BI. Come minimo, l'app richiede l'autorizzazione **User.ReadWrite.All**. Per consentire agli utenti di visualizzare i report da aree di lavoro Power BI condivise, l'app richiede l'autorizzazione **Workspace.Read.All**. Per ulteriori informazioni, vedi [Registrazione di [!INCLUDE[prod_short](includes/prod_short.md)] locale in Microsoft Entra ID per l'integrazione con altri servizi](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Se la distribuzione utilizza l'autenticazione NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] si connette allo stesso servizio Power BI per tutti gli utenti. Specificare questo account di servizio come parte della registrazione dell'applicazione. Con l'autenticazione Microsoft Entra, [!INCLUDE[prod_short](includes/prod_short.md)] si connette al servizio Power BI associato ai singoli account utente.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Effettuare la connessione iniziale da Business Central a Power BI.

    Affinché gli utenti finali possano utilizzare Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], un amministratore dell'applicazione Azure dovrà concedere l'autorizzazione al servizio Power BI.

    Per effettuare la connessione iniziale, apri [!INCLUDE[prod_short](includes/prod_short.md)] ed esegui **Introduzione a Power BI** dalla home page. In questo modo, verrà avviato il processo di autorizzazione e verrà controllata la licenza di Power BI. Quando richiesto, accedi utilizzando un account amministratore di Microsoft Entra. Per ulteriori informazioni, vedere [Connettersi a Power BI- una sola volta](across-working-with-powerbi.md#connect).

## Creare report di Power BI per visualizzare i dati di [!INCLUDE [prod_long](includes/prod_long.md)]

È possibile rendere disponibili i dati di Dynamics 365 Business Central come origine di dati in Power BI Desktop e sviluppare report efficaci dello stato dell'attività.

Utilizza Power BI Desktop per creare report che visualizzano dati di Dynamics 365 Business Central. Dopo aver creato i report, è possibile pubblicarli nel servizio Power BI o condividerli con tutti gli utenti dell'organizzazione. Una volta che questi report sono nel servizio Power BI, gli utenti configurati per il suo utilizzo possono quindi visualizzare i report in Dynamics 365 Business Central.

- Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, ottenere le seguenti informazioni:

  - L'URL OData per [!INCLUDE[prod_short](includes/prod_short.md)].
  
    In genere, questo URL ha il formato `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, per esempio `https://localhost:7048/BC190/ODataV4`. Se si dispone di una distribuzione multi-tenant, includere il tenant nell'URL, ad esempio `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Un nome utente e una chiave di accesso al servizio Web di un account [!INCLUDE[prod_short](includes/prod_short.md)].

    Per ottenere dati da [!INCLUDE[prod_short](includes/prod_short.md)], Power BI utilizza l'autenticazione di base. Quindi, sono necessari un nome utente e una chiave di accesso al servizio web per la connessione. L'account potrebbe essere l'account utente oppure l'organizzazione potrebbe avere un account specifico per questo scopo.

## <a name="getdata"></a>Aggiungi [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop

La prima attività della creazione di report è aggiungere [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop. Una volta connesso, è possibile iniziare a creare il report.

1. Avviare Power BI Desktop.
2. Selezionare **Ottieni dati**.

    Se **Ottieni dati** non è visibile, selezionare il menu **File**, quindi **Ottieni dati**.
3. Nella pagina **Ottieni dati** selezionare **Servizi online**.
4. Nel riquadro **Servizi online**, connettiti a [!INCLUDE [prod_short](includes/prod_short.md)] locale, seleziona **Dynamics 365 Business Central (locale)** e quindi **Connetti**.
5. Accedi a [!INCLUDE [prod_short](includes/prod_short.md)] (una sola volta).

    Se non hai mai effettuato l'accesso a [!INCLUDE [prod_short](includes/prod_short.md)] dal Power BI desktop prima, ti viene chiesto di accedere.

   - Per [!INCLUDE [prod_short](includes/prod_short.md)] locale, inserisci prima l'URL OData per [!INCLUDE[prod_short](includes/prod_short.md)], quindi seleziona **OK**. Quando richiesto, immetti il nome utente e la password dell'account da utilizzare per la connessione a [!INCLUDE[prod_short](includes/prod_short.md)]. Nella casella **Password**, immettere la chiave di accesso del servizio web. Al termine, seleziona **Connetti**.
   
    > [!NOTE]  
    > Una volta eseguita la connessione a [!INCLUDE[prod_short](includes/prod_short.md)], non verrà richiesto nuovamente di eseguire l'accesso. [Come posso modificare o cancellare l'account che sto utilizzando attualmente per connettermi a Business Central da Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Una volta connesso, Power BI contatta il servizio Business Central. La finestra dello **strumento di navigazione** viene visualizzata con le origini dati disponibili per la creazione di report. Seleziona una cartella per espanderla e vedere le origini dati disponibili. 

   Le origini dati, indicano tutti i servizi Web e le pagine API pubblicati per [!INCLUDE [prod_short](includes/prod_short.md)]. Le origini dati sono raggruppate per ambienti e società di Business Central.

   > [!NOTE]
    > La struttura per Business Central locale è diversa perché non supporta le pagine API.

7. Seleziona una o più origini dati che vuoi aggiungere al modello dati quindi scegli il pulsante **Carica**.
8. Se in seguito vuoi aggiungere altri dati di Business Central, puoi ripetere i passaggi precedenti.

Dopo che i dati sono stati caricati puoi vederli nel riquadro di spostamento destro nella pagina. A questo punto, è stata stabilita correttamente la connessione ai dati di [!INCLUDE[prod_short](includes/prod_short.md)] ed è possibile iniziare a creare il report di Power BI.  

> [!TIP]
> Per ulteriori informazioni sull'uso di Power BI Desktop, vedere [Introduzione a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## Gestire e modificare i report

> [!NOTE]
> Non puoi gestire e modificare i report. 

## Caricare i report

Per [!INCLUDE [prod_short](includes/prod_short.md)] locale, non sono disponibili report demo, quindi dovrai iniziare da zero utilizzando Power BI Desktop. In alternativa, i report Power BI possono essere distribuiti come file che puoi caricare direttamente dal servizio online Power BI. Per ulteriori informazioni, vedere [Caricare il report nel servizio](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## Vedere anche

[Business Central e Power BI](admin-powerbi.md)  
[Caricare i report](across-working-with-business-central-in-powerbi.md#upload-reports)
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
