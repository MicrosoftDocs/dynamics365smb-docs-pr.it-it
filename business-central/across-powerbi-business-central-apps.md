---
title: Uso delle app Business Central in Power BI | Microsoft Docs
description: Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con le app Business Central per Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 479fa9897d817075aec8d2d6fd9431dbe49ab162
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754319"
---
# <a name="using-the-prod_short-apps-in-power-bi"></a>Utilizzo delle app [!INCLUDE [prod_short](includes/prod_short.md)] in Power BI

> **SI APPLICA A:** [!INCLUDE [prod_long](includes/prod_long.md)] online 

[!INCLUDE [prod_long](includes/prod_long.md)] pubblica le seguenti app Power BI che forniscono dashboard dettagliate per la visualizzazione dei dati:

- [!INCLUDE [prod_long](includes/prod_long.md)] - CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Sales

## <a name="overview"></a>Sintesi

Ogni app include diversi report di cui è possibile approfondire i dati, incluse le seguenti funzionalità:

- Selezionare una qualsiasi visualizzazione nel dashboard per portare in primo piano uno dei report sottostanti.  
- Filtrare il report o aggiungere i campi che si desidera monitorare.  
- Aggiungere una visualizzazione personalizzata al dashboard per continuare la tracciabilità.  
  È possibile aggiornare manualmente i dati e configurare la pianificazione degli aggiornamenti. Per ulteriori informazioni, vedere [Configurazione di aggiornamenti pianificati](/power-bi/refresh-scheduled-refresh)  

