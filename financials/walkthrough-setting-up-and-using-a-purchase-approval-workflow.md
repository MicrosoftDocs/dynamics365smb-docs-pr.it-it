---
title: 'Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto | Documenti Microsoft'
description: "È possibile automatizzare il processo di approvazione dei record nuovi o modificati, ad esempio documenti, righe di registrazione e schede cliente, creando i flussi di lavoro con le fasi indicate per le approvazioni in questione. Prima di creare i flussi di lavoro di approvazione, è necessario impostare un responsabile approvazione e un responsabile approvazione sostitutivo per ogni utente approvazione. È inoltre possibile impostare i limiti di importo per i responsabili approvazione per definire i record di vendita e acquisto che sono qualificati ad approvare. Le richieste di approvazione e altre notifiche possono essere inviate per e-mail o come nota interna. Per ogni setup utente approvazione, è inoltre possibile impostare quando vengono ricevute le notifiche."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 58c243000bea5b70666b2a08cdd5696444e22f0f
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto
È possibile automatizzare il processo di approvazione dei record nuovi o modificati, ad esempio documenti, righe di registrazione e schede cliente, creando i flussi di lavoro con le fasi indicate per le approvazioni in questione. Prima di creare i flussi di lavoro di approvazione, è necessario impostare un responsabile approvazione e un responsabile approvazione sostitutivo per ogni utente approvazione. È inoltre possibile impostare i limiti di importo per i responsabili approvazione per definire i record di vendita e acquisto che sono qualificati ad approvare. Le richieste di approvazione e altre notifiche possono essere inviate per e-mail o come nota interna. Per ogni setup utente approvazione, è inoltre possibile impostare quando vengono ricevute le notifiche.  

 È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  
In questa procedura dettagliata sono illustrati i task seguenti:  

-   Impostazione di utenti approvazione, compresa l'impostazione di un utente in Windows e in [!INCLUDE[d365fin](includes/d365fin_md.md)].  
-   Impostazione delle notifiche per gli utenti approvazione.  
-   Modifica e abilitazione di un flusso di lavoro di approvazione.  
-   Avvio della coda processi che invia le notifiche.  
-   Richiesta di approvazione di un ordine di acquisto, come Elisa.  
-   Ricezione di una notifica e approvazione della richiesta, come Sean.  

## <a name="prerequisites"></a>Prerequisiti  
Per completare questa procedura dettagliata si utilizza la società di esempio CRONUS International Ltd.

## <a name="story"></a>Scenario  
Sean è un utente con privilegi elevati in CRONUS sul proprio computer.  

Crea due utenti approvazione. Un utente è Elisa che rappresenta un rivenditore. L'altro è se stesso che rappresenta il responsabile approvazione di Alicia. Sean quindi concede a se stesso i diritti di approvazione acquisti illimitati e specifica che riceverà le notifiche tramite nota interna non appena si verifica un evento correlato. Infine, Sean crea il flusso di lavoro di approvazione richiesto come copia del modello esistente del flusso di lavoro di approvazione dell'ordine di acquisto, lascia inalterate tutte le condizioni di evento e le opzioni di risposta, quindi abilita il flusso di lavoro.  

Per verificare il flusso di lavoro di approvazione, Sean innanzitutto accede a [!INCLUDE[d365fin](includes/d365fin_md.md)] come Alicia, quindi richiede l'approvazione di un ordine di acquisto. Sean quindi si collega come se stesso, vede la nota in Gestione ruolo utente, seleziona il collegamento della richiesta di approvazione per l'ordine di acquisto e approva la richiesta.  

## <a name="setting-up-the-sample-data"></a>Impostazione dei dati di esempio  
È necessario creare sul computer locale e in [!INCLUDE[d365fin](includes/d365fin_md.md)] un nuovo utente che rappresenta Elisa, il quale verrà successivamente selezionato come utente approvazione. Il proprio account utente rappresenterà Sean.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Per aggiungere Elisa come utente sul computer locale  

