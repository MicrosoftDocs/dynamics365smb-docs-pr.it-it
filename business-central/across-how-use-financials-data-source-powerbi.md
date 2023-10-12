---
title: Creazione di report in Power BI Desktop per visualizzare i dati di Business Central | Microsoft Docs
description: Rendere disponibili i dati come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 09/07/2022
ms.author: jswymer
---

# <a name="building-power-bi-reports-to-display--data"></a>Creazione di report di Power BI per visualizzare i dati di [!INCLUDE [prod_long](includes/prod_long.md)]

È possibile rendere disponibili i dati di [!INCLUDE[prod_long](includes/prod_long.md)] come origine di dati in Power BI Desktop e sviluppare report efficaci dello stato dell'attività.

Questo articolo descrive come iniziare a utilizzare Power BI Desktop per creare report che visualizzano i dati di [!INCLUDE[prod_long](includes/prod_long.md)].  Dopo aver creato i report, è possibile pubblicarli nel servizio Power BI o condividerli con tutti gli utenti dell'organizzazione. Una volta che questi report sono nel servizio Power BI, gli utenti configurati per il suo utilizzo possono quindi visualizzare i report in [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Preparazione

- Iscriversi al servizio Power BI.

  Se non si è già registrati andare a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Quando ci si registra, utilizzare l'indirizzo e-mail e la password di lavoro.

