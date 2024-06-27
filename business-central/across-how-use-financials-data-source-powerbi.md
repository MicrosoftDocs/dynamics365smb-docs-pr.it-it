---
title: Creazione di report in Power BI Desktop per visualizzare i dati di Business Central
description: Rendere disponibili i dati come origine di dati in Power BI e sviluppare report efficaci dello stato dell'attività.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/12/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Creare report Power BI per visualizzare dati [!INCLUDE [prod_long](includes/prod_long.md)]

È possibile rendere disponibili i dati di [!INCLUDE[prod_long](includes/prod_long.md)] come origine di dati in Power BI Desktop e sviluppare report efficaci sullo stato dell'attività.

Questo articolo descrive come iniziare a utilizzare Power BI Desktop per creare report che visualizzano i dati di [!INCLUDE[prod_long](includes/prod_long.md)]. Dopo aver creato i report, è possibile pubblicarli nel servizio Power BI o condividerli con tutti gli utenti dell'organizzazione. Quando i report sono nel servizio Power BI, gli utenti configurati per il suo utilizzo possono visualizzare i report in [!INCLUDE[prod_long](includes/prod_long.md)].

## Preparazione

- Iscriversi al servizio Power BI.

  Se non ti sei già registrati, vai a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Quando ci si registra, utilizzare l'indirizzo e-mail e la password di lavoro.

