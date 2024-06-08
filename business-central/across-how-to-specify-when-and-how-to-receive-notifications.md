---
title: Specificare come e quando ricevere le notifiche del flusso di lavoro
description: 'Quando imposti gli utenti nei flussi di lavoro di approvazione, puoi specificare come e quando ogni utente di approvazione riceve le notifiche.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '663, 1500, 1512, 1513,'
ms.date: 09/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Specificare come e quando ricevere le notifiche del flusso di lavoro

Quando imposti gli utenti di approvazione nei flussi di lavoro in cui vuoi che qualcuno approvi le modifiche, ad esempio quando vengono creati nuovi record o quando qualcuno richiede un'approvazione, devi specificare come e quando l'utente di approvazione riceverà una notifica. Ad esempio, puoi specificare che un utente di approvazione riceverà immediatamente un messaggio e-mail quando qualcuno crea un nuovo cliente. In alternativa, puoi programmare le notifiche da consegnare insieme, insieme, ad esempio su base settimanale o mensile.

Le persone possono inoltre modificare la propria impostazione delle notifiche scegliendo **Modifica impostazioni di notifica** per qualsiasi notifica.  

> [!NOTE]
> Le notifiche vengono inviate in base alle impostazioni di notifica per il destinatario, non per il mittente. Questa è una distinzione importante poiché significa che quando qualcuno richiede un'approvazione nel contesto di un flusso di lavoro, la sua richiesta non viene necessariamente inviata immediatamente. Verrà invece consegnato in base alla pianificazione delle notifiche specificata nelle impostazioni di notifica del responsabile dell'approvazione.

Prima di impostare le preferenze di notifica di un utente di approvazione, è necessario impostarlo come utente di approvazione. Ulteriori informazioni in [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Se si desidera utilizzare la posta elettronica come metodo di notifica, è necessario impostarla sia per il mittente che per il destinatario in [!INCLUDE [prod_short](includes/prod_short.md)]. Ulteriori informazioni sulla [Configurazione e-mail](admin-how-setup-email.md).

## Passaggi nei flussi di lavoro

Molte fasi del workflow di approvazione riguardano la comunicazione, agli utenti, di un evento che si è verificato e la relativa necessità di intervento. Ad esempio, in una fase del workflow, l'evento potrebbe essere che l'Utente 1 richiede l'approvazione di un nuovo record. La risposta correlata prevede l'invio di una notifica all'Utente 2, cioè il responsabile dell'approvazione. Nella fase successiva del workflow, l'evento potrebbe essere che l'Utente 2 approva il record. La risposta correlata prevede l'invio di una notifica all'Utente 3 per iniziare un processo con il record approvato. Per le fasi del workflow che includono l'approvazione, ogni notifica è collegata a un movimento di approvazione. Ulteriori informazioni in [Workflow](across-workflow.md).  

## Specificare come e quando gli utenti per l'approvazione ricevono le notifiche  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup utente approvazione**, quindi scegli il collegamento correlato.  
2. Selezionare la riga per l'utente per il quale si desidera impostare le preferenze di notifica, quindi scegliere l'azione **Setup notifiche**.  
3. Compilare i campi nella pagina **Setup notifiche workflow** come descritto nella tabella riportata di seguito.  

   > [!NOTE]
   > Se apri la pagina **Setup notifiche workflow** dalla pagina **Setup utente approvazione** l'impostazione della notifica è collegata all'utente di approvazione. L'utente di approvazione riceverà sempre le notifiche del flusso di lavoro in base a tale impostazione di notifica. Se usi la *Funzionalità delle informazioni* per aprire la pagina **Setup notifiche workflow** l'impostazione di notifica si applicherà a tutti gli utenti.

   |Campo|Descrizione|
   |-----|-----------|
   |**Tipo di notifica**|Specificare il tipo di evento a cui fa riferimento la notifica.<br /><br /> Selezionare una delle seguenti opzioni:<br /><br /> -   **Nuovo record** specifica che la notifica è relativa a un nuovo record, ad esempio un documento, che l'utente deve utilizzare.<br />-   **Approvazione** specifica che la notifica è relativa a una o più richieste di approvazione.<br />-   **Scaduto** specifica che la notifica ha lo scopo di ricordare agli utenti che sono in ritardo nell'azione relativa a un evento.|
   |**Metodo di notifica**|Specificare se la notifica viene inviata come messaggio di posta elettronica o una nota interna.|

   È possibile definire il layout delle notifiche e-mail personalizzando Report 1320, E-mail di notifica. Ulteriori informazioni in [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

   A questo punto hai specificato il modo in cui l'utente riceve le notifiche. Continuare specificando quando l'utente le deve ricevere.  
4. Scegliere l'azione **Programmazione notifica**.  
5. Compilare i campi nella pagina **Programmazione notifica** come descritto nella tabella riportata di seguito.  

   |Campo|Descrizione|
   |-----|-----------|
   |**Ricorrenza**|Specificare il modello di ricorrenza con cui le notifiche vengono inviate all'utente.|
   |**Ora**|Specifica il momento delle notifiche giornaliere all'utente riceve le notifiche quando il valore del campo **Ricorrenza** è diverso da **Immediatamente**.|
   |**Frequenza giornaliera**|Specificare in quale tipo di giorni l'utente riceve le notifiche quando il valore nel campo **Ricorrenza** è **Ogni giorno**.<br /><br /> Seleziona **Giorno feriale** per ricevere le notifiche ogni giorno lavorativo della settimana. Selezionare **Giornaliero** per ricevere le notifiche ogni giorno della settimana, incluso il fine settimana.|
   |**Lunedì**-**Domenica**|Specificare in quali giorni l'utente riceve le notifiche quando il valore nel campo **Ricorrenza** è **Ogni settimana**.|
   |**Data del mese**|Specificare se l'utente riceve le notifiche il primo giorno o l'ultimo giorno del mese o in una data specifica del mese.|
   |**Data notifica mensile**|Specificare la data del mese in cui l'utente riceve le notifiche quando il valore nel campo **Data del mese** è **Personalizzato**.|

## Modificare come e quando si ricevono le notifiche

1. In una delle notifiche ricevute, come e-mail o nota, fai clic sul pulsante **Modifica impostazioni di notifica**.  
2. Nella pagina **Setup notifiche workflow** modifica le preferenze relative alla notifica come descritto nei passaggi da 3 a 5 sopra descritti.
   1. Conferma che la notifica corretta è stata scelta nel campo **Tipo di notifica**.
   2. Scegli se ricevere un'e-mail o una notifica di nota nel campo **Metodo di notifica**.
   3. Seleziona **Programmazione notifica** per modificare la frequenza e la ricorrenza di invio delle notifiche.

## Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Impostazione delle notifiche del workflow di approvazione](across-setting-up-workflow-notifications.md)  
[Configurare i flussi di lavoro di approvazione](across-set-up-workflows.md)  
[Utilizzare i workflow di approvazione](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
