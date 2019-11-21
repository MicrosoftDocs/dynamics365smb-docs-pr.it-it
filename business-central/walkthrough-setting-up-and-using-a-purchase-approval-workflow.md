---
title: Impostazione e utilizzo di un workflow di approvazione di acquisto | Documenti Microsoft
description: È possibile automatizzare il processo di approvazione dei record nuovi o modificati, ad esempio documenti, righe di registrazione e schede cliente, creando i flussi di lavoro con le fasi indicate per le approvazioni in questione. Prima di creare i flussi di lavoro di approvazione, è necessario impostare un responsabile approvazione e un responsabile approvazione sostitutivo per ogni utente approvazione. È inoltre possibile impostare i limiti di importo per i responsabili approvazione per definire i record di vendita e acquisto che sono qualificati ad approvare. Le richieste di approvazione e altre notifiche possono essere inviate per e-mail o come nota interna. Per ogni setup utente approvazione, è inoltre possibile impostare quando vengono ricevute le notifiche.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/11/2019
ms.author: sgroespe
ms.openlocfilehash: fe99b7cf27a294a0f8198740631acfe5fec8e21f
ms.sourcegitcommit: 02f1633213793bfc040ad0d2a96fe76572215aa5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "2798431"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto
È possibile automatizzare il processo di approvazione dei record nuovi o modificati, ad esempio documenti, righe di registrazione e schede cliente, creando i flussi di lavoro con le fasi indicate per le approvazioni in questione. Prima di creare i flussi di lavoro di approvazione, è necessario impostare un responsabile approvazione e un responsabile approvazione sostitutivo per ogni utente approvazione. È inoltre possibile impostare i limiti di importo per i responsabili approvazione per definire i record di vendita e acquisto che sono qualificati ad approvare. Le richieste di approvazione e altre notifiche possono essere inviate per e-mail o come nota interna. Per ogni setup utente approvazione, è inoltre possibile impostare quando vengono ricevute le notifiche.

> [!NOTE]
> Oltre alla funzionalità Workflow in [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile eseguire l'integrazione a Microsoft Flow per definire workflow per gli eventi in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si noti che sebbene siano presenti due sistemi del flusso di lavoro, qualsiasi modello di flusso creato con Microsoft Flow viene aggiunta all'elenco dei modelli di flusso in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Uso di Business Central in un workflow automatizzato](across-how-use-financials-data-source-flow.md).   

 È possibile impostare e utilizzare i workflow che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del workflow. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  
In questa procedura dettagliata sono illustrati i task seguenti:  

-   Impostazione degli utenti approvazione.  
-   Impostazione delle notifiche per gli utenti approvazione.  
-   Modifica e abilitazione di un flusso di lavoro di approvazione.  
-   Richiesta di approvazione di un ordine di acquisto, come Alicia.  
-   Ricezione di una notifica e approvazione della richiesta, come Sean.  

## <a name="story"></a>Scenario  
Sean è un utente con privilegi avanzati di CRONUS. Crea due utenti approvazione. Un utente è Alicia che rappresenta un rivenditore. L'altro è se stesso che rappresenta il responsabile approvazione di Alicia. Sean quindi concede a se stesso i diritti di approvazione acquisti illimitati e specifica che riceverà le notifiche tramite nota interna non appena si verifica un evento correlato. Infine, Sean crea il flusso di lavoro di approvazione richiesto come copia del modello esistente del flusso di lavoro di approvazione dell'ordine di acquisto, lascia inalterate tutte le condizioni di evento e le opzioni di risposta, quindi abilita il flusso di lavoro.  

Per verificare il flusso di lavoro di approvazione, Sean innanzitutto accede a [!INCLUDE[d365fin](includes/d365fin_md.md)] come Alicia, quindi richiede l'approvazione di un ordine di acquisto. Sean quindi accede come se stesso, vede la nota in Gestione ruolo utente, seleziona il collegamento della richiesta di approvazione per l'ordine di acquisto e approva la richiesta.  

