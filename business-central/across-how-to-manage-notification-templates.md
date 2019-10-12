---
title: Come gestire i modelli di notifica | Microsoft Docs
description: Le notifiche vengono inviate agli utenti del flusso di lavoro per informarli sui passaggi che devono eseguire o sullo stato dei passaggi del flusso di lavoro. È possibile impostare gli utenti che ricevono la notifica e il momento in cui la ricevono configurando gli utenti di approvazione, la pianificazione della notifica agli utenti e le risposte del workflow interessato per definire il destinatario della notifica.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: across-how-to-specify-when-and-how-to-receive-notifications
ms.openlocfilehash: c195ffa8b798f13d92f78896f101a84b07728d08
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305358"
---
# <a name="manage-notification-templates"></a>Gestire i modelli di notifica
Le notifiche vengono inviate agli utenti del workflow per informarli sui passaggi che devono eseguire o sullo stato delle fasi del workflow. È possibile impostare gli utenti che ricevono la notifica e il momento in cui la ricevono configurando gli utenti di approvazione, la pianificazione della notifica agli utenti e le risposte del workflow interessato per definire il destinatario della notifica. Per ulteriori informazioni, vedere [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md).  

 Le notifiche si basano sui modelli che ne definiscono il contenuto e il layout. Il contenuto di un modello di notifica può essere esportato, modificato e, successivamente, importato nello stesso modello di notifica o in uno nuovo. Questa funzionalità è descritta nelle procedure seguenti.  

 Nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)] sono inclusi tre modelli di notifica per informare sulle richieste di approvazione, sui nuovi record e sulle richieste di approvazione scadute. I tre modelli di notifica predefiniti supportano **E-mail** e **Nota** come metodo di notifica. Per visualizzare il contenuto dei tre modelli di notifica, vedere la sezione "Contenuto dei modelli di notifica" in questo argomento.

## <a name="to-create-a-new-notification-template"></a>Per creare un nuovo modello di notifica  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modelli di notifica** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Modelli di notifica** scegliere l'azione **Nuovo**.  
3.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Codice**|Identificare il modello di notifica.|  
    |**Description**|Descrivere il modello di notifica.|  
    |**Metodo di notifica**|Specificare se la notifica viene inviata come messaggio di posta elettronica o nota.|  
    |**Tipo**|Specificare il processo commerciale per cui sarà utilizzata la notifica.<br /><br /> Selezionare uno dei tipi seguenti:<br /><br /> -   **Approvazione** specifica che il modello è utilizzato per informare gli utenti durante i workflow di approvazione.<br />-   **Nuovo record** specifica che il modello viene utilizzato per notificare ai responsabili dell'approvazione il momento in cui un nuovo record, ad esempio una scheda cliente, deve essere approvato.<br />-   **Scaduto** specifica che il modello è utilizzato per notificare agli utenti le richieste di approvazione scadute.|  
    |**Default**|Specificare se il modello di notifica sarà utilizzato per impostazione predefinita.|  

## <a name="to-modify-a-notification-template"></a>Per modificare un modello di notifica  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modelli di notifica** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Modelli di notifica** selezionare il modello di notifica che si desidera modificare.  
3.  Scegliere l'azione **Esporta contenuto modello**.  
4.  Nella pagina **Esporta file** scegliere il pulsante **Salva**, quindi denominare e salvare il file HTML in un percorso appropriato.  
5.  Fare clic con il pulsante destro del mouse sul file, selezionare **Apri con**, quindi scegliere il programma appropriato.  

    > [!NOTE]  
    >  Il contenuto dei modelli di notifica di tipo messaggio di posta elettronica è in formato HTML. Il contenuto dei modelli di notifica di tipo nota è in formato TXT.  
6.  Modificare il contenuto del modello di notifica aggiungendo, modificando o rimuovendo le variabili dei parametri per definire il contenuto desiderato, quindi salvarlo. Per ulteriori informazioni, vedere la sezione "Contenuto dei modelli di notifica".  

    Continuare a importare il contenuto modificato nello stesso modello di notifica o in uno nuovo.  
7.  Per modificare il modello di notifica esportato, nella pagina **Modelli di notifica** selezionare il modello scelto nel passaggio 2.  

    In alternativa, per importare il contenuto del modello modificato in un nuovo modello di notifica, attenersi alla procedura "Per creare un nuovo modello di notifica" e, successivamente, selezionare il nuovo modello di notifica.  
8.  Scegliere l'azione **Importa contenuto modello**.  
9. Se si sta modificando un modello di notifica esistente, scegliere il pulsante **Sì** nel messaggio relativo alla sovrascrittura del modello esistente.  
10. Nella pagina **Seleziona un file da importare** scegliere il file HTML modificato nel passaggio 6, quindi selezionare il pulsante **Apri**.  

Il modello di notifica nuovo o esistente nella pagina **Modelli di notifica** è ora aggiornato con il contenuto modificato.  

### <a name="content-of-the-notification-templates"></a>Contenuto dei modelli di notifica  
Nei tre tipi di modelli di notifica, **Nuovo record**, **Approvazione** e **Scaduto** sono presenti contenuti diversi.  

I valori dei parametri vengono inseriti automaticamente nelle notifiche in base al tipo del modello di notifica.  

#### <a name="new-record"></a>Nuovo record  
 ![NAV&#95;notification&#95;template&#95;new&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Approvazione  
 ![NAV&#95;notification&#95;template&#95;approval&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Scaduto  
 ![NAV&#95;notification&#95;overdue&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Vedi anche  
 [Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)   
 [Impostare la posta elettronica](admin-how-setup-email.md)   
 [Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)   
 [Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)   
 [Creare i workflow](across-how-to-create-workflows.md)   
 [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md)   
 [Workflow](across-workflow.md)   
