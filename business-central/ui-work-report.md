---
title: Programmazione dell'esecuzione di un report per una data e un'ora specifiche | Documenti Microsoft
description: Informazioni su come inserire un report in una coda di processi e programmare per l'elaborazione per una data e un'ora specifiche.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 709e444d185e6950d6367036db622b30c8062f25
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310614"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Utilizzo di report, processi batch e XMLport
Un report raccoglie informazioni basate su un set di criteri specificato e organizza e presenta le informazioni in un formato facile da leggere e che è possibile stampare o salvare come file. Sono disponibili molti report a cui è possibile accedere dall'applicazione. I report in genere forniscono informazioni relative al contesto della pagina visualizzata. Ad esempio, la pagina **Cliente** include i report per i principali 10 clienti, statistiche di vendita e altro ancora.

I processi batch e XMLport eseguono più o meno gli stessi report ma per eseguire un processo o esportare dati. Ad esempio, il processo batch **Crea solleciti** crea documenti di sollecito per clienti con pagamenti scaduti.  

> [!NOTE]
> Questo argomento fa essenzialmente riferimento a “report" ma informazioni simili si applicano ai processi batch e a XMLport.

I report sono disponibili nella scheda **Reports** elle pagine selezionate oppure è possibile utilizzare una ricerca tramite l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") per individuare i report per nome.

## <a name="specifying-the-data-to-include-in-reports"></a>Specificare la data da includere nei report
Quando si apre un report, processo batch o XMLport, viene di norma visualizzata una pagina di richiesta dove è possibile impostare varie opzioni e filtri che determinano cosa includere nel report.

È possibile impostare i filtri in un report più o meno nello stesso modo in cui si impostano i filtri negli elenchi. Per ulteriori informazioni, vedere [Filtri](ui-enter-criteria-filters.md#-filtering).

> [!Caution]
> La sezione **Filtra elenco per** in una pagina di richiesta fornisce una generica capacità di filtro per i report. Tali filtri sono facoltativi.<br /><br /> Alcuni report ignoreranno tali filtri, nel senso che qualsiasi filtro venga impostato nella sezione **Filtra elenco per**, l'output del report è lo stesso. Non è possibile fornire un elenco dei campi che vengono ignorati in quali report, quindi sarà necessario sperimentare con i filtri quando utilizzati.<br /><br />
**Esempio**: quando si utilizza il processo batch **Crea solleciti**, un filtro per il campo **Movimenti contabili clienti** di **Livello ultimo sollecito emesso** verrà ignorato perché i filtri sono fissi per tale processo batch.

## <a name="SavedSettings"></a>Uso delle impostazioni salvate
La pagina di richiesta può includere la sezione **Impostazioni salvate** contenente uno o più voci nella casella **Utilizza valori predefiniti da**. Le Impostazioni salvate sono fondamentalmente un gruppo di default di opzioni e filtri che si possono applicare al report prima di visualizzarlo in anteprima o inviarlo in un file. Esiste sempre una voce Impostazioni salvate, che viene chiamata **Filtri e opzioni utilizzati di recente**. Questa voce imposta il report per utilizzare le opzioni e i filtri che sono stati utilizzati l'ultima volta che è stato utilizzato il report.

L'utilizzo delle impostazioni salvate è un metodo rapido e affidabile di generare coerentemente report contenenti dati corretti. Dopo aver impostato la casella **Utilizza valori predefiniti da** su una voce di impostazione salvata, è possibile modificare le opzioni e i filtri prima di visualizzare in anteprima o di salvare il report. Le modifiche effettuate non verranno salvate nella voce di impostazione salvata selezionata, ma verranno salvate in **Filtri e opzioni utilizzati più di recente**.

>[!NOTE]
>In qualità di amministratore, è possibile creare e gestire le impostazioni salvate per i report di tutti gli utenti. Per ulteriori informazioni, vedere [Gestire impostazioni salvate per report e processi batch](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Anteprima di un report
Scegliere il pulsante **Anteprima** per visualizzare il report. Utilizzare la barra dei menu nell'anteprima del report per:

-   Spostarsi tra le pagine
-   Ingrandire o ridurre
-   Ridimensionare per adattare alla pagina
-   Seleziona testo

    È possibile copiare il testo di un report e incollarlo altrove, come una pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)] o Microsoft Word.  Ad esempio, tenere premuto il pulsante del mouse sul punto da cui si desidera iniziare, quindi spostare il mouse per selezionare una o più parole, frasi o paragrafi. È quindi possibile premere il pulsante destro del mouse e selezionare **Copia**. È possibile quindi incollare il testo selezionato nella posizione desiderata.
-   Panoramica del documento

    È possibile spostare l'area visibile del report in qualsiasi direzione in modo da poter visualizzare altre aree o il report. Ciò risulta utile quando è stato eseguito l'ingrandimento per visualizzare i dettagli.  Ad esempio, tenere premuto il pulsante del mouse su un punto dell'anteprima del report, quindi spostare il mouse.

-   Scaricare in un file PDF sul computer o in rete.
-   Stampa

## <a name="saving-a-report"></a>Salvataggio di un report
È possibile salvare un report in un documento PDF, documento di Microsoft Word o documento di Microsoft Excel scegliendo il pulsante **Invia a** ed effettuando la scelta desiderata.

## <a name="ScheduleReport"></a> Pianificazione dell'esecuzione di un report
È possibile pianificare l'esecuzione di un processo batch o di un report a una data e un'ora specifiche. I report e i processi batch pianificati vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse. Scegliere l'opzione **Programmazione** dopo aver scelto il pulsante **Invia a**, quindi immettere informazioni quali stampante, ora e data. Il report viene aggiunto alla coda processi e sarà eseguito alla data specificata. Quando il report viene elaborato, l'elemento verrà rimosso dalla coda commesse. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

È possibile salvare il report elaborato in un file, ad esempio un file Excel, Word, PDF, o stamparlo con una stampante selezionata, o semplicemente elaborare il report. Se si sceglie di salvare il report in un file, il report elaborato viene inviato nell'area **Report elaborati** della Gestione ruolo utente, dove è possibile visualizzarlo.

## <a name="PrintReport"></a>Stampa di un report
È possibile stampare un report usando il pulsante **Stampa** nella pagina Oopzioni che appare quando si apre il report o dalla barra dei menu in Anteprima.  

### <a name="printing-reports-in-thai"></a>Stampa di report nella versione tailandese
Nella versione tailandese di [!INCLUDE[prodshort](includes/prodshort.md)], non è possibile stampare correttamente i report con il pulsante **Stampa** a causa delle limitazioni nel servizio che genera il file PDF stampabile. In alternativa, è possibile aprire il report in Word e quindi salvare il report come PDF stampabile.  

Oppure è possibile richiedere all'amministratore di creare un layout report Word per i report più utilizzati. Per ulteriori informazioni, vedere [Gestione dei layout di report e documento](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Modifica dei layout di report
Un layout di report determina le informazioni che verranno visualizzate nel report, nonché la disposizione e l'aspetto delle stesse. Se si desidera passare a un layout diverso, vedere [Modificare il layout del report corrente](ui-how-change-layout-currently-used-report.md) Per personalizzare un layout di report, vedere [Creare e modificare un layout di report personalizzato](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Vedere anche
[Specificare la selezione della stampante per i report](ui-specify-printer-selection-reports.md)  
[Utilizzo di date e orari del calendario](ui-enter-date-ranges.md)  
[Gestione dei layout di report e documento](ui-manage-report-layouts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
