---
title: Abilitare i dati aziendali per Power BI | Microsoft Docs
description: Ottenere informazioni dettagliate, business intelligence e KPI a partire dai dati di Business Central è semplice con le app Business Central per Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: e17485563e331f7e78500650e174f6b2b57bbb8e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307974"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Abilitare i dati aziendali per Power BI 

Ottenere informazioni dettagliate sui dati di [!INCLUDE[prodshort](includes/prodshort.md)] è semplice con le app [!INCLUDE[prodshort](includes/prodshort.md)] per Power BI. Power BI recupera i dati e quindi sviluppa un dashboard e i report pronti per l'uso basati su tali dati.  

È necessario disporre di un account valido con [!INCLUDE[prodshort](includes/prodshort.md)] e con Power BI. Inoltre, è necessario scaricare [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) per creare i propri report Power BI. Le app Power BI richiedono autorizzazioni di accesso alle tabelle da dove vengono recuperati i dati. Più informazioni dettagliate sui requisiti sono descritte di seguito.  

> [!IMPORTANT]
> Le app Power BI descritte in questo articolo sono progettate per utilizzare Azure Active Directory come meccanismo di autenticazione salvo diversa indicazione. Per installare un'app Power BI è necessario disporre anche di una licenza Power BI Pro.  Dopo l'installazione, l'app Power BI può essere condivisa con utenti con qualsiasi tipo di licenza.

[!INCLUDE [prodlong](includes/prodlong.md)] ha pubblicato le seguenti app per Power BI:

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)] (in locale) - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] (in locale) - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] (in locale) - Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>Utilizzo dei dashboard di [!INCLUDE [prodshort](includes/prodshort.md)] in Power BI

Ogni app include report che è possibile analizzare in dettaglio:

- Selezionare una qualsiasi visualizzazione nel dashboard per portare in primo piano uno dei report sottostanti.  
- Filtrare il report o aggiungere i campi che si desidera monitorare.  
- Aggiungere la visualizzazione personalizzata al dashboard per continuare la tracciabilità.  
  È possibile aggiornare manualmente i dati e configurare la pianificazione degli aggiornamenti. Per ulteriori informazioni, vedere [Configurazione di aggiornamenti pianificati](/power-bi/refresh-scheduled-refresh)  

