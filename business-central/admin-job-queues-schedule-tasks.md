---
title: Programmare l'esecuzione automatica di processi
description: I task programmati sono gestiti dalla coda processi. Questi processi eseguono report e codeunit. È possibile impostare processi da eseguire una sola volta o periodicamente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b1d9893364d7472759a478877ebec49ace5e9647
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441295"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Utilizzare le code processi per programmare i task

Le code processi in [!INCLUDE[prod_short](includes/prod_short.md)] consentono agli utenti di programmare ed eseguire report e codeunit specifici. È possibile impostare processi da eseguire una sola volta o periodicamente. Ad esempio, è possibile voler eseguire il report **Venditore * Statistiche di vendita** settimanale per monitorare le vendite per venditore ogni settimana, oppure è possibile voler eseguire la codeunit **Delegare le richieste di approvazione** quotidianamente per evitare che i documenti si accumulino o altrimenti blocchino il flusso di lavoro.

Nella pagina **Movimenti coda processi** sono elencati tutti i processi esistenti. Se si aggiunge un nuovo movimento coda processi che si desidera programmare, è necessario specificare informazioni sul tipo di oggetto che si intende eseguire, ad esempio un report o una codeunit, e il nome e l'ID dell'oggetto da eseguire. È inoltre possibile aggiungere i parametri per specificare il comportamento del movimento coda processi. Ad esempio, è possibile aggiungere un parametro per inviare solo ordini di vendita registrati. È necessario disporre delle autorizzazioni per eseguire un report o una codeunit particolare oppure verrà restituito un errore quando la coda processi viene eseguita.  
> [!IMPORTANT]  
> Se si utilizza il set di autorizzazioni SUPER fornito con [!INCLUDE[prod_short](includes/prod_short.md)], la società e gli utenti dispongono delle autorizzazioni per eseguire tutti gli oggetti nella licenza. Ciò non è ancora sufficiente per gli amministratori delegati o gli utenti con licenza per dispositivo, che non possono creare movimenti coda processi.

Una coda processi può avere più movimenti, che rappresentano i processi gestiti ed eseguiti dalla coda. Le informazioni nel movimento specificano quale codeunit o report viene eseguito, quando e con quale frequenza il movimento viene eseguito, in quale categoria viene eseguito il processo e le relative modalità di esecuzione.  

Dopo la configurazione e l'esecuzione delle code processi, lo stato può cambiare come segue durante ogni periodo ricorrente:

* **In sospeso**  
* **Pronto**  
* **In corso**  
* **Errore**  
* **Completato**  

Dopo che un processo viene eseguito correttamente, viene rimosso dell'elenco dei movimenti coda processi a meno che non sia un processo ricorrente. Se è un processo ricorrente, il campo **Prima data/ora inizio** viene rettificato per mostrare la volta successiva in cui è prevista l'esecuzione del processo.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Per visualizzare lo stato o gli errori nella coda processi

I dati generati quando una coda processi viene eseguita sono memorizzati nel database, in modo da poter risolvere gli errori relativi alla coda processi.  
Per ogni movimento coda processi, è possibile visualizzare e modificare lo stato. Quando si crea un movimento coda processi, il relativo stato è impostato su **In sospeso**. Ad esempio, è possibile impostare lo stato su **Pronto** e di nuovo su **In sospeso**. In caso contrario, le informazioni relative allo stato verranno aggiornate automaticamente.

La tabella seguente descrive i valori del campo **Stato**.

| Stato | Descrizione |
|--|--|
| Pronto | Indica che il movimento coda processi è pronto per l'esecuzione. |
| In corso | Indica che il movimento coda processi è in corso. Il campo viene aggiornato durante l'esecuzione della coda processi. |
| In sospeso | Default. Indica lo stato del movimento coda processi quando viene creato. Selezionare l'azione **Imposta stato su Pronto** per modificare lo stato in **Pronto**. Selezionare le azioni **Imposta in sospeso** o **Sospendi** per modificare di nuovo lo stato a **In sospeso**. |
| Errore | Indica che è presente un errore. Selezionare **Mostra errore** per visualizzare il messaggio di errore. |
| Completato | Indica che il movimento coda processi è stato completato. |

### <a name="to-view-status-for-any-job"></a>Per visualizzare lo stato di qualsiasi processo
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti coda processi**, quindi scegli il collegamento correlato.
2. Nella pagina **Movimenti coda processi**, selezionare un movimento coda processi quindi scegliere il l'azione **Movimenti log**.  

> [!TIP]
> Con [!INCLUDE [prod_short](includes/prod_short.md)] online, è anche possibile visualizzare lo stato dei movimenti coda processi utilizzando Application Insights in Microsoft Azure. Per ulteriori informazioni, vedere [Analizzare la telemetria della traccia del ciclo di vita della coda processi](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) nel contenuto per [!INCLUDE [prod_short](includes/prod_short.md)] per sviluppatori e amministrazione.

## <a name="the-my-job-queue-part"></a>Parte Coda processi
La parte **Coda processi** in Gestione ruolo utente mostra i movimenti delle code processi avviati da un utente, ma non ancora completati. Per impostazione predefinita, la parte non è visibile, pertanto è necessario aggiungerla alla Gestione ruolo utente utilizzata. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).  

La parte mostra quali documenti con il proprio ID nel campo **ID utente assegnato** sono in fase di elaborazione o in coda, inclusi quelli relativi alla registrazione in background. La parte indica immediatamente se si è verificato un errore durante la registrazione di un documento oppure se sono presenti errori in un movimento coda processi. La parte consente inoltre di annullare la registrazione del documento se non è in esecuzione.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Per visualizzare un errore dalla parte Coda processi
1. In un movimento con lo stato, **Errore** scegliere l'azione **Mostra errore**.
2. Analizzare il messaggio di errore e correggere il problema.


## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Esempi di cosa può essere programmato utilizzando la coda processi

### <a name="schedule-reports"></a>Programmare report

È possibile programmare un report o un processo batch da eseguire a una data e un'ora specifiche. I report e i processi batch programmati vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse. Scegliere l'opzione **Programmazione** dopo aver scelto l'azione **Invia a**, quindi immettere informazioni quali stampante, ora e data, ricorrenza.  

Per ulteriori informazioni, vedere [Programmazione dell'esecuzione di un report](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Programmare la sincronizzazione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)]

Se si è integrato [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)], è possibile utilizzare la coda processi per programmare quando si intende sincronizzare i dati per i record che sono stati associati nelle due app aziendali. A seconda della direzione e delle regole definite per l'integrazione, i processi di sincronizzazione possono anche creare nuovi record nell'app di destinazione in modo che corrispondano a quelli nell'origine. Ad esempio, se un venditore crea un nuovo contatto in [!INCLUDE[crm_md](includes/crm_md.md)], il processo di sincronizzazione può creare quel contatto per il venditore associato in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Programmazione di una sincronizzazione tra Business Central e Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Programmare la registrazione delle vendite e gli ordini acquisto

Le code processi sono un efficace strumento per programmare l'esecuzione dei processi aziendali in background, ad esempio quando più utenti tentano di registrare gli ordini di vendita, ma un solo ordine può essere elaborato alla volta.  

Per ulteriori informazioni, vedere [Per configurare la registrazione background con le code processi](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## <a name="see-also"></a>Vedere anche

[Amministrazione](admin-setup-and-administration.md)  
[Impostazione di Business Central](setup.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Analizzare la telemetria della traccia del ciclo di vita della coda processi](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]