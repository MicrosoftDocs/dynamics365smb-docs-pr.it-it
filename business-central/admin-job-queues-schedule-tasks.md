---
title: Programmare l'esecuzione automatica di processi | Microsoft Docs
description: "I task pianificati sono gestiti dalla coda processi. Questi processi eseguono report e codeunit. È possibile impostare commesse da eseguire una sola volta o periodicamente."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ad0f99509ff1a191c62dd1c3a6d569c9884ea851
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Utilizzare le code processi per pianificare i task
Le code processi in [!INCLUDE[d365fin](includes/d365fin_md.md)] consentono agli utenti di pianificare ed eseguire report e codeunit specifici. È possibile impostare commesse da eseguire una sola volta o periodicamente. Potrebbe essere necessario, ad esempio, eseguire il report **Agente - Statistiche vendita** ogni settimana, per tenere traccia delle vendite effettuate da un agente ogni settimana, oppure eseguire la codeunit **Elabora coda e-mail assistenza** ogni giorno, per verificare che i messaggi di posta elettronica in sospeso relativi agli ordini di assistenza vengano inviati ai clienti in modo tempestivo.  

## <a name="add-jobs-to-the-job-queue"></a>Aggiungere processi alla coda processi
Nella pagina **Movimenti coda processi** sono elencati tutti i processi esistenti. Se si aggiunge un nuovo movimento coda processi che si desidera pianificare, è necessario specificare informazioni sul tipo di oggetto che si intende eseguire, ad esempio un report o una codeunit, e il nome e l'ID dell'oggetto da eseguire. È inoltre possibile aggiungere i parametri per specificare il comportamento del movimento coda processi. Ad esempio, è possibile aggiungere un parametro per inviare solo ordini di vendita registrati. È necessario disporre delle autorizzazioni per eseguire un report o una codeunit particolare oppure verrà restituito un errore quando la coda processi viene eseguita.  

In alternativa, è possibile impostare un filtro nel campo **Filtro categoria coda processi**. Le categorie della coda processi possono essere utilizzate per raggruppare i processi nell'elenco.

[!INCLUDE[d365fin](includes/d365fin_md.md)] esegue automaticamente i processi in base alle pianificazioni specificate per ogni movimento coda processi. È inoltre possibile avviare, arrestare e sospendere manualmente un movimento coda processi.

### <a name="log-files"></a>File log
Gli errori vengono elencati nella pagina **Movimenti log coda processi** accessibile dalla barra multifunzione. È possibile anche risolvere gli errori della coda processi. I dati generati quando viene eseguita una coda processi vengono archiviati nel database.  

### <a name="background-posting-with-job-queues"></a>Registrazione background con le code processi
Le code processi sono uno strumento efficace per pianificare l'esecuzione dei processi aziendali in background. Ad esempio, potrebbe esserci un'istanza in cui più utenti stanno tentando di registrare ordini di vendita contemporaneamente, ma può essere elaborato solo un ordine alla volta. Impostando una routine di registrazione background, è possibile inserire le registrazioni in una coda per l'elaborazione in background.  

 In alternativa, è possibile pianificare le registrazioni nelle ore in cui è conveniente per la propria organizzazione. Ad esempio, può avere senso nella propria l'attività commerciale eseguire determinate procedure quando si è conclusa la maggior parte dell'immissione dati del giorno. Per riuscirci, impostare la coda commesse sull'esecuzione di diversi report di registrazione tramite processo batch, come i report **Registra ordini vendite tramite processo batch**, **Registra fatture vendita tramite processo batch** e **Agg. note di cr. vend. tramite processo batch**.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta la registrazione background per i seguenti tipi di documento:  

-   Vendite: ordine di vendita, ordine di reso, nota di credito, fattura  

-   Acquisti: ordine di acquisto, ordine di reso, nota di credito, fattura  

 Se la coda processi non può registrare l'ordine di vendita, lo stato viene modificato in **Errore** e l'ordine di vendita viene aggiunto all'elenco degli ordini di vendita che l'utente dovrà gestire.  

> [!NOTE]  
>  Quando viene programmato un documento per la registrazione e inizia il processo di registrazione, la routine di registrazione viene configurata automaticamente affinché scada entro due ore se la routine di registrazione smette di rispondere per un motivo qualsiasi.  

