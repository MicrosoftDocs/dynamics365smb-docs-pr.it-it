---
title: Introduzione a Business Central e Power BI
description: 'Ottenere una panoramica dell''utilizzo di Power BI per avere informazioni dettagliate, business intelligence e KPI dai dati di Business Central.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: edupont
ms.date: 08/30/2022
ms.author: jswymer
---
# Introduzione a [!INCLUDE[prod_short](includes/prod_short.md)] e Power BI

Ottenere informazioni dettagliate sui dati [!INCLUDE[prod_short](includes/prod_short.md)] è facile con [Power BI](https://powerbi.microsoft.com), un sistema di visualizzazione dei dati di Microsoft. Power BI recupera i dati [!INCLUDE[prod_short](includes/prod_short.md)] che consentono di creare dashboard e report basati sui dati. Power BI fornisce un'alternativa flessibile ai report integrati in [!INCLUDE[prod_short](includes/prod_short.md)], consentendo di eseguire il drill-down e personalizzare la visualizzazione e persino unire i dati di diverse società in [!INCLUDE[prod_short](includes/prod_short.md)] Alcuni report Power BI possono anche essere incorporati in Business Central e visualizzati senza lasciare il sistema. I dashboard più complessi sono meglio utilizzati nel sito web Power BI.

![Power BI e Business Central.](media/power-bi-intro.png)

## Operazioni che è possibile eseguire con Power BI e [!INCLUDE[prod_short](includes/prod_short.md)]

Ci sono varie funzionalità da utilizzare con [!INCLUDE[prod_short](includes/prod_short.md)] e Power BI. Alcune cose possono essere eseguite in Power BI, mentre altre vengono fatte da [!INCLUDE[prod_short](includes/prod_short.md)]. Inoltre, alcune funzionalità sono disponibili solo con [!INCLUDE[prod_short](includes/prod_short.md)] online e non in locale. La tabella seguente offre una panoramica.

|Funzionalità|Descrizione|Online|Locale|Ulteriori informazioni|
|-------|-----------|--------------|-----------|----------------|
|Visualizzare dati [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI|È possibile visualizzare i dati da [!INCLUDE[prod_short](includes/prod_short.md)] nei report in Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online include alcuni report Power BI predefiniti. Oppure l'organizzazione potrebbe aver reso disponibili alcuni report personalizzati.|![Funziona online.](media/check.png)|![Funziona in locale](media/check.png)|[Qui...](across-working-with-business-central-in-powerbi.md)|
|Visualizzare report Power BI nel client [!INCLUDE[prod_short](includes/prod_short.md)].| I report Power BI che visualizzano dati [!INCLUDE[prod_short](includes/prod_short.md)] possono essere incorporati direttamente nelle pagine [!INCLUDE[prod_short](includes/prod_short.md)] delle parti. È possibile cambiare la parte per visualizzare qualsiasi report reso disponibile. |![disponibile online.](media/check.png)|![Funziona in locale](media/check.png)<sup>[*](#onprem)</sup>|[Qui...](across-working-with-powerbi.md).|
|Creare report e dashboard in Power BI che visualizzano dati [!INCLUDE[prod_short](includes/prod_short.md)].|Usare Power BI Desktop per creare report e dashboard personalizzati. È possibile pubblicare i report nel servizio Power BI o condividerli con altri utenti dell'organizzazione.|![Funziona online.](media/check.png)|![funziona in locale](media/check.png)|[Qui...](across-how-use-financials-data-source-powerbi.md)|
|App [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] pubblica tre app per Power BI in Microsoft AppSource. Queste app creano report e dashboard dettagliati nel servizio Power BI per la visualizzazione dei dati [!INCLUDE[prod_short](includes/prod_short.md)]. Le app disponibili includono: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Funziona online.](media/check.png)||[Qui...](across-powerbi-business-central-apps.md)|
|Lavorare con i dati [!INCLUDE [prod_short](includes/prod_short.md)] in datamart e nei flussi di dati|A partire da luglio 2022 è possibile utilizzare il connettore [!INCLUDE [prod_short](includes/prod_short.md)] in Power Query Online nei flussi di dati che condividi tra diversi report e dashboard.|[Qui...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a>Questa funzione richiede un'applicazione registrata per Business Central in Microsoft Azure. Per ulteriori informazioni, vedere [Registrazione di Business Central locale in Azure AD per l'integrazione con altri servizi](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## Preparati all'uso di Power BI

Ci sono alcune attività che devono essere eseguite prima di poter iniziare a utilizzare Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]. <!-- Some of the tasks are typically only done by administrators or super users.--> Le attività dipenderanno dal tuo ruolo nella tua organizzazione e da cosa vuoi fare con Power BI:

- Come *utente aziendale*, vuoi vedere i report Power BI sia nel servizio Power BI sia in Business Central
- Come *amministratore*, sei responsabile della gestione delle impostazioni a livello di organizzazione che controllano come funzionano Business Central e Power BI.
- Come *creatore di report*, vuoi creare report Power BI personalizzati che puoi condividere con altri utenti.

|Attività|Utente aziendale|Amministratore|Creatore di report|Ulteriori informazioni|
|----|-------------|-------------|-----------------------|----------------|
|Ottenere un account Power BI.|![ancora un altro segno di spunta.](media/check.png)|![è un segno di spunta](media/check.png)|![ancora un segno di spunta](media/check.png)|Vai a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Per accedere per un account utilizzare l'indirizzo e-mail e la password di lavoro. <br /><br/>La registrazione richiede una licenza, ma nella maggior parte dei casi dovrebbe già essere disponibile una licenza gratuita. Per ulteriori informazioni, vedi [Licenze di Power BI](admin-powerbi-setup.md#license).|
|Ottenere Power BI Desktop|||![ancora un segno di spunta.](media/check.png)|Per scaricare, vai su [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Per ulteriori informazioni, vedere [Ottenere Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Esponi i dati di Business Central in Power BI||![è un segno di spunta.](media/check.png)|![ancora un segno di spunta](media/check.png)|[Esporre i dati tramite pagine API o servizi web OData](admin-powerbi-setup.md#exposedata)
|Abilita integrazione di Power BI<br />(solo locale)||![è un segno di spunta.](media/check.png)||[Impostare Business Central locale per l'integrazione con Power BI](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## Vedi il relativo [training Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Vedi anche

[Business Intelligence](bi.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Configurare [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati di Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  
[Documentazione di Power BI](/power-bi/)  
[Che cos'è Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Introduzione ai datamart](/power-bi/transform-model/datamarts/datamarts-overview)  
[Introduzione ai flussi di dati e alla preparazione dei dati self-service](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
