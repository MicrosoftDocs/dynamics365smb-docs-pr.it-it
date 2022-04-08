---
title: Impostare i flussi di lavoro ( video)
description: Imposta flussi di lavoro, utenti del flusso di lavoro e utenti di approvazione per connettere le attività di sistema dei processi aziendali eseguite da questi diversi utenti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: c07a3cfc9807ddcb78a97dc342013ff6e498fee7
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518443"
---
# <a name="set-up-workflows"></a>Impostare i flussi di lavoro

È possibile impostare e utilizzare i flussi di lavoro che collegano task di processi aziendali eseguiti da utenti diversi. I task di sistema, ad esempio la registrazione automatica, possono essere inclusi come passaggi nei flussi di lavoro e preceduti o seguiti da task degli utenti. La richiesta e la concessione dell'approvazione per creare nuovi record sono passaggi tipici del flusso di lavoro. Per ulteriori informazioni, vedi [Utilizzare i flussi di lavoro](across-use-workflows.md).  

 Prima di poter iniziare a utilizzare i flussi di lavoro, è necessario impostare gli utenti del workflow e gli utenti dell'approvazione, specificare la modalità di ricezione delle notifiche sui passaggi del workflow e successivamente creare i flussi di lavoro, potenzialmente preceduti dalla personalizzazione del codice.  

 Nella pagina **Workflow** creare un workflow elencando le fasi interessate nelle righe. Ogni fase consiste in un evento del flusso di lavoro, moderato dalle condizioni di evento, e in una risposta del flusso di lavoro, moderata dalle opzioni di risposta. È possibile definire le fasi workflow compilando i campi delle righe del workflow in base a elenchi fissi di valori di evento e di risposta che rappresentano gli scenari supportati dal codice dell'applicazione.  

 Se uno scenario aziendale richiede un evento o una risposta del workflow non supportati, un partner Microsoft deve implementarli tramite il codice o e possibile impostare un workflow utilizzando Power Automate. Per ulteriori informazioni, vedi rispettivamente [Usare [!INCLUDE[prod_short](includes/prod_short.md)] in un flusso di lavoro automatizzato](across-how-use-financials-data-source-flow.md) o [Eventi in AL](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al) nella guida per sviluppatori.

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.  

|**Task**|**Vedere**|  
|------------|-------------|  
|Impostare gli utenti e i gruppi di utenti del workflow.|[Impostare gli utenti del workflow](across-how-to-set-up-workflow-users.md)|  
|Impostare gli utenti del workflow che partecipano ai flussi di approvazione.|[Impostare gli utenti per l'approvazione](across-how-to-set-up-approval-users.md)|  
|Specificare in che modo gli utenti ricevono le notifiche dei passaggi del workflow, incluse le richieste di approvazione.|[Impostazione delle notifiche del workflow](across-setting-up-workflow-notifications.md)|  
|Specificare se gli utenti sono avvertiti mediante e-mail o nota e la frequenza alla quale le notifiche vengono inviate.|[Specificare come e quando ricevere le notifiche](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Personalizzare il contenuto delle notifiche e-mail modificando Report 1320, E-mail di notifica.|[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)|  
|Impostare un server SMTP per consentire la comunicazione e-mail in entrata e in uscita di [!INCLUDE[prod_short](includes/prod_short.md)]|[Configurare la posta elettronica](admin-how-setup-email.md)|
|Specificare i diversi passaggi di un workflow in base al collegamento tra gli eventi del workflow e le risposte del workflow.|[Creare i workflow](across-how-to-create-workflows.md)|  
|Usare i modelli di flussi di lavoro per creare nuovi flussi di lavoro.|[Creare workflow da modelli di workflow](across-how-to-create-workflows-from-workflow-templates.md)|  
|Condividere workflow con altri database [!INCLUDE[prod_short](includes/prod_short.md)].|[Importare ed esportare workflow](across-how-to-export-and-import-workflows.md)|  
|Come impostare un workflow per approvare documenti di vendita seguendo una procedura end-to-end.|[Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Esempio di workflow di approvazione
Questo video mostra come impostare un workflow che chiede a qualcuno di richiedere l'approvazione di qualcun altro prima di poter modificare le informazioni su un cliente esistente o creare un nuovo cliente.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Vedere anche  
 [Utilizzare i flussi di lavoro](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
 [Procedura dettagliata: Impostazione e utilizzo di un workflow di approvazione di acquisto](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Utilizzare Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]