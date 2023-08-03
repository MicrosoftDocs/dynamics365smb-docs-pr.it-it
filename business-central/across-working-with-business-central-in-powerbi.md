---
title: Utilizzo dei dati di Business Central in Power BI | Microsoft Docs
description: 'Ottenere informazioni dettagliate, business intelligence e KPI dai dati di Business Central utilizzando Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2022
ms.author: jswymer
---
# Utilizzare i dati di [!INCLUDE [prod_short](includes/prod_short.md)] in Power BI

In questo articolo vengono illustrate alcune delle nozioni di base sull'utilizzo di report e dashboard in Power BI che usa [!INCLUDE [prod_short](includes/prod_short.md)] come origine dati. L'articolo discute alcuni aspetti che aiuteranno a iniziare come utente di [!INCLUDE[prod_short](includes/prod_short.md)]. Per le linee guida generali e le istruzioni sull'uso di Power BI, vedi la [documentazione di Power BI per i consumatori](/power-bi/consumer).

## Preparazione

Iscriversi al servizio Power BI. Se non si è già registrati andare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Quando ci si registra, utilizzare un indirizzo e-mail e una password di lavoro.

## Inizia

Una volta che l'account Power BI è disponibile è possibile accedere a [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Il servizio Power BI ospita tutti i report disponibili. Per vedere il report, selezionare **Area di lavoro personale** > **Report**. Quindi selezionare semplicemente il report che si desidera visualizzare.

Con [!INCLUDE[prod_short](includes/prod_short.md)] online, viene automaticamente visualizzata una serie di report predefiniti nell'area di lavoro personale. Se si desidera creare propri report, è possibile utilizzare Power BI Desktop per creare report e quindi pubblicarli nell'area di lavoro. Per ulteriori informazioni, vedere [Introduzione alla creazione di report in Power BI Desktop per visualizzare i dati di [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

Se si sta usando [!INCLUDE[prod_short](includes/prod_short.md)] locale è necessario iniziare da zero utilizzando Power BI Desktop. Facoltativamente, i report Power BI possono essere distribuiti come file, che è possibile caricare.

## Ottenere i dati più recenti

Ogni report Power BI si basa su un set di dati che ottiene i dati dalle origini [!INCLUDE[prod_short](includes/prod_short.md)]. Si desidera assicurarsi che i dati nel report Power BI siano aggiornati con i dati in [!INCLUDE[prod_short](includes/prod_short.md)]. Questo concetto è definito *aggiornamento*.  A seconda di come è stata configurata l'organizzazione Power BI, l'aggiornamento potrebbe non avvenire automaticamente. Esistono due modi per aggiornare i dati: manualmente o pianificando un aggiornamento. L'aggiornamento manuale viene eseguito su richiesta, se necessario. L'aggiornamento pianificato consente di aggiornare automaticamente a intervalli di tempo definiti.

### Aggiornare manualmente

Nel riquadro di spostamento, sotto **Set di dati**, selezionare **Altre opzioni (...)** accanto al set di dati, quindi selezionare **Aggiorna ora**.

### Pianificare un aggiornamento

Nel riquadro di spostamento, sotto Set di dati, selezionare Altre opzioni (...) accanto al set di dati, quindi selezionare **Pianifica aggiornamento**. Compilare le informazioni sotto la sezione **Pianifica aggiornamento** e selezionare **Applica**.

Per ulteriori informazioni, vedere [Configurare l'aggiornamento pianificato](/power-bi/connect-data/refresh-scheduled-refresh)

## <a name="upload"></a>Caricare report da file

I report Power BI possono essere distribuiti tra gli utenti come file .pbix. Se è disponibile un file .pbix è possibile caricare il file in un'area di lavoro. Per caricare un report, procedere nel seguente modo:

1. Nella nuova area di lavoro, selezionare **Ottieni dati**.

2. Nella casella File, selezionare **Ottieni**.

3. Selezionare **File locale**, andare alla posizione in cui è salvato il file e selezionare **Apri**.

Per ulteriori informazioni, vedere [Caricare il report nel servizio](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Il caricamento di un report richiede la presenza di un'area di lavoro con [capacità premium](/power-bi/service-premium-what-is). Per ulteriori informazioni, vedere [Gestione delle capacità premium](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> Se si sta usando [!INCLUDE[prod_short](includes/prod_short.md)] online, è possibile anche caricare un report da [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Utilizzare i report Power BI in [!INCLUDE [prod_short](includes/prod_short.md)] - Caricare report](across-working-with-powerbi.md#upload).

## <a name="share"></a>Condividere i report con altri

Una volta che un report si trova nell'area di lavoro, è possibile condividerlo con altri nell'organizzazione.

Per condividere un report, in un rapport di elenco o in un rapporto aperto, selezionare **Condividi**. Nel riquadro **Condividi report** immettere gli indirizzi e-mail completi delle persone o dei gruppi di distribuzione con cui si desidera condividere. Seguire le istruzioni sullo schermo per completare la condivisione. Per ulteriori informazioni, vedere [Condividere una dashboard o un report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> È necessario avere una [licenza Power BI Pro](/power-bi/service-features-license-type) per se e per le persone con cui si condivide. Il contenuto deve trovarsi in un'area di lavoro con una [capacità premium](/power-bi/service-premium-what-is). Per ulteriori informazioni, vedere [In che modo condividere il tuo lavoro in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## Vedi il relativo [training Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Vedi anche

[Business Central e Power BI](admin-powerbi.md)  
[Creazione di report di Power BI per visualizzare i dati di [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
[Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Utilizzare i report Power BI in [!INCLUDE [prod_short](includes/prod_short.md)]](across-working-with-powerbi.md)  
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