Questa impostazione relativa alla coda processi viene eseguita nella pagina **Setup contabilità clienti e vendite** o nella pagina **Contabilità fornitori**. Nella Scheda dettaglio **Registrazione background**, scegliere la casella di controllo **Contabilizza documenti tramite la coda processi** e immettre le informazioni pertinenti. È inoltre possibile selezionare il campo **Codice categoria coda processi** per eseguire tutti i movimenti coda processi con tale codice. Ad esempio, è possibile utilizzare la categoria **Regvend** per filtrare tutti gli ordini di vendita che corrispondono alla coda processi che presenta lo stesso codice categoria.  

> [!IMPORTANT]  
>  Se si imposta un processo che prevede la registrazione e la stampa di documenti e nella stampante viene visualizzata una finestra di dialogo, ad esempio una richiesta di credenziali o un avvertimento sul basso livello di inchiostro della stampante, il documento viene registrato ma non stampato. Il movimento coda processi corrispondente alla fine incorre in un timeout e il campo **Stato** viene impostato su **Errore**. Di conseguenza, è consigliabile non utilizzare un setup di stampante che richieda l'interazione con la visualizzazione delle finestre di dialogo della stampante insieme alla registrazione in background.  

## <a name="use-the-my-job-queue-part"></a>Utilizzare la parte Coda processi
Nella parte **Coda processi** sono riportati i movimenti delle code processi iniziati da un utente, ma non ancora completati. Per impostazione predefinita, la parte non è visibile, pertanto è necessario aggiungerla alla Gestione ruolo utente utilizzata. Per ulteriori informazioni, vedere [Modifica delle impostazioni di base](ui-change-basic-settings.md).  

In questa parte, è possibile visualizzare i documenti che sono stati elaborati, o che sono in coda, per cui è stato specificato il proprio ID nel campo **ID utente assegnato**. La parte consente di tenere traccia di tutti i movimenti della coda commesse, inclusi quelli relativi alla registrazione background. La parte indica immediatamente se si è verificato un errore durante la registrazione di un documento oppure se sono presenti errori in un movimento coda commesse. La parte consente inoltre di annullare la registrazione del documento se non è in esecuzione.  

## <a name="security"></a>Protezione  
I movimenti coda processi vengono eseguiti in base alle autorizzazioni. Le autorizzazioni devono consentire l'esecuzione del report oppure della codeunit.  

Quando una coda processi è attivata manualmente, viene eseguita con le credenziali dell'utente. Quando una coda processi è attivata come un task pianificato, viene eseguita con le credenziali dell'istanza server. Quando una commessa viene eseguita, viene eseguita con le credenziali della coda processi che ne esegue l'attivazione. Tuttavia, all'utente che ha creato il movimento coda processi è inoltre necessario disporre dei permessi. Quando un processo viene "eseguito nella sessione utente" (ad esempio durante la registrazione background), viene eseguito con le credenziali dell'utente che ha creato il processo.  

> [!IMPORTANT]  
>  Se si utilizza il set di autorizzazioni SUPER fornito con [!INCLUDE[d365fin](includes/d365fin_md.md)], la società e gli utenti dispongono delle autorizzazioni per eseguire tutti gli oggetti. In questo caso, l'accesso per ogni utente è limitato solo dalle autorizzazioni per i dati.  

## <a name="using-job-queues-effectively"></a>Utilizzo delle code processi in modo efficace  
Il record del movimento coda processi ha molti campi di cui lo scopo è quello di portare i parametri in una codeunit specificata per essere eseguita con una coda processi. Questo significa inoltre che le codeunit che devono essere eseguite mediante la coda processi devono essere specificate con il record Movimento coda processi come parametro nel trigger **OnRun**. Cio fornisce un livello di sicurezza aggiuntivo, poiché impedisce agli utenti di eseguire codeunit scelte casualmente tramite la coda processi. Se l'utente deve necessariamente passare i parametri a un report, l'unico modo possibile è eseguire il wrapping dell'esecuzione del report in una codeunit, che analizzerà i parametri di input e li immetterà nel report prima dell'esecuzione.  

## <a name="see-also"></a>Vedi anche  
[Amministrazione](admin-setup-and-administration.md)  
[Impostazione di Business Central](setup.md)  

