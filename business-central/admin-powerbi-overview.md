---
title: Componente di integrazione Power BI e panoramica dell'architettura per Business Central | Microsoft Docs
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
ms.openlocfilehash: 23a0c72775dbddc89a81105de3b2ed79d1f09432
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753772"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prod_short](includes/prod_short.md)]

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
|App Power BI in Microsoft AppSource|Online.|

## <a name="architecture"></a>Architettura

[!INCLUDE[prod_short](includes/prod_short.md)] si integra con Power BI tramite un connettore utilizzando OData. L'origine dati per i report Power BI è esposta come servizi web OData.

![Architettura Power BI per l'integrazione con Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Flusso generale

Il diagramma seguente illustra il flusso di lavoro di base per gli utenti durante la connessione di [!INCLUDE[prod_short](includes/prod_short.md)] a Power BI.

![Flusso di lavoro Power BI per l'integrazione con Business Central](./media/power-bi-flow.png)

1. L'utente si iscrive per un account Power BI.
2. L'utente si connette a Power BI da [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] verifica la licenza.
4. [!INCLUDE[prod_short](includes/prod_short.md)] distribuisce report predefiniti al servizio Power BI. Questo passaggio avviene solo per [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] rende i report in Power BI disponibili per la selezione in [!INCLUDE[prod_short](includes/prod_short.md)]. I report predefiniti vengono visualizzati automaticamente nelle parti Power BI.
6. L'utente crea un report in Power BI Desktop.
7. L'utente pubblica il report nel servizio Power BI. I report diventano anche disponibili per la selezione in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Central e Power BI](admin-powerbi.md)  
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