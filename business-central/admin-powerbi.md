---
title: Introduzione a Business Central e Power BI
description: 'Ottenere una panoramica dell''utilizzo di Power BI per avere informazioni dettagliate, business intelligence e KPI dai dati di Business Central.'
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 04/24/2024
ms.author: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Introduzione a Business Central e Power BI

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Ottenere informazioni dettagliate sui dati [!INCLUDE[prod_short](includes/prod_short.md)] è facile con [Power BI](https://powerbi.microsoft.com), un sistema di visualizzazione dei dati di Microsoft. Power BI recupera i dati [!INCLUDE[prod_short](includes/prod_short.md)] che consentono di creare dashboard e report basati sui dati. Power BI fornisce un'alternativa flessibile ai report integrati in [!INCLUDE[prod_short](includes/prod_short.md)], consentendo di eseguire il drill-down e personalizzare la visualizzazione e persino unire i dati di diverse società in [!INCLUDE[prod_short](includes/prod_short.md)] Alcuni report Power BI possono anche essere incorporati in Business Central e visualizzati senza lasciare il sistema. I dashboard più complessi sono meglio utilizzati nel sito web Power BI.

![Power BI e Business Central.](media/power-bi-intro.png)

## Cosa puoi fare con Power BI e Business Central

Ci sono varie funzionalità da utilizzare con [!INCLUDE[prod_short](includes/prod_short.md)] e Power BI. Alcune cose possono essere eseguite in Power BI, mentre altre vengono fatte da [!INCLUDE[prod_short](includes/prod_short.md)]. Inoltre, alcune funzionalità sono disponibili solo con [!INCLUDE[prod_short](includes/prod_short.md)] online e non in locale. La tabella seguente offre una panoramica.

|Funzionalità|Descrizione|Online|Locale|Ulteriori informazioni|
|-------|-----------|--------------|-----------|----------------|
|Visualizzare dati [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI|È possibile visualizzare i dati da [!INCLUDE[prod_short](includes/prod_short.md)] nei report in Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online include alcuni report Power BI predefiniti. Oppure l'organizzazione potrebbe aver reso disponibili alcuni report personalizzati.|![Funziona online.](media/check.png)|![Funziona in locale](media/check.png)|[Qui...](across-working-with-powerbi.md)|
|Visualizzare report Power BI nel client [!INCLUDE[prod_short](includes/prod_short.md)].| I report Power BI che visualizzano dati [!INCLUDE[prod_short](includes/prod_short.md)] possono essere incorporati direttamente nelle pagine [!INCLUDE[prod_short](includes/prod_short.md)] delle parti. È possibile cambiare la parte per visualizzare qualsiasi report reso disponibile. |![disponibile online.](media/check.png)|![Funziona in locale](media/check.png)<sup>[*](#onprem)</sup>|[Qui...](across-working-with-powerbi.md).|
|Creare report e dashboard in Power BI che visualizzano dati [!INCLUDE[prod_short](includes/prod_short.md)].|Usare Power BI Desktop per creare report e dashboard personalizzati. È possibile pubblicare i report nel servizio Power BI o condividerli con altri utenti dell'organizzazione.|![Funziona online.](media/check.png)|![funziona in locale](media/check.png)|[Qui...](across-how-use-financials-data-source-powerbi.md)|
|App [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] pubblica tre app per Power BI in Microsoft AppSource. Queste app creano report e dashboard dettagliati nel servizio Power BI per la visualizzazione dei dati [!INCLUDE[prod_short](includes/prod_short.md)]. Le app disponibili includono: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Funziona online.](media/check.png)||[Qui...](across-powerbi-business-central-apps.md)|
|Lavorare con i dati [!INCLUDE [prod_short](includes/prod_short.md)] in datamart e nei flussi di dati|A partire da luglio 2022 è possibile utilizzare il connettore [!INCLUDE [prod_short](includes/prod_short.md)] in Power Query Online nei flussi di dati che condividi tra diversi report e dashboard.|![disponibile online.](media/check.png)||[Qui...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a>Questa funzione richiede un'applicazione registrata per Business Central in Microsoft Azure. Per ulteriori informazioni, vedi [Registrazione di Business Central locale in Microsoft Entra ID per l'integrazione con altri servizi](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

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
|Abilita integrazione di Power BI<br />(solo locale)||![è un segno di spunta.](media/check.png)||[Impostare Business Central locale per l'integrazione con Power BI](across-working-with-business-central-in-powerbi.md#setup)|

## Tieni traccia dei tuoi indicatori KPI aziendali con le metriche Power BI

Se utilizzi Power BI su dati [!INCLUDE[prod_short](includes/prod_short.md)], è facile tenere traccia degli indicatori KPI o delle metriche importanti per te. 

Con le metriche in Power BI, puoi curare le tue metriche e monitorarle rispetto ai principali obiettivi aziendali, in un unico riquadro. Questa funzionalità migliora la cultura dei dati promuovendo responsabilità, allineamento e visibilità per i team e le iniziative all'interno delle organizzazioni. 

Segui questa procedura in quattro passaggi per configurare le metriche Power BI:

1. Crea una scorecard nel servizio Power BI. Scopri di più su [Crea scorecard in Power BI](/power-bi/create-reports/service-goals-create).  
2. Aggiungi le _metriche_ che desideri monitorare connettendoti al tuo report Power BI sulla telemetria. Ulteriori informazioni in [Creare metriche connesse](/power-bi/create-reports/service-goals-create-connected).  
3. Per aggiungere avvisi, definisci le regole di stato per le tue metriche. Ulteriori informazioni in [Creare regole di stato automatizzate per le metriche](/power-bi/create-reports/service-metrics-status-rules).  

    Questo passaggio automatizzerà gli aggiornamenti dello stato in base alle regole che governano quella metrica. Le regole attivano modifiche in base al valore, alla percentuale di obiettivo raggiunto, alle condizioni della data o a una combinazione dei tre, rendendo le regole il più versatili possibile. Per le metriche connesse, queste regole di stato vengono aggiornate ogni volta che vengono aggiornati i dati nella scorecard.
4. Infine, segui le metriche per ricevere avvisi in Teams o tramite e-mail. Scopri di più su [Segui le tue metriche](/power-bi/create-reports/service-metrics-follow).  

Per ulteriori informazioni sulle metriche Power BI, vedi [Introduzione alle metriche in Power BI](/power-bi/create-reports/service-goals-introduction).

> [!NOTE]
> A partire dal secondo ciclo di rilascio di Business Central 2023, è possibile incorporare scorecard da metriche di Power BI in [!INCLUDE[prod_short](includes/prod_short.md)].

## Passaggi successivi

- Se sei un amministratore che deve configurare Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], vai ad [Abilitazione dell'integrazione di Power BI](admin-powerbi-setup.md).
- Se Power BI è già configurato e desideri provare le funzionalità, vai a [Uso dei report Power BI in Business Central](across-working-with-powerbi.md).

## Vedere anche

[Business Intelligence](bi.md)  
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
