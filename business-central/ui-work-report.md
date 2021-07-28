---
title: Utilizzo di report, processi batch e XMLport
description: Informazioni su come inserire un report in una coda di processi e programmare per l'elaborazione per una data e un'ora specifiche.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: 9deb7e30e05da74e6ea263a0262680d2e99b8b4b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439952"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Utilizzo di report, processi batch e XMLport

Un report raccoglie informazioni in base a una serie di criteri specificati. Organizza e presenta le informazioni in un formato di facile lettura che puoi stampare o salvare come file. Sono disponibili molti report a cui è possibile accedere dall'applicazione. I report in genere forniscono informazioni relative al contesto della pagina visualizzata. Ad esempio, la pagina **Cliente** include i report per i principali 10 clienti, statistiche di vendita e altro ancora.

I processi batch e XMLport eseguono più o meno gli stessi report ma sono usati più per eseguire un processo o esportare dati. Ad esempio, il processo batch **Crea solleciti** crea documenti di sollecito per clienti con pagamenti scaduti.  

> [!NOTE]
> Questo argomento fa essenzialmente riferimento a “report" ma informazioni simili si applicano ai processi batch e a XMLport.

## <a name="getting-started"></a>Introduzione

I report sono disponibili nella scheda **Report** delle pagine selezionate oppure è possibile utilizzare una ricerca tramite l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") per individuare i report per nome.

Quando si apre un report, processo batch o XMLport, viene di norma visualizzata una pagina di richiesta dove è possibile impostare varie opzioni e filtri che determinano cosa includere nel report. Le sezioni seguenti spiegano come utilizzare la pagina di richiesta per creare, visualizzare in anteprima e stampare un report.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Utilizzo dei valori predefiniti: impostazioni predefinite 

La maggior parte delle pagine di richiesta include il campo **Utilizza valori predefiniti di**. Questo campo consente di selezionare le impostazioni predefinite per il report, che impostano automaticamente opzioni e filtri per il report. Selezionare una voce dall'elenco a discesa per vedere che le opzioni e i filtri nella pagina della richiesta cambiano di conseguenza.

La voce **Filtri e opzioni utilizzati di recente** è sempre disponibile. Questa voce imposta il report per utilizzare le opzioni e i filtri che sono stati utilizzati l'ultima volta che è stato eseguito il report.

Il campo **Utilizza valori predefiniti di** fornisce un modo rapido e affidabile per generare costantemente report che contengono i dati corretti. Dopo aver selezionato una voce, è possibile modificare qualsiasi opzione e filtro prima di visualizzare in anteprima o stampare il report. Le modifiche effettuate non verranno salvate nella voce di impostazione predefinita selezionata, ma verranno salvate in **Filtri e opzioni utilizzati più di recente**.

