---
title: Impostazione delle notifiche del workflow | Microsoft Docs
description: Molte risposte del flusso di lavoro riguardano la comunicazione, a un utente, di un evento che si è verificato e la relativa necessità di intervento. Ad esempio, in un passaggio del flusso di lavoro, l'evento potrebbe essere che l'utente 1 richiede l'approvazione di un nuovo record e la risposta riguarda l'invio di una notifica all'utente 2, cioè il responsabile dell'approvazione. Nel passaggio successivo del flusso di lavoro, l'evento potrebbe essere che l'utente 2 approva il record e la risposta riguarda l'invio di una notifica all'utente 3 per iniziare un'elaborazione correlata del record approvato. Per le fasi del workflow che riguardano l'approvazione, ogni notifica è collegata a un movimento di approvazione.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/08/2018
ms.author: sgroespe
ms.openlocfilehash: 53b063598cf21ca5b5de72d953995b48a17d64a2
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802255"
---
# <a name="setting-up-workflow-notifications"></a>Impostazione delle notifiche del workflow
Molte risposte workflow riguardano la comunicazione, a un utente, di un evento che si è verificato e la relativa necessità di intervento. Ad esempio, in un passaggio del flusso di lavoro, l'evento potrebbe essere che l'utente 1 richiede l'approvazione di un nuovo record e la risposta riguarda l'invio di una notifica all'utente 2, cioè il responsabile dell'approvazione. Nel passaggio successivo del flusso di lavoro, l'evento potrebbe essere che l'utente 2 approva il record e la risposta riguarda l'invio di una notifica all'utente 3 per iniziare un'elaborazione correlata del record approvato. Per le fasi del workflow che riguardano l'approvazione, ogni notifica è collegata a un movimento di approvazione. Per ulteriori informazioni, vedere [Workflow](across-workflow.md).  

> [!NOTE]  
>  La versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta le notifiche come messaggi e-mail e note interne.  

> [!IMPORTANT]  
>  Tutte le notifiche del flusso di lavoro vengono inviate tramite una coda processi. Assicurarsi che la coda processi nella propria installazione sia impostata in modo da gestire le notifiche del workflow e che la casella di controllo **Avvia automaticamente da server** sia selezionata. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

È possibile impostare diversi aspetti delle notifiche del flusso di lavoro nelle aree seguenti:  

1.  Per i workflow di approvazione, è possibile impostare i destinatari delle notifiche del workflow compilando una riga nella pagina **Setup utente approvazione** per ogni utente che fa parte del workflow. Ad esempio, se l'utente 2 è specificato nel campo **ID resp. approvazione** nella riga per l'utente 1, la notifica di richiesta dell'approvazione viene inviata all'utente 1. Per ulteriori informazioni, vedere [Impostare utenti per l'approvazione](across-how-to-set-up-approval-users.md).  
2.  È possibile impostare il momento e la modalità di ricezione delle notifiche del workflow da parte degli utenti compilando la pagina **Programmazione notifica** per ogni utente del workflow. Per ulteriori informazioni, vedere [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Se lo si desidera, è possibile personalizzare il contenuto della notifica e-mail modificando Report 1320, E-mail di notifica. Per ulteriori informazioni, vedere [Creare e modificare un layout di documento o report personalizzato](ui-how-create-custom-report-layout.md).  
4.  È possibile impostare le regole e il contenuto specifici della notifica di un flusso di lavoro durante la creazione del flusso di lavoro in questione. Questa operazione può essere eseguita selezionando le opzioni nella pagina **Opzioni di risposta workflow** per la risposta workflow che rappresenta la notifica. Per ulteriori informazioni, vedere il passaggio 9 in [Creare workflow](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Vedi anche  
 [Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
 [Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)   
 [Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Creare i workflow](across-how-to-create-workflows.md)   
 [Creare e modificare un layout di documento o report personalizzato](ui-how-create-custom-report-layout.md)   
 [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md)   
 [Impostare la posta elettronica](admin-how-setup-email.md)   
 [Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Workflow](across-workflow.md)   
