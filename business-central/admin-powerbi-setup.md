---
title: Abilitazione dell'integrazione di Power BI con Business Central
description: Scopri come impostare la connessione a Power BI. Con i report Power BI puoi ottenere informazioni dettagliate, business intelligence e KPI dai dati di Business Central.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, setup, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: c893513098d5078995e6cab09abcf0d2e0bb2769
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950358"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Abilitazione dell'integrazione Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]

Questo articolo descrive come preparare [!INCLUDE[prod_short](includes/prod_short.md)] per l'integrazione con Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online è già abilitato per l'integrazione, sebbene ci siano alcune informazioni sulle licenze che si potrebbe voler leggere. Per [!INCLUDE[prod_short](includes/prod_short.md)] locale sarà stato configurato l'ambiente a cui connettere Power BI prima che gli utenti possano lavorarci.

## <a name="power-bi-licensing"></a><a name="license"></a>Licenze Power BI

Con [!INCLUDE[prod_short](includes/prod_short.md)], gli utenti ottengono una licenza Power BI che fornisce l'accesso alle funzionalità più comuni in [!INCLUDE[prod_short](includes/prod_short.md)] e Power BI. È anche possibile acquistare una licenza Power BI Pro che fornisce accesso a funzionalità aggiuntive. La tabella seguente fornisce una panoramica delle funzionalità disponibili con ciascuna licenza.

