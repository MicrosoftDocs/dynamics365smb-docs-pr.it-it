---
title: Componente di integrazione Power BI e panoramica dell'architettura per Business Central | Microsoft Docs
description: Scopri i diversi aspetti dell'integrazione Power BI con Business Central.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.reviewer: bholtorf
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="power-bi-integration-component-and-architecture-overview-for-"></a>Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prod_short](includes/prod_short.md)]

In questo articolo vengono descritti i diversi aspetti dell'integrazione Power BI con [!INCLUDE[prod_short](includes/prod_short.md)] per comprenderne l'implementazione e l'utilizzo.

## <a name="components"></a>Componenti

La tabella seguente descrive i principali componenti coinvolti nell'integrazione Power BI.

|Componente|Descrizione|
|---------|-----------|
|Power BI|Un servizio di hosting e gestione di report basato su cloud.|
|Power BI Desktop|Uno strumento per la creazione di report e dashboard e consente di eseguire report. È disponibile come download gratuito su Microsoft Store e viene installato localmente.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Soluzione online o locale con connettori esposti a Power BI e la capacità di incorporare una parte Power BI.|

## <a name="whats-available-from-the-start"></a>Cosa è disponibile dall'inizio

Nella seguente tabella vengono illustrate le funzionalità disponibili.

|Funzionalità|Supporto [!INCLUDE[prod_short](includes/prod_short.md)] online o locale|
|-------|---------------------|
|Connettori Power BI|Entrambe. Connettori diversi per online e locale. Stesso connettore utilizzato per Power BI Desktop e il servizio Power BI |
|Esperienza incorporata per la visualizzazione di un determinato report all'interno di un riquadro Dettaglio informazioni in [!INCLUDE[prod_short](includes/prod_short.md)]|Entrambe. Richiede la configurazione per visualizzare i report in locale.|
|Gestione dei report Power BI da [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Report Power BI predefiniti nella Gestione ruolo utente distribuiti a Power BI|Online|
|App Power BI in Microsoft AppSource|Online|

## <a name="architecture"></a>Architettura

[!INCLUDE[prod_short](includes/prod_short.md)] si integra con Power BI tramite un connettore utilizzando OData. L'origine dati per i report Power BI è esposta come pagine API e servizi web OData.

:::image type="content" source="./media/power-bi-architecture.svg" alt-text="Testo alternativo immagine." lightbox="./media/power-bi-architecture.svg":::

A partire da febbraio 2022, i report Power BI per [!INCLUDE[prod_short](includes/prod_short.md)] online provengono da una replica del database di sola lettura secondaria. La replica del database fa parte della funzionalità [scalabilità orizzontale in lettura](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in [!INCLUDE[prod_short](includes/prod_short.md)] online. Questa configurazione libera il database principale per le transazioni, migliorando le prestazioni del sistema. La connessione alla replica del database di sola lettura è parte integrante del connettore di Business Central online e non richiede alcuna configurazione aggiuntiva da parte dell'utente. Tutti i nuovi report si collegheranno alla replica del database di sola lettura per impostazione predefinita. I vecchi report continueranno a utilizzare il database principale. Per ulteriori informazioni, vedi [Piano del secondo ciclo di rilascio del 2021 di Business Central](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

## <a name="general-flow"></a>Flusso generale

Il diagramma seguente illustra il flusso di lavoro di base per gli utenti durante la connessione di [!INCLUDE[prod_short](includes/prod_short.md)] a Power BI.

![Flusso di lavoro Power BI per l'integrazione con Business Central.](./media/power-bi-flow-v2.svg)

1. L'utente si iscrive per un account Power BI.
2. L'utente si connette a Power BI da [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] verifica la licenza.
4. [!INCLUDE[prod_short](includes/prod_short.md)] distribuisce report predefiniti al servizio Power BI. Questo passaggio avviene solo per [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] rende i report in Power BI disponibili per la selezione in [!INCLUDE[prod_short](includes/prod_short.md)]. I report predefiniti vengono visualizzati automaticamente nelle parti Power BI.
6. L'utente crea un report in Power BI Desktop.
7. L'utente pubblica il report nel servizio Power BI. I report diventano anche disponibili per la selezione in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Vedi anche

[Business Central e Power BI](admin-powerbi.md)  
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
