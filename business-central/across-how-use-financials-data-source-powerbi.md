---
title: Creazione di report in Power BI Desktop per visualizzare i dati di Business Central | Microsoft Docs
description: Rendere disponibili i dati come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: a19d2bbff275ea4401943b588a68cdd2e6740e12
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924805"
---
# <a name="building-power-bi-reports-to-display-prodlong-data"></a>Creazione di report di Power BI per visualizzare i dati di [!INCLUDE [prodlong](includes/prodlong.md)]

È possibile rendere disponibili i dati di [!INCLUDE[prodlong](includes/prodlong.md)] come origine di dati in Power BI Desktop e sviluppare report efficaci dello stato dell'attività.

Questo articolo descrive come iniziare a utilizzare Power BI Desktop per creare report che visualizzano i dati di [!INCLUDE[prodlong](includes/prodlong.md)].  Dopo aver creato i report, è possibile pubblicarli nel servizio Power BI o condividerli con tutti gli utenti dell'organizzazione. Una volta che questi report sono nel servizio Power BI, gli utenti configurati per il suo utilizzo possono quindi visualizzare i report in [!INCLUDE[prodlong](includes/prodlong.md)].

## <a name="get-ready"></a>Preparazione

- Iscriversi al servizio Power BI.

    Se non si è già registrati andare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Quando ci si registra, utilizzare l'indirizzo e-mail e la password di lavoro.