- Scaricare [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop è un'applicazione gratuita che si installa sul computer locale. Per ulteriori informazioni, vedere [Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Assicurati che i dati che desideri nel report siano disponibili come pagina API o pubblicati come servizio web.

  Per ulteriori informazioni, vedi [Esporre i dati tramite pagine API o servizi web OData](admin-powerbi-setup.md#exposedata).

- Per [!INCLUDE[prod_short](includes/prod_short.md)] in locale, ottenere le seguenti informazioni:

  - L'URL OData per [!INCLUDE[prod_short](includes/prod_short.md)].
  
    In genere, questo URL ha il formato `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, per esempio `https://localhost:7048/BC190/ODataV4`. Se si dispone di una distribuzione multi-tenant, includere il tenant nell'URL, ad esempio `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Un nome utente e una chiave di accesso al servizio Web di un account [!INCLUDE[prod_short](includes/prod_short.md)].

    Per ottenere dati da [!INCLUDE[prod_short](includes/prod_short.md)], Power BI utilizza l'autenticazione di base. Quindi, sono necessari un nome utente e una chiave di accesso al servizio web per la connessione. L'account potrebbe essere l'account utente oppure l'organizzazione potrebbe avere un account specifico per questo scopo.

- Scaricare il tema del report [!INCLUDE [prod_short](includes/prod_short.md)] (opzionale).

  Per ulteriori informazioni, vedi [Utilizzare il tema del report [!INCLUDE [prod_short](includes/prod_short.md)]](#theme) in questo articolo.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Aggiungi [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop

La prima attività della creazione di report è aggiungere [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop. Una volta connesso, è possibile iniziare a creare il report.

1. Avviare Power BI Desktop.
2. Selezionare **Ottieni dati**.

    Se **Ottieni dati** non è visibile, selezionare il menu **File**, quindi **Ottieni dati**.
3. Nella pagina **Ottieni dati** selezionare **Servizi online**.
4. Nel riquadro **Servizi online** eseguire una delle seguenti operazioni:

    - Per connetterti a [!INCLUDE [prod_short](includes/prod_short.md)] online, seleziona **Dynamics 365 Business Central**, poi **Connetti**.
    - Per connetterti a [!INCLUDE [prod_short](includes/prod_short.md)] locale, seleziona **Dynamics 365 Business Central (locale)**, poi **Connetti**.

5. Accedi a [!INCLUDE [prod_short](includes/prod_short.md)] (una sola volta).

    Se non hai mai effettuato l'accesso a [!INCLUDE [prod_short](includes/prod_short.md)] dal Power BI desktop prima, ti viene chiesto di accedere.

    - Per [!INCLUDE [prod_short](includes/prod_short.md)] online, seleziona **Accedi**, quindi scegli l'account pertinente. Utilizzare lo stesso account usato per accedere a [!INCLUDE [prod_short](includes/prod_short.md)]. Al termine, seleziona **Connetti**.

    - Per [!INCLUDE [prod_short](includes/prod_short.md)] locale, inserisci prima l'URL OData per [!INCLUDE[prod_short](includes/prod_short.md)], quindi seleziona **OK**. Quando richiesto, immetti il nome utente e la password dell'account da utilizzare per la connessione a [!INCLUDE[prod_short](includes/prod_short.md)]. Nella casella **Password**, immettere la chiave di accesso del servizio web. Al termine, seleziona **Connetti**.

    > [!NOTE]  
    > Una volta eseguita la connessione a [!INCLUDE[prod_short](includes/prod_short.md)], non verrà richiesto nuovamente di eseguire l'accesso. [Come posso modificare o cancellare l'account che sto utilizzando attualmente per connettermi a Business Central da Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Una volta connesso, Power BI contatta il servizio Business Central. La finestra dello **strumento di navigazione** viene visualizzata con le origini dati disponibili per la creazione di report. Seleziona una cartella per espanderla e vedere le origini dati disponibili. 

   Le origini dati, indicano tutti i servizi Web e le pagine API pubblicati per [!INCLUDE [prod_short](includes/prod_short.md)]. Le origini dati sono raggruppate per ambienti e società di Business Central. Con Business Central online, lo **strumento di navigazione** ha la seguente struttura:

    - **Nome ambiente**
      - **Nome società**
        - **API avanzate**

          Questa cartella elenca le pagine API avanzate pubblicate da Microsoft, come le [API di automazione di Business Central](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) e le [pagine API personalizzate per Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Le pagine API personalizzate sono ulteriormente raggruppate in cartelle per proprietà [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) del codice sorgente della pagina API.

        - **API standard v2.0**

          Questa cartella elenca le pagine API esposte dall'[API Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Servizi web \(legacy)**

          Questa cartella elenca le pagine, le codeunit e le query pubblicate come servizi Web in Business Central.

    > [!NOTE]
    > La struttura per Business Central locale è diversa perché non supporta le pagine API.

7. Seleziona una o più origini dati che vuoi aggiungere al modello dati quindi scegli il pulsante **Carica**.
8. Se in seguito vuoi aggiungere altri dati di Business Central, puoi ripetere i passaggi precedenti.

Dopo che i dati sono stati caricati puoi vederli nel riquadro di spostamento destro nella pagina. A questo punto, è stata stabilita correttamente la connessione ai dati di [!INCLUDE[prod_short](includes/prod_short.md)] ed è possibile iniziare a creare il report di Power BI.  

> [!TIP]
> Per ulteriori informazioni sull'uso di Power BI Desktop, vedere [Introduzione a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Creazione di report accessibili

È importante rendere i tuoi report utilizzabili per il maggior numero di persone possibile. Prova a progettare report in modo che non richiedano adattamenti speciali per soddisfare esigenze specifiche di utenti diversi. Assicurati che il design consenta agli utenti di sfruttare le tecnologie per l'accessibilità standard, come le utilità per la lettura dello schermo. Power BI include varie funzioni di accessibilità, strumenti e linee guida per aiutarti a raggiungere questo obiettivo. Per maggiori informazioni, [Progettare report Power BI per l'accessibilità](/power-bi/create-reports/desktop-accessibility-creating-reports) nella documentazione di Power BI.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Creazione di report per visualizzare i dati associati a un elenco

È possibile creare report che vengono visualizzati in un riquadro Dettaglio informazioni di una pagina elenco [!INCLUDE [prod_short](includes/prod_short.md)]. I report possono contenere dati sul record selezionato nell'elenco. La creazione di questi report è simile ad altri report, tranne che per alcune cose che è necessario eseguire per assicurarsi che i report vengano visualizzati come previsto. Per ulteriori informazioni, vedere [Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the--report-theme-optional"></a><a name="theme"></a>Uso del tema del report [!INCLUDE [prod_short](includes/prod_short.md)] (opzionale)

Prima di creare il report, è consigliabile scaricare e importare il file del tema [!INCLUDE [prod_short](includes/prod_short.md)]. Il file del tema crea una tavolozza dei colori in modo da creare report con lo stesso stile cromatico delle app [!INCLUDE [prod_short](includes/prod_short.md)] senza dover definire i colori personalizzati per ogni elemento grafico.

> [!NOTE]
> Questa attività è facoltativa. È sempre possibile creare i report e quindi scaricare e applicare il modello di stile in un secondo momento.

### <a name="download-the-theme"></a>Scaricare il tema

Il file del tema è disponibile come file json nella raccolta dei temi di Microsoft Power BI Community. Per scaricare il file del tema, procedere nel seguente modo:

1. Andare alla [raccolta dei temi di Microsoft Power BI Community per Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Selezionare l'allegato **Microsoft Dynamics Business Central.json** del download.

### <a name="import-the-theme-on-a-report"></a>Importare il tema in un report

Dopo aver scaricato il tema del report [!INCLUDE [prod_short](includes/prod_short.md)] è possibile importarlo nei report. Per importare il tema, selezionare **Visualizza** > **Temi** > **Cerca temi**. Per ulteriori informazioni, vedere [Power BI Desktop - Importare temi di report personalizzati](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Pubblicare i report

Dopo aver creato o modificato un report è possibile pubblicarlo nel servizio Power BI e condividerlo anche con altre persone nell'organizzazione. Una volta pubblicato, il report è visibile in Power BI. Il report diventa anche disponibile per la selezione in [!INCLUDE[prod_short](includes/prod_short.md)].

Per pubblicare un report, selezionare **Pubblica** nella scheda **Home** della barra multifunzione o dal menu **File**. Se è stato effettuato l'accesso al servizio Power BI il report viene pubblicato in questo servizio. In caso contrario, verrà richiesto di accedere. 

## <a name="distribute-or-share-a-report"></a>Distribuire o condividere un report

Ci sono un paio di modi per inviare report ai colleghi e ad altre persone:

- Distribuire report come file .pbix.

    I report vengono archiviati sul computer come file .pbix. È possibile distribuire il file .pbix del report agli utenti, come qualsiasi altro file. Quindi, gli utenti possono caricare il file nel servizio Power BI. Vedere [Caricare report da file](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > La distribuzione dei report in questo modo comporta che l'aggiornamento dei dati per i report verrà eseguito individualmente da ciascun utente. Questa situazione potrebbe avere un impatto sulle prestazioni di [!INCLUDE[prod_short](includes/prod_short.md)].

- Condividere il report dal servizio Power BI

    Se si dispone di una licenza Power BI Pro, è possibile condividere il report con altre persone direttamente dal servizio Power BI. Per ulteriori informazioni, vedere [Power BI - Condividere una dashboard o un report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="fixing-problems"></a>Risolvere i problemi

### <a name="cannot-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page"></a>"Impossibile inserire un record. L'intento di connessione corrente è di sola lettura." errore durante la connessione alla pagina API personalizzata

> **APPLICABILE A:** Business Central Online

A partire da febbraio 2022, i nuovi report che utilizzano i dati di Business Central si collegheranno a una replica di sola lettura del database di Business Central per impostazione predefinita. In rari casi, a seconda della progettazione della pagina, riceverai un errore quando tenti di connetterti e ottenere i dati dalla pagina.

1. Avviare Power BI Desktop.
2. Nella barra multifunzione seleziona **Ottieni dati** > **Servizi online**.
3. Nel riquadro **Servizi online**, seleziona **Dynamics 365 Business Central**, poi **Connetti**.
4. Nella finestra **Navigatore** seleziona l'endpoint dell'API da cui vuoi caricare i dati.
5. Nel riquadro di anteprima a destra, vedrai il seguente errore:

   *Dynamics365BusinessCentral: richiesta non riuscita: il server remoto ha restituito un errore: (400) richiesta non valida. (Impossibile inserire un record. L'intento di connessione corrente è di sola lettura. CorrelationId: [...])".*

6. Seleziona **Trasforma i dati** invece di **Carica** come faresti normalmente.
7. In **Editor di Power Query**, seleziona **Editor avanzato** dalla barra multifunzione.
8. Nella riga che inizia con **Origine =**, sostituisci il testo seguente:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   con:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Seleziona **Fatto**.
10. Seleziona **Chiudi e applica** dalla barra multifunzione per salvare le modifiche e chiudere l'editor di Power Query.

## <a name="see-also"></a>Vedi anche

[Abilitare i dati aziendali per Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
