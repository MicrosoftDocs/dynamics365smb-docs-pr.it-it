---
title: Abilitazione dell'integrazione di Power BI con Business Central
description: Informazioni su come configurare la connessione a Power Bi in modo da poter ottenere informazioni dettagliate, business intelligence e KPI dai dati di Business Central con le app Business Central per Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: dd0974c20f8c038fcc0cac27c9ef165b2aadcd36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752502"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Abilitazione dell'integrazione Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]

Questo articolo descrive come preparare [!INCLUDE[prod_short](includes/prod_short.md)] per l'integrazione con Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online è già abilitato per l'integrazione, sebbene ci siano alcune informazioni sulle licenze che si potrebbe voler leggere. Per [!INCLUDE[prod_short](includes/prod_short.md)] locale sarà stato configurato l'ambiente a cui connettere Power BI prima che gli utenti possano lavorarci.

## <a name="power-bi-licensing"></a><a name="license"></a>Licenze Power BI

Con [!INCLUDE[prod_short](includes/prod_short.md)], gli utenti ottengono una licenza Power BI che fornisce l'accesso alle funzionalità più comuni in [!INCLUDE[prod_short](includes/prod_short.md)] e Power BI. È anche possibile acquistare una licenza Power BI Pro che fornisce accesso a funzionalità aggiuntive. La tabella seguente fornisce una panoramica delle funzionalità disponibili con ciascuna licenza.

|Licenza Power|Visualizzare report|Creare report|Condividere report|Aggiornare report| App [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI gratuito|![un segno di spunta](media/check.png)|![un altro segno di spunta](media/check.png)|(limitato)|(limitato)||
|Power BI Pro|![ancora un altro segno di spunta](media/check.png)|![è un segno di spunta](media/check.png)|![ancora un segno di spunta](media/check.png)|(esteso)|![ultimo segno di spunta](media/check.png)|

Per ulteriori informazioni, vedere [Concedere in licenza il servizio Power BI per gli utenti dell'organizzazione](/power-bi/admin/service-admin-licensing-organization) o [Iscriversi al servizio Power BI come utente singolo](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Configurare [!INCLUDE[prod_short](includes/prod_short.md)] locale per l'integrazione Power BI

Questa sezione spiega i requisiti per una distribuzione di [!INCLUDE[prod_short](includes/prod_short.md)] locale da integrare con Power BI.

1. I servizi Web OData e l'endpoint ODataV4 sono abilitati.

    Il servizio Web OData deve essere abilitato in [!INCLUDE[server](includes/server.md)] e la porta OData aperta nel firewall. Per ulteriori informazioni, vedere [Configurazione di Business Central Server - Servizi Web OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Il server locale deve essere accessibile da Internet.

2. Gli account utente [!INCLUDE[prod_short](includes/prod_short.md)] dispongono di una chiave di accesso al servizio Web.

    È necessaria una chiave di accesso al servizio Web per visualizzare i dati [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI. È possibile assegnare una chiave di accesso al servizio Web a ciascun account utente. In alternativa, creare un account specifico con una chiave di accesso al servizio Web utilizzabile da tutti gli utenti. Per ulteriori informazioni, vedere [Autenticazione dei servizi Web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. L'autenticazione NavUserPassword o Azure Active Directory è configurata.

4. Per visualizzare i report Power BI incorporati nelle pagine [!INCLUDE[prod_short](includes/prod_short.md)] è necessario registrare un'applicazione per [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    L'applicazione registrata richiede l'autorizzazione per i servizi Power BI. Per ulteriori informazioni, vedere [Registrazione di [!INCLUDE[prod_short](includes/prod_short.md)] locale in Azure AD per l'integrazione con altri servizi](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Se la distribuzione utilizza l'autenticazione NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] si connette allo stesso servizio Power BI per tutti gli utenti. Specificare questo account di servizio come parte della registrazione dell'applicazione. Con l'autenticazione Azure AD, [!INCLUDE[prod_short](includes/prod_short.md)] si connette al servizio Power BI associato ai singoli account utente.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Pubblicare i dati come servizi Web

Codeunit, pagine e query da utilizzare come origine dati nei report Power BI devono essere pubblicati come servizi web. Ci sono molti servizi web pubblicati per impostazione predefinita. Un modo agevole di individuare i *servizi Web* consiste nel cercarli in [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Servizi web**, assicurarsi che il campo **Pubblica** sia selezionato per i servizi web elencati sopra. Questa attività è in genere amministrativa.

Per ulteriori informazioni sulla pubblicazione di servizi Web, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

> [!TIP]
> Per informazioni su cosa è possibile fare per garantire le migliori prestazioni dei servizi Web, come visto dal Business Central Server (l'endpoint) e dal consumatore (il client), leggere [Scrittura di servizi Web efficienti](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Central e Power BI](admin-powerbi.md)  
[Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI per i consumatori](/power-bi/consumer/end-user-consumer)  
[Il "nuovo look" del servizio Power BI](/power-bi/service-new-look)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentazione di Power BI](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Uso di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Uso di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Uso di [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
