---
title: Programmare l'esecuzione automatica di processi
description: I task programmati sono gestiti dalla coda processi. Questi processi eseguono report e codeunit. È possibile impostare processi da eseguire una sola volta o periodicamente.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '672, 673, 674, 671'
ms.date: 10/01/2021
ms.author: edupont
---
# Utilizzare le code processi per programmare i task

La pagina Movimenti coda processi consente agli utenti di programmare ed eseguire report e codeunit specifici. È possibile impostare processi da eseguire una sola volta o periodicamente. Ad esempio, è possibile eseguire il report **Venditore * Statistiche di vendita** settimanale per monitorare le vendite per venditore ogni settimana, oppure è possibile eseguire la codeunit **Delegare le richieste di approvazione** quotidianamente per evitare che i documenti si accumulino.

Nella pagina **Movimenti coda processi** sono elencati tutti i processi esistenti. Se aggiungi un nuovo movimento coda processi che vuoi pianificare, devi fornire alcune informazioni. Ad esempio:

* Il tipo di oggetto da eseguire, ad esempio un report o una codeunit. È necessario disporre dell'autorizzazione per eseguire il report o la codeunit particolare.
* Il nome e l'ID dell'oggetto. 
* I parametri per specificare il comportamento del movimento coda processi. Ad esempio, è possibile aggiungere un parametro per inviare solo ordini di vendita registrati. 
* Quando e con quale frequenza verrà eseguito il movimento coda processi.

> [!IMPORTANT]  
> Se hai il set di autorizzazioni SUPER assegnato con [!INCLUDE[prod_short](includes/prod_short.md)], disponi delle autorizzazioni per eseguire tutti gli oggetti inclusi nella licenza. Se hai il ruolo di amministratore con delega, puoi creare e pianificare i movimenti coda processi, ma solo gli amministratori e gli utenti con licenza possono eseguirli. Gli utenti con la licenza del dispositivo non possono creare o eseguire i movimenti coda processi.

Dopo la configurazione e l'esecuzione delle code processi, lo stato può cambiare come segue durante ogni periodo ricorrente:

* **In sospeso**  
* **Pronto**  
* **In corso**  
* **Errore**  
* **Completato**  

Dopo che un processo viene eseguito correttamente, viene rimosso dell'elenco dei movimenti coda processi a meno che non sia un processo ricorrente. Se è un processo ricorrente, il campo **Prima data/ora inizio** viene rettificato per mostrare la volta successiva in cui è prevista l'esecuzione del processo.  

## Monitorare lo stato o gli errori nella coda processi

I dati generati dalla coda processi vengono memorizzati nel database, in modo da poter risolvere gli errori relativi alla coda processi.  

Per ogni movimento coda processi, è possibile visualizzare e modificare lo stato. Quando si crea un movimento coda processi, il relativo stato è impostato su **In sospeso**. Ad esempio, è possibile impostare lo stato su **Pronto** e di nuovo su **In sospeso**. In caso contrario, le informazioni relative allo stato verranno aggiornate automaticamente.

La tabella seguente descrive i valori del campo **Stato**.

| Stato | Descrizione |
|--|--|
| Pronto | Il movimento coda processi è pronto per l'esecuzione. |
| In corso | Il movimento coda processi è in corso. Il campo viene aggiornato durante l'esecuzione della coda processi. |
| In sospeso | Lo stato predefinito del movimento coda processi quando viene creato. Selezionare l'azione **Imposta stato su Pronto** per modificare lo stato in **Pronto**. Scegli l'azione **Imposta in sospeso** per ripristinare lo stato **In sospeso**. |
| Errore | Si è verificato un errore. Seleziona **Mostra errore** per visualizzare il messaggio di errore. |
| Finito | Il movimento coda processi è stato completato. |

> [!Tip]  
> I movimenti coda processi smettono di essere eseguiti quando si verifica un errore. Ad esempio, questo può essere un problema quando un movimento si connette a un servizio esterno, come un feed bancario. Se il servizio non è temporaneamente disponibile e il movimento coda processi non riesce a connettersi, il movimento mostrerà un errore e interromperà l'esecuzione. Dovrai riavviare manualmente il movimento coda processi. In ogni caso, i campi **Numero massimo di tentativi** e **Ritardo nuova esecuzione (sec.)** possono aiutarti a evitare questa situazione. Il campo **Numero massimo di tentativi** ti consente di specificare quante volte il movimento coda processi può non riuscire prima che smetta di tentare di essere eseguito. Il campo **Ritardo nuova esecuzione (sec.)** ti consente di specificare la quantità di tempo, in secondi, tra i tentativi. La combinazione di questi due campi può mantenere in esecuzione il movimento coda processi finché il servizio esterno non diventa disponibile.