Le app sono progettate per l'utilizzo dei dati di qualsiasi società in [!INCLUDE[prodshort](includes/prodshort.md)]. Quando si installa l'app Power BI, si specificano uno o più parametri per la connessione a [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> È inoltre possibile creare i propri report e dashboard in Power BI in base ai dati di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Collegare i dati aziendali a Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Per connettere i dati in Power BI

1. Aprire il browser, passare a https://powerbi.microsoft.com e accedere al proprio account.
2. Selezionare **Ottieni i dati** nella parte inferiore del riquadro di spostamento sinistro.  

    ![Passare a Ottieni i dati](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    È inoltre possibile iniziare da [!INCLUDE [prodshort](includes/prodshort.md)]. Nella Home page, passare a **Selezione report**nella sezione Power BI. Selezionare **Assistenza** o **Organizzazione personale** dalla barra multifunzione. Quando viene selezionata una di queste azioni, si verrà reindirizzati alla raccolta dell'organizzazione in Power BI o a Microsoft AppSource e le app verranno filtrate per visualizzare solo quelle relative a [!INCLUDE[prodshort](includes/prodshort.md)].

3. Nella casella **Servizi**, selezionare **Ottieni**. Viene visualizzata una pagina che visualizza **AppSource** e **App per Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Selezionare **App** nella scheda **App per Power BI** e scegliere l'app **Microsoft Dynamics 365 Business Central** che si desidera utilizzare e selezionare **Ottienilo ora**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Quando richiesto, immettere il nome dell'ambiente e dell'azienda nell'app [!INCLUDE[prodshort](includes/prodshort.md)] a cui si intende connettersi. Se non sono stati creati più ambienti, immettere **Produzione**. Per il parametro dell'azienda, assicurarsi di inserire il nome e non il nome visualizzato. È possibile trovare Il nome della società nella pagina **Società'** dell'istanza di [!INCLUDE[prodshort](includes/prodshort.md)].  

    > [!NOTE]
    > Se ci si connette a [!INCLUDE [prodshort](includes/prodshort.md)] in locale, è necessario specificare il parametro *URL servizio Web*. Questa parametro è presente nella pagina **Servizi web** in [!INCLUDE [prodshort](includes/prodshort.md)]. L'istanza di [!INCLUDE [server](includes/server.md)] deve essere configurata per l'autenticazione Base ed è necessario specificare un utente e la chiave di accesso Web di quell'utente come password. Nell'esempio seguente, sostituire *myserver: 7048* con il nome [!INCLUDE [server](includes/server.md)] e *CRONUS%20US* con il nome della società.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Dopo la connessione, un dashboard e i report vengono aggiunti all'area di lavoro Power BI. Al termine, i riquadri visualizzano i dati della società [!INCLUDE[prodshort](includes/prodshort.md)].

    ![Selezionare Dynamics 365 Business Central e quindi Ottienilo ora.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Operazioni successive

- Provare a [porre una domanda nella casella delle domande e risposte](/power-bi/service-q-and-a-tips) nella parte superiore del dashboard.
- [Modificare i riquadri](/power-bi/service-dashboard-edit-tile) nel dashboard.  
- [Selezionare un riquadro](/power-bi/service-dashboard-tiles) per aprire il report sottostante.  
- Per impostazione predefinita, il set di dati non è pianificato per l'aggiornamento. È possibile modificare la pianificazione dell'aggiornamento o eseguire l'aggiornamento su richiesta utilizzando **Aggiorna ora**. Per ulteriori informazioni, vedere [Configurazione di aggiornamenti pianificati](/power-bi/refresh-scheduled-refresh)

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI in [!INCLUDE [prodshort](includes/prodshort.md)]

La Home page in [!INCLUDE [prodshort](includes/prodshort.md)] può includere un elemento di controllo Power BI che può essere configurato per la visualizzazione dei report Power BI nella Home page.

> [!IMPORTANT]
> È necessario disporre di un account valido con [!INCLUDE [prodshort](includes/prodshort.md)] e con Power BI. Inoltre, se si desidera modificare qualsiasi report, è necessario scaricare Power BI Desktop. Per ulteriori informazioni, vedere [Uso di Business Central come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Al primo accesso

Quando si esegue il primo accesso a [!INCLUDE [prodshort](includes/prodshort.md)], si noterà che una parte di Power BI nella Home page è vuota. Per visualizzare i report, è necessario innanzitutto connettersi a Power BI selezionando il collegamento *Introduzione a Power BI*.

[!INCLUDE [prodshort](includes/prodshort.md)] comunica quindi con il servizio Power BI per determinare se si dispone di un account Power BI valido. Dopo la verifica della licenza, i report Power BI predefiniti sono visualizzati nella Home page.

### <a name="selecting-power-bi-reports"></a>Selezione di report Power BI

Il controllo Power BI nella Home page può visualizzare qualsiasi report Power BI. Per visualizzare un rapporto esistente, scegliere l'azione **Seleziona report** dall'elenco a discesa Power BI.  

La pagina di selezione dei report mostra un elenco di tutti i report Power BI a cui si ha accesso. Questo elenco viene recuperato dall'area di lavoro Power BI. Abilitare ogni report che si intende visualizzare nella Home page, quindi scegliere OK. Viene visualizzata di nuovo la Home page con l'ultimo report abilitato. Mediante l'elenco a discesa, utilizzare i comandi Precedente e Successivo per spostarsi tra i report.  

### <a name="get-reports"></a>Ottenere i report

Se non è visualizzato alcun report nella pagina Selezionare i report o non è visualizzato il report desiderato, è possibile scegliere di ottenere report da *Organizzazione personale* o *Servizi*.
Scegliere *Organizzazione personale* per accedere ai servizi Power BI dove è possibile visualizzare i report dell'organizzazione per i quali si dispone di diritti di visualizzazione e aggiungerli all'area di lavoro. Scegliere *Servizi* per passare a Microsoft AppSource dove è possibile installare le app Power BI.  

È anche possibile scegliere di creare nuovi report Power BI. Dopo la pubblicazione di questi report nell'area di lavoro Power BI, i report saranno visualizzati in questa pagina.  

### <a name="managing-reports"></a>Gestione di report

Nella sezione Power BI della Home page, è possibile scegliere l'azione **Gestisci report** dall'elenco dei comandi a discesa in modo da poter modificare il report attivo in Gestione ruolo utente.  

Le modifiche possono essere apportate al report e salvate.  Eventuali modifiche apportate al report verranno modificate per qualsiasi utente con cui questo rapporto è condiviso poiché si sta modificando il report archiviato nel servizio Power BI.  

Dopo il completamento delle modifiche, selezionare Salva. Se si tratta di un report condiviso, è possibile selezionare Salva con nome per evitare di apportare questa modifica per tutti gli utenti.
Ritornare a Gestione ruolo utente; il ruolo aggiornato verrà visualizzato. Se si è utilizzato un comando Salva con nome, sarà necessario aprire la pagina Seleziona report e abilitare il nuovo report.

### <a name="uploading-reports"></a>Caricamento dei report

È possibile caricare nuovi report Power BI e condividerli con tutti gli utenti di [!INCLUDE [prodshort](includes/prodshort.md)]. I report sono condivisi in ogni società in [!INCLUDE [prodshort](includes/prodshort.md)].  

Per caricare un report, selezionare l'azione **Carica report** dall'elenco a discesa. È quindi possibile caricare un file .pbix che definisce i report che si desidera condividere. È possibile modificare il nome predefinito del file.  

Una volta che il rapporto è stato caricato nella propria area di lavoro Power BI, viene caricato automaticamente nelle aree di lavoro Power BI di tutti gli altri utenti fino al successivo accesso a [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Requisiti di sistema

Per importare i dati di [!INCLUDE[prodshort](includes/prodshort.md)] in Power BI, è necessario disporre delle autorizzazioni di accesso ai servizi Web utilizzati per recuperare i dati. I servizi Web necessari per ogni app Power BI sono:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central - CRM

- Opportunità di vendita
- Modello di Excel Visualizza informazioni società
- Etichette report Power BI

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central - Finance

- PowerBIFinance
- Modello di Excel Visualizza informazioni società
- Etichette report Power BI

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central - Sales

- Vendite articolo per cliente
- Dashboard vendite
- Modello di Excel Visualizza socetà
- Etichette report Power BI

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] in locale utilizza gli stessi endpoint del servizio Web di [!INCLUDE [prodshort](includes/prodshort.md)] online.

## <a name="web-services"></a>Servizi Web

Un modo agevole di individuare i *servizi Web* consiste nel cercarli in [!INCLUDE[prodshort](includes/prodshort.md)]. Nella pagina **Servizi web**, assicurarsi che il campo **Pubblica** sia selezionato per i servizi web elencati sopra.

## <a name="troubleshooting"></a>Troubleshooting

Il dashboard di Power BI si basa sui servizi Web rilasciati che sono elencati sopra e visualizza i dati della società demo o della società dell'utente se si importano i dati della soluzione finanziario corrente. Tuttavia, se si verifica un errore, in questa sezione viene fornita una soluzione alternativa per i problemi più comuni.  

### <a name="you-do-not-have-a-power-bi-account"></a>Non si dispone di un account Power BI

Un account Power BI non è stato impostato. Per disporre di un account Power BI valido, è necessario avere una licenza e aver effettuato l'accesso a Power BI in precedenza per creare l'area di lavoro Power BI.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Messaggio: Non sono presenti report abilitati. Scegliere Seleziona report per visualizzare un elenco di report che è possibile visualizzare.

Questo messaggio verrà visualizzato se il report predefinito non viene distribuito alla propria area di lavoro Power BI o il report è stato distribuito ma non aggiornato correttamente. In questo caso, accedere al report nella propria area di lavoro Power BI, selezionare **Set di dati**, **Impostazioni** e quindi aggiornare manualmente le credenziali. Dopo aver aggiornato correttamente il set di dati, tornare a Business Central e selezionare manualmente il report dalla pagina **Selezionare i report**. 

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>È necessaria una licenza Power BI Pro per installare l'app [!INCLUDE [prodshort](includes/prodshort.md)] in Power BI

Le app Power BI possono essere installate solo dagli utenti che hanno una licenza Power BI Pro. Dopo l'installazione dell'app Power BI, è possibile condividerla con utenti che non dispongono della licenza Power BI Pro.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"La convalida dei parametri non è riuscita. Assicurarsi che tutti i parametri siano validi"

Questo errore indica che uno o più parametri non sono validi.

- Il parametro di ambiente specificato non corrisponde ad alcun ambiente di produzione o sandbox di [!INCLUDE [prodshort](includes/prodshort.md)]. 
- Il parametro dell'azienda specificato non corrisponde ad alcuna società [!INCLUDE [prodshort](includes/prodshort.md)] esistente. Verificare il nome della società nella pagina **Società** in [!INCLUDE [prodshort](includes/prodshort.md)].
- Se ci si connette a [!INCLUDE [prodshort](includes/prodshort.md)] in locale, si è immesso un URL non valido. È possibile verificare l'URL nella pagina **Servizi web** in [!INCLUDE [prodshort](includes/prodshort.md)].  
- Una porta non viene aperta per consentire il passaggio della richiesta attraverso il firewall.

### <a name="login-failed"></a>Accesso non riuscito

Se viene visualizzato un errore "Accesso non riuscito" dopo l'utilizzo delle credenziali utente di [!INCLUDE [prodshort](includes/prodshort.md)] per eseguire l'accesso, è probabile che si sia verificato uno dei seguenti problemi:

- L'account che si sta utilizzando non dispone delle autorizzazioni per recuperare i dati di [!INCLUDE [prodshort](includes/prodshort.md)] da tale account. Verificare di disporre delle autorizzazioni per i dati richiesti in [!INCLUDE [prodshort](includes/prodshort.md)] e riprovare.
- Si è selezionato un tipo di autenticazione diverso da Base per la connessione a [!INCLUDE [prodshort](includes/prodshort.md)] in locale.
- Non è stato inserito un nome utente o una password validi.

### <a name="incorrect-company-name"></a>Nome della società non corretto

Un errore comune consiste nell'immettere il nome visualizzato della società al posto del nome della società. Per individuare il nome della società, cercare **Società**. Quindi utilizzare il campo **Nome** quando si immette il nome della società.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nessuna riga corrispondente alla chiave nella tabella

Se si immette un nome di società non valido durante il processo di connessione, è possibile che sia visualizzato il messaggio di errore "Nessuna riga corrispondente alla chiave nella tabella". Immettere il nome di società corretto e riprovare.

### <a name="historical-data-appears-to-be-missing"></a>Dati storici mancanti

Una volta che l'app Power BI è installata e i dati sono visualizzati in Power BI, è possibile notare che non tutti siano visualizzati. I set di dati vengono filtrati per restituire solo i 365 giorni precedenti dei dati. Questa impostazione predefinita rende più rapida la creazione di report.  

### <a name="i-only-see-data-for-a-single-company"></a>Visualizzazione unicamente dei dati di una singola società

L'app Power BI visualizzerà solo i dati della società [!INCLUDE [prodshort](includes/prodshort.md)] definita all'installazione dell'app Power BI. I dati di altre società possono essere aggiunti ai report aggiungendo nuove query che utilizzano società differenti come origine dati.  

## <a name="see-also"></a>Vedere anche

[Power BI per i consumatori](/power-bi/consumer/end-user-consumer)  
[Il "nuovo look" del servizio Power BI](/power-bi/service-new-look)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentazione di Power BI](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di Power BI](across-how-use-financials-data-source-powerbi.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati di PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Uso di [!INCLUDE[d365fin](includes/d365fin_md.md)] in Microsoft Flow](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
