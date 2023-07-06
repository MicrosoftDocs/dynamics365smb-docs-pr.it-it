---
title: Impostazione e utilizzo di un workflow di approvazione acquisti
description: Questa procedura dettagliata illustra tutte le fasi coinvolte nell'impostazione e nell'utilizzo di un flusso di lavoro di approvazione acquisti in Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a><a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a><a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto

È possibile automatizzare il processo di approvazione dei record nuovi o modificati, ad esempio documenti, righe di registrazione e schede cliente, creando workflow con le fasi indicate per le approvazioni in questione.

Prima di creare workflow di approvazione, è necessario impostare un responsabile approvazione e un responsabile approvazione sostitutivo per ogni utente approvazione. È inoltre possibile impostare i limiti di importo per i responsabili approvazione per definire i record di vendita e acquisto che sono qualificati ad approvare. Le richieste di approvazione e altre notifiche possono essere inviate per e-mail o come nota interna. Per ogni setup utente approvazione, è inoltre possibile impostare quando vengono ricevute le notifiche.

> [!NOTE]
> Oltre alla funzionalità Workflow in [!INCLUDE[prod_short](includes/prod_short.md)], è possibile utilizzare Power Automate per definire workflow per gli eventi in [!INCLUDE[prod_short](includes/prod_short.md)]. Si noti che sebbene siano presenti due sistemi del workflow, qualsiasi modello di flusso creato con Power Automate viene aggiunta all'elenco dei modelli di flusso in [!INCLUDE[prod_short](includes/prod_short.md)]. Ulteriori informazioni in [Usare Business Central in un flusso di lavoro automatizzato](across-how-use-financials-data-source-flow.md).  

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro. Ulteriori informazioni in [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata

Questa procedura dettagliata è uno scenario che illustra le attività seguenti:  

- Impostazione degli utenti approvazione  
- Impostazione delle notifiche per gli utenti approvazione  
- Modifica e abilitazione di un workflow di approvazione  
- Richiesta di approvazione di un ordine di acquisto (come Alicia)  
- Ricezione di una notifica e approvazione della richiesta (come Sean)  

## <a name="story"></a><a name="story"></a><a name="story"></a>Scenario

Sean è un utente con privilegi avanzati di CRONUS e crea due utenti di approvazione. Un utente è Alicia che rappresenta un rivenditore. L'altro è Sean stesso che rappresenta il responsabile approvazione di Alicia. Sean quindi concede a se stesso i diritti di approvazione acquisti illimitati e specifica che riceverà le notifiche tramite nota interna non appena si verifica un evento correlato. Infine, Sean crea il workflow di approvazione richiesto come copia del modello esistente del *workflow di approvazione dell'ordine di acquisto*, lascia inalterate tutte le condizioni di evento e le opzioni di risposta, quindi abilita il workflow.  

Per verificare il workflow di approvazione, Sean innanzitutto accede a [!INCLUDE[prod_short](includes/prod_short.md)] come Alicia, quindi richiede l'approvazione di un ordine di acquisto. Sean quindi accede come se stesso, vede la nota in Gestione ruolo utente, seleziona il collegamento della richiesta di approvazione per l'ordine di acquisto e approva la richiesta.  

## <a name="users"></a><a name="users"></a><a name="users"></a>Utenti

Prima di poter impostare gli utenti di approvazione e il relativo metodo di notifica, è necessario assicurarsi che questi utenti esistano in [!INCLUDE[prod_short](includes/prod_short.md)]: Un utente rappresenterà Alicia. L'altro utente, l'utente corrente, rappresenterà Sean. Ulteriori informazioni in [Creare utenti in base alle licenze](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a><a name="setting-up-approval-users"></a><a name="setting-up-approval-users"></a>Impostazione degli utenti approvazione

Dopo aver eseguito l'accesso, imposta Alicia come utente di approvazione di cui sei il responsabile. Imposta i diritti di approvazione e specifica come e quando si riceve la notifica delle richieste di approvazione.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a><a name="to-set-up-yourself-and-alicia-as-approval-users"></a><a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Per impostare l'utente corrente e Alicia come utenti approvazione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup utente approvazione**, quindi scegli il collegamento correlato.  
2. Nella pagina **Setup utente approvazione** scegliere l'azione **Nuovo**.  

    > [!NOTE]  
    >  È necessario impostare un responsabile dell'approvazione prima di poter impostare gli utenti che richiedono l'approvazione del responsabile. Pertanto, è necessario impostare l'utente corrente prima di impostare Alicia.  

3. Impostare i due utenti approvazione compilando i campi come descritto nella tabella seguente.  

    |ID utente|ID resp. approvazione|Approvazione acquisti illimitati|  
    |-------|-----------|---------------------------|  
    |UTENTE CORRENTE||Selezionato|
    |ALICIA|UTENTE CORRENTE||

### <a name="setting-up-notifications"></a><a name="setting-up-notifications"></a><a name="setting-up-notifications"></a>Impostazione delle notifiche

In questa procedura dettagliata, l'utente viene avvisato sulle richieste di approvare mediante la nota interna. Le notifiche di approvazione possono essere anche inviate tramite posta elettronica ed è possibile aggiungere un passaggio di risposta workflow che avvisa il mittente quando una richiesta viene approvata o rifiutata. Ulteriori informazioni in [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a><a name="to-set-up-how-and-when-you-are-notified"></a><a name="to-set-up-how-and-when-you-are-notified"></a>Per impostare come e quando si riceve la notifica

1. Nella pagina **Setup utente approvazione**, selezionare la riga dell'utente corrente e quindi scegliere l'azione **Setup di notifica**.  
2. Nella pagina **Setup di notifica**, nel campo **Tipo di notifica**, scegliere **Approvazione**.  
3. Nel campo **Metodo di notifica**, scegliere **Nota**.  
4. Nella pagina **Setup di notifica** scegliere l'azione **Programmazione notifica**.  
5. Nella pagina **Programmazione notifica**, nel campo **Ricorrenza** selezionare **Immediatamente**.  

## <a name="creating-the-approval-workflow"></a><a name="creating-the-approval-workflow"></a><a name="creating-the-approval-workflow"></a>Creazione del workflow di approvazione

Crea il workflow di approvazione dell'ordine di acquisto copiando i passaggi dal modello di workflow **Workflow di approvazione ordine acquisto**. Lasciare le fasi esistenti del workflow invariate quindi abilitare il workflow.  

> [!TIP]
> Facoltativamente, aggiungere un passaggio di risposta del workflow per notificare al mittente quando la relativa richiesta è stata approvata o rifiutata. Ulteriori informazioni in [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a><a name="to-create-and-enable-a-purchase-order-approval-workflow"></a><a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Per creare e abilitare un workflow di approvazione dell'ordine di acquisto

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Flussi di lavoro**, quindi scegli il collegamento correlato.  
2. Nella pagina **Worflows**, selezionare **Azioni**, quindi **Nuovo**, poi scegliere l'azione **Nuovo workflow da modello**.  
3. Nella pagina **Modelli del workflow**, selezionare il modello di flusso di lavoro denominato **Flusso di lavoro approvazione ordine acquisto**.  

   Verrà visualizzata la pagina **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato. Il valore nel campo **Codice** è esteso con *-01* per indicare che si tratta del primo workflow che viene creato dal modello di workflow **Workflow di approvazione ordine acquisto**.  
4. Nell'intestazione della pagina **Workflow**, seleziona la casella di controllo **Abilitato**.  

## <a name="use-the-approval-workflow"></a><a name="use-the-approval-workflow"></a><a name="use-the-approval-workflow"></a>Utilizzare il flusso di lavoro di approvazione

Utilizza il nuovo workflow di approvazione dell'ordine di acquisto eseguendo per prima cosa l'accesso a [!INCLUDE[prod_short](includes/prod_short.md)] come Alicia per richiedere l'approvazione di un ordine di acquisto. Eseguire quindi l'accesso come l'utente corrente, visualizzare la nota in Gestione ruolo utente, selezionare il collegamento della richiesta di approvazione e approvare la richiesta.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a><a name="to-request-approval-of-a-purchase-order-as-alicia"></a><a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Per richiedere l'approvazione di un ordine di acquisto, come Alicia

1. Effettuare l'accesso come Alicia.
2. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.  
3. Seleziona la riga per aprire l'*ordine di acquisto 106001*.  
4. Nella pagina **Ordine acquisto**, selezionare **Azioni**, poi **Richiedi approvazione**, quindi scegli l'azione **Invia richiesta di approvazione**.  

Si noti che il valore nel campo **Stato** è diventato **Approvazione in sospeso**.  

### <a name="to-approve-the-purchase-order-as-sean"></a><a name="to-approve-the-purchase-order-as-sean"></a><a name="to-approve-the-purchase-order-as-sean"></a>Per approvare l'ordine di acquisto, come Sean

1. Effettuare l'accesso come Sean.
2. In Gestione ruolo utente, nell'area **Self-service** seleziona **Richieste da approvare**.
3. Nella pagina **Richieste da approvare** seleziona la riga relativa all'ordine di acquisto di Alicia, quindi seleziona l'azione**Approva**.  

Il valore nel campo **Stato** dell'ordine di acquisto di Elisa diventa **Rilasciato**.  

A questo punto, è stato impostato e testato un workflow di approvazione semplice in base alle prime due fasi del **workflow di approvazione dell'ordine di acquisto**. È possibile facilmente estendere il workflow per registrare automaticamente l'ordine di acquisto di Elisa quando Sean lo approva. A tale scopo, è necessario abilitare il **workflow della fattura di acquisto** in cui la risposta a una fattura di acquisto emessa è di registrarla. È innanzitutto necessario modificare la condizione di evento nella prima fase del workflow da **Fattura** in **Ordine** di acquisto.  

La versione generica di [!INCLUDE[prod_short](includes/prod_short.md)] comprende molti modelli del workflow per gli scenari supportati dal codice dell'applicazione. La maggior parte dei modelli è per i workflow di approvazione.  

È possibile definire le variazioni dei workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/use-approval-workflows/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)  
[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md)  
[Workflow](across-workflow.md)  
[Usare Business Central in un flusso di lavoro automatizzato](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
