---
title: Impostazione delle notifiche del workflow | Microsoft Docs
description: "Molte risposte del flusso di lavoro riguardano la comunicazione, a un utente, di un evento che si è verificato e la relativa necessità di intervento. Ad esempio, in un passaggio del flusso di lavoro, l'evento potrebbe essere che l'utente 1 richiede l'approvazione di un nuovo record e la risposta riguarda l'invio di una notifica all'utente 2, cioè il responsabile dell'approvazione. Nel passaggio successivo del flusso di lavoro, l'evento potrebbe essere che l'utente 2 approva il record e la risposta riguarda l'invio di una notifica all'utente 3 per iniziare un'elaborazione correlata del record approvato. Per le fasi del workflow che riguardano l'approvazione, ogni notifica è collegata a un movimento di approvazione."
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
ms.openlocfilehash: 351c079df25516a83de42d5fa12954b25ba5e63e
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-workflow-notifications"></a>Impostazione delle notifiche del workflow
Molte risposte workflow riguardano la comunicazione, a un utente, di un evento che si è verificato e la relativa necessità di intervento. Ad esempio, in un passaggio del flusso di lavoro, l'evento potrebbe essere che l'utente 1 richiede l'approvazione di un nuovo record e la risposta riguarda l'invio di una notifica all'utente 2, cioè il responsabile dell'approvazione. Nel passaggio successivo del flusso di lavoro, l'evento potrebbe essere che l'utente 2 approva il record e la risposta riguarda l'invio di una notifica all'utente 3 per iniziare un'elaborazione correlata del record approvato. Per le fasi del workflow che riguardano l'approvazione, ogni notifica è collegata a un movimento di approvazione. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
>  La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta le notifiche come messaggi e-mail e note interne.  

> [!IMPORTANT]  
>  Tutte le notifiche del flusso di lavoro vengono inviate tramite una coda processi. Assicurarsi che la coda processi sia presente nella soluzione. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

È possibile impostare diversi aspetti delle notifiche del flusso di lavoro nelle aree seguenti:  

1.  Per i workflow di approvazione, è possibile impostare i destinatari delle notifiche del workflow compilando una riga nella finestra **Setup utente approvazione** per ogni utente che fa parte del workflow. Ad esempio, se l'utente 2 è specificato nel campo **ID resp. approvazione** nella riga per l'utente 1, la notifica di richiesta dell'approvazione viene inviata all'utente 1. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  
2.  È possibile impostare il momento e la modalità di ricezione delle notifiche del workflow da parte degli utenti compilando la finestra **Programmazione notifica**  per ogni utente del workflow. Per ulteriori informazioni, vedere [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  È possibile impostare il contenuto e il layout generali delle notifiche, incluse le notifiche relative alle risposte del workflow scadute, impostando i modelli di notifica nella finestra **Modelli di notifica**. È possibile utilizzare i modelli di default forniti con [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4.  È possibile impostare le regole e il contenuto specifici della notifica di un flusso di lavoro durante la creazione del flusso di lavoro in questione. Questa operazione può essere eseguita selezionando le opzioni nella finestra **Opzioni di risposta workflow** per la risposta workflow che rappresenta la notifica. Per ulteriori informazioni, vedere il passaggio 9 in [Creare workflow](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Vedi anche  
 [Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
 [Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)   
 [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Creare i workflow](across-how-to-create-workflows.md)   
 [Gestire i modelli di notifica](across-how-to-manage-notification-templates.md)   
 [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md)   
 [Impostare la posta elettronica](madeira-how-setup-email.md)   
 [Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Workflow](across-workflow.md)   