- Scaricare [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

   Power BI Desktop è un'applicazione gratuita che si installa sul computer locale. Per ulteriori informazioni, vedere [Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Assicurarsi che i dati desiderati nel report siano pubblicati come servizio web.
    
    Ci sono molti servizi web pubblicati per impostazione predefinita. Un modo agevole di individuare i *servizi Web* consiste nel cercarli in [!INCLUDE[prodshort](includes/prodshort.md)]. Nella pagina **Servizi Web**, assicurarsi che il campo **Pubblica** sia selezionato. Questa attività è in genere amministrativa.
    
    Per ulteriori informazioni sulla pubblicazione di servizi Web, vedere [Pubblicare un servizio Web](across-how-publish-web-service.md).

- Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale, ottenere le seguenti informazioni:

    - L'URL OData per [!INCLUDE[prodshort](includes/prodshort.md)]. In genere, questo URL ha il formato `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, per esempio `https://localhost:7048/BC160/ODataV4`. Se si dispone di una distribuzione multi-tenant, includere il tenant nell'URL, ad esempio `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - Un nome utente e una chiave di accesso al servizio Web di un account [!INCLUDE[prodshort](includes/prodshort.md)].

      Per ottenere dati da [!INCLUDE[prodshort](includes/prodshort.md)], Power BI utilizza l'autenticazione di base. Quindi, sono necessari un nome utente e una chiave di accesso al servizio web per la connessione. L'account potrebbe essere l'account utente oppure l'organizzazione potrebbe avere un account specifico per questo scopo.

- Scaricare il tema del report [!INCLUDE [prodshort](includes/prodshort.md)] (opzionale).

    Per ulteriori informazioni, vedere [Uso del tema del report [!INCLUDE [prodshort](includes/prodshort.md)]](#theme) in questo articolo.

## <a name="add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Aggiungere [!INCLUDE[prodshort](includes/prodshort.md)] come origine dati in Power BI Desktop

La prima attività della creazione di report è aggiungere [!INCLUDE[prodshort](includes/prodshort.md)] come origine dati in Power BI Desktop. Una volta connesso, è possibile iniziare a creare il report.

1. Avviare Power BI Desktop.
2. Selezionare **Ottieni dati**.

    Se **Ottieni dati** non è visibile, selezionare il menu **File**, quindi **Ottieni dati**.
2. Nella pagina **Ottieni dati** selezionare **Servizi online**.
3. Nel riquadro **Servizi online** eseguire una delle seguenti operazioni:

    1. Se ci si sta connettendo a [!INCLUDE [prodshort](includes/prodshort.md)] online, scegliere **Dynamics 365 Business Central**, poi **Connetti**.
    2. Se ci si sta connettendo a [!INCLUDE [prodshort](includes/prodshort.md)] locale, scegliere **Dynamics 365 Business Central (locale)**, poi **Connetti**.

4. Power BI visualizza una procedura guidata per il processo di connessione, incluso l'accesso a [!INCLUDE [prodshort](includes/prodshort.md)].

    Per online, scegliere **Accedi**, quindi selezionare l'account pertinente. Utilizzare lo stesso account usato per accedere a [!INCLUDE [prodshort](includes/prodshort.md)].
    
    Per locale, inserire l'URL OData per [!INCLUDE[prodshort](includes/prodshort.md)] e, facoltativamente, il nome della società. Quindi, quando richiesto, immettere il nome utente e la password dell'account da utilizzare per la connessione a [!INCLUDE[prodshort](includes/prodshort.md)]. Nella casella **Password**, immettere la chiave di accesso del servizio web.

    > [!NOTE]  
    > Una volta eseguita la connessione a [!INCLUDE[prodshort](includes/prodshort.md)], non verrà richiesto nuovamente di eseguire l'accesso.
    
5. Scegliere **Connetti** per continuare.

    La procedura guidata di Power BI mostra un elenco di ambienti, origini dati e società di Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le origini dati, indicano tutti i servizi Web pubblicati tramite [!INCLUDE [prodshort](includes/prodshort.md)].
6. Specificare i dati che si desidera aggiungere al modello dati quindi scegliere il pulsante **Carica**.
7. Ripetere i passaggi precedenti per aggiungere ulteriori [!INCLUDE [prodshort](includes/prodshort.md)], o altri dati, per il modello dati Power BI.

Dopo che i dati sono stati caricati puoi vederli nel riquadro di spostamento destro nella pagina. A questo punto, è stata stabilita correttamente la connessione ai dati di [!INCLUDE[prodshort](includes/prodshort.md)] ed è possibile iniziare a creare il report di Power BI.  

> [!TIP]
> Per ulteriori informazioni sull'uso di Power BI Desktop, vedere [Introduzione a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Creazione di report per visualizzare i dati associati a un elenco

È possibile creare report che vengono visualizzati in un riquadro Dettaglio informazioni di una pagina elenco [!INCLUDE [prodshort](includes/prodshort.md)]. I report possono contenere dati sul record selezionato nell'elenco. La creazione di questi report è simile ad altri report, tranne che per alcune cose che è necessario eseguire per assicurarsi che i report vengano visualizzati come previsto. Per ulteriori informazioni, vedere [Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prodshort](includes/prodshort.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prodshort-report-theme-optional"></a><a name="theme"></a>Uso del tema del report [!INCLUDE [prodshort](includes/prodshort.md)] (opzionale)

Prima di creare il report, è consigliabile scaricare e importare il file del tema [!INCLUDE [prodshort](includes/prodshort.md)]. Il file del tema crea una tavolozza dei colori in modo da creare report con lo stesso stile cromatico delle app [!INCLUDE [prodshort](includes/prodshort.md)] senza dover definire i colori personalizzati per ogni elemento grafico.

> [!NOTE]
> Questa attività è facoltativa. È sempre possibile creare i report e quindi scaricare e applicare il modello di stile in un secondo momento.

### <a name="download-the-theme"></a>Scaricare il tema

Il file del tema è disponibile come file json nella raccolta dei temi di Microsoft Power BI Community. Per scaricare il file del tema, procedere nel seguente modo:

1. Andare a [Raccolta dei temi di Microsoft Power BI Community per Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Selezionare l'allegato **Microsoft Dynamics Business Central.json** del download.

### <a name="import-the-theme-on-a-report"></a>Importare il tema in un report

Dopo aver scaricato il tema del report [!INCLUDE [prodshort](includes/prodshort.md)] è possibile importarlo nei report. Per importare il tema, selezionare **Visualizza** > **Temi** > **Cerca temi**. Per ulteriori informazioni, vedere [Power BI Desktop - Importare temi di report personalizzati](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Pubblicare i report

Dopo aver creato o modificato un report è possibile pubblicarlo nel servizio Power BI e condividerlo anche con altre persone nell'organizzazione. Una volta pubblicato, il report è visibile in Power BI. Il report diventa anche disponibile per la selezione in [!INCLUDE[prodshort](includes/prodshort.md)].

Per pubblicare un rapporto, selezionare **Pubblica** nella scheda **Home** della barra multifunzione o dal menu **File**. Se è stato effettuato l'accesso al servizio Power BI il report viene pubblicato in questo servizio. In caso contrario, verrà richiesto di accedere. 

## <a name="distribute-or-share-a-report"></a>Distribuire o condividere un report

Ci sono un paio di modi per inviare report ai colleghi e ad altre persone:

- Distribuire report come file .pbix.

    I report vengono archiviati sul computer come file .pbix. È possibile distribuire il file .pbix del report agli utenti, come qualsiasi altro file. Quindi, gli utenti possono caricare il file nel servizio Power BI. Vedere [Caricare report da file](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > La distribuzione dei report in questo modo comporta che l'aggiornamento dei dati per i report verrà eseguito individualmente da ciascun utente. Questa situazione potrebbe avere un impatto sulle prestazioni di [!INCLUDE[prodshort](includes/prodshort.md)].

- Condividere il report dal servizio Power BI

    Se si dispone di una licenza Power BI Pro, è possibile condividere il report con altre persone direttamente dal servizio Power BI. Per ulteriori informazioni, vedere [Power BI - Condividere una dashboard o un report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Abilitare i dati aziendali per Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