- Scaricare [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop è un'applicazione gratuita che si installa sul computer locale. Per ulteriori informazioni, vedere [Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Assicurati che i dati che desideri nel report siano disponibili come pagina API o pubblicati come servizio web. Per ulteriori informazioni, vedi [Esporre i dati tramite pagine API o servizi web OData](admin-powerbi-setup.md#exposedata).

<!--- For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, get the following information:

  - The OData URL for [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Typically, this URL has the format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, for example, `https://localhost:7048/BC190/ODataV4`. If you have a multi-tenant deployment, include the tenant in the URL, for example, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - A user name and web service access key of a [!INCLUDE[prod_short](includes/prod_short.md)] account.

    To get data from [!INCLUDE[prod_short](includes/prod_short.md)], Power BI uses basic authentication. So, you'll need a user name and web service access key to connect. The account might be your own user account, or your organization may have specific account for this purpose.-->

- Scaricare il tema del report [!INCLUDE [prod_short](includes/prod_short.md)] (opzionale).

  Per ulteriori informazioni, vedi [Utilizzare il tema del report [!INCLUDE [prod_short](includes/prod_short.md)]](#theme) in questo articolo.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="getdata"></a>Aggiungi [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop

La prima attività della creazione di report è aggiungere [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power BI Desktop. Una volta connesso, è possibile iniziare a creare il report.

1. Avviare Power BI Desktop.
2. Selezionare **Ottieni dati**.

    Se **Ottieni dati** non è visibile, selezionare il menu **File**, quindi **Ottieni dati**.
3. Nella pagina **Ottieni dati** selezionare **Servizi online**.
4. Nel riquadro **Servizi online** eseguire una delle seguenti operazioni:

    - Per connetterti a [!INCLUDE [prod_short](includes/prod_short.md)] online, seleziona **Dynamics 365 Business Central**, poi **Connetti**.
    <!--- To connect to  [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, select **Dynamics 365 Business Central (on-premises)**, then **Connect**.-->

5. Accedi a [!INCLUDE [prod_short](includes/prod_short.md)] (una sola volta).

    Se non hai mai effettuato l'accesso a [!INCLUDE [prod_short](includes/prod_short.md)] da Power BI Desktop, ti viene chiesto di accedere.

    - Per [!INCLUDE [prod_short](includes/prod_short.md)] online, seleziona **Accedi**, quindi scegli l'account pertinente. Utilizzare lo stesso account usato per accedere a [!INCLUDE [prod_short](includes/prod_short.md)]. Al termine, seleziona **Connetti**.

    <!--- For [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, first enter the OData URL for [!INCLUDE[prod_short](includes/prod_short.md)], then select **OK**. When prompted, enter the user name and password of the account to use for connecting to [!INCLUDE[prod_short](includes/prod_short.md)]. In the **Password** box, enter the web service access key. When done, select **Connect**.-->

    > [!NOTE]  
    > Una volta eseguita la connessione a [!INCLUDE[prod_short](includes/prod_short.md)], non ti verrà richiesto di eseguire di nuovo l'accesso. [Come posso modificare o cancellare l'account che sto utilizzando attualmente per connettermi a Business Central da Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Una volta eseguita la connessione, Power BI contatta il servizio [!INCLUDE [prod_short](includes/prod_short.md)]. La finestra **Navigatore** visualizza le origini dati disponibili per la creazione di report. Seleziona una cartella per espanderla e vedere le origini dati disponibili.

   Le origini dati indicano tutti i servizi Web e le pagine API pubblicati per [!INCLUDE [prod_short](includes/prod_short.md)], raggruppate per ambienti e società. Con [!INCLUDE [prod_short](includes/prod_short.md)] online, la finestra **Navigator**ha la seguente struttura:

    - **Nome ambiente**
      - **Nome società**
        - **API avanzate**

          Questa cartella elenca le pagine API avanzate pubblicate da Microsoft, come le [API di automazione di Business Central](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) e le [pagine API personalizzate per Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Le pagine API personalizzate sono ulteriormente raggruppate in cartelle secondo le proprietà [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) del codice sorgente della pagina API.

        - **API standard v2.0**

          Questa cartella elenca le pagine API esposte dall'[API Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Servizi web \(legacy)**

          Questa cartella elenca le pagine, le codeunit e le query pubblicate come servizi Web in Business Central.

    <!--
    > [!NOTE]
    > The structure for Business Central on-premises is different because it doesn't support API pages.-->

7. Seleziona una o più origini dati che vuoi aggiungere al modello dati quindi scegli il pulsante **Carica**.
8. Se in seguito vuoi aggiungere altri dati di Business Central, puoi ripetere i passaggi precedenti.

Dopo che i dati sono stati caricati puoi vederli nel riquadro di spostamento destro nella pagina. A questo punto, sei connesso ai dati di [!INCLUDE[prod_short](includes/prod_short.md)] e puoi iniziare a creare il report di Power BI.  

> [!TIP]
> Per ulteriori informazioni sull'uso di Power BI Desktop, vedere [Introduzione a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## Creazione di report accessibili

È importante rendere i tuoi report utilizzabili per il maggior numero di persone possibile. Prova a progettare report in modo che non richiedano adattamenti speciali per soddisfare esigenze specifiche di utenti diversi. Assicurati che il design consenta agli utenti di sfruttare le tecnologie per l'accessibilità standard, come le utilità per la lettura dello schermo. Power BI include varie funzioni di accessibilità, strumenti e linee guida per aiutarti a raggiungere questo obiettivo. Per maggiori informazioni, [Progettare report Power BI per l'accessibilità](/power-bi/create-reports/desktop-accessibility-creating-reports) nella documentazione di Power BI.

## Creazione di report per visualizzare i dati associati a un elenco

È possibile creare report che vengono visualizzati in un riquadro Dettaglio informazioni di una pagina elenco [!INCLUDE [prod_short](includes/prod_short.md)]. I report possono contenere dati sul record selezionato nell'elenco. La creazione di questi report è simile ad altri report, tranne che per alcune cose che è necessario eseguire per assicurarsi che i report vengano visualizzati come previsto. Per ulteriori informazioni, vedere [Creazione di report Power BI per la visualizzazione dei dati di elenco in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="theme"></a>Uso del tema del report [!INCLUDE [prod_short](includes/prod_short.md)] (opzionale)

Prima di creare il report, è consigliabile scaricare e importare il file del tema [!INCLUDE [prod_short](includes/prod_short.md)]. Il file del tema crea una tavolozza dei colori in modo da creare report con lo stesso stile cromatico delle app [!INCLUDE [prod_short](includes/prod_short.md)] senza dover definire i colori personalizzati per ogni elemento grafico.

> [!NOTE]
> Questa attività è facoltativa. È sempre possibile creare i report e quindi scaricare e applicare il modello di stile in un secondo momento.

### Scaricare il tema

Il file del tema è disponibile come file json nella raccolta dei temi di Microsoft Power BI Community. Per scaricare il file del tema, procedere nel seguente modo:

1. Andare alla [raccolta dei temi di Microsoft Power BI Community per Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Selezionare l'allegato **Microsoft Dynamics Business Central.json** del download.

### Importare il tema in un report

Dopo aver scaricato il tema del report [!INCLUDE [prod_short](includes/prod_short.md)] è possibile importarlo nei report. Per importare il tema, selezionare **Visualizza** > **Temi** > **Cerca temi**. Per ulteriori informazioni, vedere [Power BI Desktop - Importare temi di report personalizzati](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## Pubblicare i report

Dopo aver creato o modificato un report puoi pubblicarlo nel servizio Power BI e condividerlo anche con altre persone nell'organizzazione. Dopo aver pubblicato un report, è disponibile in Power BI. Il report diventa anche disponibile per la selezione in [!INCLUDE[prod_short](includes/prod_short.md)].

Per pubblicare un report, selezionare **Pubblica** nella scheda **Home** della barra multifunzione o dal menu **File**. Se è stato effettuato l'accesso al servizio Power BI il report viene pubblicato in questo servizio. In caso contrario, verrà richiesto di accedere. 

## Distribuire o condividere un report

Ci sono un paio di modi per inviare report ai colleghi e ad altre persone:

- Distribuire report come file .pbix.

    I report vengono archiviati sul computer come file .pbix. È possibile distribuire il file .pbix del report agli utenti, come qualsiasi altro file. Quindi, gli utenti possono caricare il file nel servizio Power BI. Vedere [Caricare report da file](across-working-with-powerbi.md#upload).

    > [!NOTE]
    > La distribuzione dei report in questo modo comporta che l'aggiornamento dei dati per i report verrà eseguito individualmente da ciascun utente. Questa situazione potrebbe avere un impatto sulle prestazioni di [!INCLUDE[prod_short](includes/prod_short.md)].

- Condividere il report dal servizio Power BI

    Se si dispone di una licenza Power BI Pro, è possibile condividere il report con altre persone direttamente dal servizio Power BI. Per ulteriori informazioni, vedere [Power BI - Condividere una dashboard o un report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## Come sviluppare report Power BI interaziendali o interambientali

Gli endpoint API [!INCLUDE[prod_short](includes/prod_short.md)] hanno tutti il prefisso `https://api.businesscentral.dynamics.com/v2.0/<environment_name>/api/v2.0` seguito da `/companies({company_id})/accounts({id})` (qui usiamo l'API `accounts` come illustrazione). Puoi utilizzare questa struttura per creare query PowerQuery che caricano dati per più società o più ambienti se l'utente che sta leggendo i dati può accedervi.

Per impostare una query per caricare dati per più società, attieniti alla seguente procedura:

1. Prendi la query PowerQuery che carica i dati per una singola società. Convertila in una funzione Power Query personalizzata che accetta come parametri l'ID società (o forse il nome dell'ambiente). Per saperne di più, vai a [Utilizzo delle funzioni Power Query personalizzate](/power-query/custom-function).
1. Ora utilizza la nuova funzione personalizzata in una query PowerQuery, in cui mappi la funzione su un elenco di società e quindi unisci i set di dati utilizzando la funzione [Table.Combine](/powerquery-m/table-combine) di Power Query.

## Risolvere i problemi

### "Impossibile inserire un record. L'intento di connessione corrente è di sola lettura." errore durante la connessione alla pagina API personalizzata

> **APPLICABILE A:** Business Central Online

A partire da febbraio 2022, i nuovi report che utilizzano i dati di [!INCLUDE [prod_short](includes/prod_short.md)] vengono collegati a una replica di sola lettura del database di [!INCLUDE [prod_short](includes/prod_short.md)] per impostazione predefinita. In rari casi, a seconda della progettazione della pagina, potresti ricevere un errore quando tenti di connetterti e ottenere i dati dalla pagina.

1. Avviare Power BI Desktop.
2. Nella barra multifunzione seleziona **Ottieni dati** > **Servizi online**.
3. Nel riquadro **Servizi online**, seleziona **Dynamics 365 Business Central**, poi **Connetti**.
4. Nella finestra **Navigatore** seleziona l'endpoint dell'API da cui vuoi caricare i dati.
5. Il riquadro di anteprima mostra il seguente errore:

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

## Vedi anche

[Abilitare i dati aziendali per Power BI](admin-powerbi-setup.md)  
[Business Intelligence](bi.md)  
[Preparazione al business](ui-get-ready-business.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanze](finance.md)  
[Avvio rapido: connettersi ai dati in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
