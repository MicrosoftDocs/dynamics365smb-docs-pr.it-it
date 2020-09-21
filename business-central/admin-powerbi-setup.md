---
title: Abilitazione dell'integrazione Power BI con Business Central | Microsoft Docs
description: Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con le app Business Central per Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 92b3bb1d04c58332db20c978928fe1b04ed2ab37
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697775"
---
# <a name="enabling-power-bi-integration-with-prodshort"></a>Abilitazione dell'integrazione Power BI con [!INCLUDE[prodshort](includes/prodshort.md)]

Questo articolo descrive come preparare [!INCLUDE[prodshort](includes/prodshort.md)] per l'integrazione con Power BI. [!INCLUDE[prodshort](includes/prodshort.md)] online è già abilitato per l'integrazione, sebbene ci siano alcune informazioni sulle licenze che si potrebbe voler leggere. Per [!INCLUDE[prodshort](includes/prodshort.md)] locale sarà stato configurato l'ambiente a cui connettere Power BI prima che gli utenti possano lavorarci.

## <a name="power-bi-licensing"></a><a name="license"></a>Licenze Power BI

Con [!INCLUDE[prodshort](includes/prodshort.md)], gli utenti ottengono una licenza Power BI che fornisce l'accesso alle funzionalità più comuni in [!INCLUDE[prodshort](includes/prodshort.md)] e Power BI. È anche possibile acquistare una licenza Power BI Pro che fornisce accesso a funzionalità aggiuntive. La tabella seguente fornisce una panoramica delle funzionalità disponibili con ciascuna licenza.

|Licenza Power|Visualizzare report|Creare report|Condividere report|Aggiornare report| App [!INCLUDE[prodshort](includes/prodshort.md)]|
|-------------|--------||
|Power BI gratuito|![selezionato](media/check.png)|![selezionato](media/check.png)|(limitato)|(limitato)||
|Power BI Pro|![selezionato](media/check.png)|![selezionato](media/check.png)|![selezionato](media/check.png)|(esteso)|![selezionato](media/check.png)|

Per ulteriori informazioni, vedere [Concedere in licenza il servizio Power BI per gli utenti dell'organizzazione](/power-bi/admin/service-admin-licensing-organization) o [Iscriversi al servizio Power BI come utente singolo](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prodshort-on-premises-for-power-bi-integration"></a><a name="setup"></a>Configurare [!INCLUDE[prodshort](includes/prodshort.md)] locale per l'integrazione Power BI

Questa sezione spiega i requisiti per una distribuzione di [!INCLUDE[prodshort](includes/prodshort.md)] locale da integrare con Power BI.

1. I servizi Web OData e l'endpoint ODataV4 sono abilitati.

    Il servizio Web OData deve essere abilitato in [!INCLUDE[server](includes/server.md)] e la porta OData aperta nel firewall. Per ulteriori informazioni, vedere [Configurazione di Business Central Server - Servizi Web OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Il server locale deve essere accessibile da Internet.

2. Gli account utente [!INCLUDE[prodshort](includes/prodshort.md)] dispongono di una chiave di accesso al servizio Web.

    È necessaria una chiave di accesso al servizio Web per visualizzare i dati [!INCLUDE[prodshort](includes/prodshort.md)] in Power BI. È possibile assegnare una chiave di accesso al servizio Web a ciascun account utente. In alternativa, creare un account specifico con una chiave di accesso al servizio Web utilizzabile da tutti gli utenti. Per ulteriori informazioni, vedere [Autenticazione dei servizi Web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. L'autenticazione NavUserPassword o Azure Active Directory è configurata.

4. Per visualizzare i report Power BI incorporati nelle pagine [!INCLUDE[prodshort](includes/prodshort.md)] è necessario registrare un'applicazione per [!INCLUDE[prodshort](includes/prodshort.md)] in Microsoft Azure.

    L'applicazione registrata richiede l'autorizzazione per i servizi Power BI. Per ulteriori informazioni, vedere [Registrazione di [!INCLUDE[prodshort](includes/prodshort.md)] locale in Azure AD per l'integrazione con altri servizi](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Se la distribuzione utilizza l'autenticazione NavUserPassword, [!INCLUDE[prodshort](includes/prodshort.md)] si connette allo stesso servizio Power BI per tutti gli utenti. Specificare questo account di servizio come parte della registrazione dell'applicazione. Con l'autenticazione Azure AD, [!INCLUDE[prodshort](includes/prodshort.md)] si connette al servizio Power BI associato ai singoli account utente.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Pubblicare i dati come servizi Web

Codeunit, pagine e query da utilizzare come origine dati nei report Power BI devono essere pubblicati come servizi web. Ci sono molti servizi web pubblicati per impostazione predefinita. Un modo agevole di individuare i *servizi Web* consiste nel cercarli in [!INCLUDE[prodshort](includes/prodshort.md)]. Nella pagina **Servizi web**, assicurarsi che il campo **Pubblica** sia selezionato per i servizi web elencati sopra. Questa attività è in genere amministrativa.

Per ulteriori informazioni sulla pubblicazione di servizi Web, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

> [!TIP]
> Per informazioni su cosa è possibile fare per garantire le migliori prestazioni dei servizi Web, come visto dal Business Central Server (l'endpoint) e dal consumatore (il client), leggere [Scrittura di servizi Web efficienti](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Central e Power BI](admin-powerbi.md)  
[Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Power BI per i consumatori](/power-bi/consumer/end-user-consumer)  
[Il "nuovo look" del servizio Power BI](/power-bi/service-new-look)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentazione di Power BI](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
