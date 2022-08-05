---
title: Impostazione delle notifiche del flusso di lavoro
description: Questo articolo spiega come impostare le notifiche del flusso di lavoro per avvisare un utente che si è verificato un evento a cui deve reagire con la risposta del flusso di lavoro obbligatoria.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 99c08769429eef51a1d52e142d455ccd227781c7
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130012"
---
# <a name="workflow-notifications"></a>Notifiche del workflow

Impostare i workflow per notificare automaticamente agli utenti quando è richiesta la loro attenzione per un passaggio del workflow. Molte risposte del workflow riguardano la comunicazione, a un utente, di un evento che si è verificato e la relativa necessità di intervento.

Ad esempio, è possibile impostare che l'utente 2, l'utente responsabile dell'approvazione, riceva una notifica ogni volta che l'utente 1 richiede l'approvazione per un nuovo record. Nella fase successiva del flusso di lavoro, l'utente 3 riceve una notifica dopo che l'utente 2 ha approvato il record per avviare un'elaborazione correlata del record. Con le fasi del workflow di approvazione, ogni notifica è collegata a un movimento di approvazione. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
> La versione predefinita di [!INCLUDE[prod_short](includes/prod_short.md)] supporta le notifiche come messaggi e-mail e note interne.  

> [!IMPORTANT]  
> Tutte le notifiche del workflow vengono inviate tramite una coda processi. Assicurarsi che la coda processi nella propria installazione sia impostata in modo da gestire le notifiche del workflow e che la casella di controllo **Avvia automaticamente da server** sia selezionata. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Impostazione delle notifiche

È possibile impostare diversi aspetti delle notifiche del workflow nelle aree seguenti:  

* Notifica del responsabile dell'approvazione

    Per i workflow di approvazione, è possibile impostare i destinatari delle notifiche del workflow compilando una riga nella pagina **Setup utente approvazione** per ogni utente che fa parte del workflow.  

    Ad esempio, se l'utente 2 è specificato nel campo **ID resp. approvazione** nella riga per l'utente 1, la notifica di richiesta dell'approvazione viene inviata all'utente 2. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  
* Programmazione delle notifiche

    È possibile impostare il momento e la modalità di ricezione delle notifiche del workflow da parte degli utenti compilando la pagina **Programmazione notifica** per ogni utente del workflow. Per ulteriori informazioni, vedere [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Personalizzazione delle notifiche di posta elettronica

    È possibile se lo desideri personalizzare il contenuto della notifica e-mail modificando Report 1320, E-mail di notifica. Per ulteriori informazioni, vedere [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Se si desidera utilizzare la posta elettronica come metodo di notifica, è necessario impostarla sia per il mittente che per il destinatario in [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Configurare la posta elettronica](admin-how-setup-email.md).

* Opzioni di risposta

    È possibile impostare le regole e il contenuto specifici della notifica di un workflow durante la creazione del workflow in questione. Seleziona le opzioni di personalizzazione nella pagina **Risposte workflow** per la risposta workflow che rappresenta la notifica. Per ulteriori informazioni, vedi il passaggio 9 in [Creare workflow](across-how-to-create-workflows.md#to-create-a-workflow).  

* Notifica per il mittente

    Per i workflow di approvazione, aggiungere un passaggio di risposta del workflow per notificare al mittente quando la richiesta è stata approvata o rifiutata. Per ulteriori informazioni, vedi il passaggio 9 in [Creare workflow](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/create-workflows/)

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