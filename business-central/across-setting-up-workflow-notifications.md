---
title: Impostazione delle notifiche del flusso di lavoro
description: Questo argomento spiega come impostare le notifiche del flusso di lavoro per avvisare un utente che si è verificato un evento a cui deve reagire con la risposta del flusso di lavoro obbligatoria.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 80d796a827f2c0196c6590c89de04a1945938313
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "6320616"
---
# <a name="workflow-notifications"></a>Notifiche del workflow

Impostare i workflow per notificare automaticamente agli utenti quando è richiesta la loro attenzione per un passaggio del workflow. Molte risposte del workflow riguardano la comunicazione, a un utente, di un evento che si è verificato e la relativa necessità di intervento. Ad esempio, in un passaggio del workflow, l'evento potrebbe essere che l'utente 1 richiede l'approvazione di un nuovo record e la risposta riguarda l'invio di una notifica all'utente 2, cioè il responsabile dell'approvazione. Nel passaggio successivo del workflow, l'evento potrebbe essere che l'utente 2 approva il record e la risposta riguarda l'invio di una notifica all'utente 3 per iniziare un'elaborazione correlata del record approvato. Per le fasi del workflow che riguardano l'approvazione, ogni notifica è collegata a un movimento di approvazione. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
> La versione generica di [!INCLUDE[prod_short](includes/prod_short.md)] supporta le notifiche come messaggi e-mail e note interne.  

> [!IMPORTANT]  
> Tutte le notifiche del workflow vengono inviate tramite una coda processi. Assicurarsi che la coda processi nella propria installazione sia impostata in modo da gestire le notifiche del workflow e che la casella di controllo **Avvia automaticamente da server** sia selezionata. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Impostazione delle notifiche

È possibile impostare diversi aspetti delle notifiche del workflow nelle aree seguenti:  

* Notifica del responsabile dell'approvazione

    Per i workflow di approvazione, è possibile impostare i destinatari delle notifiche del workflow compilando una riga nella pagina **Setup utente approvazione** per ogni utente che fa parte del workflow.  

    Ad esempio, se l'utente 2 è specificato nel campo **ID resp. approvazione** nella riga per l'utente 1, la notifica di richiesta dell'approvazione viene inviata all'utente 1. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  
* Programmazione delle notifiche

    È possibile impostare il momento e la modalità di ricezione delle notifiche del workflow da parte degli utenti compilando la pagina **Programmazione notifica** per ogni utente del workflow. Per ulteriori informazioni, vedere [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Personalizzazione delle notifiche di posta elettronica

    Se lo si desidera, è possibile personalizzare il contenuto della notifica e-mail modificando Report 1320, E-mail di notifica. Per ulteriori informazioni, vedere [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).  
* Opzioni di risposta

    È possibile impostare le regole e il contenuto specifici della notifica di un workflow durante la creazione del workflow in questione. Questa operazione può essere eseguita selezionando le opzioni nella pagina **Opzioni di risposta workflow** per la risposta workflow che rappresenta la notifica. Per ulteriori informazioni, vedere il passaggio 9 in [Creare workflow](across-how-to-create-workflows.md).  

* Notifica per il mittente

    Per i workflow di approvazione, aggiungere un passaggio di risposta del workflow per notificare al mittente quando la richiesta è stata approvata o rifiutata. Per ulteriori informazioni, vedere il passaggio 9 in [Creare workflow](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Vedere anche

[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)  
[Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)  
[Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Creare i workflow](across-how-to-create-workflows.md)  
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Utilizzare le code processi per pianificare le attività](admin-job-queues-schedule-tasks.md)  
[Configurare la posta elettronica](admin-how-setup-email.md)  
[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]