|Licenza Power|Visualizzare report|Creare report|Condividere report|Aggiornare report| App [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI gratuito|![un segno di spunta.](media/check.png)|![un altro segno di spunta](media/check.png)|(limitato)|(limitato)||
|Power BI Pro|![ancora un altro segno di spunta.](media/check.png)|![è un segno di spunta](media/check.png)|![ancora un segno di spunta](media/check.png)|(esteso)|![ultimo segno di spunta](media/check.png)|

Per ulteriori informazioni, vedere [Concedere in licenza il servizio Power BI per gli utenti dell'organizzazione](/power-bi/admin/service-admin-licensing-organization) o [Iscriversi al servizio Power BI come utente singolo](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-pages-or-odata-web-services"></a><a name="exposedata"></a>Esporre i dati tramite pagine API o servizi web OData

Business Central offre due modi per esporre i dati che possono essere usati dai report Power BI: pagine API e servizi web Open Data Protocol (OData).

### <a name="api-pages"></a>Pagine API

> **APPLICABILE A:** Solo Business Central Online 

Una pagina API è un tipo di pagina specifico creato nel codice AL che fornisce l'accesso alle tabelle del database tramite un servizio REST supportato da webhook, abilitato per OData v4. Questo tipo di pagina non può essere visualizzato nell'interfaccia utente, ma è destinato alla creazione di servizi di integrazione affidabili.

Business Central online è disponibile con una serie di API integrate, che è possibile utilizzare per ottenere dati per le entità aziendali più comuni, come clienti, articoli, ordini di vendita e altro. Non è richiesto alcun lavoro aggiuntivo o configurazione per utilizzare queste API come origine dati per report Power BI. Per ulteriori informazioni su queste API, vedi [API Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online supporta anche le API personalizzate. Gli sviluppatori di applicazioni delle soluzioni Business Central possono creare le proprie pagine API e comprimerle in estensioni. Puoi installare le estensioni sul tuo tenant. Una volta installate, puoi utilizzare le pagine API per il tuo report Power BI, come faresti con le API integrate (v2.0). Per ulteriori informazioni su come creare pagine API, vedi [Sviluppo di un'API personalizzata](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> A partire da febbraio 2022, i report Power BI per [!INCLUDE[prod_short](includes/prod_short.md)] online provengono da una replica del database di sola lettura secondaria per motivi di prestazioni. Di conseguenza, gli sviluppatori AL dovrebbero evitare di progettare pagine API che apportano modifiche al database mentre le pagine aprono o caricano record. In particolare, considera il codice dei trigger AL: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord e OnAfterGetCurrRecord. Queste modifiche al database, in alcuni casi, possono causare problemi di prestazioni e impedire l'aggiornamento dei dati del report. Per ulteriori informazioni, vedi [Articoli sulle prestazioni per gli sviluppatori](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) nella guida allo sviluppo di Business Central.
>
> In rari casi, il comportamento causerà un errore quando un utente tenta di ottenere dati dalla pagina API per un report in Power BI Desktop. Tuttavia, se sono necessarie modifiche al database nella pagina dell'API personalizzata, gli utenti Power BI Desktop possono forzare il comportamento. Per ulteriori informazioni, vedi [Creare report Power BI per visualizzare i dati di Business Central](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>Servizi Web OData

È possibile pubblicare oggetti dell'applicazione Business Central, come codeunit, pagine e query, come [servizi web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Con Business Central online, sono disponibili molti servizi Web pubblicati per impostazione predefinita. Un modo agevole di individuare i *servizi Web* consiste nel cercarli in [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Servizi web**, assicurarsi che il campo **Pubblica** sia selezionato per i servizi web elencati sopra. Per ulteriori informazioni sulla pubblicazione di servizi Web, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

Per informazioni su cosa è possibile fare per garantire le migliori prestazioni dei servizi Web, come visto dal Business Central Server (l'endpoint) e dal consumatore (il client), leggere [Scrittura di servizi Web efficienti](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Scegliere se utilizzare le pagine API o i servizi web OData

Quando possibile, ti invitiamo a utilizzare le pagine API invece del servizio web OData. Le pagine API sono generalmente più veloci nel caricamento dei dati nei report Power BI rispetto ai servizi Web OData. Inoltre, sono più flessibili perché ti consentono di ottenere dati dai campi della tabella che non sono definiti in un oggetto pagina.

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Configurare [!INCLUDE[prod_short](includes/prod_short.md)] locale per l'integrazione Power BI

Questa sezione spiega i requisiti per una distribuzione di [!INCLUDE[prod_short](includes/prod_short.md)] locale da integrare con Power BI.

1. Configurare NavUserPassword o l'autenticazione di Azure Active Directory per la distribuzione.

    L'integrazione di Power BI non supporta l'autenticazione di Windows.  

2. Abilitare i servizi Web OData e l'endpoint ODataV4.

    Il servizio Web OData deve essere abilitato in [!INCLUDE[server](includes/server.md)] e la porta OData aperta nel firewall. Per ulteriori informazioni, vedere [Configurazione di Business Central Server - Servizi Web OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Il server locale deve essere accessibile da Internet.

3. Concedere agli account utente [!INCLUDE[prod_short](includes/prod_short.md)] una chiave di accesso al servizio Web.

    Una chiave di accesso al servizio Web è necessaria solo per visualizzare i dati di [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI. È possibile assegnare una chiave di accesso al servizio Web a ciascun account utente. In alternativa, creare un account specifico con una chiave di accesso al servizio Web utilizzabile da tutti gli utenti. Per ulteriori informazioni, vedere [Autenticazione dei servizi Web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Creare una registrazione dell'applicazione per [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    Per visualizzare i report Power BI incorporati nelle pagine [!INCLUDE[prod_short](includes/prod_short.md)] è necessario registrare un'applicazione per [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. L'applicazione registrata richiede l'autorizzazione per i servizi Power BI. Come minimo, l'app richiede l'autorizzazione **User.ReadWrite.All**. Per consentire agli utenti di visualizzare i report da aree di lavoro Power BI condivise, l'app richiede l'autorizzazione **Workspace.Read.All**. Per ulteriori informazioni, vedere [Registrazione di [!INCLUDE[prod_short](includes/prod_short.md)] locale in Azure AD per l'integrazione con altri servizi](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Se la distribuzione utilizza l'autenticazione NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] si connette allo stesso servizio Power BI per tutti gli utenti. Specificare questo account di servizio come parte della registrazione dell'applicazione. Con l'autenticazione Azure AD, [!INCLUDE[prod_short](includes/prod_short.md)] si connette al servizio Power BI associato ai singoli account utente.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Effettuare la connessione iniziale da Business Central a Power BI.

    Affinché gli utenti finali possano utilizzare Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], un amministratore dell'applicazione Azure dovrà concedere l'autorizzazione al servizio Power BI.

    Per effettuare la connessione iniziale, aprire [!INCLUDE[prod_short](includes/prod_short.md)] ed eseguire **Introduzione a Power BI** da Gestione ruolo utente. In questo modo, verrà avviato il processo di autorizzazione e verrà controllata la licenza di Power BI. Quando richiesto, accedere utilizzando un account amministratore di Azure. Per ulteriori informazioni, vedere [Connettersi a Power BI- una sola volta](across-working-with-powerbi.md#connect).


## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Central e Power BI](admin-powerbi.md)  
[Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI per i consumatori](/power-bi/consumer/end-user-consumer)  
[Il "nuovo look" del servizio Power BI](/power-bi/service-new-look)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentazione di Power BI](/power-bi/)  
[Business Intelligence](bi.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]