>[!NOTE]
> Le impostazioni predefinite vengono generalmente configurate e gestite da un amministratore. Per ulteriori informazioni, vedere [Gestire impostazioni salvate per report e processi batch](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Specificare la data da includere nei report

Usare i campi in **Opzioni** e **Filtri** per limitare le informazioni che si desiderano nel report. È possibile impostare i filtri in un report più o meno nello stesso modo in cui si impostano i filtri negli elenchi. Per ulteriori informazioni, vedere [Filtri](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La sezione **Filtra elenco per** in una pagina di richiesta fornisce una generica capacità di filtro per i report. Tali filtri sono facoltativi.
>
> Alcuni report ignoreranno tali filtri, nel senso che qualsiasi filtro venga impostato nella sezione **Filtra elenco per**, l'output del report è lo stesso. Non è possibile fornire un elenco dei campi che vengono ignorati in quali report, quindi sarà necessario sperimentare con i filtri quando utilizzati.
>
> **Esempio**: quando si utilizza il processo batch **Crea solleciti**, un filtro per il campo **Movimenti contabili clienti** di **Livello ultimo sollecito emesso** verrà ignorato perché i filtri sono fissi per tale processo batch.

## <a name="previewing-a-report"></a>Anteprima di un report

L'anteprima di un report consente di vedere come apparirà il report prima di stamparlo. L'anteprima non è basata sul campo **Stampante** selezionato nella pagina della richiesta. È controllato dal browser. Dopo l'anteprima, è possibile tornare alla pagina della richiesta e modificare le opzioni e i filtri secondo necessità.

Per visualizzare in anteprima un report, scegliere il pulsante **Anteprima** o **Anteprima e chiudi** nella pagina di richiesta del report. Il pulsante visualizzato dipende dal report, quindi alcuni report hanno **Anteprima** mentre altri hanno il pulsante **Anteprima e chiudi**. Entrambi i pulsanti aprono un'anteprima del report. La differenza è che **Anteprima** mantiene la pagina della richiesta aperta, in modo da potervi tornare, apportare modifiche, visualizzare di nuovo l'anteprima o stampare. Con **Anteprima e chiudi**, la pagina di richiesta si chiude, quindi è necessario aprire nuovamente il report per apportare modifiche o stamparlo.

> [!NOTE]
> Se si utilizza il primo ciclo di rilascio di Business Central 2020 o una versione precedente, è disponibile solo un pulsante **Anteprima** che chiude la pagina di richiesta in anteprima, come descritto per **Anteprima e chiudi**.

### <a name="working-with-the-preview"></a>Utilizzo dell'anteprima

Nell'anteprima, utilizzare la barra dei menu nell'anteprima del report per:

- Spostarsi tra le pagine
- Ingrandire o ridurre
- Ridimensionare per adattare alla pagina
- Seleziona testo

    È possibile copiare il testo di un report e incollarlo altrove, come una pagina in [!INCLUDE[prod_short](includes/prod_short.md)] o Microsoft Word.  Usando un mouse, ad esempio, tieni premuto sul punto in cui vuoi iniziare. Quindi sposta il mouse per selezionare una o più parole, frasi o paragrafi. Premere il pulsante destro del mouse e selezionare **Copia**. Quindi incollare il testo selezionato nella posizione desiderata.
- Panoramica del documento

    È possibile spostare l'area visibile del report in qualsiasi direzione in modo da poter visualizzare altre aree o il report. La panoramica risulta utile quando hai eseguito l'ingrandimento per visualizzare i dettagli.  Ad esempio, tenere premuto il pulsante del mouse su un punto dell'anteprima del report, quindi spostare il mouse.

- Scaricare in un file PDF sul computer o in rete.
- Stampa

## <a name="saving-a-report-to-a-file"></a>Salvataggio di un report in un file

Puoi salvare un report in un documento PDF, documento di Microsoft Word o foglio di lavoro di Microsoft Excel scegliendo il pulsante **Invia a** ed effettuando la scelta desiderata.

### <a name="send-to-excel"></a>Inviare a Excel

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Sono disponibili due opzioni per salvare i risultati del report come foglio di lavoro in una cartella di lavoro di Excel: **Documento Microsoft Excel (dati e layout)** e **Documento Microsoft Excel (solo dati)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Documento di Microsoft Excel (dati e layout)](#tab/data-and-layout)

Questa opzione è disponibile solo per i report che utilizzano un layout RDLC. Esporta i risultati del report con il layout RDLC applicato. Utilizza questa opzione se vuoi esportare i dati una volta e vuoi apportare solo modifiche minori al loro aspetto, come carattere e combinazione di colori.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Documento di Microsoft Excel (solo dati)](#tab/data-only)

L'opzione **Documento di Microsoft Excel (solo dati)** esporta i risultati del report e i criteri utilizzati per generarli, ma non include il layout del report. Il file Excel includerà l'intero set di dati, come dati non elaborati, organizzato in righe e colonne. Sono incluse tutte le colonne di dati del set di dati del report, indipendentemente dal fatto che siano utilizzate nel layout del report.  Usa questa opzione quando vuoi:

- Eseguire analisi ad hoc dei dati. Ad esempio, puoi filtrare i dati e utilizzare Power Pivot per visualizzarli.

  Ogni volta che esporti i risultati, viene creato un nuovo foglio di lavoro. Usando l'opzione **Documento Microsoft Excel (solo dati)** puoi eseguire lo stesso report e riutilizzare le modifiche alla formattazione. Ad esempio, per Power Pivot, puoi eseguire nuovamente il report per un altro periodo di tempo, copiare i risultati nel foglio di lavoro e quindi aggiornare il foglio di lavoro. Puoi anche trovare un'app per la creazione di report in [AppSource](https://appsource.microsoft.com/).
- Esamina il set di dati del report durante la creazione o la modifica dei layout di report personalizzati.

  Per informazioni sulla creazione di layout di report personalizzati, vedi [Creazione o modifica di layout di report personalizzati](ui-how-create-custom-report-layout.md)
- Diagnostica i problemi relativi ai dati nei report.

##### <a name="for-administrators"></a>Per gli amministratori

- **Documento Microsoft Excel (solo dati)** è stato introdotto come funzionalità facoltativa nel primo ciclo di rilascio del 2021, aggiornamento 18.3. Per consentire agli utenti l'accesso a questa funzione, abilita aggiornamento della funzionalità **Salva set di dati del report in documento di Microsoft Excel** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management). Nel secondo ciclo di rilascio del 2021, questa funzione diventa permanente, quindi non dovrai abilitarla.

- Gli account utente avranno bisogno dell'autorizzazione **<!--Export Report Dataset To Excel-->Consenti l'azione Esporta set di dati del report in Excel**, che puoi applicare utilizzando il set di autorizzazioni **Strumenti per la risoluzione dei problemi** o **Esporta report in Excel**.  

- Non puoi esportare un report con più di 1.048.576 righe o 16.384 colonne.

    > [!NOTE]
    > Con Business Central in locale, il numero massimo di righe esportate potrebbe essere anche inferiore. Business Central Server include un'impostazione di configurazione, denominata **Numero massimo di righe di dati consentite per l'invio a Excel**, per diminuire il limite del valore massimo. Per ulteriori informazioni, vedi [Configurazione di Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) oppure contatta il tuo amministratore.

##### <a name="for-developers-and-advanced-users"></a>Per gli sviluppatori e gli utenti avanzati

L'opzione **Documento Microsoft Excel (solo dati)** esporta tutte le colonne, comprese le colonne che contengono filtri e istruzioni di formattazione per altri valori. Ecco alcuni punti di interesse:

- I dati binari in un campo, come un'immagine, non vengono esportati.

  Nelle colonne che contengono dati binari, i campi includeranno il testo **Dati binari ({0} byte)**, dove **{0}** indica il numero di byte.
- A partire dal secondo ciclo di rilascio di Business Central 2021, il file Excel include anche il foglio di lavoro **Metadati del report**.

  Questo foglio di lavoro mostra i filtri applicati al report e le proprietà generali del report, come il nome, l'ID e i dettagli dell'estensione. I filtri sono mostrati nella colonna **Filtro (DataItem::Table::FilterGroupNo::FieldName)**. I filtri in questa colonna includono i filtri impostati nella pagina di richiesta del report. Include anche i filtri definiti nel codice AL, ad esempio, dalla [proprietà DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) e dalla [proprietà DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Per ulteriori informazioni sulla progettazione del report, vedi [Panoramica dei report](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Alcuni report esportano i numeri come testo, il che impedisce di eseguire calcoli o utilizzare Power Pivot nelle celle del foglio di lavoro di Excel. Dopo l'esportazione, è una buona norma verificare i numeri nel foglio di lavoro. Se vuoi eseguire analisi e grafici sui numeri, cambia il formato delle celle rilevanti da **Testo** in **Numero**. Per ulteriori informazioni sulla formattazione dei numeri nelle celle, guarda questo video [Formattazione dei numeri nelle celle in Microsoft Excel](https://www.youtube.com/watch?v=2suE4YmZu_Q).

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Pianificazione dell'esecuzione di un report

È possibile pianificare l'esecuzione di un processo batch o di un report a una data e un'ora specifiche. I report e i processi batch pianificati vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse. Scegliere l'opzione **Programmazione** dopo aver scelto il pulsante **Invia a**, quindi immettere informazioni quali stampante, ora e data. Il report viene aggiunto alla coda processi e sarà eseguito alla data specificata. Quando il report viene elaborato, l'elemento verrà rimosso dalla coda commesse. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).  

Quando si pianifica l'esecuzione di un report, è possibile specificare che deve essere eseguito ogni giovedì impostando il campo **Prossima esecuzione formula della data** su *D4*, per esempio. Per ulteriori informazioni, vedere [Utilizzo di formule per le date](ui-enter-date-ranges.md#using-date-formulas).  

È possibile salvare il report in un file, come un file Excel, Word, PDF, o stamparlo, o solo generare il report. Se si sceglie di salvare il report in un file, il report elaborato viene inviato nell'area **Report elaborati** della Gestione ruolo utente, dove è possibile visualizzarlo.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Stampa di un report

Per stampare un report scegliere il pulsante **Stampa** nella pagina di richiesta o nella barra dei menu della pagina **Anteprima**.

### <a name="printer"></a><a name="Printer"></a>Stampante

Il campo **Stampante** nella pagina di richiesta del report mostra il nome della stampante a cui verrà inviato il report. Per cambiare una stampante, seleziona semplicemente la stampante dall'elenco.

> [!NOTE]
> **(Gestito dal browser)** indica che non esiste una stampante designata per il report. In questo caso, il browser gestirà la stampa e visualizzerà un'esperienza standard, in cui è possibile scegliere una stampante locale collegata al dispositivo. **(Gestito dal browser)** non è disponibile nell'app per dispositivi mobili [!INCLUDE[prod_short](includes/prod_short.md)] o nell'app per Microsoft Teams.

> [!TIP]
> La stampante selezionata per impostazione predefinita è configurata nella pagina **Selezioni della stampante**. Per informazioni sulla modifica della stampante predefinita, vedi [Per scegliere quali stampanti devono stampare quali report](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Stampa di report nella versione tailandese

Nella versione tailandese di [!INCLUDE[prod_short](includes/prod_short.md)], non è possibile stampare correttamente i report con il pulsante **Stampa** a causa delle limitazioni nel servizio che genera il file PDF stampabile. In alternativa, è possibile aprire il report in Word e quindi salvare il report come PDF stampabile.  

Oppure è possibile richiedere all'amministratore di creare un layout report Word per i report più utilizzati. Per ulteriori informazioni, vedere [Gestione dei layout di report e documento](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Modifica dei layout di report

Un layout di report determina le informazioni che verranno visualizzate nel report, nonché la disposizione e l'aspetto delle stesse. Se si desidera passare a un layout diverso, vedere [Modificare il layout del report corrente](ui-how-change-layout-currently-used-report.md) Per personalizzare un layout di report, vedere [Creare e modificare un layout di report personalizzato](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Opzioni avanzate

I campi in **Avanzate** impostano le limitazioni sul report generato per controllare le risorse della stampante. In genere non è necessario modificare queste impostazioni, a meno che il report non sia di grandi dimensioni. Se un report supera questi limiti quando si tenta di visualizzarlo in anteprima o stamparlo, viene visualizzato un messaggio che indica quale limite è stato superato. È quindi possibile modificare le impostazioni per adattarle al report. Ogni campo, tuttavia, ha un valore massimo che è necessario conoscere:

|Campo|Valore massimo|
|-----|-------------|
|Tempo massimo di rendering|12:00:00|
|Numero massimo di righe|1000000|
|Numero massimo documenti|500|

> [!NOTE]
> I valori massimi possono essere diversi per [!INCLUDE[prod_short](includes/prod_short.md)] in locale e un amministratore può modificarli. Per ulteriori informazioni, vedere [Configurazione di Business Central Server - Report](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Per una panoramica dei limiti dei report in [!INCLUDE[prod_short](includes/prod_short.md)] online, vedere [Limiti operativi](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Vedere anche

[Configurare le stampanti](ui-specify-printer-selection-reports.md)  
[Utilizzo di date e orari del calendario](ui-enter-date-ranges.md)  
[Gestione dei layout di report e documento](ui-manage-report-layouts.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]