### Per visualizzare lo stato di qualsiasi processo

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Movimenti coda processi**, quindi scegli il collegamento correlato.
2. Nella pagina **Movimenti coda processi**, selezionare un movimento coda processi quindi scegliere il l'azione **Movimenti log**.  

> [!TIP]
> È inoltre possibile visualizzare lo stato dei movimenti della coda processi utilizzando Application Insights in Microsoft Azure per analisi più approfondite basate sulla telemetria. Per ulteriori informazioni, vedere [Monitoraggio e analisi della telemetria](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) e [Analisi della telemetria della traccia del ciclo di vita della coda processi](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) nel contenuto per sviluppatori e amministratori [!INCLUDE [prod_short](includes/prod_short.md)].

## Visualizza i compiti programmati

La pagina **Attività pianificate** in [!INCLUDE [prod_short](includes/prod_short.md)] mostra quali compiti sono pronti per essere eseguiti nella coda di lavoro. La pagina mostra anche informazioni sull'azienda in cui ogni compito è impostato per essere eseguito. Tuttavia, solo i compiti che sono contrassegnati come appartenenti all'ambiente corrente possono essere eseguiti.  

Ad esempio, tutte le attività pianificate vengono interrotte se l'azienda si trova in un ambiente che è una copia di un altro ambiente. Usa la pagina **Attività pianificate** per impostare le attività come pronte per l'esecuzione nella coda di lavoro.  

> [!NOTE]
> Gli amministratori interni e gli utenti con licenza possono programmare l'esecuzione di attività. Gli amministratori con delega possono impostare e pianificare le attività da eseguire, ma solo gli utenti con licenza possono eseguirle.

## Parte Coda processi

La parte **Coda processi** in Gestione ruolo utente mostra i movimenti delle code processi avviati, ma non ancora completati. Per impostazione predefinita, la parte non è visibile, ma puoi aggiungerla alla Gestione ruolo utente. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).  

La parte mostra le seguenti informazioni:

* Quali documenti con il tuo ID nel campo **ID utente assegnato** sono in fase di elaborazione o in coda, inclusi quelli relativi alla registrazione in background. 
* Se si è verificato un errore durante la registrazione di un documento o nel movimento coda processi. 

La parte Coda processi personali consente inoltre di annullare la registrazione del documento.

### Per visualizzare un errore dalla parte Coda processi

1. In un movimento con lo stato, **Errore**scegliere l'azione **Mostra errore**.
2. Analizzare il messaggio di errore e correggere il problema.

## Esempi di cosa può essere programmato utilizzando la coda processi

### Programmare report

È possibile programmare un report o un processo batch da eseguire a una data e un'ora specifiche. I report e i processi batch programmati vengono inseriti nella coda commesse e vengono elaborati all'orario pianificato, in maniera analoga alle altre commesse. Scegliere l'opzione **Programmazione** dopo aver scelto l'azione **Invia a**, quindi immettere informazioni quali stampante, ora e data, ricorrenza.  

Per ulteriori informazioni, vedere [Programmazione dell'esecuzione di un report](ui-work-report.md#ScheduleReport)

### Programmare la sincronizzazione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)]

Se hai integrato [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)], la coda processi ti consente di pianificare quando sincronizzare i dati. A seconda della direzione e delle regole che hai definito, il movimento coda processi può creare record in un'app in modo che corrispondano ai record nell'altra. Un buon esempio è quando registri un contatto in [!INCLUDE[crm_md](includes/crm_md.md)], il movimento coda processi può impostare quel contatto per te in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Programmazione di una sincronizzazione tra Business Central e Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)

### Programmare la registrazione delle vendite e gli ordini acquisto

È possibile utilizzare i movimenti coda processi per pianificare l'esecuzione in background dei processi aziendali. Ad esempio, le attività in background sono utili quando più utenti registrano ordini di vendita contemporaneamente, ma può essere elaborato solo un ordine alla volta. Per ulteriori informazioni, vedere [Per configurare la registrazione background con le code processi](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## Monitorare la coda processi con la telemetria

In qualità di amministratore, è possibile usare [Application Insights](/azure/azure-monitor/app/app-insights-overview) per raccogliere e analizzare i dati di telemetria da utilizzare per identificare i problemi. Per ulteriori informazioni, vedere [Monitoraggio e analisi della telemetria](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) nel contenuto per sviluppatori e amministratori.  

## Vedere anche

[Amministrazione](admin-setup-and-administration.md)  
[Impostazione di Business Central](setup.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Analizzare la telemetria della traccia del ciclo di vita della coda processi](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]