## <a name="setting-up-sample-data"></a>Impostazione dei dati di esempio
Prima di poter impostare gli utenti di approvazione e il relativo metodo di notifica, è necessario assicurarsi che due utenti esistano in [!INCLUDE[d365fin](includes/d365fin_md.md)]: Un utente rappresenterà Alicia. L'altro utente, l'utente corrente, rappresenterà Sean. Per ulteriori informazioni, vedere [Creare utenti in base alle licenze](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Impostazione degli utenti approvazione  
Quando si esegue l'accesso come utente corrente, impostare Alicia come utente di approvazione il cui responsabile è l'utente corrente. Impostare i diritti di approvazione e specificare come e quando si riceve la notifica delle richieste di approvazione.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Per impostare l'utente corrente e Alicia come utenti approvazione  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup utente approvazione** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Setup utente approvazione** scegliere l'azione **Nuovo**.  

    > [!NOTE]  
    >  È necessario impostare un responsabile dell'approvazione prima di poter impostare gli utenti che richiedono l'approvazione del responsabile. Pertanto, è necessario impostare l'utente corrente prima di impostare Alicia.  

3.  Impostare i due utenti approvazione compilando i campi come descritto nella tabella seguente.  

    |ID utente|ID resp. approvazione|Approvazione acquisti illimitati|  
    |-------------|-----------------|---------------------------------|  
    |UTENTE CORRENTE||Selezionato|  
    |ALICIA|UTENTE CORRENTE||  

### <a name="setting-up-notifications"></a>Impostazione delle notifiche  
In questa procedura dettagliata, l'utente viene avvisato sulle richieste di approvare mediante la nota interna. La notifica di approvazione può anche essere inviata tramite e-mail. Per ulteriori informazioni, vedere [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Per impostare come e quando si riceve la notifica  
1.  Nella pagina **Setup utente approvazione**, selezionare la riga dell'utente corrente e quindi scegliere l'azione **Setup di notifica**.  
2.  Nella pagina **Setup di notifica**, nel campo **Tipo di notifica**, scegliere **Approvazione**.  
3.  Nel campo **Metodo di notifica**, scegliere **Nota**.  
6.  Nella pagina **Setup di notifica** scegliere l'azione **Programmazione notifica**.  
7.  Nella pagina **Programmazione notifica**, nel campo **Ricorrenza** selezionare **Immediatamente**.  

## <a name="creating-the-approval-workflow"></a>Creazione del flusso di lavoro di approvazione  
 Creare il flusso di lavoro di approvazione dell'ordine di acquisto copiando le fasi dal modello del flusso di lavoro di approvazione dell'ordine di acquisto. Lasciare le fasi esistenti del flusso di lavoro invariate quindi abilitare il flusso di lavoro.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Per creare e abilitare un flusso di lavoro di approvazione dell'ordine di acquisto  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Workflow** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Workflow** scegliere l'azione **Nuovo workflow da modello**.  
3.  Nella pagina **Modelli del workflow**, selezionare il modello di flusso di lavoro denominato Flusso di lavoro approvazione ordine acquisto, quindi scegliere il pulsante **OK**.  

    Verrà visualizzata la pagina **Workflow** per un nuovo workflow contenente tutte le informazioni del modello selezionato. Il valore nel campo **Coda** è esteso con "-01" per indicare che si tratta del primo flusso di lavoro che viene creato dal modello Flusso di lavoro approvazione ordine acquisto.  
5.  Nell'intestazione della pagina **Workflow**, selezionare la casella di controllo **Abilitato**.  

## <a name="using-the-approval-workflow"></a>Utilizzo del flusso di lavoro di approvazione  
Utilizzare il nuovo workflow di approvazione dell'ordine di acquisto eseguendo per prima cosa l'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)] come Alicia per richiedere l'approvazione di un ordine di acquisto. Eseguire quindi l'accesso come l'utente corrente, visualizzare la nota in Gestione ruolo utente, selezionare il collegamento della richiesta di approvazione e approvare la richiesta.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Per richiedere l'approvazione di un ordine di acquisto, come Alicia  
1. Effettuare l'accesso come Alicia.
2.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.  
3.  Selezionare la riga per l'ordine di acquisto aperto 106001, quindi scegliere l'azione **Modifica**.  
4.  Nella pagina **Ordine di acquisto**, scegliere l'azione **Invia richiesta approvazione**.  

Si noti che il valore nel campo **Stato** è diventato **Approvazione in sospeso**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Per approvare l'ordine di acquisto, come Sean  
1. Effettuare l'accesso come Sean.
2. In Gestione ruolo utente, nell'area **Self-service** selezionare il riquadro **Richieste da approvare**.
3. Nella pagina **Richieste da approvare** selezionare la riga relativa all'ordine di acquisto di Alicia, quindi selezionare l'azione**Approva**.  

Il valore nel campo **Stato** dell'ordine di acquisto di Elisa diventa **Rilasciato**.  

A questo punto, è stato impostato e testato un flusso di lavoro di approvazione semplice in base alle prime due fasi del flusso di lavoro di approvazione dell'ordine di acquisto. È possibile facilmente estendere il flusso di lavoro per registrare automaticamente l'ordine di acquisto di Elisa quando Sean lo approva. A tale scopo, è necessario abilitare il flusso di lavoro della fattura di acquisto in cui la risposta a una fattura di acquisto emessa è di registrarla. È innanzitutto necessario modificare la condizione di evento nella prima fase del flusso di lavoro da **Fattura** in **Ordine** di acquisto.  

La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] comprende diversi modelli del flusso di lavoro per gli scenari supportati dal codice dell'applicazione. La maggior parte di essi sono per i flussi di lavoro di approvazione.  

È possibile definire le variazioni dei workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione. Per ulteriori informazioni, vedere [Creare workflow](across-how-to-create-workflows.md).  

Se uno scenario aziendale richiede un evento o una risposta del flusso di lavoro non supportati, il partner Microsoft deve implementarli tramite la personalizzazione del codice dell'applicazione. Per ulteriori informazioni, vedere [Procedura dettagliata: Implementazione di nuovi eventi e risposte workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) nella Guida per sviluppatori e professionisti IT.  

## <a name="see-also"></a>Vedi anche  
[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)   
[Creare i workflow](across-how-to-create-workflows.md)   
[Utilizzare i workflow di approvazione](across-how-use-approval-workflows.md)   
[Workflow](across-workflow.md)  
[Uso di Business Central in un workflow automatizzato](across-how-use-financials-data-source-flow.md)