1.  Scegliere **Avvia** e nella casella **Cerca programmi e file** scegliere **Modifica utenti e gruppi locali**, quindi selezionare il collegamento correlato.  
2.  Aprire la cartella **Utenti**.  
3.  Nella scheda **Azioni** selezionare **Nuovo utente**.  
4.  Nel campo **Nome utente**, immettere Elisa.  
5.  Nei campi **Password** e **Conferma password**, immettere una password valida.  
6.  Deselezionare la casella di controllo **Al prossimo accesso è necessario modificare la password**.  
7.  Chiudere la finestra **Utenti e gruppi locali**.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Per aggiungere Elisa come utente in [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Utenti**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Utenti di Windows** nel gruppo **Nuovo** della scheda **Pagina iniziale** scegliere **Nuovo**.  
3.  Nella finestra **Scheda utente**, nel campo **Nome utente**, immettere Elisa.  
4.  Nel campo **Nome utente di Windows** scegliere il pulsante AssistEdit.  
5.  Nella finestra **Seleziona utente o gruppo**, immettere Elisa nel campo **Immettere il nome dell'oggetto da selezionare** e scegliere il pulsante **Controlla nomi**.  
6.  Quando nel campo viene visualizzato [NOME COMPUTER]ELISA, fare clic sul pulsante **OK**.  
7.  Nella Scheda dettaglio **Set di autorizzazioni utente** selezionare **SUPER** nel campo **Set di autorizzazioni**.  
8.  Nel campo **Società**, selezionare **CRONUS International Ltd.**  
9. Scegliere il pulsante **OK**.  

## <a name="setting-up-approval-users"></a>Impostazione degli utenti approvazione  
Utilizzando l'utente Windows appena creato, impostare Elisa come utente approvazione il cui responsabile approvazione è l'utente in uso stesso. Impostare i diritti di approvazione e specificare come e quando si riceve la notifica delle richieste di approvazione.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Per impostare l'utente in uso e Alicia come utenti approvazione  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Setup utente approvazione**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Setup utente approvazione** della scheda **Pagina iniziale** nel gruppo **Nuovo**, scegliere **Nuovo**.  

    > [!NOTE]  
    >  È necessario impostare un responsabile dell'approvazione prima di poter impostare gli utenti che richiedono l'approvazione del responsabile. Pertanto, è necessario impostare l'utente in uso prima di impostare Elisa.  

3.  Impostare i due utenti approvazione compilando i campi come descritto nella tabella seguente.  

    |ID utente|ID resp. approvazione|Approvazione acquisti illimitati|  
    |-------------|-----------------|---------------------------------|  
    |[NOME COMPUTER][UTENTE]||Selezionato|  
    |[NOME COMPUTER]ELISA|[NOME COMPUTER][UTENTE]||  

## <a name="setting-up-notifications"></a>Impostazione delle notifiche  
Specificare come e quando si riceve la notifica delle richieste di approvazione.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Per impostare come e quando si riceve la notifica  
1.  Nella finestra **Setup utente approvazione**, selezionare la riga dell'utente in uso e quindi nella scheda **Pagina iniziale**, nel gruppo **Processo**, scegliere **Setup di notifica**.  
2.  Nella finestra **Setup di notifica**, nel campo **Tipo di notifica**, **Approvazione**.  
3.  Scegliere il campo **Codice modello di notifica**, quindi il pulsante **Avanzate**.  
4.  Nel gruppo **Gestione** della scheda **Pagina iniziale** della finestra **Modelli di notifica** scegliere **Modifica lista**.  
5.  Nella riga del modello di APPROVAZIONE, nel campo **Metodo di notifica**, immettere **Nota**.  
6.  Scegliere il pulsante **OK**.  
7.  Nella finestra **Setup di notifica**, nella scheda **Pagina iniziale**, nel gruppo **Processo**, scegliere **Programmazione notifica**.  
8.  Nella finestra **Programmazione notifica**, nel campo **Occorrenza**, scegliere **Immediatamente**.  
9. Scegliere il pulsante **OK**.  

## <a name="creating-the-approval-workflow"></a>Creazione del flusso di lavoro di approvazione  
 Creare il flusso di lavoro di approvazione dell'ordine di acquisto copiando le fasi dal modello del flusso di lavoro di approvazione dell'ordine di acquisto. Lasciare le fasi esistenti del flusso di lavoro invariate quindi abilitare il flusso di lavoro.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Per creare e abilitare un flusso di lavoro di approvazione dell'ordine di acquisto  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Workflow** e quindi scegliere il collegamento correlato.  
2.  Nella finestra **Workflow**, nel gruppo **Generale** della scheda **Azioni**, scegliere **Crea flusso di lavoro da modello**.  
3.  Nel gruppo **Generale** della scheda **Azioni** scegliere **Crea flusso di lavoro da modello**. Verrà aperta la finestra **Modelli del workflow**.  
4.  Selezionare il modello di flusso di lavoro denominato Flusso di lavoro approvazione ordine acquisto, quindi scegliere il pulsante **OK**.  

    Verrà visualizzata la finestra **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato. Il valore nel campo **Coda** è esteso con "-01" per indicare che si tratta del primo flusso di lavoro che viene creato dal modello Flusso di lavoro approvazione ordine acquisto.  
5.  Nell'intestazione della finestra **Workflow**, selezionare la casella di controllo **Abilitato**.  

## <a name="starting-a-notification-job-queue"></a>Avvio di una coda processi di notifica  
Assicurarsi che una coda processi sia impostata nella versione in uso in modo da gestire le notifiche del flusso di lavoro.  

### <a name="to-start-the-notify-job-queue"></a>Per avviare la coda processi di NOTIFICA  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Code processi**, quindi scegliere il collegamento correlato.  
2.  Nella finestra **Code processi**, selezionare la riga della coda processi di NOTIFICA e nella scheda **Pagina iniziale**, nel gruppo **Processo**, scegliere **Avvia coda processi**.  

## <a name="using-the-approval-workflow"></a>Utilizzo del flusso di lavoro di approvazione  
Utilizzare il nuovo flusso di lavoro di approvazione dell'ordine di acquisto eseguendo per prima cosa l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] come Elisa per richiedere l'approvazione di un ordine di acquisto. Quindi, eseguire l'accesso come l'utente in uso, visualizzare la nota in Gestione ruolo utente, selezionare il collegamento della richiesta di approvazione e approvare la richiesta.  

Per accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)] come un altro utente, si utilizza la funzione **Esegui come altro utente**.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Per accedere a [!INCLUDE[d365fin](includes/d365fin_md.md)] come Elisa  

