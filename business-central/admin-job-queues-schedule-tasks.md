---
title: Programmare l'esecuzione automatica di processi | Microsoft Docs
description: I task pianificati sono gestiti dalla coda processi. Questi processi eseguono report e codeunit. È possibile impostare processi da eseguire una sola volta o periodicamente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 1cf5b75bc63acfa07a90cda1d03f45579a0aa51d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "935377"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Utilizzare le code processi per pianificare i task
Le code processi in [!INCLUDE[d365fin](includes/d365fin_md.md)] consentono agli utenti di pianificare ed eseguire report e codeunit specifici. È possibile impostare processi da eseguire una sola volta o periodicamente. Potrebbe essere necessario, ad esempio, eseguire il report **Agente - Statistiche vendita** ogni settimana, per tenere traccia delle vendite effettuate da un agente ogni settimana, oppure eseguire la codeunit **Elabora coda e-mail assistenza** ogni giorno, per verificare che i messaggi di posta elettronica in sospeso relativi agli ordini di assistenza vengano inviati ai clienti in modo tempestivo.

Nella pagina **Movimenti coda processi** sono elencati tutti i processi esistenti. Se si aggiunge un nuovo movimento coda processi che si desidera pianificare, è necessario specificare informazioni sul tipo di oggetto che si intende eseguire, ad esempio un report o una codeunit, e il nome e l'ID dell'oggetto da eseguire. È inoltre possibile aggiungere i parametri per specificare il comportamento del movimento coda processi. Ad esempio, è possibile aggiungere un parametro per inviare solo ordini di vendita registrati. È necessario disporre delle autorizzazioni per eseguire un report o una codeunit particolare oppure verrà restituito un errore quando la coda processi viene eseguita.  

Una coda processi può avere più movimenti, che rappresentano i processi gestiti ed eseguiti dalla coda. Le informazioni nel movimento specificano quale codeunit o report viene eseguito, quando e con quale frequenza il movimento viene eseguito, in quale categoria viene eseguito il processo e le relative modalità di esecuzione.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Per configurare la registrazione background con le code processi
Le code processi sono un efficace strumento per pianificare l'esecuzione dei processi aziendali in background, ad esempio quando più utenti tentano di registrare gli ordini di vendita, ma un solo ordine può essere elaborato alla volta. In alternativa, è possibile pianificare le registrazioni nelle ore in cui è conveniente per la propria organizzazione. Ad esempio, può avere senso nella propria l'attività commerciale eseguire determinate procedure quando si è conclusa la maggior parte dell'immissione dati del giorno.

Per riuscirci, impostare la coda processi sull'esecuzione di diversi report di registrazione tramite processo batch, come i report **Registra batch ordini vendite**, **Registra batch fatture vendita**, **Batch reg. ordini resi vendita** e **Agg. batch note di cr. vend.**. Per ulteriori informazioni, vedere [Creare un movimento coda processi per la registrazione in background di ordini di vendita](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders)  

[!INCLUDE[d365fin](includes/d365fin_md.md)] supporta la registrazione in background per tutti i documenti di vendita, acquisto e assistenza.

La procedura seguente illustra come configurare la registrazione in background di ordini di vendita. I passaggi sono simili per l'acquisto e l'assistenza.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità clienti e vendite** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup contabilità clienti e vendite**, selezionare la casella di controllo **Registra mediante coda processi**.
3. Per filtrare i movimenti coda processi per la registrazione degli ordini di vendita, scegliere **Codice categoria coda processi** e selezionare la categoria **SalesPost**.

    Viene creato un oggetto di coda processi, codeunit 88 **Registrazione vendita via coda processi**. Continuare per attivarlo nella pagina **Movimento coda coda processi**.
4. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Movimenti coda processi** e quindi scegliere il collegamento correlato.
5. Nella pagina **Movimenti coda processi**, scegliere l'azione **Nuovo**.
6. Nel campo **Tipo di oggetto da eseguire**, selezionare **Codeunit**.  
7. Nel campo **ID oggetto da eseguire**, selezionare 88, **Registrazione vendita via coda processi**.

    Non vi sono altri campi pertinenti per questo scenario.
8. Scegliere l'azione **Imposta stato su Pronto**.
9. Per verificare che la coda processi stia funzionando come previsto, registrare un ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
10. Verificare nella pagina **Voci log coda processi** se l'ordine di vendita è stato registrato correttamente. Per ulteriori informazioni, vedere [Per visualizzare lo stato o gli errori nella coda processi](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Se anche i documenti di vendita devono essere stampati al momento della registrazione, selezionare la casella di controllo **Registra e stampa mediante coda processi** nella pagina **Setup contabilità clienti e vendite**.  

> [!IMPORTANT]  
> Se si imposta un processo che prevede la registrazione e la stampa di documenti e nella stampante viene visualizzata una finestra di dialogo, ad esempio una richiesta di credenziali o un avvertimento sul basso livello di inchiostro della stampante, il documento viene registrato ma non stampato. Il movimento coda processi corrispondente alla fine incorre in un timeout e il campo **Stato** viene impostato su **Errore**. Di conseguenza, è consigliabile non utilizzare un setup di stampante che richieda l'interazione con la visualizzazione delle finestre di dialogo della stampante insieme alla registrazione in background.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Per creare un movimento coda processi per la registrazione batch di ordini di vendita
La seguente procedura illustra come impostare il report **Registra batch ordini vendite** per registrare automaticamente gli ordini di vendita rilasciati alle ore 16 nei giorni della settimana.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Movimenti coda processi** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Tipo oggetto da eseguire**, selezionare **Report**.  
4. Nel campo **ID oggetto da eseguire**, selezionare 296, **Registra batch ordini vendite**.
5. Selezionare la casella controllo **Pagina di richiesta report**.
6. Nella pagina di richiesta **Registra batch ordini vendite**, definire cosa includere durante la registrazione automatica di ordini di vendita quindi scegliere il pulsante **OK**.
7. Selezionare tutte le caselle di controllo da **Esegui di Lunedì** a **Esegui di Venerdì**.
8. Nel campo **Ora inizio**, immettere 16.
9. Scegliere l'azione **Imposta stato su Pronto**.