Le app sono progettate per l'utilizzo dei dati di qualsiasi società in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando si installa l'app Power BI, si specificano uno o più parametri per la connessione a [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> È inoltre possibile creare i propri report e dashboard in Power BI in base ai dati di [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Collegare i dati aziendali a Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Prerequisiti

Le app Power BI richiedono autorizzazioni per le tabelle da cui vengono recuperati i dati e i servizi Web utilizzati per recuperare i dati. La tabella seguente elenca i servizi Web richiesti per ciascuna app Power BI:
    
|App | Servizi Web|
|----|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Opportunità di vendita</li><li>Modello di Excel Visualizza informazioni società</li><li>Etichette report Power BI</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Finance| <ul><li>PowerBIFinance</li><li>Modello di Excel Visualizza informazioni società</li><li>Etichette report Power BI</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Sales| <ul><li>Vendite articolo per cliente</li><li>Dashboard vendite</li><li>Modello di Excel Visualizza informazioni società</li><li>Etichette report Power BI</li></ul>|

> [!TIP]
> Un modo agevole di individuare i *servizi Web* consiste nel cercarli in [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Servizi web**, assicurarsi che il campo **Pubblica** sia selezionato per i servizi web elencati sopra. Per ulteriori informazioni, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

## <a name="get-ready"></a>Preparazione

Iscriversi al servizio Power BI. Se non si è già registrati andare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Quando ci si registra, utilizzare l'indirizzo e-mail e la password di lavoro.

## <a name="install-a-prod_short-app-in-power-bi"></a>Installare un'app [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI

1. Aprire il browser, passare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com) e accedere al proprio account.
2. Selezionare **Ottieni i dati** nella parte inferiore del riquadro di spostamento sinistro.  

    ![Passare a Ottieni i dati](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    È inoltre possibile iniziare da [!INCLUDE [prod_short](includes/prod_short.md)]. Nella Home page, passare a **Selezione report** nella sezione Power BI. Selezionare **Assistenza** o **Organizzazione personale** dalla barra multifunzione. La raccolta dell'organizzazione in Power BI o Microsoft AppSource si apre, filtrata per visualizzare solo le app relative a [!INCLUDE[prod_short](includes/prod_short.md)].

3. Nella casella **Servizi**, selezionare **Ottieni**.

    Questo passaggio apre la pagina **App Power BI** che consente di cercare l'app Power BI disponibile in **AppSource**.  

4. Nella casella **Cerca** immettere **Dynamics 365 Business Central**.
5. Selezionare l'app che si desidera utilizzare, selezionare **Scarica ora** e poi **Installa**.  

    Al termine, l'app sarà disponibile da **App** nel menu di spostamento in Power BI.

## <a name="connect-the-prod_short-app-to-your-data"></a>Connettere l'app [!INCLUDE[prod_short](includes/prod_short.md)] ai dati

1. In **App**, selezionare l'app Business Central, quindi **Connetti**.
2. Quando richiesto, compilare i campi **Nome società** e **Ambiente** con le informazioni sull'istanza di [!INCLUDE[prod_short](includes/prod_short.md)] a cui ci si desidera connettere.

    - Per **Nome società**, assicurarsi di utilizzare il nome completo, non il nome visualizzato. È possibile trovare Il nome della società nella pagina **Società** in [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Per **Ambiente** se non sono stati creati più ambienti, immettere **Produzione**.

3. Selezionare **Avanti**.
4. Selezionare **Accedi**.
5. Quando richiesto, immettere il nome utente e la password per l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)].
6. Dopo la connessione, un dashboard e i report vengono aggiunti all'area di lavoro Power BI. Al termine, i riquadri visualizzano i dati della società [!INCLUDE[prod_short](includes/prod_short.md)].

    ![Selezionare Dynamics 365 Business Central e quindi Ottienilo ora.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Risolvere i problemi

Il dashboard Power BI si basa sui servizi Web pubblicati che sono elencati sopra. Mostra i dati della società di dimostrazione o della società se si importano i dati dall'attuale soluzione finanziaria. Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.  

### <a name="you-dont-have-a-power-bi-account"></a>Non si dispone di un account Power BI

Un account Power BI non è stato impostato. È necessario avere una licenza per ottenere un account Power BI valido. Inoltre, è necessario aver effettuato l'accesso in precedenza a Power BI per creare l'area di lavoro Power BI.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Messaggio: Non sono presenti report abilitati. Scegliere Seleziona report per visualizzare un elenco di report che è possibile visualizzare.

Questo messaggio viene visualizzato se la distribuzione del report predefinito non è riuscita nell'area di lavoro Power BI. Oppure il report è stato distribuito ma non è stato aggiornato correttamente. Se si verifica questo problema, accedere al report nella propria area di lavoro Power BI, selezionare **Set di dati**, **Impostazioni** e quindi aggiornare manualmente le credenziali. Dopo aver aggiornato correttamente il set di dati, tornare a [!INCLUDE[prod_short](includes/prod_short.md)] e selezionare manualmente il report dalla pagina **Selezionare i report**.

### <a name="you-need-a-power-bi-pro-license-to-install-the-prod_short-app-in-power-bi"></a>È necessaria una licenza Power BI Pro per installare l'app [!INCLUDE[prod_short](includes/prod_short.md)] in Power BI

È necessaria una [licenza Power BI Pro](/power-bi/service-features-license-type) per condividere i contenuti per se e per le persone con cui si condivide. Il contenuto deve trovarsi in un'area di lavoro con una [capacità premium](/power-bi/service-premium-what-is). Per ulteriori informazioni, vedere [In che modo condividere il tuo lavoro in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"La convalida dei parametri non è riuscita. Assicurarsi che tutti i parametri siano validi"

Questo errore indica che uno o più parametri non sono validi.

- Il parametro di ambiente specificato non corrisponde ad alcun ambiente di produzione o sandbox di [!INCLUDE[prod_short](includes/prod_short.md)].
- Il parametro dell'azienda specificato non corrisponde ad alcuna società [!INCLUDE[prod_short](includes/prod_short.md)] esistente. Verificare il nome della società nella pagina **Società** in [!INCLUDE[prod_short](includes/prod_short.md)].
- Se ci si collega a [!INCLUDE[prod_short](includes/prod_short.md)] in locale, è stato immesso un URL non valido. È possibile verificare l'URL nella pagina **Servizi web** in [!INCLUDE[prod_short](includes/prod_short.md)].  
- Una porta non viene aperta per consentire il passaggio della richiesta attraverso il firewall.

### <a name="cant-sign-in"></a>Impossibile accedere

Se viene visualizzato un errore "Accesso non riuscito" dopo l'utilizzo delle credenziali utente di [!INCLUDE[prod_short](includes/prod_short.md)] per eseguire l'accesso, è probabile che si sia verificato uno dei seguenti problemi:

- L'account che si sta utilizzando non dispone delle autorizzazioni per recuperare i dati di [!INCLUDE[prod_short](includes/prod_short.md)] da tale account. Verificare di disporre delle autorizzazioni per i dati richiesti in [!INCLUDE[prod_short](includes/prod_short.md)] e riprovare.
- Si è selezionato un tipo di autenticazione diverso da Base per la connessione a [!INCLUDE[prod_short](includes/prod_short.md)] in locale.
- Non è stato inserito un nome utente o una password validi.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Messaggio: non è possibile aggiornare l'origine dati perché le credenziali non sono valide. Aggiornare le credenziali e riprovare

Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, il problema potrebbe essere che l'URL OData è esposto solo alla rete locale.

### <a name="incorrect-company-name"></a>Nome della società non corretto

Un errore comune consiste nell'immettere il nome visualizzato della società al posto del nome della società. Per individuare il nome della società, cercare **Società**. Quindi utilizzare il campo **Nome** quando si immette il nome della società.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nessuna riga corrispondente alla chiave nella tabella

Se si immette un nome di società non valido durante il processo di connessione, è possibile che sia visualizzato il messaggio di errore "Nessuna riga corrispondente alla chiave nella tabella". Immettere il nome di società corretto e riprovare.

### <a name="historical-data-appears-to-be-missing"></a>Dati storici mancanti

Una volta che l'app Power BI è installata e i dati sono visualizzati in Power BI, è possibile notare che non tutti siano visualizzati. I set di dati vengono filtrati per restituire solo i 365 giorni precedenti dei dati. Questa impostazione predefinita rende più rapida la creazione di report.  

### <a name="i-only-see-data-for-a-single-company"></a>Visualizzazione unicamente dei dati di una singola società

L'app Power BI visualizzerà solo i dati della società [!INCLUDE[prod_short](includes/prod_short.md)] definita all'installazione dell'app Power BI. I dati di altre società possono essere aggiunti ai report aggiungendo nuove query che utilizzano società differenti come origine dati.  

### <a name="what-now"></a>Operazioni successive

- Provare a [porre una domanda nella casella delle domande e risposte](/power-bi/service-q-and-a-tips) nella parte superiore del dashboard.
- [Modificare i riquadri](/power-bi/service-dashboard-edit-tile) nel dashboard.  
- [Selezionare un riquadro](/power-bi/service-dashboard-tiles) per aprire il report sottostante.  
- Per impostazione predefinita, il set di dati non è pianificato per l'aggiornamento. È possibile modificare la pianificazione dell'aggiornamento o eseguire l'aggiornamento su richiesta utilizzando **Aggiorna ora**. Per ulteriori informazioni, vedere [Configurazione di aggiornamenti pianificati](/power-bi/refresh-scheduled-refresh)

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Business Central e Power BI](admin-powerbi.md)  
[Componente di integrazione Power BI e panoramica dell'architettura per [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Utilizzo di dati di [!INCLUDE [prod_short](includes/prod_short.md)] in Power BI](across-working-with-business-central-in-powerbi.md)  
[Creazione di report di Power BI per visualizzare i dati di [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
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