1.  Per il client Web [!INCLUDE[d365fin](includes/d365fin_md.md)], sul pulsante di avvio del browser per la pagina Web, premere MAIUSC + fare clic con il pulsante destro del mouse e scegliere **Esegui come altro utente**.  

    Per il client Windows [!INCLUDE[d365fin](includes/d365fin_md.md)], sul pulsante di avvio del browser per il programma, premere MAIUSC + fare clic con il pulsante destro del mouse e scegliere **Esegui come altro utente**.  

2.  Nella finestra **Sicurezza di Windows**, immettere [NOME COMPUTER]ELISA e la password richiesta.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Per richiedere l'approvazione di un ordine di acquisto, come Elisa  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Ordini acquisto**, quindi scegliere il collegamento correlato.  
2.  Selezionare la riga per l'ordine di acquisto aperto 104001 e nel gruppo **Gestione** della scheda **Pagina iniziale** selezionare **Modifica**.  
3.  Nella finestra **Ordine acquisto**, nel gruppo **Approvazione** della scheda **Azioni** scegliere **Invia richiesta approvazione**.  

    Si noti che il valore nel campo **Stato** è diventato **Approvazione in sospeso**.  

4.  Chiudere [!INCLUDE[d365fin](includes/d365fin_md.md)].  

### <a name="to-approve-the-purchase-order-as-sean"></a>Per approvare l'ordine di acquisto, come Sean  

1.  Aprire [!INCLUDE[d365fin](includes/d365fin_md.md)] normalmente. Il programma verrà aperto con l'utente in uso.  
2.  In Gestione ruolo utente, nella finestra **Notifiche personali**, cercare una nuova nota di Elisa.  

    > [!NOTE]  
    >  Sebbene l'occorrenza di notifica sia impostata su **Immediatamente**, la nota arriva circa un minuto dopo l'invio da parte di Elisa della richiesta di approvazione. Ciò è dovuto alla frequenza di ricorrenza di default della funzionalità Coda processi.  

3.  Quando la nota viene visualizzata nella finestra **Notifiche personali**, scegliere il valore **Movimento approvazione: XX, XX** nel campo **Pagina**. Viene visualizzata la finestra **Richieste da approvare** con la richiesta di Elisa per l'ordine di acquisto evidenziato.  
4.  Nel gruppo **Processo** della scheda **Pagina iniziale** della finestra **Richieste da approvare** scegliere **Approva**.  

    Il valore nel campo **Stato** dell'ordine di acquisto di Elisa diventa **Rilasciato**.  

A questo punto, è stato impostato e testato un flusso di lavoro di approvazione semplice in base alle prime due fasi del flusso di lavoro di approvazione dell'ordine di acquisto. È possibile facilmente estendere il flusso di lavoro per registrare automaticamente l'ordine di acquisto di Elisa quando Sean lo approva. A tale scopo, è necessario abilitare il flusso di lavoro della fattura di acquisto in cui la risposta a una fattura di acquisto emessa è di registrarla. È innanzitutto necessario modificare la condizione di evento nella prima fase del flusso di lavoro da **Fattura** in **Ordine** di acquisto.  

La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] comprende diversi modelli del flusso di lavoro per gli scenari supportati dal codice dell'applicazione. La maggior parte di essi sono per i flussi di lavoro di approvazione. Per ulteriori informazioni, vedere Modelli del workflow.  

È possibile definire le variazioni dei workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).  

Se uno scenario aziendale richiede un evento o una risposta del flusso di lavoro non supportati, il partner Microsoft deve implementarli tramite la personalizzazione del codice dell'applicazione. Per ulteriori informazioni, vedere [Procedura dettagliata: Implementazione di nuovi eventi e risposte workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) nella Guida per sviluppatori e professionisti IT.  

## <a name="see-also"></a>Vedi anche  
[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)   
[Creare i workflow](across-how-to-create-workflows.md)   
[Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md)   
[Workflow](across-workflow.md)

