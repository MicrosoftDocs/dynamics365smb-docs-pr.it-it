---
title: Introduzione a Business Central e Power BI | Documenti Microsoft
description: Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con le app Business Central per Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 51c9e2cd05deba5fd8ace46382ebeb4eb41d13ba
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753744"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] e Power BI

Ottenere informazioni dettagliate sui dati [!INCLUDE[prod_short](includes/prod_short.md)] è facile con [Power BI](https://powerbi.microsoft.com) - un sistema di visualizzazione dei dati di Microsoft. Power BI recupera i dati [!INCLUDE[prod_short](includes/prod_short.md)] che consentono di creare dashboard e report basati sui dati. Power BI fornisce un'alternativa flessibile ai report integrati in [!INCLUDE[prod_short](includes/prod_short.md)], consentendo di eseguire il drill-down e personalizzare la visualizzazione e persino unire i dati di diverse società in [!INCLUDE[prod_short](includes/prod_short.md)] Alcuni report Power BI possono anche essere incorporati in Business Central e visualizzati senza lasciare il sistema. I dashboard più complessi sono meglio utilizzati nel sito web Power BI.

![Power BI e Business Central](media/power-bi-intro.png)


## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Operazioni che è possibile eseguire con Power BI e [!INCLUDE[prod_short](includes/prod_short.md)]

Ci sono varie funzionalità da utilizzare con [!INCLUDE[prod_short](includes/prod_short.md)] e Power BI. Alcune cose possono essere eseguite in Power BI, mentre altre vengono fatte da [!INCLUDE[prod_short](includes/prod_short.md)]. Inoltre, alcune funzionalità sono disponibili solo con [!INCLUDE[prod_short](includes/prod_short.md)] online e non in locale. La tabella seguente offre una panoramica.

|Funzionalità|Descrizione|Online|Locale|Ulteriori informazioni|
|-------|-----------|--------------|-----------|----------------|
|Visualizzare dati [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI|È possibile visualizzare i dati da [!INCLUDE[prod_short](includes/prod_short.md)] nei report in Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online include alcuni report Power BI predefiniti. Oppure l'organizzazione potrebbe aver reso disponibili alcuni report personalizzati.|![Funziona online](media/check.png)|![Funziona in locale](media/check.png)|[Vedere...](across-working-with-powerbi.md)|
|Visualizzare report Power BI nel client [!INCLUDE[prod_short](includes/prod_short.md)].| I report Power BI che visualizzano dati [!INCLUDE[prod_short](includes/prod_short.md)] possono essere incorporati direttamente nelle pagine [!INCLUDE[prod_short](includes/prod_short.md)] delle parti. È possibile cambiare la parte per visualizzare qualsiasi report reso disponibile. |![funziona online](media/check.png)|![Funziona in locale](media/check.png)<sup>[*](#onprem)</sup>|[Vedere...](across-working-with-business-central-in-powerbi.md).|
|Creare report e dashboard in Power BI che visualizzano dati [!INCLUDE[prod_short](includes/prod_short.md)].|Usare Power BI Desktop per creare report e dashboard personalizzati. È possibile pubblicare i report nel servizio Power BI o condividerli con altri utenti dell'organizzazione.|![Funziona online](media/check.png)|![funziona in locale](media/check.png)|[Vedere...](across-how-use-financials-data-source-powerbi.md)
|App [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] pubblica tre app per Power BI in Microsoft AppSource. Queste app creano report e dashboard dettagliati nel servizio Power BI per la visualizzazione dei dati [!INCLUDE[prod_short](includes/prod_short.md)]. Le app disponibili includono: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Funziona online](media/check.png)||[Vedere...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a>Questa funzione richiede un'applicazione registrata per Business Central in Microsoft Azure. Per ulteriori informazioni, vedere [Registrazione di Business Central locale in Azure AD per l'integrazione con altri servizi](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Prepararsi all'uso di Power BI

Ci sono alcune attività che devono essere eseguite prima di poter iniziare a utilizzare Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]. Alcune delle attività vengono in genere eseguite solo da amministratori o super user.

1. Se si sta usando [!INCLUDE[prod_short](includes/prod_short.md)] locale, assicurarsi che la distribuzione soddisfi i requisiti delineati in [Impostare [!INCLUDE[prod_short](includes/prod_short.md)] in locale per l'integrazione di Power BI](admin-powerbi-setup.md#setup). Questa attività è in genere amministrativa.

2. Pubblicare i dati come servizi Web.

    Codeunit, pagine e query da utilizzare come origine dati nei report Power BI devono essere pubblicati come servizi web. Ci sono molti servizi web pubblicati per impostazione predefinita. Un modo agevole di individuare i *servizi Web* consiste nel cercarli in [!INCLUDE[prod_short](includes/prod_short.md)].
    
    Per ulteriori informazioni sulla pubblicazione di servizi Web, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

3. Ottenere un account Power BI.

    Per fare qualsiasi cosa con Power BI e [!INCLUDE[prod_short](includes/prod_short.md)], che si sia un amministratore o solo un consumatore, è necessario un account del servizio Power BI. Per ottenere un account, andare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Per accedere per un account utilizzare l'indirizzo e-mail e la password di lavoro. La registrazione richiede una licenza, ma nella maggior parte dei casi dovrebbe già essere disponibile una licenza gratuita. Per ulteriori informazioni, vedere [Licenze Power BI](admin-powerbi-setup.md#license).

4. Se si desidera creare propri report Power BI ottenere Power BI Desktop.

    È possibile scaricare [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Per ulteriori informazioni, vedere [Ottenere Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

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


[!INCLUDE[footer-include](includes/footer-banner.md)]