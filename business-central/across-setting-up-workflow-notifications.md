---
title: Impostazione delle notifiche del workflow di approvazione
description: Questo articolo spiega come impostare le notifiche del flusso di lavoro per avvisare un utente che si è verificato un evento a cui deve reagire con la risposta del flusso di lavoro obbligatoria.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Notifiche del workflow di approvazione

Impostare i workflow per notificare automaticamente agli utenti quando è richiesta la loro attenzione per un passaggio del workflow. Molte risposte del workflow riguardano la comunicazione, a un utente, di un evento che si è verificato e la relativa necessità di intervento.

Ad esempio, è possibile impostare che l'utente 2, l'utente responsabile dell'approvazione, riceva una notifica ogni volta che l'utente 1 richiede l'approvazione per un nuovo record. Nella fase successiva del workflow, l'utente 2 approva il record, l'utente 3 viene notificato e può iniziare un'elaborazione correlata del record. Con le fasi del workflow di approvazione, ogni notifica è collegata a un movimento di approvazione. Ulteriori informazioni in [Workflow](across-workflow.md).  

> [!NOTE]  
> La versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)] supporta le notifiche come messaggi e-mail e note interne.  

> [!IMPORTANT]  
> Tutte le notifiche del workflow vengono inviate tramite una coda processi. Assicurarsi che la coda processi nella propria installazione sia impostata in modo da gestire le notifiche del workflow e che la casella di controllo **Avvia automaticamente da server** sia selezionata. Per ulteriori informazioni, vedi [Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md).

## Impostazione delle notifiche

È possibile impostare diversi aspetti delle notifiche del workflow nelle aree seguenti:  

* Notifica del responsabile dell'approvazione

  Per i workflow di approvazione, è possibile impostare i destinatari delle notifiche del workflow compilando una riga nella pagina **Setup utente approvazione** per ogni utente che fa parte del workflow.  

  Ad esempio, se l'utente 2 è specificato nel campo **ID resp. approvazione** nella riga per l'utente 1, la notifica di richiesta dell'approvazione viene inviata all'utente 2. Ulteriori informazioni in [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md). 
  
* Programmazione delle notifiche

  È possibile impostare il momento e la modalità di ricezione delle notifiche del workflow da parte degli utenti compilando la pagina **Programmazione notifica** per ogni utente del workflow. Ulteriori informazioni in [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Personalizzazione delle notifiche di posta elettronica

  È possibile se lo desideri personalizzare il contenuto della notifica e-mail modificando Report 1320, E-mail di notifica. Ulteriori informazioni in [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Se si desidera utilizzare la posta elettronica come metodo di notifica, è necessario impostarla sia per il mittente che per il destinatario in [!INCLUDE [prod_short](includes/prod_short.md)]. Ulteriori informazioni sulla [Configurazione e-mail](admin-how-setup-email.md).
  
* Opzioni di risposta

  È possibile impostare le regole e il contenuto specifici della notifica di un workflow durante la creazione del workflow in questione. Seleziona le opzioni di personalizzazione nella pagina **Risposte workflow** per la risposta workflow che rappresenta la notifica. Scopri di più dal passaggio 9 nella sezione [Creare workflow](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Notifica per il mittente

  Per i workflow di approvazione, aggiungere un passaggio di risposta del workflow per notificare al mittente quando la richiesta è stata approvata o rifiutata. Scopri di più dal passaggio 9 nella sezione [Creare workflow](across-how-to-create-workflows.md#to-create-a-workflow).   

## Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Impostare gli utenti del flusso di lavoro](across-how-to-set-up-workflow-users.md)  
[Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Creare workflow di approvazione](across-how-to-create-workflows.md)  
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)  
[Configurare la posta elettronica](admin-how-setup-email.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
