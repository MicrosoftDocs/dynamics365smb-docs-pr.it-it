---
title: Come specificare come e quando ricevere le notifiche | Microsoft Docs
description: "Quando si impostano gli utenti nei workflow di approvazione, è necessario specificare nelle finestre Setup di notifica e Programmazione notifica come e quando ciascun utente riceverà le notifiche relative alle fasi del workflow di approvazione. I singoli utenti possono inoltre modificare la propria impostazione delle notifiche scegliendo il pulsante Modifica impostazioni di notifica per qualsiasi notifica."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 714ebd289407293f2a9fb8f05cad68330c79ad9a
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="specify-when-and-how-to-receive-notifications"></a>Specificare come e quando ricevere le notifiche
Quando si impostano gli utenti nei workflow di approvazione, è necessario specificare nelle finestre **Setup di notifica** e **Programmazione notifica** come e quando ciascun utente riceverà le notifiche relative alle fasi del workflow di approvazione. I singoli utenti possono inoltre modificare la propria impostazione delle notifiche scegliendo il pulsante **Modifica impostazioni di notifica** per qualsiasi notifica.  

 Prima di impostare le preferenze di notifica di un utente di approvazione, è necessario impostarlo come utente di approvazione. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  

 Il layout e il contenuto delle notifiche possono essere definiti impostando dei modelli di notifica. Per ulteriori informazioni, vedere [Gestire i modelli di notifica](across-how-to-manage-notification-templates.md).  

 Molte fasi del workflow di approvazione riguardano la comunicazione, agli utenti, di un evento che si è verificato e la relativa necessità di intervento. Ad esempio, in una fase del workflow, l'evento potrebbe essere che l'Utente 1 richiede l'approvazione di un nuovo record. La risposta correlata prevede l'invio di una notifica all'Utente 2, cioè il responsabile dell'approvazione. Nella fase successiva del workflow, l'evento potrebbe essere che l'Utente 2 approva il record. La risposta correlata prevede l'invio di una notifica all'Utente 3 per iniziare un processo con il record approvato. Per le fasi del workflow che riguardano l'approvazione, ogni notifica è collegata a un movimento di approvazione. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Specificare come e quando gli utenti ricevono le notifiche  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup utente approvazione** e quindi scegliere il collegamento correlato.  
2.  Selezionare la riga per l'utente per il quale si desidera impostare le preferenze di notifica, quindi scegliere l'azione **Setup notifiche**.  
3.  Compilare i campi nella finestra **Setup di notifica** come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo di notifica**|Specificare il tipo di evento a cui fa riferimento la notifica.<br /><br /> Selezionare una delle seguenti opzioni:<br /><br /> -   **Nuovo record** specifica che la notifica è relativa a un nuovo record, ad esempio un documento, che l'utente deve utilizzare.<br />-   **Approvazione** specifica che la notifica è relativa a una o più richieste di approvazione.<br />-   **Scaduto** specifica che la notifica ha lo scopo di ricordare agli utenti che sono in ritardo nell'azione relativa a un evento.|  
    |**Codice modello di notifica**|Specificare il codice del modello di notifica utilizzato per creare le notifiche per l'utente.|  
    |**Notifiche non aggregate**|Specificare se l'utente riceve una notifica per ogni evento o più notifiche aggregate.<br /><br /> Se la casella di controllo **Notifiche non aggregate** non è selezionata, l'utente riceve notifiche che raggruppano le informazioni sugli eventi che si verificano all'interno dello stesso modello di ricorrenza nella programmazione delle notifiche.|  

     A questo punto è stato specificato il modo in cui l'utente riceve le notifiche. Continuare specificando quando l'utente le deve ricevere.  

4.  Scegliere l'azione **Programmazione notifica**.  
5.  Compilare i campi nella finestra **Programmazione notifica** come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ricorrenza**|Specificare il modello di ricorrenza con cui l'utente riceve le notifiche.|  
    |**Ora**|Specificare il momento della giornata in cui l'utente riceve le notifiche quando il valore del campo **Ricorrenza** è diverso da **Immediatamente**.|  
    |**Frequenza giornaliera**|Specificare in quale tipo di giorni l'utente riceve le notifiche quando il valore nel campo **Ricorrenza** è **Ogni giorno**.<br /><br /> Selezionare **Giorno feriale** per ricevere le notifiche ogni giorno lavorativo della settimana. Selezionare **Giornaliero** per ricevere le notifiche ogni giorno della settimana, incluso il fine settimana.|  
    |**Lunedì**-**Domenica**|Specificare in quali giorni l'utente riceve le notifiche quando il valore nel campo **Ricorrenza** è **Ogni settimana**.|  
    |**Data del mese**|Specificare se l'utente riceve le notifiche il primo giorno o l'ultimo giorno del mese o in una data specifica del mese.|  
    |**Data notifica mensile**|Specificare la data del mese in cui l'utente riceve le notifiche quando il valore nel campo **Data del mese** è **Personalizzato**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Modificare come e quando si ricevono le notifiche  
1.  In una delle notifiche ricevute, come e-mail o nota, fare clic sul pulsante **Modifica impostazioni di notifica**.  
2.  Nella finestra **Setup di notifica** modificare le preferenze relative alla notifica come descritto nella procedura precedente.  

## <a name="see-also"></a>Vedi anche  
 [Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
 [Gestire i modelli di notifica](across-how-to-manage-notification-templates.md)   
 [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)   
 [Impostazione dei workflow](across-set-up-workflows.md)   
 [Utilizzo dei workflow](across-use-workflows.md)