Gli ordini di vendita pronti per essere registrati saranno registrati ogni giorno della settimana alle ore 16.

> [!NOTE]
> Se la coda processi non può registrare l'ordine di vendita, lo stato viene modificato in **Errore** e l'ordine di vendita viene aggiunto all'elenco degli ordini di vendita che l'utente deve gestire manualmente. Per ulteriori informazioni, vedere [Per visualizzare lo stato o gli errori nella coda processi](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Dopo la configurazione e l'esecuzione delle code processi, lo stato può cambiare come segue durante ogni periodo ricorrente:

* **In sospeso**  
* **Pronto**  
* **In corso**  
* **Errore**  
* **Completato**  

Dopo che un processo viene eseguito correttamente, viene rimosso dell'elenco dei movimenti coda processi a meno che non sia un processo ricorrente. Se è un processo ricorrente, il campo **Prima data/ora inizio** viene rettificato per mostrare la volta successiva in cui è prevista l'esecuzione del processo.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Per visualizzare lo stato o gli errori nella coda processi
I dati generati quando una coda processi viene eseguita sono memorizzati nel database, in modo da poter risolvere gli errori relativi alla coda processi.

### <a name="to-view-status-for-any-job"></a>Per visualizzare lo stato di qualsiasi processo
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Movimenti coda processi** e quindi scegliere il collegamento correlato.
2. Nella pagina **Movimenti coda processi**, selezionare un movimento coda processi quindi scegliere il l'azione **Movimenti log**.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Per visualizzare lo stato di un documento di vendita o di acquisto
1. Dal documento che si è tentato di registrare con la coda processi, scegliere il campo **Stato coda processi**, che conterrà **Errore**.
2. Analizzare il messaggio di errore e correggere il problema.

## <a name="the-my-job-queue-part"></a>Parte Coda processi
La parte **Coda processi** in Gestione ruolo utente mostra i movimenti delle code processi avviati da un utente, ma non ancora completati. Per impostazione predefinita, la parte non è visibile, pertanto è necessario aggiungerla alla Gestione ruolo utente utilizzata. Per ulteriori informazioni, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).  

La parte mostra quali documenti con il proprio ID nel campo **ID utente assegnato** sono in fase di elaborazione o in coda, inclusi quelli relativi alla registrazione in background. La parte indica immediatamente se si è verificato un errore durante la registrazione di un documento oppure se sono presenti errori in un movimento coda processi. La parte consente inoltre di annullare la registrazione del documento se non è in esecuzione.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Per visualizzare un errore dalla parte Coda processi
1. In un movimento con lo stato, **Errore**scegliere l'azione **Mostra errore**.
2. Analizzare il messaggio di errore e correggere il problema.

## <a name="security"></a>Protezione  
I movimenti coda processi vengono eseguiti in base alle autorizzazioni. Le autorizzazioni devono consentire l'esecuzione del report oppure della codeunit.  

Quando una coda processi è attivata manualmente, viene eseguita con le credenziali dell'utente. Quando una coda processi è attivata come un task pianificato, viene eseguita con le credenziali dell'istanza server. Quando si esegue un processo, viene eseguito con le credenziali della coda processi che ne esegue l'attivazione. Tuttavia, all'utente che ha creato il movimento coda processi è inoltre necessario disporre dei permessi. Quando un processo viene "eseguito nella sessione utente" (ad esempio durante la registrazione background), viene eseguito con le credenziali dell'utente che ha creato il processo.  

> [!IMPORTANT]  
>  Se si utilizza il set di autorizzazioni SUPER fornito con [!INCLUDE[d365fin](includes/d365fin_md.md)], la società e gli utenti dispongono delle autorizzazioni per eseguire tutti gli oggetti. In questo caso, l'accesso per ogni utente è limitato solo dalle autorizzazioni per i dati.  

## <a name="using-job-queues-effectively"></a>Utilizzo delle code processi in modo efficace  
Il record del movimento coda processi ha molti campi di cui lo scopo è quello di portare i parametri in una codeunit specificata per essere eseguita con una coda processi. Questo significa inoltre che le codeunit che devono essere eseguite mediante la coda processi devono essere specificate con il record Movimento coda processi come parametro nel trigger **OnRun**. Cio fornisce un livello di sicurezza aggiuntivo, poiché impedisce agli utenti di eseguire codeunit scelte casualmente tramite la coda processi. Se l'utente deve necessariamente passare i parametri a un report, l'unico modo possibile è eseguire il wrapping dell'esecuzione del report in una codeunit, che analizzerà i parametri di input e li immetterà nel report prima dell'esecuzione.  

## <a name="see-also"></a>Vedi anche  
[Amministrazione](admin-setup-and-administration.md)  
[Impostazione di Business Central](setup.md)  
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
