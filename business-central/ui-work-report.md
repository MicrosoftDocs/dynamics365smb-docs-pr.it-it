---
title: Programmazione dell'esecuzione di un report per una data e un'ora specifiche | Documenti Microsoft
description: Informazioni su come inserire un report in una coda di processi e programmare per l'elaborazione per una data e un'ora specifiche.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 81df1625531b3b4c5bf1a55a9e09d37af8b6f7fe
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782986"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Utilizzo di report, processi batch e XMLport

Un report raccoglie informazioni basate su un set di criteri specificato e organizza e presenta le informazioni in un formato facile da leggere e che è possibile stampare o salvare come file. Sono disponibili molti report a cui è possibile accedere dall'applicazione. I report in genere forniscono informazioni relative al contesto della pagina visualizzata. Ad esempio, la pagina **Cliente** include i report per i principali 10 clienti, statistiche di vendita e altro ancora.

I processi batch e XMLport eseguono più o meno gli stessi report ma per eseguire un processo o esportare dati. Ad esempio, il processo batch **Crea solleciti** crea documenti di sollecito per clienti con pagamenti scaduti.  

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

    È possibile copiare il testo di un report e incollarlo altrove, come una pagina in [!INCLUDE[prod_short](includes/prod_short.md)] o Microsoft Word.  Ad esempio, tenere premuto il pulsante del mouse sul punto da cui si desidera iniziare, quindi spostare il mouse per selezionare una o più parole, frasi o paragrafi. Premere il pulsante destro del mouse e selezionare **Copia**. Quindi incollare il testo selezionato nella posizione desiderata.
- Panoramica del documento

    È possibile spostare l'area visibile del report in qualsiasi direzione in modo da poter visualizzare altre aree o il report. La panoramica risulta utile quando è stato eseguito l'ingrandimento per visualizzare i dettagli.  Ad esempio, tenere premuto il pulsante del mouse su un punto dell'anteprima del report, quindi spostare il mouse.

- Scaricare in un file PDF sul computer o in rete.
- Stampa

## <a name="saving-a-report"></a>Salvataggio di un report

È possibile salvare un report in un documento PDF, documento di Microsoft Word o documento di Microsoft Excel scegliendo il pulsante **Invia a** ed effettuando la scelta desiderata.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Pianificazione dell'esecuzione di un report

È possibile pianificare l'esecuzione di un processo batch o di un report a una data e un'ora specifiche. I report e i processi batch pianificati vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse. Scegliere l'opzione **Programmazione** dopo aver scelto il pulsante **Invia a**, quindi immettere informazioni quali stampante, ora e data. Il report viene aggiunto alla coda processi e sarà eseguito alla data specificata. Quando il report viene elaborato, l'elemento verrà rimosso dalla coda commesse. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).  

Quando si pianifica l'esecuzione di un report, è possibile specificare che deve essere eseguito ogni giovedì impostando il campo **Prossima esecuzione formula della data** su *D4*, per esempio. Per ulteriori informazioni, vedere [Utilizzo di formule per le date](ui-enter-date-ranges.md#using-date-formulas).  

È possibile salvare il report in un file, ad esempio un file Excel, Word, PDF, o stamparlo con una stampante selezionata, o solo generare il report. Se si sceglie di salvare il report in un file, il report elaborato viene inviato nell'area **Report elaborati** della Gestione ruolo utente, dove è possibile visualizzarlo.  

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